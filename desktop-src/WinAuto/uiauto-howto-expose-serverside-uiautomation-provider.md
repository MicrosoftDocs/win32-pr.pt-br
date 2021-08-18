---
title: Como expor um provedor Server-Side Automação da Interface do Usuário dados
description: Este tópico contém um código de exemplo que mostra como expor um provedor microsoft Automação da Interface do Usuário do lado do servidor para um controle personalizado.
ms.assetid: 68bf16c7-fbab-478a-97be-47d1195028f3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 771e81a058af16320673e46a7981cf49ee22105fa841807bc07e3a528ff223cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133309"
---
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a>Como expor um provedor Server-Side Automação da Interface do Usuário dados

Este tópico contém um código de exemplo que mostra como expor um provedor microsoft Automação da Interface do Usuário do lado do servidor para um controle personalizado.

O Microsoft Automação da Interface do Usuário envia a [**mensagem WM \_ GETOBJECT**](wm-getobject.md) a um aplicativo de provedor para recuperar informações sobre um objeto acessível com suporte pelo provedor. Automação da Interface do Usuário envia **WM \_ GETOBJECT** quando um cliente chama [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)e [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)e ao manipular eventos para os quais o cliente se registrou.

Quando um provedor recebe uma mensagem [**WM \_ GETOBJECT,**](wm-getobject.md) ele deve verificar se o parâmetro *lParam* é igual a **UiaRootObjectId**. Se for, o provedor deverá retornar a interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) do objeto . O provedor retorna a interface chamando a [**função UiaReturnRawElementProvider.**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider)

O exemplo a seguir demonstra como responder ao [**WM \_ GETOBJECT.**](wm-getobject.md)


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

**Conceitual**
</dt> <dt>

[Implementando um provedor Server-Side Automação da Interface do Usuário dados](uiauto-serversideprovider.md)
</dt> <dt>

[A mensagem \_ WM GETOBJECT](the-wm-getobject-message.md)
</dt> <dt>

[Tópicos de ida e Automação da Interface do Usuário provedores](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




