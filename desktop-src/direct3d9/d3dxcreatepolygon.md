---
description: Usa um sistema de coordenadas à esquerda para criar uma malha que contém um polígono n.
ms.assetid: f3313f55-3e60-4440-8bea-d2886b636c9a
title: Função D3DXCreatePolygon (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePolygon
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94a7e48f512d25ca53d1f3ff80889a013e2ecdcb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012098"
---
# <a name="d3dxcreatepolygon-function"></a><span data-ttu-id="2fbfa-103">Função D3DXCreatePolygon</span><span class="sxs-lookup"><span data-stu-id="2fbfa-103">D3DXCreatePolygon function</span></span>

<span data-ttu-id="2fbfa-104">Usa um sistema de coordenadas à esquerda para criar uma malha que contém um polígono n.</span><span class="sxs-lookup"><span data-stu-id="2fbfa-104">Uses a left-handed coordinate system to create a mesh containing an n-sided polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fbfa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2fbfa-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePolygon(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Length,
  _In_  UINT              Sides,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="2fbfa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2fbfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fbfa-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2fbfa-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fbfa-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2fbfa-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2fbfa-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à malha Polygon criada.</span><span class="sxs-lookup"><span data-stu-id="2fbfa-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created polygon mesh.</span></span>

</dd> <dt>

<span data-ttu-id="2fbfa-110">*Comprimento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2fbfa-110">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fbfa-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2fbfa-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2fbfa-112">Comprimento de cada lado.</span><span class="sxs-lookup"><span data-stu-id="2fbfa-112">Length of each side.</span></span>

</dd> <dt>

<span data-ttu-id="2fbfa-113">*Lados* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2fbfa-113">*Sides* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fbfa-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2fbfa-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2fbfa-115">Número de lados do polígono.</span><span class="sxs-lookup"><span data-stu-id="2fbfa-115">Number of sides for the polygon.</span></span> <span data-ttu-id="2fbfa-116">O valor deve ser maior ou igual a 3.</span><span class="sxs-lookup"><span data-stu-id="2fbfa-116">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="2fbfa-117">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2fbfa-117">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fbfa-118">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="2fbfa-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="2fbfa-119">Endereço de um ponteiro para a forma de saída, uma interface [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="2fbfa-119">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="2fbfa-120">*ppAdjacency* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="2fbfa-120">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2fbfa-121">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="2fbfa-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="2fbfa-122">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="2fbfa-122">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="2fbfa-123">Quando o método retorna, esse parâmetro é preenchido com uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="2fbfa-123">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="2fbfa-124">**NULL** pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="2fbfa-124">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fbfa-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2fbfa-125">Return value</span></span>

<span data-ttu-id="2fbfa-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2fbfa-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2fbfa-127">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2fbfa-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2fbfa-128">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="2fbfa-128">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fbfa-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="2fbfa-129">Remarks</span></span>

<span data-ttu-id="2fbfa-130">O polígono criado é centralizado na origem.</span><span class="sxs-lookup"><span data-stu-id="2fbfa-130">The created polygon is centered at the origin.</span></span>

<span data-ttu-id="2fbfa-131">Essa função cria uma malha com a \_ opção de criação gerenciada D3DXMESH e [D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) formato de vértice flexível normal (FVF).</span><span class="sxs-lookup"><span data-stu-id="2fbfa-131">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="2fbfa-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fbfa-132">Requirements</span></span>



| <span data-ttu-id="2fbfa-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fbfa-133">Requirement</span></span> | <span data-ttu-id="2fbfa-134">Valor</span><span class="sxs-lookup"><span data-stu-id="2fbfa-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fbfa-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2fbfa-135">Header</span></span><br/>  | <dl> <span data-ttu-id="2fbfa-136"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fbfa-136"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="2fbfa-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2fbfa-137">Library</span></span><br/> | <dl> <span data-ttu-id="2fbfa-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2fbfa-138"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="2fbfa-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="2fbfa-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fbfa-140">Funções de desenho de forma</span><span class="sxs-lookup"><span data-stu-id="2fbfa-140">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
