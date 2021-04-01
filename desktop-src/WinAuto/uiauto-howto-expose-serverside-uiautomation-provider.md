---
title: Como expor um provedor de automação de interface do usuário Server-Side
description: Este tópico contém um código de exemplo que mostra como expor um provedor de automação de interface do usuário da Microsoft do lado do servidor para um controle personalizado.
ms.assetid: 68bf16c7-fbab-478a-97be-47d1195028f3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5af3fa9e663bc737df95015db94cdedc1073ab9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160023"
---
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a>Como expor um provedor de automação de interface do usuário Server-Side

Este tópico contém um código de exemplo que mostra como expor um provedor de automação de interface do usuário da Microsoft do lado do servidor para um controle personalizado.

A automação da interface do usuário da Microsoft envia a mensagem do [**WM \_ GetObject**](wm-getobject.md) para um aplicativo de provedor para recuperar informações sobre um objeto acessível com suporte pelo provedor. A automação da interface do usuário envia o **WM \_ GetObject** quando um cliente chama [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)e [**getconcentrouelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)e ao manipular eventos para os quais o cliente registrou.

Quando um provedor recebe uma mensagem do [**WM \_ GetObject**](wm-getobject.md) , ele deve verificar se o parâmetro *lParam* é igual a **UiaRootObjectId**. Se for, o provedor deverá retornar a interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) do objeto. O provedor retorna a interface chamando a função [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .

O exemplo a seguir demonstra como responder ao [**WM \_ GetObject**](wm-getobject.md).


```C++
    // Expose the custom button's server-side provider to UI Automation.
    case WM_GETOBJECT:
        {
            // If lParam matches UiaRootObjectId, return IRawElementProviderSimple.
            if (static_cast<long>(lParam) == static_cast<long>(UiaRootObjectId))
            {
                // Retrieve the pointer to the custom button object from the
                // window data.
                CustomButton* pControl = reinterpret_cast<CustomButton*>(
                    GetWindowLongPtr(hwnd, GWLP_USERDATA));

                // Call an application-defined method to get the
                // IRawElementProviderSimple pointer.
                IRawElementProviderSimple* pRootProvider = 
                    pControl->GetUIAutomationProvider(hwnd);

                // Return the IRawElementProviderSimple pointer to UI Automation.
                return UiaReturnRawElementProvider(hwnd, wParam, lParam, 
                    pRootProvider);
            }
            return 0;
        }
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Implementando um provedor de automação de interface do usuário Server-Side](uiauto-serversideprovider.md)
</dt> <dt>

[A mensagem do WM \_ GETobject](the-wm-getobject-message.md)
</dt> <dt>

[Tópicos de instruções para provedores de automação de interface do usuário](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




