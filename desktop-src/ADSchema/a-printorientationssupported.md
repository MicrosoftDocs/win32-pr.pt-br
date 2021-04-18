---
title: Orientações de impressão – atributo com suporte
description: A rotação da página para impressão em paisagem.
ms.assetid: a3e910f1-452e-4b85-8ede-50b7274475a0
ms.tgt_platform: multiple
keywords:
- Orientações de impressão – esquema de anúncio de atributo com suporte
- Esquema de AD do atributo printOrientationsSupported
topic_type:
- apiref
api_name:
- Print-Orientations-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49888caa713de7dd12616dcb9932e52b15b2a454
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105755723"
---
# <a name="print-orientations-supported-attribute"></a><span data-ttu-id="f0cad-105">Orientações de impressão – atributo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0cad-105">Print-Orientations-Supported attribute</span></span>

<span data-ttu-id="f0cad-106">A rotação da página para impressão em paisagem.</span><span class="sxs-lookup"><span data-stu-id="f0cad-106">The page rotation for landscape printing.</span></span>



| <span data-ttu-id="f0cad-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0cad-107">Entry</span></span> | <span data-ttu-id="f0cad-108">Valor</span><span class="sxs-lookup"><span data-stu-id="f0cad-108">Value</span></span> |
|-------------------|-------------------------------------------------------------|
| <span data-ttu-id="f0cad-109">CN</span><span class="sxs-lookup"><span data-stu-id="f0cad-109">CN</span></span>                | <span data-ttu-id="f0cad-110">Orientações de impressão-com suporte</span><span class="sxs-lookup"><span data-stu-id="f0cad-110">Print-Orientations-Supported</span></span>                                |
| <span data-ttu-id="f0cad-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="f0cad-111">Ldap-Display-Name</span></span> | <span data-ttu-id="f0cad-112">printOrientationsSupported</span><span class="sxs-lookup"><span data-stu-id="f0cad-112">printOrientationsSupported</span></span>                                  |
| <span data-ttu-id="f0cad-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="f0cad-113">Size</span></span>              | <span data-ttu-id="f0cad-114">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="f0cad-114">4 bytes.</span></span> <span data-ttu-id="f0cad-115">Valores possíveis: 0, 90, 270 e 0 = sem paisagem.</span><span class="sxs-lookup"><span data-stu-id="f0cad-115">Possible values: 0, 90, 270, and 0 = no landscape.</span></span> |
| <span data-ttu-id="f0cad-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="f0cad-116">Update Privilege</span></span>  | \-                                                          |
| <span data-ttu-id="f0cad-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="f0cad-117">Update Frequency</span></span>  | \-                                                          |
| <span data-ttu-id="f0cad-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="f0cad-118">Attribute-Id</span></span>      | <span data-ttu-id="f0cad-119">1.2.840.113556.1.4.240</span><span class="sxs-lookup"><span data-stu-id="f0cad-119">1.2.840.113556.1.4.240</span></span>                                      |
| <span data-ttu-id="f0cad-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="f0cad-120">System-Id-Guid</span></span>    | <span data-ttu-id="f0cad-121">281416d0-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="f0cad-121">281416d0-1968-11d0-a28f-00aa003049e2</span></span>                        |
| <span data-ttu-id="f0cad-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0cad-122">Syntax</span></span>            | [<span data-ttu-id="f0cad-123">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="f0cad-123">**String(Unicode)**</span></span>](s-string-unicode.md)                 |



## <a name="implementations"></a><span data-ttu-id="f0cad-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="f0cad-124">Implementations</span></span>

-   [<span data-ttu-id="f0cad-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="f0cad-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="f0cad-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="f0cad-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="f0cad-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="f0cad-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="f0cad-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="f0cad-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="f0cad-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="f0cad-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="f0cad-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="f0cad-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="f0cad-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f0cad-131">Windows 2000 Server</span></span>



| <span data-ttu-id="f0cad-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0cad-132">Entry</span></span> | <span data-ttu-id="f0cad-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f0cad-133">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f0cad-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0cad-134">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f0cad-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0cad-135">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f0cad-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0cad-136">System-Only</span></span>            | <span data-ttu-id="f0cad-137">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-137">False</span></span>                                          |
| <span data-ttu-id="f0cad-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0cad-138">Is-Single-Valued</span></span>       | <span data-ttu-id="f0cad-139">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-139">False</span></span>                                          |
| <span data-ttu-id="f0cad-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0cad-140">Is Indexed</span></span>             | <span data-ttu-id="f0cad-141">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-141">False</span></span>                                          |
| <span data-ttu-id="f0cad-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0cad-142">In Global Catalog</span></span>      | <span data-ttu-id="f0cad-143">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-143">False</span></span>                                          |
| <span data-ttu-id="f0cad-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0cad-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0cad-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0cad-145">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f0cad-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0cad-146">Range-Lower</span></span>            | <span data-ttu-id="f0cad-147">1</span><span class="sxs-lookup"><span data-stu-id="f0cad-147">1</span></span>                                              |
| <span data-ttu-id="f0cad-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0cad-148">Range-Upper</span></span>            | <span data-ttu-id="f0cad-149">256</span><span class="sxs-lookup"><span data-stu-id="f0cad-149">256</span></span>                                            |
| <span data-ttu-id="f0cad-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0cad-150">Search-Flags</span></span>           | <span data-ttu-id="f0cad-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0cad-151">0x00000000</span></span>                                     |
| <span data-ttu-id="f0cad-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0cad-152">System-Flags</span></span>           | <span data-ttu-id="f0cad-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0cad-153">0x00000010</span></span>                                     |
| <span data-ttu-id="f0cad-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0cad-154">Classes used in</span></span>        | [<span data-ttu-id="f0cad-155">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="f0cad-155">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="f0cad-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f0cad-156">Windows Server 2003</span></span>



| <span data-ttu-id="f0cad-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0cad-157">Entry</span></span> | <span data-ttu-id="f0cad-158">Valor</span><span class="sxs-lookup"><span data-stu-id="f0cad-158">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f0cad-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0cad-159">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f0cad-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0cad-160">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f0cad-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0cad-161">System-Only</span></span>            | <span data-ttu-id="f0cad-162">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-162">False</span></span>                                          |
| <span data-ttu-id="f0cad-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0cad-163">Is-Single-Valued</span></span>       | <span data-ttu-id="f0cad-164">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-164">False</span></span>                                          |
| <span data-ttu-id="f0cad-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0cad-165">Is Indexed</span></span>             | <span data-ttu-id="f0cad-166">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-166">False</span></span>                                          |
| <span data-ttu-id="f0cad-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0cad-167">In Global Catalog</span></span>      | <span data-ttu-id="f0cad-168">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-168">False</span></span>                                          |
| <span data-ttu-id="f0cad-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0cad-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0cad-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0cad-170">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f0cad-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0cad-171">Range-Lower</span></span>            | <span data-ttu-id="f0cad-172">1</span><span class="sxs-lookup"><span data-stu-id="f0cad-172">1</span></span>                                              |
| <span data-ttu-id="f0cad-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0cad-173">Range-Upper</span></span>            | <span data-ttu-id="f0cad-174">256</span><span class="sxs-lookup"><span data-stu-id="f0cad-174">256</span></span>                                            |
| <span data-ttu-id="f0cad-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0cad-175">Search-Flags</span></span>           | <span data-ttu-id="f0cad-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0cad-176">0x00000000</span></span>                                     |
| <span data-ttu-id="f0cad-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0cad-177">System-Flags</span></span>           | <span data-ttu-id="f0cad-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0cad-178">0x00000010</span></span>                                     |
| <span data-ttu-id="f0cad-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0cad-179">Classes used in</span></span>        | [<span data-ttu-id="f0cad-180">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="f0cad-180">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="f0cad-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="f0cad-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="f0cad-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0cad-182">Entry</span></span> | <span data-ttu-id="f0cad-183">Valor</span><span class="sxs-lookup"><span data-stu-id="f0cad-183">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f0cad-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0cad-184">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f0cad-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0cad-185">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f0cad-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0cad-186">System-Only</span></span>            | <span data-ttu-id="f0cad-187">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-187">False</span></span>                                          |
| <span data-ttu-id="f0cad-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0cad-188">Is-Single-Valued</span></span>       | <span data-ttu-id="f0cad-189">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-189">False</span></span>                                          |
| <span data-ttu-id="f0cad-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0cad-190">Is Indexed</span></span>             | <span data-ttu-id="f0cad-191">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-191">False</span></span>                                          |
| <span data-ttu-id="f0cad-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0cad-192">In Global Catalog</span></span>      | <span data-ttu-id="f0cad-193">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-193">False</span></span>                                          |
| <span data-ttu-id="f0cad-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0cad-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0cad-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0cad-195">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f0cad-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0cad-196">Range-Lower</span></span>            | <span data-ttu-id="f0cad-197">1</span><span class="sxs-lookup"><span data-stu-id="f0cad-197">1</span></span>                                              |
| <span data-ttu-id="f0cad-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0cad-198">Range-Upper</span></span>            | <span data-ttu-id="f0cad-199">256</span><span class="sxs-lookup"><span data-stu-id="f0cad-199">256</span></span>                                            |
| <span data-ttu-id="f0cad-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0cad-200">Search-Flags</span></span>           | <span data-ttu-id="f0cad-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0cad-201">0x00000000</span></span>                                     |
| <span data-ttu-id="f0cad-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0cad-202">System-Flags</span></span>           | <span data-ttu-id="f0cad-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0cad-203">0x00000010</span></span>                                     |
| <span data-ttu-id="f0cad-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0cad-204">Classes used in</span></span>        | [<span data-ttu-id="f0cad-205">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="f0cad-205">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="f0cad-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0cad-206">Windows Server 2008</span></span>



| <span data-ttu-id="f0cad-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0cad-207">Entry</span></span> | <span data-ttu-id="f0cad-208">Valor</span><span class="sxs-lookup"><span data-stu-id="f0cad-208">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f0cad-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0cad-209">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f0cad-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0cad-210">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f0cad-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0cad-211">System-Only</span></span>            | <span data-ttu-id="f0cad-212">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-212">False</span></span>                                          |
| <span data-ttu-id="f0cad-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0cad-213">Is-Single-Valued</span></span>       | <span data-ttu-id="f0cad-214">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-214">False</span></span>                                          |
| <span data-ttu-id="f0cad-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0cad-215">Is Indexed</span></span>             | <span data-ttu-id="f0cad-216">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-216">False</span></span>                                          |
| <span data-ttu-id="f0cad-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0cad-217">In Global Catalog</span></span>      | <span data-ttu-id="f0cad-218">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-218">False</span></span>                                          |
| <span data-ttu-id="f0cad-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0cad-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0cad-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0cad-220">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f0cad-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0cad-221">Range-Lower</span></span>            | <span data-ttu-id="f0cad-222">1</span><span class="sxs-lookup"><span data-stu-id="f0cad-222">1</span></span>                                              |
| <span data-ttu-id="f0cad-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0cad-223">Range-Upper</span></span>            | <span data-ttu-id="f0cad-224">256</span><span class="sxs-lookup"><span data-stu-id="f0cad-224">256</span></span>                                            |
| <span data-ttu-id="f0cad-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0cad-225">Search-Flags</span></span>           | <span data-ttu-id="f0cad-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0cad-226">0x00000000</span></span>                                     |
| <span data-ttu-id="f0cad-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0cad-227">System-Flags</span></span>           | <span data-ttu-id="f0cad-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0cad-228">0x00000010</span></span>                                     |
| <span data-ttu-id="f0cad-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0cad-229">Classes used in</span></span>        | [<span data-ttu-id="f0cad-230">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="f0cad-230">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="f0cad-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f0cad-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="f0cad-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0cad-232">Entry</span></span> | <span data-ttu-id="f0cad-233">Valor</span><span class="sxs-lookup"><span data-stu-id="f0cad-233">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f0cad-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0cad-234">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f0cad-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0cad-235">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f0cad-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0cad-236">System-Only</span></span>            | <span data-ttu-id="f0cad-237">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-237">False</span></span>                                          |
| <span data-ttu-id="f0cad-238">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0cad-238">Is-Single-Valued</span></span>       | <span data-ttu-id="f0cad-239">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-239">False</span></span>                                          |
| <span data-ttu-id="f0cad-240">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0cad-240">Is Indexed</span></span>             | <span data-ttu-id="f0cad-241">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-241">False</span></span>                                          |
| <span data-ttu-id="f0cad-242">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0cad-242">In Global Catalog</span></span>      | <span data-ttu-id="f0cad-243">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-243">False</span></span>                                          |
| <span data-ttu-id="f0cad-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0cad-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0cad-245">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0cad-245">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f0cad-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0cad-246">Range-Lower</span></span>            | <span data-ttu-id="f0cad-247">1</span><span class="sxs-lookup"><span data-stu-id="f0cad-247">1</span></span>                                              |
| <span data-ttu-id="f0cad-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0cad-248">Range-Upper</span></span>            | <span data-ttu-id="f0cad-249">256</span><span class="sxs-lookup"><span data-stu-id="f0cad-249">256</span></span>                                            |
| <span data-ttu-id="f0cad-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0cad-250">Search-Flags</span></span>           | <span data-ttu-id="f0cad-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0cad-251">0x00000000</span></span>                                     |
| <span data-ttu-id="f0cad-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0cad-252">System-Flags</span></span>           | <span data-ttu-id="f0cad-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0cad-253">0x00000010</span></span>                                     |
| <span data-ttu-id="f0cad-254">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0cad-254">Classes used in</span></span>        | [<span data-ttu-id="f0cad-255">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="f0cad-255">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="f0cad-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0cad-256">Windows Server 2012</span></span>



| <span data-ttu-id="f0cad-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="f0cad-257">Entry</span></span> | <span data-ttu-id="f0cad-258">Valor</span><span class="sxs-lookup"><span data-stu-id="f0cad-258">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="f0cad-259">ID do link</span><span class="sxs-lookup"><span data-stu-id="f0cad-259">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="f0cad-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="f0cad-260">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="f0cad-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="f0cad-261">System-Only</span></span>            | <span data-ttu-id="f0cad-262">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-262">False</span></span>                                          |
| <span data-ttu-id="f0cad-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="f0cad-263">Is-Single-Valued</span></span>       | <span data-ttu-id="f0cad-264">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-264">False</span></span>                                          |
| <span data-ttu-id="f0cad-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="f0cad-265">Is Indexed</span></span>             | <span data-ttu-id="f0cad-266">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-266">False</span></span>                                          |
| <span data-ttu-id="f0cad-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="f0cad-267">In Global Catalog</span></span>      | <span data-ttu-id="f0cad-268">Falso</span><span class="sxs-lookup"><span data-stu-id="f0cad-268">False</span></span>                                          |
| <span data-ttu-id="f0cad-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="f0cad-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="f0cad-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="f0cad-270">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="f0cad-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="f0cad-271">Range-Lower</span></span>            | <span data-ttu-id="f0cad-272">1</span><span class="sxs-lookup"><span data-stu-id="f0cad-272">1</span></span>                                              |
| <span data-ttu-id="f0cad-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="f0cad-273">Range-Upper</span></span>            | <span data-ttu-id="f0cad-274">256</span><span class="sxs-lookup"><span data-stu-id="f0cad-274">256</span></span>                                            |
| <span data-ttu-id="f0cad-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="f0cad-275">Search-Flags</span></span>           | <span data-ttu-id="f0cad-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="f0cad-276">0x00000000</span></span>                                     |
| <span data-ttu-id="f0cad-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="f0cad-277">System-Flags</span></span>           | <span data-ttu-id="f0cad-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="f0cad-278">0x00000010</span></span>                                     |
| <span data-ttu-id="f0cad-279">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="f0cad-279">Classes used in</span></span>        | [<span data-ttu-id="f0cad-280">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="f0cad-280">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





