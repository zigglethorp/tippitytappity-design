# tippitytappity-design

tippitytappity is a program to practice typing


## Data model

```mermaid
classDiagram
  TypingSession <|-- Phrase
  class Phrase{
        - id: string
        - Text: string
        - Source: string
        + difficultyRatting: string
  }
  TypingSession <|-- RandomPhraseRepo
  class RandomPhraseRepo{
        + Phrase: string
        + nextPhrase: string
}
  TypingSession <|-- ScoringService
  class ScoringService{
        + accuracy: double
        + wpm: double
  }
  TypingSession <|-- TimerService
  class TimerService{
        + startPhase(): datetime
        + stopPhrase(): datetime
        + resetTimer: void 
        + accuracy: double
        + durration: sessionElapsed
  }

  class TypingSession{
        + start(): void
        + submit: void
        + next(): void
        + preveous(): void
  }

```
