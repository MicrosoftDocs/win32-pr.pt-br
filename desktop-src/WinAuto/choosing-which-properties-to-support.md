---
title: Escolhendo quais propriedades para dar suporte
description: As propriedades IAccessible fornecem uma maneira para os desenvolvedores de servidor descreverem uma grande variedade de elementos da interface do usuário.
ms.assetid: c51fd8a1-dc23-4d64-8921-e0a795c3ffb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c88a808889403f88d414f7ad950b3e431c00e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292419"
---
# <a name="choosing-which-properties-to-support"></a>Escolhendo quais propriedades para dar suporte

As propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fornecem uma maneira para os desenvolvedores de servidor descreverem uma grande variedade de elementos da interface do usuário. Mas nem todas as propriedades são aplicáveis a todos os tipos de elemento de interface do usuário. Além disso, algumas propriedades fornecem informações descritivas que são úteis, mas não essenciais.

Os servidores devem dar suporte às seguintes propriedades e métodos para cada objeto:

-   [**Nome**](name-property.md)
-   [**Role**](role-property.md)
-   [**Status**](state-property.md)
-   [**Localização**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) e [ **IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**Pai**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) e [ **IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

As propriedades e o método a seguir devem ter suporte se forem aplicáveis ao objeto:

-   [**KeyboardShortcut**](keyboardshortcut-property.md)
-   [**Valor**](value-property.md)

As propriedades e o método a seguir devem ter suporte se o objeto tiver filhos:

-   [**Filho**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) e [ **ChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)
-   [**Foco, seleção**](selection-and-focus-properties-and-methods.md)e [ **IAccessible:: accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

As propriedades a seguir são opcionais, mas fornecem informações descritivas úteis sobre o objeto. A propriedade [**Description**](description-property.md) é implementada para descrever bitmaps e outras imagens.

-   [**Descrição**](description-property.md)
-   [**DefaultAction**](defaultaction-property.md) e [ **IAccessible:: accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction)
-   [**Ajuda**](help-property.md)
-   [**HelpTopic**](helptopic-property.md)

 

 




