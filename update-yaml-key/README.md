# Update YAML Key

Sweet and simple.  It updates a YAML key to the given value.

Generated documentation is in the [docs/](./docs) directory.

## Usage

In this example pipeline step I have defined the variables `DEV_VALUES_FILE`,
   `YAML_KEY`, and `IMAGE_NAME`.  Provided below are the Helm Chart
   and Codefresh Steps YAML.

Additionally, the step will track the current value prior to updating
via `CURRENT_VALUE`, and the value after updating via `UPDATED_VALUE` in
the step outputs.

This will allow you to avoid steps that aren't required when the value
did not change.

### Variable Values

- `YAML_KEY` is `.image.tag`
- `DEV_VALUES_FILE` is `my-chart/values/cluster-name/values.dev.yaml`
- `IMAGE_NAME` is generally `${{CF_BRANCH}}` or `${{CF_TAG}}`

### Codefresh Step YAML

This will update `YAML_KEY` in `DEV_VALUES_FILE` to `IMAGE_NAME`
during the **chart** stage in the pipeline.

```yaml
steps:
  # Promote this image to dev
  update_dev_chart_tag:
    title: Update Image Tag for Dev Chart
    type: r35/update_yaml_key
    stage: chart
    arguments:
      working_directory: "helm-charts/stable/${{CHART_DIR}}"
      VALUES_FILE: '${{DEV_VALUES_FILE}}'
      YAML_KEY: '${{YAML_KEY}}'
      NEW_VALUE: '${{IMAGE_NAME}}'
```

### Helm Chart Values File

```yaml
config:
  FOO: bar
image:
  repository: ghcr.io/r35krag0th/spiffy-project
  tag: "1.2.3"
```

## Install/Update

You will need to bump the version prior to using the following
command otherwise you'll get an error, because versions are
immutable.

If you want to publish this in your own CodeFresh account then you'll also
need to adjust the `r35/` on the `.metadata.name` in `update-yaml-key-step.yml`.

```shell
$ codefresh create step-type -f ./update-yaml-key-step.yml
OK
```

