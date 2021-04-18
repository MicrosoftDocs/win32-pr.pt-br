---
description: Define os modos de remoção com suporte.
ms.assetid: b669307c-0d40-4ecb-8a2e-8bd1d9c65647
title: Enumeração D3DCULL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCULL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: e88aa1baf86b2b03177cc686bf83299311065283
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771627"
---
# <a name="d3dcull-enumeration"></a><span data-ttu-id="8c4b9-103">Enumeração D3DCULL</span><span class="sxs-lookup"><span data-stu-id="8c4b9-103">D3DCULL enumeration</span></span>

<span data-ttu-id="8c4b9-104">Define os modos de remoção com suporte.</span><span class="sxs-lookup"><span data-stu-id="8c4b9-104">Defines the supported culling modes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c4b9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c4b9-105">Syntax</span></span>


```C++
typedef enum D3DCULL { 
  D3DCULL_NONE         = 1,
  D3DCULL_CW           = 2,
  D3DCULL_CCW          = 3,
  D3DCULL_FORCE_DWORD  = 0x7fffffff
} D3DCULL, *LPD3DCULL;
```



## <a name="constants"></a><span data-ttu-id="8c4b9-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="8c4b9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8c4b9-107"><span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="8c4b9-107"><span id="D3DCULL_NONE"></span><span id="d3dcull_none"></span>**D3DCULL\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="8c4b9-108">Não faça a remoção de faces.</span><span class="sxs-lookup"><span data-stu-id="8c4b9-108">Do not cull back faces.</span></span>

</dd> <dt>

<span data-ttu-id="8c4b9-109"><span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**PV de D3DCULL \_**</span><span class="sxs-lookup"><span data-stu-id="8c4b9-109"><span id="D3DCULL_CW"></span><span id="d3dcull_cw"></span>**D3DCULL\_CW**</span></span>
</dt> <dd>

<span data-ttu-id="8c4b9-110">Faça a remoção de faces com vértices no sentido horário.</span><span class="sxs-lookup"><span data-stu-id="8c4b9-110">Cull back faces with clockwise vertices.</span></span>

</dd> <dt>

<span data-ttu-id="8c4b9-111"><span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**\_CCW D3DCULL**</span><span class="sxs-lookup"><span data-stu-id="8c4b9-111"><span id="D3DCULL_CCW"></span><span id="d3dcull_ccw"></span>**D3DCULL\_CCW**</span></span>
</dt> <dd>

<span data-ttu-id="8c4b9-112">Faça a remoção de faces com vértices no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="8c4b9-112">Cull back faces with counterclockwise vertices.</span></span>

</dd> <dt>

<span data-ttu-id="8c4b9-113"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="8c4b9-113"><span id="D3DCULL_FORCE_DWORD"></span><span id="d3dcull_force_dword"></span>**D3DCULL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="8c4b9-114">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="8c4b9-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="8c4b9-115">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="8c4b9-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="8c4b9-116">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="8c4b9-116">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c4b9-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c4b9-117">Remarks</span></span>

<span data-ttu-id="8c4b9-118">Os valores nesse tipo enumerado são usados pelo estado de renderização D3DRS de \_ seleção.</span><span class="sxs-lookup"><span data-stu-id="8c4b9-118">The values in this enumerated type are used by the D3DRS\_CULLMODE render state.</span></span> <span data-ttu-id="8c4b9-119">Os modos de remoção definem como as faces traseiras são refeitas ao renderizar uma geometria.</span><span class="sxs-lookup"><span data-stu-id="8c4b9-119">The culling modes define how back faces are culled when rendering a geometry.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c4b9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c4b9-120">Requirements</span></span>



| <span data-ttu-id="8c4b9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c4b9-121">Requirement</span></span> | <span data-ttu-id="8c4b9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8c4b9-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c4b9-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8c4b9-123">Header</span></span><br/> | <dl> <span data-ttu-id="8c4b9-124"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c4b9-124"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c4b9-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c4b9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c4b9-126">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="8c4b9-126">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="8c4b9-127">**D3DCAPS9**</span><span class="sxs-lookup"><span data-stu-id="8c4b9-127">**D3DCAPS9**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)
</dt> <dt>

[<span data-ttu-id="8c4b9-128">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="8c4b9-128">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> </dl>

 

 
