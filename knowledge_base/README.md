# Knowledge base – Raiffeisen Family Agent

Baza de cunoștințe pentru cele 3 fluxuri (P5). Un fișier JSON per flux, toate cu aceeași structură.

| Fișier | Flux |
|---|---|
| `kb_deces_succesiune.json` | Deces / Succesiune |
| `kb_casatorie_divort.json` | Căsătorie / Divorț |
| `kb_imputernicire.json` | Împuternicire |

## Structura unui fișier

- `flux_id`, `nume`, `cuvinte_cheie` – după ce recunoaște agentul situația (P1)
- `ton`, `intrebari_de_clarificare` – cum vorbește agentul (P1)
- `scenarii` – ce acte trebuie în fiecare situație (`acte_necesare`, `acte_optionale`)
- `acte[].campuri_cheie` – ce câmpuri se extrag din fiecare act (P2)
- `acte[].reguli_validare` – verificări pe un singur act (P3)
- `crosscheck` – verificări între acte, cu severitate `eroare` / `avertisment` (P3)
- `pasi`, `sfaturi`, `faq` – conținut pentru răspunsuri (P1)
- `trimite_la_consilier_cand` – când agentul nu răspunde și trimite la sucursală
- `surse` – de unde vine informația

Informațiile sunt bazate pe surse publice și trebuie confirmate la sucursală. Agentul răspunde doar din aceste fișiere.
