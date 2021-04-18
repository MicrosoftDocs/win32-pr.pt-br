---
description: Converte o subconjunto de malha especificado em uma única faixa de triângulo.
ms.assetid: 618c7bee-dd09-4379-bb8b-30505e809df9
title: Função D3DXConvertMeshSubsetToSingleStrip (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXConvertMeshSubsetToSingleStrip
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c76aa52b08a21faf9bc2a6ef35745513063cc3b4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105756118"
---
# <a name="d3dxconvertmeshsubsettosinglestrip-function"></a><span data-ttu-id="a357c-103">Função D3DXConvertMeshSubsetToSingleStrip</span><span class="sxs-lookup"><span data-stu-id="a357c-103">D3DXConvertMeshSubsetToSingleStrip function</span></span>

<span data-ttu-id="a357c-104">Converte o subconjunto de malha especificado em uma única faixa de triângulo.</span><span class="sxs-lookup"><span data-stu-id="a357c-104">Converts the specified mesh subset into a single triangle strip.</span></span>

## <a name="syntax"></a><span data-ttu-id="a357c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a357c-105">Syntax</span></span>


```C++
HRESULT D3DXConvertMeshSubsetToSingleStrip(
  _In_  LPD3DXBASEMESH         MeshIn,
  _In_  DWORD                  AttribId,
  _In_  DWORD                  IBOptions,
  _Out_ LPDIRECT3DINDEXBUFFER9 *ppIndexBuffer,
  _Out_ DWORD                  *pNumIndices
);
```



## <a name="parameters"></a><span data-ttu-id="a357c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a357c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a357c-107">*Malha* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a357c-107">*MeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a357c-108">Tipo: **[ **LPD3DXBASEMESH**](id3dxbasemesh.md)**</span><span class="sxs-lookup"><span data-stu-id="a357c-108">Type: **[**LPD3DXBASEMESH**](id3dxbasemesh.md)**</span></span>

<span data-ttu-id="a357c-109">Ponteiro para uma interface [**ID3DXBaseMesh**](id3dxbasemesh.md) , representando a malha a ser convertida em uma faixa.</span><span class="sxs-lookup"><span data-stu-id="a357c-109">Pointer to an [**ID3DXBaseMesh**](id3dxbasemesh.md) interface, representing the mesh to convert to a strip.</span></span>

</dd> <dt>

<span data-ttu-id="a357c-110">*Atribid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a357c-110">*AttribId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a357c-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a357c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a357c-112">ID de atributo do subconjunto de malha a ser convertido em faixas.</span><span class="sxs-lookup"><span data-stu-id="a357c-112">Attribute ID of the mesh subset to convert to strips.</span></span>

</dd> <dt>

<span data-ttu-id="a357c-113">*IBOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a357c-113">*IBOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a357c-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a357c-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a357c-115">Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) , especificando opções para criar o buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="a357c-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for creating the index buffer.</span></span> <span data-ttu-id="a357c-116">Não pode ser D3DXMESH \_ 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a357c-116">Cannot be D3DXMESH\_32BIT.</span></span> <span data-ttu-id="a357c-117">O buffer de índice será criado com índices de 32 bits ou de 16 bits, dependendo do formato do buffer de índice da malha especificada pelo parâmetro *mesh* .</span><span class="sxs-lookup"><span data-stu-id="a357c-117">The index buffer will be created with 32-bit or 16-bit indices, depending on the format of the index buffer of the mesh specified by the *MeshIn* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a357c-118">*ppIndexBuffer* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a357c-118">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a357c-119">Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span><span class="sxs-lookup"><span data-stu-id="a357c-119">Type: **[**LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)\***</span></span>

<span data-ttu-id="a357c-120">Ponteiro para uma interface [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , representando o buffer de índice que contém a faixa.</span><span class="sxs-lookup"><span data-stu-id="a357c-120">Pointer to an [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) interface, representing the index buffer containing the strip.</span></span>

</dd> <dt>

<span data-ttu-id="a357c-121">*pNumIndices* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="a357c-121">*pNumIndices* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a357c-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a357c-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a357c-123">Número de índices no buffer retornado no parâmetro *ppIndexBuffer* .</span><span class="sxs-lookup"><span data-stu-id="a357c-123">Number of indices in the buffer returned in the *ppIndexBuffer* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a357c-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a357c-124">Return value</span></span>

<span data-ttu-id="a357c-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a357c-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a357c-126">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a357c-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a357c-127">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a357c-127">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a357c-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="a357c-128">Remarks</span></span>

<span data-ttu-id="a357c-129">Antes de executar essa função, chame [**Optimize**](id3dxmesh--optimize.md) ou [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), com o \_ sinalizador D3DXMESHOPT ATTRSORT definido.</span><span class="sxs-lookup"><span data-stu-id="a357c-129">Before running this function, call [**Optimize**](id3dxmesh--optimize.md) or [**D3DXOptimizeFaces**](d3dxoptimizefaces.md), with the D3DXMESHOPT\_ATTRSORT flag set.</span></span>

## <a name="requirements"></a><span data-ttu-id="a357c-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a357c-130">Requirements</span></span>



| <span data-ttu-id="a357c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a357c-131">Requirement</span></span> | <span data-ttu-id="a357c-132">Valor</span><span class="sxs-lookup"><span data-stu-id="a357c-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a357c-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a357c-133">Header</span></span><br/>  | <dl> <span data-ttu-id="a357c-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a357c-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a357c-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a357c-135">Library</span></span><br/> | <dl> <span data-ttu-id="a357c-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a357c-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a357c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="a357c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a357c-138">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="a357c-138">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
