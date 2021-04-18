---
description: Define as operações de combinação com suporte. Consulte comentários para ver as definições de termos.
ms.assetid: ae750d84-ed7d-4a76-bf64-eae8828c66c7
title: Enumeração D3DBLENDOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLENDOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3ad23d3fb2a93734047f55a46c14335069c95ea9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105815564"
---
# <a name="d3dblendop-enumeration"></a><span data-ttu-id="f4549-104">Enumeração D3DBLENDOP</span><span class="sxs-lookup"><span data-stu-id="f4549-104">D3DBLENDOP enumeration</span></span>

<span data-ttu-id="f4549-105">Define as operações de combinação com suporte.</span><span class="sxs-lookup"><span data-stu-id="f4549-105">Defines the supported blend operations.</span></span> <span data-ttu-id="f4549-106">Consulte comentários para ver as definições de termos.</span><span class="sxs-lookup"><span data-stu-id="f4549-106">See Remarks for definitions of terms.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4549-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4549-107">Syntax</span></span>


```C++
typedef enum D3DBLENDOP { 
  D3DBLENDOP_ADD          = 1,
  D3DBLENDOP_SUBTRACT     = 2,
  D3DBLENDOP_REVSUBTRACT  = 3,
  D3DBLENDOP_MIN          = 4,
  D3DBLENDOP_MAX          = 5,
  D3DBLENDOP_FORCE_DWORD  = 0x7fffffff
} D3DBLENDOP, *LPD3DBLENDOP;
```



## <a name="constants"></a><span data-ttu-id="f4549-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="f4549-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f4549-109"><span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP \_ Adicionar**</span><span class="sxs-lookup"><span data-stu-id="f4549-109"><span id="D3DBLENDOP_ADD"></span><span id="d3dblendop_add"></span>**D3DBLENDOP\_ADD**</span></span>
</dt> <dd>

<span data-ttu-id="f4549-110">O resultado é o destino adicionado à origem.</span><span class="sxs-lookup"><span data-stu-id="f4549-110">The result is the destination added to the source.</span></span> <span data-ttu-id="f4549-111">Resultado = origem + destino</span><span class="sxs-lookup"><span data-stu-id="f4549-111">Result = Source + Destination</span></span>

</dd> <dt>

<span data-ttu-id="f4549-112"><span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**\_Subtrair D3DBLENDOP**</span><span class="sxs-lookup"><span data-stu-id="f4549-112"><span id="D3DBLENDOP_SUBTRACT"></span><span id="d3dblendop_subtract"></span>**D3DBLENDOP\_SUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="f4549-113">O resultado é o destino subtraído da origem.</span><span class="sxs-lookup"><span data-stu-id="f4549-113">The result is the destination subtracted from to the source.</span></span> <span data-ttu-id="f4549-114">Resultado = destino de origem</span><span class="sxs-lookup"><span data-stu-id="f4549-114">Result = Source - Destination</span></span>

</dd> <dt>

<span data-ttu-id="f4549-115"><span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP \_ REVSUBTRACT**</span><span class="sxs-lookup"><span data-stu-id="f4549-115"><span id="D3DBLENDOP_REVSUBTRACT"></span><span id="d3dblendop_revsubtract"></span>**D3DBLENDOP\_REVSUBTRACT**</span></span>
</dt> <dd>

<span data-ttu-id="f4549-116">O resultado é a origem subtraída do destino.</span><span class="sxs-lookup"><span data-stu-id="f4549-116">The result is the source subtracted from the destination.</span></span> <span data-ttu-id="f4549-117">Resultado = origem-de-destino</span><span class="sxs-lookup"><span data-stu-id="f4549-117">Result = Destination - Source</span></span>

</dd> <dt>

<span data-ttu-id="f4549-118"><span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP \_ mín.**</span><span class="sxs-lookup"><span data-stu-id="f4549-118"><span id="D3DBLENDOP_MIN"></span><span id="d3dblendop_min"></span>**D3DBLENDOP\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="f4549-119">O resultado é o mínimo da origem e do destino.</span><span class="sxs-lookup"><span data-stu-id="f4549-119">The result is the minimum of the source and destination.</span></span> <span data-ttu-id="f4549-120">Resultado = mín (origem, destino)</span><span class="sxs-lookup"><span data-stu-id="f4549-120">Result = MIN(Source, Destination)</span></span>

</dd> <dt>

<span data-ttu-id="f4549-121"><span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP \_ Max**</span><span class="sxs-lookup"><span data-stu-id="f4549-121"><span id="D3DBLENDOP_MAX"></span><span id="d3dblendop_max"></span>**D3DBLENDOP\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="f4549-122">O resultado é o máximo da origem e do destino.</span><span class="sxs-lookup"><span data-stu-id="f4549-122">The result is the maximum of the source and destination.</span></span> <span data-ttu-id="f4549-123">Resultado = máximo (origem, destino)</span><span class="sxs-lookup"><span data-stu-id="f4549-123">Result = MAX(Source, Destination)</span></span>

</dd> <dt>

<span data-ttu-id="f4549-124"><span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f4549-124"><span id="D3DBLENDOP_FORCE_DWORD"></span><span id="d3dblendop_force_dword"></span>**D3DBLENDOP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="f4549-125">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="f4549-125">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="f4549-126">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="f4549-126">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="f4549-127">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="f4549-127">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4549-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4549-128">Remarks</span></span>

<span data-ttu-id="f4549-129">Origem, destino e resultado são definidos como:</span><span class="sxs-lookup"><span data-stu-id="f4549-129">Source, Destination, and Result are defined as:</span></span>



| <span data-ttu-id="f4549-130">Termo</span><span class="sxs-lookup"><span data-stu-id="f4549-130">Term</span></span>        | <span data-ttu-id="f4549-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4549-131">Type</span></span>   | <span data-ttu-id="f4549-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4549-132">Description</span></span>                                                            |
|-------------|--------|------------------------------------------------------------------------|
| <span data-ttu-id="f4549-133">Fonte</span><span class="sxs-lookup"><span data-stu-id="f4549-133">Source</span></span>      | <span data-ttu-id="f4549-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4549-134">Input</span></span>  | <span data-ttu-id="f4549-135">Cor do pixel de origem antes da operação.</span><span class="sxs-lookup"><span data-stu-id="f4549-135">Color of the source pixel before the operation.</span></span>                        |
| <span data-ttu-id="f4549-136">Destino</span><span class="sxs-lookup"><span data-stu-id="f4549-136">Destination</span></span> | <span data-ttu-id="f4549-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4549-137">Input</span></span>  | <span data-ttu-id="f4549-138">A cor do pixel no buffer de destino antes da operação.</span><span class="sxs-lookup"><span data-stu-id="f4549-138">Color of the pixel in the destination buffer before the operation.</span></span>     |
| <span data-ttu-id="f4549-139">Resultado</span><span class="sxs-lookup"><span data-stu-id="f4549-139">Result</span></span>      | <span data-ttu-id="f4549-140">Saída</span><span class="sxs-lookup"><span data-stu-id="f4549-140">Output</span></span> | <span data-ttu-id="f4549-141">Valor retornado que é a cor mesclada resultante da operação.</span><span class="sxs-lookup"><span data-stu-id="f4549-141">Returned value that is the blended color resulting from the operation.</span></span> |



 

<span data-ttu-id="f4549-142">Esse tipo enumerado define os valores usados pelos seguintes Estados de renderização:</span><span class="sxs-lookup"><span data-stu-id="f4549-142">This enumerated type defines values used by the following render states:</span></span>

-   <span data-ttu-id="f4549-143">D3DRS \_ BLENDOP</span><span class="sxs-lookup"><span data-stu-id="f4549-143">D3DRS\_BLENDOP</span></span>
-   <span data-ttu-id="f4549-144">D3DRS \_ BLENDOPALPHA</span><span class="sxs-lookup"><span data-stu-id="f4549-144">D3DRS\_BLENDOPALPHA</span></span>

## <a name="requirements"></a><span data-ttu-id="f4549-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4549-145">Requirements</span></span>



| <span data-ttu-id="f4549-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4549-146">Requirement</span></span> | <span data-ttu-id="f4549-147">Valor</span><span class="sxs-lookup"><span data-stu-id="f4549-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4549-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4549-148">Header</span></span><br/> | <dl> <span data-ttu-id="f4549-149"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4549-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4549-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4549-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4549-151">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="f4549-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="f4549-152">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="f4549-152">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="f4549-153">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="f4549-153">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
