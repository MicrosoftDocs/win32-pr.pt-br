---
title: Objeto de cliente (referência de elemento de interface do usuário do MSAA)
description: A área do cliente é a parte de uma janela em que o aplicativo exibe a saída, como texto ou elementos gráficos. Por exemplo, um aplicativo de publicação de área de trabalho exibe a página atual de um documento na área do cliente.
ms.assetid: 1b3a800e-e3c1-4737-8ad0-41707eb1e985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be28ae4c31e1a2d2f72674a39d7db08730562816
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084664"
---
# <a name="client-object-msaa-ui-element-reference"></a>Objeto de cliente (referência de elemento de interface do usuário do MSAA)

A área do cliente é a parte de uma janela em que o aplicativo exibe a saída, como texto ou elementos gráficos. Por exemplo, um aplicativo de publicação de área de trabalho exibe a página atual de um documento na área do cliente.

Os desenvolvedores de aplicativos de servidor são responsáveis por criar objetos acessíveis que fornecem informações sobre o conteúdo da área do cliente do aplicativo.

Se um aplicativo cliente solicitar informações sobre um elemento de interface do usuário personalizado dentro de um aplicativo e o elemento de interface do usuário personalizado que não oferece suporte à interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , o Microsoft acessibilidade ativa criará um objeto acessível padrão com informações mínimas.

## <a name="iaccessible-methods"></a>Métodos IAccessible

A área cliente dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades de IAccessible

A área cliente oferece suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obter \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obter \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Envia a mensagem de [**\_ gettext do WM**](/windows/desktop/winmsg/wm-gettext) para recuperar o texto da janela.                                                                                                                                                                                                                                                                                                                                                                                |
| [**obter \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obter \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A propriedade **role** é [**\_ \_ cliente do sistema de função**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                |
| [**obter \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md):[**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interface IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

