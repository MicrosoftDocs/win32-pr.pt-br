---
description: Descreve um patch de ordem superior retangular.
ms.assetid: 5f195009-d047-4dc0-a386-e1a434914e34
title: Estrutura de D3DRECTPATCH_INFO (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRECTPATCH_INFO
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: a2b7fedbaac2cc9c204d4691828d31794cea1f47
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761257"
---
# <a name="d3drectpatch_info-structure"></a><span data-ttu-id="98306-103">Estrutura de informações do D3DRECTPATCH \_</span><span class="sxs-lookup"><span data-stu-id="98306-103">D3DRECTPATCH\_INFO structure</span></span>

<span data-ttu-id="98306-104">Descreve um patch de ordem superior retangular.</span><span class="sxs-lookup"><span data-stu-id="98306-104">Describes a rectangular high-order patch.</span></span>

## <a name="syntax"></a><span data-ttu-id="98306-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="98306-105">Syntax</span></span>


```C++
typedef struct D3DRECTPATCH_INFO {
  UINT          StartVertexOffsetWidth;
  UINT          StartVertexOffsetHeight;
  UINT          Width;
  UINT          Height;
  UINT          Stride;
  D3DBASISTYPE  Basis;
  D3DDEGREETYPE Degree;
} D3DRECTPATCH_INFO, *LPD3DRECTPATCH_INFO;
```



## <a name="members"></a><span data-ttu-id="98306-106">Membros</span><span class="sxs-lookup"><span data-stu-id="98306-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="98306-107">**StartVertexOffsetWidth**</span><span class="sxs-lookup"><span data-stu-id="98306-107">**StartVertexOffsetWidth**</span></span>
</dt> <dd>

<span data-ttu-id="98306-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98306-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="98306-109">Iniciando a largura de deslocamento do vértice, em número de vértices.</span><span class="sxs-lookup"><span data-stu-id="98306-109">Starting vertex offset width, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="98306-110">**StartVertexOffsetHeight**</span><span class="sxs-lookup"><span data-stu-id="98306-110">**StartVertexOffsetHeight**</span></span>
</dt> <dd>

<span data-ttu-id="98306-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98306-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="98306-112">Iniciando a altura de deslocamento do vértice, em número de vértices.</span><span class="sxs-lookup"><span data-stu-id="98306-112">Starting vertex offset height, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="98306-113">**Largura**</span><span class="sxs-lookup"><span data-stu-id="98306-113">**Width**</span></span>
</dt> <dd>

<span data-ttu-id="98306-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98306-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="98306-115">Largura de cada vértice, em número de vértices.</span><span class="sxs-lookup"><span data-stu-id="98306-115">Width of each vertex, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="98306-116">**Altura**</span><span class="sxs-lookup"><span data-stu-id="98306-116">**Height**</span></span>
</dt> <dd>

<span data-ttu-id="98306-117">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98306-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="98306-118">Altura de cada vértice, em número de vértices.</span><span class="sxs-lookup"><span data-stu-id="98306-118">Height of each vertex, in number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="98306-119">**Passo**</span><span class="sxs-lookup"><span data-stu-id="98306-119">**Stride**</span></span>
</dt> <dd>

<span data-ttu-id="98306-120">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="98306-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="98306-121">Largura da matriz de vértices imaginários bidimensionais, que ocupa o mesmo espaço que o buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="98306-121">Width of the imaginary two-dimensional vertex array, which occupies the same space as the vertex buffer.</span></span> <span data-ttu-id="98306-122">Para obter um exemplo, consulte o diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="98306-122">For an example, see the diagram below.</span></span>

</dd> <dt>

<span data-ttu-id="98306-123">**Base**</span><span class="sxs-lookup"><span data-stu-id="98306-123">**Basis**</span></span>
</dt> <dd>

<span data-ttu-id="98306-124">Tipo: **[ **D3DBASISTYPE**](./d3dbasistype.md)**</span><span class="sxs-lookup"><span data-stu-id="98306-124">Type: **[**D3DBASISTYPE**](./d3dbasistype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="98306-125">Membro do tipo enumerado [**D3DBASISTYPE**](./d3dbasistype.md) , definindo o tipo base para o patch de ordem superior retangular.</span><span class="sxs-lookup"><span data-stu-id="98306-125">Member of the [**D3DBASISTYPE**](./d3dbasistype.md) enumerated type, defining the basis type for the rectangular high-order patch.</span></span>



| <span data-ttu-id="98306-126">Valor</span><span class="sxs-lookup"><span data-stu-id="98306-126">Value</span></span>                 | <span data-ttu-id="98306-127">Pedido com suporte</span><span class="sxs-lookup"><span data-stu-id="98306-127">Order supported</span></span>            | <span data-ttu-id="98306-128">Largura e altura</span><span class="sxs-lookup"><span data-stu-id="98306-128">Width and height</span></span>                  |
|-----------------------|----------------------------|-----------------------------------|
| <span data-ttu-id="98306-129">\_BEZIER D3DBASIS</span><span class="sxs-lookup"><span data-stu-id="98306-129">D3DBASIS\_BEZIER</span></span>      | <span data-ttu-id="98306-130">Linear, cúbica e QUINTIC</span><span class="sxs-lookup"><span data-stu-id="98306-130">Linear, cubic, and quintic</span></span> | <span data-ttu-id="98306-131">Width = altura = (DWORD) ordem + 1</span><span class="sxs-lookup"><span data-stu-id="98306-131">Width = height = (DWORD)order + 1</span></span> |
| <span data-ttu-id="98306-132">D3DBASIS \_ BSPLINE</span><span class="sxs-lookup"><span data-stu-id="98306-132">D3DBASIS\_BSPLINE</span></span>     | <span data-ttu-id="98306-133">Linear, cúbica e QUINTIC</span><span class="sxs-lookup"><span data-stu-id="98306-133">Linear, cubic, and quintic</span></span> | <span data-ttu-id="98306-134">Largura = altura > (DWORD) ordem</span><span class="sxs-lookup"><span data-stu-id="98306-134">Width = height > (DWORD)order</span></span>  |
| <span data-ttu-id="98306-135">\_Interpolação de D3DBASIS</span><span class="sxs-lookup"><span data-stu-id="98306-135">D3DBASIS\_INTERPOLATE</span></span> | <span data-ttu-id="98306-136">Baias</span><span class="sxs-lookup"><span data-stu-id="98306-136">Cubic</span></span>                      | <span data-ttu-id="98306-137">Largura = altura > (DWORD) ordem</span><span class="sxs-lookup"><span data-stu-id="98306-137">Width = height > (DWORD)order</span></span>  |



 

</dd> <dt>

<span data-ttu-id="98306-138">**Grau**</span><span class="sxs-lookup"><span data-stu-id="98306-138">**Degree**</span></span>
</dt> <dd>

<span data-ttu-id="98306-139">Tipo: **[ **D3DDEGREETYPE**](./d3ddegreetype.md)**</span><span class="sxs-lookup"><span data-stu-id="98306-139">Type: **[**D3DDEGREETYPE**](./d3ddegreetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="98306-140">Membro do tipo enumerado [**D3DDEGREETYPE**](./d3ddegreetype.md) , definindo o grau para o patch retangular.</span><span class="sxs-lookup"><span data-stu-id="98306-140">Member of the [**D3DDEGREETYPE**](./d3ddegreetype.md) enumerated type, defining the degree for the rectangular patch.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98306-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="98306-141">Remarks</span></span>

<span data-ttu-id="98306-142">O diagrama a seguir identifica os parâmetros que especificam um patch de retângulo.</span><span class="sxs-lookup"><span data-stu-id="98306-142">The following diagram identifies the parameters that specify a rectangle patch.</span></span>

![diagrama de um patch de ordem superior retangular e os parâmetros que o especificam](images/hop-rectpatch.png)

<span data-ttu-id="98306-144">Cada um dos vértices no buffer de vértice é mostrado como um ponto preto.</span><span class="sxs-lookup"><span data-stu-id="98306-144">Each of the vertices in the vertex buffer is shown as a black dot.</span></span> <span data-ttu-id="98306-145">Nesse caso, o buffer de vértice tem 20 vértices, 16 dos quais estão no patch de retângulo.</span><span class="sxs-lookup"><span data-stu-id="98306-145">In this case, the vertex buffer has 20 vertices in it, 16 of which are in the rectangle patch.</span></span> <span data-ttu-id="98306-146">O stride é o número de vértices na largura do buffer de vértice, neste caso, cinco.</span><span class="sxs-lookup"><span data-stu-id="98306-146">The stride is the number of vertices in the width of the vertex buffer, in this case five.</span></span> <span data-ttu-id="98306-147">O deslocamento x para o primeiro vértice é chamado de StartIndexVertexWidth e, nesse caso, 1.</span><span class="sxs-lookup"><span data-stu-id="98306-147">The x offset to the first vertex is called the StartIndexVertexWidth and is in this case 1.</span></span> <span data-ttu-id="98306-148">O deslocamento y para o primeiro vértice do patch é chamado de StartIndexVertexHeight e, nesse caso, 0.</span><span class="sxs-lookup"><span data-stu-id="98306-148">The y offset to the first patch vertex is called the StartIndexVertexHeight and is in this case 0.</span></span>

<span data-ttu-id="98306-149">Para renderizar um fluxo de patches retangulares individuais (não-mosaico), você deve interpretar a geometria como um patch retangular longo estreito (1 x N).</span><span class="sxs-lookup"><span data-stu-id="98306-149">To render a stream of individual rectangular patches (non-mosaic), you should interpret your geometry as a long narrow (1 x N) rectangular patch.</span></span> <span data-ttu-id="98306-150">A estrutura de **\_ informações de D3DRECTPATCH** para tal faixa (Bézier cúbica) seria configurada da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="98306-150">The **D3DRECTPATCH\_INFO** structure for such a strip (cubic Bézier) would be set up in the following manner.</span></span>


```
    
D3DRECTPATCH_INFO RectInfo;

RectInfo.Width = 4;
RectInfo.Height = 4;
RectInfo.Stride = 4;
RectInfo.Basis = D3DBASIS_BEZIER;
RectInfo.Order = D3DORDER_CUBIC;
RectInfo.StartVertexOffsetWidth = 0;
RectInfo.StartVertexOffsetHeight = 4*i;  // The variable i is the index of the 
//   patch you want to render.
```



## <a name="requirements"></a><span data-ttu-id="98306-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98306-151">Requirements</span></span>



| <span data-ttu-id="98306-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="98306-152">Requirement</span></span> | <span data-ttu-id="98306-153">Valor</span><span class="sxs-lookup"><span data-stu-id="98306-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98306-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="98306-154">Header</span></span><br/> | <dl> <span data-ttu-id="98306-155"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="98306-155"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98306-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="98306-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98306-157">Estruturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="98306-157">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="98306-158">**DrawRectPatch**</span><span class="sxs-lookup"><span data-stu-id="98306-158">**DrawRectPatch**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawrectpatch)
</dt> <dt>

[<span data-ttu-id="98306-159">**D3DXTessellateRectPatch**</span><span class="sxs-lookup"><span data-stu-id="98306-159">**D3DXTessellateRectPatch**</span></span>](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
