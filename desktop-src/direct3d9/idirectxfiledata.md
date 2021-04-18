---
description: Os aplicativos usam os métodos da interface IDirectXFileData para criar ou acessar a hierarquia imediata do objeto de dados.
ms.assetid: 8810162f-76a8-45ba-b069-7910fd611a60
title: Interface IDirectXFileData (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 30d2fb26e3752e302726edce51354369f3b067eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793351"
---
# <a name="idirectxfiledata-interface"></a><span data-ttu-id="b4118-103">Interface IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="b4118-103">IDirectXFileData interface</span></span>

<span data-ttu-id="b4118-104">Os aplicativos usam os métodos da interface IDirectXFileData para criar ou acessar a hierarquia imediata do objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="b4118-104">Applications use the methods of the IDirectXFileData interface to build or to access the immediate hierarchy of the data object.</span></span> <span data-ttu-id="b4118-105">As restrições de modelo determinam a hierarquia.</span><span class="sxs-lookup"><span data-stu-id="b4118-105">Template restrictions determine the hierarchy.</span></span> <span data-ttu-id="b4118-106">Os tipos de dados permitidos pelo modelo são chamados de membros opcionais.</span><span class="sxs-lookup"><span data-stu-id="b4118-106">Data types allowed by the template are called optional members.</span></span> <span data-ttu-id="b4118-107">Os membros opcionais não são necessários, mas um objeto pode perder informações importantes sem eles.</span><span class="sxs-lookup"><span data-stu-id="b4118-107">The optional members are not required, but an object might miss important information without them.</span></span> <span data-ttu-id="b4118-108">Esses membros opcionais são salvos como filhos do objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="b4118-108">These optional members are saved as children of the data object.</span></span> <span data-ttu-id="b4118-109">Os filhos podem ser outro objeto de dados, uma referência a um objeto de dados anterior ou um objeto binário.</span><span class="sxs-lookup"><span data-stu-id="b4118-109">The children can be another data object, a reference to an earlier data object, or a binary object.</span></span> <span data-ttu-id="b4118-110">Preterido.</span><span class="sxs-lookup"><span data-stu-id="b4118-110">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="b4118-111">Membros</span><span class="sxs-lookup"><span data-stu-id="b4118-111">Members</span></span>

<span data-ttu-id="b4118-112">A interface **IDirectXFileData** herda de [**IDirectXFileObject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="b4118-112">The **IDirectXFileData** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="b4118-113">**IDirectXFileData** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b4118-113">**IDirectXFileData** also has these types of members:</span></span>

-   [<span data-ttu-id="b4118-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="b4118-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b4118-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="b4118-115">Methods</span></span>

<span data-ttu-id="b4118-116">A interface **IDirectXFileData** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="b4118-116">The **IDirectXFileData** interface has these methods.</span></span>



| <span data-ttu-id="b4118-117">Método</span><span class="sxs-lookup"><span data-stu-id="b4118-117">Method</span></span>                                                         | <span data-ttu-id="b4118-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="b4118-118">Description</span></span>                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4118-119">**Addbinaryobject**</span><span class="sxs-lookup"><span data-stu-id="b4118-119">**AddBinaryObject**</span></span>](idirectxfiledata--addbinaryobject.md)   | <span data-ttu-id="b4118-120">Cria um objeto binário e o adiciona como um objeto filho.</span><span class="sxs-lookup"><span data-stu-id="b4118-120">Creates a binary object and adds it as a child object.</span></span> <span data-ttu-id="b4118-121">Preterido.</span><span class="sxs-lookup"><span data-stu-id="b4118-121">Deprecated.</span></span><br/>                                             |
| [<span data-ttu-id="b4118-122">**Adddataobject**</span><span class="sxs-lookup"><span data-stu-id="b4118-122">**AddDataObject**</span></span>](idirectxfiledata--adddataobject.md)       | <span data-ttu-id="b4118-123">Adiciona um objeto de dados como um objeto filho.</span><span class="sxs-lookup"><span data-stu-id="b4118-123">Adds a data object as a child object.</span></span> <span data-ttu-id="b4118-124">Preterido.</span><span class="sxs-lookup"><span data-stu-id="b4118-124">Deprecated.</span></span><br/>                                                              |
| [<span data-ttu-id="b4118-125">**AddDataReference**</span><span class="sxs-lookup"><span data-stu-id="b4118-125">**AddDataReference**</span></span>](idirectxfiledata--adddatareference.md) | <span data-ttu-id="b4118-126">Cria e adiciona um objeto de referência de dados como um objeto filho.</span><span class="sxs-lookup"><span data-stu-id="b4118-126">Creates and adds a data reference object as a child object.</span></span> <span data-ttu-id="b4118-127">Preterido.</span><span class="sxs-lookup"><span data-stu-id="b4118-127">Deprecated.</span></span><br/>                                        |
| [<span data-ttu-id="b4118-128">**GetData**</span><span class="sxs-lookup"><span data-stu-id="b4118-128">**GetData**</span></span>](idirectxfiledata--getdata.md)                   | <span data-ttu-id="b4118-129">Recupera os dados para um dos membros do objeto ou os dados de todos os membros.</span><span class="sxs-lookup"><span data-stu-id="b4118-129">Retrieves the data for one of the object's members or the data for all members.</span></span> <span data-ttu-id="b4118-130">Preterido.</span><span class="sxs-lookup"><span data-stu-id="b4118-130">Deprecated.</span></span><br/>                    |
| [<span data-ttu-id="b4118-131">**GetNextObject**</span><span class="sxs-lookup"><span data-stu-id="b4118-131">**GetNextObject**</span></span>](idirectxfiledata--getnextobject.md)       | <span data-ttu-id="b4118-132">Recupera o próximo objeto de dados filho, objeto de referência de dados ou objeto binário no arquivo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="b4118-132">Retrieves the next child data object, data reference object, or binary object in the DirectX file.</span></span> <span data-ttu-id="b4118-133">Preterido.</span><span class="sxs-lookup"><span data-stu-id="b4118-133">Deprecated.</span></span><br/> |
| [<span data-ttu-id="b4118-134">**GetType**</span><span class="sxs-lookup"><span data-stu-id="b4118-134">**GetType**</span></span>](idirectxfiledata--gettype.md)                   | <span data-ttu-id="b4118-135">Recupera o GUID do modelo do objeto.</span><span class="sxs-lookup"><span data-stu-id="b4118-135">Retrieves the GUID of the object's template.</span></span> <span data-ttu-id="b4118-136">Preterido.</span><span class="sxs-lookup"><span data-stu-id="b4118-136">Deprecated.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="b4118-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4118-137">Remarks</span></span>

<span data-ttu-id="b4118-138">O GUID da interface IDirectXFileData é IDirectXFileData IID \_ .</span><span class="sxs-lookup"><span data-stu-id="b4118-138">The GUID for the IDirectXFileData interface is IID\_IDirectXFileData.</span></span>

<span data-ttu-id="b4118-139">O tipo LPDIRECTXFILEDATA é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="b4118-139">The LPDIRECTXFILEDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileData *LPDIRECTXFILEDATA;
```



## <a name="requirements"></a><span data-ttu-id="b4118-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4118-140">Requirements</span></span>



| <span data-ttu-id="b4118-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4118-141">Requirement</span></span> | <span data-ttu-id="b4118-142">Valor</span><span class="sxs-lookup"><span data-stu-id="b4118-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4118-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b4118-143">Header</span></span><br/>  | <dl> <span data-ttu-id="b4118-144"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4118-144"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4118-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b4118-145">Library</span></span><br/> | <dl> <span data-ttu-id="b4118-146"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4118-146"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4118-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4118-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4118-148">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="b4118-148">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="b4118-149">X interfaces de arquivo</span><span class="sxs-lookup"><span data-stu-id="b4118-149">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




