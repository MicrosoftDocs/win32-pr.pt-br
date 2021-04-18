---
description: Cria um objeto de malha usando um Declarador.
ms.assetid: ff977517-0a46-4c32-8d5e-f5fc3c1718c1
title: Função D3DXCreateMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cfb56fe5c52d2726dff0877522b6f72f70437552
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781367"
---
# <a name="d3dxcreatemesh-function"></a><span data-ttu-id="74430-103">Função D3DXCreateMesh</span><span class="sxs-lookup"><span data-stu-id="74430-103">D3DXCreateMesh function</span></span>

<span data-ttu-id="74430-104">Cria um objeto de malha usando um Declarador.</span><span class="sxs-lookup"><span data-stu-id="74430-104">Creates a mesh object using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="74430-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74430-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMesh(
  _In_        DWORD               NumFaces,
  _In_        DWORD               NumVertices,
  _In_        DWORD               Options,
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _In_        LPDIRECT3DDEVICE9   pD3DDevice,
  _Out_       LPD3DXMESH          *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="74430-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74430-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74430-107">*NumFaces* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74430-107">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74430-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74430-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74430-109">Número de faces para a malha.</span><span class="sxs-lookup"><span data-stu-id="74430-109">Number of faces for the mesh.</span></span> <span data-ttu-id="74430-110">O intervalo válido para esse número é maior que 0 e um menor que o DWORD (normalmente 65534), pois o último índice é reservado.</span><span class="sxs-lookup"><span data-stu-id="74430-110">The valid range for this number is greater than 0, and one less than the maximum DWORD (typically 65534), because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="74430-111">*NumVertices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74430-111">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74430-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74430-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74430-113">Número de vértices para a malha.</span><span class="sxs-lookup"><span data-stu-id="74430-113">Number of vertices for the mesh.</span></span> <span data-ttu-id="74430-114">Esse parâmetro deve ser maior que 0.</span><span class="sxs-lookup"><span data-stu-id="74430-114">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="74430-115">*Opções* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="74430-115">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74430-116">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="74430-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="74430-117">Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) , especificando as opções para a malha.</span><span class="sxs-lookup"><span data-stu-id="74430-117">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="74430-118">*pDeclaration* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74430-118">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74430-119">Tipo: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="74430-119">Type: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="74430-120">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que descreve o formato de vértice para a malha retornada.</span><span class="sxs-lookup"><span data-stu-id="74430-120">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span> <span data-ttu-id="74430-121">Esse parâmetro deve ser mapeado diretamente para um formato de vértice flexível (FVF).</span><span class="sxs-lookup"><span data-stu-id="74430-121">This parameter must map directly to a flexible vertex format (FVF).</span></span>

</dd> <dt>

<span data-ttu-id="74430-122">*pD3DDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="74430-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74430-123">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="74430-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="74430-124">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o objeto de dispositivo a ser associado à malha.</span><span class="sxs-lookup"><span data-stu-id="74430-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="74430-125">*ppMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="74430-125">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="74430-126">Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="74430-126">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="74430-127">Endereço de um ponteiro para uma interface [**ID3DXMesh**](id3dxmesh.md) , que representa o objeto de malha criado.</span><span class="sxs-lookup"><span data-stu-id="74430-127">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74430-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="74430-128">Return value</span></span>

<span data-ttu-id="74430-129">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="74430-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="74430-130">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="74430-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="74430-131">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="74430-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="74430-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="74430-132">Requirements</span></span>



| <span data-ttu-id="74430-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="74430-133">Requirement</span></span> | <span data-ttu-id="74430-134">Valor</span><span class="sxs-lookup"><span data-stu-id="74430-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74430-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="74430-135">Header</span></span><br/>  | <dl> <span data-ttu-id="74430-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="74430-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="74430-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="74430-137">Library</span></span><br/> | <dl> <span data-ttu-id="74430-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74430-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="74430-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="74430-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74430-140">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="74430-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="74430-141">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="74430-141">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
