---
description: Converta o subconjunto de malha especificado em uma série de faixas.
ms.assetid: 4f005383-6a5a-4393-ac88-202e45946d3d
title: Função D3DXConvertMeshSubsetToStrips (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToStrips
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d62461c13f76eb0efce809fa1114771a5ea2fe6d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105771516"
---
# <a name="d3dxconvertmeshsubsettostrips-function"></a><span data-ttu-id="18790-103">Função D3DXConvertMeshSubsetToStrips</span><span class="sxs-lookup"><span data-stu-id="18790-103">D3DXConvertMeshSubsetToStrips function</span></span>

<span data-ttu-id="18790-104">Converta o subconjunto de malha especificado em uma série de faixas.</span><span class="sxs-lookup"><span data-stu-id="18790-104">Convert the specified mesh subset into a series of strips.</span></span>

## <a name="syntax"></a><span data-ttu-id="18790-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="18790-105">Syntax</span></span>


```C++
HRESULT D3DXConvertMeshSubsetToStrips(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices,
  _Out_ LPD3DXBUFFER           *ppStripLengths,
  _Out_ DWORD                  *pNumStrips
);
```



## <a name="parameters"></a><span data-ttu-id="18790-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18790-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18790-107">*Malha* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="18790-107">*MeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18790-108">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="18790-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="18790-109">Ponteiro para uma interface [**ID3DXBaseMesh**](id3dxbasemesh.md) , representando a malha a ser convertida em uma faixa.</span><span class="sxs-lookup"><span data-stu-id="18790-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.</span></span>

</dd> <dt>

<span data-ttu-id="18790-110">*Atribid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="18790-110">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18790-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18790-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18790-112">ID de atributo do subconjunto de malha a ser convertido em faixas.</span><span class="sxs-lookup"><span data-stu-id="18790-112">Attribute ID of the mesh subset to convert to strips.</span></span>

</dd> <dt>

<span data-ttu-id="18790-113">*IBOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="18790-113">*IBOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18790-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="18790-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="18790-115">Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) , especificando opções para criar o buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="18790-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for creating the index buffer.</span></span> <span data-ttu-id="18790-116">Não pode ser D3DXMESH \_ 32 bits.</span><span class="sxs-lookup"><span data-stu-id="18790-116">Cannot be D3DXMESH\_32BIT.</span></span> <span data-ttu-id="18790-117">O buffer de índice será criado com índices de 32 bits ou de 16 bits, dependendo do formato do buffer de índice da malha especificada pelo parâmetro *mesh* .</span><span class="sxs-lookup"><span data-stu-id="18790-117">The index buffer will be created with 32-bit or 16-bit indices depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="18790-118">*ppIndexBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="18790-118">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18790-119">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="18790-119">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="18790-120">Ponteiro para uma interface [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , representando o buffer de índice que contém a faixa.</span><span class="sxs-lookup"><span data-stu-id="18790-120">Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing index buffer containing the strip.</span></span>

</dd> <dt>

<span data-ttu-id="18790-121">*pNumIndices* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="18790-121">*pNumIndices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18790-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="18790-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="18790-123">Número de índices no buffer retornado no parâmetro *ppIndexBuffer* .</span><span class="sxs-lookup"><span data-stu-id="18790-123">Number of indices in the buffer returned in the *ppIndexBuffer* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="18790-124">*ppStripLengths* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="18790-124">*ppStripLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18790-125">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="18790-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="18790-126">Buffer que contém uma matriz de um DWORD por faixa, que especifica o número de triângulos na faixa.</span><span class="sxs-lookup"><span data-stu-id="18790-126">Buffer containing an array of one DWORD per strip, which specifies the number of triangles in the that strip.</span></span>

</dd> <dt>

<span data-ttu-id="18790-127">*pNumStrips* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="18790-127">*pNumStrips* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18790-128">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="18790-128">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="18790-129">Número de faixas individuais no buffer de índice e na matriz de comprimento de faixa correspondente.</span><span class="sxs-lookup"><span data-stu-id="18790-129">Number of individual strips in the index buffer and corresponding strip length array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18790-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="18790-130">Return value</span></span>

<span data-ttu-id="18790-131">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="18790-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="18790-132">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="18790-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="18790-133">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="18790-133">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="18790-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="18790-134">Remarks</span></span>

<span data-ttu-id="18790-135">Antes de executar essa função, chame [**Optimize**](id3dxmesh--optimize.md) ou [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), com o \_ sinalizador D3DXMESHOPT ATTRSORT definido.</span><span class="sxs-lookup"><span data-stu-id="18790-135">Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="18790-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18790-136">Requirements</span></span>



| <span data-ttu-id="18790-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="18790-137">Requirement</span></span> | <span data-ttu-id="18790-138">Valor</span><span class="sxs-lookup"><span data-stu-id="18790-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18790-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="18790-139">Header</span></span><br/>  | <dl> <span data-ttu-id="18790-140"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="18790-140"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="18790-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="18790-141">Library</span></span><br/> | <dl> <span data-ttu-id="18790-142"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18790-142"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="18790-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="18790-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18790-144">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="18790-144">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
