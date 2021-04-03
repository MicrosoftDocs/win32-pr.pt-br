---
description: Define o tipo base de uma superfície de patch de ordem superior.
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: Enumeração D3DBASISTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBASISTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7e166f56aa2625c868d3e2e2223efbb577e05bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104091949"
---
# <a name="d3dbasistype-enumeration"></a><span data-ttu-id="dd68b-103">Enumeração D3DBASISTYPE</span><span class="sxs-lookup"><span data-stu-id="dd68b-103">D3DBASISTYPE enumeration</span></span>

<span data-ttu-id="dd68b-104">Define o tipo base de uma superfície de patch de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="dd68b-104">Defines the basis type of a high-order patch surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd68b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd68b-105">Syntax</span></span>


```C++
typedef enum D3DBASISTYPE { 
  D3DBASIS_BEZIER       = 0,
  D3DBASIS_BSPLINE      = 1,
  D3DBASIS_CATMULL_ROM  = 2,
  D3DBASIS_FORCE_DWORD  = 0x7fffffff
} D3DBASISTYPE, *LPD3DBASISTYPE;
```



## <a name="constants"></a><span data-ttu-id="dd68b-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="dd68b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dd68b-107"><span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**\_BEZIER D3DBASIS**</span><span class="sxs-lookup"><span data-stu-id="dd68b-107"><span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS\_BEZIER**</span></span>
</dt> <dd>

<span data-ttu-id="dd68b-108">Os vértices de entrada são tratados como uma série de patches de Bézier.</span><span class="sxs-lookup"><span data-stu-id="dd68b-108">Input vertices are treated as a series of Bézier patches.</span></span> <span data-ttu-id="dd68b-109">O número de vértices especificado deve ser divisível por 4.</span><span class="sxs-lookup"><span data-stu-id="dd68b-109">The number of vertices specified must be divisible by 4.</span></span> <span data-ttu-id="dd68b-110">Partes da malha além desse critério não serão renderizadas.</span><span class="sxs-lookup"><span data-stu-id="dd68b-110">Portions of the mesh beyond this criterion will not be rendered.</span></span> <span data-ttu-id="dd68b-111">A continuidade completa é presumida entre os subpatches no interior da superfície renderizada por cada chamada.</span><span class="sxs-lookup"><span data-stu-id="dd68b-111">Full continuity is assumed between sub-patches in the interior of the surface rendered by each call.</span></span> <span data-ttu-id="dd68b-112">Somente os vértices nos cantos de cada subpatch têm a garantia de estar na superfície resultante.</span><span class="sxs-lookup"><span data-stu-id="dd68b-112">Only the vertices at the corners of each sub-patch are guaranteed to lie on the resulting surface.</span></span>

</dd> <dt>

<span data-ttu-id="dd68b-113"><span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS \_ BSPLINE**</span><span class="sxs-lookup"><span data-stu-id="dd68b-113"><span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**D3DBASIS\_BSPLINE**</span></span>
</dt> <dd>

<span data-ttu-id="dd68b-114">Os vértices de entrada são tratados como pontos de controle de uma superfície B-spline.</span><span class="sxs-lookup"><span data-stu-id="dd68b-114">Input vertices are treated as control points of a B-spline surface.</span></span> <span data-ttu-id="dd68b-115">O número de aberturas renderizadas é de dois a menos do que o número de aberturas nessa direção.</span><span class="sxs-lookup"><span data-stu-id="dd68b-115">The number of apertures rendered is two fewer than the number of apertures in that direction.</span></span> <span data-ttu-id="dd68b-116">Em geral, a superfície gerada não contém os vértices de controle especificados.</span><span class="sxs-lookup"><span data-stu-id="dd68b-116">In general, the generated surface does not contain the control vertices specified.</span></span>

</dd> <dt>

<span data-ttu-id="dd68b-117"><span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS \_ CATMULL \_ ROM**</span><span class="sxs-lookup"><span data-stu-id="dd68b-117"><span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS\_CATMULL\_ROM**</span></span>
</dt> <dd>

<span data-ttu-id="dd68b-118">Uma base de interpolação define a superfície de forma que a superfície percorra todos os vértices de entrada especificados.</span><span class="sxs-lookup"><span data-stu-id="dd68b-118">An interpolating basis defines the surface so that the surface goes through all the input vertices specified.</span></span> <span data-ttu-id="dd68b-119">No DirectX 8, essa era D3DBASIS \_ interpolação.</span><span class="sxs-lookup"><span data-stu-id="dd68b-119">In DirectX 8, this was D3DBASIS\_INTERPOLATE.</span></span>

</dd> <dt>

<span data-ttu-id="dd68b-120"><span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="dd68b-120"><span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="dd68b-121">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="dd68b-121">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="dd68b-122">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dd68b-122">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="dd68b-123">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="dd68b-123">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd68b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd68b-124">Remarks</span></span>

<span data-ttu-id="dd68b-125">Os membros de **D3DBASISTYPE** especificam a formulação a ser usada na avaliação do primitivo de superfície de patch de ordem superior durante o mosaico.</span><span class="sxs-lookup"><span data-stu-id="dd68b-125">The members of **D3DBASISTYPE** specify the formulation to be used in evaluating the high-order patch surface primitive during tessellation.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd68b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dd68b-126">Requirements</span></span>



| <span data-ttu-id="dd68b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="dd68b-127">Requirement</span></span> | <span data-ttu-id="dd68b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="dd68b-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd68b-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dd68b-129">Header</span></span><br/> | <dl> <span data-ttu-id="dd68b-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd68b-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd68b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd68b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd68b-132">Enumerações do Direct3D</span><span class="sxs-lookup"><span data-stu-id="dd68b-132">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="dd68b-133">**Informações de D3DRECTPATCH \_**</span><span class="sxs-lookup"><span data-stu-id="dd68b-133">**D3DRECTPATCH\_INFO**</span></span>](d3drectpatch-info.md)
</dt> <dt>

[<span data-ttu-id="dd68b-134">**Informações de D3DTRIPATCH \_**</span><span class="sxs-lookup"><span data-stu-id="dd68b-134">**D3DTRIPATCH\_INFO**</span></span>](d3dtripatch-info.md)
</dt> </dl>

 

 




