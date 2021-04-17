---
title: Métodos ID2D1Factory CreateHwndRenderTarget (D2d1. h)
description: Cria um ID2D1HwndRenderTarget, um destino de renderização que é renderizado para uma janela.
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
keywords:
- Métodos CreateHwndRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 984de8aea923c5b90d05fb79bc0c9edc319fb4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747426"
---
# <a name="id2d1factorycreatehwndrendertarget-methods"></a><span data-ttu-id="bdcb8-104">Métodos ID2D1Factory:: CreateHwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="bdcb8-104">ID2D1Factory::CreateHwndRenderTarget methods</span></span>

<span data-ttu-id="bdcb8-105">Cria um [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), um destino de renderização que é renderizado para uma janela.</span><span class="sxs-lookup"><span data-stu-id="bdcb8-105">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span>

### <a name="overload-list"></a><span data-ttu-id="bdcb8-106">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="bdcb8-106">Overload list</span></span>



| <span data-ttu-id="bdcb8-107">Método</span><span class="sxs-lookup"><span data-stu-id="bdcb8-107">Method</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="bdcb8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="bdcb8-108">Description</span></span>                                                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdcb8-109">[**CreateHwndRenderTarget (D2D1 \_ render \_ Propriedades de destino \_ \* , \_ d2d1 \_ HWND \_ process \_ Propriedades \* de destino, ID2D1HwndRenderTarget \* \* )**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="bdcb8-109">[**CreateHwndRenderTarget(D2D1\_RENDER\_TARGET\_PROPERTIES\*,D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES\*,ID2D1HwndRenderTarget\*\*)**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))</span></span> | <span data-ttu-id="bdcb8-110">Cria um [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), um destino de renderização que é renderizado para uma janela.</span><span class="sxs-lookup"><span data-stu-id="bdcb8-110">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span><br/> |
| <span data-ttu-id="bdcb8-111">[**CreateHwndRenderTarget ( \_ Propriedades de destino de RENDERIZAÇÃO D2D1 \_ \_&, d2d1 \_ HWND de renderização de propriedades de \_ \_ destino \_&, ID2D1HwndRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))</span><span class="sxs-lookup"><span data-stu-id="bdcb8-111">[**CreateHwndRenderTarget(D2D1\_RENDER\_TARGET\_PROPERTIES&,D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES&,ID2D1HwndRenderTarget\*\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))</span></span>   | <span data-ttu-id="bdcb8-112">Cria um [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), um destino de renderização que é renderizado para uma janela.</span><span class="sxs-lookup"><span data-stu-id="bdcb8-112">Creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)), a render target that renders to a window.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bdcb8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdcb8-113">Remarks</span></span>

<span data-ttu-id="bdcb8-114">Quando você cria um destino de renderização e a aceleração de hardware está disponível, você aloca recursos na GPU do computador.</span><span class="sxs-lookup"><span data-stu-id="bdcb8-114">When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU.</span></span> <span data-ttu-id="bdcb8-115">Ao criar um destino de renderização uma vez e mantê-lo o mais longo possível, você obterá benefícios de desempenho.</span><span class="sxs-lookup"><span data-stu-id="bdcb8-115">By creating a render target once and retaining it as long as possible, you gain performance benefits.</span></span> <span data-ttu-id="bdcb8-116">Seu aplicativo deve criar destinos de renderização uma vez e mantê-los durante a vida útil do aplicativo ou até que o erro de [**\_ \_ destino de recriação de D2DERR**](direct2d-error-codes.md) seja recebido.</span><span class="sxs-lookup"><span data-stu-id="bdcb8-116">Your application should create render targets once and hold onto them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="bdcb8-117">Quando receber esse erro, você precisará recriar o destino de renderização (e todos os recursos que ele criou).</span><span class="sxs-lookup"><span data-stu-id="bdcb8-117">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

## <a name="examples"></a><span data-ttu-id="bdcb8-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bdcb8-118">Examples</span></span>

<span data-ttu-id="bdcb8-119">O exemplo a seguir cria um [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="bdcb8-119">The following example creates an [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)).</span></span>


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



## <a name="requirements"></a><span data-ttu-id="bdcb8-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdcb8-120">Requirements</span></span>



| <span data-ttu-id="bdcb8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdcb8-121">Requirement</span></span> | <span data-ttu-id="bdcb8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="bdcb8-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bdcb8-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bdcb8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="bdcb8-124"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdcb8-124"><dt>D2d1.h</dt></span></span> </dl>   |
| <span data-ttu-id="bdcb8-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bdcb8-125">Library</span></span><br/> | <dl> <span data-ttu-id="bdcb8-126"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdcb8-126"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="bdcb8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bdcb8-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="bdcb8-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdcb8-128"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdcb8-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdcb8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdcb8-130">**ID2D1Factory**</span><span class="sxs-lookup"><span data-stu-id="bdcb8-130">**ID2D1Factory**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
