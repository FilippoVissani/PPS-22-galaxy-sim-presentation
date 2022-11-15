---
marp: true
theme: gaia
backgroundColor: #2e3440
style: |
  h1 {
    color: #eceff4;
    font-size: 40px;
    text-align: center;
    border-radius: 10px;
    background-color: #4c566a;
  }

  p {
    color: #2e3440;
    text-align: center;
    border: 2px solid #eceff4;
    border-radius: 10px;
    background-color: white;
  }

  ul {
    color: #2e3440;
    border: 2px solid #eceff4;
    border-radius: 10px;
    background-color: #eceff4;
  }

---

# Introduzione

Galaxy Simulator permette di simulare il comportamento dei corpi celesti presenti all'interno di una galassia

---

# Requisiti

- Rappresentazione 2D della simulazione
- L'andamento della simulazione è scandito da un tempo virtuale
- I corpi celesti hanno un'orbita
- Sono presenti diversi tipi di corpi celesti
- Le stelle hanno un ciclo di vita
- La collisione tra due corpi ne modifica le caratteristiche
---

# Architettura del sistema

![Architettura w:30cm](./assets/mvc_actor_architecture.svg)

---

# Simulazione

![Simulazione w:14cm](./assets/simulation_class_diagram.svg)

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

# Attori: ciclo di vita

![Attori: ciclo di vita w:17.5cm](./assets/actors_lifecycle_sequence.svg)

---

# Attori: loop della simulazione

![Attori: loop della simulazione w:22cm](./assets/actors_simulation_loop_sequence.svg)

---

# Attori: aggiornamento della View

![Attori: aggiornamento della View w:20cm](./assets/actors_view_simulation_update_sequence.svg)

---

# Ciclo di vita
![Ciclo di vita w:15cm](./assets/lifecycle.svg)

---

# Fisica: dynamics

- PhysicalEntity: the subject of dynamics laws, with relevant physical attributes;
- GravitationLaws: logic to calculate gravitational force of objects, their speed and their new position.

---
# Fisica: collisions

- Intersection: logic to detect if two bodies are colliding or not, based on bounding box shapes;
- Impact: logic to express the result of the collision;

---
# Fisica: rigidbody

- Reunites common concepts of physics: a physical entity with a bounding box;

---

# GUI: Info

![GUI: Info w:24cm](./assets/gui-info.png)

---

# GUI: Log

![GUI: Log w:24cm](./assets/gui-log.png)

---

# GUI: Statistiche

![GUI: Statistiche w:24cm](./assets/gui-stats.png)
