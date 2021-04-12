---
description: Os aplicativos usam os métodos da interface ID3DXFileData para criar ou acessar a hierarquia imediata do objeto de dados. As restrições de modelo determinam a hierarquia.
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: Interface ID3DXFileData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1764787864c059e9c7417525a1a5ab5ff862f7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173084"
---
# <a name="id3dxfiledata-interface"></a><span data-ttu-id="78c20-104">Interface ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="78c20-104">ID3DXFileData interface</span></span>

<span data-ttu-id="78c20-105">Os aplicativos usam os métodos da interface ID3DXFileData para criar ou acessar a hierarquia imediata do objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="78c20-105">Applications use the methods of the ID3DXFileData interface to build or to access the immediate hierarchy of the data object.</span></span> <span data-ttu-id="78c20-106">As restrições de modelo determinam a hierarquia.</span><span class="sxs-lookup"><span data-stu-id="78c20-106">Template restrictions determine the hierarchy.</span></span>

## <a name="members"></a><span data-ttu-id="78c20-107">Membros</span><span class="sxs-lookup"><span data-stu-id="78c20-107">Members</span></span>

<span data-ttu-id="78c20-108">A interface **ID3DXFileData** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="78c20-108">The **ID3DXFileData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="78c20-109">**ID3DXFileData** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="78c20-109">**ID3DXFileData** also has these types of members:</span></span>

-   [<span data-ttu-id="78c20-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="78c20-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="78c20-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="78c20-111">Methods</span></span>

<span data-ttu-id="78c20-112">A interface **ID3DXFileData** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="78c20-112">The **ID3DXFileData** interface has these methods.</span></span>



| <span data-ttu-id="78c20-113">Método</span><span class="sxs-lookup"><span data-stu-id="78c20-113">Method</span></span>                                            | <span data-ttu-id="78c20-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="78c20-114">Description</span></span>                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78c20-115">**GetChild**</span><span class="sxs-lookup"><span data-stu-id="78c20-115">**GetChild**</span></span>](id3dxfiledata--getchild.md)       | <span data-ttu-id="78c20-116">Recupera um objeto filho neste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="78c20-116">Retrieves a child object in this file data object.</span></span><br/>                                                        |
| [<span data-ttu-id="78c20-117">**GetChildren**</span><span class="sxs-lookup"><span data-stu-id="78c20-117">**GetChildren**</span></span>](id3dxfiledata--getchildren.md) | <span data-ttu-id="78c20-118">Recupera o número de filhos neste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="78c20-118">Retrieves the number of children in this file data object.</span></span><br/>                                                |
| [<span data-ttu-id="78c20-119">**Getenum**</span><span class="sxs-lookup"><span data-stu-id="78c20-119">**GetEnum**</span></span>](id3dxfiledata--getenum.md)         | <span data-ttu-id="78c20-120">Recupera o objeto de enumeração neste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="78c20-120">Retrieves the enumeration object in this file data object.</span></span><br/>                                                |
| [<span data-ttu-id="78c20-121">**GetId**</span><span class="sxs-lookup"><span data-stu-id="78c20-121">**GetId**</span></span>](id3dxfiledata--getid.md)             | <span data-ttu-id="78c20-122">Recupera o GUID deste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="78c20-122">Retrieves the GUID of this file data object.</span></span><br/>                                                              |
| [<span data-ttu-id="78c20-123">**GetName**</span><span class="sxs-lookup"><span data-stu-id="78c20-123">**GetName**</span></span>](id3dxfiledata--getname.md)         | <span data-ttu-id="78c20-124">Recupera o nome deste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="78c20-124">Retrieves the name of this file data object.</span></span><br/>                                                              |
| [<span data-ttu-id="78c20-125">**GetType**</span><span class="sxs-lookup"><span data-stu-id="78c20-125">**GetType**</span></span>](id3dxfiledata--gettype.md)         | <span data-ttu-id="78c20-126">Recupera a ID do modelo neste objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="78c20-126">Retrieves the template ID in this file data object.</span></span><br/>                                                       |
| [<span data-ttu-id="78c20-127">**IsReference**</span><span class="sxs-lookup"><span data-stu-id="78c20-127">**IsReference**</span></span>](id3dxfiledata--isreference.md) | <span data-ttu-id="78c20-128">Indica se este objeto de dados de arquivo é um objeto de referência que aponta para outro objeto de dados filho.</span><span class="sxs-lookup"><span data-stu-id="78c20-128">Indicates whether this file data object is a reference object that points to another child data object.</span></span><br/>   |
| [<span data-ttu-id="78c20-129">**Bloquear**</span><span class="sxs-lookup"><span data-stu-id="78c20-129">**Lock**</span></span>](id3dxfiledata--lock.md)               | <span data-ttu-id="78c20-130">Acessa os dados do arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="78c20-130">Accesses the .x file data.</span></span><br/>                                                                                |
| [<span data-ttu-id="78c20-131">**Unlock**</span><span class="sxs-lookup"><span data-stu-id="78c20-131">**Unlock**</span></span>](id3dxfiledata--unlock.md)           | <span data-ttu-id="78c20-132">Termina o ciclo de vida do ponteiro *ppData* retornado por [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md).</span><span class="sxs-lookup"><span data-stu-id="78c20-132">Ends the lifespan of the *ppData* pointer returned by [**ID3DXFileData::Lock**](id3dxfiledata--lock.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="78c20-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="78c20-133">Remarks</span></span>

<span data-ttu-id="78c20-134">Os tipos de dados permitidos pelo modelo são chamados de membros opcionais.</span><span class="sxs-lookup"><span data-stu-id="78c20-134">Data types allowed by the template are called optional members.</span></span> <span data-ttu-id="78c20-135">Os membros opcionais não são necessários, mas um objeto pode perder informações importantes sem eles.</span><span class="sxs-lookup"><span data-stu-id="78c20-135">The optional members are not required, but an object might miss important information without them.</span></span> <span data-ttu-id="78c20-136">Esses membros opcionais são salvos como filhos do objeto de dados.</span><span class="sxs-lookup"><span data-stu-id="78c20-136">These optional members are saved as children of the data object.</span></span> <span data-ttu-id="78c20-137">Um filho pode ser outro objeto de dados ou uma referência a um objeto de dados anterior.</span><span class="sxs-lookup"><span data-stu-id="78c20-137">A child can be another data object or a reference to an earlier data object.</span></span>

<span data-ttu-id="78c20-138">O GUID da interface ID3DXFileData é ID3DXFileData IID \_ .</span><span class="sxs-lookup"><span data-stu-id="78c20-138">The GUID for the ID3DXFileData interface is IID\_ID3DXFileData.</span></span>

<span data-ttu-id="78c20-139">O tipo LPD3DXFILEDATA é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="78c20-139">The LPD3DXFILEDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
```



## <a name="requirements"></a><span data-ttu-id="78c20-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78c20-140">Requirements</span></span>



| <span data-ttu-id="78c20-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="78c20-141">Requirement</span></span> | <span data-ttu-id="78c20-142">Valor</span><span class="sxs-lookup"><span data-stu-id="78c20-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78c20-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="78c20-143">Header</span></span><br/>  | <dl> <span data-ttu-id="78c20-144"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="78c20-144"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="78c20-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="78c20-145">Library</span></span><br/> | <dl> <span data-ttu-id="78c20-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78c20-146"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="78c20-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="78c20-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78c20-148">Interfaces de arquivo D3DX X</span><span class="sxs-lookup"><span data-stu-id="78c20-148">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
