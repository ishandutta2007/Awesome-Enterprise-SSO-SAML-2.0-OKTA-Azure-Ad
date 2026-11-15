# Awesome-Enterprise-SSO-SAML-2.0-OKTA-Azure-Ad

## Top Enterprise SSO (SAML 2.0 / Okta / Azure AD) Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on SAML Federation, OIDC Providers & Self-Hosted Identity Platforms*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Enterprise Single Sign-On (SSO)**. These tools help organizations centralize authentication across applications—covering everything from commercial IdP suites like Okta and Microsoft Entra ID to open-source identity providers that speak SAML 2.0, OIDC, and OAuth 2.0 without per-user licensing.

**Examples** include Okta, Microsoft Entra ID, OneLogin, PingFederate, CyberArk Identity, Google Workspace, Duo, Auth0, JumpCloud, Keycloak, Authentik, Casdoor, and ZITADEL (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted SSO, open-source SAML/OIDC identity providers, and community-driven authentication platforms—ideal for organizations seeking data sovereignty and avoiding per-user SaaS pricing that compounds across workforces. The open-source landscape is genuinely mature: **Keycloak** is the enterprise-grade standard with the deepest Java extension points, **Authentik** offers the most flexible sign-in flow engine and SCIM provisioning, **Casdoor** provides a lightweight Go binary with built-in LDAP/RADIUS and MCP support, and **ZITADEL** delivers event-sourced audit trails with strict multi-tenancy.

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Druva SSO](https://help.druva.com/en/articles/8580828-set-up-single-sign-on-sso)** | **SAML 2.0 SSO for the Druva Cloud Platform.** Integrates with Okta, Microsoft Entra ID, and other SAML IdPs. The IdP configuration requires the **Assertion Consumer Service URL** (`https://login.druva.com/api/commonlogin/samlconsume` for Public Cloud) and the **SAML Identifier** (`DCP-login` as the entity ID). Users are assigned SSO access via profiles—select "SSO" in the User Privacy & Access login option [citation:1][citation:11]. | Included with Druva subscription (no standalone SSO fee) | No free tier; SSO bundled with Druva platform |
| **[Okta](https://www.okta.com/)** | **The independent IAM benchmark.** Workforce Identity bundles SSO, MFA, and Universal Directory. **Starter: $6/user/month** (annual, includes SSO + MFA). **Essentials: $17/user/month** adds Adaptive MFA, Lifecycle Management, and Access Governance. **Single modules are no longer sold separately**—you buy a suite even for SSO alone. **$1,500/year minimum contract** applies to smaller teams (~under 20 seats) [citation:2][citation:12]. | Starter: **$6/user/month**; Essentials: **$17/user/month** | No free plan; median buyer pays **~$43,840/year** (Vendr), with ~14% average discount available [citation:2] |
| **[Microsoft Entra ID](https://www.microsoft.com/en-us/security/business/identity-access/microsoft-entra-id)** | **The default for Microsoft estates.** SAML 2.0 and OIDC federation with Conditional Access. **P1: ~$7/user/month** standalone; **P2: ~$10/user/month**. **Often bundled at no extra cost** with Microsoft 365 Business Premium, E3 (P1), or E5 (P2)—many organizations already own it [citation:13]. | P1: **~$7/user/month**; P2: **~$10/user/month** (standalone) | **Free edition** included with Azure/M365; P1/P2 bundled in many enterprise plans |
| **[OneLogin](https://www.onelogin.com/)** | Mid-market SSO with SAML and OIDC. **Transparent published tiers: Basic $3, Essentials $6, Business $10, Enterprise (quote)** per user/month [citation:5]. Vendr data shows buyers often achieve **$2.50–$5.00/user/month** for Advanced tier with annual prepayment and multi-year terms [citation:15]. | Basic: **$3/user/month**; Essentials: **$6**; Business: **$10** | Free trial available; implementation services **$5K–$15K** typical for basic onboarding [citation:15] |
| **[PingFederate](https://www.pingidentity.com/)** | **Enterprise federation server for complex, high-assurance environments.** SAML 2.0, OIDC, WS-Federation, and WS-Trust. **Essential plan starts at $35,000/year** (no monthly billing, no free tier)—positioned for large organizations with dedicated identity teams [citation:14]. | Essential: **~$35,000/year** | No free tier; trial via sales |
| **[CyberArk Identity](https://www.cyberark.com/)** | **Modular pricing with the lowest SSO entry point.** **Workforce Identity SSO: $2/user/month** (annual). **Real cost compounds**—adding MFA (~$3) and Lifecycle Management (~$4) pushes effective per-user cost to **~$9/month** [citation:6]. | SSO: **$2/user/month**; Modules: $2–$5 each | No free tier; demo via sales |
| **[Google Workspace](https://workspace.google.com/)** | SAML-based SSO **included at no separate charge** in all paid Workspace tiers. **Business Starter: $7/user/month** list (annual effective ~$5.60 with discount). **No free-seat allowance**—bills from seat 1 [citation:7]. | Business Starter: **$7/user/month** (list); annual effective ~$5.60 | **14-day free trial**; no permanent free tier |
| **[Duo](https://duo.com/editions-and-pricing)** | **Duo Free: $0 for 1–10 users**—genuine free tier for small teams. **Duo Essentials: $3/user/month** adds Single Sign-On (SAML/OIDC). Advantage ($6) and Premier ($9) add advanced access policies and reporting [citation:8]. | Free: **$0** (1–10 users); Essentials: **$3/user/month** | **Free forever**: 1–10 users, core MFA (SSO requires Essentials) [citation:8] |
| **[Auth0](https://auth0.com/pricing)** | Developer-first identity platform. **Free tier: 25,000 MAU**. **Self-Service SSO is available on select Enterprise plans only**—not on free or lower tiers. Dashboard SSO requires higher tiers [citation:9]. | Quote-only for SSO features; Free tier: 25K MAU | **Free**: 25,000 MAU (SSO not included); **Startup plan**: 100K MAU + SSO free for one year [citation:9] |
| **[JumpCloud](https://jumpcloud.com/)** | Cloud directory with SSO. **SSO package: ~$11/user/month** (OMR listing)—positioned for organizations wanting directory + SSO + device management in one platform [citation:10]. | SSO: **~$11/user/month** | Free tier available for up to 10 users (limited features) |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Keycloak](https://github.com/keycloak/keycloak)** | [![Stars](https://img.shields.io/github/stars/keycloak/keycloak?style=social&color=white)](https://github.com/keycloak/keycloak/stargazers) | **The enterprise-grade open-source SSO standard.** Apache-2.0, Java/Quarkus. **SAML 2.0, OIDC, OAuth 2.0, and LDAP federation** native. **Realms provide multi-tenancy**. SCIM 2.0 server support since 26.8. **The most extension points for Java developers**—custom authentication flows via SPIs. **Trade-off**: heavyweight deployment and large configuration surface area—teams wanting quick setup may find initial configuration frustrating. **Best for enterprises needing battle-tested SSO** with deep Java customization and Red Hat backing. |
| **[Authentik](https://github.com/goauthentik/authentik)** | [![Stars](https://img.shields.io/github/stars/goauthentik/authentik?style=social&color=white)](https://github.com/goauthentik/authentik/stargazers) | **The most approachable open-source SSO with the most flexible sign-in flows.** MIT core with paid enterprise features. **Flows and stages edited in the admin interface**—custom authentication logic without code. **The only one of the four leading IdPs with a SCIM provider** (push users to downstream apps). **Forward Auth** for Nginx-backed services is straightforward. **Best for teams with mixed technical backgrounds** wanting maintainable SSO without deep identity expertise—often the recommended starting point over Keycloak. |
| **[Casdoor](https://github.com/casdoor/casdoor)** | [![Stars](https://img.shields.io/github/stars/casdoor/casdoor?style=social&color=white)](https://github.com/casdoor/casdoor/stargazers) | **Lightweight Go-based SSO with the widest protocol coverage.** Apache-2.0. **Single Go binary + React UI**—no JVM, no separate worker process. **SAML 2.0, OIDC, OAuth 2.0, CAS, LDAP, RADIUS, and SCIM** all supported. **Built-in MCP server with OAuth 2.1 for AI agents**—no other open-source IdP offers this natively. **70+ social/enterprise providers** including WeChat and DingTalk. **Syncers import users from Keycloak, Okta, Entra ID, and Google Workspace**—enabling gradual migration. **Best for teams wanting a lighter, UI-first IdP** with legacy protocol support and AI-agent readiness. |
| **[ZITADEL](https://github.com/zitadel/zitadel)** | [![Stars](https://img.shields.io/github/stars/zitadel/zitadel?style=social&color=white)](https://github.com/zitadel/zitadel/stargazers) | **Event-sourced SSO with the strongest audit trail and tenant isolation.** AGPL-3.0, Go/TypeScript. **SAML 2.0, OIDC, OAuth 2.0, and SCIM** support. **Instances → Organizations → Projects** hierarchy provides **infrastructure-level tenant isolation**. **Every mutation is an immutable event** for a complete, API-accessible audit trail. **API-first design** with connectRPC, gRPC, and REST. **Best for organizations needing the strongest audit trail and tenant isolation** with a modern API-first design. |
| **[Authelia](https://github.com/authelia/authelia)** | [![Stars](https://img.shields.io/github/stars/authelia/authelia?style=social&color=white)](https://github.com/authelia/authelia/stargazers) | **Lightweight SSO for protecting reverse proxy endpoints.** Go-based. **Not a standalone directory**—sits in front of Nginx, Traefik, or HAProxy and handles authentication and 2FA for services behind those proxies. **Best for homelabs and internal service protection** where a full IdP is overkill—it will not cover application-level OIDC federation on its own. |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[WSO2 Identity Server](https://github.com/wso2/product-is)** | [![Stars](https://img.shields.io/github/stars/wso2/product-is?style=social&color=white)](https://github.com/wso2/product-is/stargazers) | **Open-source IAM with SAML, OIDC, OAuth2, SCIM 2.0, and FIDO2 support.** Apache-2.0. Recognized as a Digital Public Good by the Digital Public Goods Alliance. **Used in 93 countries** across finance, public administration, healthcare, and telecommunications. **Best for organizations wanting a recognized open-source IAM** with broad standards support and enterprise adoption. |
| **[Janssen Project](https://github.com/JanssenProject/jans)** | [![Stars](https://img.shields.io/github/stars/JanssenProject/jans?style=social&color=white)](https://github.com/JanssenProject/jans/stargazers) | **Linux Foundation-governed IAM server providing OAuth 2.0, OIDC, SAML, FIDO2/WebAuthn, and SCIM.** Apache-2.0. **Kubernetes-native with auto-scaling** for enterprise and national scale. **Low-code flow orchestration (Agama) and policy engine (Cedarling)** for custom authentication logic without forking the core. **Best for organizations needing population-scale SSO** with strong federation readiness and Digital Public Good recognition. |
| **[Dex](https://github.com/dexidp/dex)** | [![Stars](https://img.shields.io/github/stars/dexidp/dex?style=social&color=white)](https://github.com/dexidp/dex/stargazers) | **OpenID Connect (OIDC) identity and OAuth 2.0 provider with pluggable connectors.** CNCF project. Often used as an authentication layer in Kubernetes clusters (integrates with Kubernetes API server OIDC). **Best for Kubernetes-native SSO** where Dex acts as the bridge between upstream IdPs and cluster authentication. |

**Frameworks for building custom systems**: Choose **Keycloak** for enterprise-grade SSO with the broadest Java extension ecosystem, **Authentik** for the most approachable setup with SCIM provisioning, **Casdoor** for a lightweight Go binary with built-in LDAP/RADIUS and AI-agent MCP support, or **ZITADEL** for event-sourced audit trails and strict tenant isolation —all without per-user pricing that compounds across large workforces.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- SSO platforms handle authentication credentials and identity data; enforce MFA, least-privilege access, and compliance with applicable regulations (GDPR, SOC 2, HIPAA where relevant). **A compromised IdP exposes every connected application.**
- **Commercial pricing has significant hidden costs and escalators.** **Okta** no longer sells SSO as a standalone module—Starter ($6/user/mo) bundles SSO+MFA+directory, but a **$1,500/year minimum** applies to teams under ~20 seats [citation:2][citation:12]. **PingFederate starts at $35,000/year** with no monthly option or free tier [citation:14]. **OneLogin's list prices** ($3–$10/user/mo) are starting points—implementation adds **$5K–$15K**, and annual escalators of **3–5%** are common [citation:15]. **CyberArk's $2/user/month SSO** looks cheapest but compounds to **~$9/month** when MFA and Lifecycle are added [citation:6]. **Duo offers a genuine free tier** for 1–10 users, but SSO requires the $3/user/month Essentials plan [citation:8]. **Auth0's self-service SSO is Enterprise-only**—the 25K MAU free tier does not include it [citation:9]. **Druva SSO is bundled** with the platform, requiring the specific ACS URL and entity ID (`DCP-login`) during IdP configuration [citation:1]. **Validate whether SSO is already bundled in your existing Microsoft 365 or Google Workspace plan** before purchasing a standalone IdP—many organizations already own Entra ID P1/P2 through E3/E5 licensing [citation:13].

---

**Made for identity architects, IT administrators, and organizations building authentication infrastructure.**  
Let's make enterprise single sign-on more open, interoperable, and secure.
