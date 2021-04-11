---
title: Rotinas de verificação
description: Esta seção descreve as rotinas de verificação que o verificador de acessibilidade da interface do usuário pode executar para testar a implementação de acessibilidade de um aplicativo.
ms.assetid: 0ff38f83-5741-4c0e-a070-a8385f95eba3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78eea821a4c918078c6390e33fa7046de1452f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292243"
---
# <a name="verification-routines"></a>Rotinas de verificação

Esta seção descreve as rotinas de verificação que o verificador de acessibilidade da interface do usuário pode executar para testar a implementação de acessibilidade de um aplicativo.



<table>
<thead>
<tr class="header">
<th>Categoria</th>
<th>Rotina</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><strong>Consistência</strong>$ {remove} $<br />
</td>
<td><strong>ScreenReader</strong></td>
<td>Compila todos os elementos visíveis no destino de verificação e os exibe em um controle ListView na ordem em que um leitor de tela padrão os anuncia para um usuário.</td>
</tr>
<tr class="even">
<td><strong>UiaScreenReader</strong></td>
<td>O mesmo que <strong>ScreenReader</strong>, mas para implementações UIA.</td>

</tr>
<tr class="odd">
<td rowspan="2"><strong>Navegação</strong>$ {remove} $<br />
</td>
<td><strong>CheckTreeDepth</strong></td>
<td>Envia caracteres de tabulação (ou Shift + Tab) como entrada para o destino de verificação para confirmar se a interface do usuário do destino não é excessivamente complexa ou inacessível usando a navegação de teclado padrão.</td>
</tr>
<tr class="even">
<td><strong>CheckTabbingUia</strong></td>
<td>Envia caracteres de tabulação (ou Shift + Tab) como entrada para o destino de verificação para confirmar se todos os elementos que podem ser focados na interface do usuário são acessíveis de maneira ordenada e lógica usando a navegação de teclado padrão.</td>

</tr>
<tr class="odd">
<td rowspan="5"><strong>Propriedades</strong>$ {remove} $<br />
</td>
<td><strong>CheckRole</strong></td>
<td>Confirma que cada elemento focado na interface do usuário relata uma função de MSAA lógica válida e que o controle tem um valor conforme exigido por essa função.</td>
</tr>
<tr class="even">
<td><strong>CheckState</strong></td>
<td>Confirma que cada elemento focado na interface do usuário relata um estado de MSAA lógico válido.</td>

</tr>
<tr class="odd">
<td><strong>CHECKNAME</strong></td>
<td>Confirma que cada elemento focado na interface do usuário relata um nome de MSAA lógico válido.</td>

</tr>
<tr class="even">
<td><strong>CheckAccessKeys</strong></td>
<td>Confirma que as chaves de acesso atribuídas a elementos no destino de verificação são exclusivas dentro do destino de verificação.</td>

</tr>
<tr class="odd">
<td><strong>CheckBoundingRect</strong></td>
<td>Confirma que cada elemento focado na interface do usuário tem um retângulo delimitador que pode ser usado como um destino para teste de clique.</td>

</tr>
<tr class="even">
<td rowspan="2"><strong>Árvore</strong>$ {remove} $<br />
</td>
<td><strong>CheckParentChild</strong></td>
<td>As relações pai e filho na árvore de elementos são consistentes e previsíveis.</td>
</tr>
<tr class="odd">
<td><strong>CheckOrphanChildren</strong></td>
<td>Confirma que cada elemento focado na interface do usuário relata um pai de MSAA válido.</td>

</tr>
<tr class="even">
<td rowspan="6"><strong>Propriedades UIA</strong>$ {remove} $<br />
</td>
<td><strong>CheckNameUIA</strong></td>
<td>Confirma que cada elemento focado na interface do usuário relata um nome de UIA lógico válido.</td>
</tr>
<tr class="odd">
<td><strong>CheckTreeDepthUIA</strong></td>
<td>Envia caracteres de tabulação (ou Shift + Tab) como entrada para o destino de verificação para confirmar que os elementos UIA na interface do usuário de destino não são excessivamente complexos ou inacessíveis usando a navegação de teclado padrão.</td>

</tr>
<tr class="even">
<td><strong>CheckStateUIA</strong></td>
<td>Confirma que cada elemento focado na interface do usuário relata um estado de UIA lógico válido.</td>

</tr>
<tr class="odd">
<td><strong>CheckAccessKeysUIA</strong></td>
<td>Confirma que os elementos irmãos não têm a mesma chave de acesso e/ou acelerador.</td>

</tr>
<tr class="even">
<td><strong>CheckBoundingRectUIA</strong></td>
<td>Confirma que cada elemento UIA com foco na interface do usuário tem um retângulo delimitador que pode ser usado como um destino para teste de clique.</td>

</tr>
<tr class="odd">
<td><strong>CheckControlTypeUIA</strong></td>
<td>Confirma que cada elemento focado na interface do usuário relata um tipo de controle UIA lógico válido.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Árvore UIA</strong>$ {remove} $<br />
</td>
<td><strong>CheckNavigateUia</strong></td>
<td>Confirma que o UIA TreeWalker pode navegar pelos filhos de um elemento.</td>
</tr>
<tr class="odd">
<td><strong>CheckOrphanChildrenUia</strong></td>
<td>Confirma que cada elemento focado na interface do usuário relata um pai de UIA válido.</td>

</tr>
<tr class="even">
<td><strong>CheckSiblingsUia</strong></td>
<td>Confirma que os elementos irmãos não têm o mesmo nome: pares ControlType, nem o mesmo AutomationId.</td>

</tr>
<tr class="odd">
<td>$ {ROWSPAN9} $<strong>verificações na Web do Aria</strong>$ {remover} $<br />
</td>
<td><strong>CheckARIARole</strong></td>
<td>Confirma que todos os elementos têm uma função do ARIA válida. A marca HTML associada e a função do ARIA são elementos de informações com funções inválidas sinalizadas como erros.</td>
</tr>
<tr class="even">
<td><strong>CheckLabel</strong></td>
<td>Confirma que cada elemento com entrada, botão, imagem-botão ou função de ponto de referência tem um rótulo.</td>

</tr>
<tr class="odd">
<td><strong>CheckRangeControls</strong></td>
<td>Confirma que os controles de intervalo com a função de barra deslizante ou de progresso têm atributos apropriados do ARIA definidos.</td>

</tr>
<tr class="even">
<td><strong>CheckContainerRole</strong></td>
<td>Confirma um elemento ou pelo menos um de seus filhos, tem OnKeyDown/OnKeyPress definido.</td>

</tr>
<tr class="odd">
<td><strong>CheckLayoutTable</strong></td>
<td>Confirma que um layout de tabela tem um resumo/th/Aria-DescribedBy incluído.</td>

</tr>
<tr class="even">
<td><strong>CheckGridStructure</strong></td>
<td>Confirma que um elemento que não é de tabela com a função de grade tem uma estrutura de grade>linha>gridcell com atributos associados.</td>

</tr>
<tr class="odd">
<td><strong>CheckDataTable</strong></td>
<td>Confirma as propriedades das tabelas de dados.</td>

</tr>
<tr class="even">
<td><strong>CheckActiveDescendants</strong></td>
<td>Confirma as propriedades dos elementos com um descendente ativo definido.</td>

</tr>
<tr class="odd">
<td><strong>CheckElementsWithClickHandler</strong></td>
<td>Confirma o índice de tabulação dos elementos com manipuladores de clique.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Verificações na Web</strong>$ {remove} $<br />
</td>
<td><strong>CheckHtml (Web)</strong></td>
<td>Confirma várias características de HTML, como cabeçalhos, nome, quadros e títulos.</td>
</tr>
<tr class="odd">
<td><strong>CHECKNAME (Web)</strong></td>
<td>Confirma características de nome, como comprimento, caracteres inválidos e inclusão de função.</td>

</tr>
<tr class="even">
<td><strong>CheckRole (Web)</strong></td>
<td>Confirma funções inválidas, funções que devem ter valores e/ou funções não implementadas.</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 




