---
description: Descreve um patch de ordem superior triangular.
ms.assetid: 3f97120b-3b32-4f95-8614-7b263ff330db
title: Estrutura de D3DTRIPATCH_INFO (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRIPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b910d38025c44d6157a76aa3e3425ba46d628787
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105780303"
---
# <a name="d3dtripatch_info-structure"></a><span data-ttu-id="d6032-103">Estrutura de informações do D3DTRIPATCH \_</span><span class="sxs-lookup"><span data-stu-id="d6032-103">D3DTRIPATCH\_INFO structure</span></span>

<span data-ttu-id="d6032-104">Descreve um patch de ordem superior triangular.</span><span class="sxs-lookup"><span data-stu-id="d6032-104">Describes a triangular high-order patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6032-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6032-105">Syntax</span></span>


```C++
typedef struct D3DTRIPATCH_INFO {
  UINT          StartVertexOffset;
  UINT          NumVertices;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DTRIPATCH_INFO, *LPD3DTRIPATCH_INFO;
```



## <a name="members"></a><span data-ttu-id="d6032-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d6032-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d6032-107">**StartVertexOffset**</span><span class="sxs-lookup"><span data-stu-id="d6032-107">**StartVertexOffset**</span></span>
</dt> <dd>

<span data-ttu-id="d6032-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6032-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d6032-109">Iniciando deslocamento de vértice, em número de vértices.</span><span class="sxs-lookup"><span data-stu-id="d6032-109">Starting vertex offset, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d6032-110">**NumVertices**</span><span class="sxs-lookup"><span data-stu-id="d6032-110">**NumVertices**</span></span>
</dt> <dd>

<span data-ttu-id="d6032-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d6032-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d6032-112">Número de vértices.</span><span class="sxs-lookup"><span data-stu-id="d6032-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d6032-113">**Base**</span><span class="sxs-lookup"><span data-stu-id="d6032-113">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="d6032-114">Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="d6032-114">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d6032-115">Membro do tipo enumerado [**D3DBASISTYPE**](./d3dbasistype.md) , que define o tipo base para o patch de ordem superior triangular.</span><span class="sxs-lookup"><span data-stu-id="d6032-115">Member of the [**D3DBASISTYPE**](./d3dbasistype.md) enumerated type, which defines the basis type for the triangular high-order patch.</span></span> <span data-ttu-id="d6032-116">O único valor válido para esse membro é D3DBASIS \_ BEZIER.</span><span class="sxs-lookup"><span data-stu-id="d6032-116">The only valid value for this member is D3DBASIS\_BEZIER.</span></span>

</dd> <dt>

<span data-ttu-id="d6032-117">**Grau**</span><span class="sxs-lookup"><span data-stu-id="d6032-117">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="d6032-118">Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="d6032-118">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d6032-119">Membro do tipo enumerado [**D3DDEGREETYPE**](./d3ddegreetype.md) , definindo o tipo de grau para o patch de ordem superior triangular.</span><span class="sxs-lookup"><span data-stu-id="d6032-119">Member of the [**D3DDEGREETYPE**](./d3ddegreetype.md) enumerated type, defining the degree type for the triangular high-order patch.</span></span>



| <span data-ttu-id="d6032-120">Valor</span><span class="sxs-lookup"><span data-stu-id="d6032-120">Value</span></span>                | <span data-ttu-id="d6032-121">Número de vértices</span><span class="sxs-lookup"><span data-stu-id="d6032-121">Number of vertices</span></span> |
|----------------------|--------------------|
| <span data-ttu-id="d6032-122">D3DDEGREE \_ cúbico</span><span class="sxs-lookup"><span data-stu-id="d6032-122">D3DDEGREE\_CUBIC</span></span>     | <span data-ttu-id="d6032-123">10</span><span class="sxs-lookup"><span data-stu-id="d6032-123">10</span></span>                 |
| <span data-ttu-id="d6032-124">D3DDEGREE \_ linear</span><span class="sxs-lookup"><span data-stu-id="d6032-124">D3DDEGREE\_LINEAR</span></span>    | <span data-ttu-id="d6032-125">3</span><span class="sxs-lookup"><span data-stu-id="d6032-125">3</span></span>                  |
| <span data-ttu-id="d6032-126">D3DDEGREE \_ quadrática</span><span class="sxs-lookup"><span data-stu-id="d6032-126">D3DDEGREE\_QUADRATIC</span></span> | <span data-ttu-id="d6032-127">N/D</span><span class="sxs-lookup"><span data-stu-id="d6032-127">N/A</span></span>                |
| <span data-ttu-id="d6032-128">D3DDEGREE \_ QUINTIC</span><span class="sxs-lookup"><span data-stu-id="d6032-128">D3DDEGREE\_QUINTIC</span></span>   | <span data-ttu-id="d6032-129">21</span><span class="sxs-lookup"><span data-stu-id="d6032-129">21</span></span>                 |



 

<span data-ttu-id="d6032-130">N/A-não disponível.</span><span class="sxs-lookup"><span data-stu-id="d6032-130">N/A - Not available.</span></span> <span data-ttu-id="d6032-131">Não há suporte.</span><span class="sxs-lookup"><span data-stu-id="d6032-131">Not supported.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d6032-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6032-132">Remarks</span></span>

<span data-ttu-id="d6032-133">Por exemplo, o diagrama a seguir identifica a ordem de vértice e os números de segmento para um patch de triângulo Bézier cúbico.</span><span class="sxs-lookup"><span data-stu-id="d6032-133">For example, the following diagram identifies the vertex order and segment numbers for a cubic Bézier triangle patch.</span></span> <span data-ttu-id="d6032-134">A ordem de vértice determina os números de segmento usados pelo [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch).</span><span class="sxs-lookup"><span data-stu-id="d6032-134">The vertex order determines the segment numbers used by [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch).</span></span> <span data-ttu-id="d6032-135">O deslocamento é o número de bytes para o primeiro vértice de patch de triângulo no buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="d6032-135">The offset is the number of bytes to the first triangle patch vertex in the vertex buffer.</span></span>

![diagrama de um patch de ordem superior triangular com nove vértices](images/hop-tripatch-info.png)

## <a name="requirements"></a><span data-ttu-id="d6032-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6032-137">Requirements</span></span>



| <span data-ttu-id="d6032-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6032-138">Requirement</span></span> | <span data-ttu-id="d6032-139">Valor</span><span class="sxs-lookup"><span data-stu-id="d6032-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6032-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6032-140">Header</span></span><br/> | <dl> <span data-ttu-id="d6032-141"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6032-141"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6032-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6032-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6032-143">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="d6032-143">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="d6032-144">**DrawTriPatch**</span><span class="sxs-lookup"><span data-stu-id="d6032-144">**DrawTriPatch**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch)
</dt> <dt>

[<span data-ttu-id="d6032-145">**D3DXTessellateTriPatch**</span><span class="sxs-lookup"><span data-stu-id="d6032-145">**D3DXTessellateTriPatch**</span></span>](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
