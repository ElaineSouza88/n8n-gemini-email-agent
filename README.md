# 📧 AI Agent for Email: Triagem Inteligente com n8n & Google Gemini

[![n8n](https://img.shields.io/badge/n8n-Automation-ff6d5a?style=flat&logo=n8n)](https://n8n.io/)
[![Google Gemini](https://img.shields.io/badge/Google%20Gemini-AI%20Model-8E7CC3?style=flat&logo=googlegemini)](https://ai.google.dev/)
[![Gmail API](https://img.shields.io/badge/Gmail-Integration-EA4335?style=flat&logo=gmail)](https://developers.google.com/gmail/api)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Projeto de automação *No-Code/Low-Code* desenvolvido no **n8n** integrado ao **Google Gemini AI**. O objetivo principal é atuar como um triador de caixa de entrada em tempo real, analisando mensagens recebidas, classificando seu conteúdo contextual e tomando ações automáticas (lixeira, arquivamento ou retenção na Inbox).

---

## 📌 Visão Geral da Arquitetura

O fluxo intercepta novos e-mails assim que chegam ao servidor do Gmail, extrai seus metadados (remetente, assunto e corpo) e submete as informações a um agente cognitivo construído sobre o modelo **Google Gemini Chat Model**. 

Com base na resposta estruturada do agente, o fluxo executa o roteamento condicional via nó **Switch** para direcionar a ação correspondente no Gmail.
