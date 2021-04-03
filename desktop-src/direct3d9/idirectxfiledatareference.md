---
description: Os aplicativos usam os métodos da interface IDirectXFileDataReference para dar suporte a objetos de referência de dados.
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: Interface IDirectXFileDataReference (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: d04d2367f914c2e8d64a3c9c64fb55df1e51e47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104092009"
---
# <a name="idirectxfiledatareference-interface"></a><span data-ttu-id="b4f1f-103">Interface IDirectXFileDataReference</span><span class="sxs-lookup"><span data-stu-id="b4f1f-103">IDirectXFileDataReference interface</span></span>

<span data-ttu-id="b4f1f-104">Os aplicativos usam os métodos da interface IDirectXFileDataReference para dar suporte a objetos de referência de dados.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-104">Applications use the methods of the IDirectXFileDataReference interface to support data reference objects.</span></span> <span data-ttu-id="b4f1f-105">Um objeto de referência de dados refere-se a um objeto de dados que é definido anteriormente no arquivo.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-105">A data reference object refers to a data object that is defined earlier in the file.</span></span> <span data-ttu-id="b4f1f-106">Isso permite que você use o mesmo objeto várias vezes sem repeti-lo no arquivo.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-106">This enables you to use the same object multiple times without repeating it in the file.</span></span> <span data-ttu-id="b4f1f-107">Preterido.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-107">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="b4f1f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="b4f1f-108">Members</span></span>

<span data-ttu-id="b4f1f-109">A interface **IDirectXFileDataReference** herda de [**IDirectXFileObject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="b4f1f-109">The **IDirectXFileDataReference** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="b4f1f-110">**IDirectXFileDataReference** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b4f1f-110">**IDirectXFileDataReference** also has these types of members:</span></span>

-   [<span data-ttu-id="b4f1f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b4f1f-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b4f1f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="b4f1f-112">Methods</span></span>

<span data-ttu-id="b4f1f-113">A interface **IDirectXFileDataReference** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-113">The **IDirectXFileDataReference** interface has these methods.</span></span>



| <span data-ttu-id="b4f1f-114">Método</span><span class="sxs-lookup"><span data-stu-id="b4f1f-114">Method</span></span>                                                | <span data-ttu-id="b4f1f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4f1f-115">Description</span></span>                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="b4f1f-116">**Resolver**</span><span class="sxs-lookup"><span data-stu-id="b4f1f-116">**Resolve**</span></span>](idirectxfiledatareference--resolve.md) | <span data-ttu-id="b4f1f-117">Resolve referências de dados.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-117">Resolves data references.</span></span> <span data-ttu-id="b4f1f-118">Preterido.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-118">Deprecated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4f1f-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4f1f-119">Remarks</span></span>

<span data-ttu-id="b4f1f-120">Depois de determinar que um objeto é um objeto de referência de dados, use o método [**IDirectXFileDataReference:: resolve**](idirectxfiledatareference--resolve.md) para recuperar o objeto referenciado definido anteriormente no arquivo.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-120">After you have determined that an object is a data reference object, use the [**IDirectXFileDataReference::Resolve**](idirectxfiledatareference--resolve.md) method to retrieve the referenced object defined earlier in the file.</span></span> <span data-ttu-id="b4f1f-121">Para obter informações sobre como identificar um objeto de referência de dados, consulte a interface [**IDirectXFileData**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="b4f1f-121">For information about how to identify a data reference object, see the [**IDirectXFileData**](idirectxfiledata.md) interface.</span></span>

<span data-ttu-id="b4f1f-122">O GUID da interface IDirectXFileDataReference é IDirectXFileDataReference IID \_ .</span><span class="sxs-lookup"><span data-stu-id="b4f1f-122">The GUID for the IDirectXFileDataReference interface is IID\_IDirectXFileDataReference.</span></span>

<span data-ttu-id="b4f1f-123">O tipo LPDIRECTXFILEDataReference é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="b4f1f-123">The LPDIRECTXFILEDataReference type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
```



## <a name="requirements"></a><span data-ttu-id="b4f1f-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4f1f-124">Requirements</span></span>



| <span data-ttu-id="b4f1f-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4f1f-125">Requirement</span></span> | <span data-ttu-id="b4f1f-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b4f1f-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f1f-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4f1f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="b4f1f-128"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4f1f-128"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4f1f-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4f1f-129">Library</span></span><br/> | <dl> <span data-ttu-id="b4f1f-130"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4f1f-130"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4f1f-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4f1f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4f1f-132">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="b4f1f-132">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="b4f1f-133">X interfaces de arquivo</span><span class="sxs-lookup"><span data-stu-id="b4f1f-133">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




