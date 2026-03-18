# Entity Ontology Policy

## Entity Types

| Prefix | Meaning |
|--------|--------|
| art_   | artifact |
| creat_ | creature |
| pers_  | person |
| loc_   | place / location |
| org_   | organization |
| factn_ | faction |
| play_  | player |
| ref_   | reference / external figure |
| off_   | office |
| role_  | role |

---

## General Rule

Only `off_` and `role_` use a structured internal ontology beyond the entity-type prefix.

Most other entity IDs are simply:

`<entity_type><name_or_key>`

Examples:
- `pers_henry`
- `loc_dhassa`
- `org_folly`
- `factn_krach-ul`

---

## Office Ontology

**Pattern:** `off_<auth>_<org>_<qualifier>`

### Authority Types

| Authority | Meaning |
|-----------|---------|
| lead_     | overall executive |
| dpty_     | deputy / 2nd in command |
| ops_      | operational leader |

---

## Role Ontology

**Pattern:** `role_<domain>_<org>_<qualifier>`

### Domain Types

| Domain | Meaning |
|--------|---------|
| adm_   | administrative / coordination |
| intel_ | intelligence / covert / investigative |
| logis_ | logistics / supply / transport |
| eng_   | engineering / construction / maintenance |
| med_   | healing / medical / care |
| arc_   | arcane / magical |
| recon_ | scouting / tracking / field intelligence |
| rng_   | ranged combat |
| cmb_   | combat (general / frontline) |
| craft_ | artisan / skilled making |
| ops_   | general operations / support |

---

## Unit-Level Entities (Squads, Teams)

Small operational units (e.g., squads) are modeled as `org_` entities.

- Pattern: `org_<parent>_squad_<leadername>`
- Units belong to a parent org or faction via `current_member_of`
- Unit leaders are modeled with `off_lead_<unit>`
- Members belong to the unit via `current_member_of`

