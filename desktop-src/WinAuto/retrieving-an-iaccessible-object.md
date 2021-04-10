---
title: Recuperando um objeto IAccessible
description: O Microsoft Acessibilidade Ativa fornece funções como AccessibleObjectFromWindow e AccessibleObjectFromPoint que permitem aos clientes recuperar objetos acessíveis.
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89237916597f27c7179fce9516df1e0ecf43a6db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291887"
---
# <a name="retrieving-an-iaccessible-object"></a>Recuperando um objeto IAccessible

O Microsoft Acessibilidade Ativa fornece funções como [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) e [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) que permitem aos clientes recuperar objetos acessíveis. Essas funções retornam um ponteiro de interface [**IDispatch**](idispatch-interface.md) ou [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) por meio do qual os clientes obtêm informações sobre o objeto acessível.

Quando um cliente chama [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) ou qualquer uma das outras funções **AccessibleObjectFrom * * * X* que recuperam uma interface para um objeto, o Microsoft acessibilidade ativa envia a mensagem da janela do [**WM \_ GetObject**](wm-getobject.md) para o procedimento de janela aplicável no aplicativo apropriado. Para fornecer informações aos clientes, os servidores devem responder à mensagem do **WM \_ GetObject** .

Para coletar informações específicas sobre um elemento de interface do usuário, os clientes devem primeiro recuperar uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o elemento. Para recuperar o objeto **IAccessible** de um elemento, os clientes podem usar uma das seguintes funções:

-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

**Para recuperar um ponteiro de interface IAccessible**

1.  O cliente chama uma das funções **AccessibleObjectFrom ** * * X.
2.  Oleacc.dll envia uma mensagem do [**WM \_ GetObject**](wm-getobject.md) para o servidor.
3.  O servidor determina qual elemento de interface do usuário corresponde à solicitação.
4.  O servidor retorna zero para solicitar um proxy de Oleacc.dll,

    Ou

    Retorna um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (implementação nativa). Para fazer isso, ele:

    -   Constrói um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para o elemento.
    -   Chama [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) para realizar marshaling do ponteiro do objeto.
    -   Retorna o LRESULT para Oleacc.dll.

5.  Oleacc.dll examina o valor de retorno do [**WM \_ GetObject**](wm-getobject.md).

    Se for zero, Oleacc.dll construirá um objeto proxy e o retornará ao cliente.

    Ou

    Se ele for diferente de zero, Oleacc.dll chamará [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) para desempacotar o ponteiro do objeto do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo e retorne-o para o cliente.

 

 




