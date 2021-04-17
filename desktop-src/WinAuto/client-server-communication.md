---
title: Comunicação de cliente/servidor
description: O mecanismo WinEvents fornece uma maneira para que os servidores se comuniquem facilmente com os clientes do Microsoft Acessibilidade Ativa.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95b29170d5a903493977af130ef6d48bb3b896b6
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "105813624"
---
# <a name="clientserver-communication"></a>Comunicação de cliente/servidor

O mecanismo [WinEvents](winevents-overview.md) fornece uma maneira para que os servidores se comuniquem facilmente com os clientes do Microsoft acessibilidade ativa. Os clientes geralmente coletam informações reagindo ao WinEvents (por exemplo, o foco seguinte), mas são livres para solicitar informações de um servidor a qualquer momento.

Para solicitar informações para um objeto acessível que gera um WinEvent, um cliente deve processar o evento e estabelecer uma conexão com o objeto acessível relevante. Para fazer isso, o cliente executa as seis etapas a seguir:

-   Um servidor chama [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para gerar uma notificação WinEvent para cada alteração em seus elementos de interface do usuário.
-   O código de gerenciamento WinEvent no usuário determina se algum aplicativo cliente registrou uma [*função de Hook*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) WinEvent usando [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) e chama a função de retorno de chamada registrada.
-   Em sua função de retorno de chamada, o cliente solicita acesso ao objeto que gerou o evento chamando [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) ou outras funções de recuperação de objeto acessíveis. Para obter mais informações, consulte [recuperando um objeto IAccessible](retrieving-an-iaccessible-object.md).
-   Essa API do Microsoft Acessibilidade Ativa envia ao aplicativo de servidor uma mensagem do [**WM \_ GetObject**](wm-getobject.md) para recuperar o objeto acessível.
-   Em resposta ao [**WM \_ GetObject**](wm-getobject.md), o aplicativo de servidor retorna zero ou retorna um valor que atua como uma referência única para o objeto que gerou o evento.
-   Se o servidor retornar zero, o Microsoft Acessibilidade Ativa criará um objeto proxy e fornecerá seu endereço ao cliente. Caso contrário, o Microsoft Acessibilidade Ativa usa essa referência para recuperar o endereço de uma interface de objeto, como [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ou [**IDispatch**](idispatch-interface.md), e fornece esse endereço ao cliente.

Depois que o cliente tem um endereço de interface, ele pode chamar as propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e os métodos do objeto acessível para recuperar informações.

## <a name="in-this-section"></a>Nesta seção

-   [WinEvents e Acessibilidade Ativa](winevents-overview.md)
-   [Como o WM \_ GetObject funciona](how-wm-getobject-works.md)
-   [Recuperando um objeto IAccessible](retrieving-an-iaccessible-object.md)

 

 




