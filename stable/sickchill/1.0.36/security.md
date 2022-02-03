---
hide:
  - toc
---

# Security Overview

<link href="https://truecharts.org/_static/trivy.css" type="text/css" rel="stylesheet" />

## Helm-Chart

##### Scan Results

#### Chart Object: sickchill/templates/common.yaml
    

      
| Type         |    Misconfiguration ID   |   Check  |  Severity |                   Explaination                   | Links  |
|:----------------|:------------------:|:-----------:|:------------------:|-----------------------------------------|-----------------------------------------|
| Kubernetes Security Check         |    KSV003   |   Default capabilities not dropped  |  LOW | <details><summary>Expand...</summary> The container should drop all default capabilities and add only those that are needed for its execution. <br> <hr> <br> Container &#39;RELEASE-NAME-sickchill&#39; of Deployment &#39;RELEASE-NAME-sickchill&#39; should add &#39;ALL&#39; to &#39;securityContext.capabilities.drop&#39; </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/">https://kubesec.io/basics/containers-securitycontext-capabilities-drop-index-all/</a><br><a href="https://avd.aquasec.com/appshield/ksv003">https://avd.aquasec.com/appshield/ksv003</a><br></details>  |
| Kubernetes Security Check         |    KSV012   |   Runs as root user  |  MEDIUM | <details><summary>Expand...</summary> &#39;runAsNonRoot&#39; forces the running image to run as a non-root user to ensure least privileges. <br> <hr> <br> Container &#39;RELEASE-NAME-sickchill&#39; of Deployment &#39;RELEASE-NAME-sickchill&#39; should set &#39;securityContext.runAsNonRoot&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv012">https://avd.aquasec.com/appshield/ksv012</a><br></details>  |
| Kubernetes Security Check         |    KSV012   |   Runs as root user  |  MEDIUM | <details><summary>Expand...</summary> &#39;runAsNonRoot&#39; forces the running image to run as a non-root user to ensure least privileges. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-sickchill&#39; should set &#39;securityContext.runAsNonRoot&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv012">https://avd.aquasec.com/appshield/ksv012</a><br></details>  |
| Kubernetes Security Check         |    KSV014   |   Root file system is not read-only  |  LOW | <details><summary>Expand...</summary> An immutable root file system prevents applications from writing to their local disk. This can limit intrusions, as attackers will not be able to tamper with the file system or write foreign executables to disk. <br> <hr> <br> Container &#39;RELEASE-NAME-sickchill&#39; of Deployment &#39;RELEASE-NAME-sickchill&#39; should set &#39;securityContext.readOnlyRootFilesystem&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/">https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/</a><br><a href="https://avd.aquasec.com/appshield/ksv014">https://avd.aquasec.com/appshield/ksv014</a><br></details>  |
| Kubernetes Security Check         |    KSV014   |   Root file system is not read-only  |  LOW | <details><summary>Expand...</summary> An immutable root file system prevents applications from writing to their local disk. This can limit intrusions, as attackers will not be able to tamper with the file system or write foreign executables to disk. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-sickchill&#39; should set &#39;securityContext.readOnlyRootFilesystem&#39; to true </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/">https://kubesec.io/basics/containers-securitycontext-readonlyrootfilesystem-true/</a><br><a href="https://avd.aquasec.com/appshield/ksv014">https://avd.aquasec.com/appshield/ksv014</a><br></details>  |
| Kubernetes Security Check         |    KSV020   |   Runs with low user ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with user ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;RELEASE-NAME-sickchill&#39; of Deployment &#39;RELEASE-NAME-sickchill&#39; should set &#39;securityContext.runAsUser&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv020">https://avd.aquasec.com/appshield/ksv020</a><br></details>  |
| Kubernetes Security Check         |    KSV020   |   Runs with low user ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with user ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-sickchill&#39; should set &#39;securityContext.runAsUser&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv020">https://avd.aquasec.com/appshield/ksv020</a><br></details>  |
| Kubernetes Security Check         |    KSV021   |   Runs with low group ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with group ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;RELEASE-NAME-sickchill&#39; of Deployment &#39;RELEASE-NAME-sickchill&#39; should set &#39;securityContext.runAsGroup&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv021">https://avd.aquasec.com/appshield/ksv021</a><br></details>  |
| Kubernetes Security Check         |    KSV021   |   Runs with low group ID  |  MEDIUM | <details><summary>Expand...</summary> Force the container to run with group ID &gt; 10000 to avoid conflicts with the host’s user table. <br> <hr> <br> Container &#39;autopermissions&#39; of Deployment &#39;RELEASE-NAME-sickchill&#39; should set &#39;securityContext.runAsGroup&#39; &gt; 10000 </details>| <details><summary>Expand...</summary><a href="https://kubesec.io/basics/containers-securitycontext-runasuser/">https://kubesec.io/basics/containers-securitycontext-runasuser/</a><br><a href="https://avd.aquasec.com/appshield/ksv021">https://avd.aquasec.com/appshield/ksv021</a><br></details>  |
| Kubernetes Security Check         |    KSV029   |   A root primary or supplementary GID set  |  LOW | <details><summary>Expand...</summary> Containers should be forbidden from running with a root primary or supplementary GID. <br> <hr> <br> Deployment &#39;RELEASE-NAME-sickchill&#39; should set &#39;spec.securityContext.runAsGroup&#39;, &#39;spec.securityContext.supplementalGroups[*]&#39; and &#39;spec.securityContext.fsGroup&#39; to integer greater than 0 </details>| <details><summary>Expand...</summary><a href="https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted">https://kubernetes.io/docs/concepts/security/pod-security-standards/#restricted</a><br><a href="https://avd.aquasec.com/appshield/ksv029">https://avd.aquasec.com/appshield/ksv029</a><br></details>  |

## Containers

##### Detected Containers

          tccr.io/truecharts/alpine:v3.14.2@sha256:4095394abbae907e94b1f2fd2e2de6c4f201a5b9704573243ca8eb16db8cdb7c
          tccr.io/truecharts/sickchill:v2021.5.10-1-ls63@sha256:f9fd82d8c6d12bc85dcc7813b7216087efb006dc05104ce67386ec989be25dc4

##### Scan Results


#### Container: tccr.io/truecharts/alpine:v3.14.2@sha256:4095394abbae907e94b1f2fd2e2de6c4f201a5b9704573243ca8eb16db8cdb7c (alpine 3.14.2)
    

**alpine**

      
| Package         |    Vulnerability   |   Severity  |  Installed Version | Fixed Version |                   Links                   |
|:----------------|:------------------:|:-----------:|:------------------:|:-------------:|-----------------------------------------|
| busybox         |    CVE-2021-42378   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42378">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42378</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| busybox         |    CVE-2021-42379   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42379">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42379</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| busybox         |    CVE-2021-42380   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42380">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42380</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| busybox         |    CVE-2021-42381   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42381">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42381</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| busybox         |    CVE-2021-42382   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42382">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42382</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| busybox         |    CVE-2021-42383   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br></details>  |
| busybox         |    CVE-2021-42384   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42384">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42384</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| busybox         |    CVE-2021-42385   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42385">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42385</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| busybox         |    CVE-2021-42386   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42386">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42386</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| busybox         |    CVE-2021-42374   |   MEDIUM  |  1.33.1-r3 | 1.33.1-r4 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42374">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42374</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| busybox         |    CVE-2021-42375   |   MEDIUM  |  1.33.1-r3 | 1.33.1-r5 | <details><summary>Expand...</summary><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br></details>  |
| ssl_client         |    CVE-2021-42378   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42378">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42378</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| ssl_client         |    CVE-2021-42379   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42379">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42379</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| ssl_client         |    CVE-2021-42380   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42380">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42380</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| ssl_client         |    CVE-2021-42381   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42381">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42381</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| ssl_client         |    CVE-2021-42382   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42382">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42382</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| ssl_client         |    CVE-2021-42383   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br></details>  |
| ssl_client         |    CVE-2021-42384   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42384">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42384</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| ssl_client         |    CVE-2021-42385   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42385">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42385</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| ssl_client         |    CVE-2021-42386   |   HIGH  |  1.33.1-r3 | 1.33.1-r6 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42386">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42386</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| ssl_client         |    CVE-2021-42374   |   MEDIUM  |  1.33.1-r3 | 1.33.1-r4 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42374">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-42374</a><br><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br><a href="https://ubuntu.com/security/notices/USN-5179-1">https://ubuntu.com/security/notices/USN-5179-1</a><br></details>  |
| ssl_client         |    CVE-2021-42375   |   MEDIUM  |  1.33.1-r3 | 1.33.1-r5 | <details><summary>Expand...</summary><a href="https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/">https://jfrog.com/blog/unboxing-busybox-14-new-vulnerabilities-uncovered-by-claroty-and-jfrog/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/6T2TURBYYJGBMQTTN2DSOAIQGP7WCPGV/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/UQXGOGWBIYWOIVXJVRKHZR34UMEHQBXS/</a><br><a href="https://security.netapp.com/advisory/ntap-20211223-0002/">https://security.netapp.com/advisory/ntap-20211223-0002/</a><br></details>  |


#### Container: Python
    

**python-pkg**

      
| Package         |    Vulnerability   |   Severity  |  Installed Version | Fixed Version |                   Links                   |
|:----------------|:------------------:|:-----------:|:------------------:|:-------------:|-----------------------------------------|
| lxml         |    CVE-2021-43818   |   HIGH  |  4.6.3 | 4.6.5 | <details><summary>Expand...</summary><a href="https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-43818">https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-43818</a><br><a href="https://github.com/advisories/GHSA-55x5-fj6c-h6m8">https://github.com/advisories/GHSA-55x5-fj6c-h6m8</a><br><a href="https://github.com/lxml/lxml/blob/lxml-4.6.5/CHANGES.txt">https://github.com/lxml/lxml/blob/lxml-4.6.5/CHANGES.txt</a><br><a href="https://github.com/lxml/lxml/commit/12fa9669007180a7bb87d990c375cf91ca5b664a">https://github.com/lxml/lxml/commit/12fa9669007180a7bb87d990c375cf91ca5b664a</a><br><a href="https://github.com/lxml/lxml/commit/12fa9669007180a7bb87d990c375cf91ca5b664a (lxml-4.6.5)">https://github.com/lxml/lxml/commit/12fa9669007180a7bb87d990c375cf91ca5b664a (lxml-4.6.5)</a><br><a href="https://github.com/lxml/lxml/commit/a3eacbc0dcf1de1c822ec29fb7d090a4b1712a9c#diff-59130575b4fb2932c957db2922977d7d89afb0b2085357db1a14615a2fcad776">https://github.com/lxml/lxml/commit/a3eacbc0dcf1de1c822ec29fb7d090a4b1712a9c#diff-59130575b4fb2932c957db2922977d7d89afb0b2085357db1a14615a2fcad776</a><br><a href="https://github.com/lxml/lxml/commit/f2330237440df7e8f39c3ad1b1aa8852be3b27c0">https://github.com/lxml/lxml/commit/f2330237440df7e8f39c3ad1b1aa8852be3b27c0</a><br><a href="https://github.com/lxml/lxml/commit/f2330237440df7e8f39c3ad1b1aa8852be3b27c0 (lxml-4.6.5)">https://github.com/lxml/lxml/commit/f2330237440df7e8f39c3ad1b1aa8852be3b27c0 (lxml-4.6.5)</a><br><a href="https://github.com/lxml/lxml/security/advisories/GHSA-55x5-fj6c-h6m8">https://github.com/lxml/lxml/security/advisories/GHSA-55x5-fj6c-h6m8</a><br><a href="https://lists.debian.org/debian-lts-announce/2021/12/msg00037.html">https://lists.debian.org/debian-lts-announce/2021/12/msg00037.html</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/TUIS2KE3HZ2AAQKXFLTJFZPP2IFHJTC7/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/TUIS2KE3HZ2AAQKXFLTJFZPP2IFHJTC7/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/V2XMOM5PFT6U5AAXY6EFNT5JZCKKHK2V/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/V2XMOM5PFT6U5AAXY6EFNT5JZCKKHK2V/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/WZGNET2A4WGLSUXLBFYKNC5PXHQMI3I7/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/WZGNET2A4WGLSUXLBFYKNC5PXHQMI3I7/</a><br><a href="https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/ZQ4SPKJX3RRJK4UWA6FXCRHD2TVRQI44/">https://lists.fedoraproject.org/archives/list/package-announce@lists.fedoraproject.org/message/ZQ4SPKJX3RRJK4UWA6FXCRHD2TVRQI44/</a><br><a href="https://nvd.nist.gov/vuln/detail/CVE-2021-43818">https://nvd.nist.gov/vuln/detail/CVE-2021-43818</a><br><a href="https://security.netapp.com/advisory/ntap-20220107-0005/">https://security.netapp.com/advisory/ntap-20220107-0005/</a><br><a href="https://ubuntu.com/security/notices/USN-5225-1">https://ubuntu.com/security/notices/USN-5225-1</a><br><a href="https://www.debian.org/security/2022/dsa-5043">https://www.debian.org/security/2022/dsa-5043</a><br></details>  |
