---
description: Esta seção contém informações de referência para as interfaces COM usadas para ler e gravar em arquivos DirectX. x. Preterido.
ms.assetid: 66e3476a-4ee8-48ac-aab8-6653793e0ef3
title: X interfaces de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6e47325a4912faeb919cb60571de3cccbbe265
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500521"
---
# <a name="x-file-interfaces"></a><span data-ttu-id="4a0b3-104">X interfaces de arquivo</span><span class="sxs-lookup"><span data-stu-id="4a0b3-104">X File Interfaces</span></span>

<span data-ttu-id="4a0b3-105">Esta seção contém informações de referência para as interfaces COM usadas para ler e gravar em arquivos DirectX. x.</span><span class="sxs-lookup"><span data-stu-id="4a0b3-105">This section contains reference information for the COM interfaces used to read to and write from DirectX .x files.</span></span> <span data-ttu-id="4a0b3-106">Preterido.</span><span class="sxs-lookup"><span data-stu-id="4a0b3-106">Deprecated.</span></span>

-   [<span data-ttu-id="4a0b3-107">**IDirectXFile**</span><span class="sxs-lookup"><span data-stu-id="4a0b3-107">**IDirectXFile**</span></span>](idirectxfile.md)
-   [<span data-ttu-id="4a0b3-108">**IDirectXFileBinary**</span><span class="sxs-lookup"><span data-stu-id="4a0b3-108">**IDirectXFileBinary**</span></span>](idirectxfilebinary.md)
-   [<span data-ttu-id="4a0b3-109">**IDirectXFileData**</span><span class="sxs-lookup"><span data-stu-id="4a0b3-109">**IDirectXFileData**</span></span>](idirectxfiledata.md)
-   [<span data-ttu-id="4a0b3-110">**IDirectXFileDataReference**</span><span class="sxs-lookup"><span data-stu-id="4a0b3-110">**IDirectXFileDataReference**</span></span>](idirectxfiledatareference.md)
-   [<span data-ttu-id="4a0b3-111">**IDirectXFileEnumObject**</span><span class="sxs-lookup"><span data-stu-id="4a0b3-111">**IDirectXFileEnumObject**</span></span>](idirectxfileenumobject.md)
-   [<span data-ttu-id="4a0b3-112">**IDirectXFileObject**</span><span class="sxs-lookup"><span data-stu-id="4a0b3-112">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
-   [<span data-ttu-id="4a0b3-113">**IDirectXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="4a0b3-113">**IDirectXFileSaveObject**</span></span>](idirectxfilesaveobject.md)

<span data-ttu-id="4a0b3-114">As tabelas a seguir ilustram a relação entre as interfaces de arquivo. x.</span><span class="sxs-lookup"><span data-stu-id="4a0b3-114">The following tables illustrate the relationship between the .x file interfaces.</span></span>



| <span data-ttu-id="4a0b3-115">Interface</span><span class="sxs-lookup"><span data-stu-id="4a0b3-115">Interface</span></span>             | <span data-ttu-id="4a0b3-116">Deriva de</span><span class="sxs-lookup"><span data-stu-id="4a0b3-116">Derives from</span></span>           | <span data-ttu-id="4a0b3-117">Deriva de</span><span class="sxs-lookup"><span data-stu-id="4a0b3-117">Derives from</span></span> |
|-----------------------|------------------------|--------------|
|                       | <span data-ttu-id="4a0b3-118">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="4a0b3-118">IDirectXFile</span></span>           | <span data-ttu-id="4a0b3-119">IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a0b3-119">IUnknown</span></span>     |
| <span data-ttu-id="4a0b3-120">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="4a0b3-120">IDirectXFileBinary</span></span>    | <span data-ttu-id="4a0b3-121">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="4a0b3-121">IDirectXFileObject</span></span>     | <span data-ttu-id="4a0b3-122">IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a0b3-122">IUnknown</span></span>     |
| <span data-ttu-id="4a0b3-123">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="4a0b3-123">IDirectXFileData</span></span>      | <span data-ttu-id="4a0b3-124">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="4a0b3-124">IDirectXFileObject</span></span>     | <span data-ttu-id="4a0b3-125">IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a0b3-125">IUnknown</span></span>     |
| <span data-ttu-id="4a0b3-126">IDirectXFileReference</span><span class="sxs-lookup"><span data-stu-id="4a0b3-126">IDirectXFileReference</span></span> | <span data-ttu-id="4a0b3-127">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="4a0b3-127">IDirectXFileObject</span></span>     | <span data-ttu-id="4a0b3-128">IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a0b3-128">IUnknown</span></span>     |
|                       | <span data-ttu-id="4a0b3-129">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="4a0b3-129">IDirectXFileSaveObject</span></span> | <span data-ttu-id="4a0b3-130">IUnknown</span><span class="sxs-lookup"><span data-stu-id="4a0b3-130">IUnknown</span></span>     |



 

## <a name="related-topics"></a><span data-ttu-id="4a0b3-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4a0b3-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a0b3-132">X referência de arquivo (herdada)</span><span class="sxs-lookup"><span data-stu-id="4a0b3-132">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



