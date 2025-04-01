# Blackbird environment templates

This Helm chart provisions the necessary components for running a Blackbird environment in a Kubernetes cluster, including Ambassador Edge Stack (AES), Telepresence, and optional cluster-wide security policies.

## Configuration

All configuration can be customized via the `values.yaml` file.


| Key                   | Description                                       | Default                        |
|------------------------|---------------------------------------------------|--------------------------------|
| `AES4Version`          | The version of Ambassador Edge Stack to deploy    | `"v4.0.0-preview.2.dev.1"`     |
| `AmbassadorNamespace` | Namespace where Ambassador is deployed             | `"ambassador"`                |
| `ServicesNamespace`   | Namespace for Blackbird's services                 | `"blackbird-services"`        |
| `TelepresenceVersion` | Telepresence version to deploy                     | `"2.20.1-test.0"`             |

### Labels

These labels are applied to all chart managed resources:

```yaml
Labels:
  app.kubernetes.io/managed-by: blackbird
