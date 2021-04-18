---
description: Os aplicativos usam os métodos da interface ID3DXFileSaveObject para gravar um arquivo. x em disco e para adicionar e salvar objetos de dados e modelos.
ms.assetid: 1131c151-fa21-4654-9776-484922d58487
title: Interface ID3DXFileSaveObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f8d657c327c75045cf4feb2080a2e57d80f752df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105785237"
---
# <a name="id3dxfilesaveobject-interface"></a><span data-ttu-id="f4a94-103">Interface ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="f4a94-103">ID3DXFileSaveObject interface</span></span>

<span data-ttu-id="f4a94-104">Os aplicativos usam os métodos da interface ID3DXFileSaveObject para gravar um arquivo. x em disco e para adicionar e salvar objetos de dados e modelos.</span><span class="sxs-lookup"><span data-stu-id="f4a94-104">Applications use the methods of the ID3DXFileSaveObject interface to write a .x file to disk, and to add and save data objects and templates.</span></span>

## <a name="members"></a><span data-ttu-id="f4a94-105">Membros</span><span class="sxs-lookup"><span data-stu-id="f4a94-105">Members</span></span>

<span data-ttu-id="f4a94-106">A interface **ID3DXFileSaveObject** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f4a94-106">The **ID3DXFileSaveObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f4a94-107">**ID3DXFileSaveObject** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f4a94-107">**ID3DXFileSaveObject** also has these types of members:</span></span>

-   [<span data-ttu-id="f4a94-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="f4a94-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f4a94-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="f4a94-109">Methods</span></span>

<span data-ttu-id="f4a94-110">A interface **ID3DXFileSaveObject** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f4a94-110">The **ID3DXFileSaveObject** interface has these methods.</span></span>



| <span data-ttu-id="f4a94-111">Método</span><span class="sxs-lookup"><span data-stu-id="f4a94-111">Method</span></span>                                                      | <span data-ttu-id="f4a94-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f4a94-112">Description</span></span>                                                                                                                  |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4a94-113">**Adddataobject**</span><span class="sxs-lookup"><span data-stu-id="f4a94-113">**AddDataObject**</span></span>](id3dxfilesaveobject--adddataobject.md) | <span data-ttu-id="f4a94-114">Adiciona um objeto de dados como um filho do objeto [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="f4a94-114">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span><br/>                       |
| [<span data-ttu-id="f4a94-115">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="f4a94-115">**GetFile**</span></span>](id3dxfilesaveobject--getfile.md)             | <span data-ttu-id="f4a94-116">Obtém a interface [**ID3DXFile**](id3dxfile.md) do objeto que criou este objeto **ID3DXFileSaveObject** .</span><span class="sxs-lookup"><span data-stu-id="f4a94-116">Gets the [**ID3DXFile**](id3dxfile.md) interface of the object that created this **ID3DXFileSaveObject** object.</span></span><br/> |
| [<span data-ttu-id="f4a94-117">**Salvar**</span><span class="sxs-lookup"><span data-stu-id="f4a94-117">**Save**</span></span>](id3dxfilesaveobject--save.md)                   | <span data-ttu-id="f4a94-118">Salva um objeto de dados e seus filhos em um arquivo. x no disco.</span><span class="sxs-lookup"><span data-stu-id="f4a94-118">Saves a data object and its children to a .x file on disk.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="f4a94-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="f4a94-119">Remarks</span></span>

<span data-ttu-id="f4a94-120">Os modelos não são necessários em todos os arquivos.</span><span class="sxs-lookup"><span data-stu-id="f4a94-120">Templates are not required in every file.</span></span> <span data-ttu-id="f4a94-121">Por exemplo, você pode colocar todos os modelos em um único arquivo. x em vez de duplicá-los em cada arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="f4a94-121">For example, you could put all templates into a single .x file rather than duplicating them in every .x file.</span></span>

<span data-ttu-id="f4a94-122">A interface ID3DXFileSaveObject é obtida chamando o método [**ID3DXFile:: Createsaveobject**](id3dxfile--createsaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="f4a94-122">The ID3DXFileSaveObject interface is obtained by calling the [**ID3DXFile::CreateSaveObject**](id3dxfile--createsaveobject.md) method.</span></span>

<span data-ttu-id="f4a94-123">O GUID (identificador global exclusivo) da interface ID3DXFileSaveObject é ID3DXFileSaveObject de IID \_ .</span><span class="sxs-lookup"><span data-stu-id="f4a94-123">The globally unique identifier (GUID) for the ID3DXFileSaveObject interface is IID\_ID3DXFileSaveObject.</span></span>

<span data-ttu-id="f4a94-124">O tipo LPD3DXFILESAVEOBJECT é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="f4a94-124">The LPD3DXFILESAVEOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileSaveObject *LPD3DXFILESAVEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="f4a94-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4a94-125">Requirements</span></span>



| <span data-ttu-id="f4a94-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4a94-126">Requirement</span></span> | <span data-ttu-id="f4a94-127">Valor</span><span class="sxs-lookup"><span data-stu-id="f4a94-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4a94-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f4a94-128">Header</span></span><br/>  | <dl> <span data-ttu-id="f4a94-129"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4a94-129"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="f4a94-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f4a94-130">Library</span></span><br/> | <dl> <span data-ttu-id="f4a94-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f4a94-131"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f4a94-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f4a94-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4a94-133">Interfaces de arquivo D3DX X</span><span class="sxs-lookup"><span data-stu-id="f4a94-133">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
