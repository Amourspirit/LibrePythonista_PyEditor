# Developer Readme

## Building Flatpak

```sh
flatpak-builder build --verbose --force-clean com.github.amourspirit.librepythonista.PyEditor.yml
```

## Installing

```sh
flatpak-builder --force-clean build-dir com.github.amourspirit.librepythonista.PyEditor.yml --install --user
```

## Uninstalling

```sh
flatpak uninstall com.github.amourspirit.librepythonista.PyEditor
```

## PIP

Generating pip requirements.

The `requirements.txt` file contains the requirements for this flatpak app. Getting the requirements for the manifest file can be automated.
Running one of these commands will generate a `python3-requirements.yaml` file in the project root directory. The contents can be copied and pasted into the manifest file.

### Virtual Environment

```sh
flatpak_pip_generator --runtime='org.freedesktop.Sdk//24.08' librepythonista_python_editor --yaml
```

### Using UV

```sh
uv run flatpak_pip_generator --runtime='org.freedesktop.Sdk//24.08' --requirements-file='requirements.txt'  --yaml
```

## Other Notes

Make sure chmod +x `cell_edit` file.

## Other Resources

Flatpak Documentation [Manifest](https://docs.flatpak.org/en/latest/manifests.html)