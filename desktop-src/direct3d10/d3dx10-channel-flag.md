---
description: Esses sinalizadores são usados por funções que operam em um ou mais canais em uma textura.
ms.assetid: 54ecb39a-a36e-43bb-bb51-78b7375716d8
title: Enumeração de D3DX10_CHANNEL_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_CHANNEL_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f21958ab964a70116a551c0cb8dadbce6db88f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298776"
---
# <a name="d3dx10_channel_flag-enumeration"></a><span data-ttu-id="fcf62-103">Enumeração de sinalizador de \_ canal D3DX10 \_</span><span class="sxs-lookup"><span data-stu-id="fcf62-103">D3DX10\_CHANNEL\_FLAG enumeration</span></span>

<span data-ttu-id="fcf62-104">Esses sinalizadores são usados por funções que operam em um ou mais canais em uma textura.</span><span class="sxs-lookup"><span data-stu-id="fcf62-104">These flags are used by functions which operate on one or more channels in a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcf62-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcf62-105">Syntax</span></span>


```C++
typedef enum D3DX10_CHANNEL_FLAG { 
  D3DX10_CHANNEL_RED        = (1 << 0),
  D3DX10_CHANNEL_BLUE       = (1 << 1),
  D3DX10_CHANNEL_GREEN      = (1 << 2),
  D3DX10_CHANNEL_ALPHA      = (1 << 3),
  D3DX10_CHANNEL_LUMINANCE  = (1 << 4)
} D3DX10_CHANNEL_FLAG, *LPD3DX10_CHANNEL_FLAG;
```



## <a name="constants"></a><span data-ttu-id="fcf62-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="fcf62-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fcf62-107"><span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10 do \_ canal \_ vermelho**</span><span class="sxs-lookup"><span data-stu-id="fcf62-107"><span id="D3DX10_CHANNEL_RED"></span><span id="d3dx10_channel_red"></span>**D3DX10\_CHANNEL\_RED**</span></span>
</dt> <dd>

<span data-ttu-id="fcf62-108">Indica que o canal vermelho deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="fcf62-108">Indicates the red channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="fcf62-109"><span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10 de \_ canal \_ azul**</span><span class="sxs-lookup"><span data-stu-id="fcf62-109"><span id="D3DX10_CHANNEL_BLUE"></span><span id="d3dx10_channel_blue"></span>**D3DX10\_CHANNEL\_BLUE**</span></span>
</dt> <dd>

<span data-ttu-id="fcf62-110">Indica que o canal azul deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="fcf62-110">Indicates the blue channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="fcf62-111"><span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3DX10 de \_ canal \_ verde**</span><span class="sxs-lookup"><span data-stu-id="fcf62-111"><span id="D3DX10_CHANNEL_GREEN"></span><span id="d3dx10_channel_green"></span>**D3DX10\_CHANNEL\_GREEN**</span></span>
</dt> <dd>

<span data-ttu-id="fcf62-112">Indica que o canal verde deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="fcf62-112">Indicates the green channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="fcf62-113"><span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3DX10 \_ canal \_ alfa**</span><span class="sxs-lookup"><span data-stu-id="fcf62-113"><span id="D3DX10_CHANNEL_ALPHA"></span><span id="d3dx10_channel_alpha"></span>**D3DX10\_CHANNEL\_ALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="fcf62-114">Indica que o canal alfa deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="fcf62-114">Indicates the alpha channel should be used.</span></span>

</dd> <dt>

<span data-ttu-id="fcf62-115"><span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**\_Luminância de canal D3DX10 \_**</span><span class="sxs-lookup"><span data-stu-id="fcf62-115"><span id="D3DX10_CHANNEL_LUMINANCE"></span><span id="d3dx10_channel_luminance"></span>**D3DX10\_CHANNEL\_LUMINANCE**</span></span>
</dt> <dd>

<span data-ttu-id="fcf62-116">Indica que o luminaces dos canais vermelho, verde e azul deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="fcf62-116">Indicates the luminaces of the red, green, and blue channels should be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fcf62-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcf62-117">Requirements</span></span>



| <span data-ttu-id="fcf62-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcf62-118">Requirement</span></span> | <span data-ttu-id="fcf62-119">Valor</span><span class="sxs-lookup"><span data-stu-id="fcf62-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcf62-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fcf62-120">Header</span></span><br/> | <dl> <span data-ttu-id="fcf62-121"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcf62-121"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fcf62-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="fcf62-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcf62-123">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="fcf62-123">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




