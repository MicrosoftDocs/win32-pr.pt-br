---
description: Usa um sistema de coordenadas à esquerda para criar uma malha que contém um cilindro.
ms.assetid: 54b8a59e-d13f-44cb-84c0-f63c7b1ffb1b
title: Função D3DXCreateCylinder (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCylinder
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec97755d45b21a85e1a73bbcd2214ee4c1e2358f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103664019"
---
# <a name="d3dxcreatecylinder-function"></a><span data-ttu-id="c5988-103">Função D3DXCreateCylinder</span><span class="sxs-lookup"><span data-stu-id="c5988-103">D3DXCreateCylinder function</span></span>

<span data-ttu-id="c5988-104">Usa um sistema de coordenadas à esquerda para criar uma malha que contém um cilindro.</span><span class="sxs-lookup"><span data-stu-id="c5988-104">Uses a left-handed coordinate system to create a mesh containing a cylinder.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5988-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5988-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCylinder(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius1,
  _In_  FLOAT             Radius2,
  _In_  FLOAT             Length,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="c5988-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5988-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5988-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5988-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5988-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c5988-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c5988-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à malha de cilindros criada.</span><span class="sxs-lookup"><span data-stu-id="c5988-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created cylinder mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c5988-110">*Radius1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5988-110">*Radius1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5988-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5988-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5988-112">RADIUS na extremidade Z negativa.</span><span class="sxs-lookup"><span data-stu-id="c5988-112">Radius at the negative Z end.</span></span> <span data-ttu-id="c5988-113">O valor deve ser maior ou igual a 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="c5988-113">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="c5988-114">*Radius2* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5988-114">*Radius2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5988-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5988-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5988-116">RADIUS na extremidade Z positiva.</span><span class="sxs-lookup"><span data-stu-id="c5988-116">Radius at the positive Z end.</span></span> <span data-ttu-id="c5988-117">O valor deve ser maior ou igual a 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="c5988-117">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="c5988-118">*Comprimento* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5988-118">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5988-119">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5988-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5988-120">Comprimento do cilindro ao longo do eixo z.</span><span class="sxs-lookup"><span data-stu-id="c5988-120">Length of the cylinder along the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="c5988-121">*Fatias* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5988-121">*Slices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5988-122">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5988-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5988-123">Número de fatias sobre o eixo principal.</span><span class="sxs-lookup"><span data-stu-id="c5988-123">Number of slices about the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="c5988-124">*Pilhas* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c5988-124">*Stacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5988-125">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5988-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5988-126">Número de pilhas ao longo do eixo principal.</span><span class="sxs-lookup"><span data-stu-id="c5988-126">Number of stacks along the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="c5988-127">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c5988-127">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5988-128">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5988-128">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="c5988-129">Endereço de um ponteiro para a forma de saída, uma interface [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="c5988-129">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="c5988-130">*ppAdjacency* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="c5988-130">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5988-131">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c5988-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="c5988-132">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c5988-132">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="c5988-133">Quando o método retorna, esse parâmetro é preenchido com uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="c5988-133">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="c5988-134">**NULL** pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="c5988-134">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5988-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5988-135">Return value</span></span>

<span data-ttu-id="c5988-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5988-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5988-137">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c5988-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c5988-138">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c5988-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5988-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5988-139">Remarks</span></span>

<span data-ttu-id="c5988-140">O cilindro criado é centralizado na origem e seu eixo é alinhado com o eixo z.</span><span class="sxs-lookup"><span data-stu-id="c5988-140">The created cylinder is centered at the origin, and its axis is aligned with the z-axis.</span></span>

<span data-ttu-id="c5988-141">Essa função cria uma malha com a \_ opção de criação gerenciada D3DXMESH e [D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) formato de vértice flexível normal (FVF).</span><span class="sxs-lookup"><span data-stu-id="c5988-141">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="c5988-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5988-142">Requirements</span></span>



| <span data-ttu-id="c5988-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5988-143">Requirement</span></span> | <span data-ttu-id="c5988-144">Valor</span><span class="sxs-lookup"><span data-stu-id="c5988-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5988-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5988-145">Header</span></span><br/>  | <dl> <span data-ttu-id="c5988-146"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5988-146"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="c5988-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c5988-147">Library</span></span><br/> | <dl> <span data-ttu-id="c5988-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5988-148"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="c5988-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5988-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5988-150">Funções de desenho de forma</span><span class="sxs-lookup"><span data-stu-id="c5988-150">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
