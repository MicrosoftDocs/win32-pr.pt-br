---
title: Barra de título (referência de elemento da interface do usuário do MSAA)
description: A barra de título na parte superior de uma janela exibe um ícone e uma linha de texto definidos pelo aplicativo.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9183e4c4f5364fb45ba2a73dd2d40509c03c7838bbb248e1d95765b675f50cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993996"
---
# <a name="title-bar-msaa-ui-element-reference"></a>Barra de título (referência de elemento da interface do usuário do MSAA)

> [!Note]  
> Este tópico descreve objetos da **barra de título** para fins de referência de elemento da interface do usuário do MSAA. Como criar objetos de **barra de título** em várias estruturas de interface do usuário não é descrito aqui. Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.

 

A barra de título na parte superior de uma janela exibe um ícone e uma linha de texto definidos pelo aplicativo. O texto especifica o nome do aplicativo e indica a finalidade da janela. A barra de título também torna possível que o usuário mova a janela usando um mouse ou outro dispositivo apontador.

As barras de título contêm pelo menos três botões pequenos que minimizam, maximizam ou restauram e fecham a janela associada à barra de título. As barras de título também contêm um botão de ajuda contextual. os aplicativos executados na versão Far-East do sistema operacional Windows também podem conter botões do ime (Editor de método de entrada). O Microsoft Acessibilidade Ativa expõe esses botões como elementos filho da barra de título.

## <a name="iaccessible-methods"></a>Métodos IAccessible

As barras de título dão suporte aos seguintes métodos de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

As barras de título dão suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>Comentários</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></td>
<td>A propriedade <strong>ChildCount</strong> é cinco. A propriedade <strong>ChildCount</strong> inclui o IME e botões de ajuda sensíveis ao contexto, mesmo quando eles não são exibidos. Os botões que não são exibidos têm a propriedade <strong>State</strong> <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</td>
</tr>
<tr class="even">
<td><strong>get_accDescription</strong></td>
<td>A propriedade <strong>Description</strong> da própria barra de título é: &quot; exibe o nome da janela e contém controles para manipulá-la. &quot; Os botões filho na barra de título têm as seguintes descrições:<br/>
<ul>
<li>&quot;Move a janela para fora de</li>
<li>&quot;Torna a janela completa</li>
<li>&quot;Coloca um minimizado ou um</li>
<li>&quot;Fecha a janela&quot;</li>
<li>&quot;Entra ou sai do contexto-</li>
<li>&quot;Abre o teclado quando pressionado&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>get_accName</strong></td>
<td>A barra de título em si não oferece suporte à propriedade <strong>Name</strong> . Os botões filho na barra de título têm os seguintes nomes:
<ul>
<li>&quot;Minimizar&quot;</li>
<li>&quot;Maximizar &quot; ou &quot; restaurar &quot; ,</li>
<li>&quot;Fechar&quot;</li>
<li>&quot;Ajuda de contexto&quot;</li>
<li>&quot;IME&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>get_accParent</strong></td>
<td>A propriedade <strong>Parent</strong> da barra de título é a janela principal do aplicativo ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) que tem o mesmo nome de classe da janela definida pelo aplicativo que a barra de título.</td>
</tr>
<tr class="odd">
<td><strong>get_accRole</strong></td>
<td>A propriedade de <strong>função</strong> é <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>. Os botões filho na barra de título têm a <strong></strong> propriedade Role <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</td>
</tr>
<tr class="even">
<td><strong>get_accState</strong></td>
<td>A propriedade <strong>State</strong> para a barra de título e os botões filho pode ser uma combinação de um ou mais dos seguintes <a href="object-state-constants.md">valores</a>: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a><br/></td>
</tr>
<tr class="odd">
<td><strong>get_accValue</strong></td>
<td>A propriedade <strong>Value</strong> é uma cadeia de caracteres que é igual ao texto exibido na barra de título.</td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a>Observações

-   Embora a barra de título de um aplicativo tenha o estado de sinalizador de propriedade de **estado** , o sistema de estado do **sinalizador de** estado não [**tem foco. \_ \_**](object-state-constants.md) [**\_ \_**](object-state-constants.md) Definir o foco para um objeto de barra de título enfoca a janela do aplicativo.
-   Como o objeto da barra de título não dá suporte a [**Get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), os botões na barra de título são elementos simples. Eles não oferecem suporte à própria interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . O objeto da barra de título fornece informações sobre esses botões filho.
-   Como as barras de título não têm foco e não têm nenhuma ação padrão, os métodos [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) e [**Get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) não têm suporte para esse controle.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





