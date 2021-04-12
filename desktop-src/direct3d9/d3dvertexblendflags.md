---
description: Define sinalizadores usados para controlar o número ou as matrizes que o sistema aplica ao executar a mesclagem de vértice de várias matrizes.
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: Enumeração D3DVERTEXBLENDFLAGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBLENDFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0b4d22740a9ad06a9848dc7649d62ac06d37a056
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298596"
---
# <a name="d3dvertexblendflags-enumeration"></a><span data-ttu-id="8cc31-103">Enumeração D3DVERTEXBLENDFLAGS</span><span class="sxs-lookup"><span data-stu-id="8cc31-103">D3DVERTEXBLENDFLAGS enumeration</span></span>

<span data-ttu-id="8cc31-104">Define sinalizadores usados para controlar o número ou as matrizes que o sistema aplica ao executar a mesclagem de vértice de várias matrizes.</span><span class="sxs-lookup"><span data-stu-id="8cc31-104">Defines flags used to control the number or matrices that the system applies when performing multimatrix vertex blending.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc31-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8cc31-105">Syntax</span></span>


```C++
typedef enum D3DVERTEXBLENDFLAGS { 
  D3DVBF_DISABLE   = 0,
  D3DVBF_1WEIGHTS  = 1,
  D3DVBF_2WEIGHTS  = 2,
  D3DVBF_3WEIGHTS  = 3,
  D3DVBF_TWEENING  = 255,
  D3DVBF_0WEIGHTS  = 256
} D3DVERTEXBLENDFLAGS, *LPD3DVERTEXBLENDFLAGS;
```



## <a name="constants"></a><span data-ttu-id="8cc31-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="8cc31-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8cc31-107"><span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF \_ desabilitar**</span><span class="sxs-lookup"><span data-stu-id="8cc31-107"><span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**D3DVBF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="8cc31-108">Desabilitar mesclagem de vértice; Aplique somente a matriz mundial definida pela macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , em que o valor de índice para o estado de transformação é 0.</span><span class="sxs-lookup"><span data-stu-id="8cc31-108">Disable vertex blending; apply only the world matrix set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation state is 0.</span></span>

</dd> <dt>

<span data-ttu-id="8cc31-109"><span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="8cc31-109"><span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF\_1WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="8cc31-110">Habilite a mesclagem de vértice entre as duas matrizes definidas pela macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , em que o valor de índice para os Estados de transformação é 0 e 1.</span><span class="sxs-lookup"><span data-stu-id="8cc31-110">Enable vertex blending between the two matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0 and 1.</span></span>

</dd> <dt>

<span data-ttu-id="8cc31-111"><span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="8cc31-111"><span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF\_2WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="8cc31-112">Habilite a mesclagem de vértice entre as três matrizes definidas pela macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , em que o valor de índice para os Estados de transformação é 0, 1 e 2.</span><span class="sxs-lookup"><span data-stu-id="8cc31-112">Enable vertex blending between the three matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0, 1, and 2.</span></span>

</dd> <dt>

<span data-ttu-id="8cc31-113"><span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="8cc31-113"><span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF\_3WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="8cc31-114">Habilite a mesclagem de vértice entre as quatro matrizes definidas pela macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , em que o valor de índice para os Estados de transformação é 0, 1, 2 e 3.</span><span class="sxs-lookup"><span data-stu-id="8cc31-114">Enable vertex blending between the four matrices set by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, where the index value for the transformation states are 0, 1, 2, and 3.</span></span>

</dd> <dt>

<span data-ttu-id="8cc31-115"><span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**\_Interpolação D3DVBF**</span><span class="sxs-lookup"><span data-stu-id="8cc31-115"><span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**D3DVBF\_TWEENING**</span></span>
</dt> <dd>

<span data-ttu-id="8cc31-116">A mesclagem de vértice é feita usando o valor atribuído a D3DRS \_ TWEENFACTOR.</span><span class="sxs-lookup"><span data-stu-id="8cc31-116">Vertex blending is done by using the value assigned to D3DRS\_TWEENFACTOR.</span></span>

</dd> <dt>

<span data-ttu-id="8cc31-117"><span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0WEIGHTS**</span><span class="sxs-lookup"><span data-stu-id="8cc31-117"><span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF\_0WEIGHTS**</span></span>
</dt> <dd>

<span data-ttu-id="8cc31-118">Use uma matriz única com peso de 1,0.</span><span class="sxs-lookup"><span data-stu-id="8cc31-118">Use a single matrix with a weight of 1.0.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cc31-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cc31-119">Remarks</span></span>

<span data-ttu-id="8cc31-120">Os membros desse tipo são usados com o \_ estado de RENDERIZAÇÃO D3DRS VERTEXBLEND.</span><span class="sxs-lookup"><span data-stu-id="8cc31-120">Members of this type are used with the D3DRS\_VERTEXBLEND render state.</span></span>

<span data-ttu-id="8cc31-121">A combinação de geometria (mesclagem de vértice multimatriz) requer que seu aplicativo use um formato de vértice com pesos de mistura (beta) para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="8cc31-121">Geometry blending (multimatrix vertex blending) requires that your application use a vertex format that has blending (beta) weights for each vertex.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc31-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cc31-122">Requirements</span></span>



| <span data-ttu-id="8cc31-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cc31-123">Requirement</span></span> | <span data-ttu-id="8cc31-124">Valor</span><span class="sxs-lookup"><span data-stu-id="8cc31-124">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc31-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8cc31-125">Header</span></span><br/> | <dl> <span data-ttu-id="8cc31-126"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cc31-126"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8cc31-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cc31-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cc31-128">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="8cc31-128">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="8cc31-129">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="8cc31-129">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)
</dt> <dt>

[<span data-ttu-id="8cc31-130">**D3DTS \_ World**</span><span class="sxs-lookup"><span data-stu-id="8cc31-130">**D3DTS\_WORLD**</span></span>](d3dts-world.md)
</dt> <dt>

[<span data-ttu-id="8cc31-131">**D3DTS \_ worldn**</span><span class="sxs-lookup"><span data-stu-id="8cc31-131">**D3DTS\_WORLDn**</span></span>](d3dts-worldn.md)
</dt> <dt>

[<span data-ttu-id="8cc31-132">**D3DTS \_ WORLDMATRIX**</span><span class="sxs-lookup"><span data-stu-id="8cc31-132">**D3DTS\_WORLDMATRIX**</span></span>](d3dts-worldmatrix.md)
</dt> </dl>

 

 
