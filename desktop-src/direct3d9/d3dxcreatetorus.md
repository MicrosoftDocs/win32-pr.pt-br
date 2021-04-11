---
description: Usa um sistema de coordenadas à esquerda para criar uma malha que contém um Torus.
ms.assetid: 68df7650-8a87-4762-8b57-5704c419b0d7
title: Função D3DXCreateTorus (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTorus
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 384950ca1f00d0115135cf9ae36a2883ec5470e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173008"
---
# <a name="d3dxcreatetorus-function"></a><span data-ttu-id="ee302-103">Função D3DXCreateTorus</span><span class="sxs-lookup"><span data-stu-id="ee302-103">D3DXCreateTorus function</span></span>

<span data-ttu-id="ee302-104">Usa um sistema de coordenadas à esquerda para criar uma malha que contém um Torus.</span><span class="sxs-lookup"><span data-stu-id="ee302-104">Uses a left-handed coordinate system to create a mesh containing a torus.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee302-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee302-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTorus(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             InnerRadius,
  _In_  FLOAT             OuterRadius,
  _In_  UINT              Sides,
  _In_  UINT              Rings,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="ee302-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee302-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee302-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee302-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee302-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ee302-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ee302-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à malha Torus criada.</span><span class="sxs-lookup"><span data-stu-id="ee302-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created torus mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ee302-110">*InnerRadius* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee302-110">*InnerRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee302-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee302-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee302-112">Interno-raio do Torus.</span><span class="sxs-lookup"><span data-stu-id="ee302-112">Inner-radius of the torus.</span></span> <span data-ttu-id="ee302-113">O valor deve ser maior ou igual a 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="ee302-113">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="ee302-114">*OuterRadius* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee302-114">*OuterRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee302-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee302-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee302-116">Externo-RADIUS do Torus.</span><span class="sxs-lookup"><span data-stu-id="ee302-116">Outer-radius of the torus.</span></span> <span data-ttu-id="ee302-117">O valor deve ser maior ou igual a 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="ee302-117">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="ee302-118">*Lados* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee302-118">*Sides* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee302-119">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee302-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee302-120">Número de lados em uma seção cruzada.</span><span class="sxs-lookup"><span data-stu-id="ee302-120">Number of sides in a cross-section.</span></span> <span data-ttu-id="ee302-121">O valor deve ser maior ou igual a 3.</span><span class="sxs-lookup"><span data-stu-id="ee302-121">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="ee302-122">*Anéis* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ee302-122">*Rings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee302-123">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ee302-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ee302-124">Número de anéis que compõem o Torus.</span><span class="sxs-lookup"><span data-stu-id="ee302-124">Number of rings making up the torus.</span></span> <span data-ttu-id="ee302-125">O valor deve ser maior ou igual a 3.</span><span class="sxs-lookup"><span data-stu-id="ee302-125">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="ee302-126">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ee302-126">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee302-127">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee302-127">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="ee302-128">Endereço de um ponteiro para a forma de saída, uma interface [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="ee302-128">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ee302-129">*ppAdjacency* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ee302-129">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee302-130">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ee302-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ee302-131">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ee302-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="ee302-132">Quando o método retorna, esse parâmetro é preenchido com uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="ee302-132">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="ee302-133">**NULL** pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="ee302-133">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee302-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee302-134">Return value</span></span>

<span data-ttu-id="ee302-135">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ee302-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ee302-136">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee302-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ee302-137">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ee302-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee302-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee302-138">Remarks</span></span>

<span data-ttu-id="ee302-139">O Torus criado é centralizado na origem e seu eixo é alinhado com o eixo z.</span><span class="sxs-lookup"><span data-stu-id="ee302-139">The created torus is centered at the origin, and its axis is aligned with the z-axis.</span></span> <span data-ttu-id="ee302-140">O raio interno do Torus é o raio da seção cruzada (o raio secundário) e o raio externo do Torus é o raio do buraco central.</span><span class="sxs-lookup"><span data-stu-id="ee302-140">The inner radius of the torus is the radius of the cross-section (the minor radius), and the outer radius of the torus is the radius of the central hole.</span></span>

<span data-ttu-id="ee302-141">Essa função retorna uma malha que pode ser usada posteriormente para desenhar ou manipular pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee302-141">This function returns a mesh that can be used later for drawing or manipulation by the application.</span></span>

<span data-ttu-id="ee302-142">Essa função cria uma malha com a \_ opção de criação gerenciada D3DXMESH e [D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) formato de vértice flexível normal (FVF).</span><span class="sxs-lookup"><span data-stu-id="ee302-142">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee302-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee302-143">Requirements</span></span>



| <span data-ttu-id="ee302-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee302-144">Requirement</span></span> | <span data-ttu-id="ee302-145">Valor</span><span class="sxs-lookup"><span data-stu-id="ee302-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee302-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee302-146">Header</span></span><br/>  | <dl> <span data-ttu-id="ee302-147"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee302-147"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="ee302-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee302-148">Library</span></span><br/> | <dl> <span data-ttu-id="ee302-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ee302-149"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ee302-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee302-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee302-151">Funções de desenho de forma</span><span class="sxs-lookup"><span data-stu-id="ee302-151">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
