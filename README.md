# Resume Buddy

Resume Buddy is an AI-assisted resume tailoring skill designed to help job seekers analyze job descriptions, identify the most relevant experience, and generate concise, defensible, role-specific resume content.

It is built as a modular workflow that separates career knowledge, job analysis, resume generation, and human review. The goal is not to create generic AI-written resumes, but to produce tailored resumes grounded in verified experience and aligned with the language, priorities, and evaluation criteria of each target role.

## What It Does

Resume Buddy helps users:

* Analyze a job description and extract its core responsibilities, skills, seniority signals, and hiring priorities
* Rewrite resume summaries and experience bullets for a specific role
* Prioritize the most relevant achievements while keeping the resume concise
* Generate structured resume content for final editing in tools such as Google Docs

## Core Principles

### Evidence First

Every resume statement should be grounded in documented experience, responsibilities, outcomes, or metrics.

Resume Buddy should never invent:

* Work experience
* Metrics
* Technical skills
* Clients
* Responsibilities
* Leadership scope
* Business impact

### Tailoring, Not Fabrication

The system improves relevance through framing, prioritization, terminology, and structure. It does not change the underlying facts.

### Human-in-the-Loop

Resume Buddy is designed to support, not replace, human judgment. The user should review the generated content for factual accuracy, tone, emphasis, and final formatting.

### Separation of Knowledge and Logic

The skill itself contains the resume-tailoring workflow. Personal career information should remain in a separate private knowledge base whenever possible.

A recommended setup is:

```text
violetOS
└── Career
    └── Resume-Knowledge-Base
        ├── Master-Experience-Archive.md
        ├── Metrics-and-Achievements.md
        ├── Skills-Taxonomy.md
        ├── Target-Roles.md
        └── Resume-Writing-Principles.md

resume-buddy
├── SKILL.md
├── README.md
├── prompts
├── templates
├── examples
└── tests
```

In this structure:

* `violetOS` acts as the source of truth
* Resume Buddy acts as the reasoning and execution layer
* Google Docs acts as the final review and formatting space

## Workflow

Resume Buddy follows a structured multi-step process.

### 1. Job Description Analysis

The job description is broken down into:

* Core responsibilities
* Required and preferred qualifications
* Role-specific terminology
* Business objectives
* Stakeholder expectations
* Technical requirements
* Leadership and seniority signals
* Likely evaluation criteria

### 2. Candidate Evidence Retrieval

The system reviews the candidate's career knowledge base and identifies:

* Directly relevant experience
* Transferable experience
* Relevant metrics and outcomes
* Industry and domain knowledge
* Product, technical, and commercial capabilities
* Experience that should be deprioritized or removed

### 3. Fit and Gap Analysis

Resume Buddy compares the job description with the candidate profile to determine:

* Strong matches
* Partial matches
* Transferable strengths
* Missing qualifications
* Potential credibility risks
* Recommended positioning

### 4. Resume Strategy

Before rewriting, the system defines:

* The candidate's strongest positioning for the role
* Which experiences should receive the most space
* Which keywords should be incorporated naturally
* Which bullets should be rewritten, shortened, or removed
* What the summary should emphasize

### 5. Resume Generation

The system produces role-specific content such as:

* Professional summary
* Experience bullets
* Skills section
* Selected project descriptions
* Optional cover letter or recruiter introduction

### 6. Quality Review

The final output is checked for:

* Factual accuracy
* Relevance to the job description
* Unsupported claims
* Repetition
* Generic language
* Excessive jargon
* Resume length
* Clarity and readability
* Interview defensibility

## Repository Structure

```text
resume-buddy/
├── README.md
├── SKILL.md
├── skill.yaml
│
├── prompts/
│   ├── jd-analyzer.md
│   ├── experience-matcher.md
│   ├── resume-strategist.md
│   ├── resume-writer.md
│   └── resume-reviewer.md
│
├── templates/
│   ├── candidate-profile-template.md
│   ├── job-description-template.md
│   ├── resume-output-template.md
│   └── evaluation-schema.md
│
├── examples/
│   ├── fictional-candidate-profile.md
│   ├── sample-job-description.md
│   └── sample-output.md
│
├── tests/
│   ├── test-cases.md
│   └── evaluation-rubric.md
│
├── docs/
│   ├── architecture.md
│   ├── workflow.md
│   └── design-decisions.md
│
├── .gitignore
└── LICENSE
```

## Inputs

Resume Buddy works best when provided with the following inputs.

### Required

* Target job description
* Current resume
* Structured experience archive

### Recommended

* Verified career metrics
* Skills inventory
* Target role preferences
* Resume length requirements
* Geographic or industry preferences
* Writing and tone preferences
* Previous resume versions
* Feedback from recruiters or hiring managers

## Example Input

```text
Target role:
Technical Account Manager

Resume constraints:
- Maximum one page
- Do not invent experience or metrics
- Prioritize enterprise AI, product adoption, and stakeholder management
- Maintain a concise and professional tone

Candidate knowledge sources:
- Master-Experience-Archive.md
- Metrics-and-Achievements.md
- Skills-Taxonomy.md
- Current-Resume.md
```

## Example Output

```text
Professional Summary

AI product and solutions leader with 7+ years of experience spanning enterprise product adoption, digital transformation, and global go-to-market execution across China, North America, and the Middle East. Combines architecture-trained systems thinking with hands-on experience translating complex customer needs into scalable product, implementation, and growth strategies.
```

The generated content should always remain traceable to the candidate's verified experience.

## Evaluation Criteria

Resume Buddy outputs can be evaluated across the following dimensions:

| Dimension       | Evaluation Question                                         |
| --------------- | ----------------------------------------------------------- |
| Relevance       | Does the content clearly address the target role?           |
| Accuracy        | Is every statement supported by candidate evidence?         |
| Specificity     | Does the resume use concrete responsibilities and outcomes? |
| Prioritization  | Are the most relevant experiences given the most emphasis?  |
| Clarity         | Is the writing concise and easy to scan?                    |
| Credibility     | Can the candidate defend each statement in an interview?    |
| ATS Alignment   | Are important job-description terms included naturally?     |
| Differentiation | Does the resume communicate a clear competitive advantage?  |

## Privacy and Security

Do not commit sensitive personal information to a public repository.

The following files should remain private or be excluded through `.gitignore`:

* Real resumes containing phone numbers or email addresses
* Personal career archives
* Confidential company information
* Private job applications
* Client names that cannot be publicly disclosed
* API keys
* Local configuration files
* Unredacted evaluation data

Public examples should use fictional or anonymized candidate information.


## Current Status

Resume Buddy is an evolving personal AI workflow and portfolio project.

Current development priorities include:

* Improving job-description decomposition
* Building a more reliable evidence-retrieval workflow
* Adding structured resume evaluation
* Testing output consistency across different models
* Improving one-page resume prioritization
* Connecting the skill with a private career knowledge base
* Supporting final export and review workflows in Google Docs


## Intended Use

Resume Buddy is intended for:

* Personal resume tailoring
* Career portfolio experimentation
* AI skill development
* Prompt and agent workflow research
* Human-in-the-loop career support

It is not intended to make hiring decisions or automatically submit job applications without user review.

## License

Add the appropriate license based on how you plan to share and reuse the project.

For an open-source project, the MIT License is a common option.

For a personal or private project, you may choose to omit the license or include an explicit all-rights-reserved notice.

## Author

Created by Violet Ding as part of the broader `violetOS` personal knowledge and AI workflow system.
