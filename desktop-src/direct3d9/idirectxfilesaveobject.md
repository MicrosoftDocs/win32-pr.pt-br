---
description: Os aplicativos usam os métodos da interface IDirectXFileSaveObject para criar objetos de dados e para salvar modelos e objetos de dados.
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: Interface IDirectXFileSaveObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 4be69b10037381d4b06466d52483427b6d40499a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105811996"
---
# <a name="idirectxfilesaveobject-interface"></a><span data-ttu-id="013e8-103">Interface IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="013e8-103">IDirectXFileSaveObject interface</span></span>

<span data-ttu-id="013e8-104">Os aplicativos usam os métodos da interface IDirectXFileSaveObject para criar objetos de dados e para salvar modelos e objetos de dados.</span><span class="sxs-lookup"><span data-stu-id="013e8-104">Applications use the methods of the IDirectXFileSaveObject interface to create data objects and to save templates and data objects.</span></span> <span data-ttu-id="013e8-105">Observe que os modelos não são necessários em todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="013e8-105">Note that templates are not required in every file.</span></span> <span data-ttu-id="013e8-106">Por exemplo, você pode colocar todos os modelos em um único arquivo do Microsoft DirectX em vez de duplicá-los em todos os arquivos do DirectX.</span><span class="sxs-lookup"><span data-stu-id="013e8-106">For example, you could put all templates into a single Microsoft DirectX file rather than duplicating them in every DirectX file.</span></span> <span data-ttu-id="013e8-107">Preterido.</span><span class="sxs-lookup"><span data-stu-id="013e8-107">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="013e8-108">Membros</span><span class="sxs-lookup"><span data-stu-id="013e8-108">Members</span></span>

<span data-ttu-id="013e8-109">A interface **IDirectXFileSaveObject** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="013e8-109">The **IDirectXFileSaveObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="013e8-110">**IDirectXFileSaveObject** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="013e8-110">**IDirectXFileSaveObject** also has these types of members:</span></span>

-   [<span data-ttu-id="013e8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="013e8-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="013e8-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="013e8-112">Methods</span></span>

<span data-ttu-id="013e8-113">A interface **IDirectXFileSaveObject** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="013e8-113">The **IDirectXFileSaveObject** interface has these methods.</span></span>



| <span data-ttu-id="013e8-114">Método</span><span class="sxs-lookup"><span data-stu-id="013e8-114">Method</span></span>                                                               | <span data-ttu-id="013e8-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="013e8-115">Description</span></span>                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="013e8-116">**Createdataobject**</span><span class="sxs-lookup"><span data-stu-id="013e8-116">**CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md) | <span data-ttu-id="013e8-117">Cria um objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="013e8-117">Creates a data object.</span></span> <span data-ttu-id="013e8-118">Preterido.</span><span class="sxs-lookup"><span data-stu-id="013e8-118">Deprecated.</span></span><br/>                                  |
| [<span data-ttu-id="013e8-119">**SaveData**</span><span class="sxs-lookup"><span data-stu-id="013e8-119">**SaveData**</span></span>](idirectxfilesaveobject--savedata.md)                 | <span data-ttu-id="013e8-120">Salva um objeto de dados e seus filhos em um arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="013e8-120">Saves a data object and its children to a DirectX file.</span></span> <span data-ttu-id="013e8-121">Preterido.</span><span class="sxs-lookup"><span data-stu-id="013e8-121">Deprecated.</span></span><br/> |
| [<span data-ttu-id="013e8-122">**SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="013e8-122">**SaveTemplates**</span></span>](idirectxfilesaveobject--savetemplates.md)       | <span data-ttu-id="013e8-123">Salva modelos em um arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="013e8-123">Saves templates to a DirectX file.</span></span> <span data-ttu-id="013e8-124">Preterido.</span><span class="sxs-lookup"><span data-stu-id="013e8-124">Deprecated.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="013e8-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="013e8-125">Remarks</span></span>

<span data-ttu-id="013e8-126">O GUID (identificador global exclusivo) da interface IDirectXFileSaveObject é IDirectXFileSaveObject de **IID \_**.</span><span class="sxs-lookup"><span data-stu-id="013e8-126">The globally unique identifier (GUID) for the IDirectXFileSaveObject interface is **IID\_IDirectXFileSaveObject**.</span></span>

<span data-ttu-id="013e8-127">A interface **IDirectXFileSaveObject** é obtida chamando o método [**IDirectXFile:: createsaveobject**](idirectxfile--createsaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="013e8-127">The **IDirectXFileSaveObject** interface is obtained by calling the [**IDirectXFile::CreateSaveObject**](idirectxfile--createsaveobject.md) method.</span></span>

<span data-ttu-id="013e8-128">O tipo **LPDIRECTXFILESAVEOBJECT** é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="013e8-128">The **LPDIRECTXFILESAVEOBJECT** type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="013e8-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="013e8-129">Requirements</span></span>



| <span data-ttu-id="013e8-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="013e8-130">Requirement</span></span> | <span data-ttu-id="013e8-131">Valor</span><span class="sxs-lookup"><span data-stu-id="013e8-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="013e8-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="013e8-132">Header</span></span><br/>  | <dl> <span data-ttu-id="013e8-133"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="013e8-133"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="013e8-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="013e8-134">Library</span></span><br/> | <dl> <span data-ttu-id="013e8-135"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="013e8-135"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="013e8-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="013e8-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="013e8-137">X interfaces de arquivo</span><span class="sxs-lookup"><span data-stu-id="013e8-137">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
