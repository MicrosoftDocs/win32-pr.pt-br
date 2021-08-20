---
title: Recebendo erros para ponteiros de interface IAccessible
description: Este tópico descreve as situações em que você pode receber um erro para um ponteiro de interface do IAccessible.
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d36a29c688966526d5431e1fe2f643e39b378779d122d22f38dea2089a5191c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115137"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a>Recebendo erros para ponteiros de interface IAccessible

Este tópico descreve as situações em que você pode receber um erro para um ponteiro de interface do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . As funções **IAccessible** podem retornar erros para ponteiros de interface **IAccessible** quando um usuário fecha um aplicativo ao qual o objeto pertence, ou se um usuário ignora um controle por meio da interface do usuário.

## <a name="user-closes-an-application"></a>O usuário fecha um aplicativo

Se um usuário fechar o aplicativo que contém um objeto ao qual o ponteiro da interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) estava apontando, todas as chamadas futuras para esse objeto retornarão um código de erro. O erro, como **co \_ E \_ OBJNOTCONNECTED**, indicará que o objeto não existe mais. Isso se aplica a todos os ponteiros de interface do **IAccessible** .

## <a name="user-dismisses-a-control"></a>O usuário ignora um controle

Se um usuário ignorar um controle (por exemplo, pressionando um botão de ação), os clientes ainda poderão chamar métodos e propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nesse objeto, pois o objeto não foi liberado. No entanto, chamadas futuras receberão mensagens de erro.

Essa situação se aplica às seguintes funções e métodos:

-   [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**IAccessible:: obter \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [**IAccessible:: obter \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




