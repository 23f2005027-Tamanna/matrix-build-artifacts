# Multi-Platform Matrix Build with Artifacts

[![Multi-Platform Matrix Build](https://github.com/23f2005027-Tamanna/matrix-build-artifacts/actions/workflows/matrix-build.yml/badge.svg)](https://github.com/23f2005027-Tamanna/matrix-build-artifacts/actions/workflows/matrix-build.yml)

## DevOps Challenge: GitHub Actions Matrix Strategy

This repository demonstrates a sophisticated CI/CD pipeline using GitHub Actions matrix builds to compile software across multiple platforms and configurations simultaneously.

## 📧 Contact
**Email:** 23f2005027@studentmail.upes.ac.in

## 🎯 Challenge Details
- **Transaction ID:** TXN-23F2005027-0905
- **Student ID:** 23f2005027-Tamanna

## 🔧 Matrix Configuration

This workflow builds across **9 different variants**:

### Matrix Dimensions:
- **Operating Systems:** 3 variants
  - Ubuntu Latest (Linux)
  - macOS Latest
  - Windows Latest

- **Node.js Versions:** 3 variants
  - Node.js 16
  - Node.js 18
  - Node.js 20

### Total Combinations: 3 OS × 3 Node versions = **9 parallel jobs**

## 📦 Artifact Management

Each matrix job generates unique artifacts with the naming pattern:
```
build-58c3fe0-<platform>-node<version>
```

### Example Artifacts:
- `build-58c3fe0-linux-node16`
- `build-58c3fe0-linux-node18`
- `build-58c3fe0-linux-node20`
- `build-58c3fe0-macos-node16`
- `build-58c3fe0-macos-node18`
- `build-58c3fe0-macos-node20`
- `build-58c3fe0-windows-node16`
- `build-58c3fe0-windows-node18`
- `build-58c3fe0-windows-node20`

## 🚀 Features

✅ **Matrix Strategy**: 9 parallel build variants  
✅ **Cross-Platform**: Linux, macOS, Windows  
✅ **Multi-Version**: Node.js 16, 18, 20  
✅ **Artifact Generation**: Each job creates unique build outputs  
✅ **Artifact Upload**: Using actions/upload-artifact@v4  
✅ **Step Identifier**: matrix-58c3fe0 included  
✅ **Parallel Execution**: All jobs run concurrently  

## 📝 Workflow Structure

```yaml
strategy:
  matrix:
    os: [ubuntu-latest, macos-latest, windows-latest]
    node-version: [16, 18, 20]
```

## 🏗️ Build Artifacts Contents

Each artifact contains:
1. **output.txt** - Detailed build information
2. **metadata.json** - Structured build metadata

### Sample output.txt:
```
Build Information
==================
OS: ubuntu-latest
Node Version: 18
Platform: linux
Build Time: 2025-11-09 07:37:30
Runner: Linux
Workflow: Multi-Platform Matrix Build
Run ID: 123456789
```

### Sample metadata.json:
```json
{
  "os": "ubuntu-latest",
  "node": "18",
  "platform": "linux",
  "timestamp": "2025-11-09T07:37:30Z"
}
```

## ✅ Validation Checklist

- [x] At least 3 successful matrix jobs (we have 9!)
- [x] At least 3 artifacts with prefix `build-58c3fe0` (we have 9!)
- [x] All artifacts contain actual content (non-empty files)
- [x] Step identifier `matrix-58c3fe0` included
- [x] README.md with email address

## 🎓 Learning Outcomes

This project demonstrates:
- GitHub Actions matrix strategy
- Parallel job execution
- Cross-platform CI/CD
- Artifact management and retention
- Build automation best practices

## 📊 Workflow Status

Check the [Actions tab](https://github.com/23f2005027-Tamanna/matrix-build-artifacts/actions) to see all workflow runs and download artifacts.

---
echo ""
**Repository:** https://github.com/23f2005027-Tamanna/matrix-build-artifacts  
**Author:** 23f2005027-Tamanna  
**Challenge:** Multi-Platform Matrix Build with Artifacts# matrix-build-artifacts
