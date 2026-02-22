**Here is  a RoadMap to learn Nix**

# Phase 0 — Understand What Nix _Actually_ Is (1–2 days)

If you skip this, you’ll stay confused forever.

Nix is:

- A **pure, lazy, functional language**
    
- Used to describe **derivations (build instructions)**
    
- Designed around **immutability and reproducibility**
    

Key mental shifts:

- No mutation.
    
- No loops (you map and fold).
    
- Everything is an expression.
    
- Evaluation ≠ building.
    

If you still think of it like Bash or Python, you’ll struggle.

Read:

- Official Nix language reference (skim once)
    
- Then move on. Don’t get stuck.
    

---

# Phase 1 — Core Language Mechanics (1 week max)

Open `nix repl`. Stop watching tutorials.

You must be fluent in:

### 1. Basic Types

- strings
    
- integers
    
- floats
    
- bool
    
- null
    
- lists
    
- attribute sets
    

Practice:

{ a = 1; b = "hello"; }

If attrsets don’t feel natural, you’re not ready to continue.

---

### 2. Functions (Critical)

Nix is function-heavy.

Understand:

x: x + 1

Then:

{ pkgs, ... }: { }

Then:

{ a, b ? 10 }: a + b

If you don’t deeply understand:

- currying
    
- default arguments
    
- argument destructuring
    

You will suffer in NixOS modules.

---

### 3. Let / In

let  
  x = 5;  
in  
  x + 1

If you don’t understand lexical scoping, stop and fix that.

---

### 4. With (Use Carefully)

with pkgs; [ git vim ]

Know what it does.  
Also know why overusing it is sloppy.

---

# Phase 2 — Laziness & Evaluation Model (This separates amateurs)

Nix is lazy.

This means:

- Infinite recursion won’t crash immediately.
    
- Some errors only show during evaluation.
    
- Some only during build.
    

Learn:

- `nix-instantiate --eval`
    
- `builtins.trace`
    
- `builtins.deepSeq`
    

If you don’t understand when something is evaluated, you’re not mastering Nix.

---

# Phase 3 — Derivations (The Real Point)

Now you move from language → packaging.

Learn:

stdenv.mkDerivation {  
  pname = "test";  
  version = "1.0";  
  src = ./.;  
}

Understand:

- `src`
    
- `buildInputs`
    
- `nativeBuildInputs`
    
- phases
    
- `$out`
    

If you can’t package a simple C program or shell script, you don’t understand Nix yet.

---

# Phase 4 — Nixpkgs Architecture (This is where most people quit)

You need to understand:

- overlays
    
- callPackage
    
- fixpoints
    
- self / super
    
- package sets
    

This is where Nix stops being cute and becomes serious.

Study:

callPackage ./default.nix { }

Understand why arguments auto-fill.

If you don’t get fixpoints, overlays will feel like black magic.

---

# Phase 5 — NixOS Module System (Advanced)

Completely different layer.

Learn:

- options
    
- types
    
- mkOption
    
- mkIf
    
- mkMerge
    
- config vs options
    

This is a declarative merge system, not “just Nix code”.

If you think it’s just a config file, you’re wrong.

---

# Phase 6 — Flakes (Optional but Realistic)

Understand:

- inputs
    
- outputs
    
- systems
    
- devShell
    
- apps
    
- nix develop
    

Don’t memorize boilerplate.  
Understand evaluation graph.

---

# What Will Actually Make You Good

Forget passive learning.

Do this:

1. Write your own mini package.
    
2. Create a custom overlay.
    
3. Write a simple NixOS module.
    
4. Debug a broken evaluation.
    
5. Read 5 real nixpkgs files and understand them.
    

If you can read nixpkgs source without panic, you’re competent.

---

# What Most People Do Wrong

- They memorize syntax but don’t understand evaluation.
    
- They copy flakes without understanding them.
    
- They never package anything.
    
- They avoid overlays because they “look scary”.
    
- They stay at the Home Manager config level.
    

That’s surface-level usage.

---

# Timeline (Realistic)

If you’re serious:

- 2 weeks: Comfortable writing expressions
    
- 1 month: Can package simple software
    
- 2–3 months: Understand overlays & module system
    
- 6+ months: Actually fluent
    

You won’t “master” it in a weekend.

---