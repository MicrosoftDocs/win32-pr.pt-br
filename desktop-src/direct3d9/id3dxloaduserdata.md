---
description: Essa interface é implementada pelo aplicativo para salvar os dados de usuário adicionais inseridos nos arquivos. x.
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: Interface ID3DXLoadUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fcb07ba9351e5f6c23dd86c8147151932b3972ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105772532"
---
# <a name="id3dxloaduserdata-interface"></a><span data-ttu-id="4f80b-103">Interface ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="4f80b-103">ID3DXLoadUserData interface</span></span>

<span data-ttu-id="4f80b-104">Essa interface é implementada pelo aplicativo para salvar os dados de usuário adicionais inseridos nos arquivos. x.</span><span class="sxs-lookup"><span data-stu-id="4f80b-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="4f80b-105">Uma instância dessa interface é passada para [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)e D3DX chama o método apropriado nessa interface sempre que os dados apropriados são encontrados.</span><span class="sxs-lookup"><span data-stu-id="4f80b-105">An instance of this interface is passed to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="4f80b-106">Por exemplo, para cada objeto de quadro no arquivo. x, [**ID3DXLoadUserData:: LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) é chamado e passado os dados filho.</span><span class="sxs-lookup"><span data-stu-id="4f80b-106">For example, for each frame object in the .x file, [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="4f80b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="4f80b-107">Members</span></span>

<span data-ttu-id="4f80b-108">A interface **ID3DXLoadUserData** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="4f80b-108">The **ID3DXLoadUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="4f80b-109">**ID3DXLoadUserData** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4f80b-109">**ID3DXLoadUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="4f80b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="4f80b-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4f80b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="4f80b-111">Methods</span></span>

<span data-ttu-id="4f80b-112">A interface **ID3DXLoadUserData** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="4f80b-112">The **ID3DXLoadUserData** interface has these methods.</span></span>



| <span data-ttu-id="4f80b-113">Método</span><span class="sxs-lookup"><span data-stu-id="4f80b-113">Method</span></span>                                                              | <span data-ttu-id="4f80b-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="4f80b-114">Description</span></span>                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="4f80b-115">**LoadFrameChildData**</span><span class="sxs-lookup"><span data-stu-id="4f80b-115">**LoadFrameChildData**</span></span>](id3dxloaduserdata--loadframechilddata.md) | <span data-ttu-id="4f80b-116">Carregar dados filho do quadro de um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="4f80b-116">Load frame child data from a .x file.</span></span><br/> |
| [<span data-ttu-id="4f80b-117">**LoadMeshChildData**</span><span class="sxs-lookup"><span data-stu-id="4f80b-117">**LoadMeshChildData**</span></span>](id3dxloaduserdata--loadmeshchilddata.md)   | <span data-ttu-id="4f80b-118">Carregar dados filho de malha de um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="4f80b-118">Load mesh child data from a .x file.</span></span><br/>  |
| [<span data-ttu-id="4f80b-119">**LoadTopLevelData**</span><span class="sxs-lookup"><span data-stu-id="4f80b-119">**LoadTopLevelData**</span></span>](id3dxloaduserdata--loadtopleveldata.md)     | <span data-ttu-id="4f80b-120">Carregar dados de nível superior de um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="4f80b-120">Load top level data from a .x file.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="4f80b-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="4f80b-121">Remarks</span></span>

<span data-ttu-id="4f80b-122">O tipo LPD3DXLOADUSERDATA é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="4f80b-122">The LPD3DXLOADUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="4f80b-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f80b-123">Requirements</span></span>



| <span data-ttu-id="4f80b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f80b-124">Requirement</span></span> | <span data-ttu-id="4f80b-125">Valor</span><span class="sxs-lookup"><span data-stu-id="4f80b-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f80b-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f80b-126">Header</span></span><br/>  | <dl> <span data-ttu-id="4f80b-127"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f80b-127"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="4f80b-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f80b-128">Library</span></span><br/> | <dl> <span data-ttu-id="4f80b-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f80b-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4f80b-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f80b-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f80b-131">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="4f80b-131">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
