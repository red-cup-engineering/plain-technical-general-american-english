# plain-technical-general-american-english

<!-- 561-group-standards:badges:start -->
[![Red Cup Engineering](https://img.shields.io/badge/561%20Group-Red%20Cup%20Engineering-c0392b)](https://github.com/red-cup-engineering)
[![License: MIT](https://img.shields.io/badge/license-MIT-c0392b)](LICENSE)
[![Indigenous data: CARE](https://img.shields.io/badge/Indigenous%20data-CARE-4b6f44)](https://github.com/red-cup-engineering/.github/blob/main/GOVERNANCE.md)
[![Tips welcome](https://img.shields.io/badge/tips-welcome-d4a017)](https://github.com/561-group/.github/blob/main/TIPS.md)
<!-- 561-group-standards:badges:end -->

Versioned PTGAE language fibers for the 561 language engine.

## Selected review-only rewrite fiber

`fibers/safe-rewrite-rules.json` is the versioned, locale-qualified source for the **two existing** PTGAE review proposals: `PTG004` (`in order to`) and `PTG010` (`due to the fact that`). Both use the literal `action: "propose-for-review"`. This is an opt-in policy fiber, not an implicit English grammar or a statement that either substitution preserves meaning.

The original `ptgae-language-fiber-service` loads it as the optional `safeRewriteRules` resource, carrying the selected policy's version and parsed-content SHA-256 in its receipt. A consuming prose reviewer must withhold the candidate when this resource is missing or when any proposed rule is not explicitly admitted. The consuming `ptgae-engineering-services-section/fiber-review` API does so while retaining original UTF-16 source spans and separating selection, lint findings, and human review. It does not authorize execution or publishing.

The package export is `@561-group/plain-technical-general-american-english/fibers/safe-rewrite-rules`. Existing consumers that supply only the original required fibers remain legitimate **partial selections**; they do not silently inherit the optional rewrite permissions. Source hashes identify supplied parsed JSON content, not authenticated upstream custody, semantic truth, or editorial sign-off.
