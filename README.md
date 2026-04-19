# Sanskrit Study Tool

An interactive offline Sanskrit study application. No installation, no server — just open `index.html` in any browser.

## Files

| File | Description |
|------|-------------|
| `index.html` | Main app — Dhatu, Vibhakti, and Notes study tools |
| `vocab-study.html` | Vocabulary study tool with 3,000 words |
| `gen_vocab.py` | Python data source — all 3,000 word entries; run to regenerate `vocab-study.html` |

---

## Features

### Dhatu (Verb Roots)
- **Browse** — Filter by Gana (verb class), Pada (Parasmaipada / Atmanepada / Ubhayapada), and Lakara (tense/mood). Full-text search.
- **Flashcards** — Drill conjugation forms with the same filter controls. Track learned/unlearned progress per root.
- **Quiz** — Multiple-choice quiz drawn from your filtered set. Start / Stop / Reset controls. Score tracked per session.
- **Progress** — Visual progress bars showing how many roots you have mastered.

### Shabda / Vibhakti (Noun Forms)
- **Browse** — Filter by Category and Gender. Full-text search.
- **Flashcards** — Drill Vibhakti forms. Unlearned toggle. Progress tracking.
- **Quiz** — Multiple-choice quiz on Vibhakti forms. Filter by Category and Gender before starting.
- **Progress** — Learned/unlearned breakdown per shabda.

### Helpful Notes
Structured study notes covering:
- Varnamala — Svaraha, Vyanjannni, Ayogavahah
- Word Structure — Suptiganta Padam, Sarvanamani, Vibhakti overview
- Lakara — Parasmaipada & Atmanepada Examples
- Sandhi rules
- Avyayani (indeclinables) — comprehensive merged table

### Vocabulary Study (`vocab-study.html`)

**3,000 words** — English with Sanskrit (Devanagari + IAST), grammatical gender (m./f./n.), word type, category, and difficulty.

| Level | Count |
|-------|-------|
| Common | 1,374 |
| Uncommon | 1,386 |
| Harder | 240 |
| **Total** | **3,000** |

**Categories covered:** nature, body, health, family, animals, food, household, clothing, travel, social, emotions, concepts, learning, descriptions, work, professions, sports, arts, music, ritual, deities, sacred texts, grammar, aesthetics, yoga, ayurveda, philosophy, cosmology, and more.

**Study modes:**
- **Browse** — Filter by difficulty, category, word type; search by English or transliteration.
- **Flashcards** — Flip cards EN→Sanskrit or Sanskrit→EN. Shuffle, mark learned.
- **Spelling Bee** — See the English word, type the correct IAST transliteration. IAST keyboard included. Score and streak tracking.
- **Quiz** — 4-option multiple-choice. EN→Sanskrit or Sanskrit→EN.
- **Progress** — Learned/remaining by difficulty and category. Export progress as JSON.

Word data sourced from learnsanskrit.cc (Monier-Williams) and ashtadhyayi.com.

#### Regenerating `vocab-study.html`

```bash
python gen_vocab.py
```

Requires Python 3. Reads the existing `vocab-study.html` for its app shell and rewrites the `WORDS` array with the latest data from `gen_vocab.py`.

---

## How to Use

1. Download or clone this repository.
2. Open `index.html` in any modern browser (Chrome, Firefox, Edge, Safari).
3. No internet connection required after download.
4. Progress is saved automatically in your browser's `localStorage`.

---

## Data Sources

- Dhatu data compiled from authority sources
- Shabda data compiled from authority sources
- Vocabulary data from learnsanskrit.cc and ashtadhyayi.com (Monier-Williams Dictionary)
- Helpful Notes from personal study notes
