---
description: Opções de disposição de textura para APIs de computação IMT.
ms.assetid: ec364418-67c6-42c7-9c5d-b97aa7e17c24
title: Enumeração de sinalizadores D3DXIMT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXIMT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 97731d4720e67fce899bf96f457e55f6adbc05a7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761231"
---
# <a name="d3dximt-flags-enumeration"></a><span data-ttu-id="1e4b4-103">Enumeração de sinalizadores D3DXIMT</span><span class="sxs-lookup"><span data-stu-id="1e4b4-103">D3DXIMT FLAGS enumeration</span></span>

<span data-ttu-id="1e4b4-104">Opções de disposição de textura para APIs de computação IMT.</span><span class="sxs-lookup"><span data-stu-id="1e4b4-104">Texture wrapping options for IMT computation APIs.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e4b4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1e4b4-105">Syntax</span></span>


```C++
typedef enum D3DXIMT_FLAGS { 
  D3DXIMT_WRAP_U   = 1,
  D3DXIMT_WRAP_V   = 2,
  D3DXIMT_WRAP_UV  = 3
} D3DXIMT FLAGS, *LPD3DXIMT FLAGS;
```



## <a name="constants"></a><span data-ttu-id="1e4b4-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="1e4b4-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1e4b4-107"><span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT \_ Wrap \_ U**</span><span class="sxs-lookup"><span data-stu-id="1e4b4-107"><span id="D3DXIMT_WRAP_U"></span><span id="d3dximt_wrap_u"></span>**D3DXIMT\_WRAP\_U**</span></span>
</dt> <dd>

<span data-ttu-id="1e4b4-108">A textura é encapsulada na direção U.</span><span class="sxs-lookup"><span data-stu-id="1e4b4-108">The texture wraps in the U direction.</span></span>

</dd> <dt>

<span data-ttu-id="1e4b4-109"><span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT \_ Wrap \_ V**</span><span class="sxs-lookup"><span data-stu-id="1e4b4-109"><span id="D3DXIMT_WRAP_V"></span><span id="d3dximt_wrap_v"></span>**D3DXIMT\_WRAP\_V**</span></span>
</dt> <dd>

<span data-ttu-id="1e4b4-110">A textura é encapsulada na direção V.</span><span class="sxs-lookup"><span data-stu-id="1e4b4-110">The texture wraps in the V direction.</span></span>

</dd> <dt>

<span data-ttu-id="1e4b4-111"><span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**\_UV de encapsulamento D3DXIMT \_**</span><span class="sxs-lookup"><span data-stu-id="1e4b4-111"><span id="D3DXIMT_WRAP_UV"></span><span id="d3dximt_wrap_uv"></span>**D3DXIMT\_WRAP\_UV**</span></span>
</dt> <dd>

<span data-ttu-id="1e4b4-112">A textura é encapsulada na direção de você e do V.</span><span class="sxs-lookup"><span data-stu-id="1e4b4-112">The texture wraps in both the U and V direction.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e4b4-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e4b4-113">Requirements</span></span>



| <span data-ttu-id="1e4b4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e4b4-114">Requirement</span></span> | <span data-ttu-id="1e4b4-115">Valor</span><span class="sxs-lookup"><span data-stu-id="1e4b4-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e4b4-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e4b4-116">Header</span></span><br/> | <dl> <span data-ttu-id="1e4b4-117"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e4b4-117"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e4b4-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e4b4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e4b4-119">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="1e4b4-119">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="1e4b4-120">**D3DXComputeIMTFromSignal**</span><span class="sxs-lookup"><span data-stu-id="1e4b4-120">**D3DXComputeIMTFromSignal**</span></span>](d3dxcomputeimtfromsignal.md)
</dt> <dt>

[<span data-ttu-id="1e4b4-121">**D3DXComputeIMTFromTexture**</span><span class="sxs-lookup"><span data-stu-id="1e4b4-121">**D3DXComputeIMTFromTexture**</span></span>](d3dxcomputeimtfromtexture.md)
</dt> <dt>

[<span data-ttu-id="1e4b4-122">**D3DXComputeIMTFromPerTexelSignal**</span><span class="sxs-lookup"><span data-stu-id="1e4b4-122">**D3DXComputeIMTFromPerTexelSignal**</span></span>](d3dxcomputeimtfrompertexelsignal.md)
</dt> <dt>

[<span data-ttu-id="1e4b4-123">**D3DXComputeIMTFromPerVertexSignal**</span><span class="sxs-lookup"><span data-stu-id="1e4b4-123">**D3DXComputeIMTFromPerVertexSignal**</span></span>](d3dxcomputeimtfrompervertexsignal.md)
</dt> </dl>

 

 




