---
description: Usa um sistema de coordenadas à esquerda para criar uma malha que contém uma caixa alinhada ao eixo.
ms.assetid: 396ef0f7-65d5-46f9-9b97-e6471f2fb5fe
title: Função D3DXCreateBox (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBox
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 187c389dd2d90b4457237540026a63edc4ab4f4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765163"
---
# <a name="d3dxcreatebox-function"></a><span data-ttu-id="99e8e-103">Função D3DXCreateBox</span><span class="sxs-lookup"><span data-stu-id="99e8e-103">D3DXCreateBox function</span></span>

<span data-ttu-id="99e8e-104">Usa um sistema de coordenadas à esquerda para criar uma malha que contém uma caixa alinhada ao eixo.</span><span class="sxs-lookup"><span data-stu-id="99e8e-104">Uses a left-handed coordinate system to create a mesh containing an axis-aligned box.</span></span>

## <a name="syntax"></a><span data-ttu-id="99e8e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99e8e-105">Syntax</span></span>


```C++
HRESULT D3DXCreateBox(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Width,
  _In_  FLOAT             Height,
  _In_  FLOAT             Depth,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="99e8e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99e8e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99e8e-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99e8e-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e8e-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="99e8e-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="99e8e-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à malha da caixa criada.</span><span class="sxs-lookup"><span data-stu-id="99e8e-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created box mesh.</span></span>

</dd> <dt>

<span data-ttu-id="99e8e-110">*Largura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99e8e-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e8e-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99e8e-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99e8e-112">Largura da caixa, ao longo do eixo x.</span><span class="sxs-lookup"><span data-stu-id="99e8e-112">Width of the box, along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="99e8e-113">*Altura* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99e8e-113">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e8e-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99e8e-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99e8e-115">Altura da caixa, ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="99e8e-115">Height of the box, along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="99e8e-116">*Profundidade* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="99e8e-116">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99e8e-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99e8e-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99e8e-118">Profundidade da caixa, ao longo do eixo z.</span><span class="sxs-lookup"><span data-stu-id="99e8e-118">Depth of the box, along the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="99e8e-119">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="99e8e-119">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99e8e-120">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="99e8e-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="99e8e-121">Endereço de um ponteiro para a forma de saída, uma interface [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="99e8e-121">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="99e8e-122">*ppAdjacency* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="99e8e-122">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99e8e-123">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="99e8e-123">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="99e8e-124">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="99e8e-124">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="99e8e-125">Quando o método retorna, esse parâmetro é preenchido com uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="99e8e-125">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="99e8e-126">**NULL** pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="99e8e-126">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99e8e-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="99e8e-127">Return value</span></span>

<span data-ttu-id="99e8e-128">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99e8e-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99e8e-129">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="99e8e-129">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="99e8e-130">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="99e8e-130">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="99e8e-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="99e8e-131">Remarks</span></span>

<span data-ttu-id="99e8e-132">A caixa criada é centralizada na origem.</span><span class="sxs-lookup"><span data-stu-id="99e8e-132">The created box is centered at the origin.</span></span>

<span data-ttu-id="99e8e-133">Essa função cria uma malha com a \_ opção de criação gerenciada D3DXMESH e [D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) formato de vértice flexível normal (FVF).</span><span class="sxs-lookup"><span data-stu-id="99e8e-133">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="99e8e-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99e8e-134">Requirements</span></span>



| <span data-ttu-id="99e8e-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="99e8e-135">Requirement</span></span> | <span data-ttu-id="99e8e-136">Valor</span><span class="sxs-lookup"><span data-stu-id="99e8e-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99e8e-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99e8e-137">Header</span></span><br/>  | <dl> <span data-ttu-id="99e8e-138"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="99e8e-138"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="99e8e-139">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="99e8e-139">Library</span></span><br/> | <dl> <span data-ttu-id="99e8e-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99e8e-140"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="99e8e-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="99e8e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99e8e-142">Funções de desenho de forma</span><span class="sxs-lookup"><span data-stu-id="99e8e-142">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
