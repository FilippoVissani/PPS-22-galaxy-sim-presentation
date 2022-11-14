---
marp: true
theme: gaia
backgroundColor: white
paginate: true
---

# **Introduzione**

---

# **Requisiti**

---

# **Architettura**

![Architettura bg 90%](./assets/mvc_actor_architecture.svg)

---

### **Attori**

![Architettura bg 80%](./assets/celestial_body_actor_class_diagram.svg)

---

### **Attori: ciclo di vita**

![Architettura bg 45%](./assets/actors_lifecycle_sequence.svg)

---

### **Attori: loop della simulazione**

![Architettura bg 55%](./assets/actors_simulation_loop_sequence.svg)

---

### **Attori: aggiornamento della View**

![Architettura bg 55%](./assets/actors_view_simulation_update_sequence.svg)

---

# **Ciclo di vita**

---

## **Fisica** {.smaller}

### Dynamics 
- PhysicalEntity: the subject of dynamics laws, with relevant physical attributes;
- ???

### Collisions
- Intersection: logic to detect if two bodies are colliding or not, based on bounding box shapes;
- Impact: logic to express the result of the collision;

### Rigidbody
- Reunites common concepts of physics: a physical entity with a bounding box;

---

### **GUI: Info**

![Architettura bg 60%](./assets/gui-info.png)

---

### **GUI: Log**

![Architettura bg 60%](./assets/gui-log.png)

---

### **GUI: Statistiche**

![Architettura bg 60%](./assets/gui-stats.png)
