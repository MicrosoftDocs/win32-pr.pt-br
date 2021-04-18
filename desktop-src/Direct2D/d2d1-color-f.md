---
title: D2D1_COLOR_F (D2DBaseTypes. h)
description: Descreve os componentes vermelho, verde, azul e alfa de uma cor. | D2D1_COLOR_F (D2DBaseTypes. h)
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105812861"
---
# <a name="d2d1_color_f"></a><span data-ttu-id="9bd4a-105">D2D1 \_ cor \_ F</span><span class="sxs-lookup"><span data-stu-id="9bd4a-105">D2D1\_COLOR\_F</span></span>

<span data-ttu-id="9bd4a-106">Descreve os componentes vermelho, verde, azul e alfa de uma cor.</span><span class="sxs-lookup"><span data-stu-id="9bd4a-106">Describes the red, green, blue, and alpha components of a color.</span></span>


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a><span data-ttu-id="9bd4a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bd4a-107">Remarks</span></span>

<span data-ttu-id="9bd4a-108">**D2d1 \_ A cor \_ f** é um typedef para [**D2D \_ Color \_ f**](d2d-color-f.md), que, por sua vez, é um typedef para [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="9bd4a-108">**D2D1\_COLOR\_F** is a typedef for [**D2D\_COLOR\_F**](d2d-color-f.md), which is itself a typedef for [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span></span> <span data-ttu-id="9bd4a-109">Para obter informações sobre os membros fornecidos pelo **d2d1 \_ Color \_ F**, consulte [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="9bd4a-109">For information about the members provided by **D2D1\_COLOR\_F**, see [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md).</span></span>

<span data-ttu-id="9bd4a-110">A classe [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) fornece um conjunto de cores predefinidas e funções auxiliares para definir cores.</span><span class="sxs-lookup"><span data-stu-id="9bd4a-110">The [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class provides a set of predefined colors and helper functions for defining colors.</span></span> <span data-ttu-id="9bd4a-111">Para obter mais informações, consulte a referência de [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) .</span><span class="sxs-lookup"><span data-stu-id="9bd4a-111">For more information, see the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) reference.</span></span>

## <a name="examples"></a><span data-ttu-id="9bd4a-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9bd4a-112">Examples</span></span>

<span data-ttu-id="9bd4a-113">O exemplo a seguir usa a classe [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) para especificar uma cor predefinida (preto) ao criar um [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span><span class="sxs-lookup"><span data-stu-id="9bd4a-113">The following example uses the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to specify a predefined color (black) when creating an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



<span data-ttu-id="9bd4a-114">O exemplo a seguir usa a classe [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) para especificar uma cor usando valores vermelho, verde, azul e alfa.</span><span class="sxs-lookup"><span data-stu-id="9bd4a-114">The following example uses the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to specify a color using red, green, blue, and alpha values.</span></span>


```C++
ID2D1SolidColorBrush *pGridBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
    &pGridBrush
    );
```



## <a name="requirements"></a><span data-ttu-id="9bd4a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bd4a-115">Requirements</span></span>



| <span data-ttu-id="9bd4a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bd4a-116">Requirement</span></span> | <span data-ttu-id="9bd4a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9bd4a-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bd4a-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bd4a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9bd4a-119">Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="9bd4a-119">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="9bd4a-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bd4a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9bd4a-121">Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9bd4a-121">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="9bd4a-122">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="9bd4a-122">Minimum supported phone</span></span><br/>  | <span data-ttu-id="9bd4a-123">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="9bd4a-123">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="9bd4a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9bd4a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bd4a-125"><dt>D2DBaseTypes. h (incluir D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bd4a-125"><dt>D2DBaseTypes.h (include D2d1.h)</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9bd4a-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bd4a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bd4a-127">D3DCOLORVALUE</span><span class="sxs-lookup"><span data-stu-id="9bd4a-127">D3DCOLORVALUE</span></span>](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[<span data-ttu-id="9bd4a-128">**ColorF**</span><span class="sxs-lookup"><span data-stu-id="9bd4a-128">**ColorF**</span></span>](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 

