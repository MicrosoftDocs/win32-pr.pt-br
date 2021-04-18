---
title: Interfaces de controles ActiveX
description: Interfaces de controles ActiveX
ms.assetid: c4ca5696-c461-4d65-b2a8-c689c056dac8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcd7c4e0b726e9f330910bd468c237c72462fa21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105810625"
---
# <a name="activex-controls-interfaces"></a><span data-ttu-id="f7e0a-103">Interfaces de controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="f7e0a-103">ActiveX Controls Interfaces</span></span>

<span data-ttu-id="f7e0a-104">Além de outros mecanismos de comunicação entre o controle e seu cliente, a tecnologia de controles ActiveX especifica as interfaces [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) e [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) para comunicação de controle de cliente.</span><span class="sxs-lookup"><span data-stu-id="f7e0a-104">In addition to other mechanisms for communicating between the control and its client, ActiveX controls technology specifies the [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) and [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) interfaces for client-control communication.</span></span> <span data-ttu-id="f7e0a-105">Também há a interface [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) para contêineres de controle simples.</span><span class="sxs-lookup"><span data-stu-id="f7e0a-105">There is also the [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) interface for simple control containers.</span></span>

<span data-ttu-id="f7e0a-106">No entanto, essas três interfaces são específicas para controles e não são geralmente úteis fora do contexto dos controles.</span><span class="sxs-lookup"><span data-stu-id="f7e0a-106">These three interfaces are, however, specific to controls and are not generally useful outside the context of controls.</span></span> <span data-ttu-id="f7e0a-107">Essas interfaces são definidas da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="f7e0a-107">These interfaces are defined as follows.</span></span>

``` syntax
interface IOleControl : IUnknown 
  { 
    HRESULT GetControlInfo([out] CONTROLINFO *pCI); 
    HRESULT OnMnemonic([in] LPMSG pMsg); 
    HRESULT OnAmbientPropertyChange([in] DISPID dispID); 
    HRESULT FreezeEvents([in] BOOL bFreeze); 
  } 
 
interface IOleControlSite : IUnknown 
  { 
    HRESULT OnControlInfoChanged(void); 
    HRESULT LockInPlaceActive([in] BOOL fLock); 
    HRESULT GetExtendedControl([out] IDispatch **ppDisp); 
    HRESULT TransformCoords([in-out] POINTL *pptlHimetric, [in-out] POINTF *pptfContainer, [in] DWORD dwFlags); 
    HRESULT TranslateAccelerator([in] LPMSG pMsg, [in] DWORD grfModifiers); 
    HRESULT OnFocus([in] BOOL fGotFocus); 
    HRESULT ShowPropertyFrame(void); 
  } 
 
interface ISimpleFrameSite : IUnknown 
  { 
    HRESULT PreMessageFilter([in] HWND hWnd, [in] UINT msg, [in] WPARAM wp, [in] LPARAM lp, 
        [out] LRESULT *plResult, [out] DWORD *pdwCookie); 
    HRESULT PostMessageFilter([in] HWND hWnd, [in] UINT msg, [in] WPARAM wp, [in] LPARAM lp, 
        [out] LRESULT *plResult, [in] DWORD dwCookie); 
  } 
 
```

<span data-ttu-id="f7e0a-108">Alguns controles, como uma caixa de grupo, são meramente um contêiner simples de outros controles.</span><span class="sxs-lookup"><span data-stu-id="f7e0a-108">Some controls, like a group box, are merely a simple container of other controls.</span></span> <span data-ttu-id="f7e0a-109">Nesses casos, o controle simples, chamado de quadro simples, não precisa implementar todos os requisitos de contêiner.</span><span class="sxs-lookup"><span data-stu-id="f7e0a-109">In such cases, the simple control, called a simple frame, doesn't have to implement all the container requirements.</span></span> <span data-ttu-id="f7e0a-110">Ele pode delegar a maioria das chamadas de interface de seus controles contidos para o contêiner que gerencia o quadro simples.</span><span class="sxs-lookup"><span data-stu-id="f7e0a-110">It can delegate most of the interface calls from its contained controls to the container that manages the simple frame.</span></span> <span data-ttu-id="f7e0a-111">Além das chamadas de interface, o quadro simples também tem de lidar com mensagens do Windows que potencialmente vêm de controles dentro dela.</span><span class="sxs-lookup"><span data-stu-id="f7e0a-111">Besides interface calls, the simple frame also has to deal with Windows messages that potentially come from controls within it.</span></span> <span data-ttu-id="f7e0a-112">Por esse motivo, um contêiner fornece [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) para permitir que esses controles de quadro simples passem mensagens até o contêiner.</span><span class="sxs-lookup"><span data-stu-id="f7e0a-112">For this reason, a container supplies [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite) to allow such simple frame controls to pass messages up to the container.</span></span> <span data-ttu-id="f7e0a-113">[**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) processa a mensagem primeiro; [**PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) é chamado depois que o quadro simples processa a própria mensagem.</span><span class="sxs-lookup"><span data-stu-id="f7e0a-113">[**PreMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-premessagefilter) processes the message first; [**PostMessageFilter**](/windows/desktop/api/OCIdl/nf-ocidl-isimpleframesite-postmessagefilter) is called after the simple frame has processed the message itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7e0a-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f7e0a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7e0a-115">Controles ActiveX</span><span class="sxs-lookup"><span data-stu-id="f7e0a-115">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




