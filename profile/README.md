<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/lockup-horizontal-dark.svg">
    <img alt="OpenCTEM" src="assets/lockup-horizontal-light.svg" width="380">
  </picture>
</p>

<h3 align="center">Open-source Continuous Threat Exposure Management</h3>
<p align="center"><em>Nền tảng mã nguồn mở quản lý phơi nhiễm mối đe doạ liên tục</em></p>

<p align="center">
  <a href="https://openctem.io">openctem.io</a>
  &nbsp;&nbsp;|&nbsp;&nbsp;
  <a href="https://docs.openctem.io">Documentation</a>
  &nbsp;&nbsp;|&nbsp;&nbsp;
  <a href="https://github.com/openctemio/openctem">Get started</a>
</p>

---

**OpenCTEM** runs the whole CTEM loop in one self-hostable platform: scope what matters, discover your attack surface, prioritise by real exploitability, validate with retests and pentest campaigns, and mobilise fixes until they are verified closed. It never auto-closes a finding without evidence, signs every job it sends to a sensor, and keeps each tenant's data isolated.

**OpenCTEM** chạy trọn vòng lặp CTEM trên một nền tảng tự cài được: xác định phạm vi, phát hiện bề mặt tấn công, xếp ưu tiên theo khả năng khai thác thực tế, xác minh bằng kiểm thử lại và pentest, rồi theo dõi việc khắc phục cho tới khi được xác nhận đã đóng.

| Scope | Discover | Prioritise | Validate | Mobilise |
|---|---|---|---|---|
| Assets, owners, scope rules and approvals | EASM, cloud, code and network inventory | KEV, EPSS, reachability, attack paths | Retests, pentest campaigns, evidence | Grouped fixes, two-way tickets, verified close |

### Repositories

| | Repository | What it is |
|---|---|---|
| Platform | [openctem](https://github.com/openctemio/openctem) | Go API and Next.js web console, all-in-one image |
| Sensors | [sensor](https://github.com/openctemio/sensor) | Scanner runtime that runs close to your assets |
| | [sdk-go](https://github.com/openctemio/sdk-go) | Go SDK, sensor kit and scanner integrations |
| | [connector-tenable](https://github.com/openctemio/connector-tenable) | Tenable Security Center connector |
| | [ci](https://github.com/openctemio/ci) | CI/CD scanner images and pipeline integrations |
| Data | [ctis](https://github.com/openctemio/ctis) | CTEM Ingest Schema: the open format for assets, findings and SBOMs |
| | [vulnfeed](https://github.com/openctemio/vulnfeed) | Signed, normalised vulnerability feed |
| | [programfeed](https://github.com/openctemio/programfeed) | Signed feed of public disclosure programs |
| | [sast-rules](https://github.com/openctemio/sast-rules) | Tested, signed SAST rules |
| Deploy | [helm-charts](https://github.com/openctemio/helm-charts) | Helm charts for Kubernetes |
| | [openctem-ansible](https://github.com/openctemio/openctem-ansible) | Hardened single-VM install with Ansible |
| Docs | [docs](https://github.com/openctemio/docs) | Source of [docs.openctem.io](https://docs.openctem.io) |

### Contributing

Issues and pull requests are welcome. Read the contributing guide in each repository; contributions are made under the [Contributor License Agreement](https://github.com/openctemio/openctem/blob/main/CLA.md).

### Security

Report vulnerabilities privately to **security@openctem.io** or through GitHub private vulnerability reporting. Never open a public issue for a security report. See the [security policy](https://github.com/openctemio/openctem/security/policy).
