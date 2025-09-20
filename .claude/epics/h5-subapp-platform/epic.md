---
updated: 2025-09-20T05:44:46Z
name: h5-subapp-platform
status: backlog
created: 2025-09-20T03:27:18Z
progress: 0%
prd: .claude/prds/h5-subapp-platform.md
github: https://github.com/markfredchen/mozac-subapp/issues/1
---
updated: 2025-09-20T05:44:46Z

# Epic: H5 Sub-Application Platform

## Overview

Build a comprehensive H5 sub-application platform using React 18, TypeScript, pnpm monorepo, and Arco Design Mobile. The platform will enable independent development and deployment of mobile web applications as zip-packaged bundles for native app integration, with shared component libraries, CLI tooling, and mobile-optimized build pipelines.

## Architecture Decisions

**Monorepo Strategy**: Use pnpm workspaces for efficient dependency management and code sharing across sub-applications
**Build System**: Leverage Vite for fast builds with mobile-specific optimizations and bundle splitting
**Component Architecture**: Extend Arco Design Mobile with custom components in a shared library
**CLI Framework**: Build custom CLI using Commander.js for project scaffolding and build operations
**Performance Strategy**: Implement bundle size budgets, code splitting, and mobile-first optimization
**Integration Pattern**: Zip-based deployment with manifest metadata for native app consumption

## Technical Approach

### Frontend Components
- **Shared Component Library**: Extend Arco Design Mobile with platform-specific components
- **Sub-App Template**: Standardized React + TypeScript boilerplate with optimal mobile configuration
- **State Management**: Recommend Zustand for lightweight state management across sub-apps
- **Routing**: Use React Router with hash-based routing for WebView compatibility
- **Build Optimization**: Implement tree-shaking, code splitting, and mobile-specific polyfills

### Backend Services
- **Build Service**: Node.js service for processing builds, optimization, and zip packaging
- **CLI Tools**: Command-line interface for scaffolding, development, and deployment operations
- **Development Server**: Hot-reloading dev server with cross-app testing capabilities
- **Asset Management**: Static asset optimization and CDN integration utilities

### Infrastructure
- **Monorepo Structure**: Organized workspace with packages/, apps/, and tools/ directories
- **Build Pipeline**: Automated CI/CD with performance budgets and quality gates
- **Package Distribution**: NPM-based distribution for shared components and CLI tools
- **Development Environment**: Docker-based consistent development setup

## Implementation Strategy

**Phase 1: Foundation (MVP)**
- Establish monorepo structure with pnpm workspaces
- Create basic CLI for project scaffolding
- Build core shared component library (10-15 essential components)
- Implement basic build system with zip packaging

**Phase 2: Enhancement**
- Add hot-reloading development server
- Implement performance monitoring and bundle analysis
- Create comprehensive documentation and Storybook
- Add native app integration examples and utilities

**Risk Mitigation**
- Start with proven technologies (React 18, TypeScript, Vite)
- Implement performance budgets early to prevent regression
- Create migration guides for breaking changes
- Maintain compatibility matrix for supported versions

**Testing Approach**
- Unit tests for all shared components and utilities
- Integration tests for CLI tools and build processes
- E2E tests for complete sub-app development workflows
- Performance testing on target mobile devices

## Tasks Created
- [ ] #2 - monorepo-setup-workspace-configuration (parallel: true)
- [ ] #3 - Zip Packaging and Bundle System (parallel: true)
- [ ] #4 - Performance Monitoring and Bundle Analysis (parallel: true)
- [ ] #5 - cli-foundation-project-scaffolding (parallel: false)
- [ ] #6 - Shared Component Library Foundation (parallel: true)
- [ ] #7 - Documentation and API Guides (parallel: true)
- [ ] #8 - Native App Integration Examples (parallel: true)
- [ ] #9 - Sub-App Template and Boilerplate (parallel: false)
- [ ] #10 - Hot-Reloading Development Server (parallel: true)
- [ ] #11 - core-build-system-vite (parallel: true)

Total tasks: 10
Parallel tasks: 8
Sequential tasks: 2
## Dependencies

**External Dependencies**
- React 18+ ecosystem stability
- Arco Design Mobile framework maintenance
- pnpm package manager continued development
- Vite build tool ecosystem evolution
- Node.js LTS version support

**Internal Dependencies**
- UX/UI design system specifications
- Native mobile app team integration requirements
- DevOps team for CI/CD pipeline setup
- QA team for testing strategy implementation

**Prerequisites**
- Design system tokens and component specifications
- Performance benchmarks and mobile device testing lab
- CI/CD infrastructure for automated builds and testing

## Success Criteria (Technical)

**Performance Benchmarks**
- Bundle size: Initial < 1.5MB, Total < 3MB compressed
- Load times: FCP < 2s, TTI < 3s on 3G networks
- Build times: < 5 minutes for typical sub-app
- Memory usage: < 50MB per sub-app in mobile WebView

**Quality Gates**
- 90% test coverage for shared components and CLI tools
- Zero TypeScript errors in production builds
- Accessibility compliance (WCAG 2.1 AA) for all components
- Performance budgets enforced in CI/CD pipeline

**Acceptance Criteria**
- Developers can scaffold new sub-app in < 30 minutes
- Hot reloading works consistently across development workflows
- Zip packaging produces valid bundles for native app integration
- Documentation covers all major use cases and integration patterns

## Estimated Effort

**Overall Timeline**: 12-16 weeks (3-4 months)

**Resource Requirements**
- 2 senior frontend engineers (full-time)
- 1 platform/DevOps engineer (50% allocation)
- 1 UX designer (25% allocation for component design)
- 1 technical writer (25% allocation for documentation)

**Critical Path Items**
1. Monorepo setup and basic CLI (Weeks 1-2)
2. Component library foundation (Weeks 3-5)
3. Build system and packaging (Weeks 6-8)
4. Development server and tooling (Weeks 9-11)
5. Documentation and integration examples (Weeks 12-14)
6. Testing, optimization, and polish (Weeks 15-16)

**Risk Factors**
- Arco Design Mobile compatibility issues: +2 weeks
- Performance optimization challenges: +3 weeks
- Native app integration complexity: +2 weeks
- Team onboarding and training: +1 week
