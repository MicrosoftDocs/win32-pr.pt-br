---
title: Alternar janela (referência de elemento de interface do usuário do MSAA)
description: A janela comutador é exibida sempre que um usuário pressiona ALT + TAB para alternar para um aplicativo diferente. A janela switch contém um ícone para cada aplicativo em execução no momento.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eead618e23f8a56c90b37eae2386f16a90f6dd67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637111"
---
# <a name="switch-window-msaa-ui-element-reference"></a>Alternar janela (referência de elemento de interface do usuário do MSAA)

A janela comutador é exibida sempre que um usuário pressiona ALT + TAB para alternar para um aplicativo diferente. A janela switch contém um ícone para cada aplicativo em execução no momento.

O nome da classe de janela da janela de comutador é " \# 32771".

## <a name="iaccessible-methods"></a>Métodos IAccessible

A janela switch dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Método                                                                    | Comentários                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | O objeto de janela de opção em si não tem uma propriedade **DefaultAction** . O método [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) para cada item na janela de comutador ativa o item especificado. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

A janela switch dá suporte às seguintes propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



|                                                                                |                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | A propriedade **ChildCount** é zero.                                                                                                                                                                                           |
| [**obter \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | O objeto de janela de opção em si não tem uma propriedade **DefaultAction** . A propriedade **DefaultAction** para cada item na janela switch é "switch".                                                                     |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | O objeto pai da janela de comutador não pode receber o foco; somente os filhos individuais podem receber o foco.                                                                                                                          |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | O objeto de janela de opção em si não tem uma propriedade **Name** . A propriedade **Name** para cada ícone de aplicativo na janela switch é igual ao nome do aplicativo exibido.                                         |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | O próprio objeto Window do switch tem uma propriedade **role** de "Window \[ 32771 \] ". Além disso, cada ícone de aplicativo na **janela de comutador tem a função** de Propriedade do [**\_ sistema \_ ListItem**](object-roles.md). |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | O objeto de janela de switch em si não oferece suporte à propriedade **State** . O valor de **estado** para os itens de exibição de lista é de [**estado do \_ sistema \_**](object-state-constants.md).                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




