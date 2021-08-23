---
title: Objeto Client (Referência de elemento de interface do usuário MSAA)
description: A área de cliente é a parte de uma janela em que o aplicativo exibe a saída, como texto ou gráficos. Por exemplo, um aplicativo de publicação da área de trabalho exibe a página atual de um documento na área de cliente.
ms.assetid: 1b3a800e-e3c1-4737-8ad0-41707eb1e985
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f33190ebd1013c92a58ecc64b07993a5a5ae1cd842e50c88691295114a128074
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119645056"
---
# <a name="client-object-msaa-ui-element-reference"></a>Objeto Client (Referência de elemento de interface do usuário MSAA)

A área de cliente é a parte de uma janela em que o aplicativo exibe a saída, como texto ou gráficos. Por exemplo, um aplicativo de publicação da área de trabalho exibe a página atual de um documento na área de cliente.

Os desenvolvedores de aplicativos de servidor são responsáveis por criar objetos acessíveis que fornecem informações sobre o conteúdo da área de cliente do aplicativo.

Se um aplicativo cliente solicitar informações sobre um elemento de interface do usuário personalizado dentro de um aplicativo e o elemento de interface do usuário personalizado que não dá suporte à interface [**IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o Microsoft Active Accessibility criará um objeto acessível padrão com informações mínimas.

## <a name="iaccessible-methods"></a>Métodos IAccessible

A área de cliente dá suporte aos seguintes métodos [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**Acchittest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Acclocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**Accnavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**Accselect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propriedades IAccessible

A área de cliente dá suporte às seguintes [**propriedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propriedade                                                                             | Comentários                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | Envia a [**mensagem WM \_ GETTEXT**](/windows/desktop/winmsg/wm-gettext) para recuperar o texto da janela.                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | A **propriedade Role** é ROLE SYSTEM [**\_ \_ CLIENT.**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | A **propriedade State** é uma combinação de um ou mais dos seguintes valores: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE [](object-state-constants.md)SYSTEM UNAVAILABLE STATE SYSTEM FOCUSED STATE SYSTEM \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IAccessible Interface](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

