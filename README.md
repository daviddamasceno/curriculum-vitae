# 📄 Resume as Code (DevOps Automation)

Este repositório contém o currículo profissional de **David Damasceno Farias**, estruturado em HTML e automatizado para gerar versões em PDF de forma sincronizada via CI/CD.

## 🚀 O Projeto

A ideia central é tratar o currículo como um artefato de software. Em vez de editar manualmente arquivos PDF ou Word, a "fonte da verdade" é um arquivo HTML estilizado. Sempre que há uma atualização no conteúdo, o pipeline de automação entra em ação para garantir que todos os formatos estejam atualizados.

### 🛠️ Fluxo de Automação (CI/CD)

O projeto utiliza **GitHub Actions** para gerenciar o ciclo de vida do documento. O workflow opera da seguinte forma:

1. **Trigger:** O pipeline é acionado automaticamente em cada `push` que altere o arquivo `curriculum.html` ou manualmente via `workflow_dispatch`.
    
2. **Ambiente:** Executado em um runner `ubuntu-latest`.
    
3. **Engine de Conversão:** Utiliza o **WeasyPrint**, uma biblioteca visual de alta fidelidade que renderiza o CSS para PDF de forma profissional, mantendo a integridade do layout estrutural.
    
4. **Sincronização:** O PDF gerado é commitado de volta ao repositório pelo `github-actions[bot]`, garantindo que a versão disponível para download seja sempre a mais recente.
    

### 🔧 Tecnologias Utilizadas

- **HTML5/CSS3:** Para a estrutura e design do currículo.
    
- **GitHub Actions:** Orquestração do pipeline de entrega contínua.
    
- **WeasyPrint (Python):** Engine de renderização de documentos.
    
- **Git:** Versionamento e controle de histórico do documento.
    

## 📖 Como utilizar

Se você deseja clonar este projeto para seu próprio currículo:

1. Edite o arquivo `curriculum.html` com suas informações profissionais.
    
2. Certifique-se de que o caminho do arquivo no arquivo `.yml` do workflow corresponde ao nome do seu arquivo HTML.
    
3. Ao realizar o `push`, o GitHub Actions gerará o `.pdf` automaticamente na raiz do seu repositório.
    

---

_Mantido com ❤️ e automação por um Engenheiro de DevOps._

---