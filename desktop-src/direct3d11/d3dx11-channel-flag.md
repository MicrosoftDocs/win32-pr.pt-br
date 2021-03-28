---
title: Enumeração de D3DX11_CHANNEL_FLAG (D3DX11tex. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Esses sinalizadores são usados por funções que operam em um ou mais canais em uma textura.
ms.assetid: 058a0a1e-3c1b-4397-a41a-2e47d878cd92
keywords:
- Enumeração D3DX11_CHANNEL_FLAG Direct3D 11
- Ponteiro de enumeração LPD3DX11_CHANNEL_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_CHANNEL_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e3097552637ce96663671dda443684ebda2b65
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104371018"
---
# <a name="d3dx11_channel_flag-enumeration"></a><span data-ttu-id="775a5-106">Enumeração de sinalizador de \_ canal D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="775a5-106">D3DX11\_CHANNEL\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="775a5-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="775a5-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="775a5-108">Esses sinalizadores são usados por funções que operam em um ou mais canais em uma textura.</span><span class="sxs-lookup"><span data-stu-id="775a5-108">These flags are used by functions which operate on one or more channels in a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="775a5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="775a5-109">Syntax</span></span>


```C++
typedef enum D3DX11_CHANNEL_FLAG { 
  D3DX11_CHANNEL_RED        = (1 << 0),
  D3DX11_CHANNEL_BLUE       = (1 << 1),
  D3DX11_CHANNEL_GREEN      = (1 << 2),
  D3DX11_CHANNEL_ALPHA      = (1 << 3),
  D3DX11_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX11_CHANNEL_FLAG, *LPD3DX11_CHANNEL_FLAG;
```



## <a name="constants"></a><span data-ttu-id="775a5-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="775a5-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="775a5-111"><span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**D3DX11 do \_ canal \_ vermelho**</span><span class="sxs-lookup"><span data-stu-id="775a5-111"><span id="D3DX11_CHANNEL_RED"></span><span id="d3dx11_channel_red"></span>**D3DX11\_CHANNEL\_RED**</span></span>
</dt> <dd>

<span data-ttu-id="775a5-112">Indica que o canal vermelho deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="775a5-112">Indicates the red channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="775a5-113"><span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**D3DX11 de \_ canal \_ azul**</span><span class="sxs-lookup"><span data-stu-id="775a5-113"><span id="D3DX11_CHANNEL_BLUE"></span><span id="d3dx11_channel_blue"></span>**D3DX11\_CHANNEL\_BLUE**</span></span>
</dt> <dd>

<span data-ttu-id="775a5-114">Indica que o canal azul deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="775a5-114">Indicates the blue channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="775a5-115"><span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**D3DX11 de \_ canal \_ verde**</span><span class="sxs-lookup"><span data-stu-id="775a5-115"><span id="D3DX11_CHANNEL_GREEN"></span><span id="d3dx11_channel_green"></span>**D3DX11\_CHANNEL\_GREEN**</span></span>
</dt> <dd>

<span data-ttu-id="775a5-116">Indica que o canal verde deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="775a5-116">Indicates the green channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="775a5-117"><span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**D3DX11 \_ canal \_ alfa**</span><span class="sxs-lookup"><span data-stu-id="775a5-117"><span id="D3DX11_CHANNEL_ALPHA"></span><span id="d3dx11_channel_alpha"></span>**D3DX11\_CHANNEL\_ALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="775a5-118">Indica que o canal alfa deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="775a5-118">Indicates the alpha channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="775a5-119"><span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**\_Luminância de canal D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="775a5-119"><span id="D3DX11_CHANNEL_LUMINANCE"></span><span id="d3dx11_channel_luminance"></span>**D3DX11\_CHANNEL\_LUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="775a5-120">Indica que o luminaces dos canais vermelho, verde e azul deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="775a5-120">Indicates the luminaces of the red, green, and blue channels should be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="775a5-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="775a5-121">Requirements</span></span>



| <span data-ttu-id="775a5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="775a5-122">Requirement</span></span> | <span data-ttu-id="775a5-123">Valor</span><span class="sxs-lookup"><span data-stu-id="775a5-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="775a5-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="775a5-124">Header</span></span><br/> | <dl> <span data-ttu-id="775a5-125"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="775a5-125"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="775a5-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="775a5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="775a5-127">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="775a5-127">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





