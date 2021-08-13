---
title: Janela do cliente MDI (referência de elemento da interface do usuário do MSAA)
description: A interface de vários documentos (MDI) é uma especificação que define a interface do usuário padrão para aplicativos escritos para Windows. Um aplicativo MDI permite que um usuário trabalhe com mais de um documento por vez.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cff8279e9934c953e30a7d91710565562cb538d3140d971b1f74ff8963ca7345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565127"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a>Janela do cliente MDI (referência de elemento da interface do usuário do MSAA)

A interface de vários documentos (MDI) é uma especificação que define a interface do usuário padrão para aplicativos escritos para Windows. Um aplicativo MDI permite que um usuário trabalhe com mais de um documento por vez.

Um aplicativo MDI tem três tipos de janelas: uma janela de quadro, uma janela de cliente e uma série de janelas filhas. A janela do quadro é como a janela principal de um aplicativo e envolve a janela do cliente. A janela do cliente é um filho da janela do quadro e serve como o plano de fundo para as janelas filhas. A janela do cliente também fornece suporte para criar e manipular as janelas filhas nas quais os documentos são exibidos.

O nome da classe de janela para uma janela de cliente MDI é "MDIClient".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Uma janela de cliente MDI dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

Uma janela do cliente MDI dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                 | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | A propriedade **ChildCount** é o número de janelas filhas nas quais os documentos são exibidos.                                                                                                                                                                                                                                                                                                                                                                              |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | A propriedade **Name** é "Workspace".                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | A propriedade **Parent** é a janela de quadro MDI.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | A propriedade **role** é [**\_ \_ cliente do sistema de função**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obter \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md): [**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





