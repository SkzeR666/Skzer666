<h1 align="left">
  SkzeR666
</h1>

<sub>Augusto Santos · she/her</sub>

---

```tsx
import type { Metadata } from "next";

export const metadata: Metadata = {
  title: "Augusto Santos",
  description: "solo dev · brasil · só bug de deploy",
};

type Projeto = {
  nome: string;
  sobre: string;
};

const projetos: Projeto[] = [
  {
    nome: "Fragbase",
    sobre: "casa de torneios de cs2 — hub competitivo",
  },
  {
    nome: "Fragguard",
    sobre: "anticheat em go + rust que não tira folga",
  },
  {
    nome: "OrçaZap",
    sobre: "do orçamento ao pix sem sair do zap",
  },
  {
    nome: "ZERO Autos",
    sobre: "curadoria de veículos selecionados à venda",
  },
];

const stack = {
  linguagens: ["TypeScript", "Go", "Rust"],
  frontend: ["React", "Next.js", "Tailwind"],
  backend: ["Node.js", "Go"],
  dados: ["PostgreSQL", "Redis"],
  infra: ["Docker", "Linux", "Git"],
};

const contato = {
  github: "github.com/Sixer666",
  instagram: "instagram.com/augusto_santos666",
};

export default function Augusto() {
  return (
    <main className="grind">
      <h1>Augusto Santos</h1>
      <p>solo dev · brasil · commits e prazo</p>

      <section id="focus">
        <p>
          no momento subindo a Fragbase, plataforma de torneios de CS2
        </p>
      </section>

      <section id="projects">
        {projetos.map(({ nome, sobre }) => (
          <article key={nome}>
            <strong>{nome}</strong> — {sobre}
          </article>
        ))}
      </section>

      <section id="stack">
        {Object.entries(stack).map(([area, techs]) => (
          <p key={area}>
            {area}: {techs.join(" · ")}
          </p>
        ))}
      </section>

      <footer>
        {Object.entries(contato).map(([rede, href]) => (
          <p key={rede}>
            {rede}: {href}
          </p>
        ))}
      </footer>
    </main>
  );
}
```

```diff
+ LOCATION=BRASIL
+ ROLE=SOLO_DEV
+ MODE=BUILDING
+ STACK=TS / GO / RUST
+ DEPLOY=VERCEL
+ COFFEE=REQUIRED

! CURRENT=ZERO
! STATUS=SHIPPING
! DEBUG=FALSE
! UPTIME=99.8%

- SLEEP
- FREE_TIME
- BORING_SOFTWARE

@@ FAVORITE_BUG=works_on_my_machine @@
@@ NEXT_PUBLIC_WTF=cinematic @@
```

---

## system

```ini
[IDENTITY]
name=Sixer666
location=Brazil
role=solo_dev

[CURRENT]
project=ZERO
status=building
mode=shipping

[STACK]
frontend=TypeScript, Next.js, React, Tailwind
backend=Go, Rust, Node.js
database=PostgreSQL, Redis
infra=Docker, Linux, Git, Vercel

[SYSTEM]
coffee=required
sleep=optional
debug=false
```

---

## projects

```yaml
projects:
  - name: Fragbase
    type: competitive_platform
    status: active

  - name: Fragguard
    type: anticheat
    status: building

  - name: OrçaZap
    type: saas
    status: building

  - name: ZERO Autos
    type: automotive_curatorship
    status: active
```

---

## current

```diff
+ building products
+ breaking production
+ fixing production
+ shipping anyway

! frontend ≠ just visuals
! backend ≠ black magic

@@ still_works=true @@
```

---

## stack

`TypeScript` · `Go` · `Rust` · `React` · `Next.js` · `Tailwind` · `Node.js` · `PostgreSQL` · `Redis` · `Docker` · `Linux` · `Git`

---

## contact

```yaml
github: Sixer666
instagram: augusto_santos666
location: Brazil
```

---

<sub>
works on my machine.
</sub>
