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
# <a name="how-to-expose-a-server-side-ui-automation-provider"></a><span data-ttu-id="5494a-103">Como expor um provedor de automação de interface do usuário Server-Side</span><span class="sxs-lookup"><span data-stu-id="5494a-103">How to Expose a Server-Side UI Automation Provider</span></span>

<span data-ttu-id="5494a-104">Este tópico contém um código de exemplo que mostra como expor um provedor de automação de interface do usuário da Microsoft do lado do servidor para um controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="5494a-104">This topic contains example code that shows how to expose a server-side Microsoft UI Automation provider for a custom control.</span></span>

<span data-ttu-id="5494a-105">A automação da interface do usuário da Microsoft envia a mensagem do [**WM \_ GetObject**](wm-getobject.md) para um aplicativo de provedor para recuperar informações sobre um objeto acessível com suporte pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="5494a-105">Microsoft UI Automation sends the [**WM\_GETOBJECT**](wm-getobject.md) message to a provider application to retrieve information about an accessible object supported by the provider.</span></span> <span data-ttu-id="5494a-106">A automação da interface do usuário envia o **WM \_ GetObject** quando um cliente chama [**IUIAutomation:: ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)e [**getconcentrouelement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement)e ao manipular eventos para os quais o cliente registrou.</span><span class="sxs-lookup"><span data-stu-id="5494a-106">UI Automation sends **WM\_GETOBJECT** when a client calls [**IUIAutomation::ElementFromHandle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfromhandle), [**ElementFromPoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint), and [**GetFocusedElement**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-getfocusedelement), and when handling events for which the client has registered.</span></span>

<span data-ttu-id="5494a-107">Quando um provedor recebe uma mensagem do [**WM \_ GetObject**](wm-getobject.md) , ele deve verificar se o parâmetro *lParam* é igual a **UiaRootObjectId**.</span><span class="sxs-lookup"><span data-stu-id="5494a-107">When a provider receives a [**WM\_GETOBJECT**](wm-getobject.md) message, it should check whether the *lParam* parameter is equal to **UiaRootObjectId**.</span></span> <span data-ttu-id="5494a-108">Se for, o provedor deverá retornar a interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) do objeto.</span><span class="sxs-lookup"><span data-stu-id="5494a-108">If it is, the provider should return the [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) interface of the object.</span></span> <span data-ttu-id="5494a-109">O provedor retorna a interface chamando a função [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) .</span><span class="sxs-lookup"><span data-stu-id="5494a-109">The provider returns the interface by calling the [**UiaReturnRawElementProvider**](/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-uiareturnrawelementprovider) function.</span></span>

<span data-ttu-id="5494a-110">O exemplo a seguir demonstra como responder ao [**WM \_ GetObject**](wm-getobject.md).</span><span class="sxs-lookup"><span data-stu-id="5494a-110">The following example demonstrates shows how to respond to [**WM\_GETOBJECT**](wm-getobject.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5494a-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5494a-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5494a-112">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="5494a-112">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5494a-113">Implementando um provedor de automação de interface do usuário Server-Side</span><span class="sxs-lookup"><span data-stu-id="5494a-113">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="5494a-114">A mensagem do WM \_ GETobject</span><span class="sxs-lookup"><span data-stu-id="5494a-114">The WM\_GETOBJECT Message</span></span>](the-wm-getobject-message.md)
</dt> <dt>

[<span data-ttu-id="5494a-115">Tópicos de instruções para provedores de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="5494a-115">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




