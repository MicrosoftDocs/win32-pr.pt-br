---
title: Verificação de automação da interface do usuário Visual
description: verificação de automação da interface do usuário visual (verificação de UIA visual) é um Windows \ 32; Driver de GUI para a biblioteca de teste UIA projetada para teste manual da automação da interface do usuário.
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
# <a name="visual-ui-automation-verify"></a>Verificação de automação da interface do usuário Visual

a verificação de automação da interface do usuário visual (verificação do visual UIA) é um driver de GUI Windows para a biblioteca de testes UIA que foi projetada para teste manual da automação da interface do usuário. Ele fornece uma interface para a funcionalidade de biblioteca de teste UIA que elimina a sobrecarga de codificação de uma ferramenta de linha de comando.

-   [Comandos de menu](#menu-commands)
-   [Painéis funcionais](#functional-panes)
    -   [Painel de árvore de elementos de automação](#automation-elements-tree-pane)
    -   [Painel de testes](#tests-pane)
    -   [Painel de resultados de testes](#test-results-pane)
    -   [Painel Propriedades](#properties-pane)

A verificação de UIA Visual dá suporte apenas à verificação de UIA de agente XML (WUIALoggerXml.dll) nativamente. As transformações XML selecionáveis pelo usuário são incorporadas à verificação de UIA Visual para apresentar várias exibições do relatório do agente de log XML no painel de **resultados de teste** .

Por padrão, o Visual UIA Verify carrega o provedor do lado do cliente de automação da interface do usuário fornecido com a versão original da automação da interface do usuário. Você pode optar por não carregar esse provedor adicionando **/NOCLIENTSIDEPROVIDER** na opção de linha de comando de VisualUIVerifyNative.exe.

A captura de tela a seguir mostra as principais áreas funcionais da interface do usuário do Visual UIA Verify.

![principais áreas funcionais da interface do usuário de verificação do Visual UIA](images/visual-uia-verify-ui.png)

## <a name="menu-commands"></a>Comandos de menu

A tabela a seguir descreve os comandos no menu verificar do Visual UIA.



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
<td>Saia da verificação de UIA Visual.</td>
</tr>
<tr class="even">
<td><strong>Exibir</strong></td>
<td><strong>Realçar</strong></td>
<td>Realce o retângulo delimitador do elemento selecionado no painel de <strong>árvore elementos de automação</strong> . As opções a seguir estão disponíveis.
<ul>
<li><strong>Rectangle</strong>— uma linha vermelha sólida.</li>
<li><strong>Retângulo esmaecido</strong>— uma linha vermelha sólida que desaparece depois de alguns segundos.</li>
<li><strong>Raios e retângulo</strong>— uma linha vermelha sólida com linhas de realce azul adicionais que radiam de cada canto do retângulo delimitador.</li>
<li><strong>Nenhum</strong>– nenhum realce visível.</li>
</ul></td>
</tr>
<tr class="odd">
<td rowspan="2"><strong>Árvore de elementos de automação</strong>$ {remove} $<br />
</td>
<td><strong>Atualizar elemento selecionado</strong></td>
<td>Atualize os filhos do elemento selecionado no painel de <strong>árvore elementos de automação</strong> . A lista de elementos é estática e não é atualizada dinamicamente (automaticamente) se a árvore do elemento for alterada.</td>
</tr>
<tr class="even">
<td><strong>Navegação</strong></td>
<td>Navegue pela hierarquia de árvore de elementos para um dos elementos a seguir.
<ul>
<li><strong>Pai</strong>– vá para o elemento pai.</li>
<li><strong>Primeiro filho</strong>— vá para o primeiro elemento filho.</li>
<li><strong>Próximo irmão</strong>— ir para o primeiro elemento irmão.</li>
<li><strong>Irmão anterior</strong>— vá para o elemento irmão anterior.</li>
<li><strong>Último filho</strong>– vá para o último elemento filho.</li>
</ul></td>

</tr>
<tr class="odd">
<td rowspan="3"><strong>Mode</strong>$ {remove} $<br />
</td>
<td><strong>Always On superior</strong></td>
<td>A janela Verificação de UIA Visual permanece na parte superior da ordem z da área de trabalho.</td>
</tr>
<tr class="even">
<td><strong>Modo de foco (use Ctrl)</strong></td>
<td>Quando a tecla CTRL é pressionada, o elemento sob o cursor do mouse é identificado como o elemento de interesse. O painel de <strong>árvore elementos de automação</strong> é atualizado e o item correspondente na lista de elementos é realçado.</td>

</tr>
<tr class="odd">
<td><strong>Acompanhamento de foco</strong></td>
<td>À medida que o foco é alterado, o elemento com o foco é identificado como o elemento de interesse. O painel de <strong>árvore elementos de automação</strong> é atualizado e o item correspondente na lista de elementos é realçado.</td>

</tr>
<tr class="even">
<td rowspan="6"><strong>Testes</strong>$ {remove} $<br />
</td>
<td><strong>Ir para a esquerda</strong></td>
<td>Mova um nó para a esquerda na árvore de <strong>testes</strong> .</td>
</tr>
<tr class="odd">
<td><strong>Subir</strong></td>
<td>Mova um nó para cima na árvore de <strong>testes</strong> .</td>

</tr>
<tr class="even">
<td><strong>Descer</strong></td>
<td>Mova um nó para baixo na árvore de <strong>testes</strong> .</td>

</tr>
<tr class="odd">
<td><strong>Ir para a direita</strong></td>
<td>Mova um nó para a direita na árvore de <strong>testes</strong> .</td>

</tr>
<tr class="even">
<td><strong>Executar teste (s) selecionados no elemento selecionado</strong></td>
<td>Execute os testes selecionados na árvore de <strong>testes</strong> no elemento selecionado.</td>

</tr>
<tr class="odd">
<td><strong>Filtrar problemas conhecidos</strong></td>
<td>Filtre bugs de automação da interface do usuário conhecidos dos resultados do teste.</td>

</tr>
<tr class="even">
<td><strong>Ajuda</strong></td>
<td><strong>Sobre a verificação da automação da interface do usuário Visual</strong></td>
<td>Exiba a versão do software e as informações de direitos autorais para verificação de UIA Visual.</td>
</tr>
</tbody>
</table>



 

## <a name="functional-panes"></a>Painéis funcionais

Esta seção descreve os painéis funcionais na interface do usuário de verificação do Visual UIA.

-   [Painel de árvore de elementos de automação](#automation-elements-tree-pane)
-   [Painel de testes](#tests-pane)
-   [Painel de resultados de testes](#test-results-pane)
-   [Painel Propriedades](#properties-pane)

### <a name="automation-elements-tree-pane"></a>Painel de árvore de elementos de automação

O painel de **árvore elementos de automação** contém um instantâneo hierárquico dos objetos de elemento de automação que estão disponíveis para teste. O elemento superior na árvore representa a área de trabalho.

Essa exibição é uma coleção estática que é compilada quando a verificação de UIA Visual é iniciada. Para atualizar a exibição no nó selecionado, use o comando de menu **Atualizar elemento selecionado** ou o botão da barra de ferramentas.

A captura de tela a seguir mostra o painel de **árvore elementos de automação** .

![painel de árvore de elementos de automação da verificação de UIA Visual](images/automation-elements-tree-pane.png)

Um nó esmaecido (não disponível) na **árvore elementos de automação** indica que o elemento é um membro da exibição bruta de automação da interface do usuário, mas não atende às condições necessárias para ser considerado um membro da exibição de conteúdo ou da exibição de controle. No entanto, o elemento ainda pode ser testado da verificação da automação da interface do usuário visual. Para obter mais informações, consulte [visão geral da árvore de automação da interface do usuário](uiauto-treeoverview.md).

Os comandos disponíveis na barra de ferramentas da **árvore elementos de automação** incluem:

-   **Atualizar**— atualize o nó selecionado e seus filhos. Esse comando não atualiza toda a árvore de elementos, a menos que o nó raiz esteja selecionado.
-   **Pai (Ctrl + Shift + F6)**– vá para o pai do nó atual.
-   **Primeiro filho (Ctrl + Shift + F7)**– vá para o primeiro filho do nó atual.
-   **Próximo irmão (Ctrl + Shift + F8)**— vá para próximo filho irmão do nó atual.
-   **Irmão anterior (Ctrl + Shift + F9)**– vá para irmão anterior do nó atual.
-   **Último filho (Ctrl + Shift + F10)**– vá para o último filho do nó atual.
-   **Acompanhamento de foco**— ativar ou desativar a seleção de nó com base no controle de foco.

### <a name="tests-pane"></a>Painel de testes

O painel de **testes** contém uma lista de testes de automação de interface do usuário organizados por tipo de teste (**elemento de automação**, **controle** e **padrão**) e prioridade (**verificação de compilação**, **prioridade 0**, **prioridade 1**, **prioridade 2** e **prioridade 3**). Essa lista é gerada com base no tipo de controle do elemento selecionado no painel de **árvore elementos de automação** . Para obter mais informações, consulte [visão geral de tipos de controle de automação da interface do usuário](uiauto-controltypesoverview.md).

A captura de tela a seguir mostra o painel **testes** .

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

O **Resultados de Teste** painel contém a funcionalidade de registro em log do Visual UIA Verify. A captura de tela a seguir mostra **o Resultados de Teste** painel.

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
-   **Pesquisa Rápida**– pesquisa de texto simples da exibição atual no **Resultados de Teste** de texto.
-   **Abrir em Nova Janela**— abre a exibição atual em uma nova instância do Internet Explorer.

### <a name="properties-pane"></a>Painel Propriedades

O **painel** Propriedades contém uma lista de Automação da Interface do Usuário propriedades e valores de propriedade organizados por tipo de propriedade: Acessibilidade **Geral,** **Identificação,** **Padrões** (padrões de controle), **Estado** e **Visibilidade.** Os valores de propriedade são preenchidos dinamicamente com base no tipo de controle do objeto selecionado no painel Árvore de **Elementos de** Automação. A captura de tela a seguir mostra **o painel** Propriedades.

![painel propriedades](images/properties-pane.png)

Se o controle selecionado dá suporte a um padrão de controle específico, o Visual UIA Verify fornece a capacidade de chamar métodos compatíveis com esse padrão de controle. Por exemplo, [](uiauto-supportwindowcontroltype.md) o tipo de controle Janela dá suporte ao padrão de  controle Janela [,](uiauto-implementingwindow.md)que tem um método [**Close**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-close) que pode ser invocado do painel Propriedades, conforme mostrado na captura de tela a seguir. Para obter mais informações, consulte [Visão geral Automação da Interface do Usuário tipos de controle .](uiauto-controltypesoverview.md)

![método close do padrão de controle de janela invocado do painel de propriedades](images/close-invoked-from-properties-pane.png)

Os comandos disponíveis na barra **de ferramentas Propriedades** incluem:

-   **Atualizar**– atualize a **árvore** Propriedades.
-   **Expanda Tudo**— expande todos os nós na **árvore Propriedades.**

 

 




