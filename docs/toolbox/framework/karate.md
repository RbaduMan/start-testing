# Karate

> Karate is the only open-source tool to combine API test-automation, mocks, performance-testing and even UI automation into a single, unified framework. You don't have to compile (Java) code. Just write tests in a readable syntax.
>
> — [Official website](https://intuit.github.io/karate/)

## Code

Example of automation at [GitHub](https://github.com/rbaduman/start-testing/tree/main/code/framework/karate).

## Review

| Category          | Opinion |  Score   |
| ----------------- | ------- | :------: |
| _Use cases_       | Automate API tests. It also supports performance and end-to-end (E2E) tests. Mobile testing is in the roadmap. |    🥇    |
| _Learning curve_  | Steep. It's easy to understand how it works, but it lacks an official step-by-step tutorial where each main DSL keyword is introduced, one at a time. It feels like a framework made by and to "hardcore developers". The purpose of using Gherkin is to make the tools accessible to non-devs, yet I never felt productive or in control. |    🥈    |
| _Language_      | Tests are written in [Karate's DSL](https://hackernoon.com/yes-karate-is-not-true-bdd-698bf4a9be39). It uses the syntax of Gherkin and it adds some custom keywords and operators. It also supports calls to Java and JavaScript, outside the Given-When-Then structure. |    🥇    |
| _Ecosystem_       | The [VS Code extension](https://marketplace.visualstudio.com/items?itemName=kirkslota.karate-runner) didn't work at all (e.g. no autocomplete, no debugger, no run test button). In terms of community… there's not much since it's a recent tool. The author is an [enthusiastic](https://twitter.com/KarateDSL/status/1167533484560142336) salesperson which led to [some bad PR](https://twitter.com/jarbon/status/1136589061605416961), result of the "my tool is amazing, if you disagree you're against me" attitude. He's very active on Stack Overflow and GitHub though, replies within hours! |    🥉    |
| _Readability_     | It's easier to read than to know what to write. Without autocomplete or good documentation it becomes hard to know how to use the Karate DSL to achieve what you want to do. Your tests use Gherkin's structure, but you have to mix programming syntax too (e.g. operators, selectors). This [sums the downsides](https://club.ministryoftesting.com/t/karate-for-test-automation-what-is-your-experience/39336/2) of natural (e.g. no refactoring) and programming (e.g. learning curve) languages. The CLI output is very verbose (without colours or whitespace) so it's hard. The HTML report doesn't clear results from previous test runs. Oh, and the DSL doesn't allow inline comments. |    😭    |
| _Extensibility_   | You don't need plugins, since it follows the "batteries included" philosophy. Running tests in parallel is very easy. It includes Mocking, [code coverage](https://github.com/intuit/karate/tree/master/karate-demo#code-coverage-using-jacoco) and HTML reports (but it doesn't reset results between runs, even when using `--clean`, which makes the report useless). |    🥈    |
| _Maintainability_ | The [*big difference*](https://intuit.github.io/karate/#cucumber-vs-karate) from Cucumber is that you *don't* need to write extra "step definitions" (but you end up mixing Gherkin with programming). You can't use PageObjects, but you can centralise selectors in a `locators.json` to achieve DRY.  I could not debug at all, zero of features [advertised here](https://twitter.com/KarateDSL/status/1167533484560142336) worked for me (Cypress, even [Selenium](https://hackernoon.com/the-world-needs-an-alternative-to-selenium-so-we-built-one-zrk3j3nyr), does a better job). On top of that, I got [incoherent test results on UI automation](https://stackoverflow.com/questions/62308044/karate-ui-automation-test-results-are-not-coherent). |    😭    |
| _Documentation_   | Documentation is a single README file. It's verbose, exhaustive for beginners, hard to navigate and find what you are looking for. It feels like the official docs were written by the author but never revised from the perspective of a beginner (e.g. the provided quick start example fails; it can't be copied because it's an image; it was faster to skim blogs for examples and reverse-engineer the bits that I needed). |    🥉    |
| **VERDICT**       | Useful for [API testing](https://docs.google.com/document/d/1ETTrdMVcBXaPjdKY-_67zCWBsi2Ctc5DIQUIfr02H7A/edit), because it uses a generic language and can be executed as a standalone. But don't be fooled, the target audience are developers and it's not an alternative for UI/E2E tests. | **3/5** |
