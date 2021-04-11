---
description: Usa um sistema de coordenadas à esquerda para criar uma malha que contém uma esfera.
ms.assetid: d3198805-9435-4849-892d-ec98dc2221d2
title: Função D3DXCreateSphere (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56ac6b8e8cc2195e2176e505cf430ea33b6b6ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173012"
---
# <a name="d3dxcreatesphere-function"></a><span data-ttu-id="0a4f6-103">Função D3DXCreateSphere</span><span class="sxs-lookup"><span data-stu-id="0a4f6-103">D3DXCreateSphere function</span></span>

<span data-ttu-id="0a4f6-104">Usa um sistema de coordenadas à esquerda para criar uma malha que contém uma esfera.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-104">Uses a left-handed coordinate system to create a mesh containing a sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a4f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a4f6-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSphere(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="0a4f6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0a4f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a4f6-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a4f6-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a4f6-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0a4f6-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à malha de sphere criada.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created sphere mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0a4f6-110">*RADIUS* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a4f6-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a4f6-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a4f6-112">Raio da esfera.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-112">Radius of the sphere.</span></span> <span data-ttu-id="0a4f6-113">Esse valor deve ser maior ou igual a 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-113">This value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="0a4f6-114">*Fatias* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a4f6-114">*Slices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a4f6-115">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a4f6-116">Número de fatias sobre o eixo principal.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-116">Number of slices about the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="0a4f6-117">*Pilhas* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0a4f6-117">*Stacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a4f6-118">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0a4f6-119">Número de pilhas ao longo do eixo principal.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-119">Number of stacks along the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="0a4f6-120">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0a4f6-120">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a4f6-121">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a4f6-121">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="0a4f6-122">Endereço de um ponteiro para a forma de saída, uma interface [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="0a4f6-122">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0a4f6-123">*ppAdjacency* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="0a4f6-123">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a4f6-124">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0a4f6-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0a4f6-125">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0a4f6-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="0a4f6-126">Quando o método retorna, esse parâmetro é preenchido com uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-126">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="0a4f6-127">**NULL** pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-127">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a4f6-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0a4f6-128">Return value</span></span>

<span data-ttu-id="0a4f6-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0a4f6-130">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0a4f6-131">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a4f6-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a4f6-132">Remarks</span></span>

<span data-ttu-id="0a4f6-133">A esfera criada é centralizada na origem e seu eixo é alinhado com o eixo z.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-133">The created sphere is centered at the origin, and its axis is aligned with the z-axis.</span></span>

<span data-ttu-id="0a4f6-134">Essa função cria uma malha com a \_ opção de criação gerenciada D3DXMESH e [D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) formato de vértice flexível normal (FVF).</span><span class="sxs-lookup"><span data-stu-id="0a4f6-134">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="0a4f6-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a4f6-135">Requirements</span></span>



| <span data-ttu-id="0a4f6-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a4f6-136">Requirement</span></span> | <span data-ttu-id="0a4f6-137">Valor</span><span class="sxs-lookup"><span data-stu-id="0a4f6-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a4f6-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0a4f6-138">Header</span></span><br/>  | <dl> <span data-ttu-id="0a4f6-139"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a4f6-139"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="0a4f6-140">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0a4f6-140">Library</span></span><br/> | <dl> <span data-ttu-id="0a4f6-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a4f6-141"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0a4f6-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a4f6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4f6-143">Funções de desenho de forma</span><span class="sxs-lookup"><span data-stu-id="0a4f6-143">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
