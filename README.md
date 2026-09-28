[![Go Report Card](https://goreportcard.com/badge/github.com/hostinger/fireactions)](https://goreportcard.com/report/github.com/hostinger/fireactions)

![Banner](docs/img/banner_violet.png)

Fireactions is an orchestrator for GitHub runners. BYOM (Bring Your Own Metal) and run self-hosted GitHub runners in ephemeral, fast and secure [Firecracker](https://firecracker-microvm.github.io/) based virtual machines.

> [!IMPORTANT]
> There's been multiple improvements with a lot of breaking changes. The current stable version is **v2.0.0**. Please use this version for production environments.

<!--
https://excalidraw.com/#json=GrJMj6LLYt39mgC0me7Di,C65TV9FhicnxNKgPeRhi3A
sequenceDiagram
    autonumber
    participant Fireactions
    participant Configuration file (YAML)
    participant Pool(s)
    participant Firecracker VM with GitHub runner
    participant GitHub

    Fireactions->>Configuration file (YAML): Load pools
    Fireactions->>Pool(s): Start pool(s)
    loop Ensure min amount of GitHub runners every 1s
        Pool(s)->>GitHub: Create JIT GitHub runner token
        Pool(s)->>Firecracker VM with GitHub runner: Start Firecracker VM
        Firecracker VM with GitHub runner->>GitHub: Run GitHub workflow job
        Firecracker VM with GitHub runner->>Pool(s): Exit (on workflow job finish)
    end
    GitHub->>Fireactions: Scale pool on workflow_job event
-->
![Architecture](docs/img/architecture.png)

Several key features:

- **Scalable**

  Pool based scaling approach. Fireactions always ensures the minimum amount of GitHub runners in the pool.

- **Ephemeral**

  Each virtual machine is created from scratch and destroyed after the job is finished, no state is preserved between jobs, just like with GitHub hosted runners.

- **Customizable**

  Define job labels and customize virtual machine resources to fit Your needs.

## Quickstart

```bash
$ fireactions --help
BYOM (Bring Your Own Metal) and run self-hosted GitHub runners in ephemeral, fast and secure Firecracker based virtual machines.

Usage:
  fireactions [command]

Main application commands:
  server      Starts the server
  agent       Starts the agent and GitHub Actions runner inside the VM

Pool management commands:
  pools       Manage pools

Machine management commands:
  ps          List all running machines across all pools
  login       SSH into a running VM as root user
  logs        Stream logs from the fireactions-agent service inside a machine

Image management commands:
  image       Manage images

Additional Commands:
  version     Show version information
  help        Help about any command
  completion  Generate the autocompletion script for the specified shell

Flags:
  -h, --help      help for fireactions
  -v, --version   version for fireactions

Use "fireactions [command] --help" for more information about a command.
```

See the [Guide](https://fireactions.io/latest/) for installation and configuration instructions.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for more information on how to contribute to Fireactions.
```
 def rotation_matrix(theta):
    c, s = np.cos(theta), np.sin(theta)
    return np.array([[c, -s],
                     [s,  c]])

theta = np.pi / 4   # 45 degrees
R = rotation_matrix(theta)

# Apply to a vector
v = np.array([1.0, 0.0])
v_rotated = R @ v
print("Rotated vector:", v_rotated)# Computational basis
ket0 = np.array([1, 0], dtype=complex)
ket1 = np.array([0, 1], dtype=complex)

# Hadamard action
plus  = H @ ket0          # |+>
minus = H @ ket1          # |->

# X gate action
print("X|0> =", X @ ket0)   # should be |1>
print("X|1> =", X @ ket1)   # should be |0>def rc_current(t, E, R, tau):
    """i(t) = (E/R) * (1 - exp(-t/tau))"""
    return (E / R) * (1 - np.exp(-t / tau))

t = np.linspace(0, 5*0.01, 500)
i = rc_current(t, E=12, R=4.7, tau=0.01)# From one of your pages: X = (Y - 3) / 2
def final_result(Y):
    return (Y - 3) / 2

# Infinite series fragment ∑ X_n / n!
from math import factorial

def series_approx(X, terms=20):
    return sum(X**n / factorial(n) for n in range(terms))

// Rough translation of the control-flow notes
function applicationX(options) {
  // replace = option
  let value = options.replace || null;

  if (!value) {
    // ! # ! # end if  style guard
    return null;
  }

  // trusted-click-element + transform idea
  const transformed = U_transform(value);
  return transformed;
}
options.replace.
