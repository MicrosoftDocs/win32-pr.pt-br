---
description: Os aplicativos usam os métodos da interface IDirectXFileBinary para ler e recuperar informações sobre dados binários. Preterido.
ms.assetid: 43b20ab3-67b2-4717-ad90-0bf4ddb3207e
title: Interface IDirectXFileBinary (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: b6707e4e685289f16b85ab85c2cce13dcd1da962
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104172964"
---
# <a name="idirectxfilebinary-interface"></a><span data-ttu-id="04d5d-104">Interface IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="04d5d-104">IDirectXFileBinary interface</span></span>

<span data-ttu-id="04d5d-105">Os aplicativos usam os métodos da interface IDirectXFileBinary para ler e recuperar informações sobre dados binários.</span><span class="sxs-lookup"><span data-stu-id="04d5d-105">Applications use the methods of the IDirectXFileBinary interface to read and retrieve information about binary data.</span></span> <span data-ttu-id="04d5d-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="04d5d-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="04d5d-107">Membros</span><span class="sxs-lookup"><span data-stu-id="04d5d-107">Members</span></span>

<span data-ttu-id="04d5d-108">A interface **IDirectXFileBinary** herda de [**IDirectXFileObject**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="04d5d-108">The **IDirectXFileBinary** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="04d5d-109">**IDirectXFileBinary** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="04d5d-109">**IDirectXFileBinary** also has these types of members:</span></span>

-   [<span data-ttu-id="04d5d-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="04d5d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="04d5d-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="04d5d-111">Methods</span></span>

<span data-ttu-id="04d5d-112">A interface **IDirectXFileBinary** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="04d5d-112">The **IDirectXFileBinary** interface has these methods.</span></span>



| <span data-ttu-id="04d5d-113">Método</span><span class="sxs-lookup"><span data-stu-id="04d5d-113">Method</span></span>                                                 | <span data-ttu-id="04d5d-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="04d5d-114">Description</span></span>                                                                                                 |
|:-------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04d5d-115">**GetMimeType**</span><span class="sxs-lookup"><span data-stu-id="04d5d-115">**GetMimeType**</span></span>](idirectxfilebinary--getmimetype.md) | <span data-ttu-id="04d5d-116">Recupera o tipo MIME (Multipurpose Internet Mail Extensions) para os dados binários.</span><span class="sxs-lookup"><span data-stu-id="04d5d-116">Retrieves the Multipurpose Internet Mail Extensions (MIME) type for the binary data.</span></span> <span data-ttu-id="04d5d-117">Preterido.</span><span class="sxs-lookup"><span data-stu-id="04d5d-117">Deprecated.</span></span><br/> |
| [<span data-ttu-id="04d5d-118">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="04d5d-118">**GetSize**</span></span>](idirectxfilebinary--getsize.md)         | <span data-ttu-id="04d5d-119">Recupera o tamanho dos dados binários.</span><span class="sxs-lookup"><span data-stu-id="04d5d-119">Retrieves the size of the binary data.</span></span> <span data-ttu-id="04d5d-120">Preterido.</span><span class="sxs-lookup"><span data-stu-id="04d5d-120">Deprecated.</span></span><br/>                                               |
| [<span data-ttu-id="04d5d-121">**Ler**</span><span class="sxs-lookup"><span data-stu-id="04d5d-121">**Read**</span></span>](idirectxfilebinary--read.md)               | <span data-ttu-id="04d5d-122">Lê os dados binários.</span><span class="sxs-lookup"><span data-stu-id="04d5d-122">Reads the binary data.</span></span> <span data-ttu-id="04d5d-123">Preterido.</span><span class="sxs-lookup"><span data-stu-id="04d5d-123">Deprecated.</span></span><br/>                                                               |



 

## <a name="remarks"></a><span data-ttu-id="04d5d-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="04d5d-124">Remarks</span></span>

<span data-ttu-id="04d5d-125">O GUID da interface IDirectXFileBinary é IDirectXFileBinary IID \_ .</span><span class="sxs-lookup"><span data-stu-id="04d5d-125">The GUID for the IDirectXFileBinary interface is IID\_IDirectXFileBinary.</span></span>

<span data-ttu-id="04d5d-126">O tipo LPDIRECTXFileBinary é definido como um ponteiro para essa interface.</span><span class="sxs-lookup"><span data-stu-id="04d5d-126">The LPDIRECTXFileBinary type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileBinary *LPDIRECTXFILEBINARY;
```



## <a name="requirements"></a><span data-ttu-id="04d5d-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04d5d-127">Requirements</span></span>



| <span data-ttu-id="04d5d-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="04d5d-128">Requirement</span></span> | <span data-ttu-id="04d5d-129">Valor</span><span class="sxs-lookup"><span data-stu-id="04d5d-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04d5d-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04d5d-130">Header</span></span><br/>  | <dl> <span data-ttu-id="04d5d-131"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="04d5d-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="04d5d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="04d5d-132">Library</span></span><br/> | <dl> <span data-ttu-id="04d5d-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="04d5d-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04d5d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="04d5d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d5d-135">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="04d5d-135">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="04d5d-136">X interfaces de arquivo</span><span class="sxs-lookup"><span data-stu-id="04d5d-136">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




