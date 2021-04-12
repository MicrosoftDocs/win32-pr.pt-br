---
description: Usa um sistema de coordenadas à esquerda para criar uma malha que contém um bule.
ms.assetid: c002d6d4-1829-4293-9a86-d8560d6ec0e9
title: Função D3DXCreateTeapot (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTeapot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 13f5ed44bdc31958729209f01183eba409298fcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173011"
---
# <a name="d3dxcreateteapot-function"></a><span data-ttu-id="112e8-103">Função D3DXCreateTeapot</span><span class="sxs-lookup"><span data-stu-id="112e8-103">D3DXCreateTeapot function</span></span>

<span data-ttu-id="112e8-104">Usa um sistema de coordenadas à esquerda para criar uma malha que contém um bule.</span><span class="sxs-lookup"><span data-stu-id="112e8-104">Uses a left-handed coordinate system to create a mesh containing a teapot.</span></span>

## <a name="syntax"></a><span data-ttu-id="112e8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="112e8-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTeapot(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="112e8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="112e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="112e8-107">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="112e8-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="112e8-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="112e8-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="112e8-109">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , representando o dispositivo associado à malha bule criada.</span><span class="sxs-lookup"><span data-stu-id="112e8-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created teapot mesh.</span></span>

</dd> <dt>

<span data-ttu-id="112e8-110">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="112e8-110">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="112e8-111">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="112e8-111">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="112e8-112">Endereço de um ponteiro para a forma de saída, uma interface [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="112e8-112">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="112e8-113">*ppAdjacency* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="112e8-113">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="112e8-114">Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="112e8-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="112e8-115">Endereço de um ponteiro para uma interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="112e8-115">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="112e8-116">Quando o método retorna, esse parâmetro é preenchido com uma matriz de três DWORDs por face que especificam os três vizinhos para cada face na malha.</span><span class="sxs-lookup"><span data-stu-id="112e8-116">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="112e8-117">**NULL** pode ser especificado.</span><span class="sxs-lookup"><span data-stu-id="112e8-117">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="112e8-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="112e8-118">Return value</span></span>

<span data-ttu-id="112e8-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="112e8-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="112e8-120">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="112e8-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="112e8-121">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="112e8-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="112e8-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="112e8-122">Remarks</span></span>

<span data-ttu-id="112e8-123">Essa função cria uma malha com a \_ opção de criação gerenciada D3DXMESH e [D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) formato de vértice flexível normal (FVF).</span><span class="sxs-lookup"><span data-stu-id="112e8-123">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="112e8-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="112e8-124">Requirements</span></span>



| <span data-ttu-id="112e8-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="112e8-125">Requirement</span></span> | <span data-ttu-id="112e8-126">Valor</span><span class="sxs-lookup"><span data-stu-id="112e8-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="112e8-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="112e8-127">Header</span></span><br/>  | <dl> <span data-ttu-id="112e8-128"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="112e8-128"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="112e8-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="112e8-129">Library</span></span><br/> | <dl> <span data-ttu-id="112e8-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="112e8-130"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="112e8-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="112e8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="112e8-132">Funções de desenho de forma</span><span class="sxs-lookup"><span data-stu-id="112e8-132">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
