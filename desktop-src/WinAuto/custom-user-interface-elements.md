---
title: Elementos personalizados da interface do usuário
description: Os desenvolvedores de servidor criam objetos acessíveis com base na interface do usuário de um aplicativo.
ms.assetid: d9453fb0-9b4a-4103-81e3-1255091255a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b32a086b977a1737a17206261aaaa94faa754d93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822384"
---
# <a name="custom-user-interface-elements"></a>Elementos personalizados da interface do usuário

Os desenvolvedores de servidor criam objetos acessíveis com base na interface do usuário de um aplicativo. Como [acessibilidade ativa implementa a interface IAccessible em nome dos elementos da interface do usuário fornecidos pelo sistema](appendix-a--supported-user-interface-elements-reference.md) , como caixas de listagem, menus e controles TrackBar, você precisa implementar a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) somente para os seguintes tipos de elementos personalizados da interface do usuário:

-   Controles personalizados criados pelo registro de uma classe de janela definida pelo aplicativo
-   Controles personalizados desenhados diretamente na tela que não têm um **HWND** associado
-   Controles personalizados, como Microsoft ActiveX e controles Java
-   Controles ou objetos na janela do cliente do aplicativo que ainda não estão expostos

Os controles e menus desenhados pelo proprietário estarão acessíveis contanto que você siga as diretrizes discutidas em [atalhos para expor elementos personalizados da interface do usuário](shortcuts-for-exposing-custom-user-interface-elements.md). Se você seguir essas diretrizes, não precisará implementar a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para controles e menus desenhados pelo proprietário.

Na maioria dos casos, os controles de subclasse e de subclasse são acessíveis porque o sistema manipula a funcionalidade básica do controle. No entanto, se um controle de subclasse ou de subclasse modificar significativamente o comportamento do controle fornecido pelo sistema no qual ele se baseia, você deverá implementar a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Para obter mais informações, consulte [expondo controles com base em controles do sistema](exposing-controls-based-on-system-controls.md).

Se um aplicativo usar apenas elementos de interface do usuário fornecidos pelo sistema, ele não precisará implementar o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), exceto a janela do cliente. Por exemplo, um aplicativo que inclui um editor de texto, não implementado usando um controle de edição, expõe linhas de texto como objetos acessíveis. Observe que o Microsoft Acessibilidade Ativa expõe automaticamente o texto em controles Edit e Rich Edit como uma única cadeia de texto na propriedade [**Value**](value-property.md) do controle.

 

 




