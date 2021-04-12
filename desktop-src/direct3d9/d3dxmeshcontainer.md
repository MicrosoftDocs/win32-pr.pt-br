---
description: Encapsula um objeto de malha em uma hierarquia de quadros de transformação.
ms.assetid: 50e98230-7dc3-468a-92c4-8165e8fe242b
title: Estrutura D3DXMESHCONTAINER (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHCONTAINER
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: f57daea26f42d8dd680d0259199b0df77badf510
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104298485"
---
# <a name="d3dxmeshcontainer-structure"></a><span data-ttu-id="726ba-103">Estrutura D3DXMESHCONTAINER</span><span class="sxs-lookup"><span data-stu-id="726ba-103">D3DXMESHCONTAINER structure</span></span>

<span data-ttu-id="726ba-104">Encapsula um objeto de malha em uma hierarquia de quadros de transformação.</span><span class="sxs-lookup"><span data-stu-id="726ba-104">Encapsulates a mesh object in a transformation frame hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="726ba-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="726ba-105">Syntax</span></span>


```C++
typedef struct D3DXMESHCONTAINER {
  LPSTR                Name;
  D3DXMESHDATA         MeshData;
  LPD3DXMATERIAL       pMaterials;
  LPD3DXEFFECTINSTANCE pEffects;
  DWORD                NumMaterials;
  DWORD                *pAdjacency;
  LPD3DXSKININFO       pSkinInfo;
  D3DXMESHCONTAINER    *pNextMeshContainer;
} D3DXMESHCONTAINER, *LPD3DXMESHCONTAINER;
```



## <a name="members"></a><span data-ttu-id="726ba-106">Membros</span><span class="sxs-lookup"><span data-stu-id="726ba-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="726ba-107">**Nome**</span><span class="sxs-lookup"><span data-stu-id="726ba-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="726ba-108">Tipo: **LPSTR**</span><span class="sxs-lookup"><span data-stu-id="726ba-108">Type: **LPSTR**</span></span>

</dd> <dd>

<span data-ttu-id="726ba-109">Nome da malha.</span><span class="sxs-lookup"><span data-stu-id="726ba-109">Mesh name.</span></span>

</dd> <dt>

<span data-ttu-id="726ba-110">**MeshData**</span><span class="sxs-lookup"><span data-stu-id="726ba-110">**MeshData**</span></span>
</dt> <dd>

<span data-ttu-id="726ba-111">Tipo: **[ **D3DXMESHDATA**](d3dxmeshdata.md)**</span><span class="sxs-lookup"><span data-stu-id="726ba-111">Type: **[**D3DXMESHDATA**](d3dxmeshdata.md)**</span></span>

</dd> <dd>

<span data-ttu-id="726ba-112">Tipo de dados na malha.</span><span class="sxs-lookup"><span data-stu-id="726ba-112">Type of data in the mesh.</span></span> <span data-ttu-id="726ba-113">Consulte [**D3DXMESHDATA**](d3dxmeshdata.md).</span><span class="sxs-lookup"><span data-stu-id="726ba-113">See [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="726ba-114">**pMaterials**</span><span class="sxs-lookup"><span data-stu-id="726ba-114">**pMaterials**</span></span>
</dt> <dd>

<span data-ttu-id="726ba-115">Tipo: **[ **LPD3DXMATERIAL**](d3dxmaterial.md)**</span><span class="sxs-lookup"><span data-stu-id="726ba-115">Type: **[**LPD3DXMATERIAL**](d3dxmaterial.md)**</span></span>

</dd> <dd>

<span data-ttu-id="726ba-116">Matriz de materiais de malha.</span><span class="sxs-lookup"><span data-stu-id="726ba-116">Array of mesh materials.</span></span> <span data-ttu-id="726ba-117">Consulte [**D3DXMATERIAL**](d3dxmaterial.md).</span><span class="sxs-lookup"><span data-stu-id="726ba-117">See [**D3DXMATERIAL**](d3dxmaterial.md).</span></span>

</dd> <dt>

<span data-ttu-id="726ba-118">**pEffects**</span><span class="sxs-lookup"><span data-stu-id="726ba-118">**pEffects**</span></span>
</dt> <dd>

<span data-ttu-id="726ba-119">Tipo: **[ **LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**</span><span class="sxs-lookup"><span data-stu-id="726ba-119">Type: **[**LPD3DXEFFECTINSTANCE**](d3dxeffectinstance.md)**</span></span>

</dd> <dd>

<span data-ttu-id="726ba-120">Ponteiro para um conjunto de parâmetros de efeito padrão.</span><span class="sxs-lookup"><span data-stu-id="726ba-120">Pointer to a set of default effect parameters.</span></span> <span data-ttu-id="726ba-121">Consulte [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span><span class="sxs-lookup"><span data-stu-id="726ba-121">See [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).</span></span>

</dd> <dt>

<span data-ttu-id="726ba-122">**NumMaterials**</span><span class="sxs-lookup"><span data-stu-id="726ba-122">**NumMaterials**</span></span>
</dt> <dd>

<span data-ttu-id="726ba-123">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="726ba-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="726ba-124">Número de materiais na malha.</span><span class="sxs-lookup"><span data-stu-id="726ba-124">Number of materials in the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="726ba-125">**pAdjacency**</span><span class="sxs-lookup"><span data-stu-id="726ba-125">**pAdjacency**</span></span>
</dt> <dd>

<span data-ttu-id="726ba-126">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="726ba-126">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="726ba-127">Ponteiro para uma matriz de três DWORDs por triângulo da malha que contém informações de adjacência.</span><span class="sxs-lookup"><span data-stu-id="726ba-127">Pointer to an array of three DWORDs per triangle of the mesh that contains adjacency information.</span></span>

</dd> <dt>

<span data-ttu-id="726ba-128">**pSkinInfo**</span><span class="sxs-lookup"><span data-stu-id="726ba-128">**pSkinInfo**</span></span>
</dt> <dd>

<span data-ttu-id="726ba-129">Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)**</span><span class="sxs-lookup"><span data-stu-id="726ba-129">Type: **[**LPD3DXSKININFO**](id3dxskininfo.md)**</span></span>

</dd> <dd>

<span data-ttu-id="726ba-130">Ponteiro para a interface de informações da capa.</span><span class="sxs-lookup"><span data-stu-id="726ba-130">Pointer to the skin information interface.</span></span> <span data-ttu-id="726ba-131">Consulte [**ID3DXSkinInfo**](id3dxskininfo.md).</span><span class="sxs-lookup"><span data-stu-id="726ba-131">See [**ID3DXSkinInfo**](id3dxskininfo.md).</span></span>

</dd> <dt>

<span data-ttu-id="726ba-132">**pNextMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="726ba-132">**pNextMeshContainer**</span></span>
</dt> <dd>

<span data-ttu-id="726ba-133">Tipo: \* \* \* \* D3DXMESHCONTAINER **\***</span><span class="sxs-lookup"><span data-stu-id="726ba-133">Type: \*\*\*\*D3DXMESHCONTAINER **\***</span></span>

</dd> <dd>

<span data-ttu-id="726ba-134">Ponteiro para o próximo contêiner de malha.</span><span class="sxs-lookup"><span data-stu-id="726ba-134">Pointer to the next mesh container.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="726ba-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="726ba-135">Remarks</span></span>

<span data-ttu-id="726ba-136">Um aplicativo pode derivar dessa estrutura para adicionar outros dados.</span><span class="sxs-lookup"><span data-stu-id="726ba-136">An application can derive from this structure to add other data.</span></span>

## <a name="requirements"></a><span data-ttu-id="726ba-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="726ba-137">Requirements</span></span>



| <span data-ttu-id="726ba-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="726ba-138">Requirement</span></span> | <span data-ttu-id="726ba-139">Valor</span><span class="sxs-lookup"><span data-stu-id="726ba-139">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="726ba-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="726ba-140">Header</span></span><br/> | <dl> <span data-ttu-id="726ba-141"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="726ba-141"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="726ba-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="726ba-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="726ba-143">Estruturas D3DX</span><span class="sxs-lookup"><span data-stu-id="726ba-143">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
