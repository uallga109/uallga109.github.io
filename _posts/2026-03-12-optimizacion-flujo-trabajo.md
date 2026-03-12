---
layout: post
title: "🚀 Más allá del código: Arquitectura de Despliegue y Flujo Colaborativo en EscuderoGarcia"
date: 2026-03-12
author: uallga109
categories: [DevOps]
tags: [Azure, GitHub, Jekyll, CI-CD]
excerpt: "Un análisis técnico sobre cómo el equipo EscuderoGarcia implementó una infraestructura de despliegue continuo (CI/CD) para garantizar la integridad y escalabilidad de nuestro blog estático."
---

![Badge GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Badge Azure](https://img.shields.io/badge/Azure-0089D6?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Badge Jekyll](https://img.shields.io/badge/Jekyll-CC0000?style=for-the-badge&logo=jekyll&logoColor=white)

> "En la ingeniería de software moderna, el éxito no reside solo en escribir código que funcione, sino en construir el sistema que permite que ese código llegue al usuario de forma segura, rápida y escalable."

## 🎯 El Desafío Técnico
[cite_start]En el marco del curso **HMIS 2026**, nuestro equipo, **EscuderoGarcia**, se enfrentó al reto de desarrollar un blog colaborativo que no solo cumpliera con los requisitos funcionales, sino que sirviera como un caso de estudio real sobre **automatización y despliegue**[cite: 51, 52]. 

Mi misión principal fue liderar la integración del flujo de trabajo y asegurar que cada línea de código subida por mis compañeros pasara por un proceso de validación riguroso antes de ver la luz en producción.

## 🛠️ Stack Tecnológico de Vanguardia
Para este proyecto, seleccionamos un conjunto de herramientas diseñado para la alta disponibilidad:
* [cite_start]**Generador Estático (SSG):** Jekyll, por su robustez y natividad con el ecosistema de GitHub[cite: 12].
* [cite_start]**Control de Versiones:** Git, bajo la metodología **GitHub Flow**[cite: 40].
* [cite_start]**Infraestructura Cloud:** Despliegue multicanal utilizando **Azure Static Web Apps** y **Azure Virtual Machines** con Nginx para balanceo y redundancia.

## ⚙️ Implementación del Flujo de Trabajo (CI/CD)
No nos limitamos a subir archivos. Implementamos un ciclo de vida de desarrollo profesional:

1.  [cite_start]**Branching Strategy:** Aplicamos una política de protección de rama `main`[cite: 41]. Nadie escribe directamente en producción.
2.  [cite_start]**Feature Branches:** Cada funcionalidad nació en su propia rama aislada[cite: 40].
3.  [cite_start]**Pull Requests & Peer Review:** El responsable del repositorio validó cada cambio antes de la fusión, garantizando la calidad técnica[cite: 44, 45].

```bash
# Nuestro flujo estándar de trabajo diario
git checkout -b feature-optimizacion-seo
git add .
git commit -m "feat: optimización de metadatos para SEO"
git push origin feature-optimizacion-seo
