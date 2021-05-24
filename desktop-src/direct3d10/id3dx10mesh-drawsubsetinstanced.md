---
description: Desenhe várias instâncias do mesmo subconjunto de uma malha.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: 'ID3DX10Mesh: método rawSubsetInstanced de:D (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubsetInstanced
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2e28d7a7d2c1d743090832d68793ec3743662308
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335630"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a><span data-ttu-id="3b283-103">ID3DX10Mesh: método rawSubsetInstanced de:D</span><span class="sxs-lookup"><span data-stu-id="3b283-103">ID3DX10Mesh::DrawSubsetInstanced method</span></span>

<span data-ttu-id="3b283-104">Desenhe várias instâncias do mesmo subconjunto de uma malha.</span><span class="sxs-lookup"><span data-stu-id="3b283-104">Draw several instances of the same subset of a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b283-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3b283-105">Syntax</span></span>


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a><span data-ttu-id="3b283-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b283-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b283-107">*Atribid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b283-107">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b283-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b283-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b283-109">Especifica qual subconjunto da malha deve ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="3b283-109">Specifies which subset of the mesh to draw.</span></span> <span data-ttu-id="3b283-110">Esse valor é usado para diferenciar faces em uma malha como pertencente a um ou mais grupos de atributos.</span><span class="sxs-lookup"><span data-stu-id="3b283-110">This value is used to differentiate faces in a mesh as belonging to one or more attribute groups.</span></span> <span data-ttu-id="3b283-111">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="3b283-111">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="3b283-112">*InstanceCount* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b283-112">*InstanceCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b283-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b283-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b283-114">Número de instâncias a serem renderizadas.</span><span class="sxs-lookup"><span data-stu-id="3b283-114">Number of instances to render.</span></span>

</dd> <dt>

<span data-ttu-id="3b283-115">*StartInstanceLocation* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3b283-115">*StartInstanceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b283-116">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3b283-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3b283-117">A qual instância iniciar a busca em cada buffer marcado como dados de instância.</span><span class="sxs-lookup"><span data-stu-id="3b283-117">Which instance to start fetching from in each buffer marked as instance data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b283-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3b283-118">Return value</span></span>

<span data-ttu-id="3b283-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b283-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b283-120">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="3b283-120">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3b283-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b283-121">Remarks</span></span>

<span data-ttu-id="3b283-122">Uma malha contém uma tabela de atributos.</span><span class="sxs-lookup"><span data-stu-id="3b283-122">A mesh contains an attribute table.</span></span> <span data-ttu-id="3b283-123">A tabela de atributos pode dividir uma malha em subconjuntos, onde cada subconjunto é identificado com uma ID de atributo.</span><span class="sxs-lookup"><span data-stu-id="3b283-123">The attribute table can divide a mesh into subsets, where each subset is identified with an attribute ID.</span></span> <span data-ttu-id="3b283-124">Por exemplo, uma malha com 200 rostos, dividida em três subconjuntos, pode ter uma tabela de atributos parecida com esta:</span><span class="sxs-lookup"><span data-stu-id="3b283-124">For example, a mesh with 200 faces, divided into three subsets, might have an attribute table that looks like this:</span></span>



| <span data-ttu-id="3b283-125">Subset</span><span class="sxs-lookup"><span data-stu-id="3b283-125">Subset</span></span>     | <span data-ttu-id="3b283-126">Faces</span><span class="sxs-lookup"><span data-stu-id="3b283-126">Faces</span></span>           |
|------------|-----------------|
| <span data-ttu-id="3b283-127">AttribId 0</span><span class="sxs-lookup"><span data-stu-id="3b283-127">AttribID 0</span></span> | <span data-ttu-id="3b283-128">Faces 0 ~ 50</span><span class="sxs-lookup"><span data-stu-id="3b283-128">Faces 0 ~ 50</span></span>    |
| <span data-ttu-id="3b283-129">AttribID 1</span><span class="sxs-lookup"><span data-stu-id="3b283-129">AttribID 1</span></span> | <span data-ttu-id="3b283-130">Faces 51 ~ 125</span><span class="sxs-lookup"><span data-stu-id="3b283-130">Faces 51 ~ 125</span></span>  |
| <span data-ttu-id="3b283-131">AttribID 2</span><span class="sxs-lookup"><span data-stu-id="3b283-131">AttribID 2</span></span> | <span data-ttu-id="3b283-132">Faces 126 ~ 200</span><span class="sxs-lookup"><span data-stu-id="3b283-132">Faces 126 ~ 200</span></span> |



 

<span data-ttu-id="3b283-133">O instanciamento pode estender o desempenho reutilização da mesma geometria para desenhar vários objetos em uma cena.</span><span class="sxs-lookup"><span data-stu-id="3b283-133">Instancing may extend performance by reusing the same geometry to draw multiple objects in a scene.</span></span> <span data-ttu-id="3b283-134">Um exemplo de instanciamento pode ser desenhar o mesmo objeto com diferentes posições e cores.</span><span class="sxs-lookup"><span data-stu-id="3b283-134">One example of instancing could be to draw the same object with different positions and colors.</span></span> <span data-ttu-id="3b283-135">A indexação requer vários buffers de vértice: pelo menos um para dados por vértice e um segundo buffer para dados por instância.</span><span class="sxs-lookup"><span data-stu-id="3b283-135">Indexing requires multiple vertex buffers: at least one for per-vertex data and a second buffer for per-instance data.</span></span>

<span data-ttu-id="3b283-136">As instâncias de desenho com DrawSubsetInstanced são muito semelhantes ao processo usado com [**ID3D10Device::D rawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) descrito em [Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="3b283-136">Drawing instances with DrawSubsetInstanced is very similar to the process used with [**ID3D10Device::DrawIndexedInstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) that is outlined in [Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx).</span></span> <span data-ttu-id="3b283-137">A principal diferença ao usar DrawSubsetInstanced é que os buffers de vértice e índice devem ser extraídos do objeto [**interface ID3DX10Mesh**](id3dx10mesh.md) antes que os dados de instanciação possam ser combinados.</span><span class="sxs-lookup"><span data-stu-id="3b283-137">The key difference when using DrawSubsetInstanced is that vertex and index buffers must be extracted from the [**ID3DX10Mesh Interface**](id3dx10mesh.md) object before the instancing data can be combined.</span></span>

<span data-ttu-id="3b283-138">O código a seguir ilustra a extração dos buffers de vértice e índice do objeto de malha.</span><span class="sxs-lookup"><span data-stu-id="3b283-138">The following code illustrates extracting the vertex and index buffers from the mesh object.</span></span>


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



## <a name="requirements"></a><span data-ttu-id="3b283-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b283-139">Requirements</span></span>



| <span data-ttu-id="3b283-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b283-140">Requirement</span></span> | <span data-ttu-id="3b283-141">Valor</span><span class="sxs-lookup"><span data-stu-id="3b283-141">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b283-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b283-142">Header</span></span><br/>  | <dl> <span data-ttu-id="3b283-143"><dt>D3DX10.h</dt></span><span class="sxs-lookup"><span data-stu-id="3b283-143"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b283-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3b283-144">Library</span></span><br/> | <dl> <span data-ttu-id="3b283-145"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b283-145"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b283-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b283-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b283-147">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="3b283-147">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="3b283-148">D3DX Interfaces</span><span class="sxs-lookup"><span data-stu-id="3b283-148">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
