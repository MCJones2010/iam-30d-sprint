WEEK 1 – Core IAM Concepts + Python Foundations
Goals
Understand SAML/OIDC/OAuth2/SCIM vocabulary
Ship a tiny Python script that proves you can call an IAM API
Capture every win in a running Learning Log (Markdown)
Day | <=2 hr Week-nights • <=6 hr W-end | Deliverable
1 (Mon) | ① Create Learning-Log.md in new GitHub repo iam-30d-sprint. ② Download IDPro Body of Knowledge chapters 1–3 (free) Automate the Boring Stuff.③ Write down every past authN/authZ project (VPN MFA, Zero-Trust pilot, AD migration, etc.). | Git commit “Log initialized + prior wins”
2 (Tue) | Read NIST SP 800-63-3 sec. 6 & SP 800-53 control family IA; capture ten bullet takeaways.Watch Microsoft Entra video “SC-300 Module 1 – Course intro” Microsoft Learn. | ✍️ Concept flashcards (use Anki)
3 (Wed) | Python crash: Chapters 0-3 of Automate the Boring Stuff online book Automate the Boring Stuff – do every exercise.Spin up virtualenv with python -m venv venv && source venv/bin/activate && pip install boto3. | hello_iam.py → prints your AWS ARN (sts get-caller-identity)
4 (Thu) | Deep-dive OAuth2 vs OIDC:curl --location -vvv "https://dev-{yourOktaSub}.okta.com/oauth2/default/.well-known/openid-configuration"; note endpoints. | Diagram in draw.io (“Auth code flow w/ PKCE”)
5 (Fri) | Stand up Azure sandbox tenant: enable PIM -> create just-in-time role.Write msal Python script that creates Azure Entra app reg + secret; push to GitHub with README. | Repo azure-iam-scripts
6 (Sat) | Morning: Complete Automate the Boring Stuff chapters 4–6 (flow control, functions, files) Automate the Boring Stuff.Afternoon: Microsoft Learn path “Implement authN & access mgmt” (4 modules, 3 h) Microsoft Learn — take end-of-module quizzes (≥80%). | Screenshot + upload to LinkedIn (“Day 6 progress”)
7 (Sun) | Build a FastAPI micro-API /token that calls AWS STS → presigned URL for S3 putObject.Post a LinkedIn article summarizing Week 1 (what you built + key lessons). | Public thought-leadership post

WEEK 2 – Vendor Cert Sprint + Java Taste
Day | Focus (≈2 hr) | Micro-Deliverable
8 (Mon) | Book Okta Certified Professional exam for Day 28 ($250) Microsoft Learn.Book free SC-300 practice assessment for Day 24 Microsoft Learn. | Calendar confirmations
9 (Tue) | Okta Learning Portal → “Identity Foundations” course (90 min). Hook Google Workspace SAML integration in your dev tenant. | Screen-cap SSO success
10 (Wed) | Okta Hands-On Config Lab – MFA policies, user lockout, self-service.Export tenant config via okta-aws-cli --profile dev —export. | YAML export checked-in
11 (Thu) | Install IntelliJ IDEA CE. Follow JetBrains Academy “Java Basics” 90-min track academy.jetbrains.com.Write IamDemo.java → GET Okta /authorize request, parse ID token header. | Git repo java-iam-demo
12 (Fri) | Docker-compose: Keycloak 22 + Postgres.Create realm, client cred; secure Spring Boot sample (curl localhost:8080/actuator returns 401). | Repo keycloak-spring-lab
13 (Sat) | Morning: Spring Security tutorial – add OAuth2 login.Afternoon: Draft comparison matrix (Okta vs Azure AD vs Keycloak vs AWS IAM): authN, authZ, B2B, B2C, pricing. | PDF one-pager
14 (Sun) | Record 5-min Loom video explaining the matrix; post to GitHub README + LinkedIn. | Permanent portfolio asset

WEEK 3 – Cloud IAM + Automation
Day | Task block | Output
15 (Mon) | Create AWS org w/ root + 1 child account. Apply SCP denying iam:CreateUser globally; test w/ child creds. | Terraform org.tf + README
16 (Tue) | Build least-priv IAM policy for read-only S3 + CloudWatch; validate with IAM Policy Simulator. | policy JSON + screenshot
17 (Wed) | HashiCorp Vault in dev mode: enable aws engine, attach role for dynamic creds; Python script to fetch creds and perform S3 list. | vault-aws.py
18 (Thu) | Write GitHub Action workflow security-scan.yml that runs cfn-nag, checkov on Terraform (push events). | Passing badge in repo
19 (Fri) | SCIM hands-on: Okta → AWS IAM Identity Center (SCIM v2). Provision one test user + role mapping. | Video demo
20 (Sat) | Build FastAPI endpoint /rotate that triggers AWS Access Key rotation via boto3; unit tests in pytest. | CI-tested repo
21 (Sun) | Take SC-300 practice again; if ≥80 %, schedule real exam for Day 30.Blog post “7 common least-priv mistakes & how I fixed them” referencing week’s labs. | Published medium article

WEEK 4 – Certs, Branding, & Interview Prep
Day | Tasks | Evidence
22 (Mon) | Create 200-card Anki deck: Okta admin Qs, Azure Entra governance Qs, IAM trivia. | .apkg file
23 (Tue) | Review Okta exam blueprint; re-configure tenant features you haven’t touched (ILM, import rules). | Notes updated
24 (Wed) | Sit Microsoft Learn practice assessment again; target ≥85 %. Identify missed domains & schedule optional real SC-300 for Day 30. | Score PDF
25 (Thu) | Mock interview round 1: Record yourself answering “Design SSO for 50 B2B partners”.Ask ChatGPT for feedback on answer structure. | Video
26 (Fri) | Mock interview round 2: Whiteboard (Miro) “Migrate on-prem LDAP to Okta Universal Directory”. | Miro link
27 (Sat) | Resume 2.0 – integrate new repos, badges (“Okta Certified Professional – Candidate”), quantifiable wins (AWS org landing zone, SCIM deployment).Rewrite LinkedIn headline: *Cloud IAM Engineer | Okta CP
28 (Sun) | TAKE Okta Certified Professional exam (60 Qs, 90 min).Post badge to LinkedIn via Credly. | 🎖 Okta badge
29 (Mon) | Register for CIDPRO exam (long-term) IDPro. Skim the exam outline to map gaps. | Confirmation email
30 (Tue) | Networking Blitz: DM 10 recruiters + apply to 5 roles. Attach learning-log, videos, repos.If ready, sit SC-300 ($165) same day. | 1st-wave applications
