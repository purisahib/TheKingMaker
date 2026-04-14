# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a creative writing project — a long-form epic novel titled **"The Rise of Samrat: The King Maker (सम्राट का उदय: राजा बनाने वाला)"**, written in pure Hindi. There is no software codebase; the repository contains the story brief, character sheet, season outlines, and generated story pages.

## Repository Layout

- `Prompts` — Master brief (original requirements, do not edit).
- `CLAUDE.md` — This file (writing rules and guidance).
- `List of Characters.txt` — सभी पात्रों के पूरे नाम, रूप-रंग, स्वभाव, पृष्ठभूमि, संबंध। **नया पात्र आए तो यहाँ update करें।**
- `सीजन/` — 5 season outline files, each covering 160 episodes (800 episodes total):
  - `सीजन_1_अंधकार_का_जन्म.md` (अध्याय 001–160)
  - `सीजन_2_सत्ता_के_खेल.md` (अध्याय 161–320)
  - `सीजन_3_रक्त_और_आग.md` (अध्याय 321–480)
  - `सीजन_4_छाया_का_साम्राज्य.md` (अध्याय 481–640)
  - `सीजन_5_सम्राट_का_उदय.md` (अध्याय 641–800)
- `आउटलाइन` — additional outline notes.
- `अध्याय_NNN.md` — actual written story pages in repo root.
- `MyComment` — user's scratch notes.

## Workflow: Writing a New Chapter

Before writing any new `अध्याय_NNN.md`:

1. **List existing chapters** (`अध्याय_*.md` in repo root) and find the highest number.
2. **Read the latest chapter** in full — especially its `👉 अगले पृष्ठ की झलक:` hook at the end.
3. **Read the matching season file** in `सीजन/` to find that chapter's planned title + description.
4. **Read `List of Characters.txt`** for continuity on names, relationships, and established facts.
5. Write the new chapter as a **new file** `अध्याय_NNN.md` — never overwrite, never skip numbers.
6. If new characters appear, **update `List of Characters.txt`**.

## Writing Rules

- **Language**: Pure Hindi (हिंदी में लिखना है — Hinglish नहीं)। सभी पात्रों के नाम शुद्ध हिंदी/संस्कृत में।
- **Length target**: 800 अध्याय, हर अध्याय 3000+ शब्द। Write page by page — never summarize or skip ahead.
- **Setting**: प्राचीन/मध्यकालीन भारतीय शैली का राज्य (राज्य, राजा, महाराज, सेनापति, राजकुमारी आदि)।
- **Genre**: Action, Drama, Romance, War, Politics, Betrayal.
- **Tone**: Cinematic, dark, emotional, powerful — आशा, बदला, प्रेम, और नियति का मिश्रण।

## Page Structure

Every page must include:
1. Main story progression
2. Strong, natural dialogues
3. Detailed scene description
4. Emotional depth

End every page with:
```
👉 अगले पृष्ठ की झलक:
```
followed by a brief suspenseful hint of what comes next.

## Scene Types (हर तरह के दृश्य ज़रूरी)

कहानी में इन सभी प्रकार के दृश्यों का संतुलन होना चाहिए:

- **एक्शन दृश्य**: तलवारबाज़ी, युद्ध, पीछा, घात, द्वंद्व — विस्तृत, तेज़, cinematic।
- **रोमांटिक दृश्य**: रुद्र और मृगनयनी के कोमल क्षण — नज़रें, गुप्त मुलाक़ातें, पत्र।
- **प्रेम/शृंगारिक दृश्य**: गहरे भावनात्मक + शारीरिक जुड़ाव, शृंगार रस की परंपरा में (नीचे कठोर नियम देखें)।
- **भावनात्मक दृश्य**: दुख, क्रोध, विश्वासघात, मित्र-बिछोह।
- **राजनीतिक दृश्य**: दरबार की चालें, शब्दों का युद्ध, षड्यंत्र।
- **युद्ध दृश्य**: बड़ी लड़ाइयाँ, रणनीति, वीरता, बलिदान।

**संतुलन का नियम**: कोई सीजन केवल एक ही प्रकार के दृश्यों से न भरा हो। action के बाद romance, युद्ध के बाद कोमलता, षड्यंत्र के बाद मित्रता।

### ⚠️ शृंगारिक दृश्यों के कठोर नियम (अनिवार्य)

1. **आयु नियम (Absolute)**: कोई भी शृंगारिक/sensual/यौन दृश्य केवल तब लिखा जाएगा जब कहानी में **रुद्र और मृगनयनी दोनों 18 वर्ष या उससे अधिक** हों। सीजन 1 में दोनों नाबालिग हैं (15 और 16 वर्ष) — इसलिए सीजन 1 में कोई भी शृंगारिक दृश्य नहीं, केवल कोमल रोमांटिक क्षण (नज़रें, हाथ पकड़ना, पत्र, गुप्त मुलाक़ातें)। **यह नियम किसी भी परिस्थिति में नहीं तोड़ा जाएगा।**
2. **Time Jump**: सीजन 2 में कहीं time jump (2-3 वर्ष) आएगा जिससे दोनों वयस्क हो जाएँ — उसके बाद ही खुले शृंगारिक दृश्य शुरू हो सकते हैं।
3. **शैली नियम**: साहित्यिक **शृंगार रस** की परंपरा में (कालिदास, जयदेव का "गीत गोविंद", अमरुशतक) — गहरे, कामुक, खुले, काव्यात्मक। उपमाएँ, प्रकृति के बिम्ब (चंद्रमा, पुष्प, नदी, अग्नि)। भावना पहले, शरीर बाद में। pornographic/gratuitous शैली नहीं।
4. **केवल रुद्र और मृगनयनी के बीच।**

## Core Characters (पूरे नाम)

विस्तृत विवरण के लिए `List of Characters.txt` देखें।

| भूमिका | पूरा नाम | टिप्पणी |
|--------|----------|---------|
| नायक | **रुद्र प्रताप वर्मन** | 15 वर्ष, वर्मन वंश का अंतिम उत्तराधिकारी |
| दादा जी | **आचार्य शिवदत्त शर्मा** | पालनकर्ता, पूर्व राजगुरु |
| राजा | **महाराज उग्रसेन चंद्रवर्धन** | चंद्रकूट राज्य का शासक |
| राजकुमारी | **राजकुमारी मृगनयनी चंद्रवर्धन** | 16 वर्ष, बुद्धिमान, रुद्र की भावी प्रेमिका |
| खलनायक | **क्रूरसेन कालनाथ** | सेनापति (ऊपर से), काली विद्या का साधक, माता-पिता का हत्यारा |
| गुरु | **गुरु ज्ञानेश्वर त्रिकालदर्शी** | रहस्यमय मार्गदर्शक |

## Hero Arc (महत्वपूर्ण — शरीर ठीक होगा)

रुद्र की शारीरिक यात्रा का नियम:

- **अध्याय 001–010**: रुद्र अत्यंत कमज़ोर, सोचता है शरीर कभी ठीक नहीं होगा — इसलिए केवल **बुद्धि और रणनीति** से लड़ने का निर्णय।
- **अध्याय 010–046**: गुरु ज्ञानेश्वर का आगमन, रुद्र को पता चलता है कि **रक्त रक्षा फिर से जगाई जा सकती है**, वह "रक्त-रत्न" की खोज में निकलता है।
- **अध्याय ~047**: रुद्र को **रक्त-रत्न** मिलता है, शरीर धीरे-धीरे जागृत होने लगता है।
- **उसके बाद**: बुद्धि + शरीर **दोनों** का समानांतर विकास।
- **अध्याय ~754 (सीजन 5 climax)**: अंतिम महायुद्ध में रुद्र अपना रक्त-रत्न त्याग देता है — शरीर फिर कमज़ोर, पर आत्मा अमर।

पुराना नियम ("can never become physically strong") अब **बदल चुका है** — शरीर ठीक होगा, फिर अंत में फिर त्याग होगा।

## World & Lore

- **मुख्य राज्य**: चंद्रकूट (महाराज उग्रसेन का राज्य)
- **शत्रु राज्य**: अग्निकूट, विषकूट, ताम्रकूट
- **सहयोगी राज्य**: स्वर्णगिरि, नीलकूट (सीजन 5 में)
- **रुद्र का पैतृक राज्य**: वर्मन राज (विलुप्त, पिता आदित्य वर्मन — माता रानी चित्रलेखा)
- **तीन रत्न**: रक्त-रत्न, ज्ञान-रत्न, आत्म-रत्न — छायासम्राट को बाँधने के लिए आवश्यक
- **अंतिम शत्रु**: **छायासम्राट** — हज़ार वर्ष पुराना अमर काला साधक। क्रूरसेन और कालदेव उसके मोहरे हैं।
- **काली विद्या**: क्रूरसेन और उसके सहयोगियों की गुप्त शक्ति का स्रोत

## Season Roadmap

| सीजन | शीर्षक | अध्याय | मुख्य विषय |
|------|-------|-------|-----------|
| 1 | अंधकार का जन्म | 001–160 | कमज़ोर बालक, रक्त-रत्न की खोज, गाँव से चंद्रकूट |
| 2 | सत्ता के खेल | 161–320 | दरबार, प्रेम, पहला षड्यंत्र, पहला युद्ध (+ time jump → 18+) |
| 3 | रक्त और आग | 321–480 | कालदेव, दादा जी की मृत्यु, चंद्रकूट का पतन |
| 4 | छाया का साम्राज्य | 481–640 | छायासम्राट प्रकट, मीरा-अर्जुन-गुरु का बलिदान |
| 5 | सम्राट का उदय | 641–800 | महायुद्ध, अंतिम मोड़ (जुड़वाँ भाई शांत का रहस्य) |

## Continuity Rules

- Never skip pages or summarize future events.
- Track character arcs, plot threads, and established world details across pages.
- Before writing a new page, review the previous page AND the season file's entry for that chapter number.
- नए पात्र आएँ तो तुरंत `List of Characters.txt` update करें।
- पात्रों की उम्र, संबंध, मृत्यु — सब consistent रखें। किसी मर चुके पात्र को ग़लती से जीवित न दिखाएँ।
