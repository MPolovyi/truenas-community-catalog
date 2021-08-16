# handbrake

![Version: 6.6.0](https://img.shields.io/badge/Version-6.6.0-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: auto](https://img.shields.io/badge/AppVersion-auto-informational?style=flat-square)

HandBrake is a tool for converting video from nearly any format to a selection of modern, widely supported codecs.

**Homepage:** <https://github.com/truecharts/apps/tree/master/charts/stable/handbrake>

## Maintainers

| Name | Email | Url |
| ---- | ------ | --- |
| TrueCharts | info@truecharts.org | truecharts.org |
| stavros-k | stavros-k@users.noreply.github.com | truecharts.org |

## Source Code

* <https://github.com/jlesage/docker-handbrake>
* <https://hub.docker.com/r/jlesage/handbrake/>
* <https://handbrake.fr/>

## Requirements

Kubernetes: `>=1.16.0-0`

| Repository | Name | Version |
|------------|------|---------|
| https://truecharts.org/ | common | 6.8.0 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env.AUTOMATED_CONVERSION_FORMAT | string | `"mp4"` |  |
| env.AUTOMATED_CONVERSION_KEEP_SOURCE | string | `"1"` |  |
| env.AUTOMATED_CONVERSION_NON_VIDEO_FILE_ACTION | string | `"ignore"` |  |
| env.AUTOMATED_CONVERSION_PRESET | string | `"General/Very Fast 1080p30"` |  |
| env.CLEAN_TMP_DIR | string | `"1"` |  |
| env.DISPLAY_HEIGHT | string | `"768"` |  |
| env.DISPLAY_WIDTH | string | `"1280"` |  |
| env.KEEP_APP_RUNNING | string | `"0"` |  |
| env.PGID | string | `"568"` |  |
| env.PUID | string | `"568"` |  |
| env.SECURE_CONNECTION | string | `"0"` |  |
| env.VNC_PASSWORD | string | `nil` |  |
| envTpl.GROUP_ID | string | `"{{ .Values.env.PGID }}"` |  |
| envTpl.USER_ID | string | `"{{ .Values.env.PUID }}"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"jlesage/handbrake"` |  |
| image.tag | string | `"v1.24.0"` |  |
| persistence.config.enabled | bool | `true` |  |
| persistence.config.mountPath | string | `"/config"` |  |
| persistence.config.type | string | `"emptyDir"` |  |
| service.main.ports.main.port | int | `5800` |  |
| service.vnc.enabled | bool | `true` |  |
| service.vnc.ports.vnc.enabled | bool | `true` |  |
| service.vnc.ports.vnc.port | int | `5900` |  |
| service.vnc.ports.vnc.protocol | string | `"TCP"` |  |
| service.vnc.type | string | `"ClusterIP"` |  |
| strategy.type | string | `"Recreate"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.5.0](https://github.com/norwoodj/helm-docs/releases/v1.5.0)