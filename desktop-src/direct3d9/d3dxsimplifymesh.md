---
description: Gera uma malha simplificada usando os pesos fornecidos que são o mais próximo possível do MinValue especificado.
ms.assetid: 589356a9-f272-4851-92ae-54dbecc0b234
title: Função D3DXSimplifyMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSimplifyMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0258047631a41e31d108ba45531988e4cb6a35ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105812273"
---
# <a name="d3dxsimplifymesh-function"></a><span data-ttu-id="31181-103">Função D3DXSimplifyMesh</span><span class="sxs-lookup"><span data-stu-id="31181-103">D3DXSimplifyMesh function</span></span>

<span data-ttu-id="31181-104">Gera uma malha simplificada usando os pesos fornecidos que são o mais próximo possível do MinValue especificado.</span><span class="sxs-lookup"><span data-stu-id="31181-104">Generates a simplified mesh using the provided weights that come as close as possible to the given MinValue.</span></span>

## <a name="syntax"></a><span data-ttu-id="31181-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31181-105">Syntax</span></span>


```C++
HRESULT D3DXSimplifyMesh(
  _In_        LPD3DXMESH           pMesh,
  _In_  const DWORD                *pAdjacency,
  _In_  const D3DXATTRIBUTEWEIGHTS *pVertexAttributeWeights,
  _In_  const FLOAT                *pVertexWeights,
  _In_        DWORD                MinValue,
  _In_        DWORD                Options,
  _Out_       LPD3DXMESH           *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="31181-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31181-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31181-107">*pMesh* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31181-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31181-108">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="31181-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="31181-109">Ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha de origem.</span><span class="sxs-lookup"><span data-stu-id="31181-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="31181-110">*pAdjacency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31181-110">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31181-111">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="31181-111">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31181-112">Ponteiro para uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha a ser simplificada.</span><span class="sxs-lookup"><span data-stu-id="31181-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be simplified.</span></span>

</dd> <dt>

<span data-ttu-id="31181-113">*pVertexAttributeWeights* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31181-113">*pVertexAttributeWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31181-114">Tipo: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) \***</span><span class="sxs-lookup"><span data-stu-id="31181-114">Type: **const [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md)\***</span></span>

<span data-ttu-id="31181-115">Ponteiro para uma estrutura [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) , que contém o peso de cada componente de vértice.</span><span class="sxs-lookup"><span data-stu-id="31181-115">Pointer to a [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) structure, containing the weight for each vertex component.</span></span> <span data-ttu-id="31181-116">Se esse parâmetro for definido como **NULL**, uma estrutura padrão será usada.</span><span class="sxs-lookup"><span data-stu-id="31181-116">If this parameter is set to **NULL**, a default structure is used.</span></span> <span data-ttu-id="31181-117">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="31181-117">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="31181-118">*pVertexWeights* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31181-118">*pVertexWeights* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31181-119">Tipo: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="31181-119">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="31181-120">Ponteiro para uma matriz de pesos de vértice.</span><span class="sxs-lookup"><span data-stu-id="31181-120">Pointer to an array of vertex weights.</span></span> <span data-ttu-id="31181-121">Se esse parâmetro for definido como **NULL**, todos os pesos de vértice serão definidos como 1,0.</span><span class="sxs-lookup"><span data-stu-id="31181-121">If this parameter is set to **NULL**, all vertex weights are set to 1.0.</span></span>

</dd> <dt>

<span data-ttu-id="31181-122">*MinValue* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31181-122">*MinValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31181-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31181-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31181-124">Número de vértices ou rostos, dependendo do sinalizador definido no parâmetro *Options* , por meio do qual simplificar a malha de origem.</span><span class="sxs-lookup"><span data-stu-id="31181-124">Number of vertices or faces, depending on the flag set in the *Options* parameter, by which to simplify the source mesh.</span></span>

</dd> <dt>

<span data-ttu-id="31181-125">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="31181-125">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31181-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="31181-126">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="31181-127">Especifica opções de simplificação para a malha.</span><span class="sxs-lookup"><span data-stu-id="31181-127">Specifies simplification options for the mesh.</span></span> <span data-ttu-id="31181-128">Um dos sinalizadores em [**D3DXMESHSIMP**](./d3dxmeshsimp.md) pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="31181-128">One of the flags in [**D3DXMESHSIMP**](./d3dxmeshsimp.md) can be set.</span></span>

</dd> <dt>

<span data-ttu-id="31181-129">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="31181-129">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31181-130">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="31181-130">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="31181-131">Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa a malha de simplificação retornada.</span><span class="sxs-lookup"><span data-stu-id="31181-131">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned simplification mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31181-132">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31181-132">Return value</span></span>

<span data-ttu-id="31181-133">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31181-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31181-134">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="31181-134">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="31181-135">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="31181-135">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="31181-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="31181-136">Remarks</span></span>

<span data-ttu-id="31181-137">Essa função gera uma malha que tem vértices de *MinValue* ou rostos.</span><span class="sxs-lookup"><span data-stu-id="31181-137">This function generates a mesh that has *MinValue* vertices or faces.</span></span>

<span data-ttu-id="31181-138">Se o processo de simplificação não puder reduzir a malha para *MinValue*, a chamada ainda terá sucesso porque *MinValue* é um mínimo desejado, não um mínimo absoluto.</span><span class="sxs-lookup"><span data-stu-id="31181-138">If the simplification process cannot reduce the mesh to *MinValue*, the call still succeeds because *MinValue* is a desired minimum, not an absolute minimum.</span></span>

<span data-ttu-id="31181-139">Se *pVertexAttributeWeights* for definido como **NULL**, os valores a seguir serão atribuídos à estrutura [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) padrão.</span><span class="sxs-lookup"><span data-stu-id="31181-139">If *pVertexAttributeWeights* is set to **NULL**, the following values are assigned to the default [**D3DXATTRIBUTEWEIGHTS**](d3dxattributeweights.md) structure.</span></span>


```
D3DXATTRIBUTEWEIGHTS AttributeWeights;
    
AttributeWeights.Position  = 1.0;
AttributeWeights.Boundary =  1.0;
AttributeWeights.Normal   =  1.0;
AttributeWeights.Diffuse  =  0.0;
AttributeWeights.Specular =  0.0;
AttributeWeights.Tex[8]   =  {0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0, 0.0};
```



<span data-ttu-id="31181-140">Essa estrutura padrão é o que a maioria dos aplicativos deve usar, pois considera apenas o ajuste geométrico e normal.</span><span class="sxs-lookup"><span data-stu-id="31181-140">This default structure is what most applications should use because it considers only geometric and normal adjustment.</span></span> <span data-ttu-id="31181-141">Somente em casos especiais, os outros campos de membro precisarão ser modificados.</span><span class="sxs-lookup"><span data-stu-id="31181-141">Only in special cases will the other member fields need to be modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="31181-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31181-142">Requirements</span></span>



| <span data-ttu-id="31181-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="31181-143">Requirement</span></span> | <span data-ttu-id="31181-144">Valor</span><span class="sxs-lookup"><span data-stu-id="31181-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="31181-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31181-145">Header</span></span><br/>  | <dl> <span data-ttu-id="31181-146"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="31181-146"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="31181-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31181-147">Library</span></span><br/> | <dl> <span data-ttu-id="31181-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31181-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31181-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="31181-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31181-150">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="31181-150">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
