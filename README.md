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

://api.ip2location.io/?ip=127.0.0.1')

{
    "ip": "127.0.0.1",
    "country_code": "-",
    "country_name": "-",
    "region_name": "-",
    "district": "-",
    "city_name": "-",
    "latitude": null,
    "longitude": null,
    "zip_code": "-",
    "time_zone": "-",
    "asn": "-",
    "as": "-",
    "as_info": {
        "as_number": "-",
        "as_name": "-",
        "as_domain": "-",
        "as_usage_type": "-",
        "as_cidr": "-"
    },
    "isp": "Loopback",
    "domain": "-",
    "net_speed": "-",
    "idd_code": "-",
    "area_code": "-",
    "weather_station_code": "-",
    "weather_station_name": "-",
    "mcc": "-",
    "mnc": "-",
    "mobile_brand": "-",
    "elevation": 0,
    "usage_type": "RSV",
    "address_type": "Unicast",
    "ads_category": "-",
    "ads_category_name": null,
    "continent": {
        "hemisphere": null,
        "translation": {
            "lang": "en",
            "value": null
        }
    },
    "country": {
        "name": "-",
        "alpha3_code": null,
        "numeric_code": null,
        "demonym": null,
        "flag": null,
        "capital": null,
        "total_area": 0,
        "population": 0,
        "currency": {
            "code": null,
            "name": null,
            "symbol": null
        },
        "language": {
            "code": null,
            "name": null
        },
        "tld": null,
        "translation": {
            "lang": "en",
            "value": null
        }
    },
    "region": {
        "name": "-",
        "code": null,
        "translation": {
            "lang": "en",
            "value": null
        }
    },
    "city": {
        "name": "-",
        "translation": {
            "lang": "en",
            "value": null
        }
    },
    "time_zone_info": {
        "olson": null,
        "current_time": "2026-10-02T11:14:08+08:00",
        "gmt_offset": 28800,
        "is_dst": false,
        "dst_start_date": null,
        "dst_end_date": null,
        "sunrise": "13:47",
        "sunset": "01:53"
    },
    "geotargeting": {
        "metro": null
    },
    "is_proxy": false,
    "fraud_score": 0,
    "proxy": {
        "last_seen": 0,
        "proxy_type": "-",
        "threat": "-",
        "provider": "-",
        "is_vpn": false,
        "is_tor": false,
        "is_data_center": false,
        "is_public_proxy": false,
        "is_web_proxy": false,
        "is_web_crawler": false,
        "is_ai_crawler": false,
        "is_residential_proxy": false,
        "is_consumer_privacy_network": false,
        "is_enterprise_private_network": false,
        "is_spammer": false,
        "is_scanner": false,
        "is_botnet": false,
        "is_bogon": false
    }
}
 NETORGFT20489500.onmicrosoft.comNETORGFT20489500.onmicrosoft.comHTTP/2 200 
expires: Thu, 19 Nov 1981 08:52:00 GMT
cache-control: no-store, no-cache, must-revalidate
pragma: no-cache
link: <https://yhwh.com/wp-json/>; rel="https://api.w.org/", <https://yhwh.com/wp-json/wp/v2/pages/6>; rel="alternate"; title="JSON"; type="application/json", <https://yhwh.com/>; rel=shortlink
set-cookie: PHPSESSID=32771a9e1a01996659da3a9f07909a56; path=/
vary: Accept-Encoding
content-type: text/html; charset=UTF-8
date: Fri, 02 Oct 2026 03:07:17 GMT
server: yhwh.com('https://api.ip2location.io/?ip=100.0.0.1')

{
    "ip": "100.0.0.1",
    "country_code": "US",
    "country_name": "United States of America",
    "region_name": "Massachusetts",
    "district": "Suffolk County",
    "city_name": "Boston",
    "latitude": 42.35848,
    "longitude": -71.06007,
    "zip_code": "02117",
    "time_zone": "-04:00",
    "asn": "701",
    "as": "Verizon Business",
    "as_info": {
        "as_number": "701",
        "as_name": "Verizon Business",
        "as_domain": "verizonenterprise.com",
        "as_usage_type": "ISP",
        "as_cidr": "100.0.0.0/16"
    },
    "isp": "Verizon Business",
    "domain": "verizonenterprise.com",
    "net_speed": "DSL",
    "idd_code": "1",
    "area_code": "617",
    "weather_station_code": "USMA0046",
    "weather_station_name": "Boston",
    "mcc": "311",
    "mnc": "480",
    "mobile_brand": "Verizon",
    "elevation": 15,
    "usage_type": "ISP",
    "address_type": "Unicast",
    "ads_category": "419",
    "ads_category_name": "Internet Service Providers",
    "continent": {
        "name": "North America",
        "code": "NA",
        "hemisphere": [
            "north",
            "west"
        ],
        "translation": {
            "lang": "en",
            "value": "North America"
        }
    },
    "country": {
        "name": "United States of America",
        "alpha3_code": "USA",
        "numeric_code": 840,
        "demonym": "Americans",
        "flag": "https://cdn.ip2location.io/assets/img/flags/us.png",
        "capital": "Washington, D.C.",
        "total_area": 9826675,
        "population": 339665118,
        "currency": {
            "code": "USD",
            "name": "United States Dollar",
            "symbol": "$"
        },
        "language": {
            "code": "EN",
            "name": "English"
        },
        "tld": "us",
        "translation": {
            "lang": "en",
            "value": "United States of America"
        }
    },
    "region": {
        "name": "Massachusetts",
        "code": "US-MA",
        "translation": {
            "lang": "en",
            "value": "Massachusetts"
        }
    },
    "city": {
        "name": "Boston",
        "translation": {
            "lang": "en",
            "value": "Boston"
        }
    },
    "time_zone_info": {
        "olson": "America/New_York",
        "current_time": "2026-10-01T23:14:48-04:00",
        "gmt_offset": -14400,
        "is_dst": true,
        "abbreviation": "EST",
        "dst_start_date": "2026-03-08",
        "dst_end_date": "2026-11-01",
        "sunrise": "06:42",
        "sunset": "18:27"
    },
    "geotargeting": {
        "metro": "506"
    },
    "is_proxy": false,
    "fraud_score": 0,
    "proxy": {
        "last_seen": 0,
        "proxy_type": "-",
        "threat": "-",
        "provider": "-",
        "is_vpn": false,
        "is_tor": false,
        "is_data_center": false,
        "is_public_proxy": false,
        "is_web_proxy": false,
        "is_web_crawler": false,
        "is_ai_crawler": false,
        "is_residential_proxy": false,
        "is_consumer_privacy_network": false,
        "is_enterprise_private_network": false,
        "is_spammer": false,
        "is_scanner": false,
        "is_botnet": false,
        "is_bogon": false
    }
}
 ns65.domaincontrol.com. 

dns.jomax.net. 2026082100 28800 7200 604800 600

v=spf1 include:secureserver.net

 -all127.255.255.255ns65.domaincontrol.com. dns.jomax.net. 2026082100 28800 7200 604800 600

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
