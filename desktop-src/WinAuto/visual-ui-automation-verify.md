---
title: Visual Automação da Interface do Usuário Verificar
description: Visual Automação da Interface do Usuário Verify (Visual UIA Verify) é um Windows \ 32; Driver de GUI para a Biblioteca de Testes UIA projetada para testes manuais de automação de interface do usuário.
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e8c6118914c791e04226dfa11d2c3bd9548368
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466843"
---
# <a name="visual-ui-automation-verify"></a>Visual Automação da Interface do Usuário Verificar

Visual Automação da Interface do Usuário Verify (Visual UIA Verify) é um driver de GUI Windows para a Biblioteca de Testes UIA que foi projetado para testes manuais de automação de interface do usuário. Ele fornece uma interface para a funcionalidade da Biblioteca de Testes da UIA que elimina a sobrecarga de codificação de uma ferramenta de linha de comando.

-   [Comandos de menu](#menu-commands)
-   [Painéis funcionais](#functional-panes)
    -   [Painel de árvore de elementos de automação](#automation-elements-tree-pane)
    -   [Painel Testes](#tests-pane)
    -   [Painel de resultados de testes](#test-results-pane)
    -   [Painel Propriedades](#properties-pane)

O Visual UIA Verify dá suporte apenas ao WUIALoggerXml.dll XML de Verificação de UIA na nativa. As transformações XML selecionáveis **pelo** usuário são incorporadas ao Visual UIA Verify para apresentar várias exibições do relatório do Resultados de Teste XML.

Por padrão, o Visual UIA Verify carrega Automação da Interface do Usuário provedor do lado do cliente fornecido com a versão original do Automação da Interface do Usuário. Você pode optar por não carregar esse provedor **adicionando /NOCLIENTSIDEPROVIDER** na opção de linha de comando VisualUIVerifyNative.exe.

A captura de tela a seguir mostra as principais áreas funcionais da interface do usuário Do Visual UIA Verify.

![principais áreas funcionais da interface do usuário do visual uia verify](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a>Comandos de menu

A tabela a seguir descreve os comandos no menu Verificar do Visual UIA.




| Menu | Comando | Descrição | 
|------|---------|-------------|
| <strong>Arquivo</strong> | <strong>Sair</strong> | Saia do Visual UIA Verify. | 
| <strong>Exibir</strong> | <strong>Realçar</strong> | Realça o retângulo delimitativo do elemento selecionado no painel Árvore de <strong>Elementos de</strong> Automação. As opções a seguir estão disponíveis.<ul><li><strong>Retângulo</strong>— uma linha vermelha sólida.</li><li><strong>Retângulo de esmaeamento</strong>— uma linha vermelha sólida que desaparece após alguns segundos.</li><li><strong>Raios e Retângulo</strong>— uma linha vermelha sólida com linhas de realçamento azul adicionais que radiam de cada canto do retângulo delimitado.</li><li><strong>Nenhum</strong>– nenhum realçando visível.</li></ul> | 
| <strong>Árvore de elementos de</strong>automação ${REMOVE}$<br /> | <strong>Elemento Refresh Selected</strong> | Atualize os filhos do elemento selecionado no painel Árvore de <strong>Elementos de</strong> Automação. A lista de elementos é estática e não será atualizada dinamicamente (automaticamente) se a árvore de elementos for mudada. | 
| <strong>Navegação</strong> | Navegue pela hierarquia de árvore de elementos para um dos elementos a seguir.<ul><li><strong>Pai</strong>— vá para o elemento pai.</li><li><strong>Primeiro Filho</strong>— vá para o primeiro elemento filho.</li><li><strong>Próximo Irmão</strong>— vá para o primeiro elemento irmão.</li><li><strong>Irmão anterior</strong>— vá para o elemento irmão anterior.</li><li><strong>Último Filho</strong>— vá para o último elemento filho.</li></ul> | 
| <strong>Modo</strong>${REMOVE}$<br /> | <strong>Always On Superior</strong> | A janela Verificação do Visual UIA permanece na parte superior da ordem z da área de trabalho. | 
| <strong>Modo de foco (usar Ctrl)</strong> | Quando a tecla Ctrl é pressionada, o elemento sob o cursor do mouse é identificado como o elemento de interesse. O <strong>painel Árvore de Elementos</strong> de Automação é atualizado e o item correspondente na lista de elementos é realçada. | 
| <strong>Acompanhamento de foco</strong> | Conforme o foco muda, o elemento com o foco é identificado como o elemento de interesse. O <strong>painel Árvore de Elementos</strong> de Automação é atualizado e o item correspondente na lista de elementos é realçada. | 
| <strong>Testa</strong>${REMOVE}$<br /> | <strong>Ir para a esquerda</strong> | Mova um nó para a esquerda na <strong>árvore Testes.</strong> | 
| <strong>Subir</strong> | Mova um nó para cima na <strong>árvore Testes.</strong> | 
| <strong>Ir para baixo</strong> | Mova um nó para baixo na <strong>árvore Testes.</strong> | 
| <strong>Ir para a direita</strong> | Mova um nó para a direita na <strong>árvore Testes.</strong> | 
| <strong>Executar testes selecionados no elemento selecionado</strong> | Execute os testes selecionados na <strong>árvore Testes</strong> no elemento selecionado. | 
| <strong>Filtrar problemas conhecidos</strong> | Filtre bugs Automação da Interface do Usuário conhecidos dos resultados do teste. | 
| <strong>Ajuda</strong> | <strong>Sobre o Visual Automação da Interface do Usuário Verify</strong> | Exibir a versão do software e as informações de direitos autorais para Visual UIA Verify. | 




 

## <a name="functional-panes"></a>Painéis funcionais

Esta seção descreve os painéis funcionais na interface do usuário Do Visual UIA Verify.

-   [Painel de árvore de elementos de automação](#automation-elements-tree-pane)
-   [Painel Testes](#tests-pane)
-   [Painel de resultados de testes](#test-results-pane)
-   [Painel Propriedades](#properties-pane)

### <a name="automation-elements-tree-pane"></a>Painel de árvore de elementos de automação

O **painel Árvore de Elementos de** Automação contém um instantâneo hierárquico de objetos de elemento de automação que estão disponíveis para teste. O elemento superior na árvore representa a área de trabalho.

Essa exibição é uma coleção estática que é compilada quando o Visual UIA Verify é iniciado. Para atualizar a exibição no nó selecionado, use o comando de menu Atualizar **Elemento Selecionado** ou o botão de barra de ferramentas.

A captura de tela a seguir mostra o painel **Árvore de Elementos de Automação.**

![painel de árvore de elementos de automação do visual uia verify](images/automation-elements-tree-pane.png)

Um nó esmaecida  (indisponível) na Árvore de Elementos de Automação indica que o elemento é membro da exibição bruta do Automação da Interface do Usuário, mas não atendem às condições necessárias para ser considerado um membro da exibição de conteúdo ou exibição de controle. No entanto, o elemento ainda pode ser testado no Visual Automação da Interface do Usuário Verify. Para obter mais informações, consulte Visão [geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)

Os comandos disponíveis na barra de ferramentas **árvore de elementos de automação** incluem:

-   **Atualizar**– atualize o nó selecionado e seus filhos. Esse comando não atualize toda a árvore de elementos, a menos que o nó raiz esteja selecionado.
-   **Pai (Ctrl+Shift+F6)**— Vá para o pai do nó atual.
-   **Primeiro Filho (Ctrl+Shift+F7)**— Vá para o primeiro filho do nó atual..
-   **Próximo Irmão (Ctrl+Shift+F8)**— vá para o próximo filho irmão do nó atual.
-   **Irmão anterior (Ctrl+Shift+F9)**— vá para o irmão anterior do nó atual.
-   **Último filho (Ctrl+Shift+F10)**— Vá para o último filho do nó atual.
-   **Acompanhamento de foco**— a alterne a seleção de nó para dentro ou para fora com base no acompanhamento de foco.

### <a name="tests-pane"></a>Painel Testes

O  painel Testes contém uma lista de testes Automação da Interface do Usuário organizados por tipo de teste **(** Elemento de Automação, Controle e Padrão **)** e prioridade ( Verificação de **build,** Prioridade **0,** Prioridade **1,** Prioridade **2** e Prioridade **3**). Essa lista é gerada com base no tipo de controle do elemento selecionado no painel Árvore de **Elementos de** Automação. Para obter mais informações, consulte [Visão geral Automação da Interface do Usuário tipos de controle .](uiauto-controltypesoverview.md)

A captura de tela a seguir mostra **o painel** Testes.

![painel de teste](images/test-pane.png)

Os comandos disponíveis na barra **de ferramentas Testes** incluem:

-   **Mostrar**– especifica o Automação da Interface do Usuário testes a exibir; ou seja, exibir todos os testes ou apenas testes adequados para o tipo de controle do elemento selecionado na Árvore de Elementos de **Automação** (padrão).
-   **Tipo**— especifica os tipos de teste a exibir: **Elemento de Automação,** **Padrão** ou **Controle**.
-   **Prioridades**— especifica as prioridades de teste a exibir: Verificação de **Build,** Prioridade **0,** **Prioridade 1,** **Prioridade 2** ou **Prioridade 3.**
-   **Ir para** a esquerda — vá para o pai do nó atual.
-   **Ir para Cima**— vá para o irmão anterior do nó atual.
-   **Ir para** Baixo – vá para o próximo irmão do nó atual.
-   **Ir para** a direita — vá para o primeiro filho do nó atual.
-   **Executar testes selecionados**— executa os testes no elemento selecionado na Árvore **de Elementos de Automação**.

### <a name="test-results-pane"></a>Painel de resultados de testes

O **painel Resultados de Teste** contém a funcionalidade de registro em log do Visual UIA Verify. A captura de tela a seguir mostra **o Resultados de Teste** painel.

![painel de resultados do teste](images/test-results-pane.png)

Os comandos disponíveis na barra **de ferramentas Resultados** de Testes incluem:

-   **Voltar**– página para trás no histórico de exibição de relatório.
-   **Encaminhar**– encaminhar página no histórico de exibição de relatório.
-   **Geral**— Exibe um resumo dos resultados do teste (**Aprovado,** **Com Falha** e **Erro Inesperado).** O resultado do teste é vinculado à **exibição Todos os** Resultados. O **comando** Geral exibe uma tabela como a seguinte.

    ![tabela geral de resultados do teste](images/overall-test-results.png)

-   **Todos os** Resultados – exibe um log detalhado para cada resultado de teste, conforme mostrado nas tabelas a seguir.

    ![exemplo de detalhes do resultado do log da exibição todos os resultados](images/all-results-log.png)

    O nome do teste na **tabela Todos os Resultados** está vinculado a uma descrição de caso de teste para o elemento , como na tabela a seguir.

    ![detalhes do caso de teste](images/test-case-detail.png)

-   **Log completo**— exibe uma exibição alternativa do log detalhado para cada resultado de teste, conforme mostrado na captura de tela a seguir.

    ![exibição alternativa de um detalhe de caso de teste](images/alt-view-of-test-case-detail.png)

-   **XML**— exibe o XML bruto gerado pelo agente XML.
-   **Quick Find**— Pesquisa de texto simples da exibição atual no **Resultados de Teste** painel.
-   **Abrir em Nova Janela**— abre a exibição atual em uma nova instância do Internet Explorer.

### <a name="properties-pane"></a>Painel Propriedades

O **painel** Propriedades contém uma lista de Automação da Interface do Usuário propriedades e valores de propriedade organizados por tipo de propriedade: Acessibilidade **Geral,** **Identificação,** **Padrões** (padrões de **controle),** Estado e **Visibilidade.** Os valores de propriedade são preenchidos dinamicamente com base no tipo de controle do objeto selecionado no painel Árvore de **Elementos de** Automação. A captura de tela a seguir mostra **o painel** Propriedades.

![painel propriedades](images/properties-pane.png)

Se o controle selecionado dá suporte a um padrão de controle específico, o Visual UIA Verify fornece a capacidade de chamar métodos compatíveis com esse padrão de controle. Por exemplo, [](uiauto-supportwindowcontroltype.md) o tipo de controle Janela dá suporte ao padrão de  controle [Janela](uiauto-implementingwindow.md), que tem um método [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) que pode ser invocado do painel Propriedades, conforme mostrado na captura de tela a seguir. Para obter mais informações, consulte [Visão geral Automação da Interface do Usuário tipos de controle .](uiauto-controltypesoverview.md)

![método close do padrão de controle de janela invocado do painel de propriedades](images/close-invoked-from-properties-pane.png)

Os comandos disponíveis na barra **de ferramentas Propriedades** incluem:

-   **Atualizar**– atualize a **árvore** Propriedades.
-   **Expanda Tudo**— expande todos os nós na **árvore Propriedades.**

 

 




