---
description: Os valores de HRESULT a seguir são os mais comuns. Mais valores estão contidos no arquivo de cabeçalho Winerror. h.
ms.assetid: ce52efc3-92c7-40e4-ac49-0c54049e169f
title: Valores de HRESULT comuns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a64d042d9531d026cda548b2a699ed60c0bebd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827762"
---
# <a name="common-hresult-values"></a><span data-ttu-id="85037-104">Valores de HRESULT comuns</span><span class="sxs-lookup"><span data-stu-id="85037-104">Common HRESULT Values</span></span>

<span data-ttu-id="85037-105">Os valores de HRESULT a seguir são os mais comuns.</span><span class="sxs-lookup"><span data-stu-id="85037-105">The following HRESULT values are the most common.</span></span> <span data-ttu-id="85037-106">Mais valores estão contidos no arquivo de cabeçalho Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="85037-106">More values are contained in the header file Winerror.h.</span></span>

<span data-ttu-id="85037-107">Aqui estão os valores listados em ordem alfabética por nome.</span><span class="sxs-lookup"><span data-stu-id="85037-107">Here are the values listed alphabetically by name.</span></span>



| <span data-ttu-id="85037-108">Nome</span><span class="sxs-lookup"><span data-stu-id="85037-108">Name</span></span>            | <span data-ttu-id="85037-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="85037-109">Description</span></span>                         | <span data-ttu-id="85037-110">Valor</span><span class="sxs-lookup"><span data-stu-id="85037-110">Value</span></span>      |
|-----------------|-------------------------------------|------------|
| <span data-ttu-id="85037-111">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="85037-111">S\_OK</span></span>           | <span data-ttu-id="85037-112">Operação concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="85037-112">Operation successful</span></span>                | <span data-ttu-id="85037-113">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85037-113">0x00000000</span></span> |
| <span data-ttu-id="85037-114">E \_ anular</span><span class="sxs-lookup"><span data-stu-id="85037-114">E\_ABORT</span></span>        | <span data-ttu-id="85037-115">Operação anulada</span><span class="sxs-lookup"><span data-stu-id="85037-115">Operation aborted</span></span>                   | <span data-ttu-id="85037-116">0x80004004</span><span class="sxs-lookup"><span data-stu-id="85037-116">0x80004004</span></span> |
| <span data-ttu-id="85037-117">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="85037-117">E\_ACCESSDENIED</span></span> | <span data-ttu-id="85037-118">Erro geral de acesso negado</span><span class="sxs-lookup"><span data-stu-id="85037-118">General access denied error</span></span>         | <span data-ttu-id="85037-119">0x80070005</span><span class="sxs-lookup"><span data-stu-id="85037-119">0x80070005</span></span> |
| <span data-ttu-id="85037-120">E \_ falha</span><span class="sxs-lookup"><span data-stu-id="85037-120">E\_FAIL</span></span>         | <span data-ttu-id="85037-121">Falha não especificada</span><span class="sxs-lookup"><span data-stu-id="85037-121">Unspecified failure</span></span>                 | <span data-ttu-id="85037-122">0x80004005</span><span class="sxs-lookup"><span data-stu-id="85037-122">0x80004005</span></span> |
| <span data-ttu-id="85037-123">\_identificador E</span><span class="sxs-lookup"><span data-stu-id="85037-123">E\_HANDLE</span></span>       | <span data-ttu-id="85037-124">Identificador inválido</span><span class="sxs-lookup"><span data-stu-id="85037-124">Handle that is not valid</span></span>            | <span data-ttu-id="85037-125">0x80070006</span><span class="sxs-lookup"><span data-stu-id="85037-125">0x80070006</span></span> |
| <span data-ttu-id="85037-126">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="85037-126">E\_INVALIDARG</span></span>   | <span data-ttu-id="85037-127">Um ou mais argumentos não são válidos</span><span class="sxs-lookup"><span data-stu-id="85037-127">One or more arguments are not valid</span></span> | <span data-ttu-id="85037-128">0x80070057</span><span class="sxs-lookup"><span data-stu-id="85037-128">0x80070057</span></span> |
| <span data-ttu-id="85037-129">E \_ NOinterface</span><span class="sxs-lookup"><span data-stu-id="85037-129">E\_NOINTERFACE</span></span>  | <span data-ttu-id="85037-130">Nenhuma interface desse tipo é suportada</span><span class="sxs-lookup"><span data-stu-id="85037-130">No such interface supported</span></span>         | <span data-ttu-id="85037-131">0x80004002</span><span class="sxs-lookup"><span data-stu-id="85037-131">0x80004002</span></span> |
| <span data-ttu-id="85037-132">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="85037-132">E\_NOTIMPL</span></span>      | <span data-ttu-id="85037-133">Não implementado</span><span class="sxs-lookup"><span data-stu-id="85037-133">Not implemented</span></span>                     | <span data-ttu-id="85037-134">0x80004001</span><span class="sxs-lookup"><span data-stu-id="85037-134">0x80004001</span></span> |
| <span data-ttu-id="85037-135">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="85037-135">E\_OUTOFMEMORY</span></span>  | <span data-ttu-id="85037-136">Falha ao alocar a memória necessária</span><span class="sxs-lookup"><span data-stu-id="85037-136">Failed to allocate necessary memory</span></span> | <span data-ttu-id="85037-137">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="85037-137">0x8007000E</span></span> |
| <span data-ttu-id="85037-138">\_ponteiro E</span><span class="sxs-lookup"><span data-stu-id="85037-138">E\_POINTER</span></span>      | <span data-ttu-id="85037-139">Ponteiro inválido</span><span class="sxs-lookup"><span data-stu-id="85037-139">Pointer that is not valid</span></span>           | <span data-ttu-id="85037-140">0x80004003</span><span class="sxs-lookup"><span data-stu-id="85037-140">0x80004003</span></span> |
| <span data-ttu-id="85037-141">E \_ inesperado</span><span class="sxs-lookup"><span data-stu-id="85037-141">E\_UNEXPECTED</span></span>   | <span data-ttu-id="85037-142">Falha inesperada</span><span class="sxs-lookup"><span data-stu-id="85037-142">Unexpected failure</span></span>                  | <span data-ttu-id="85037-143">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="85037-143">0x8000FFFF</span></span> |



 

<span data-ttu-id="85037-144">Aqui estão os valores listados em ordem numérica por valor.</span><span class="sxs-lookup"><span data-stu-id="85037-144">Here are the values listed in numeric order by value.</span></span>



| <span data-ttu-id="85037-145">Valor</span><span class="sxs-lookup"><span data-stu-id="85037-145">Value</span></span>      | <span data-ttu-id="85037-146">Nome</span><span class="sxs-lookup"><span data-stu-id="85037-146">Name</span></span>            | <span data-ttu-id="85037-147">Descrição</span><span class="sxs-lookup"><span data-stu-id="85037-147">Description</span></span>                         |
|------------|-----------------|-------------------------------------|
| <span data-ttu-id="85037-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="85037-148">0x00000000</span></span> | <span data-ttu-id="85037-149">S \_ OK</span><span class="sxs-lookup"><span data-stu-id="85037-149">S\_OK</span></span>           | <span data-ttu-id="85037-150">Operação concluída com êxito</span><span class="sxs-lookup"><span data-stu-id="85037-150">Operation successful</span></span>                |
| <span data-ttu-id="85037-151">0x80004001</span><span class="sxs-lookup"><span data-stu-id="85037-151">0x80004001</span></span> | <span data-ttu-id="85037-152">E \_ NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="85037-152">E\_NOTIMPL</span></span>      | <span data-ttu-id="85037-153">Não implementado</span><span class="sxs-lookup"><span data-stu-id="85037-153">Not implemented</span></span>                     |
| <span data-ttu-id="85037-154">0x80004002</span><span class="sxs-lookup"><span data-stu-id="85037-154">0x80004002</span></span> | <span data-ttu-id="85037-155">E \_ NOinterface</span><span class="sxs-lookup"><span data-stu-id="85037-155">E\_NOINTERFACE</span></span>  | <span data-ttu-id="85037-156">Nenhuma interface desse tipo é suportada</span><span class="sxs-lookup"><span data-stu-id="85037-156">No such interface supported</span></span>         |
| <span data-ttu-id="85037-157">0x80004003</span><span class="sxs-lookup"><span data-stu-id="85037-157">0x80004003</span></span> | <span data-ttu-id="85037-158">\_ponteiro E</span><span class="sxs-lookup"><span data-stu-id="85037-158">E\_POINTER</span></span>      | <span data-ttu-id="85037-159">Ponteiro inválido</span><span class="sxs-lookup"><span data-stu-id="85037-159">Pointer that is not valid</span></span>           |
| <span data-ttu-id="85037-160">0x80004004</span><span class="sxs-lookup"><span data-stu-id="85037-160">0x80004004</span></span> | <span data-ttu-id="85037-161">E \_ anular</span><span class="sxs-lookup"><span data-stu-id="85037-161">E\_ABORT</span></span>        | <span data-ttu-id="85037-162">Operação anulada</span><span class="sxs-lookup"><span data-stu-id="85037-162">Operation aborted</span></span>                   |
| <span data-ttu-id="85037-163">0x80004005</span><span class="sxs-lookup"><span data-stu-id="85037-163">0x80004005</span></span> | <span data-ttu-id="85037-164">E \_ falha</span><span class="sxs-lookup"><span data-stu-id="85037-164">E\_FAIL</span></span>         | <span data-ttu-id="85037-165">Falha não especificada</span><span class="sxs-lookup"><span data-stu-id="85037-165">Unspecified failure</span></span>                 |
| <span data-ttu-id="85037-166">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="85037-166">0x8000FFFF</span></span> | <span data-ttu-id="85037-167">E \_ inesperado</span><span class="sxs-lookup"><span data-stu-id="85037-167">E\_UNEXPECTED</span></span>   | <span data-ttu-id="85037-168">Falha inesperada</span><span class="sxs-lookup"><span data-stu-id="85037-168">Unexpected failure</span></span>                  |
| <span data-ttu-id="85037-169">0x80070005</span><span class="sxs-lookup"><span data-stu-id="85037-169">0x80070005</span></span> | <span data-ttu-id="85037-170">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="85037-170">E\_ACCESSDENIED</span></span> | <span data-ttu-id="85037-171">Erro geral de acesso negado</span><span class="sxs-lookup"><span data-stu-id="85037-171">General access denied error</span></span>         |
| <span data-ttu-id="85037-172">0x80070006</span><span class="sxs-lookup"><span data-stu-id="85037-172">0x80070006</span></span> | <span data-ttu-id="85037-173">\_identificador E</span><span class="sxs-lookup"><span data-stu-id="85037-173">E\_HANDLE</span></span>       | <span data-ttu-id="85037-174">Identificador inválido</span><span class="sxs-lookup"><span data-stu-id="85037-174">Handle that is not valid</span></span>            |
| <span data-ttu-id="85037-175">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="85037-175">0x8007000E</span></span> | <span data-ttu-id="85037-176">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="85037-176">E\_OUTOFMEMORY</span></span>  | <span data-ttu-id="85037-177">Falha ao alocar a memória necessária</span><span class="sxs-lookup"><span data-stu-id="85037-177">Failed to allocate necessary memory</span></span> |
| <span data-ttu-id="85037-178">0x80070057</span><span class="sxs-lookup"><span data-stu-id="85037-178">0x80070057</span></span> | <span data-ttu-id="85037-179">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="85037-179">E\_INVALIDARG</span></span>   | <span data-ttu-id="85037-180">Um ou mais argumentos não são válidos</span><span class="sxs-lookup"><span data-stu-id="85037-180">One or more arguments are not valid</span></span> |



 

 

 



