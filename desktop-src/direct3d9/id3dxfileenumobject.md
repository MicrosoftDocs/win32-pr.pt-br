---
description: Os aplicativos usam os métodos da interface ID3DXFileEnumObject para percorrer os objetos de dados do arquivo filho no arquivo e recuperar um objeto filho por seu GUID (identificador global exclusivo) ou por seu nome.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: Interface ID3DXFileEnumObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f9b28f94c8d514f81aaa51426557c825da91c4bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103930649"
---
# <a name="id3dxfileenumobject-interface"></a><span data-ttu-id="a09b1-103">Interface ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="a09b1-103">ID3DXFileEnumObject interface</span></span>

<span data-ttu-id="a09b1-104">Os aplicativos usam os métodos da interface ID3DXFileEnumObject para percorrer os objetos de dados do arquivo filho no arquivo e recuperar um objeto filho por seu GUID (identificador global exclusivo) ou por seu nome.</span><span class="sxs-lookup"><span data-stu-id="a09b1-104">Applications use the methods of the ID3DXFileEnumObject interface to cycle through the child file data objects in the file and to retrieve a child object by its globally unique identifier (GUID) or by its name.</span></span>

## <a name="members"></a><span data-ttu-id="a09b1-105">Membros</span><span class="sxs-lookup"><span data-stu-id="a09b1-105">Members</span></span>

<span data-ttu-id="a09b1-106">A interface **ID3DXFileEnumObject** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a09b1-106">The **ID3DXFileEnumObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a09b1-107">**ID3DXFileEnumObject** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a09b1-107">**ID3DXFileEnumObject** also has these types of members:</span></span>

-   [<span data-ttu-id="a09b1-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="a09b1-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a09b1-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="a09b1-109">Methods</span></span>

<span data-ttu-id="a09b1-110">A interface **ID3DXFileEnumObject** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a09b1-110">The **ID3DXFileEnumObject** interface has these methods.</span></span>



| <span data-ttu-id="a09b1-111">Método</span><span class="sxs-lookup"><span data-stu-id="a09b1-111">Method</span></span>                                                                  | <span data-ttu-id="a09b1-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a09b1-112">Description</span></span>                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="a09b1-113">**GetChild**</span><span class="sxs-lookup"><span data-stu-id="a09b1-113">**GetChild**</span></span>](id3dxfileenumobject--getchild.md)                       | <span data-ttu-id="a09b1-114">Recupera um objeto filho neste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a09b1-114">Retrieves a child object in this file data object.</span></span><br/>              |
| [<span data-ttu-id="a09b1-115">**GetChildren**</span><span class="sxs-lookup"><span data-stu-id="a09b1-115">**GetChildren**</span></span>](id3dxfileenumobject--getchildren.md)                 | <span data-ttu-id="a09b1-116">Recupera o número de objetos filho neste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="a09b1-116">Retrieves the number of child objects in this file data object.</span></span><br/> |
| [<span data-ttu-id="a09b1-117">**GetDataObjectById**</span><span class="sxs-lookup"><span data-stu-id="a09b1-117">**GetDataObjectById**</span></span>](id3dxfileenumobject--getdataobjectbyid.md)     | <span data-ttu-id="a09b1-118">Recupera o objeto de dados que tem o GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="a09b1-118">Retrieves the data object that has the specified GUID.</span></span><br/>          |
| [<span data-ttu-id="a09b1-119">**GetDataObjectByName**</span><span class="sxs-lookup"><span data-stu-id="a09b1-119">**GetDataObjectByName**</span></span>](id3dxfileenumobject--getdataobjectbyname.md) | <span data-ttu-id="a09b1-120">Recupera o objeto de dados que tem o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="a09b1-120">Retrieves the data object that has the specified name.</span></span><br/>          |
| [<span data-ttu-id="a09b1-121">**GetFile**</span><span class="sxs-lookup"><span data-stu-id="a09b1-121">**GetFile**</span></span>](id3dxfileenumobject--getfile.md)                         | <span data-ttu-id="a09b1-122">Recupera o objeto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="a09b1-122">Retrieves the [**ID3DXFile**](id3dxfile.md) object.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="a09b1-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a09b1-123">Remarks</span></span>

<span data-ttu-id="a09b1-124">O GUID da interface ID3DXFileEnumObject é ID3DXFileEnumObject IID \_ .</span><span class="sxs-lookup"><span data-stu-id="a09b1-124">The GUID for the ID3DXFileEnumObject interface is IID\_ID3DXFileEnumObject.</span></span>

<span data-ttu-id="a09b1-125">O tipo LPD3DXFILEENUMOBJECT é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="a09b1-125">The LPD3DXFILEENUMOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="a09b1-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a09b1-126">Requirements</span></span>



| <span data-ttu-id="a09b1-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a09b1-127">Requirement</span></span> | <span data-ttu-id="a09b1-128">Valor</span><span class="sxs-lookup"><span data-stu-id="a09b1-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a09b1-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a09b1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a09b1-130"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="a09b1-130"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="a09b1-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a09b1-131">Library</span></span><br/> | <dl> <span data-ttu-id="a09b1-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a09b1-132"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a09b1-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="a09b1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a09b1-134">Interfaces de arquivo D3DX X</span><span class="sxs-lookup"><span data-stu-id="a09b1-134">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
