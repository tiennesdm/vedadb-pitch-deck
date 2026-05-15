# AGENT_MEMORY.md - vedadb-pitch-deck

> **Repository**: `tiennesdm/vedadb-pitch-deck`
> **Branch**: `master`
> **Visibility**: PRIVATE
> **Last Updated**: 2025-01-16
> **Purpose**: Full pitch deck v2 (18 slides) for VedaDB investor presentations

---

## What This Repo Is

An 18-slide investor pitch deck for VedaDB fundraising. This is the **expanded v2 version** of the pitch deck, more comprehensive than the 12-slide version in `vedadb-pitch`. It includes additional slides on team, detailed competitive analysis, and more thorough market coverage.

This repo contains not only the pitch deck itself but also supporting materials: a YAML configuration file for VedaDB, the developer's resume, and competitive landscape research.

---

## File Count & Structure

**Total Files**: 31

```
vedadb-pitch-deck/
├── vedadb.pptd                # Main PPTD presentation file (v2)
├── README.md                  # Project overview
├── outline.md                 # Detailed content outline for all 18 slides
├── design.md                  # Visual design specification
├── competitive_analysis.md    # Competitive analysis summary
│
├── pages/                     # Individual slide content files (20 files)
│   ├── p01_cover.page
│   ├── p02_toc.page           # Table of Contents (v2 addition)
│   ├── p03_ch1_problem.page
│   ├── p04_data_chaos.page    # Data chaos illustration
│   ├── p05_ch2_solution.page
│   ├── p06_vedadb_overview.page
│   ├── p07_ch3_market.page
│   ├── p08_tam_sam_som.page   # Detailed market sizing
│   ├── p09_ch4_competition.page
│   ├── p10_competitive_matrix.page
│   ├── p11_why_vedadb.page
│   ├── p12_ch5_product.page
│   ├── p13_architecture.page
│   ├── p14_ch6_business.page
│   ├── p15_business_model.page
│   ├── p16_ch7_team_ask.page  # Team + Ask combined
│   ├── p18_the_ask.page
│   └── p19_final.page
│
├── config/                    # VedaDB configuration reference
│   ├── vedadb.conf            # Full YAML config file for VedaDB server
│   ├── config_parser.py       # Python config parser utility
│   └── config_reference.md    # Config parameter documentation
│
├── research/                  # Market research materials
│   └── competitive_landscape.md # Detailed competitive landscape analysis
│
└── resume/
    └── vedadb_resume.pdf      # Developer resume PDF
```

---

## Slide-by-Slide Breakdown (18 Slides)

| # | File | Chapter | Title / Purpose |
|---|------|---------|-----------------|
| 1 | `p01_cover.page` | - | Cover - brand, tagline |
| 2 | `p02_toc.page` | - | Table of Contents (v2 addition) |
| 3 | `p03_ch1_problem.page` | Ch 1 | The Problem - database sprawl |
| 4 | `p04_data_chaos.page` | Ch 1 | Data Chaos illustration |
| 5 | `p05_ch2_solution.page` | Ch 2 | The Solution - VedaDB |
| 6 | `p06_vedadb_overview.page` | Ch 2 | VedaDB product overview |
| 7 | `p07_ch3_market.page` | Ch 3 | Market Opportunity |
| 8 | `p08_tam_sam_som.page` | Ch 3 | TAM/SAM/SOM detailed breakdown |
| 9 | `p09_ch4_competition.page` | Ch 4 | Competitive Landscape |
| 10 | `p10_competitive_matrix.page` | Ch 4 | Competitive feature matrix |
| 11 | `p11_why_vedadb.page` | Ch 4 | Why VedaDB wins |
| 12 | `p12_ch5_product.page` | Ch 5 | Product Deep Dive |
| 13 | `p13_architecture.page` | Ch 5 | System Architecture diagram |
| 14 | `p14_ch6_business.page` | Ch 6 | Business Model overview |
| 15 | `p15_business_model.page` | Ch 6 | Pricing & revenue model |
| 16 | `p16_ch7_team_ask.page` | Ch 7 | Team + The Ask |
| 17 | `p18_the_ask.page` | Ch 7 | Funding ask details |
| 18 | `p19_final.page` | - | Closing / Thank You |

**Note**: Slides are numbered with gaps (e.g., p16 -> p18) suggesting room for future additions.

---

## Content Summary

### Seven Engines (Confirmed)
1. **SQL Engine** - Relational queries, JOINs, GROUP BY, aggregates
2. **Vector Engine** - High-dimensional similarity search (HNSW, cosine, euclidean)
3. **Graph Engine** - Traversal, BFS, shortest path, PageRank
4. **Document Engine** - BSON/JSON document store
5. **Cache Engine** - In-memory caching with TTL
6. **Search Engine** - Full-text BM25F search
7. **Time Series Engine** - Time-series data with compression

### Key Config Parameters (from `config/vedadb.conf`)
- **Vector**: HNSW index, 1536 dimension limit, cosine default metric, ef_construction=200
- **Graph**: 100 traversal depth limit, PageRank enabled, 50 iterations
- **SQL**: B-tree default storage, 1000 max connections, 64MB query cache
- **Security**: AES-GCM encryption, TLS 1.3, RBAC, OIDC support
- **Replication**: Async multi-master, configurable consistency levels

### Competitive Landscape (from `research/`)
Detailed analysis comparing VedaDB against:
- PostgreSQL, MongoDB, Redis, Elasticsearch, Neo4j, InfluxDB, Milvus
- CockroachDB, TiDB, SingleStore, ArangoDB
- Evaluation on: multi-model support, query fusion, AI optimization, ops overhead, TCO

---

## Visual Design Spec (from design.md)

### Design Philosophy
- **Profile**: `profiles/strategic.md` - fundraising pitch deck
- **Style Anchors**: CockroachDB/MongoDB dark bold + Stripe precision + Sequoia data-forward clarity
- **Information Density**: Medium-high (65-80%)
- **Deviations from standard strategic**: Darker palette for dramatic impact, tech-forward visual language

### Color Palette
- **Primary**: #1A1F36 (deep navy)
- **Background**: #0D1117 (near-black)
- **Surface**: #1E2538 (dark blue-gray)
- **Text Primary**: #FFFFFF
- **Text Secondary**: #8B95A5
- **Accent**: #D4A843 (gold) - key numbers, CTAs
- **Success**: #10B981 (emerald)
- **Border**: #2D3648

### Typography
- **Titles**: Liter Bold, 36-48px, ALL CAPS, letter-spacing 2px
- **Body**: Liter Regular, 20px, line-height 1.6
- **Big Numbers**: Liter Bold, 56-72px, gold accent
- **Annotations**: Liter Regular, 14px, gray

---

## Config Directory (`config/`)

### `vedadb.conf`
Full YAML configuration file for VedaDB server with sections for:
- `data_models` - Enable/disable 7 engines with per-engine tuning
- `cluster` - Sharding, replication, consensus settings
- `security` - TLS, RBAC, OIDC, audit logging, encryption
- `performance` - Connection pools, memory limits, query timeouts
- `storage` - Data directories, WAL, compaction, backup
- `logging` - Log levels, destinations, rotation
- `plugins` - Extension loading and configuration

### `config_parser.py`
Python utility for parsing and validating `vedadb.conf`. Can be used to:
- Validate configuration syntax
- Extract settings programmatically
- Generate config documentation

### `config_reference.md`
Complete reference documentation for all configuration parameters.

---

## Research Directory (`research/`)

### `competitive_landscape.md`
Detailed competitive analysis covering:
- Market positioning of each competitor
- Feature-by-feature comparison matrix
- TCO analysis
- Migration complexity assessment
- Target customer segment overlap

---

## Resume Directory (`resume/`)

### `vedadb_resume.pdf`
Developer resume for the VedaDB project team section of the pitch deck.

---

## PPTD File Format

The `.pptd` file is the master presentation file that:
- Defines slide ordering and structure
- References `.page` files for slide content
- Specifies layout directives per slide
- Contains presentation-level metadata

---

## What NOT To Recreate

- **Do NOT confuse with `vedadb-pitch`**: That is the 12-slide v1 deck. This is the 18-slide v2 deck.
- **Do NOT add more than 7 engines**: SQL, Vector, Graph, Document, Cache, Search, Time Series only.
- **Do NOT change the dark theme**: Gold-on-dark is the established brand aesthetic.
- **Do NOT modify `vedadb.conf` structure**: It follows MongoDB's `mongod.conf` YAML convention.
- **Do NOT regenerate `vedadb_resume.pdf`**: It is a static asset for the pitch deck.

---

## Related Repos

| Repo | Purpose |
|------|---------|
| `vedadb-pitch` | 12-slide v1 pitch deck (condensed version) |
| `vedadb-investor-sprint` | Investor sprint materials |
| `vedadb-research` | Market research data sources |
| `vedadb-docs` | Product documentation |

---

## Instructions For Future Agents

1. **Slide content**: Edit `.page` files in `pages/` directory
2. **Slide order**: Modify `vedadb.pptd` master file
3. **Design changes**: Update `design.md` for global style changes
4. **Outline updates**: `outline.md` is the content source of truth
5. **Config updates**: Modify `config/vedadb.conf` and update `config_reference.md`
6. **Competitive research**: Add findings to `research/competitive_landscape.md`
7. **Resume**: Keep `resume/vedadb_resume.pdf` as-is unless updating personal info
8. **7 engines**: SQL, Vector, Graph, Document, Cache, Search, Time Series
9. **Preserve PPTD format**: Do not convert to PowerPoint/Keynote
10. **Gold-on-dark theme**: Maintain visual consistency
