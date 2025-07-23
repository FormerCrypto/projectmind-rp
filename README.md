# ProjectMind RP - AI-Powered Project Recovery Platform

An advanced AI-powered platform that transforms broken code into fully functional applications with comprehensive quality assurance and deployment automation.

## 🚀 Quick Start

### Prerequisites
- Node.js 20+
- PostgreSQL database
- GitHub Personal Access Token
- OpenAI API Key

### Environment Setup
```bash
# Required environment variables
DATABASE_URL=your_postgresql_url
GITHUB_TOKEN=your_github_pat
OPENAI_API_KEY=your_openai_key
```

### Installation
```bash
npm install
npm run db:push
npm run dev
```

## 🔧 GitHub Integration Setup

### Phase 1: Secure GitHub Connection

#### 1. Personal Access Token Setup
1. Generate GitHub PAT at: https://github.com/settings/tokens
2. Required permissions:
   - `repo` (full repository access)
   - `workflow` (GitHub Actions)
   - `admin:repo_hook` (webhooks)
   - `security_events` (security alerts)
3. Store in Replit Secrets as `GITHUB_TOKEN`

#### 2. Repository Configuration
- **Repository**: https://github.com/FormerCrypto/projectmind-rp
- **Owner**: FormerCrypto
- **Visibility**: Public
- **Created**: July 23, 2025

#### 3. Security Features Enabled
- ✅ **Dependabot**: Automated weekly security updates
- ✅ **Vulnerability Alerts**: Real-time security notifications
- ✅ **Secret Scanning**: Automatic credential detection
- ✅ **CodeQL Analysis**: Advanced code security scanning
- ✅ **Branch Protection**: Main branch protection rules

#### 4. Branch Protection Rules
- **Main Branch Protected**: ✅ Enabled
- **Signed Commits Required**: ✅ Enforced
- **Pull Request Reviews**: Required before merge
- **Status Checks**: CI/CD must pass
- **Force Push**: Disabled

### Git Remote Configuration
```bash
# Remote repository
git remote add origin https://github.com/FormerCrypto/projectmind-rp.git

# Verify connection
git remote -v
# origin  https://github.com/FormerCrypto/projectmind-rp.git (fetch)
# origin  https://github.com/FormerCrypto/projectmind-rp.git (push)
```

### Fork/Upstream Setup
```bash
# For contributors - fork the repository first
git clone https://github.com/YOUR_USERNAME/projectmind-rp.git
cd projectmind-rp

# Add upstream remote
git remote add upstream https://github.com/FormerCrypto/projectmind-rp.git

# Verify remotes
git remote -v
# origin    https://github.com/YOUR_USERNAME/projectmind-rp.git (fetch)
# origin    https://github.com/YOUR_USERNAME/projectmind-rp.git (push)
# upstream  https://github.com/FormerCrypto/projectmind-rp.git (fetch)
# upstream  https://github.com/FormerCrypto/projectmind-rp.git (push)
```

## 🔒 Security Configuration

### Automated Security Features

#### Dependabot Configuration
```yaml
# .github/dependabot.yml
version: 2
updates:
  - package-ecosystem: "npm"
    directory: "/"
    schedule:
      interval: "weekly"
      day: "monday"
      time: "09:00"
```

#### Security Scanning Workflow
```yaml
# .github/workflows/security.yml
- Semgrep static analysis
- CodeQL vulnerability detection
- npm audit dependency scanning
- Dependency review for PRs
```

### GPG Commit Signing Setup
```bash
# Generate GPG key
gpg --full-generate-key

# Add to GitHub account
gpg --armor --export YOUR_KEY_ID

# Configure Git
git config user.signingkey YOUR_KEY_ID
git config commit.gpgsign true
```

## 🏗️ Development Workflow

### Branch Strategy
- **main**: Protected production branch
- **develop**: Development integration branch
- **feature/***: Feature development branches

### Pull Request Process
1. Create feature branch from `develop`
2. Implement changes with signed commits
3. Run security checks: `npm run check`
4. Create PR to `develop`
5. Await review and CI/CD approval
6. Merge with signed commits

### CI/CD Pipeline
```yaml
# Automated checks on every PR/push
- TypeScript compilation
- Security scanning
- Build verification
- Dependency review
```

## 📦 Deployment

### Production Deployment
```bash
# Build for production
npm run build

# Deploy to hosting platform
# (Replit Deployments, Vercel, etc.)
```

### Environment Variables
```bash
# Production environment
NODE_ENV=production
DATABASE_URL=production_postgresql_url
GITHUB_TOKEN=production_github_pat
OPENAI_API_KEY=production_openai_key
```

## 🔍 Verification Commands

### Verify GitHub Integration
```bash
# Check repository access
curl -H "Authorization: token $GITHUB_TOKEN" \
  https://api.github.com/repos/FormerCrypto/projectmind-rp

# Verify security features
curl -H "Authorization: token $GITHUB_TOKEN" \
  https://api.github.com/repos/FormerCrypto/projectmind-rp/vulnerability-alerts
```

### Verify Branch Protection
```bash
# Check protection status
curl -H "Authorization: token $GITHUB_TOKEN" \
  https://api.github.com/repos/FormerCrypto/projectmind-rp/branches/main
```

## 📚 Documentation

- **Security Policy**: `.github/SECURITY.md`
- **Integration Log**: `GITHUB_INTEGRATION_LOG.md`
- **QA Evidence**: `PHASE_1_QA_EVIDENCE_REPORT.md`
- **Completion Verification**: `PHASE_1_COMPLETION_VERIFICATION.md`

## 🚨 Security Compliance

This repository follows strict security practices:
- No credentials in code or logs
- Automated vulnerability scanning
- Required signed commits
- Branch protection enforcement
- Comprehensive security monitoring

## 📞 Support

For security issues, see `.github/SECURITY.md`  
For development questions, create an issue in the repository.

---

**Repository**: https://github.com/FormerCrypto/projectmind-rp  
**Documentation Updated**: July 23, 2025  
**Security Compliance**: Phase 1 Complete