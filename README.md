# UNO-SF — Manifest


UNO-FF is a protocol-driven engine for processing wicked problems through structured cognitive cycles (C1 → C2 → C3 → D1), with optional escalation via UNO-F.


* * *


## New Paradigm: From Prompts to Protocols


Classical usage: ask → get an answer.  
UNO-SF: define the conflict → expose assumptions → reframe → translate into action.


What matters is not the final answer — but the trace of cognition.


* * *


## Core Architecture


```mermaid
flowchart LR
  P[Problem] --> C1[C1: Perception]
  C1 --> C2[C2: Autoreflection]
  C2 --> C3[C3: Recontextualization]
  C3 --> D1[D1: Deployment]
  C2 -->|stuck / paradox| UF[UNO-F: Higher-order problem]
  C3 -->|recursion| C1

C1: chaos_bundle + vital_contradiction
C2: hypotheses + correction_vector + commit_2
C3: new_frame + commit_3
D1: metaphor + strategy_one_liner + ELI5
UNO-F: escalation to higher-order problem + ghost_log

Repository Structure

protocol/ — UNO-SF protocol definition (versioned)

problems/ — 9 problems as experiment suites

each problem contains multiple model runs (Gemini / Claude / DeepSeek / ...)

media/ — YouTube links + timestamps mapped to cycles

WHITEPAPER.md — full theory and methodology

Quickstart (Reading the Data)

Pick a problem: problems/P01_.../problem.md

Compare models: problems/P01_.../models/<model_name>/

Read the synthesis: problems/P01_.../summary.md

Example: Same Protocol, Different Minds

Problem: <one-liner>
Models compared: <e.g., Gemini vs Claude>
Key divergence: <e.g., C1 vital_contradiction vs C2 correction_vector>

(put 10–20 lines of the most instructive fragments + your 3-line observation)

Metaphor

UNO-FF is a control panel for contradictions: it doesn’t hide instability — it measures it, routes it, and turns it into usable action.

Learn More

WHITEPAPER.md

protocol/

problems/

https://www.youtube.com/playlist?list=PLKivBaAOXsDA_udknrFjc1n69BHox9XWO
