## Resources

[OWASP Top 10 for Large Language Models](https://owasp.org/www-project-top-10-for-large-language-model-applications/assets/PDF/OWASP-Top-10-for-LLMs-2023-v1_1.pdf)

![OWASP Top10 for LLM](images/GOV1_Fig_4_1.jpg)
##### Figure 4.1  OWASP Top 10 for Large Language Model Applications

![OWASP Top10 for LLM Visual](images/GOV1_Fig_4_2_en.png)
##### Figure 4.2  OWASP Top 10 for Large Language Model Applications Visualized


### OWASP Resources

Using LLM solutions expands an organization's attack surface and presents new challenges, requiring special tactics and defenses. It also poses problems that are similar to known issues, and where there are already established cybersecurity procedures and mitigations. Integrating LLM cybersecurity with an organization's established cybersecurity controls, processes, and procedures allows an organization to reduce its vulnerability to threats.
How they integrate is available at the [OWASP Integration Standards.](https://owasp.org/www-project-integration-standards/)

#### OWASP Resource
  [OWASP SAMM](https://owasp.org/www-project-samm/)
#### Description
  Software Assurance Maturity Model
#### Why it is Recommended & Where To Use It
  Provides an effective and measurable way to analyze and improve an organization's secure development lifecycle. SAMM supports the complete software lifecycle. It is iterative and risk-driven, enabling organizations to identify and prioritize gaps in secure software development so resources for improving the process can be dedicated where efforts have the greatest improvement impact.

#### OWASP Resource
  [OWASP AI Exchange](https://owasp.org/www-project-ai-security-and-privacy-guide/owaspaiexchange.html)
  [OWASP Machine Learning Security Top 10](https://mltop10.info/)
#### Description
  OWASP Project to connect worldwide for an exchange on AI security, fostering standards alignment, and driving collaboration.
  OWASP AI Exchange is the intake method for the OWASP AI Security and Privacy Guide
  OWASP Machine Learning Security Top 10 security issues of machine learning systems
#### Why it is Recommended & Where To Use It
  This project includes the ML Top 10 and is a live working document that provides clear and actionable insights on designing, creating, testing, and procuring secure and privacy-preserving AI systems. It is the best OWASP resource for AI global regulatory and privacy information.

#### OWASP Resource
   [Open Common Requirement Enumeration : OpenCRE](https://www.opencre.org/)
#### Description
  OpenCRE is the interactive content-linking platform for uniting security standards and guidelines into one overview.
#### Why it is Recommended & Where To Use It
  Use this site to search for standards. You can search by standard name or by control type.

#### OWASP Resource
  [OWASP Threat Modeling](https://owasp.org/www-community/Threat_Modeling)
#### Description
  A structured, formal process for threat modeling of an application
#### Why it is Recommended & Where To Use It
  Learn everything about Threat Modeling which is a structured representation of all the information that affects the security of an application.

#### OWASP Resource
  [OWASP CycloneDX](https://owasp.org/www-project-cyclonedx/)
#### Description
  OWASP CycloneDX is a full-stack Bill of Materials (BOM) standard that provides advanced supply chain capabilities for cyber risk reduction.
#### Why it is Recommended & Where To Use It
  Modern software is assembled using third-party and open source components. They are glued together in complex and unique ways and integrated with original code to achieve the desired functionality. An SBOM provides an accurate inventory of all components which enables organizations to identify risk, allows for greater transparency, and enables rapid impact analysis.
  [EO 14028](https://www.nist.gov/itl/executive-order-14028-improving-nations-cybersecurity/software-security-supply-chains-software-1) provided minimum requirements for SBOM for federal systems.

#### OWASP Resource
  [OWASP Software Component Verification Standard (SCVS)](https://scvs.owasp.org/)
#### Description
  A community-driven effort to establish a framework for identifying activities, controls, and best practices to identify and reduce risk in a software supply chain.
#### Why it is Recommended & Where To Use It
  Use SCVS to develop a common set of activities, controls, and best practices that can reduce risk in a software supply chain and identify a baseline and path to mature software supply chain vigilance.

#### OWASP Resource
  [OWASP API Security Project](https://owasp.org/www-project-api-security/)
#### Description
  API Security focuses on strategies and solutions to understand and mitigate the unique vulnerabilities and security risks of Application Programming Interfaces (APIs).
#### Why it is Recommended & Where To Use It
  APIs are a foundational element of connecting applications and mitigating misconfigurations or vulnerabilities is mandatory to protect users and organizations. Use for security testing and red teaming the build and production environments.

#### OWASP Resource
  [OWASP Top 10 CI/CD Security Risks](https://owasp.org/www-project-top-10-ci-cd-security-risks/)
#### Description
  Helps defenders identify focus areas for securing their CI/CD ecosystem.
#### Why it is Recommended & Where To Use It
  CI/CD environments, processes, and systems are the ecosystem of modern software organizations. They deliver code from an engineer's workstation to production. They have their unique attack surface and a frequent attack target. Use for security testing and red teaming the build and production environments. 

#### OWASP Resource
  [OWASP Application Security Verification Standard ASVS](https://owasp.org/www-project-application-security-verification-standard/)
#### Description
  Application Security Verification Standard (ASVS) Project provides a basis for testing web application technical security controls and also provides developers with a list of requirements for secure development.
#### Why it is Recommended & Where To Use It
  Cookbook for web application security requirements, security testing, and metrics. Use to establish security user stories and security use case release testing.

#### OWASP Resource
  [OWASP Threat and Safeguard Matrix (TaSM)](https://owasp.org/www-project-threat-and-safeguard-matrix/)
#### Description
  An action oriented view to safeguard and enable the business
#### Why it is Recommended & Where To Use It
  This matrix allows a company to overlay its major threats with the NIST Cyber Security Framework Functions (Identify, Protect, Detect, Respond, & Recover) to build a robust security plan. Use it as a dashboard to track and report on security across the organization.

#### OWASP Resource
   [Defect Dojo](https://www.defectdojo.com/)
#### Description
  An open-source vulnerability management tool that streamlines the testing process by offering templating, report generation, metrics, and baseline self-service tools.
#### Why it is Recommended & Where To Use It
  Use Defect Dojo to reduce the time for logging vulnerabilities with templates for vulnerabilities, imports for common vulnerability scanners, report generation, and metrics.


### MITRE Resources

The increased frequency of LLM threats emphasizes the value of a resilience-first approach to defending an organization's attack surface. Existing TTPS is combined with new attack surfaces and capabilities in LLM Adversary threats and mitigations. MITRE maintains a well-established and widely accepted mechanism for coordinating opponent tactics and procedures based on real-world observations.

Coordination and mapping of an organization's LLM Security Strategy to MITRE ATT&CK and MITRE ATLAS allows an organization to determine where LLM Security is covered by current processes such as API Security Standards or where security holes exist.

MITRE ATT&CK (Adversarial Tactics, Techniques, and Common Knowledge) is a framework, collection of data matrices, and assessment tool that was made by the MITRE Corporation to help organizations figure out how well their cybersecurity works across their entire digital attack surface and find holes that had not been found before. It is a knowledge repository that is used all over the world. The MITRE ATT&CK matrix contains a collection of strategies used by adversaries to achieve a certain goal. In the ATT&CK Matrix, these objectives are classified as tactics. The objectives are outlined in attack order, beginning with reconnaissance and progressing to the eventual goal of exfiltration or impact.

MITRE ATLAS, which stands for "Adversarial Threat Landscape for Artificial Intelligence Systems," is a knowledge base that is based on real-life examples of attacks on machine learning (ML) systems by bad actors. ATLAS is based on the MITRE ATT&CK architecture, and its tactics and procedures complement those found in ATT&CK.

#### MITRE Resource
  [MITRE ATT&CK](https://attack.mitre.org/)
#### Description
  Knowledge base of adversary tactics and techniques based on real-world observations
#### Why it is Recommended & Where To Use It
  The ATT&CK knowledge base is used as a foundation for the development of specific threat models and methodologies. Map existing controls within the organization to adversary tactics and techniques to identify gaps or areas to test.

#### MITRE Resource
  [MITRE AT&CK Workbench](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/our-work/attck-workbench/)
#### Description
  Create or extend ATT&CK data in a local knowledge base
#### Why it is Recommended & Where To Use It
  Host and manage a customized copy of the ATT&CK knowledge base. This local copy of the ATT&CK knowledge base can be extended with new or updated techniques, tactics, mitigation groups, and software that is specific to your organization.

#### MITRE Resource
   [MITRE ATLAS](https://atlas.mitre.org/)
#### Description
  MITRE ATLAS (Adversarial Threat Landscape for Artificial-Intelligence Systems) is a knowledge base of adversary tactics, techniques, and case studies for machine learning (ML) systems based on real-world observations, demonstrations from ML red teams and security groups, and the state of the possible from academic research
#### Why it is Recommended & Where To Use It
  Use it to map known ML vulnerabilities and map checks and controls for proposed projects or existing systems.

#### MITRE Resource
  [MITRE ATT&CK Powered Suit](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/attack-powered-suit/)
#### Description
  ATT&CK Powered Suit is a browser extension that puts the MITRE ATT&CK knowledge base at your fingertips.
#### Why it is Recommended & Where To Use It
  Add to your browser to quickly search for tactics, techniques, and more without disrupting your workflow.

#### MITRE Resource
  [The Threat Report ATT&CK Mapper (TRAM)](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/our-work/threat-report-attck-mapper-tram/)
#### Description
  Automates TTP Identification in CTI Reports
#### Why it is Recommended & Where To Use It
  Mapping TTPs found in CTI reports to MITRE ATT&CK is difficult, error prone, and time-consuming. TRAM uses LLMs to automate this process for the 50 most common techniques. Supports Juypter notebooks.

#### MITRE Resource
   [Attack Flow v2.1.0](https://center-for-threat-informed-defense.github.io/attack-flow/)
#### Description
  Attack Flow is a language for describing how cyber adversaries combine and sequence various offensive techniques to achieve their goals.
#### Why it is Recommended & Where To Use It
  Attack Flow helps visualize how an attacker uses a technique, so defenders and leaders understand how adversaries operate and improve their defensive posture.

#### MITRE Resource
  [MITRE Caldera](https://caldera.mitre.org/)
#### Description
  A cyber security platform (framework) designed to easily automate adversary emulation, assist manual red teams, and automate incident response.
#### Why it is Recommended & Where To Use It
  Plugins are available for Caldera that help to expand the core capabilities of the framework and provide additional functionality, including agents, reporting, collections of TTPs, and others.
  [Here is the plugin library.](https://caldera.readthedocs.io/en/latest/Plugin-library.html)

#### MITRE Resource
  [CALDERA plugin: Arsenal](https://www.mitre.org/news-insights/news-release/microsoft-and-mitre-create-tool-help-security-teams-prepare-attacks)
#### Description
  A plugin developed for adversary emulation of AI-enabled systems.
#### Why it is Recommended & Where To Use It
  This plugin provides TTPs defined in MITRE ATLAS to interface with CALDERA.

#### MITRE Resource
  [Atomic Red Team](https://github.com/redcanaryco/atomic-red-team)
#### Description
  Library of tests mapped to the MITRE ATT&CK framework.
#### Why it is Recommended & Where To Use It
  Use to validate and test controls in an environment. Security teams can use Atomic Red Team to test controls.
  You can execute atomic tests directly from the command line; no installation is required.

#### MITRE Resource
  [MITRE CTI Blueprints](https://mitre-engenuity.org/cybersecurity/center-for-threat-informed-defense/our-work/cti-blueprints/)
#### Description
  Automates Cyber Threat Intelligence reporting.
#### Why it is Recommended & Where To Use It
  CTI Blueprints helps Cyber Threat Intelligence (CTI) analysts create high-quality, actionable reports more consistently and efficiently



### AI Vulnerability Repositories

[AI Incident Database](https://incidentdatabase.ai/)
  A repository of articles about different times AI has failed in real-world applications and is maintained by a college research group and crowds sourced.
[OECD AI Incidents Monitor (AIM)](https://oecd.ai/en/incidents)
  Offers an accessible starting point for comprehending the landscape of AI-related challenges.


### Leading Companies Tracking AI Model Vulnerabilities

[Huntr Bug Bounty : ProtectAI](https://huntr.com/)
  Bug bounty platform for AI/ML
[AI Vulnerability Database (AVID) : Garak](https://avidml.gitbook.io/)
  Database of model vulnerabilities
[AI Risk Database: Robust Intelligence](https://airisk.io/)
  Database of model vulnerabilities
[LVE Repository](https://lve-project.org/blog/launching-the-lve-project.html)
  Open LLM Vulnerability and Exposures Repository


### AI Procurement Guidance

[World Economic Forum: Adopting AI Responsibly: Guidelines for Procurement of AI Solutions by the Private Sector: Insight Report June 2023](https://www.weforum.org/publications/adopting-ai-responsibly-guidelines-for-procurement-of-ai-solutions-by-the-private-sector/)
  The standard benchmarks and assessment criteria for procuring Artificial systems are in early development. This procurement guidelines provide organizations with a baseline of considerations for the end-to-end procurement process.

  Use this guidance to augment an organization's existing Third Party Risk Supplier and Vendor procurement process. 

