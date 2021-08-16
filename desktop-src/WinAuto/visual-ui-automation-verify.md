---
title: Visual Automação da Interface do Usuário Verify
description: Visual Automação da Interface do Usuário Verify (Visual UIA Verify) é um Windows \ 32; Driver de GUI para a Biblioteca de Testes UIA projetada para testes manuais de automação de interface do usuário.
ms.assetid: 8AEB083E-785E-4F15-B708-2098A9A41B4E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c50fdd123d24c8a6ef4215ae2451cf49b854b60b26c5d741db1921c42f6f7aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563632"
---
# <a name="visual-ui-automation-verify"></a>Visual Automação da Interface do Usuário Verify

Visual Automação da Interface do Usuário Verify (Visual UIA Verify) é um driver Windows GUI para a Biblioteca de Testes UIA que foi projetado para testes manuais de automação de interface do usuário. Ele fornece uma interface para a funcionalidade da Biblioteca de Testes da UIA que elimina a sobrecarga de codificação de uma ferramenta de linha de comando.

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



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Menu</th>
<th>Comando</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Arquivo</strong></td>
<td><strong>Sair</strong></td>
<td>Saia do Visual UIA Verify.</td>
</tr>
<tr class="even">
<td><strong>Exibir</strong></td>
<td><strong>Realçar</strong></td>
<td>Realça o retângulo delimitativo do elemento selecionado no painel Árvore de <strong>Elementos de</strong> Automação. As opções a seguir estão disponíveis.
<ul>
<li><strong>Retângulo</strong>— uma linha vermelha sólida.</li>
<li><strong>Retângulo de esmaeamento</strong>— uma linha vermelha sólida que desaparece após alguns segundos.</li>
<li><strong>Raios e Retângulo</strong>— uma linha vermelha sólida com linhas de realçamento azul adicionais que radiam de cada canto do retângulo delimitado.</li>
<li><strong>Nenhum</strong>– nenhum realçando visível.</li>
</ul></td>
</tr>
<tr class="odd">
<td rowspan="2"><strong>Árvore de elementos de</strong>automação ${REMOVE}$<br />
</td>
<td><strong>Elemento Refresh Selected</strong></td>
<td>Atualize os filhos do elemento selecionado no painel Árvore de <strong>Elementos de</strong> Automação. A lista de elementos é estática e não será atualizada dinamicamente (automaticamente) se a árvore de elementos for mudada.</td>
</tr>
<tr class="even">
<td><strong>Navegação</strong></td>
<td>Navegue pela hierarquia de árvore de elementos para um dos elementos a seguir.
<ul>
<li><strong>Pai</strong>— vá para o elemento pai.</li>
<li><strong>Primeiro Filho</strong>— vá para o primeiro elemento filho.</li>
<li><strong>Próximo Irmão</strong>— vá para o primeiro elemento irmão.</li>
<li><strong>Irmão anterior</strong>— vá para o elemento irmão anterior.</li>
<li><strong>Último Filho</strong>— vá para o último elemento filho.</li>
</ul></td>

</tr>
<tr class="odd">
<td rowspan="3"><strong>Modo</strong>${REMOVE}$<br />
</td>
<td><strong>Always On Superior</strong></td>
<td>A janela Verificação do Visual UIA permanece na parte superior da ordem z da área de trabalho.</td>
</tr>
<tr class="even">
<td><strong>Modo de foco (usar Ctrl)</strong></td>
<td>Quando a tecla Ctrl é pressionada, o elemento sob o cursor do mouse é identificado como o elemento de interesse. O <strong>painel Árvore de Elementos</strong> de Automação é atualizado e o item correspondente na lista de elementos é realçada.</td>

</tr>
<tr class="odd">
<td><strong>Acompanhamento de foco</strong></td>
<td>Conforme o foco muda, o elemento com o foco é identificado como o elemento de interesse. O <strong>painel Árvore de Elementos</strong> de Automação é atualizado e o item correspondente na lista de elementos é realçada.</td>

</tr>
<tr class="even">
<td rowspan="6"><strong>Testa</strong>${REMOVE}$<br />
</td>
<td><strong>Ir para a esquerda</strong></td>
<td>Mova um nó para a esquerda na <strong>árvore Testes.</strong></td>
</tr>
<tr class="odd">
<td><strong>Subir</strong></td>
<td>Mova um nó para cima na <strong>árvore Testes.</strong></td>

</tr>
<tr class="even">
<td><strong>Ir para baixo</strong></td>
<td>Mova um nó para baixo na <strong>árvore Testes.</strong></td>

</tr>
<tr class="odd">
<td><strong>Ir para a direita</strong></td>
<td>Mova um nó para a direita na <strong>árvore Testes.</strong></td>

</tr>
<tr class="even">
<td><strong>Executar testes selecionados no elemento selecionado</strong></td>
<td>Execute os testes selecionados na <strong>árvore Testes</strong> no elemento selecionado.</td>

</tr>
<tr class="odd">
<td><strong>Filtrar problemas conhecidos</strong></td>
<td>Filtre bugs Automação da Interface do Usuário conhecidos dos resultados do teste.</td>

</tr>
<tr class="even">
<td><strong>Ajuda</strong></td>
<td><strong>Sobre o Visual Automação da Interface do Usuário Verify</strong></td>
<td>Exibir a versão do software e as informações de direitos autorais para Visual UIA Verify.</td>
</tr>
</tbody>
</table>



 

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

Um nó esmaecida  (indisponível) na Árvore de Elementos de Automação indica que o elemento é membro da exibição bruta do Automação da Interface do Usuário, mas não atendem às condições necessárias para ser considerado um membro da exibição de conteúdo ou exibição de controle. No entanto, o elemento ainda pode ser testado no Visual Automação da Interface do Usuário Verify. Para obter mais informações, consulte a [Visão geral Automação da Interface do Usuário árvore de dados.](uiauto-treeoverview.md)

Os comandos disponíveis na barra de ferramentas **árvore de elementos de automação** incluem:

-   **Atualizar**– atualize o nó selecionado e seus filhos. Esse comando não atualize toda a árvore de elementos, a menos que o nó raiz esteja selecionado.
-   **Pai (Ctrl+Shift+F6)**— Vá para o pai do nó atual.
-   **Primeiro Filho (Ctrl+Shift+F7)**— Vá para o primeiro filho do nó atual..
-   **Próximo Irmão (Ctrl+Shift+F8)**— vá para o próximo filho irmão do nó atual.
-   **Irmão anterior (Ctrl+Shift+F9)**— vá para o irmão anterior do nó atual.
-   **Último filho (Ctrl+Shift+F10)**— Vá para o último filho do nó atual.
-   **Acompanhamento de foco**— a alterne a seleção de nó para dentro ou para fora com base no acompanhamento de foco.

### <a name="tests-pane"></a>Painel Testes

O  painel Testes contém uma lista de testes Automação da Interface do Usuário organizados por tipo de teste **(** Elemento de Automação, Controle e Padrão **)** e prioridade ( Verificação de **Build,** Prioridade **0,** Prioridade **1,** Prioridade **2** e Prioridade **3**). Essa lista é gerada com base no tipo de controle do elemento selecionado no painel Árvore de **Elementos de** Automação. Para obter mais informações, consulte [Visão geral Automação da Interface do Usuário tipos de controle .](uiauto-controltypesoverview.md)

A captura de tela a seguir mostra **o painel** Testes.

![painel de teste](images/test-pane.png)

Os comandos disponíveis na barra de ferramentas **testes** incluem:

-   **Mostrar**— especifica os testes de automação da interface do usuário a serem exibidos; ou seja, exiba todos os testes ou apenas testes adequados para o tipo de controle do elemento selecionado na **árvore de elementos de automação** (padrão).
-   **Tipo**— especifica os tipos de teste a serem exibidos: **elemento de automação**, **padrão** ou **controle**.
-   **Prioridades**— especifica as prioridades de teste a serem exibidas: **verificação de compilação**, **prioridade 0**, **prioridade 1**, **prioridade 2** ou **prioridade 3**.
-   **Ir** para a esquerda — vá para o pai do nó atual.
-   **Subir**– vá para o irmão anterior do nó atual.
-   **Descer**– vá para o próximo irmão do nó atual.
-   **Vá** para a direita — vá para o primeiro filho do nó atual.
-   **Executar teste (s) selecionados**– executa os testes no elemento selecionado na árvore de **elementos de automação**.

### <a name="test-results-pane"></a>Painel de resultados de testes

O painel de **resultados de teste** contém a funcionalidade de log de verificação de UIA Visual. A captura de tela a seguir mostra o painel **resultados de teste** .

![painel de resultados de teste](images/test-results-pane.png)

Os comandos disponíveis na barra de ferramentas **resultados dos testes** incluem:

-   **Voltar**— Page Backward no histórico de exibição de relatório.
-   **Avançar**– avanço de página no histórico de exibição de relatório.
-   **Geral**— exibe um resumo dos resultados do teste (**passado**, **com falha** e um **erro inesperado**). O resultado do teste é vinculado à exibição **todos os resultados** . O comando **geral** exibe uma tabela como a mostrada a seguir.

    ![tabela de resultados de teste geral](images/overall-test-results.png)

-   **Todos os resultados**— exibe um log detalhado para cada resultado de teste, conforme mostrado nas tabelas a seguir.

    ![exemplo de detalhes de resultado de log da exibição todos os resultados](images/all-results-log.png)

    O nome do teste na tabela **todos os resultados** está vinculado a uma descrição do caso de teste para o elemento, como na tabela a seguir.

    ![detalhes do caso de teste](images/test-case-detail.png)

-   **Log completo**— exibe uma exibição alternativa do log detalhado para cada resultado de teste, conforme mostrado na captura de tela a seguir.

    ![exibição alternativa de um detalhe de caso de teste](images/alt-view-of-test-case-detail.png)

-   **XML**— EXIBE o XML bruto gerado pelo agente de log XML.
-   **Localização rápida**— pesquisa de texto simples da exibição atual no painel de **resultados de teste** .
-   **Abrir em nova janela**— abre a exibição atual em uma nova instância do Internet Explorer.

### <a name="properties-pane"></a>Painel Propriedades

O painel **Propriedades** contém uma lista de propriedades de automação da interface do usuário e valores de propriedade organizados por tipo de propriedade: **acessibilidade geral**, **identificação**, **padrões** (padrões de controle), **estado** e **visibilidade**. Os valores de propriedade são preenchidos dinamicamente com base no tipo de controle do objeto selecionado no painel de **árvore elementos de automação** . A captura de tela a seguir mostra o painel **Propriedades** .

![painel Propriedades](images/properties-pane.png)

Se o controle selecionado oferecer suporte a um padrão de controle específico, a verificação de UIA Visual fornecerá a capacidade de chamar métodos que são suportados por esse padrão de controle. Por exemplo, o [tipo de controle Window](uiauto-supportwindowcontroltype.md) dá suporte ao [padrão de controle Window](uiauto-implementingwindow.md), que tem um método [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) que pode ser invocado no painel **Propriedades** , conforme mostrado na captura de tela a seguir. Para obter mais informações, consulte [visão geral de tipos de controle de automação da interface do usuário](uiauto-controltypesoverview.md).

![método Close do padrão de controle Window invocado no painel Propriedades](images/close-invoked-from-properties-pane.png)

Os comandos disponíveis na barra de ferramentas **Propriedades** incluem:

-   **Atualizar**– atualize a árvore de **Propriedades** .
-   **Expandir tudo**– expande todos os nós na árvore de **Propriedades** .

 

 




