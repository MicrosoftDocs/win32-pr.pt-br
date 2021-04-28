---
description: Interface ID3DXSaveUserData – essa interface é implementada pelo aplicativo para salvar os dados de usuário adicionais inseridos nos arquivos. x.
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: Interface ID3DXSaveUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5dbdc71239455772809e44f535634a0d06cc0653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107174"
---
# <a name="id3dxsaveuserdata-interface"></a><span data-ttu-id="f6ecd-103">Interface ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="f6ecd-103">ID3DXSaveUserData interface</span></span>

<span data-ttu-id="f6ecd-104">Essa interface é implementada pelo aplicativo para salvar os dados de usuário adicionais inseridos nos arquivos. x.</span><span class="sxs-lookup"><span data-stu-id="f6ecd-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="f6ecd-105">Uma instância dessa interface é passada para [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md)e D3DX chama o método apropriado nessa interface sempre que os dados apropriados são encontrados.</span><span class="sxs-lookup"><span data-stu-id="f6ecd-105">An instance of this interface is passed to [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="f6ecd-106">Por exemplo, para cada objeto de quadro no arquivo. x, [**ID3DXSaveUserData:: AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) é chamado e passado os dados filho.</span><span class="sxs-lookup"><span data-stu-id="f6ecd-106">For example, for each frame object in the .x file, [**ID3DXSaveUserData::AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="f6ecd-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f6ecd-107">Members</span></span>

<span data-ttu-id="f6ecd-108">A interface **ID3DXSaveUserData** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f6ecd-108">The **ID3DXSaveUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f6ecd-109">**ID3DXSaveUserData** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f6ecd-109">**ID3DXSaveUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="f6ecd-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="f6ecd-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f6ecd-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="f6ecd-111">Methods</span></span>

<span data-ttu-id="f6ecd-112">A interface **ID3DXSaveUserData** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f6ecd-112">The **ID3DXSaveUserData** interface has these methods.</span></span>



| <span data-ttu-id="f6ecd-113">Método</span><span class="sxs-lookup"><span data-stu-id="f6ecd-113">Method</span></span>                                                                              | <span data-ttu-id="f6ecd-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6ecd-114">Description</span></span>                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="f6ecd-115">**AddFrameChildData**</span><span class="sxs-lookup"><span data-stu-id="f6ecd-115">**AddFrameChildData**</span></span>](id3dxsaveuserdata--addframechilddata.md)                   | <span data-ttu-id="f6ecd-116">Adicione dados filho ao quadro.</span><span class="sxs-lookup"><span data-stu-id="f6ecd-116">Add child data to the frame.</span></span><br/>                            |
| [<span data-ttu-id="f6ecd-117">**AddMeshChildData**</span><span class="sxs-lookup"><span data-stu-id="f6ecd-117">**AddMeshChildData**</span></span>](id3dxsaveuserdata--addmeshchilddata.md)                     | <span data-ttu-id="f6ecd-118">Adicione dados filho à malha.</span><span class="sxs-lookup"><span data-stu-id="f6ecd-118">Add child data to the mesh.</span></span><br/>                             |
| [<span data-ttu-id="f6ecd-119">**AddTopLevelDataObjectsPost**</span><span class="sxs-lookup"><span data-stu-id="f6ecd-119">**AddTopLevelDataObjectsPost**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspost.md) | <span data-ttu-id="f6ecd-120">Adicione um objeto de nível superior após a hierarquia de quadros.</span><span class="sxs-lookup"><span data-stu-id="f6ecd-120">Add a top level object after the frame hierarchy.</span></span><br/>       |
| [<span data-ttu-id="f6ecd-121">**AddTopLevelDataObjectsPre**</span><span class="sxs-lookup"><span data-stu-id="f6ecd-121">**AddTopLevelDataObjectsPre**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | <span data-ttu-id="f6ecd-122">Adicione um objeto de nível superior antes da hierarquia de quadros.</span><span class="sxs-lookup"><span data-stu-id="f6ecd-122">Add a top level object before the frame hierarchy.</span></span><br/>      |
| [<span data-ttu-id="f6ecd-123">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="f6ecd-123">**RegisterTemplates**</span></span>](id3dxsaveuserdata--registertemplates.md)                   | <span data-ttu-id="f6ecd-124">Um retorno de chamada para o usuário registrar um modelo de arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="f6ecd-124">A callback for the user to register a .x file template.</span></span><br/> |
| [<span data-ttu-id="f6ecd-125">**SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="f6ecd-125">**SaveTemplates**</span></span>](id3dxsaveuserdata--savetemplates.md)                           | <span data-ttu-id="f6ecd-126">Um retorno de chamada para o usuário salvar um modelo de arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="f6ecd-126">A callback for the user to save a .x file template.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="f6ecd-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6ecd-127">Remarks</span></span>

<span data-ttu-id="f6ecd-128">O tipo LPD3DXSAVEUSERDATA é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="f6ecd-128">The LPD3DXSAVEUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="f6ecd-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6ecd-129">Requirements</span></span>



| <span data-ttu-id="f6ecd-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6ecd-130">Requirement</span></span> | <span data-ttu-id="f6ecd-131">Valor</span><span class="sxs-lookup"><span data-stu-id="f6ecd-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f6ecd-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f6ecd-132">Header</span></span><br/>  | <dl> <span data-ttu-id="f6ecd-133"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6ecd-133"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="f6ecd-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f6ecd-134">Library</span></span><br/> | <dl> <span data-ttu-id="f6ecd-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f6ecd-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f6ecd-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="f6ecd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6ecd-137">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="f6ecd-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
