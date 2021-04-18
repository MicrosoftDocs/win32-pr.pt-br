---
description: Códigos de status que podem ser retornados por funções DXGI.
ms.assetid: dd7480b4-8218-4716-ab9f-74a9955b8aa7
title: DXGI_STATUS (DXGI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c402880ccdcbda009402d56127e70a61543d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765611"
---
# <a name="dxgi_status"></a><span data-ttu-id="06657-103">STATUS de DXGI \_</span><span class="sxs-lookup"><span data-stu-id="06657-103">DXGI\_STATUS</span></span>

<span data-ttu-id="06657-104">Códigos de status que podem ser retornados por funções DXGI.</span><span class="sxs-lookup"><span data-stu-id="06657-104">Status codes that can be returned by DXGI functions.</span></span>



| <span data-ttu-id="06657-105">Constante/valor</span><span class="sxs-lookup"><span data-stu-id="06657-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="06657-106">Description</span><span class="sxs-lookup"><span data-stu-id="06657-106">Description</span></span>                                                                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_STATUS_OCCLUDED"></span><span id="dxgi_status_occluded"></span><dl> <span data-ttu-id="06657-107"><dt>**Dxgi \_ STATUS \_ obstruído**</dt> <dt>0x087A0001</dt></span><span class="sxs-lookup"><span data-stu-id="06657-107"><dt>**DXGI\_STATUS\_OCCLUDED**</dt> <dt>0x087A0001</dt></span></span> </dl>                                                 | <span data-ttu-id="06657-108">O conteúdo da janela não está visível.</span><span class="sxs-lookup"><span data-stu-id="06657-108">The window content is not visible.</span></span> <span data-ttu-id="06657-109">Ao receber esse status, um aplicativo pode parar de renderizar e usar o \_ \_ teste de presente em dxgi para determinar quando retomar a renderização.</span><span class="sxs-lookup"><span data-stu-id="06657-109">When receiving this status, an application can stop rendering and use DXGI\_PRESENT\_TEST to determine when to resume rendering.</span></span> <span data-ttu-id="06657-110">Você não receberá \_ o status de dxgi \_ obstruído se estiver usando uma cadeia de permuta de modelo invertido.</span><span class="sxs-lookup"><span data-stu-id="06657-110">You will not receive DXGI\_STATUS\_OCCLUDED if you're using a flip model swap chain.</span></span><br/>                                                                                                                           |
| <span id="DXGI_STATUS_MODE_CHANGED"></span><span id="dxgi_status_mode_changed"></span><dl> <span data-ttu-id="06657-111"><dt>**Dxgi \_ Modo de STATUS \_ \_ alterado**</dt> <dt>0x087A0007</dt></span><span class="sxs-lookup"><span data-stu-id="06657-111"><dt>**DXGI\_STATUS\_MODE\_CHANGED**</dt> <dt>0x087A0007</dt></span></span> </dl>                                    | <span data-ttu-id="06657-112">O modo de exibição da área de trabalho foi alterado, pode haver conversão/alongamento de cores.</span><span class="sxs-lookup"><span data-stu-id="06657-112">The desktop display mode has been changed, there might be color conversion/stretching.</span></span> <span data-ttu-id="06657-113">O aplicativo deve chamar [**IDXGISwapChain:: ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) para corresponder ao novo modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="06657-113">The application should call [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) to match the new display mode.</span></span><br/>                                                                       |
| <span id="DXGI_STATUS_MODE_CHANGE_IN_PROGRESS"></span><span id="dxgi_status_mode_change_in_progress"></span><dl> <span data-ttu-id="06657-114"><dt>**Dxgi \_ \_ \_ Alteração do modo \_ de status em \_ andamento**</dt> <dt>0x087A0008</dt></span><span class="sxs-lookup"><span data-stu-id="06657-114"><dt>**DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS**</dt> <dt>0x087A0008</dt></span></span> </dl> | <span data-ttu-id="06657-115">[**IDXGISwapChain:: ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) e [**IDXGISwapChain:: setfullscreenstate**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) retornará \_ \_ \_ a alteração do modo de status dxgi \_ em \_ andamento se uma transição do modo de tela inteira/em janela estiver ocorrendo quando a API for chamada.</span><span class="sxs-lookup"><span data-stu-id="06657-115">[**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget) and [**IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) will return DXGI\_STATUS\_MODE\_CHANGE\_IN\_PROGRESS if a fullscreen/windowed mode transition is occurring when either API is called.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="06657-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="06657-116">Remarks</span></span>

<span data-ttu-id="06657-117">O valor **HRESULT** para cada valor de **\_ status de dxgi** é determinado por essa macro que é definida em DXGItype. h:</span><span class="sxs-lookup"><span data-stu-id="06657-117">The **HRESULT** value for each **DXGI\_STATUS** value is determined from this macro that is defined in DXGItype.h:</span></span>


```
#define _FACDXGI    0x87a
#define MAKE_DXGI_STATUS(code)  MAKE_HRESULT(0, _FACDXGI, code)
```



<span data-ttu-id="06657-118">Por exemplo, **o \_ status \_ de dxgi obstruído** é definido como **0x087A0001**:</span><span class="sxs-lookup"><span data-stu-id="06657-118">For example, **DXGI\_STATUS\_OCCLUDED** is defined as **0x087A0001**:</span></span>


```
#define DXGI_STATUS_OCCLUDED                    MAKE_DXGI_STATUS(1)
```



## <a name="requirements"></a><span data-ttu-id="06657-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06657-119">Requirements</span></span>



| <span data-ttu-id="06657-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="06657-120">Requirement</span></span> | <span data-ttu-id="06657-121">Valor</span><span class="sxs-lookup"><span data-stu-id="06657-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="06657-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="06657-122">Header</span></span><br/> | <dl> <span data-ttu-id="06657-123"><dt>DXGI. h</dt></span><span class="sxs-lookup"><span data-stu-id="06657-123"><dt>DXGI.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06657-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="06657-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06657-125">Constantes DXGI</span><span class="sxs-lookup"><span data-stu-id="06657-125">DXGI Constants</span></span>](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




