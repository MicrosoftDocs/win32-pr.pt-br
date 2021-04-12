---
description: Cria uma malha a partir de uma malha de controle-patch.
ms.assetid: 50e4f7aa-a6b8-4a2b-9813-a9448f408d06
title: Função D3DXCreatePatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePatchMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 375052e240973f56af32825f74caccf6f9411d75
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298821"
---
# <a name="d3dxcreatepatchmesh-function"></a><span data-ttu-id="1489e-103">Função D3DXCreatePatchMesh</span><span class="sxs-lookup"><span data-stu-id="1489e-103">D3DXCreatePatchMesh function</span></span>

<span data-ttu-id="1489e-104">Cria uma malha a partir de uma malha de controle-patch.</span><span class="sxs-lookup"><span data-stu-id="1489e-104">Creates a mesh from a control-patch mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="1489e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1489e-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePatchMesh(
  _In_  const D3DXPATCHINFO     *pInfo,
  _In_        DWORD             dwNumPatches,
  _In_        DWORD             dwNumVertices,
  _In_        DWORD             dwOptions,
  _In_  const D3DVERTEXELEMENT9 *pDecl,
  _In_        LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_       LPD3DXPATCHMESH   *pPatchMesh
);
```



## <a name="parameters"></a><span data-ttu-id="1489e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1489e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1489e-107">*pInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1489e-107">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1489e-108">Tipo: **const [**D3DXPATCHINFO**](d3dxpatchinfo.md) \***</span><span class="sxs-lookup"><span data-stu-id="1489e-108">Type: **const [**D3DXPATCHINFO**](d3dxpatchinfo.md)\***</span></span>

<span data-ttu-id="1489e-109">Estrutura de informações do patch.</span><span class="sxs-lookup"><span data-stu-id="1489e-109">Patch information structure.</span></span> <span data-ttu-id="1489e-110">Para obter mais informações, consulte [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span><span class="sxs-lookup"><span data-stu-id="1489e-110">For more information, see [**D3DXPATCHINFO**](d3dxpatchinfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="1489e-111">*dwNumPatches* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1489e-111">*dwNumPatches* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1489e-112">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1489e-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1489e-113">Número de patches.</span><span class="sxs-lookup"><span data-stu-id="1489e-113">Number of patches.</span></span>

</dd> <dt>

<span data-ttu-id="1489e-114">*dwNumVertices* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1489e-114">*dwNumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1489e-115">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1489e-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1489e-116">Número de vértices de controle no patch.</span><span class="sxs-lookup"><span data-stu-id="1489e-116">Number of control vertices in the patch.</span></span>

</dd> <dt>

<span data-ttu-id="1489e-117">*dwOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1489e-117">*dwOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1489e-118">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1489e-118">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1489e-119">Não utilizado.</span><span class="sxs-lookup"><span data-stu-id="1489e-119">Unused.</span></span> <span data-ttu-id="1489e-120">Reservado para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="1489e-120">Reserved for later use.</span></span>

</dd> <dt>

<span data-ttu-id="1489e-121">*pDecl* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1489e-121">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1489e-122">Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="1489e-122">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="1489e-123">Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que descreve o formato de vértice para a malha retornada.</span><span class="sxs-lookup"><span data-stu-id="1489e-123">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, describing the vertex format for the returned mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1489e-124">*pD3DDevice* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1489e-124">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1489e-125">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1489e-125">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1489e-126">Ponteiro do dispositivo que cria a malha do patch.</span><span class="sxs-lookup"><span data-stu-id="1489e-126">Pointer the device that creates the patch mesh.</span></span> <span data-ttu-id="1489e-127">Consulte [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span><span class="sxs-lookup"><span data-stu-id="1489e-127">See [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).</span></span>

</dd> <dt>

<span data-ttu-id="1489e-128">*pPatchMesh* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1489e-128">*pPatchMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1489e-129">Tipo: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="1489e-129">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="1489e-130">Ponteiro para o objeto [**ID3DXPatchMesh**](id3dxpatchmesh.md) que é criado.</span><span class="sxs-lookup"><span data-stu-id="1489e-130">Pointer to the [**ID3DXPatchMesh**](id3dxpatchmesh.md) object that is created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1489e-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1489e-131">Return value</span></span>

<span data-ttu-id="1489e-132">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1489e-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1489e-133">Se a função for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1489e-133">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1489e-134">Se a função falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1489e-134">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1489e-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="1489e-135">Remarks</span></span>

<span data-ttu-id="1489e-136">Esse método usa uma malha de patch de entrada e a converte em uma malha mosaico.</span><span class="sxs-lookup"><span data-stu-id="1489e-136">This method takes an input patch mesh and converts it to a tessellated mesh.</span></span> <span data-ttu-id="1489e-137">As malhas de patch usam buffers de índice de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1489e-137">Patch meshes use 16-bit index buffers.</span></span> <span data-ttu-id="1489e-138">Portanto, os índices para [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) são 16 bits.</span><span class="sxs-lookup"><span data-stu-id="1489e-138">Therefore, indices to [**LockIndexBuffer**](id3dxpatchmesh--lockindexbuffer.md) are 16 bits.</span></span>

## <a name="requirements"></a><span data-ttu-id="1489e-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1489e-139">Requirements</span></span>



| <span data-ttu-id="1489e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="1489e-140">Requirement</span></span> | <span data-ttu-id="1489e-141">Valor</span><span class="sxs-lookup"><span data-stu-id="1489e-141">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1489e-142">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1489e-142">Header</span></span><br/>  | <dl> <span data-ttu-id="1489e-143"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="1489e-143"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="1489e-144">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1489e-144">Library</span></span><br/> | <dl> <span data-ttu-id="1489e-145"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1489e-145"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1489e-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="1489e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1489e-147">Funções de malha</span><span class="sxs-lookup"><span data-stu-id="1489e-147">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="1489e-148">**D3DXPATCHINFO**</span><span class="sxs-lookup"><span data-stu-id="1489e-148">**D3DXPATCHINFO**</span></span>](d3dxpatchinfo.md)
</dt> </dl>

 

 
