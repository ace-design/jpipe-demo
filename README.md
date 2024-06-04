# Modelling justification diagrams using jPipe

  - Authors:
    - Sébastien Mosser, Associate Professor, McMaster University, McMSCert
    - Nirmal Chaudhari, BEng Student, McMaster University, McScert

## Abstract

_Justification models are an approach to supporting accreditation, validation, or certification in a lightweight way. Usually, when engineers work on pipelines (e.g., CI/CD, machine learning, notebooks), their primary focus is on the pipeline itself, and the justification of why this pipeline is the right one for their software is, at best, part of the documentation. This leads to operational/maintenance problems: is your machine learning pipeline reusable? What is the purpose of that “weird” step in your CI/CD pipeline that you have no idea why it’s there, but the pipeline fails if you remove it? With jPipe, we operate under the assumption that pipeline justification should be easy, and support both the initial modelling of a pipeline and its incremental evolution. In this demo, we’ll present how the jPipe compiler can be used to model a justification diagram, how composition algorithms can be used to support incremental evolution, and showcase some research leads we’re planning to investigate to make justifications first-class citizen in the development process._

## Getting jPipe on your computer

- Option 1: use the provided JAR file
  - This repository comes with a release of the compiler, in the `bin` repository.
- Option 2: get the latest version from jPipe website
  - https://github.com/ace-design/jpipe
- Option 3: use the VS code extension
  - https://marketplace.visualstudio.com/items?itemName=mcscert.jpipe-extension
    - Warning: current version only works "out of the box" with a Mac.
    - if you're not on a mac, see instructions below.

## Running the demo

  - Justification files are in the `models` directory
  - compilation instructions are inside each model
  - Refer to `slides.pdf` to get the _story-telling_ of the demo

## Recorded demonstration

This material was presented as part of the _Research Demonstration_ series of MDE Net on June 6, 2024.

## Appendix

### Recompiling the language server

1. Clone the jPipe repository
    - https://github.com/ace-design/jpipe/
2. Go to the `lsp/language-server-jpipe` directory
3. compile the rust code using cargo
    - `$ cargo build --release`
4. Copy the langaue server executable into your local extension:
    - executable: `lsp/language-server-jpipe/target/release`
    - local extension: `~/.vscode/extensions/mcscert.jpipe-extension-0.1.0/`


