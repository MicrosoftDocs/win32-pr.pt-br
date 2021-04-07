---
description: Retorno de chamada para solicitar um destino de renderização.
MS-HAID: vspixengine.IFrameBufferRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IFrameBufferRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 74497395-9956-430A-AB75-F1FD2FC4E66E
api_name:
- IFrameBufferRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 443f81cb227d76329814131acee163e1a947de8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825818"
---
# <a name="span-idvspixengineiframebufferrequestspaniframebufferrequest-interface"></a><span data-ttu-id="6898a-103"><span id="vspixengine.iframebufferrequest"></span>Interface IFrameBufferRequest</span><span class="sxs-lookup"><span data-stu-id="6898a-103"><span id="vspixengine.iframebufferrequest"></span>IFrameBufferRequest interface</span></span>

<span data-ttu-id="6898a-104">Retorno de chamada para solicitar um destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="6898a-104">Callback to request a render target.</span></span>

## <a name="members"></a><span data-ttu-id="6898a-105">Membros</span><span class="sxs-lookup"><span data-stu-id="6898a-105">Members</span></span>

<span data-ttu-id="6898a-106">A interface **IFrameBufferRequest** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6898a-106">The **IFrameBufferRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6898a-107">**IFrameBufferRequest** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6898a-107">**IFrameBufferRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="6898a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6898a-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="6898a-109"><span id="methods"></span>Maneiras</span><span class="sxs-lookup"><span data-stu-id="6898a-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="6898a-110">A interface **IFrameBufferRequest** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6898a-110">The **IFrameBufferRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="6898a-111">Método</span><span class="sxs-lookup"><span data-stu-id="6898a-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="6898a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6898a-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="6898a-113"><a href="/windows/desktop/direct3dtools/iframebufferrequest-requestasync-dword-eventid-dword-iframebuffercallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="6898a-113"><a href="/windows/desktop/direct3dtools/iframebufferrequest-requestasync-dword-eventid-dword-iframebuffercallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="6898a-114">Solicita a saída framebuffer do destino de renderização, evento e quadro especificados.</span><span class="sxs-lookup"><span data-stu-id="6898a-114">Requests framebuffer output of the specified render target, event, and frame.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="6898a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6898a-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6898a-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6898a-116">Header</span></span></p></td><td><span data-ttu-id="6898a-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6898a-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
