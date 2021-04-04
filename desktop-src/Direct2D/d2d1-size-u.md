---
title: D2D1_SIZE_U (D2DBaseTypes. h)
description: Armazena um par ordenado de inteiros, normalmente a largura e a altura de um retângulo.
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b5c317a98169957402dd125c054b8f6e0bc69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085326"
---
# <a name="d2d1_size_u"></a><span data-ttu-id="16ca6-104">D2D1 \_ tamanho \_ U</span><span class="sxs-lookup"><span data-stu-id="16ca6-104">D2D1\_SIZE\_U</span></span>

<span data-ttu-id="16ca6-105">Armazena um par ordenado de inteiros, normalmente a largura e a altura de um retângulo.</span><span class="sxs-lookup"><span data-stu-id="16ca6-105">Stores an ordered pair of integers, typically the width and height of a rectangle.</span></span>


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a><span data-ttu-id="16ca6-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="16ca6-106">Remarks</span></span>

<span data-ttu-id="16ca6-107">Como pontos, os tamanhos são outro conceito de elementos gráficos importantes.</span><span class="sxs-lookup"><span data-stu-id="16ca6-107">Like points, sizes are another important graphics concept.</span></span> <span data-ttu-id="16ca6-108">Em Direct2D, os tamanhos são representados pelas estruturas [**\_ \_ F**](d2d1-size-f.md) de tamanho **d2d1 \_ \_ U** ou d2d1 de tamanho.</span><span class="sxs-lookup"><span data-stu-id="16ca6-108">In Direct2D, sizes are represented by the **D2D1\_SIZE\_U** or [**D2D1\_SIZE\_F**](d2d1-size-f.md) structures.</span></span> <span data-ttu-id="16ca6-109">Ambos contêm um par ordenado de números.</span><span class="sxs-lookup"><span data-stu-id="16ca6-109">They both contain an ordered pair of numbers.</span></span> <span data-ttu-id="16ca6-110">A **estrutura \_ \_ U de tamanho d2d1** contém um par ordenado de valores **UINT32** e a **estrutura \_ \_ F de tamanho d2d1** contém um par ordenado de valores **float** .</span><span class="sxs-lookup"><span data-stu-id="16ca6-110">The **D2D1\_SIZE\_U** structure contains an ordered pair of **UINT32** values, and the **D2D1\_SIZE\_F** structure contains an ordered pair of **FLOAT** values.</span></span>

<span data-ttu-id="16ca6-111">A **estrutura \_ \_ U de tamanho d2d1** fornece uma maneira conveniente de armazenar um par ordenado de números, como a largura e a altura de um retângulo.</span><span class="sxs-lookup"><span data-stu-id="16ca6-111">The **D2D1\_SIZE\_U** structure provides a convenient way for you to store an ordered pair of numbers, such as the width and height of a rectangle.</span></span>

<span data-ttu-id="16ca6-112">**D2d1 \_ SIZE \_ u** é um novo nome para um tipo já definido **D2D \_ Size \_ U**.</span><span class="sxs-lookup"><span data-stu-id="16ca6-112">**D2D1\_SIZE\_U** is a new name for an already defined type **D2D\_SIZE\_U**.</span></span> <span data-ttu-id="16ca6-113">Você pode usar a função **d2d1:: sizeu** para criar uma **estrutura \_ \_ U de tamanho de d2d1** .</span><span class="sxs-lookup"><span data-stu-id="16ca6-113">You can use the **D2D1::SizeU** function to create a **D2D1\_SIZE\_U** structure.</span></span> <span data-ttu-id="16ca6-114">Um uso comum para essa estrutura é especificar o tamanho do pixel de uma estrutura de [**\_ Propriedades de destino de \_ renderização \_ \_ d2d1 HWND**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) .</span><span class="sxs-lookup"><span data-stu-id="16ca6-114">A common use for this structure is to specify the pixel size of a [**D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) structure.</span></span> <span data-ttu-id="16ca6-115">Veja a seguir um exemplo de como usar essa estrutura.</span><span class="sxs-lookup"><span data-stu-id="16ca6-115">The following provides an example of using this structure.</span></span>


```C++
    if (!m_pRenderTarget)
    {
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



## <a name="requirements"></a><span data-ttu-id="16ca6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16ca6-116">Requirements</span></span>



| <span data-ttu-id="16ca6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="16ca6-117">Requirement</span></span> | <span data-ttu-id="16ca6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="16ca6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16ca6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16ca6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="16ca6-120">Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="16ca6-120">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="16ca6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16ca6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="16ca6-122">Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="16ca6-122">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="16ca6-123">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="16ca6-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="16ca6-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="16ca6-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="16ca6-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="16ca6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="16ca6-126"><dt>D2DBaseTypes. h (incluir D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16ca6-126"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="16ca6-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="16ca6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16ca6-128">**D2D \_ tamanho \_ U**</span><span class="sxs-lookup"><span data-stu-id="16ca6-128">**D2D\_SIZE\_U**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[<span data-ttu-id="16ca6-129">**D2D1 \_ tamanho \_ F**</span><span class="sxs-lookup"><span data-stu-id="16ca6-129">**D2D1\_SIZE\_F**</span></span>](d2d1-size-f.md)
</dt> <dt>

[<span data-ttu-id="16ca6-130">**D2D1::HwndRenderTargetProperties**</span><span class="sxs-lookup"><span data-stu-id="16ca6-130">**D2D1::HwndRenderTargetProperties**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 

