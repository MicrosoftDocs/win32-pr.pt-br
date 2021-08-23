---
title: Comunicação de cliente/servidor
description: O mecanismo WinEvents fornece uma maneira para os servidores se comunicarem facilmente com Microsoft Active Accessibility clientes.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896b6f6688e0e2929ebb351fe9d7cc210803768a8031faa44a8aca8127b12002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133929"
---
# <a name="clientserver-communication"></a>Comunicação de cliente/servidor

O [mecanismo WinEvents](winevents-overview.md) fornece uma maneira para os servidores se comunicarem facilmente com Microsoft Active Accessibility clientes. Os clientes geralmente coletam informações reagindo a WinEvents (por exemplo, o foco a seguir), mas eles são livres para solicitar informações de um servidor a qualquer momento.

Para solicitar informações para um objeto acessível que gera um WinEvent, um cliente deve processar o evento e estabelecer uma conexão com o objeto acessível relevante. Para fazer isso, o cliente executa as seis etapas a seguir:

-   Um servidor chama [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para gerar uma notificação winEvent para cada alteração em seus elementos de interface do usuário.
-   O código de gerenciamento winEvent em USER determina se qualquer aplicativo cliente registrou uma função de [*gancho*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) WinEvent usando [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) e chama a função de retorno de chamada registrada.
-   Em sua função de retorno de chamada, o cliente solicita acesso ao objeto que gerou o evento chamando [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) ou outras funções de recuperação de objeto acessíveis. Para obter mais informações, [consulte Recuperando um objeto IAccessible](retrieving-an-iaccessible-object.md).
-   Essa Microsoft Active Accessibility API envia ao aplicativo de servidor [**uma mensagem WM \_ GETOBJECT**](wm-getobject.md) para recuperar o objeto acessível.
-   Em resposta ao [**WM \_ GETOBJECT**](wm-getobject.md), o aplicativo de servidor retorna zero ou retorna um valor que atua como uma referência única ao objeto que gerou o evento.
-   Se o servidor retornar zero, Microsoft Active Accessibility criará um objeto proxy e dará seu endereço ao cliente. Caso contrário, Microsoft Active Accessibility usa essa referência para recuperar o endereço de uma interface de objeto como [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ou [**IDispatch**](idispatch-interface.md)e fornece esse endereço ao cliente.

Depois que o cliente tiver um endereço de interface, ele poderá chamar as propriedades e os métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do objeto acessível para recuperar informações.

## <a name="in-this-section"></a>Nesta seção

-   [WinEvents e Acessibilidade Ativa](winevents-overview.md)
-   [Como o WM \_ GETOBJECT funciona](how-wm-getobject-works.md)
-   [Recuperando um objeto IAccessible](retrieving-an-iaccessible-object.md)

 

 




