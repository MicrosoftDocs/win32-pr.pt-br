---
description: Define operações de buffer de estêncil.
ms.assetid: 338a3b7f-236a-484f-96b8-1e6bfb014484
title: Enumeração D3DSTENCILOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSTENCILOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 34784a57d3afd3862d380554040f3909ec905898
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105759164"
---
# <a name="d3dstencilop-enumeration"></a><span data-ttu-id="8663e-103">Enumeração D3DSTENCILOP</span><span class="sxs-lookup"><span data-stu-id="8663e-103">D3DSTENCILOP enumeration</span></span>

<span data-ttu-id="8663e-104">Define operações de buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="8663e-104">Defines stencil-buffer operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="8663e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8663e-105">Syntax</span></span>


```C++
typedef enum D3DSTENCILOP { 
  D3DSTENCILOP_KEEP         = 1,
  D3DSTENCILOP_ZERO         = 2,
  D3DSTENCILOP_REPLACE      = 3,
  D3DSTENCILOP_INCRSAT      = 4,
  D3DSTENCILOP_DECRSAT      = 5,
  D3DSTENCILOP_INVERT       = 6,
  D3DSTENCILOP_INCR         = 7,
  D3DSTENCILOP_DECR         = 8,
  D3DSTENCILOP_FORCE_DWORD  = 0x7fffffff
} D3DSTENCILOP, *LPD3DSTENCILOP;
```



## <a name="constants"></a><span data-ttu-id="8663e-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="8663e-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8663e-107"><span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP \_ manter**</span><span class="sxs-lookup"><span data-stu-id="8663e-107"><span id="D3DSTENCILOP_KEEP"></span><span id="d3dstencilop_keep"></span>**D3DSTENCILOP\_KEEP**</span></span>
</dt> <dd>

<span data-ttu-id="8663e-108">Não atualize a entrada no buffer do estêncil.</span><span class="sxs-lookup"><span data-stu-id="8663e-108">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="8663e-109">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="8663e-109">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="8663e-110"><span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP \_ zero**</span><span class="sxs-lookup"><span data-stu-id="8663e-110"><span id="D3DSTENCILOP_ZERO"></span><span id="d3dstencilop_zero"></span>**D3DSTENCILOP\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="8663e-111">Defina a entrada de buffer de estêncil como 0.</span><span class="sxs-lookup"><span data-stu-id="8663e-111">Set the stencil-buffer entry to 0.</span></span>

</dd> <dt>

<span data-ttu-id="8663e-112"><span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP \_ substituir**</span><span class="sxs-lookup"><span data-stu-id="8663e-112"><span id="D3DSTENCILOP_REPLACE"></span><span id="d3dstencilop_replace"></span>**D3DSTENCILOP\_REPLACE**</span></span>
</dt> <dd>

<span data-ttu-id="8663e-113">Substitua a entrada de buffer de estêncil por um valor de referência.</span><span class="sxs-lookup"><span data-stu-id="8663e-113">Replace the stencil-buffer entry with a reference value.</span></span>

</dd> <dt>

<span data-ttu-id="8663e-114"><span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP \_ INCRSAT**</span><span class="sxs-lookup"><span data-stu-id="8663e-114"><span id="D3DSTENCILOP_INCRSAT"></span><span id="d3dstencilop_incrsat"></span>**D3DSTENCILOP\_INCRSAT**</span></span>
</dt> <dd>

<span data-ttu-id="8663e-115">Aumente a entrada do buffer de estêncil, fixação MSS para o valor máximo.</span><span class="sxs-lookup"><span data-stu-id="8663e-115">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>

</dd> <dt>

<span data-ttu-id="8663e-116"><span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP \_ DECRSAT**</span><span class="sxs-lookup"><span data-stu-id="8663e-116"><span id="D3DSTENCILOP_DECRSAT"></span><span id="d3dstencilop_decrsat"></span>**D3DSTENCILOP\_DECRSAT**</span></span>
</dt> <dd>

<span data-ttu-id="8663e-117">Decrementar a entrada de buffer de estêncil, fixação MSS para zero.</span><span class="sxs-lookup"><span data-stu-id="8663e-117">Decrement the stencil-buffer entry, clamping to zero.</span></span>

</dd> <dt>

<span data-ttu-id="8663e-118"><span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**\_Inverter D3DSTENCILOP**</span><span class="sxs-lookup"><span data-stu-id="8663e-118"><span id="D3DSTENCILOP_INVERT"></span><span id="d3dstencilop_invert"></span>**D3DSTENCILOP\_INVERT**</span></span>
</dt> <dd>

<span data-ttu-id="8663e-119">Inverta os bits na entrada do buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="8663e-119">Invert the bits in the stencil-buffer entry.</span></span>

</dd> <dt>

<span data-ttu-id="8663e-120"><span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP \_ incr**</span><span class="sxs-lookup"><span data-stu-id="8663e-120"><span id="D3DSTENCILOP_INCR"></span><span id="d3dstencilop_incr"></span>**D3DSTENCILOP\_INCR**</span></span>
</dt> <dd>

<span data-ttu-id="8663e-121">Aumente a entrada do buffer de estêncil, encapsulando para zero se o novo valor exceder o valor máximo.</span><span class="sxs-lookup"><span data-stu-id="8663e-121">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>

</dd> <dt>

<span data-ttu-id="8663e-122"><span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP \_ DECR**</span><span class="sxs-lookup"><span data-stu-id="8663e-122"><span id="D3DSTENCILOP_DECR"></span><span id="d3dstencilop_decr"></span>**D3DSTENCILOP\_DECR**</span></span>
</dt> <dd>

<span data-ttu-id="8663e-123">Decrementar a entrada de buffer de estêncil, encapsulando o valor máximo se o novo valor for menor que zero.</span><span class="sxs-lookup"><span data-stu-id="8663e-123">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span>

</dd> <dt>

<span data-ttu-id="8663e-124"><span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8663e-124"><span id="D3DSTENCILOP_FORCE_DWORD"></span><span id="d3dstencilop_force_dword"></span>**D3DSTENCILOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8663e-125">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="8663e-125">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="8663e-126">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8663e-126">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="8663e-127">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="8663e-127">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8663e-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="8663e-128">Remarks</span></span>

<span data-ttu-id="8663e-129">Entradas de buffer de estêncil são valores inteiros variando de 0 a 2 ⁿ-1, em que n é a profundidade de bits do buffer de estêncil.</span><span class="sxs-lookup"><span data-stu-id="8663e-129">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8663e-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8663e-130">Requirements</span></span>



| <span data-ttu-id="8663e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="8663e-131">Requirement</span></span> | <span data-ttu-id="8663e-132">Valor</span><span class="sxs-lookup"><span data-stu-id="8663e-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8663e-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8663e-133">Header</span></span><br/> | <dl> <span data-ttu-id="8663e-134"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8663e-134"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8663e-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="8663e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8663e-136">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="8663e-136">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




