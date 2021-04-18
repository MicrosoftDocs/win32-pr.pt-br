---
description: Solicita a alocação de um objeto de contêiner de malha.
ms.assetid: ec66b393-016b-4572-94dc-5c8903b506a3
title: 'Método ID3DXAllocateHierarchy:: CreateMeshContainer (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy.CreateMeshContainer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0351290b8dee260d52362702d520b01e1bcb7af3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105781238"
---
# <a name="id3dxallocatehierarchycreatemeshcontainer-method"></a><span data-ttu-id="9e5b8-103">Método ID3DXAllocateHierarchy:: CreateMeshContainer</span><span class="sxs-lookup"><span data-stu-id="9e5b8-103">ID3DXAllocateHierarchy::CreateMeshContainer method</span></span>

<span data-ttu-id="9e5b8-104">Solicita a alocação de um objeto de contêiner de malha.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-104">Requests allocation of a mesh container object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e5b8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9e5b8-105">Syntax</span></span>


```C++
HRESULT CreateMeshContainer(
  [in]                LPCSTR              Name,
  [in]          const D3DXMESHDATA        *pMeshData,
  [in]          const D3DXMATERIAL        *pMaterials,
  [in]          const D3DXEFFECTINSTANCE  *pEffectInstances,
  [in]                DWORD               NumMaterials,
  [in]          const DWORD               *pAdjacency,
  [in]                LPD3DXSKININFO      pSkinInfo,
  [out, retval]       LPD3DXMESHCONTAINER *ppNewMeshContainer
);
```



## <a name="parameters"></a><span data-ttu-id="9e5b8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9e5b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e5b8-107">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="9e5b8-107">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5b8-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e5b8-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e5b8-109">Nome da malha.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-109">Name of the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9e5b8-110">*pMeshData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e5b8-110">*pMeshData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5b8-111">Tipo: **const [**D3DXMESHDATA**](d3dxmeshdata.md) \***</span><span class="sxs-lookup"><span data-stu-id="9e5b8-111">Type: **const [**D3DXMESHDATA**](d3dxmeshdata.md)\***</span></span>

<span data-ttu-id="9e5b8-112">Ponteiro para a estrutura de dados de malha.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-112">Pointer to the mesh data structure.</span></span> <span data-ttu-id="9e5b8-113">Consulte [**D3DXMESHDATA**](d3dxmeshdata.md).</span><span class="sxs-lookup"><span data-stu-id="9e5b8-113">See [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e5b8-114">*pMaterials* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e5b8-114">*pMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5b8-115">Tipo: **const [**D3DXMATERIAL**](d3dxmaterial.md) \***</span><span class="sxs-lookup"><span data-stu-id="9e5b8-115">Type: **const [**D3DXMATERIAL**](d3dxmaterial.md)\***</span></span>

<span data-ttu-id="9e5b8-116">Matriz de materiais usada na malha.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-116">Array of materials used in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9e5b8-117">*pEffectInstances* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e5b8-117">*pEffectInstances* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5b8-118">Tipo: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***</span><span class="sxs-lookup"><span data-stu-id="9e5b8-118">Type: **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)\***</span></span>

<span data-ttu-id="9e5b8-119">Matriz de instâncias de efeito usadas na malha.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-119">Array of effect instances used in the mesh.</span></span> <span data-ttu-id="9e5b8-120">Consulte [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="9e5b8-120">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e5b8-121">*NumMaterials* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e5b8-121">*NumMaterials* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5b8-122">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e5b8-122">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e5b8-123">Número de materiais na matriz de materiais.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-123">Number of materials in the materials array.</span></span>

</dd> <dt>

<span data-ttu-id="9e5b8-124">*pAdjacency* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e5b8-124">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5b8-125">Tipo: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="9e5b8-125">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="9e5b8-126">Matriz de adjacência para a malha.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-126">Adjacency array for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="9e5b8-127">*pSkinInfo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9e5b8-127">*pSkinInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5b8-128">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**</span><span class="sxs-lookup"><span data-stu-id="9e5b8-128">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)**</span></span>

<span data-ttu-id="9e5b8-129">Ponteiro para o objeto de malha de capa se forem encontrados dados de capa.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-129">Pointer to the skin mesh object if skin data is found.</span></span> <span data-ttu-id="9e5b8-130">Consulte [**ID3DXSkinInfo**](id3dxskininfo.md).</span><span class="sxs-lookup"><span data-stu-id="9e5b8-130">See [**ID3DXSkinInfo**](id3dxskininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="9e5b8-131">*ppNewMeshContainer* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="9e5b8-131">*ppNewMeshContainer* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5b8-132">Tipo: **[ **LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span><span class="sxs-lookup"><span data-stu-id="9e5b8-132">Type: **[**LPD3DXMESHCONTAINER**](d3dxmeshcontainer.md)\***</span></span>

<span data-ttu-id="9e5b8-133">Retorna o contêiner de malha criado.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-133">Returns the created mesh container.</span></span> <span data-ttu-id="9e5b8-134">Consulte [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span><span class="sxs-lookup"><span data-stu-id="9e5b8-134">See [**D3DXMESHCONTAINER**](d3dxmeshcontainer.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e5b8-135">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9e5b8-135">Return value</span></span>

<span data-ttu-id="9e5b8-136">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9e5b8-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9e5b8-137">Os valores de retorno desse método são implementados por um programador de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-137">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="9e5b8-138">Em geral, se nenhum erro ocorrer, Programe o método para retornar o D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-138">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="9e5b8-139">Caso contrário, Programe o método para retornar uma mensagem de erro apropriada de D3DERR ou D3DXERR, pois isso fará com que o [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) falhe também e retorne o erro.</span><span class="sxs-lookup"><span data-stu-id="9e5b8-139">Otherwise, program the method to return an appropriate error message from D3DERR or D3DXERR, as this will cause [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) to fail also, and return the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e5b8-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e5b8-140">Requirements</span></span>



| <span data-ttu-id="9e5b8-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e5b8-141">Requirement</span></span> | <span data-ttu-id="9e5b8-142">Valor</span><span class="sxs-lookup"><span data-stu-id="9e5b8-142">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e5b8-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9e5b8-143">Header</span></span><br/>  | <dl> <span data-ttu-id="9e5b8-144"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e5b8-144"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="9e5b8-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e5b8-145">Library</span></span><br/> | <dl> <span data-ttu-id="9e5b8-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e5b8-146"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9e5b8-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="9e5b8-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e5b8-148">ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="9e5b8-148">ID3DXAllocateHierarchy</span></span>](id3dxallocatehierarchy.md)
</dt> </dl>

 

 
