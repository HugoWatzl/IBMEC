## Resumo Simples para Estudo: DevOps

### 🤝 O que é DevOps?
**DevOps** é uma **cultura** que une as equipes de **Desenvolvimento (Dev)** e **Operações (Ops)**. Em vez de trabalharem separadas, elas colaboram desde o início para entregar software de forma mais **rápida e segura**. O foco é na **comunicação**, **colaboração** e **automação** de processos.

### 💾 Controle de Versão: Git e DVCS
Um **Controlador de Versão** é uma ferramenta para salvar o histórico do seu código. O **Git** é o mais famoso.
A principal característica do Git é ser um **DVCS (Sistema de Controle de Versão Distribuído)**. Isso significa que cada desenvolvedor tem uma **cópia completa** do projeto e seu histórico na sua própria máquina. Por isso, os **commits** (salvar uma versão) são feitos primeiro **localmente**, sem precisar de internet.

### 🗂️ Organizando o Código: Monorepo vs. Multirepos
* **Multirepos:** Vários projetos, cada um em seu próprio repositório. É mais simples para projetos independentes.
* **Monorepo:** Um único repositório gigante com o código de todos os projetos da empresa. A principal **vantagem** é que facilita o **compartilhamento de código** e a realização de mudanças que afetam vários sistemas de uma vez.

### 🚀 O Pipeline Automatizado: CI/CD
Este é o coração da automação em DevOps.
1.  **Integração Contínua (CI - Continuous Integration):** É o primeiro passo. Os desenvolvedores integram seu código no repositório principal várias vezes ao dia. Cada integração dispara **builds e testes automatizados**. A função da CI é **validar o código** e encontrar erros o mais cedo possível.

2.  **Entrega Contínua (Continuous Delivery):** É o passo seguinte à CI. O código que passou nos testes é **automaticamente preparado e fica pronto para ir para produção**. Porém, o lançamento final depende de uma **aprovação manual** (alguém aperta o botão para liberar).

3.  **Deployment Contínuo (Continuous Deployment):** É o nível máximo de automação. Se o código passar por todos os testes, ele é **lançado em produção de forma 100% automática**, sem nenhuma intervenção humana.

### ✅ A Importância dos Testes Automatizados
Os **testes automatizados** são a **rede de segurança** de todo o pipeline DevOps. Eles garantem a qualidade do código a cada passo e dão a confiança necessária para que a integração e a entrega possam ser feitas de forma contínua e segura. Sem eles, a automação do CI/CD seria impossível.

---

## Perguntas para Estudo (

#### Múltipla Escolha

1.  **Sobre integração contínua (CI), entrega contínua e deployment contínuo, marque a correta:**<br>
    a) CI depende de aprovação manual para rodar os testes.<br>
    b) Deployment contínuo exige uma aprovação manual antes do lançamento.<br>
    c) Delivery contínuo lança o código em produção de forma 100% automática.<br>
    d) Deployment contínuo permite deploys automatizados se os testes forem aprovados.<br>
    e) CI e Delivery contínuo são a mesma coisa.

    <details>
      <summary>Clique para ver a resposta</summary>
      **d) Deployment contínuo permite deploys automatizados se os testes forem aprovados.**<br>
      *Justificativa: Esta é a definição exata. Se os testes automatizados passam, o código vai para produção automaticamente.
    </details>
    <br>

2.  **O que caracteriza um DVCS (Sistema de Controle de Versão Distribuído) como o Git?**<br>
    a) Os commits só podem ser feitos com acesso à internet.<br>
    b) Não existe histórico de versões, apenas o código atual.<br>
    c) Cada desenvolvedor possui uma cópia completa do repositório localmente.<br>
    d) Não é possível criar branches ou versões paralelas.<br>
    e) Só funciona através de uma interface gráfica.<br>

     <details>
    <summary>Clique para ver a resposta</summary>
      **c) Cada desenvolvedor possui uma cópia completa do repositório localmente.**<br>
      *Justificativa: Esta é a principal característica de um sistema distribuído, permitindo commits locais e trabalho offline.
    </details><br>

#### Verdadeiro ou Falso

3.  **(  ) CI (Integração Contínua) tem como principal objetivo validar o código por meio de testes automatizados a cada nova integração.**

4.  **(  ) No Git, por ser um DVCS, os commits são feitos primeiro diretamente no repositório central na nuvem.**

5.  **(  ) DevOps é principalmente uma ferramenta de software que automatiza tarefas, e não uma mudança cultural.**

<details>
      <summary>Clique para ver a justificativa</summary>
      Gabarito :V, F, F
    </details>

#### Discursivas Curtas

6.  **Qual é a principal vantagem de uma abordagem Monorepo citada no resumo?**

<details>
      <summary>Clique para ver a resposta</summary>
      A principal vantagem é que facilita o **compartilhamento de código** entre equipes e a realização de mudanças que afetam vários sistemas de uma só vez.
    </details><br>

7.  **Explique com suas palavras a principal diferença entre Delivery Contínuo e Deployment Contínuo.**
<details>
      <summary>Clique para ver a resposta</summary>
      A principal diferença está no passo final. No **Delivery Contínuo**, o lançamento para produção é **manual** (alguém precisa aprovar/apertar um botão). No **Deployment Contínuo**, o lançamento é **100% automático** se os testes passarem.
    </details><br>

8.  **Qual é o papel fundamental dos testes automatizados no contexto do DevOps?**
    <details>
      <summary>Clique para ver a resposta</summary>
      Eles são a **rede de segurança** de todo o pipeline. Garantem a qualidade contínua do código e dão a confiança necessária para permitir a automação da integração (CI) e da entrega/deployment (CD).
    </details><br>