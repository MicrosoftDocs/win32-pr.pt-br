---
description: Define o tipo de dados de malha presentes no D3DXMESHDATA.
ms.assetid: e5324f85-17cc-46a7-886a-c8f3464baade
title: Enumeração D3DXMESHDATATYPE (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATATYPE
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: 9dea67984992e4bb26cd9e2613013169b1ff097d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105770562"
---
# <a name="d3dxmeshdatatype-enumeration"></a><span data-ttu-id="32e01-103">Enumeração D3DXMESHDATATYPE</span><span class="sxs-lookup"><span data-stu-id="32e01-103">D3DXMESHDATATYPE enumeration</span></span>

<span data-ttu-id="32e01-104">Define o tipo de dados de malha presentes no [**D3DXMESHDATA**](d3dxmeshdata.md).</span><span class="sxs-lookup"><span data-stu-id="32e01-104">Defines the type of mesh data present in [**D3DXMESHDATA**](d3dxmeshdata.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="32e01-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="32e01-105">Syntax</span></span>


```C++
typedef enum D3DXMESHDATATYPE { 
  D3DXMESHTYPE_MESH         = 0x001,
  D3DXMESHTYPE_PATCHMESH    = 0x003,
  D3DXMESHTYPE_FORCE_DWORD  = 0x7fffffff
} D3DXMESHDATATYPE, *LPD3DXMESHDATATYPE;
```



## <a name="constants"></a><span data-ttu-id="32e01-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="32e01-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="32e01-107"><span id="D3DXMESHTYPE_MESH"></span><span id="d3dxmeshtype_mesh"></span>**\_Malha D3DXMESHTYPE**</span><span class="sxs-lookup"><span data-stu-id="32e01-107"><span id="D3DXMESHTYPE_MESH"></span><span id="d3dxmeshtype_mesh"></span>**D3DXMESHTYPE\_MESH**</span></span>
</dt> <dd>

<span data-ttu-id="32e01-108">O tipo de dados é uma malha.</span><span class="sxs-lookup"><span data-stu-id="32e01-108">The data type is a mesh.</span></span> <span data-ttu-id="32e01-109">Consulte [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="32e01-109">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="32e01-110"><span id="D3DXMESHTYPE_PATCHMESH"></span><span id="d3dxmeshtype_patchmesh"></span>**D3DXMESHTYPE \_ PATCHMESH**</span><span class="sxs-lookup"><span data-stu-id="32e01-110"><span id="D3DXMESHTYPE_PATCHMESH"></span><span id="d3dxmeshtype_patchmesh"></span>**D3DXMESHTYPE\_PATCHMESH**</span></span>
</dt> <dd>

<span data-ttu-id="32e01-111">O tipo de dados é uma malha de patch.</span><span class="sxs-lookup"><span data-stu-id="32e01-111">The data type is a patch mesh.</span></span> <span data-ttu-id="32e01-112">Consulte [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span><span class="sxs-lookup"><span data-stu-id="32e01-112">See [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="32e01-113"><span id="D3DXMESHTYPE_FORCE_DWORD"></span><span id="d3dxmeshtype_force_dword"></span>**D3DXMESHTYPE \_ forçar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="32e01-113"><span id="D3DXMESHTYPE_FORCE_DWORD"></span><span id="d3dxmeshtype_force_dword"></span>**D3DXMESHTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="32e01-114">Força essa enumeração a compilar a 32 bits de tamanho.</span><span class="sxs-lookup"><span data-stu-id="32e01-114">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="32e01-115">Sem esse valor, alguns compiladores permitiriam que essa enumeração fosse compilada em um tamanho diferente de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="32e01-115">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="32e01-116">Este valor não é usado.</span><span class="sxs-lookup"><span data-stu-id="32e01-116">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32e01-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32e01-117">Requirements</span></span>



| <span data-ttu-id="32e01-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="32e01-118">Requirement</span></span> | <span data-ttu-id="32e01-119">Valor</span><span class="sxs-lookup"><span data-stu-id="32e01-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32e01-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32e01-120">Header</span></span><br/> | <dl> <span data-ttu-id="32e01-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="32e01-121"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32e01-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="32e01-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32e01-123">Enumerações D3DX</span><span class="sxs-lookup"><span data-stu-id="32e01-123">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[<span data-ttu-id="32e01-124">**D3DXMESHDATA**</span><span class="sxs-lookup"><span data-stu-id="32e01-124">**D3DXMESHDATA**</span></span>](d3dxmeshdata.md)
</dt> </dl>

 

 




