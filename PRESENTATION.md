---
marp: true
theme: gaia
backgroundColor: #023047
style: |
  h1 {
    color: #023047;
    font-size: 40px;
    text-align: center;
    border: 4px solid #fb8500;
    border-radius: 10px;
    background-color: #ffb703;
  }

  p {
    color: black;
    text-align: center;
    border: 4px solid #219ebc;
    border-radius: 10px;
    background-color: white;
  }

  ul {
    color: black;
    border: 4px solid #219ebc;
    border-radius: 10px;
    background-color: white;
  }

  ol {
    color: black;
    border: 4px solid #219ebc;
    border-radius: 10px;
    background-color: white;
  }

---

# Introduzione

Galaxy Simulator è un simulatore del moto dei corpi all’interno di una galassia. Permette di vedere l’interazione che c’è tra varie tipologie di corpi celesti mentre orbitano attorno a un corpo principale posto al centro della galassia

---

# Funzionalità di base

- Rappresentazione 2D della simulazione
- Presenza di diversi tipi di corpi celesti
- Visualizzazione del movimento dei corpi celesti
- Visualizzazione delle informazioni dei corpi presenti durante la simulazione
- Visualizzazione di statistiche generali sulla simulazione
- Modifica delle caratteristiche di un corpo con il passare del tempo e con le collisioni
---

# Architettura del sistema

![Architettura w:30cm](./assets/mvc_actor_architecture.svg)

---

# Simulazione: design

![Simulazione w:14cm](./assets/simulation_class_diagram.svg)

---

# Simulazione: loop

Step eseguiti durante un'iterazione:

1. Aggiornamento del tipo dei corpi
2. Aggiornamento della posizione dei corpi
3. Risoluzione delle collisioni

---

# Attori: introduzione

- CelestialBodyActor: gestisce un corpo celeste
- SimulationManagerActor: gestisce la simulazione
- EventRecorderActor: registra gli eventi
- ControllerActor: gestisce la parte di Controller
- ViewActor: gestisce la View della simulazione

---

# Attori: design

![Attori w:30cm](./assets/celestial_body_actor_class_diagram.svg)

---

# Attori: design

![Attori w:20cm](./assets/actors_class_diagram.svg)

---

# Attori: ciclo di vita

![Attori: ciclo di vita w:17.5cm](./assets/actors_lifecycle_sequence.svg)

---

# Attori: loop della simulazione

![Attori: loop della simulazione w:22cm](./assets/actors_simulation_loop_sequence.svg)

---

# Attori: aggiornamento della View

![Attori: aggiornamento della View w:20cm](./assets/actors_view_simulation_update_sequence.svg)

---

# Identificazione delle entità
Massa e Temperatura definiscono il tipo di entità:

- **Asteroide**: Temp <= 50
- **Pianeta**: 50 < Temp <= 100
- **Nube Interstellare**: 100 < Temp <= 1000
- **Massive star**: (Temp > 1000) && (0 <= Massa < 1e10) 
- **Red super giant**: (Temp > 1000) && (1e10 <= Massa < 1e20) 
- **Supernova**: (Temp > 1000) && (1e20 <= Massa < 1e30) 
- **Black hole**: (Temp > 1000) && (Massa >= 1e30) 

---

# Ciclo di vita
![Ciclo di vita w:15cm](./assets/lifecycle.svg)

---

# Fisica: dynamics

- PhysicalEntity: il soggetto su cui vengono applicate le leggi gravitazionali, con i relativi attributi fisici;
- GravitationLaws: la logica per calcolare le formule gravitazionali, tra cui attrazione gravitazionale, velocità e nuova posizione.

---
# Fisica: collisions

- Intersection: logica per controllare se due corpi stanno collidendo, basandosi sull' intersezione di bounding boxes;
- Impact: logica per esprimere il risultato di una collisione;

---
# Fisica: rigidbody

- Riunisce concetti della fisica: una PhysicalEntity con CollisionBox;

---

# GUI: Info

![GUI: Info w:24cm](./assets/gui-info.png)

---

# GUI: Log

![GUI: Log w:24cm](./assets/gui-log.png)

---

# GUI: Statistiche

![GUI: Statistiche w:24cm](./assets/gui-stats.png)
