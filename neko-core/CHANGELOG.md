# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.6.1](https://github.com/0xPlaygrounds/neko/compare/neko-core-v0.6.0...neko-core-v0.6.1) - 2025-01-13

### Added

- Add `from_url` method to Gemini client (#194)
- Feature flag for CF worker compatibility (#176) (#175)
- *(eternal-ai)* Eternal-AI provider for neko (#171)
- Add gpt-4o-mini to openai model list (#187)

### Fixed

- *(example)* ollama example uses wrong url

### Other

- Add additional check for empty tool_calls ([#166](https://github.com/0xPlaygrounds/neko/pull/166))
- Mock provider API in vector store integration tests (#186)
- fix comment (#182)
- fix various typos

## [0.6.0](https://github.com/0xPlaygrounds/neko/compare/neko-core-v0.5.0...neko-core-v0.6.0) - 2024-12-19

### Added

- agent pipelines (#131)
- *(neko-anthropic)* Add default `max_tokens` for standard models (#151)

### Fixed

- *(openai)* Make integration more general (#156)

### Other

- *(ollama-example)* implement example showcasing ollama (#148)
- *(embeddings)* add embedding distance calculator module (#142)

## [0.5.0](https://github.com/0xPlaygrounds/neko/compare/neko-core-v0.4.1...neko-core-v0.5.0) - 2024-12-03

### Added

- Improve `InMemoryVectorStore` API ([#130](https://github.com/0xPlaygrounds/neko/pull/130))
- embeddings API overhaul ([#120](https://github.com/0xPlaygrounds/neko/pull/120))
- *(provider)* xAI (grok) integration ([#106](https://github.com/0xPlaygrounds/neko/pull/106))

### Fixed

- *(neko-lancedb)* rag embedding filtering ([#104](https://github.com/0xPlaygrounds/neko/pull/104))

## [0.4.1](https://github.com/0xPlaygrounds/neko/compare/neko-core-v0.4.0...neko-core-v0.4.1) - 2024-11-13

### Other

- Inefficient context documents serialization ([#100](https://github.com/0xPlaygrounds/neko/pull/100))

## [0.4.0](https://github.com/0xPlaygrounds/neko/compare/neko-core-v0.3.0...neko-core-v0.4.0) - 2024-11-07

### Added

- *(gemini)* move system prompt to correct request field
- *(provider-gemini)* add support for gemini specific completion parameters
- *(provider-gemini)* add agent support in client
- *(provider-gemini)* add gemini embedding support
- *(provider-gemini)* add gemini support for basic completion
- *(provider-gemini)* add gemini API client

### Fixed

- *(gemini)* issue when additionnal param is empty
- docs imports and refs
- *(gemini)* missing param to be marked as optional in completion res

### Other

- Cargo fmt
- Add module level docs for the `tool` module
- Fix loaders module docs references
- Add docstrings to loaders module
- Improve main lib docs
- Add `all` feature flag to neko-core
- *(gemini)* add utility config docstring
- *(gemini)* remove try_from and use serde deserialization
- Merge branch 'main' into feat/model-provider/16-add-gemini-completion-embedding-models
- *(gemini)* separate gemini api types module, fix pr comments
- add debug trait to embedding struct
- *(gemini)* add addtionnal types from the official documentation, add embeddings example
- *(provider-gemini)* test pre-commits
- *(provider-gemini)* Update readme entries, add gemini agent example

## [0.3.0](https://github.com/0xPlaygrounds/neko/compare/neko-core-v0.2.1...neko-core-v0.3.0) - 2024-10-24

### Added

- Generalize `EmbeddingModel::embed_documents` with `IntoIterator`
- Add `from_env` constructor to Cohere and Anthropic clients
- Small optimization to serde_json object merging
- Add better error handling for provider clients

### Fixed

- Bad Anthropic request/response handling
- *(vector-index)* In memory vector store index incorrect search

### Other

- Made internal `json_utils` module private
- Update lib docs
- Made CompletionRequest helper method private to crate
- lint + fmt
- Simplify `agent_with_tools` example
- Fix docstring links
- Add nextest test runner to CI
- Merge pull request [#42](https://github.com/0xPlaygrounds/neko/pull/42) from 0xPlaygrounds/refactor(vector-store)/update-vector-store-index-trait

## [0.2.1](https://github.com/0xPlaygrounds/neko/compare/neko-core-v0.2.0...neko-core-v0.2.1) - 2024-10-01

### Fixed

- *(docs)* Docs still referring to old types

### Other

- Merge pull request [#45](https://github.com/0xPlaygrounds/neko/pull/45) from 0xPlaygrounds/fix/docs

## [0.2.0](https://github.com/0xPlaygrounds/neko/compare/neko-core-v0.1.0...neko-core-v0.2.0) - 2024-10-01

### Added

- anthropic models

### Fixed

- *(context)* displaying documents should be deterministic (sorted by alpha)
- *(context)* spin out helper method + add tests
- move context documents to user prompt message
- adjust version const naming
- implement review suggestions + renaming
- add `completion_request.documents` to `chat_history`
- adjust API to be cleaner + add docstrings

### Other

- Merge pull request [#43](https://github.com/0xPlaygrounds/neko/pull/43) from 0xPlaygrounds/fix/context-documents
- Merge pull request [#27](https://github.com/0xPlaygrounds/neko/pull/27) from 0xPlaygrounds/feat/anthropic
- Fix docstrings
- Deprecate RagAgent and Model in favor of versatile Agent
- Make RagAgent VectorStoreIndex dynamic trait objects

## [0.1.0](https://github.com/0xPlaygrounds/neko/compare/neko-core-v0.0.7...neko-core-v0.1.0) - 2024-09-16

### Added

- add o1-preview and o1-mini

### Fixed

- *(perplexity)* fix preamble and context in completion request
- clippy warnings

### Other

- Merge pull request [#18](https://github.com/0xPlaygrounds/neko/pull/18) from 0xPlaygrounds/feat/perplexity-support
- Add logging of http errors
- fmt code
