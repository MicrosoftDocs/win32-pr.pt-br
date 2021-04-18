---
description: Os aplicativos usam os métodos da interface ID3DXFile para criar instâncias das interfaces ID3DXFileEnumObject e ID3DXFileSaveObject e para registrar modelos.
ms.assetid: 472d45b1-5c03-4417-a005-91f802667919
title: Interface ID3DXFile (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 45af79c4fb01c95b25803788f79588a3880fe264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105761630"
---
# <a name="id3dxfile-interface"></a><span data-ttu-id="86d10-103">Interface ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="86d10-103">ID3DXFile interface</span></span>

<span data-ttu-id="86d10-104">Os aplicativos usam os métodos da interface ID3DXFile para criar instâncias das interfaces [**ID3DXFileEnumObject**](id3dxfileenumobject.md) e [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) e para registrar modelos.</span><span class="sxs-lookup"><span data-stu-id="86d10-104">Applications use the methods of the ID3DXFile interface to create instances of the [**ID3DXFileEnumObject**](id3dxfileenumobject.md) and [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interfaces, and to register templates.</span></span>

## <a name="members"></a><span data-ttu-id="86d10-105">Membros</span><span class="sxs-lookup"><span data-stu-id="86d10-105">Members</span></span>

<span data-ttu-id="86d10-106">A interface **ID3DXFile** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="86d10-106">The **ID3DXFile** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="86d10-107">**ID3DXFile** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="86d10-107">**ID3DXFile** also has these types of members:</span></span>

-   [<span data-ttu-id="86d10-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="86d10-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="86d10-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="86d10-109">Methods</span></span>

<span data-ttu-id="86d10-110">A interface **ID3DXFile** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="86d10-110">The **ID3DXFile** interface has these methods.</span></span>



| <span data-ttu-id="86d10-111">Método</span><span class="sxs-lookup"><span data-stu-id="86d10-111">Method</span></span>                                                            | <span data-ttu-id="86d10-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="86d10-112">Description</span></span>                                                                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="86d10-113">**Createenumobject**</span><span class="sxs-lookup"><span data-stu-id="86d10-113">**CreateEnumObject**</span></span>](id3dxfile--createenumobject.md)           | <span data-ttu-id="86d10-114">Cria um objeto enumerador que lerá um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="86d10-114">Creates an enumerator object that will read a .x file.</span></span><br/>                                                      |
| [<span data-ttu-id="86d10-115">**Createsaveobject**</span><span class="sxs-lookup"><span data-stu-id="86d10-115">**CreateSaveObject**</span></span>](id3dxfile--createsaveobject.md)           | <span data-ttu-id="86d10-116">Cria um objeto salvar que será usado para salvar dados em um arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="86d10-116">Creates a save object that will be used to save data to a .x file.</span></span><br/>                                          |
| [<span data-ttu-id="86d10-117">**RegisterEnumTemplates**</span><span class="sxs-lookup"><span data-stu-id="86d10-117">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md) | <span data-ttu-id="86d10-118">Registra modelos personalizados, dado um objeto de enumeração [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="86d10-118">Registers custom templates, given an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object.</span></span><br/> |
| [<span data-ttu-id="86d10-119">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="86d10-119">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)         | <span data-ttu-id="86d10-120">Registra modelos personalizados.</span><span class="sxs-lookup"><span data-stu-id="86d10-120">Registers custom templates.</span></span><br/>                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="86d10-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="86d10-121">Remarks</span></span>

<span data-ttu-id="86d10-122">Um objeto ID3DXFile também contém um repositório de modelos local.</span><span class="sxs-lookup"><span data-stu-id="86d10-122">An ID3DXFile object also contains a local template store.</span></span> <span data-ttu-id="86d10-123">Esse armazenamento local pode ser adicionado somente aos métodos [**ID3DXFile:: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) e [**ID3DXFile:: RegisterTemplates**](id3dxfile--registertemplates.md) .</span><span class="sxs-lookup"><span data-stu-id="86d10-123">This local storage may be added to only with the [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) and [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) methods.</span></span>

<span data-ttu-id="86d10-124">Os objetos [**ID3DXFileEnumObject**](id3dxfileenumobject.md) e [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) criados com [**ID3DXFile:: createenumobject**](id3dxfile--createenumobject.md) e [**ID3DXFile:: createsaveobject**](id3dxfile--createsaveobject.md) também utilizam o repositório de modelos do objeto pai ID3DXFile.</span><span class="sxs-lookup"><span data-stu-id="86d10-124">[**ID3DXFileEnumObject**](id3dxfileenumobject.md) and [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) objects created with [**ID3DXFile::CreateEnumObject**](id3dxfile--createenumobject.md) and [**ID3DXFile::CreateSaveObject**](id3dxfile--createsaveobject.md) also utilize the template store of the parent ID3DXFile object.</span></span>

<span data-ttu-id="86d10-125">A interface ID3DXFile é obtida chamando a função [**D3DXFileCreate**](d3dxfilecreate.md) .</span><span class="sxs-lookup"><span data-stu-id="86d10-125">The ID3DXFile interface is obtained by calling the [**D3DXFileCreate**](d3dxfilecreate.md) function.</span></span>

<span data-ttu-id="86d10-126">O GUID (identificador global exclusivo) da interface ID3DXFile é ID3DXFile de IID \_ .</span><span class="sxs-lookup"><span data-stu-id="86d10-126">The globally unique identifier (GUID) for the ID3DXFile interface is IID\_ID3DXFile.</span></span>

<span data-ttu-id="86d10-127">O tipo LPD3DXFILE é definido como um ponteiro para a interface ID3DXFile.</span><span class="sxs-lookup"><span data-stu-id="86d10-127">The LPD3DXFILE type is defined as a pointer to the ID3DXFile interface.</span></span>


```
typedef interface ID3DXFile *LPD3DXFILE;
```



## <a name="requirements"></a><span data-ttu-id="86d10-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86d10-128">Requirements</span></span>



| <span data-ttu-id="86d10-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="86d10-129">Requirement</span></span> | <span data-ttu-id="86d10-130">Valor</span><span class="sxs-lookup"><span data-stu-id="86d10-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86d10-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="86d10-131">Header</span></span><br/>  | <dl> <span data-ttu-id="86d10-132"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="86d10-132"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="86d10-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="86d10-133">Library</span></span><br/> | <dl> <span data-ttu-id="86d10-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86d10-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="86d10-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="86d10-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86d10-136">Interfaces de arquivo D3DX X</span><span class="sxs-lookup"><span data-stu-id="86d10-136">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
