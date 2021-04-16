---
description: Os aplicativos usam os métodos da interface IDirectXFileEnumObject para percorrer os objetos de dados no arquivo e recuperar um objeto de dados por seu GUID (identificador global exclusivo) ou por seu nome. Preterido.
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: Interface IDirectXFileEnumObject (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: f9220f6e0a406cb4143798787276d7aa6cb5f5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105779406"
---
# <a name="idirectxfileenumobject-interface"></a><span data-ttu-id="1c050-104">Interface IDirectXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="1c050-104">IDirectXFileEnumObject interface</span></span>

<span data-ttu-id="1c050-105">Os aplicativos usam os métodos da interface IDirectXFileEnumObject para percorrer os objetos de dados no arquivo e recuperar um objeto de dados por seu GUID (identificador global exclusivo) ou por seu nome.</span><span class="sxs-lookup"><span data-stu-id="1c050-105">Applications use the methods of the IDirectXFileEnumObject interface to cycle through the data objects in the file and to retrieve a data object by its globally unique identifier (GUID) or by its name.</span></span> <span data-ttu-id="1c050-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="1c050-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="1c050-107">Membros</span><span class="sxs-lookup"><span data-stu-id="1c050-107">Members</span></span>

<span data-ttu-id="1c050-108">A interface **IDirectXFileEnumObject** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1c050-108">The **IDirectXFileEnumObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1c050-109">**IDirectXFileEnumObject** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1c050-109">**IDirectXFileEnumObject** also has these types of members:</span></span>

-   [<span data-ttu-id="1c050-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c050-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1c050-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="1c050-111">Methods</span></span>

<span data-ttu-id="1c050-112">A interface **IDirectXFileEnumObject** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1c050-112">The **IDirectXFileEnumObject** interface has these methods.</span></span>



| <span data-ttu-id="1c050-113">Método</span><span class="sxs-lookup"><span data-stu-id="1c050-113">Method</span></span>                                                                     | <span data-ttu-id="1c050-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1c050-114">Description</span></span>                                                                     |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="1c050-115">**GetDataObjectById**</span><span class="sxs-lookup"><span data-stu-id="1c050-115">**GetDataObjectById**</span></span>](idirectxfileenumobject--getdataobjectbyid.md)     | <span data-ttu-id="1c050-116">Recupera o objeto de dados que tem o GUID especificado.</span><span class="sxs-lookup"><span data-stu-id="1c050-116">Retrieves the data object that has the specified GUID.</span></span> <span data-ttu-id="1c050-117">Preterido.</span><span class="sxs-lookup"><span data-stu-id="1c050-117">Deprecated.</span></span><br/>   |
| [<span data-ttu-id="1c050-118">**GetDataObjectByName**</span><span class="sxs-lookup"><span data-stu-id="1c050-118">**GetDataObjectByName**</span></span>](idirectxfileenumobject--getdataobjectbyname.md) | <span data-ttu-id="1c050-119">Recupera o objeto de dados que tem o nome especificado.</span><span class="sxs-lookup"><span data-stu-id="1c050-119">Retrieves the data object that has the specified name.</span></span> <span data-ttu-id="1c050-120">Preterido.</span><span class="sxs-lookup"><span data-stu-id="1c050-120">Deprecated.</span></span><br/>   |
| [<span data-ttu-id="1c050-121">**GetNextDataObject**</span><span class="sxs-lookup"><span data-stu-id="1c050-121">**GetNextDataObject**</span></span>](idirectxfileenumobject--getnextdataobject.md)     | <span data-ttu-id="1c050-122">Recupera o próximo objeto de nível superior no arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="1c050-122">Retrieves the next top-level object in the DirectX file.</span></span> <span data-ttu-id="1c050-123">Preterido.</span><span class="sxs-lookup"><span data-stu-id="1c050-123">Deprecated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c050-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c050-124">Remarks</span></span>

<span data-ttu-id="1c050-125">O GUID da interface IDirectXFileEnumObject é IDirectXFileEnumObject IID \_ .</span><span class="sxs-lookup"><span data-stu-id="1c050-125">The GUID for the IDirectXFileEnumObject interface is IID\_IDirectXFileEnumObject.</span></span>

<span data-ttu-id="1c050-126">O tipo LPDIRECTXFILEENUMOBJECT é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="1c050-126">The LPDIRECTXFILEENUMOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileEnumObject *LPDIRECTXFILEENUMOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="1c050-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c050-127">Requirements</span></span>



| <span data-ttu-id="1c050-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c050-128">Requirement</span></span> | <span data-ttu-id="1c050-129">Valor</span><span class="sxs-lookup"><span data-stu-id="1c050-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c050-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1c050-130">Header</span></span><br/>  | <dl> <span data-ttu-id="1c050-131"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c050-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c050-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1c050-132">Library</span></span><br/> | <dl> <span data-ttu-id="1c050-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c050-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c050-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c050-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c050-135">X interfaces de arquivo</span><span class="sxs-lookup"><span data-stu-id="1c050-135">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
