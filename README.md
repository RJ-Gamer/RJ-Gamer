# 👋 Hi, I'm Rajat Jog

**Senior Backend Engineer • Production ML Systems • Python/Django Specialist**

<div align="center">

[![AWS Certified Machine Learning – Specialty](https://images.credly.com/size/340x340/images/778bde6c-ad1c-4312-ac33-2fa40d50a147/image.png)](https://www.credly.com/badges/ac9bf89a-a90f-470e-852d-1b45f42881c8)

**AWS Certified Machine Learning – Specialty**  
*Valid: January 2026 - January 2029*

</div>

---

I build **deterministic, scalable systems** where time, money, and data integrity are non-negotiable.  
6+ years architecting backend systems for healthcare, payments, and SaaS platforms.

[![PyPI](https://img.shields.io/badge/PyPI-2%20Packages-3775A9?style=for-the-badge&logo=pypi&logoColor=white)](https://pypi.org/user/rajatjog1294/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/rajat-jog/)

---

## 🎯 What I Do

I design **production-grade systems** where correctness, performance, and long-term maintainability are paramount.

**My expertise lies at the intersection of:**
- 🏗️ **Backend Architecture** — Django/DRF, FastAPI, PostgreSQL, RESTful API design
- 🤖 **Production ML** — Model deployment, feature engineering, monitoring (AWS SageMaker, local serving)
- ⚡ **Performance Engineering** — Database optimization, caching, async processing (reduced API response time by 60%)
- 🔒 **Domain Complexity** — Healthcare, payments, scheduling, audit trails, compliance systems

I don't just "make it work" — I architect systems that are:
- **Explicit over implicit** (state machines > boolean flags)
- **Safe by design** (database constraints, idempotency, auditability)
- **Evolution-friendly** (migrations without rewrites, backward compatibility)
- **Failure-aware** (retry logic, graceful degradation, observability)

---

## 🚀 Open Source Contributions

### Published on PyPI

#### 1. [django-system-audit](https://pypi.org/project/django-system-audit/) 
**Intent-aware audit trails for Django applications**

Solves the problem of tracking "who changed what, when, and why" in compliance-heavy systems.

```python
from django_system_audit import audit_event

@audit_event("USER_PASSWORD_RESET", capture_request=True)
def reset_password(user_id):
    # Automatically logs the event with user, timestamp, and request context
    user = User.objects.get(id=user_id)
    user.set_password(generate_random_password())
    user.save()
```

**Use Cases:**
- Healthcare/fintech compliance (HIPAA, SOC 2, audit trails)
- SaaS platforms with traceability requirements
- Internal tools requiring operational visibility

**Key Features:**
- Model-level change tracking
- User attribution & timestamps
- Query-optimized storage
- Compliance-ready exports
- Async logging (zero request overhead)

---

#### 2. [timeblocks](https://pypi.org/project/timeblocks/)
**Deterministic time block management for Django**

Built to eliminate timezone bugs, DST issues, and recurrence nightmares in scheduling systems.

```python
from timeblocks.services.series_service import SeriesService
from timeblocks.constants import RecurrenceType, EndType

# Create a recurring series (e.g., Monday/Wednesday/Friday classes)
series = SeriesService.create_series(
    owner=user,
    data={
        "start_date": date(2025, 1, 1),
        "start_time": time(10, 0),
        "end_time": time(11, 0),
        "timezone": "UTC",
        "recurrence_type": RecurrenceType.WEEKDAYS.value,
        "by_weekdays": ["MON", "WED", "FRI"],
        "end_type": EndType.AFTER_OCCURRENCES.value,
        "occurrence_count": 10,
    },
)
```

**Real-World Applications:**
- Appointment booking (healthcare, consulting, services)
- Resource scheduling (rooms, equipment, workstations)
- Availability management (staff, venues)
- Shift planning & workforce management

**Design Principles:**
- **Deterministic:** Same input = same output (always)
- **Database-safe:** Constraints prevent conflicts
- **Timezone-aware:** No DST surprises
- **Overlap detection:** Built-in conflict resolution
- **Explicit recurrence rules:** No hidden magic

---

## 💼 Professional Experience Highlights

### Current Role: Senior Software Engineer @ Mindbowser Inc
*Nov 2022 – Present*

- **Team Leadership:** Mentor 5+ backend engineers, own system architecture and delivery execution
- **Performance Engineering:** Reduced API response time by ~60% through PostgreSQL query optimization, indexing strategies, and intelligent caching
- **Integration Architecture:** Designed and implemented Stripe, SendGrid, and Shopify integrations with reliability and security as core requirements
- **Tech Stack:** Python, Django/DRF, FastAPI, PostgreSQL, AWS (S3, EC2, Lambda, CloudWatch)

**Recognition:**
- 🏆 "Going Above and Beyond" Award (Oct 2024)
- 🤝 "Team Player" Award (Dec 2025)

### Previous Experience

**KiwiTech** — Software Engineer (Apr 2022 – Nov 2022)
- Built RESTful APIs and backend services for core workflows
- Implemented async task processing with Celery for notifications and email systems
- Designed event management module for time-based operations

**Other Roles:** Python Developer positions at KSBS Group, RedBytes Softwares, Laxmi Civil Engg.
- E-commerce platforms, CMS development, web scraping pipelines
- Team leadership (led 3-engineer team on e-commerce delivery)
- Automation (monthly financial reporting, data aggregation systems)

---

## 🧠 Technical Stack

### Backend & Systems
![Python](https://img.shields.io/badge/Python-Expert-3776AB?style=flat&logo=python&logoColor=white)
![Django](https://img.shields.io/badge/Django-Expert-092E20?style=flat&logo=django&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Expert-4169E1?style=flat&logo=postgresql&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-Advanced-009688?style=flat&logo=fastapi&logoColor=white)

**Core Competencies:**
- Python, Django, Django REST Framework, FastAPI
- PostgreSQL (query optimization, indexing, migrations, constraints)
- REST API design & backend system architecture
- Celery (async processing, distributed task queues)
- Redis (caching, rate limiting, session management)

### Machine Learning & Data
![AWS](https://img.shields.io/badge/AWS-ML%20Certified-FF9900?style=flat&logo=amazon-aws&logoColor=white)

**ML Engineering:**
- Applied/Production ML (not research-focused)
- Data pipelines & feature engineering
- Model deployment & monitoring
- AWS SageMaker, EC2, Lambda
- ML system design & MLOps patterns

**Philosophy:** I treat ML components as **stateful system dependencies**, not magic functions.  
Focus: Correctness, observability, safe rollbacks, business-aligned metrics.

### DevOps & Infrastructure
- AWS (S3, EC2, Lambda, IAM, CloudWatch, SageMaker)
- Docker, CI/CD pipelines
- Server maintenance & deployment workflows
- Database migration strategies

### Domain Expertise
**High-Stakes Systems:**
- **Payments** — Stripe integration, idempotent charges, refund state machines
- **Healthcare** — Compliance-heavy systems, audit trails, data privacy
- **Scheduling** — Booking engines, time slot modeling, timezone handling
- **E-commerce** — Shopify integration, product catalogs, order management

---

## 🎯 Engineering Philosophy

I optimize for **systems that survive contact with reality**:

### Design Principles
- ✅ **Explicit state transitions** over implicit side effects
- ✅ **Database truth** > service assumptions  
- ✅ **Idempotency** everywhere it matters
- ✅ **Fail loudly**, log clearly, recover deterministically
- ✅ **Documentation as part of the system**, not an afterthought

### What Sets Me Apart
Most backend engineers specialize in 2-3 areas. I operate across **7+ domains**:
1. API design & implementation
2. Database optimization & schema design
3. Infrastructure (AWS services, deployments)
4. Async processing (Celery, background jobs)
5. Third-party integrations (payments, email, e-commerce)
6. ML system deployment & monitoring
7. Performance engineering & profiling

This makes me valuable for **end-to-end ownership** of complex systems.

---

## 📊 Current Focus

🔬 **Exploring:** MLOps patterns, distributed systems, Kubernetes  
🛠️ **Building:** Production ML tools that don't require cloud lock-in  
✍️ **Writing:** Technical deep-dives on backend architecture & performance  
🎯 **Learning:** Advanced system design patterns and distributed architectures

---

## 📈 GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=RJ-Gamer&show_icons=true&theme=radical&hide_border=true&count_private=true)

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=RJ-Gamer&layout=compact&theme=radical&hide_border=true)

---

## 🏆 Certifications

- **AWS Certified Machine Learning – Specialty (MLS-C01)** — *Valid: Jan 2026 - Jan 2029*
  - Data engineering for ML
  - Exploratory data analysis
  - Modeling (algorithms, hyperparameter tuning)
  - ML implementation & operations

---

## 📚 What I Write About

When I extract reusable patterns from production work, I share them:

- 🔍 **Performance optimization** — How I achieved 60% response time reduction
- 🏗️ **System design patterns** — Building audit-safe, compliance-ready systems  
- 🤖 **Production ML** — Deploying ML without breaking the bank (local alternatives to AWS)
- ⚙️ **Django deep-dives** — Query optimization, Celery patterns, API design

*Coming soon: Technical blog with case studies from real production systems.*

---

## 🤝 Let's Connect

I'm always interested in discussing:
- Complex backend architecture challenges
- Production ML system design
- Open source collaboration
- Performance engineering war stories

📧 **Email:** rajatjog1294@gmail.com  
💼 **LinkedIn:** [linkedin.com/in/rajat-jog](https://www.linkedin.com/in/rajat-jog/)  
📦 **PyPI:** [pypi.org/user/rajatjog1294](https://pypi.org/user/rajatjog1294/)  
🌐 **Location:** Pune, India

---

## 💡 Fun Facts

- 🎮 GitHub username "RJ-Gamer" because I started coding through game development
- 🏗️ I think about software like infrastructure, not experiments
- 📦 I've published 2 PyPI packages (with more in the pipeline)
- 🚀 My code has handled millions of transactions in production healthcare and payment systems
- 🧩 I love solving "unsexy" problems: timezone bugs, race conditions, audit trails

---

<div align="center">

### 🌟 If you find my open-source work useful:

[![Star on GitHub](https://img.shields.io/github/stars/RJ-Gamer?style=social)](https://github.com/RJ-Gamer)
[![Sponsor](https://img.shields.io/badge/Sponsor-GitHub-ff69b4?logo=github&style=social)](https://github.com/sponsors/RJ-Gamer)
[![Follow on LinkedIn](https://img.shields.io/badge/Follow-LinkedIn-blue?style=social&logo=linkedin)](https://www.linkedin.com/in/rajat-jog/)

*"Code should be boring. Systems should be interesting."*

</div>
