---
title: Funções ADSI
description: Active Directory interfaces de serviço expõem as seguintes funções auxiliares para clientes que não usam automação.
ms.assetid: 4f0e90e2-afcc-4cf7-a731-9b38a83ca229
ms.tgt_platform: multiple
keywords:
- ADSI, referência, ADSI, funções
- função ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c814cf4f59a391a3242fa748856eaacb35dbcc53
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291800"
---
# <a name="adsi-functions"></a><span data-ttu-id="a1b2d-105">Funções ADSI</span><span class="sxs-lookup"><span data-stu-id="a1b2d-105">ADSI Functions</span></span>

<span data-ttu-id="a1b2d-106">Active Directory interfaces de serviço expõem as seguintes funções auxiliares para clientes que não usam automação.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-106">Active Directory Service Interfaces expose the following helper functions to clients that do not use Automation.</span></span>



| <span data-ttu-id="a1b2d-107">Função</span><span class="sxs-lookup"><span data-stu-id="a1b2d-107">Function</span></span>                                           | <span data-ttu-id="a1b2d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1b2d-108">Description</span></span>                                                                                        |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a1b2d-109">**ADsBuildEnumerator**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-109">**ADsBuildEnumerator**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator)   | <span data-ttu-id="a1b2d-110">Cria um objeto enumerador para o objeto de contêiner ADSI especificado.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-110">Creates an enumerator object for the specified ADSI container object.</span></span>                              |
| [<span data-ttu-id="a1b2d-111">**ADsBuildVarArrayInt**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-111">**ADsBuildVarArrayInt**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararrayint) | <span data-ttu-id="a1b2d-112">Cria uma matriz variante de uma matriz de **DWORD** s.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-112">Builds a variant array from an array of **DWORD** s.</span></span>                                                |
| [<span data-ttu-id="a1b2d-113">**ADsBuildVarArrayStr**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-113">**ADsBuildVarArrayStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildvararraystr) | <span data-ttu-id="a1b2d-114">Cria uma matriz variante de uma matriz de cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-114">Builds a variant array from an array of Unicode strings.</span></span>                                           |
| [<span data-ttu-id="a1b2d-115">**ADsEncodeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-115">**ADsEncodeBinaryData**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsencodebinarydata) | <span data-ttu-id="a1b2d-116">Converte um blob de dados binários para o formato adequado para um filtro de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-116">Converts a blob of binary data to the format suitable for a search filter.</span></span>                         |
| [<span data-ttu-id="a1b2d-117">**ADsEnumerateNext**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-117">**ADsEnumerateNext**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)       | <span data-ttu-id="a1b2d-118">Popula uma matriz Variant com elementos recuperados do objeto enumerador especificado.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-118">Populates a variant array with elements retrieved from the specified enumerator object.</span></span>            |
| [<span data-ttu-id="a1b2d-119">**ADsFreeEnumerator**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-119">**ADsFreeEnumerator**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator)     | <span data-ttu-id="a1b2d-120">Libera um objeto enumerador criado anteriormente pelo [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator).</span><span class="sxs-lookup"><span data-stu-id="a1b2d-120">Frees an enumerator object previously created by [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator).</span></span> |
| [<span data-ttu-id="a1b2d-121">**ADsGetLastError**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-121">**ADsGetLastError**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror)         | <span data-ttu-id="a1b2d-122">Recupera o último valor de código de erro do thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-122">Retrieves the last error code value of the calling thread.</span></span>                                         |
| [<span data-ttu-id="a1b2d-123">**ADsGetObject**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-123">**ADsGetObject**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsgetobject)               | <span data-ttu-id="a1b2d-124">Associa a um objeto ADSI usando as credenciais atuais.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-124">Binds to an ADSI object using the current credentials.</span></span>                                             |
| [<span data-ttu-id="a1b2d-125">**ADsOpenObject**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-125">**ADsOpenObject**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)             | <span data-ttu-id="a1b2d-126">Associa a um objeto ADSI usando as credenciais especificadas</span><span class="sxs-lookup"><span data-stu-id="a1b2d-126">Binds to an ADSI object using specified credentials</span></span>                                                |
| [<span data-ttu-id="a1b2d-127">**ADsSetLastError**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-127">**ADsSetLastError**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-adssetlasterror)         | <span data-ttu-id="a1b2d-128">Define o valor do código de erro do thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-128">Sets the error code value of the calling thread.</span></span>                                                   |
| [<span data-ttu-id="a1b2d-129">**AllocADsMem**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-129">**AllocADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem)                 | <span data-ttu-id="a1b2d-130">Aloca um bloco de memória.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-130">Allocates a block of memory.</span></span>                                                                       |
| [<span data-ttu-id="a1b2d-131">**AllocADsStr**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-131">**AllocADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-allocadsstr)                 | <span data-ttu-id="a1b2d-132">Aloca memória para uma determinada cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-132">Allocates memory for a given string.</span></span>                                                               |
| [<span data-ttu-id="a1b2d-133">**FreeADsMem**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-133">**FreeADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-freeadsmem)                   | <span data-ttu-id="a1b2d-134">Libera a memória alocada por [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).</span><span class="sxs-lookup"><span data-stu-id="a1b2d-134">Frees the memory allocated by [**AllocADsMem**](/windows/desktop/api/Adshlp/nf-adshlp-allocadsmem).</span></span>                                  |
| [<span data-ttu-id="a1b2d-135">**FreeADsStr**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-135">**FreeADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-freeadsstr)                   | <span data-ttu-id="a1b2d-136">Libera a memória alocada para a cadeia de caracteres fornecida.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-136">Frees the memory allocated for the given string.</span></span>                                                   |
| [<span data-ttu-id="a1b2d-137">**ReallocADsMem**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-137">**ReallocADsMem**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsmem)             | <span data-ttu-id="a1b2d-138">Atribui o conteúdo de memória existente a um local de memória criado recentemente.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-138">Assigns the existing memory content to a newly created memory location.</span></span>                            |
| [<span data-ttu-id="a1b2d-139">**ReallocADsStr**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-139">**ReallocADsStr**</span></span>](/windows/desktop/api/Adshlp/nf-adshlp-reallocadsstr)             | <span data-ttu-id="a1b2d-140">Substitui uma cadeia de caracteres existente por uma nova.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-140">Replaces an existing string with a new one.</span></span>                                                        |



 

<span data-ttu-id="a1b2d-141">As seguintes funções ADSI são obsoletas.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-141">The following ADSI functions are obsolete.</span></span>



| <span data-ttu-id="a1b2d-142">Função</span><span class="sxs-lookup"><span data-stu-id="a1b2d-142">Function</span></span>                                                  | <span data-ttu-id="a1b2d-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="a1b2d-143">Description</span></span> |
|-----------------------------------------------------------|-------------|
| [<span data-ttu-id="a1b2d-144">**AdsFreeAllErrorRecords**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-144">**AdsFreeAllErrorRecords**</span></span>](obsolete-adsi-functions.md) | <span data-ttu-id="a1b2d-145">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-145">Obsolete.</span></span>   |
| [<span data-ttu-id="a1b2d-146">**AdsDecodeBinaryData**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-146">**AdsDecodeBinaryData**</span></span>](obsolete-adsi-functions.md)    | <span data-ttu-id="a1b2d-147">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-147">Obsolete.</span></span>   |
| [<span data-ttu-id="a1b2d-148">**PropVariantToAdsType**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-148">**PropVariantToAdsType**</span></span>](obsolete-adsi-functions.md)   | <span data-ttu-id="a1b2d-149">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-149">Obsolete.</span></span>   |
| [<span data-ttu-id="a1b2d-150">**AdsTypeToPropVariant**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-150">**AdsTypeToPropVariant**</span></span>](obsolete-adsi-functions.md)   | <span data-ttu-id="a1b2d-151">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-151">Obsolete.</span></span>   |
| [<span data-ttu-id="a1b2d-152">**AdsFreeAdsValues**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-152">**AdsFreeAdsValues**</span></span>](obsolete-adsi-functions.md)       | <span data-ttu-id="a1b2d-153">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-153">Obsolete.</span></span>   |
| [<span data-ttu-id="a1b2d-154">**InitAdsMem**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-154">**InitAdsMem**</span></span>](obsolete-adsi-functions.md)             | <span data-ttu-id="a1b2d-155">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-155">Obsolete.</span></span>   |
| [<span data-ttu-id="a1b2d-156">**AssertAdsmemLeaks**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-156">**AssertAdsmemLeaks**</span></span>](obsolete-adsi-functions.md)      | <span data-ttu-id="a1b2d-157">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-157">Obsolete.</span></span>   |
| [<span data-ttu-id="a1b2d-158">**DumpMemorytracker**</span><span class="sxs-lookup"><span data-stu-id="a1b2d-158">**DumpMemorytracker**</span></span>](obsolete-adsi-functions.md)      | <span data-ttu-id="a1b2d-159">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="a1b2d-159">Obsolete.</span></span>   |



 

 

 




