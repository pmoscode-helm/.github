---
title: PDG 7.01 - Legal Documentation
---

| Status | Created     | Post-History                         |
|--------|-------------|--------------------------------------|
| Active | 24-Aug-2023 | Updated SECURITY.md file             |
| Active | 20-Jul-2023 | References to PDG 7.07, 7.08 updated |
| Active | 13-Apr-2023 | Moved from OSS Development           |

## Why

Eclipse Tractus-X is an open source project hosted by the Eclipse Foundation licensed under the [Apache License 2.0](https://spdx.org/licenses/Apache-2.0). The legal obligations of the content must be observed in all forms of which the content is available.

This page contains information about legal documentation requirements in your repositories. The source of truth is always the [Eclipse Foundation Project Handbook](https://www.eclipse.org/projects/handbook/#legaldoc).

:::info

The requirements described here **must** be met for each contribution.

:::

## Description

The following files must be part of your repository root folder:

- LICENSE
- SECURITY.md
- CONTRIBUTING.md
- CODE_OF_CONDUCT.md

For examples look to the [Eclipse Tractus-X GitHub Organisation](https://github.com/eclipse-tractusx), e.g. the [APP Dashboard](https://github.com/eclipse-tractusx/app-dashboard).

### LICENSE FILE

In Eclipse Tractus-X the primary outbound license is Apache-2.0.

- SPDX-License-Identifier: Apache-2.0
- [License Text](https://www.apache.org/licenses/LICENSE-2.0.txt)

See the [Handbook#legaldoc-license](https://www.eclipse.org/projects/handbook/#legaldoc-license).

For specifically defined documentation files the Creative Commons Attribution 4.0 International (CC BY 4.0) is required, see PDG 7.08.

### SECURITY FILE

The security file contain the information, where/how to report a vulnerability issue.
See the [Handbook#vulnerability](https://www.eclipse.org/projects/handbook/#vulnerability) and this [example](https://github.com/eclipse-tractusx/eclipse-tractusx.github.io/blob/main/SECURITY.md).

Content:

```md
## Reporting a Vulnerability

Please do **not** report security vulnerabilities through public GitHub issues.

Please report vulnerabilities to this repository via **GitHub security advisories** instead.

How? Inside affected repository --> security tab

for contributor:
--> Report a vulnerability

for committer:
--> advisories --> New draft security advisory

In severe cases, you can also report a found vulnerability via mail or eclipse issue here: https://www.eclipse.org/security/

See [Eclipse Foundation Vulnerability Reporting Policy](https://www.eclipse.org/projects/handbook/#vulnerability)
```

### CODE OF CONDUCT

:::info

The Version 2.0  of the Eclipse Foundation Community Code of Conduct was released on Jan 01, 2023.
Update the file in your repositories.

:::

See the [CODE OF CONDUCT](https://www.eclipse.org/org/documents/Community_Code_of_Conduct.php)
and here in [md format](https://raw.githubusercontent.com/eclipse/.github/master/CODE_OF_CONDUCT.md).
