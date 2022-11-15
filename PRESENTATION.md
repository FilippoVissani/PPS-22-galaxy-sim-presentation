---
marp: true
theme: gaia
backgroundColor: #3b4252
style: |
  h1 {
    color: #eceff4;
    font-size: 40px;
    text-align: center;
    border-radius: 10px;
    background-color: #a3be8c;
    box-shadow: 5px 5px #2e3440;
    -webkit-text-stroke-width: 1px;
    -webkit-text-stroke-color: #2e3440;
  }

  p {
    text-align: center;
    border: 5px solid #eceff4;
    border-radius: 10px;
    background-color: white;
    box-shadow: 5px 5px #2e3440;
  }

  ul {
    color: #2e3440;
    border: 5px solid #eceff4;
    border-radius: 10px;
    background-color: #eceff4;
    box-shadow: 5px 5px #2e3440;
  }
---
<!-- _class: h1 -->
# Introduzione

---

# Requisiti

---

# Architettura

![Architettura w:30cm](./assets/mvc_actor_architecture.svg)

---

# Attori

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
