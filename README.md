# IntGest Sign ✍️

![Status](https://img.shields.io/badge/Status-Em_Produção-success?style=for-the-badge) ![Tech](https://img.shields.io/badge/Tech-Flutter_|_ML_Kit-blue?style=for-the-badge) ![Compliance](https://img.shields.io/badge/Legal-Decreto_10.543-lightgrey?style=for-the-badge)

> **Nota:** Este repositório é um **estudo de caso** de um software proprietário desenvolvido por mim na [IntellGest](https://www.linkedin.com/company/intellgest/). Ele serve como demonstração de portfólio técnico e **não contém o código-fonte original**.

---

## 📱 Sobre o Projeto

O **IntGest Sign** é uma solução móvel completa para desmaterialização de processos físicos. O aplicativo permite que usuários assinem documentos digitalmente com a mesma validade jurídica de uma assinatura física (caneta no papel), estando em total conformidade com o **Decreto Nº 10.543/2020** do Governo Federal.

O objetivo foi criar uma ferramenta que transformasse o smartphone em um scanner portátil e token de segurança, eliminando a necessidade de impressoras e cartórios para processos internos.

## 👨‍💻 Desafios Técnicos & Soluções

Como responsável pelo desenvolvimento, o maior desafio foi implementar um scanner de documentos fluido e preciso utilizando apenas a câmera do celular, garantindo legibilidade para documentos oficiais.

### 1. Scanner Inteligente (Computer Vision) 📷
Implementei um módulo de digitalização automática utilizando **ML Kit (Google)** e **Vision Kit (iOS)**.
* **Detecção de Bordas:** O app identifica o documento em tempo real, ignorando o fundo.
* **Perspectiva & Auto-Crop:** Correção matemática automática da angulação da foto (deskewing) para que o documento fique reto, mesmo se fotografado de lado.
* **Filtros de Imagem:** Processamento de imagem para converter fotos em documentos P&B ou Grayscale de alto contraste, otimizando o tamanho do arquivo final.

### 2. Assinatura Digital & Segurança 🔐
Implementação do fluxo de criptografia para garantir a integridade do documento.
* **Certificação:** O app integra-se com a infraestrutura de chaves públicas da IntGest para emitir e validar assinaturas.
* **Imutabilidade:** Após assinado, o PDF é selado digitalmente, garantindo que qualquer alteração posterior invalide a assinatura.

## 🛠️ Tech Stack

* **Linguagem:** Dart
* **Framework:** Flutter
* **Machine Learning / Visão Computacional:**
    * Google ML Kit (Android)
    * Vision Framework (iOS)
* **Manipulação de PDF:** Integração nativa para renderização e "flattening" de assinaturas.
* **Segurança:** Criptografia assimétrica para assinatura digital.
