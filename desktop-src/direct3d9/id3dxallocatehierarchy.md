---
description: Essa interface é implementada pelo aplicativo para alocar ou liberar objetos de contêiner de quadro e malha. Os métodos sobre isso são chamados durante o carregamento e destruição de hierarquias de quadros.
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: Interface ID3DXAllocateHierarchy (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec7fb2da335ecd84889b75e81c850d16368f31eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012166"
---
# <a name="id3dxallocatehierarchy-interface"></a><span data-ttu-id="751f3-104">Interface ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="751f3-104">ID3DXAllocateHierarchy interface</span></span>

<span data-ttu-id="751f3-105">Essa interface é implementada pelo aplicativo para alocar ou liberar objetos de contêiner de quadro e malha.</span><span class="sxs-lookup"><span data-stu-id="751f3-105">This interface is implemented by the application to allocate or free frame and mesh container objects.</span></span> <span data-ttu-id="751f3-106">Os métodos sobre isso são chamados durante o carregamento e destruição de hierarquias de quadros.</span><span class="sxs-lookup"><span data-stu-id="751f3-106">Methods on this are called during loading and destroying frame hierarchies.</span></span>

## <a name="members"></a><span data-ttu-id="751f3-107">Membros</span><span class="sxs-lookup"><span data-stu-id="751f3-107">Members</span></span>

<span data-ttu-id="751f3-108">A interface **ID3DXAllocateHierarchy** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="751f3-108">The **ID3DXAllocateHierarchy** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="751f3-109">**ID3DXAllocateHierarchy** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="751f3-109">**ID3DXAllocateHierarchy** also has these types of members:</span></span>

-   [<span data-ttu-id="751f3-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="751f3-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="751f3-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="751f3-111">Methods</span></span>

<span data-ttu-id="751f3-112">A interface **ID3DXAllocateHierarchy** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="751f3-112">The **ID3DXAllocateHierarchy** interface has these methods.</span></span>



| <span data-ttu-id="751f3-113">Método</span><span class="sxs-lookup"><span data-stu-id="751f3-113">Method</span></span>                                                                       | <span data-ttu-id="751f3-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="751f3-114">Description</span></span>                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="751f3-115">**CreateFrame**</span><span class="sxs-lookup"><span data-stu-id="751f3-115">**CreateFrame**</span></span>](id3dxallocatehierarchy--createframe.md)                   | <span data-ttu-id="751f3-116">Solicita a alocação de um objeto de quadro.</span><span class="sxs-lookup"><span data-stu-id="751f3-116">Requests allocation of a frame object.</span></span><br/>            |
| [<span data-ttu-id="751f3-117">**CreateMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="751f3-117">**CreateMeshContainer**</span></span>](id3dxallocatehierarchy--createmeshcontainer.md)   | <span data-ttu-id="751f3-118">Solicita a alocação de um objeto de contêiner de malha.</span><span class="sxs-lookup"><span data-stu-id="751f3-118">Requests allocation of a mesh container object.</span></span><br/>   |
| [<span data-ttu-id="751f3-119">**DestroyFrame**</span><span class="sxs-lookup"><span data-stu-id="751f3-119">**DestroyFrame**</span></span>](id3dxallocatehierarchy--destroyframe.md)                 | <span data-ttu-id="751f3-120">Solicita a desalocação de um objeto de quadro.</span><span class="sxs-lookup"><span data-stu-id="751f3-120">Requests deallocation of a frame object.</span></span><br/>          |
| [<span data-ttu-id="751f3-121">**DestroyMeshContainer**</span><span class="sxs-lookup"><span data-stu-id="751f3-121">**DestroyMeshContainer**</span></span>](id3dxallocatehierarchy--destroymeshcontainer.md) | <span data-ttu-id="751f3-122">Solicita a desalocação de um objeto de contêiner de malha.</span><span class="sxs-lookup"><span data-stu-id="751f3-122">Requests deallocation of a mesh container object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="751f3-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="751f3-123">Remarks</span></span>

<span data-ttu-id="751f3-124">O tipo LPD3DXALLOCATEHIERARCHY é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="751f3-124">The LPD3DXALLOCATEHIERARCHY type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
```



## <a name="requirements"></a><span data-ttu-id="751f3-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="751f3-125">Requirements</span></span>



| <span data-ttu-id="751f3-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="751f3-126">Requirement</span></span> | <span data-ttu-id="751f3-127">Valor</span><span class="sxs-lookup"><span data-stu-id="751f3-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="751f3-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="751f3-128">Header</span></span><br/>  | <dl> <span data-ttu-id="751f3-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="751f3-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="751f3-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="751f3-130">Library</span></span><br/> | <dl> <span data-ttu-id="751f3-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="751f3-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="751f3-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="751f3-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="751f3-133">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="751f3-133">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
