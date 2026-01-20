Com certeza! Com base na estrutura do seu projeto e nos scripts fornecidos, preparei um **README.md** profissional, organizado e focado em documentar as funcionalidades técnicas do seu setup de Realidade Virtual.

---

# 🎮 UNITY-3D-VR: Player Setup & Interactions

Este repositório contém o alicerce técnico para o desenvolvimento de experiências imersivas em Realidade Virtual utilizando o **Unity 6**. O projeto foca na implementação de um sistema robusto de player, mecânicas de locomoção inteligente e interações com objetos (sistema de combate).

## 🚀 Tecnologias e Versões

O projeto utiliza as ferramentas mais recentes do ecossistema XR da Unity:

* **Unity Engine:** Versão 6000.0.6f1.
* **XR Interaction Toolkit (XRI):** 3.3.1.
* **OpenXR Plugin:** 1.16.1.
* **Universal Render Pipeline (URP):** 17.3.0.
* **Unity Input System:** 1.17.0.

## 🛠️ Funcionalidades Principais

### 1. Sistema de Locomoção (Teleporte Dinâmico)

Implementação de um sistema de teleporte que evita poluição visual na cena. O raio de teleporte só é ativado quando o usuário realiza uma ação específica no controle.

* **Script:** `TeleportationActivator.cs`.
* **Lógica:** O `XRRayInteractor` permanece desativado por padrão e é habilitado apenas durante o evento `performed` da `InputActionProperty` configurada, sendo desativado imediatamente após o release.

### 2. Sistema de Combate (Pistola Funcional)

Configuração de uma mecânica de disparo completa integrando física e feedback auditivo.

* **Script:** `Pistol.cs`.
* **Recursos:** * Instanciação de projéteis com velocidade linear configurável (`bulletSpeed`).
* Gerenciamento automático de memória com destruição programada de projéteis (`bulletLifetime`).
* Feedback sonoro via `AudioSource` disparado no momento do tiro.



### 3. Setup do Player (XR Origin)

O Player foi estruturado para garantir a melhor experiência e conforto:

* **Camera Offset:** Configurado para o rastreamento preciso da altura do HMD.
* **Animated Hands:** Integração de modelos de mãos skeletal de baixa resolução com suporte a animações de Fist (soco) e Pinch (pinça).
* **Input Mapping:** Mapeamento otimizado para controles Oculus e dispositivos compatíveis com OpenXR.

## 📂 Estrutura de Pastas Relevante

* `/Assets/Scripts`: Lógica de interação e ativação de recursos.
* `/Assets/Animated Hands`: Modelos, materiais e controladores de animação para as mãos VR.
* `/Assets/Samples`: Ativos base do XR Interaction Toolkit.
* `/ProjectSettings`: Configurações globais de física, tags e gerenciamento de XR.

## ⚙️ Como Configurar

1. Certifique-se de estar utilizando o **Unity 6** (6000.0.6f1 ou superior).
2. Importe o projeto e aguarde a resolução das dependências do `manifest.json`.
3. No menu `Project Settings > XR Plug-in Management`, verifique se o **OpenXR** (ou Oculus) está habilitado para a plataforma desejada.
4. Abra a cena principal localizada em `Assets/Scenes/Main RV Scene.unity`.

---

*Desenvolvido para fins de estudo e como base para projetos avançados em Realidade Virtual.*
