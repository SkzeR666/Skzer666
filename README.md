<div align="center">

# SkzeR666

### Augusto Santos

`solo developer` · `product builder` · `Brazil`

<br>

> building useful systems, shipping products and occasionally discovering that production has opinions.

<br>

`TypeScript` · `Go` · `Rust` · `Next.js` · `React` · `PostgreSQL` · `Redis` · `Docker`

</div>

---

<div align="center">

## `~/profile`

</div>

```ts
type Developer = {
  name: string;
  alias: string;
  location: string;
  roles: string[];
  interests: string[];
  philosophy: string;
};

const me: Developer = {
  name: "Augusto Santos",
  alias: "SkzeR666",
  location: "Brazil",

  roles: [
    "solo developer",
    "product builder",
    "backend-oriented developer",
    "frontend when necessary",
  ],

  interests: [
    "software architecture",
    "product engineering",
    "design systems",
    "automation",
    "competitive gaming infrastructure",
    "automotive products",
  ],

  philosophy:
    "build useful systems first, then make them beautiful without making them fragile",
};
```

I like software that actually does something.

Not just landing pages.

Not just dashboards assembled from twenty libraries.

Not just interfaces created to look good in screenshots.

I like taking an idea through the entire path:

```txt
problem
   ↓
product
   ↓
architecture
   ↓
backend
   ↓
database
   ↓
automation
   ↓
interface
   ↓
deployment
   ↓
production
```

And then fixing whatever production decides to expose.

---

<div align="center">

## `~/currently-building`

</div>

```go
package projects

type Project struct {
	Name        string
	Description string
	Status      string
}

var Current = []Project{
	{
		Name:        "FRAGBASE",
		Description: "competitive infrastructure and tournament platform for Counter-Strike 2",
		Status:      "shipping",
	},
	{
		Name:        "FRAGGUARD",
		Description: "competitive integrity and anti-cheat tooling",
		Status:      "building",
	},
	{
		Name:        "ZERO",
		Description: "curated products, private experiences and experimental software",
		Status:      "building",
	},
	{
		Name:        "ZERO Autos",
		Description: "automotive curation, presentation and lead generation",
		Status:      "shipping",
	},
	{
		Name:        "OrçaZap",
		Description: "quotations, services and payments built around conversational workflows",
		Status:      "building",
	},
}
```

Most of my projects start as:

```txt
"isso aqui dava pra fazer melhor"
```

and somehow end up involving:

```txt
authentication
permissions
databases
workers
APIs
admin panels
design systems
deployments
analytics
automation
```

---

<div align="center">

# `01 / FRAGBASE`

### competitive infrastructure for CS2

</div>

```rust
pub struct Fragbase {
    pub game: &'static str,
    pub audience: Vec<&'static str>,
    pub systems: Vec<&'static str>,
}

pub fn build() -> Fragbase {
    Fragbase {
        game: "Counter-Strike 2",

        audience: vec![
            "players",
            "teams",
            "organizers",
        ],

        systems: vec![
            "tournament management",
            "registrations",
            "approvals",
            "check-in",
            "map veto",
            "MatchZy integration",
            "game servers",
            "automatic demos",
            "statistics",
            "payments",
            "competitive integrity",
        ],
    }
}
```

FRAGBASE grew from an idea around competitive Counter-Strike into a larger infrastructure problem.

Running tournaments sounds simple until every subsystem needs to communicate with everything else.

```txt
organizer
   │
   ├── tournament
   │      │
   │      ├── teams
   │      ├── brackets
   │      ├── check-in
   │      ├── veto
   │      └── matches
   │
   ├── servers
   │      ├── MatchZy
   │      ├── configs
   │      ├── demos
   │      └── results
   │
   └── platform
          ├── statistics
          ├── payments
          ├── permissions
          └── integrity
```

The interesting part for me is not just creating tournament pages.

It is making the infrastructure underneath them behave like one system.

---

<div align="center">

# `02 / FRAGGUARD`

### competitive integrity tooling

</div>

```rust
#[derive(Debug)]
pub enum IntegrityStatus {
    Trusted,
    Monitoring,
    Suspicious,
    Reviewing,
}

pub struct Player {
    pub steam_id: String,
    pub integrity: IntegrityStatus,
}

pub struct Match {
    pub players: Vec<Player>,
    pub verified: bool,
}
```

FRAGGUARD exists around the idea that competitive systems should not treat integrity as an afterthought.

The goal is to make competitive integrity part of the platform architecture itself.

Not another disconnected dashboard.

Not another manual process.

A system that understands the competitive lifecycle it belongs to.

---

<div align="center">

# `03 / ZERO`

### experimentation, curation and identity

</div>

```ts
type Zero = {
  access: "curated";
  philosophy: "quality-over-volume";
  identity: "dark-editorial";
  experiments: true;
};

const zero: Zero = {
  access: "curated",
  philosophy: "quality-over-volume",
  identity: "dark-editorial",
  experiments: true,
};
```

ZERO became the space where I can experiment with ideas that do not necessarily fit inside a traditional SaaS product.

The common principle is simple:

```txt
less volume
more intention

less noise
more identity

less generic
more curated
```

It is as much a product philosophy as it is a project.

---

<div align="center">

# `04 / ZERO AUTOS`

### automotive curation

</div>

```ts
interface Vehicle {
  id: string;
  brand: string;
  model: string;
  year: number;
  mileage: number;
}

interface VehicleExperience {
  vehicle: Vehicle;
  gallery: string[];
  specifications: Record<string, string>;
  landingPage: string;
  leadCapture: boolean;
}

const experience: VehicleExperience = {
  vehicle: {} as Vehicle,
  gallery: [],
  specifications: {},
  landingPage: "/cars/:slug",
  leadCapture: true,
};
```

Working around automotive businesses pushed me toward a different approach to selling vehicles online.

Instead of treating every vehicle like one item inside an enormous inventory grid, I became interested in treating each one almost like its own product launch.

```txt
vehicle
   │
   ├── identity
   ├── photography
   ├── specifications
   ├── storytelling
   ├── landing page
   └── lead capture
```

That became ZERO Autos.

A more curated approach to automotive presentation.

---

<div align="center">

# `05 / ORÇAZAP`

### service workflow without unnecessary friction

</div>

```ts
const quotation = await quote.create({
  customer,
  services,
});

await quotation.send();

const approval = await quotation.waitForApproval();

if (approval.accepted) {
  await payment.create(quotation);
}
```

The idea behind OrçaZap is much simpler:

service businesses already sell through conversations.

The software should adapt to that workflow instead of forcing the business to adapt to the software.

```txt
conversation
    ↓
services
    ↓
quotation
    ↓
approval
    ↓
payment
```

Less friction.

Less jumping between systems.

More focus on actually closing the service.

---

<div align="center">

## `~/architecture`

</div>

```yaml
frontend:
  language:
    - TypeScript

  framework:
    - React
    - Next.js

  styling:
    - Tailwind CSS

  principles:
    - reusable-primitives
    - explicit-states
    - responsive-first
    - design-systems
    - controlled-dependencies

backend:
  languages:
    - Go
    - TypeScript
    - Rust

  concepts:
    - REST
    - services
    - workers
    - automation
    - asynchronous-processing
    - integrations

data:
  relational:
    - PostgreSQL

  cache:
    - Redis

infrastructure:
  - Docker
  - Linux
  - Cloudflare
  - Vercel
  - Supabase
  - GitHub
```

I prefer understanding what the system is doing.

That usually means fewer magical abstractions and more explicit architecture.

```txt
simple ≠ primitive

abstraction ≠ architecture

more dependencies ≠ better product
```

---

<div align="center">

## `~/frontend`

</div>

```tsx
export default function Product() {
  return (
    <main>
      <Foundation />

      <DesignSystem>
        <Primitives />
        <Components />
        <States />
        <Interactions />
      </DesignSystem>

      <Application />
    </main>
  );
}
```

Frontend is not the part of software I originally cared about the most.

Building products changed that.

Eventually I realized that a good system with a bad interface still feels like a bad product.

So I started caring more about:

```txt
spacing
hierarchy
states
motion
interaction
responsive behavior
design tokens
component APIs
```

Not because I want to create visual experiments for their own sake.

Because interface quality is part of product quality.

---

<div align="center">

## `~/design-system`

</div>

```css
:root {
  --background: #09090b;
  --surface: #111318;

  --foreground: #fafafa;
  --muted: #71717a;

  --border: #27272a;

  --radius-sm: 8px;
  --radius-md: 12px;
  --radius-lg: 20px;

  --motion-fast: 120ms;
  --motion-default: 220ms;
}

.interface {
  hierarchy: strong;
  decoration: restrained;
  interaction: intentional;
  consistency: required;
}
```

The design direction I naturally move toward is usually:

```diff
+ minimal
+ functional
+ editorial
+ structured
+ responsive
+ high contrast
+ intentional motion

- component soup
- unnecessary gradients
- random glassmorphism
- excessive glow
- visual noise
- giant landing pages with no product behind them
```

---

<div align="center">

## `~/product-philosophy`

</div>

```sql
SELECT
    usefulness,
    maintainability,
    scalability,
    usability,
    identity
FROM product
WHERE solves_real_problem = TRUE
ORDER BY usefulness DESC;
```

I care more about whether a product can survive real usage than whether its hero section looks impressive in a video.

A product should have:

```yaml
product:
  reason_to_exist: clear

  architecture:
    predictable: true
    maintainable: true

  interface:
    usable: true
    consistent: true

  infrastructure:
    boring_when_possible: true

  identity:
    intentional: true

  complexity:
    unnecessary: false
```

---

<div align="center">

## `~/workflow`

</div>

```bash
$ ./build-product.sh

[01] understand problem
[02] define constraints
[03] model domain
[04] design architecture
[05] build backend
[06] model database
[07] build interface
[08] deploy
[09] discover production-only bug
[10] fix
[11] refactor
[12] ship again
```

---

<div align="center">

## `~/opinions`

</div>

```diff
+ boring infrastructure
+ clear APIs
+ explicit states
+ reusable primitives
+ maintainable systems
+ useful products
+ controlled dependencies
+ shipping

- dependency soup
- architecture astronautics
- fake dashboards
- abstractions without purpose
- visual complexity without usability
- copying libraries until the product loses its identity

! production is the final reviewer
```

---

<div align="center">

## `~/runtime`

</div>

```ini
[identity]
name=Augusto Santos
alias=SkzeR666
location=Brazil

[role]
primary=solo_developer
secondary=product_builder

[current]
status=building
mode=shipping

[preferences]
backend=true
frontend=true
design_systems=true
architecture=true
automation=true

[dependencies]
magic=false
unnecessary=false

[production]
works_on_my_machine=true
works_on_vercel=eventually

[system]
coffee=required
sleep=optional
```

---

<div align="center">

## `~/stack`

<br>

### Languages

`TypeScript` · `Go` · `Rust` · `JavaScript`

<br>

### Frontend

`React` · `Next.js` · `Tailwind CSS`

<br>

### Backend

`Go` · `Node.js` · `REST APIs`

<br>

### Data

`PostgreSQL` · `Redis` · `Supabase`

<br>

### Infrastructure

`Docker` · `Linux` · `Cloudflare` · `Vercel`

<br>

### Tooling

`Git` · `GitHub`

</div>

---

<div align="center">

## `~/projects`

| Project | Area | Status |
| --- | --- | --- |
| **FRAGBASE** | Competitive infrastructure / CS2 | `shipping` |
| **FRAGGUARD** | Competitive integrity | `building` |
| **ZERO** | Curated experiments / products | `building` |
| **ZERO Autos** | Automotive curation | `shipping` |
| **OrçaZap** | Service / quotation SaaS | `building` |

</div>

---

<div align="center">

## `~/status`

</div>

```txt
system:      online
developer:   SkzeR666
location:    Brazil

focus:       product engineering
mode:        building
deployment:  continuous

bugs:        expected
shipping:    required
```

```diff
+ learn
+ build
+ break
+ understand
+ rebuild
+ ship

! repeat
```

---

<div align="center">

## `~/contact`

<br>

**GitHub**

`@SkzeR666`

<br>

**Brazil**

`UTC-03:00`

<br><br>

---

### building things until they become products.

<sub>
and fixing them until production stops complaining.
</sub>

</div>
