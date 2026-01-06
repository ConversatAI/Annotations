# Annotator Instructions for Dataset Quality Assessment

## 1. Purpose of the Annotation Task

The objective of this annotation task is to evaluate the quality of conversational data and associated structured artifacts produced by the TopicGuidedChat (TGC) dataset, and to compare conversational quality against the Multi-Session Chat (MSC) dataset. Annotators were asked to assess:

- Conversational turns
- Knowledge graphs derived from conversations
- Question Answer (QA) pairs generated from new conversational turns or speaker-specific knowledge graphs

The evaluation focuses on quality assessment, not preference judgment, model comparison, or subjective stylistic taste.



## 2. Annotator Background and Preparation

- All annotators are NLP researchers with prior experience in conversational datasets, conversational AI systems, or language model evaluation.
- Before starting the task, annotators were provided with:
  - Written definitions of each evaluation metric
  - Scoring instructions using a standardized 0–100 scale
  - Worked examples illustrating high-quality and low-quality cases
- Annotators completed a small practice batch to familiarize themselves with the evaluation criteria before annotating the actual samples.



## 3. Data Presented to Annotators

Depending on the evaluation type, annotators were shown one or more of the following.

### Conversational Turns

- A complete multi-turn conversation between two speakers.
- Speaker identifiers were anonymized and abstract.
- No metadata about dataset origin was revealed during annotation.

### Knowledge Graphs (TGC only)

- A set of subject–relation–object triples derived from MSC dataset conversations.
- Triples were grouped by topic and speaker.


### QA Pairs (TGC only)

- A question and its corresponding answer.
- QA pairs are memory-grounded and generated from speaker-specific knowledge graphs or newly generated conversational turns.
- Questions involve speaker1 asking about its prior events or preferences, while speaker2 provides brief factual responses.
- Questions are grounded in either short-term conversational turns or long-term speaker knowledge graphs of speaker1.

Annotators were explicitly informed that:

- MSC does not contain knowledge graphs or QA pairs.
- Knowledge graph and QA evaluations apply only to TGC.
  
## 4. Scoring Scale

All metrics are rated on a continuous 0–100 scale, where:

- 0 represents extremely poor quality
- 50 represents acceptable but weak quality
- 100 represents excellent quality

The High, Medium, and Low descriptors used in the following sections serve as interpretive anchors on this shared numeric scale. Annotators assign numeric scores directly and are encouraged to use the full range of the scale rather than default or rounded values unless justified.



## 5. Evaluation Metrics and Definitions

### 5.1 Conversational Turn Evaluation

Annotators rated each conversation using the following five metrics.

#### Topic Consistency

Measures whether the conversation remains focused on a coherent topic throughout.

- High (80–100): All conversational turns remain clearly aligned with the main topic, with no irrelevant digressions.
- Medium (50–79): Minor topic drift, but the overall topic remains identifiable.
- Low (0–49): Frequent or severe topic shifts that break topical coherence.

Example

- High: A conversation about cooking consistently discusses recipes, ingredients, and cooking experiences.
- Low: A cooking conversation abruptly shifts to unrelated topics such as politics or personal finance.



#### Factual Correctness

Assesses whether statements in the conversation are factually accurate and internally consistent.

- High (80–100): All factual claims are correct or plausibly correct within the conversational context.
- Medium (50–79): Minor inaccuracies that do not affect overall understanding.
- Low (0–49): Multiple incorrect, contradictory, or implausible claims.

Example

- High: “I placed sixth in the 100m race” remains consistent across turns.
- Low: A speaker claims both to be allergic and not allergic to the same substance without clarification.



#### Completeness

Evaluates whether conversational turns adequately respond to prior turns and develop ideas fully.

- High (80–100): Responses are informative, directly address prior turns, and move the conversation forward.
- Medium (50–79): Responses are relevant but shallow or partially developed.
- Low (0–49): Responses are vague, incomplete, or fail to address the preceding turn.

Example

- High: A question about cooking technique is answered with specific steps or experiences.
- Low: A direct question is answered with a generic acknowledgment only.



#### Coherence

Measures logical flow and semantic continuity between consecutive conversational turns.

- High (80–100): Turns connect naturally and follow a clear conversational progression.
- Medium (50–79): Minor discontinuities but overall understandable.
- Low (0–49): Abrupt jumps, contradictions, or broken conversational flow.

Example

- High: A discussion about hobbies progresses logically from interests to specific activities.
- Low: Responses appear unrelated to immediately preceding turns.



#### Naturalness

Assesses how human-like, fluent, and conversational the dialogue feels.

- High (80–100): Language is fluent, natural, and appropriate for casual human conversation.
- Medium (50–79): Slightly stiff or repetitive but still readable.
- Low (0–49): Robotic phrasing, unnatural repetition, or awkward constructions.

Example

- High: “That sounds exciting, I would love to try that someday.”
- Low: Repetitive or template-like responses across multiple turns.



### 5.2 Knowledge Graph Evaluation (TGC only)

Annotators evaluated knowledge graphs using the following metrics.

#### Topic Consistency

Measures whether extracted triples align with the assigned topic.

- High (80–100): All triples clearly relate to the topic.
- Medium (50–79): Most triples relate to the topic, with minor noise.
- Low (0–49): Many triples are unrelated or loosely connected.



#### Factual Correctness

Evaluates whether triples accurately reflect facts stated or implied in the conversation.

- High (80–100): Triples correctly represent conversational content.
- Medium (50–79): Minor inaccuracies that do not significantly affect interpretation.
- Low (0–49): Triples misrepresent or hallucinate information.



#### Relevance

Assesses whether the selected triples are meaningful and useful for representing speaker knowledge.

- High (80–100): Triples capture salient and informative facts.
- Medium (50–79): Triples are partially informative or mildly redundant.
- Low (0–49): Triples are trivial, redundant, or uninformative.

Example

- High: “speaker1 likes jerk chicken”
- Low: Generic or redundant facts not contributing to memory representation



### 5.3 QA Pair Evaluation (TGC only)

Annotators rated QA pairs using the following metrics.

#### Factual Correctness

Measures whether the answer correctly responds to the question based on generated conversational turns or knowledge graphs.

- High (80–100): Answer is fully correct and unambiguous.
- Medium (50–79): Answer is mostly correct but partially incomplete or imprecise.
- Low (0–49): Answer is incorrect, unsupported, or misleading.


#### Relevance

Assesses whether the question is meaningful and grounded in generated conversational turns or knowledge graph context of speaker1.

- High (80–100): The question probes relevant memory or prior information specific to speaker1.
- Medium (50–79): The question is loosely related to speaker1’s context but does not probe central or salient information.
- Low (0–49): The question is trivial, vague, or unrelated to speaker1’s conversational or knowledge context.

Example

- High: “What dish do I like to cook?” grounded in speaker1’s conversational context with a correct answer from speaker2.
- Low: Questions unrelated to any facts stated about speaker1.


## 6. Annotation Procedure

- Each sampled item was independently rated by multiple annotators.
- Annotators worked independently without discussion.
- Final scores reported in the paper are obtained by averaging scores across annotators for each metric.



## 7. Additional Notes and Constraints

- Annotators were instructed not to penalize stylistic differences unless they affected clarity or correctness.
- No real personal data is present in any sample.
- All speaker references are abstract and anonymized.
- Annotators were not informed whether a sample originated from TGC or MSC during evaluation of conversational turns.

