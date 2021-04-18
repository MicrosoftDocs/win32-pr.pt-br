---
description: Os aplicativos usam os métodos da interface ID3DXFileSaveData para adicionar objetos de dados como filhos de um nó de dados de arquivo. x.
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: Interface ID3DXFileSaveData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d42f431dbb2f9108c5e503aea07ba6b11915f0ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105810725"
---
# <a name="id3dxfilesavedata-interface"></a><span data-ttu-id="8543b-103">Interface ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="8543b-103">ID3DXFileSaveData interface</span></span>

<span data-ttu-id="8543b-104">Os aplicativos usam os métodos da interface ID3DXFileSaveData para adicionar objetos de dados como filhos de um nó de dados de arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="8543b-104">Applications use the methods of the ID3DXFileSaveData interface to add data objects as children of a .x file data node.</span></span>

## <a name="members"></a><span data-ttu-id="8543b-105">Membros</span><span class="sxs-lookup"><span data-stu-id="8543b-105">Members</span></span>

<span data-ttu-id="8543b-106">A interface **ID3DXFileSaveData** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8543b-106">The **ID3DXFileSaveData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8543b-107">**ID3DXFileSaveData** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8543b-107">**ID3DXFileSaveData** also has these types of members:</span></span>

-   [<span data-ttu-id="8543b-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="8543b-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8543b-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="8543b-109">Methods</span></span>

<span data-ttu-id="8543b-110">A interface **ID3DXFileSaveData** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="8543b-110">The **ID3DXFileSaveData** interface has these methods.</span></span>



| <span data-ttu-id="8543b-111">Método</span><span class="sxs-lookup"><span data-stu-id="8543b-111">Method</span></span>                                                          | <span data-ttu-id="8543b-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="8543b-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8543b-113">**Adddataobject**</span><span class="sxs-lookup"><span data-stu-id="8543b-113">**AddDataObject**</span></span>](id3dxfilesavedata--adddataobject.md)       | <span data-ttu-id="8543b-114">Adiciona um objeto de dados como um filho do nó de dados do arquivo **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="8543b-114">Adds a data object as a child of the **ID3DXFileSaveData** file data node.</span></span><br/>                                                      |
| [<span data-ttu-id="8543b-115">**AddDataReference**</span><span class="sxs-lookup"><span data-stu-id="8543b-115">**AddDataReference**</span></span>](id3dxfilesavedata--adddatareference.md) | <span data-ttu-id="8543b-116">Adiciona uma referência de dados como um filho deste nó de dados do arquivo **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="8543b-116">Adds a data reference as a child of this **ID3DXFileSaveData** file data node.</span></span> <span data-ttu-id="8543b-117">A referência de dados aponta para um objeto de dados de arquivo.</span><span class="sxs-lookup"><span data-stu-id="8543b-117">The data reference points to a file data object.</span></span><br/> |
| [<span data-ttu-id="8543b-118">**GetId**</span><span class="sxs-lookup"><span data-stu-id="8543b-118">**GetId**</span></span>](id3dxfilesavedata--getid.md)                       | <span data-ttu-id="8543b-119">Recupera o GUID deste nó de dados do arquivo **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="8543b-119">Retrieves the GUID of this **ID3DXFileSaveData** file data node.</span></span><br/>                                                                |
| [<span data-ttu-id="8543b-120">**GetName**</span><span class="sxs-lookup"><span data-stu-id="8543b-120">**GetName**</span></span>](id3dxfilesavedata--getname.md)                   | <span data-ttu-id="8543b-121">Recupera o nome deste nó de dados do arquivo **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="8543b-121">Retrieves the name of this **ID3DXFileSaveData** file data node.</span></span><br/>                                                                |
| [<span data-ttu-id="8543b-122">**Getsave**</span><span class="sxs-lookup"><span data-stu-id="8543b-122">**GetSave**</span></span>](id3dxfilesavedata--getsave.md)                   | <span data-ttu-id="8543b-123">Recupera um ponteiro para este nó de dados do arquivo [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="8543b-123">Retrieves a pointer to this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) file data node.</span></span><br/>                                  |
| [<span data-ttu-id="8543b-124">**GetType**</span><span class="sxs-lookup"><span data-stu-id="8543b-124">**GetType**</span></span>](id3dxfilesavedata--gettype.md)                   | <span data-ttu-id="8543b-125">Recupera a ID do modelo deste nó de dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="8543b-125">Retrieves the template ID of this file data node.</span></span><br/>                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="8543b-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="8543b-126">Remarks</span></span>

<span data-ttu-id="8543b-127">O GUID da interface ID3DXFileSaveObject é ID3DXFileSaveObject IID \_ .</span><span class="sxs-lookup"><span data-stu-id="8543b-127">The GUID for the ID3DXFileSaveObject interface is IID\_ID3DXFileSaveObject.</span></span>

<span data-ttu-id="8543b-128">O tipo LPD3DXFileSaveData é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="8543b-128">The LPD3DXFileSaveData type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
```



## <a name="requirements"></a><span data-ttu-id="8543b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8543b-129">Requirements</span></span>



| <span data-ttu-id="8543b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="8543b-130">Requirement</span></span> | <span data-ttu-id="8543b-131">Valor</span><span class="sxs-lookup"><span data-stu-id="8543b-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8543b-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8543b-132">Header</span></span><br/>  | <dl> <span data-ttu-id="8543b-133"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="8543b-133"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="8543b-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8543b-134">Library</span></span><br/> | <dl> <span data-ttu-id="8543b-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8543b-135"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8543b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="8543b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8543b-137">Interfaces de arquivo D3DX X</span><span class="sxs-lookup"><span data-stu-id="8543b-137">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
