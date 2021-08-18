---
title: Escolhendo quais propriedades dar suporte
description: As propriedades do IAccessible fornecem uma maneira para os desenvolvedores de servidor descreverem uma ampla variedade de elementos de interface do usuário.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a3c9ef5d56c6d963a05ac84b5e2cacafde488c377ebcc73fa1e2c4be1adab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133959"
---
# <a name="choosing-which-properties-to-support"></a>Escolhendo quais propriedades dar suporte

As [**propriedades do IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fornecem uma maneira para os desenvolvedores de servidor descreverem uma ampla variedade de elementos de interface do usuário. Mas nem todas as propriedades são aplicáveis a cada tipo de elemento de interface do usuário. Além disso, algumas propriedades fornecem informações descritivas úteis, mas não essenciais.

Os servidores devem dar suporte às seguintes propriedades e métodos para cada objeto:

-   [**Nome**](name-property.md)
-   [**Role**](role-property.md)
-   [**Estado**](state-property.md)
-   [**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) e [ **IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Parent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) e [ **IAccessible::accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

As propriedades e o método a seguir devem ter suporte se elas são aplicáveis ao objeto :

-   [**KeyboardShortcut**](keyboardshortcut-property.md)
-   [**Valor**](value-property.md)

As seguintes propriedades e método deverão ser suportados se o objeto tiver filhos:

-   [**Child**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) e [ **ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**Foco, Seleção**](selection-and-focus-properties-and-methods.md)e [ **IAccessible::accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

As propriedades a seguir são opcionais, mas fornecem informações descritivas úteis sobre o objeto . A [**propriedade Description**](description-property.md) é implementada para descrever bitmaps e outras imagens.

-   [**Descrição**](description-property.md)
-   [**DefaultAction**](defaultaction-property.md) e [ **IAccessible::accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**Ajuda**](help-property.md)
-   [**Helptopic**](helptopic-property.md)

 

 




