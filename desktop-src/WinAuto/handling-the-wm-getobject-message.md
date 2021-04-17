---
title: Manipulando a mensagem de WM_GETOBJECT
description: O Microsoft Acessibilidade Ativa e a automação da interface do usuário da Microsoft enviam a mensagem do WM \_ GetObject para um aplicativo de servidor ou provedor para recuperar informações sobre um objeto acessível com suporte no servidor ou provedor.
ms.assetid: 4b8e551f-aba7-4a89-8874-ba690175f525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 695fad8f050606f0a95a1780551d35499e39d166
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105780309"
---
# <a name="handling-the-wm_getobject-message"></a>Manipulando a \_ mensagem do WM GETobject

O Microsoft Acessibilidade Ativa e a automação da interface do usuário da Microsoft enviam a mensagem do [**WM \_ GetObject**](wm-getobject.md) para um aplicativo de servidor ou provedor para recuperar informações sobre um objeto acessível com suporte no servidor ou provedor. Os clientes nunca enviam o **WM \_ GetObject** diretamente. Em vez disso, o Microsoft Acessibilidade Ativa envia essa mensagem quando um cliente chama as funções [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint), [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)e [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) . A automação da interface do usuário envia o **WM \_ GetObject** quando um cliente chama [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)e [**getconcentrouelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)e ao manipular eventos para os quais o cliente registrou.

O Microsoft Acessibilidade Ativa ou a automação da interface do usuário especifica o tipo de objeto do qual precisa de informações, passando um valor chamado *identificador de objeto* com a mensagem do [**WM \_ GetObject**](wm-getobject.md) . Quando ele recebe a mensagem, o servidor ou o provedor examina o identificador de objeto para determinar como responder à mensagem. A resposta depende de se o aplicativo receptor implementa o Microsoft Acessibilidade Ativa (um servidor), a automação da interface do usuário (um provedor) ou nenhum deles para o objeto especificado.

-   Se o aplicativo de recebimento for um Microsoft Acessibilidade Ativa Server e a mensagem do [**WM \_ GetObject**](wm-getobject.md) incluir um identificador de objeto do [**\_ cliente OBJID**](object-identifiers.md), o servidor deverá retornar o valor obtido passando a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) do objeto para a função [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .
-   Se o aplicativo de recebimento for o provedor de automação aUI e o identificador de objeto for **UiaRootObjectId**, o provedor deverá retornar a interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) do objeto. O provedor Obtém a interface chamando a função [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .
-   Se o aplicativo receptor não implementar o Microsoft Acessibilidade Ativa nem a automação da interface do usuário, ele deverá passar a mensagem do [**WM \_ GetObject**](wm-getobject.md) para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Passar a mensagem permite que a estrutura de acessibilidade determine se um proxy está disponível para o objeto especificado.
-   Se o identificador de objeto não [**for \_ cliente OBJID**](object-identifiers.md) nem UiaRootObjectId, o aplicativo de recebimento deverá passar a mensagem do [**WM \_ GetObject**](wm-getobject.md) para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Passar a mensagem permite que a estrutura de acessibilidade use os provedores padrão para elementos da interface do usuário padrão.

A Microsoft Acessibilidade Ativa e a automação da interface do usuário podem passar identificadores de objeto personalizados em uma mensagem do [**WM \_ GetObject**](wm-getobject.md) para recuperar valores ou objetos definidos pelo aplicativo de um servidor ou provedor. O identificador de objeto [**OBJID \_ NATIVEOM**](object-identifiers.md) ou [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) pode ser usado para recuperar uma interface de modelo de objeto nativo ou para solicitar um objeto proxy específico com suporte pelo Oleacc.dll.

Ao manipular o [**\_ cliente OBJID**](object-identifiers.md) e os identificadores de objeto **UiaRootObjectId** , uma implementação do Microsoft acessibilidade ativa Server pode coexistir junto com uma implementação do provedor de automação da interface do usuário. Como a maioria dos controles padrão do Windows e os controles comuns implementados pela biblioteca de controle comum (ComCtl32.dll) não implementam o Microsoft Acessibilidade Ativa ou a automação da interface do usuário, normalmente esses controles não manipulam a mensagem do [**WM \_ GetObject**](wm-getobject.md) . Em vez disso, o Microsoft Acessibilidade Ativa ou a estrutura de automação de interface do usuário verifica se um objeto proxy está disponível para um determinado elemento de interface do usuário. Caso contrário, ele fornece o objeto proxy padrão para o objeto de janela do host.

 

 