# Publish the prepared source repository

The local repository is in `caprae-lead-workbench/`, on branch `main`. The initial commit is `4534cec8172f54844e478b634394572b3af8a59d`. `LeadBench_Source.bundle` contains the complete Git history and has been verified with `git bundle verify`.

No repository was published to an external GitHub account in this session. No authenticated GitHub publishing tool was available. The source is ready for publication; the original private handbook and runtime SQLite files are excluded.

## Recover from the portable bundle

From the extracted submission package:

```sh
git clone LeadBench_Source.bundle leadbench
cd leadbench
```

Alternatively, use the already initialized `caprae-lead-workbench` folder directly.

## Publish to your account

Create an empty repository in your authenticated GitHub account. Then use its actual URL:

```sh
git remote add origin https://github.com/YOUR_ACCOUNT/YOUR_REPOSITORY.git
git push -u origin main
```

Replace the account and repository placeholders. If the repository is private, give the reviewer access before submitting the link. The code's initial author is recorded as Codex, reflecting the AI-assisted implementation; review the system and documentation so you can explain the decisions in your interview.

Keep your resume, work authorization details, salary, and customer data outside the source repository. Complete the applicant fields and final links in the submission materials before sending the prepared recruiting email.
