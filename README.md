# **AltaGuard – Documentação Inicial**

## **1. Descrição do Projeto**

O **AltaGuard IA** é um MVP para análise de prontuários clínicos, verificação de prescrições, checagem de disponibilidade de medicamentos e avaliação de critérios de alta hospitalar.

O objetivo é identificar possíveis inconsistências, erros de dose, alergias e riscos clínicos, oferecendo uma camada básica de apoio à decisão.

---

## **2. Tecnologias Utilizadas**

### **Frontend**

* Next.js
* Axios para comunicação com API

### **Backend**

* Java 11
* Spring Boot
* REST API
* Maven

---

## **3. Estrutura Inicial do Repositório**

### **FrontEnd**

```
clinical-ai-prototype/
├── app/
│   ├── globals.css
│   ├── layout.tsx
│   └── page.tsx
├── components/
│   ├── clinical-ai/
│   │   ├── decision-modal.tsx
│   │   ├── interaction-history.tsx
│   │   ├── patient-record-display.tsx
│   │   └── safe-discharge-checklist.tsx
│   ├── ui/
│   │   ├── accordion.tsx
│   │   ├── alert-dialog.tsx
│   │   ├── alert.tsx
│   │   ├── aspect-ratio.tsx
│   │   ├── avatar.tsx
│   │   ├── badge.tsx
│   │   ├── breadcrumb.tsx
│   │   ├── button-group.tsx
│   │   ├── button.tsx
│   │   ├── calendar.tsx
│   │   ├── card.tsx
│   │   ├── carousel.tsx
│   │   ├── chart.tsx
│   │   ├── checkbox.tsx
│   │   ├── collapsible.tsx
│   │   ├── command.tsx
│   │   ├── context-menu.tsx
│   │   ├── dialog.tsx
│   │   ├── drawer.tsx
│   │   ├── dropdown-menu.tsx
│   │   ├── empty.tsx
│   │   ├── field.tsx
│   │   ├── form.tsx
│   │   ├── hover-card.tsx
│   │   ├── input-group.tsx
│   │   ├── input-otp.tsx
│   │   ├── input.tsx
│   │   ├── item.tsx
│   │   ├── kbd.tsx
│   │   ├── label.tsx
│   │   ├── menubar.tsx
│   │   ├── navigation-menu.tsx
│   │   ├── pagination.tsx
│   │   ├── popover.tsx
│   │   ├── progress.tsx
│   │   ├── radio-group.tsx
│   │   ├── resizable.tsx
│   │   ├── scroll-area.tsx
│   │   ├── select.tsx
│   │   ├── separator.tsx
│   │   ├── sheet.tsx
│   │   ├── sidebar.tsx
│   │   ├── skeleton.tsx
│   │   ├── slider.tsx
│   │   ├── sonner.tsx
│   │   ├── spinner.tsx
│   │   ├── switch.tsx
│   │   ├── table.tsx
│   │   ├── tabs.tsx
│   │   ├── textarea.tsx
│   │   ├── toast.tsx
│   │   ├── toaster.tsx
│   │   ├── toggle-group.tsx
│   │   ├── toggle.tsx
│   │   ├── tooltip.tsx
│   │   ├── use-mobile.tsx
│   │   └── use-toast.ts
│   └── theme-provider.tsx
├── hooks/
│   ├── use-mobile.ts
│   └── use-toast.ts
├── lib/
│   ├── clinical-data.ts
│   └── utils.ts
├── public/
│   ├── apple-icon.png
│   ├── icon-dark-32x32.png
│   ├── icon-light-32x32.png
│   ├── icon.svg
│   ├── placeholder-logo.png
│   ├── placeholder-logo.svg
│   ├── placeholder-user.jpg
│   ├── placeholder.jpg
│   └── placeholder.svg
├── styles/
│   └── globals.css
├── components.json
├── next.config.mjs
├── package.json
├── pnpm-lock.yaml
├── postcss.config.mjs
└── tsconfig.json
```

### **BackEnd**

*(estrutura não detalhada no arquivo)*

---

## **4. Instruções de Instalação**

### **Frontend**

```sh
cd frontend
npm install
npm run dev
```

Acesse: **[http://localhost:3000](http://localhost:3000)**

### **Backend**

```sh
cd backend
java -jar api.hackstars.com.br
```

Acesse: **[http://localhost:8080](http://localhost:8080)**

---

## **5. Endpoints Principais**

### **medical-prescription-controller**

**POST** `/api/medical-prescription`
Avalia a prescrição médica de um paciente.

### **medical-evaluation-controller**

**POST** `/api/medical-evaluation`
Avalia o prontuário de um paciente.

### **medical-discharge-controller**

**POST** `/api/medical-discharge`
Avalia possível alta de um paciente.

### **medical-brief-controller**

**POST** `/api/medical-brief`
Produz um resumo histórico de um paciente.

---

## **6. Decisões Técnicas Iniciais**

* Next.js escolhido pela rapidez para construir interfaces.
* Spring Boot escolhido por robustez na construção de APIs REST.
* JSON definido como padrão de entrada para prontuários e estoque.
* Regras clínicas implementadas de forma isolada no backend.
* Estrutura modular para permitir trabalho paralelo da equipe.

---

## **7. Escopo Inicial**

### **Must**

* Processar prontuário JSON
* Validar dose e função renal
* Checar alergias
* Avaliar critérios básicos de alta
* Verificar disponibilidade de medicamento

### **Should**

* Priorizar alertas
* Registrar logs mínimos

### **Could**

* Interface mais detalhada
* Visualização de risco

### **Won’t**

* Integrações hospitalares reais
* Machine Learning avançado

