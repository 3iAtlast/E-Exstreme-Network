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

bash
$ fireactions --help
BYOM (Bring Your Own Metal) and run self-hosted GitHub runners in ephemeral, fast and secure Firecracker based virtual machines.

#** ∆Y={0:ic<i|AL•(√P-√p(i):i/≤ic<iu
#** ∆L•√(p(iu)-√p(i|)ic>icu/ic<iμ
** ∆X•∆L•√(1/p(i){∆L•(⅛-√p(icu)
#** 0 crossing Tx.6.2.3
#** fo:=fg-fo(66.26),to(i):={+ic≥i
                        {oic<i(6.25

# = f(2)=2²-5×2+6=0&
 
# = f(4(=3²-5×3+6=0;

# = f(x)=x³+3x²-6x-8/4;

# = f3=x³+x²-6x-8÷4;

### Research.Gate.net
(seed),[XLS]_Represents paid>10,000-SSA Aegon],public Safty assets management

  ## Iteland ##

* X=f14.8176
* solution {x=0}
* solution {f14=1/8176}
* solution in Decimal {f14=0.0001223091977,
* dirivatives both sides respect 0=8176X
* differentiate both sides X1=8176f14
* integrating both sides respectto F14 
* f14x=4088f14²x;

** {3xq+4y+5z=6}
** {2x+3y+4z=5}
** {x+2y+3z=4}
** {2=4-x2y/3}

× √5.√2.4/2√5x

× √5.√2.2

× 5.x/✓√x/x.2

× vertical asymptotes: x=0
× horizontal asymptotes: y=0


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

### <!doctype html3>

## <html3>
## <tr>
## <td>
## <th>

### IncomeQ3>Defined By $A$3 Absolute Cell Reference "enter",123".

### In Cell May Automatically Change To"$123.00".

### Press Tab Or Enter Or Click Outside The Cell.
Active Cell Is Formatted For Data Or A Text.
Text"1/2/3" 
### May Change To "01/02/2003".
Cell A20 May Contain
### A Formula That Produces The Result Of The Summation Of Cells A1-A25.
Cell 5 May Contain 
### A Formula That Averages All The Numbers In The B Column.
### AAAA.
# AAC videos "live" Or "on-the-fly".
Often Use H.264,HEVC,or VP9.
[#page:one#]
