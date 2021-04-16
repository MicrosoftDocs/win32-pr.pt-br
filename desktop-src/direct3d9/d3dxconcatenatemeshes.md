---
description: Concatena um grupo de malhas em uma malha comum. Esse método pode, opcionalmente, aplicar uma transformação de matriz para cada malha de entrada e suas coordenadas de textura.
ms.assetid: 0f2af63a-ece5-4c99-8cb8-045099eca3ea
title: Função D3DXConcatenateMeshes (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConcatenateMeshes
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b96fe47a3d818c382b35a93708ac51b60e891841
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765584"
---
# <a name="d3dxconcatenatemeshes-function"></a><span data-ttu-id="3bb79-104">Função D3DXConcatenateMeshes</span><span class="sxs-lookup"><span data-stu-id="3bb79-104">D3DXConcatenateMeshes function</span></span>

<span data-ttu-id="3bb79-105">Concatena um grupo de malhas em uma malha comum.</span><span class="sxs-lookup"><span data-stu-id="3bb79-105">Concatenates a group of meshes into one common mesh.</span></span> <span data-ttu-id="3bb79-106">Esse método pode, opcionalmente, aplicar uma transformação de matriz para cada malha de entrada e suas coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="3bb79-106">This method can optionally apply a matrix transformation to each input mesh and its texture coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="3bb79-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3bb79-107">Syntax</span></span>


```C++
HRESULT D3DXConcatenateMeshes(
  _In_        LPD3DXMESH        *ppMeshes,
  _In_        UINT              NumMeshes,
  _In_        DWORD             Options,
  _In_  const D3DXMATRIX        *pGeomXForms,
  _In_  const D3DXMATRIX        *pTextureXForms,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXMESH        *ppMeshOut
);
```



## <a name="parameters"></a><span data-ttu-id="3bb79-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3bb79-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bb79-109">*ppMeshes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3bb79-109">*ppMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb79-110">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="3bb79-110">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="3bb79-111">Matriz de ponteiros de malha de entrada (consulte [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="3bb79-111">Array of input mesh pointers (see [**ID3DXMesh**](id3dxmesh.md)).</span></span> <span data-ttu-id="3bb79-112">O número de elementos na matriz é NumMeshes.</span><span class="sxs-lookup"><span data-stu-id="3bb79-112">The number of elements in the array is NumMeshes.</span></span>

</dd> <dt>

<span data-ttu-id="3bb79-113">*NumMeshes* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3bb79-113">*NumMeshes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb79-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bb79-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3bb79-115">Número de malhas de entrada a serem concatenadas.</span><span class="sxs-lookup"><span data-stu-id="3bb79-115">Number of input meshes to concatenate.</span></span>

</dd> <dt>

<span data-ttu-id="3bb79-116">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3bb79-116">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb79-117">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3bb79-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3bb79-118">Opções de criação de malha; Essa é uma combinação de um ou mais sinalizadores [**D3DXMESH**](./d3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="3bb79-118">Mesh creation options; this is a combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags.</span></span> <span data-ttu-id="3bb79-119">As opções de criação de malha são equivalentes ao parâmetro options exigido por [**D3DXCreateMesh**](d3dxcreatemesh.md).</span><span class="sxs-lookup"><span data-stu-id="3bb79-119">The mesh creation options are equivalent to the options parameter required by [**D3DXCreateMesh**](d3dxcreatemesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="3bb79-120">*pGeomXForms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3bb79-120">*pGeomXForms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb79-121">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3bb79-121">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3bb79-122">Matriz opcional de transformações de geometria.</span><span class="sxs-lookup"><span data-stu-id="3bb79-122">Optional array of geometry transforms.</span></span> <span data-ttu-id="3bb79-123">O número de elementos na matriz é NumMeshes; cada elemento é uma matriz de transformação (consulte [**D3DXMATRIX**](d3dxmatrix.md)).</span><span class="sxs-lookup"><span data-stu-id="3bb79-123">The number of elements in the array is NumMeshes; each element is a transformation matrix (see [**D3DXMATRIX**](d3dxmatrix.md)).</span></span> <span data-ttu-id="3bb79-124">Pode ser **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3bb79-124">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3bb79-125">*pTextureXForms* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3bb79-125">*pTextureXForms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb79-126">Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3bb79-126">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="3bb79-127">Matriz opcional de transformações de textura.</span><span class="sxs-lookup"><span data-stu-id="3bb79-127">Optional array of texture transforms.</span></span> <span data-ttu-id="3bb79-128">O número de elementos na matriz é NumMeshes; cada elemento é uma matriz de transformação (consulte [**D3DXMATRIX**](d3dxmatrix.md)).</span><span class="sxs-lookup"><span data-stu-id="3bb79-128">The number of elements in the array is NumMeshes; each element is a transformation matrix (see [**D3DXMATRIX**](d3dxmatrix.md)).</span></span> <span data-ttu-id="3bb79-129">Esse parâmetro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3bb79-129">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3bb79-130">*pDecl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3bb79-130">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb79-131">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="3bb79-131">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="3bb79-132">Ponteiro opcional para uma declaração de vértice (consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)).</span><span class="sxs-lookup"><span data-stu-id="3bb79-132">Optional pointer to a vertex declaration (see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)).</span></span> <span data-ttu-id="3bb79-133">Esse parâmetro pode ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="3bb79-133">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3bb79-134">*pD3DDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3bb79-134">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb79-135">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="3bb79-135">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="3bb79-136">Ponteiro para um dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que é usado para criar a nova malha.</span><span class="sxs-lookup"><span data-stu-id="3bb79-136">Pointer to a [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) device that is used to create the new mesh.</span></span>

</dd> <dt>

<span data-ttu-id="3bb79-137">*ppMeshOut* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="3bb79-137">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3bb79-138">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="3bb79-138">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="3bb79-139">Endereço de um ponteiro para a malha criada (consulte [**ID3DXMesh**](id3dxmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="3bb79-139">Address of a pointer to the mesh created (see [**ID3DXMesh**](id3dxmesh.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bb79-140">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3bb79-140">Return value</span></span>

<span data-ttu-id="3bb79-141">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3bb79-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3bb79-142">Se a função for bem sucedido, o valor de retorno será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3bb79-142">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3bb79-143">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="3bb79-143">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3bb79-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bb79-144">Remarks</span></span>

<span data-ttu-id="3bb79-145">Se nenhuma [declaração de vértice](vertex-declaration.md) for fornecida como parte do parâmetro de criação de malha de opções, o método irá gerar uma União de todas as declarações de vértice das submalhas, promovendo canais e tipos, se necessário.</span><span class="sxs-lookup"><span data-stu-id="3bb79-145">If no [vertex declaration](vertex-declaration.md) is given as part of the Options mesh creation parameter, the method will generate a union of all of the vertex declarations of the submeshes, promoting channels and types if necessary.</span></span> <span data-ttu-id="3bb79-146">O método criará uma tabela de atributos de tabelas de atributos das malhas de entrada.</span><span class="sxs-lookup"><span data-stu-id="3bb79-146">The method will create an attribute table from attribute tables of the input meshes.</span></span> <span data-ttu-id="3bb79-147">Para garantir a criação de uma tabela de atributos, chame [**Optimize**](id3dxmesh--optimize.md) com flags definido como D3DXMESHOPT \_ Compact e D3DXMESHOPT \_ ATTRSORT (consulte [**D3DXMESHOPT**](./d3dxmeshopt.md)).</span><span class="sxs-lookup"><span data-stu-id="3bb79-147">To ensure creation of an attribute table, call [**Optimize**](id3dxmesh--optimize.md) with Flags set to D3DXMESHOPT\_COMPACT and D3DXMESHOPT\_ATTRSORT (see [**D3DXMESHOPT**](./d3dxmeshopt.md)).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bb79-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3bb79-148">Requirements</span></span>



| <span data-ttu-id="3bb79-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="3bb79-149">Requirement</span></span> | <span data-ttu-id="3bb79-150">Valor</span><span class="sxs-lookup"><span data-stu-id="3bb79-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bb79-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3bb79-151">Header</span></span><br/>  | <dl> <span data-ttu-id="3bb79-152"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="3bb79-152"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="3bb79-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3bb79-153">Library</span></span><br/> | <dl> <span data-ttu-id="3bb79-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3bb79-154"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3bb79-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="3bb79-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bb79-156">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="3bb79-156">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
