---
description: Carrega a primeira hierarquia de quadros de um arquivo. x.
ms.assetid: 428e5cfb-d6a5-4a7f-b082-2d8898e65490
title: Função D3DXLoadMeshHierarchyFromXInMemory (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromXInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 91cf119fc8907701f87ebb5bda1bb0bf45294aba
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105791558"
---
# <a name="d3dxloadmeshhierarchyfromxinmemory-function"></a><span data-ttu-id="ab679-103">Função D3DXLoadMeshHierarchyFromXInMemory</span><span class="sxs-lookup"><span data-stu-id="ab679-103">D3DXLoadMeshHierarchyFromXInMemory function</span></span>

<span data-ttu-id="ab679-104">Carrega a primeira hierarquia de quadros de um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="ab679-104">Loads the first frame hierarchy from a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab679-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab679-105">Syntax</span></span>


```C++
HRESULT D3DXLoadMeshHierarchyFromXInMemory(
  _In_  LPCVOID                   pMemory,
  _In_  DWORD                     SizeOfMemory,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHeirarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a><span data-ttu-id="ab679-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab679-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab679-107">*pMemory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ab679-107">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab679-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab679-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab679-109">Ponteiro para um buffer que contém a hierarquia de malha.</span><span class="sxs-lookup"><span data-stu-id="ab679-109">Pointer to a buffer that contains the mesh hierarchy.</span></span>

</dd> <dt>

<span data-ttu-id="ab679-110">*SizeOfMemory* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ab679-110">*SizeOfMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab679-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab679-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab679-112">Tamanho do buffer pMemory, em bytes.</span><span class="sxs-lookup"><span data-stu-id="ab679-112">Size of the pMemory buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ab679-113">*Malhas* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ab679-113">*MeshOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab679-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ab679-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ab679-115">Combinação de um ou mais sinalizadores da enumeração [**D3DXMESH**](./d3dxmesh.md) que especificam as opções de criação para a malha.</span><span class="sxs-lookup"><span data-stu-id="ab679-115">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ab679-116">*pDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ab679-116">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab679-117">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ab679-117">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ab679-118">Ponteiro para uma interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , o objeto de dispositivo associado à malha.</span><span class="sxs-lookup"><span data-stu-id="ab679-118">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ab679-119">*pAlloc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ab679-119">*pAlloc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab679-120">Tipo: **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span><span class="sxs-lookup"><span data-stu-id="ab679-120">Type: **[**LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**</span></span>

<span data-ttu-id="ab679-121">Ponteiro para uma interface [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .</span><span class="sxs-lookup"><span data-stu-id="ab679-121">Pointer to an [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ab679-122">*pUserDataLoader* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ab679-122">*pUserDataLoader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab679-123">Tipo: **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span><span class="sxs-lookup"><span data-stu-id="ab679-123">Type: **[**LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**</span></span>

<span data-ttu-id="ab679-124">Interface fornecida pelo aplicativo que permite o carregamento de dados do usuário.</span><span class="sxs-lookup"><span data-stu-id="ab679-124">Application provided interface that allows loading of user data.</span></span> <span data-ttu-id="ab679-125">Consulte [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span><span class="sxs-lookup"><span data-stu-id="ab679-125">See [**ID3DXLoadUserData**](id3dxloaduserdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab679-126">*ppFrameHeirarchy* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ab679-126">*ppFrameHeirarchy* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab679-127">Tipo: **[ **LPD3DXFRAME**](d3dxframe.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab679-127">Type: **[**LPD3DXFRAME**](d3dxframe.md)\***</span></span>

<span data-ttu-id="ab679-128">Retorna um ponteiro para a hierarquia de quadro carregada.</span><span class="sxs-lookup"><span data-stu-id="ab679-128">Returns a pointer to the loaded frame hierarchy.</span></span> <span data-ttu-id="ab679-129">Consulte [**D3DXFRAME**](d3dxframe.md).</span><span class="sxs-lookup"><span data-stu-id="ab679-129">See [**D3DXFRAME**](d3dxframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab679-130">*ppAnimController* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ab679-130">*ppAnimController* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab679-131">Tipo: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span><span class="sxs-lookup"><span data-stu-id="ab679-131">Type: **[**LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***</span></span>

<span data-ttu-id="ab679-132">Retorna um ponteiro para o controlador de animação correspondente à animação no arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="ab679-132">Returns a pointer to the animation controller corresponding to animation in the .x file.</span></span> <span data-ttu-id="ab679-133">Isso é criado com rastreamentos e eventos padrão.</span><span class="sxs-lookup"><span data-stu-id="ab679-133">This is created with default tracks and events.</span></span> <span data-ttu-id="ab679-134">Consulte [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span><span class="sxs-lookup"><span data-stu-id="ab679-134">See [**ID3DXAnimationController**](id3dxanimationcontroller.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab679-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ab679-135">Return value</span></span>

<span data-ttu-id="ab679-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ab679-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ab679-137">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ab679-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ab679-138">Se a função falhar, o valor de retorno poderá ser um dos seguintes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ab679-138">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab679-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="ab679-139">Remarks</span></span>

<span data-ttu-id="ab679-140">Todas as malhas no arquivo serão recolhidas em uma malha de saída.</span><span class="sxs-lookup"><span data-stu-id="ab679-140">All the meshes in the file will be collapsed into one output mesh.</span></span> <span data-ttu-id="ab679-141">Se o arquivo contiver uma hierarquia de quadros, todas as transformações serão aplicadas à malha.</span><span class="sxs-lookup"><span data-stu-id="ab679-141">If the file contains a frame hierarchy, all the transformations will be applied to the mesh.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab679-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab679-142">Requirements</span></span>



| <span data-ttu-id="ab679-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab679-143">Requirement</span></span> | <span data-ttu-id="ab679-144">Valor</span><span class="sxs-lookup"><span data-stu-id="ab679-144">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab679-145">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ab679-145">Header</span></span><br/>  | <dl> <span data-ttu-id="ab679-146"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab679-146"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="ab679-147">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab679-147">Library</span></span><br/> | <dl> <span data-ttu-id="ab679-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab679-148"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ab679-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab679-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab679-150">Funções de animação</span><span class="sxs-lookup"><span data-stu-id="ab679-150">Animation Functions</span></span>](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
