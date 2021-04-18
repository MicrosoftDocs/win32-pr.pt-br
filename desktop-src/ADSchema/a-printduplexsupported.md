---
title: Print-duplex-atributo com suporte
description: Indica o tipo de suporte duplex que uma impressora tem.
ms.assetid: c7d3e3f1-d6a1-41b7-a54d-c932a00b2a68
ms.tgt_platform: multiple
keywords:
- Print-duplex-atributo de AD de atributos com suporte
- Esquema de AD do atributo printDuplexSupported
topic_type:
- apiref
api_name:
- Print-Duplex-Supported
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7027b5af8d2c2bc8ece810a00c17060608b7824c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105750359"
---
# <a name="print-duplex-supported-attribute"></a><span data-ttu-id="a1e7d-105">Print-duplex-atributo com suporte</span><span class="sxs-lookup"><span data-stu-id="a1e7d-105">Print-Duplex-Supported attribute</span></span>

<span data-ttu-id="a1e7d-106">Indica o tipo de suporte duplex que uma impressora tem.</span><span class="sxs-lookup"><span data-stu-id="a1e7d-106">Indicates the type of duplex support a printer has.</span></span>



| <span data-ttu-id="a1e7d-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1e7d-107">Entry</span></span> | <span data-ttu-id="a1e7d-108">Valor</span><span class="sxs-lookup"><span data-stu-id="a1e7d-108">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="a1e7d-109">CN</span><span class="sxs-lookup"><span data-stu-id="a1e7d-109">CN</span></span>                | <span data-ttu-id="a1e7d-110">Impressão-duplex-com suporte</span><span class="sxs-lookup"><span data-stu-id="a1e7d-110">Print-Duplex-Supported</span></span>                                |
| <span data-ttu-id="a1e7d-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="a1e7d-111">Ldap-Display-Name</span></span> | <span data-ttu-id="a1e7d-112">printDuplexSupported</span><span class="sxs-lookup"><span data-stu-id="a1e7d-112">printDuplexSupported</span></span>                                  |
| <span data-ttu-id="a1e7d-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a1e7d-113">Size</span></span>              | <span data-ttu-id="a1e7d-114">4 bytes.</span><span class="sxs-lookup"><span data-stu-id="a1e7d-114">4 bytes.</span></span> <span data-ttu-id="a1e7d-115">Duplex com suporte = 2.</span><span class="sxs-lookup"><span data-stu-id="a1e7d-115">Duplex supported = 2.</span></span> <span data-ttu-id="a1e7d-116">Simplex somente = 1 ou 0.</span><span class="sxs-lookup"><span data-stu-id="a1e7d-116">Simplex only = 1 or 0.</span></span> |
| <span data-ttu-id="a1e7d-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="a1e7d-117">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="a1e7d-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="a1e7d-118">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="a1e7d-119">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="a1e7d-119">Attribute-Id</span></span>      | <span data-ttu-id="a1e7d-120">1.2.840.113556.1.4.1311</span><span class="sxs-lookup"><span data-stu-id="a1e7d-120">1.2.840.113556.1.4.1311</span></span>                               |
| <span data-ttu-id="a1e7d-121">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="a1e7d-121">System-Id-Guid</span></span>    | <span data-ttu-id="a1e7d-122">281416cc-1968-11d0-a28f-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="a1e7d-122">281416cc-1968-11d0-a28f-00aa003049e2</span></span>                  |
| <span data-ttu-id="a1e7d-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1e7d-123">Syntax</span></span>            | [<span data-ttu-id="a1e7d-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a1e7d-124">**Boolean**</span></span>](s-boolean.md)                          |



## <a name="implementations"></a><span data-ttu-id="a1e7d-125">Implementações</span><span class="sxs-lookup"><span data-stu-id="a1e7d-125">Implementations</span></span>

-   [<span data-ttu-id="a1e7d-126">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="a1e7d-126">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="a1e7d-127">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="a1e7d-127">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="a1e7d-128">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="a1e7d-128">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="a1e7d-129">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="a1e7d-129">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="a1e7d-130">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="a1e7d-130">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="a1e7d-131">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="a1e7d-131">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="a1e7d-132">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a1e7d-132">Windows 2000 Server</span></span>



| <span data-ttu-id="a1e7d-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1e7d-133">Entry</span></span> | <span data-ttu-id="a1e7d-134">Valor</span><span class="sxs-lookup"><span data-stu-id="a1e7d-134">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="a1e7d-135">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1e7d-135">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="a1e7d-136">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1e7d-136">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="a1e7d-137">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1e7d-137">System-Only</span></span>            | <span data-ttu-id="a1e7d-138">Falso</span><span class="sxs-lookup"><span data-stu-id="a1e7d-138">False</span></span>                                          |
| <span data-ttu-id="a1e7d-139">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1e7d-139">Is-Single-Valued</span></span>       | <span data-ttu-id="a1e7d-140">True</span><span class="sxs-lookup"><span data-stu-id="a1e7d-140">True</span></span>                                           |
| <span data-ttu-id="a1e7d-141">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1e7d-141">Is Indexed</span></span>             | <span data-ttu-id="a1e7d-142">Falso</span><span class="sxs-lookup"><span data-stu-id="a1e7d-142">False</span></span>                                          |
| <span data-ttu-id="a1e7d-143">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1e7d-143">In Global Catalog</span></span>      | <span data-ttu-id="a1e7d-144">True</span><span class="sxs-lookup"><span data-stu-id="a1e7d-144">True</span></span>                                           |
| <span data-ttu-id="a1e7d-145">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1e7d-145">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1e7d-146">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1e7d-146">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="a1e7d-147">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1e7d-147">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="a1e7d-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1e7d-148">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="a1e7d-149">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e7d-149">Search-Flags</span></span>           | <span data-ttu-id="a1e7d-150">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1e7d-150">0x00000000</span></span>                                     |
| <span data-ttu-id="a1e7d-151">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e7d-151">System-Flags</span></span>           | <span data-ttu-id="a1e7d-152">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1e7d-152">0x00000010</span></span>                                     |
| <span data-ttu-id="a1e7d-153">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1e7d-153">Classes used in</span></span>        | [<span data-ttu-id="a1e7d-154">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="a1e7d-154">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="a1e7d-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a1e7d-155">Windows Server 2003</span></span>



| <span data-ttu-id="a1e7d-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1e7d-156">Entry</span></span> | <span data-ttu-id="a1e7d-157">Valor</span><span class="sxs-lookup"><span data-stu-id="a1e7d-157">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="a1e7d-158">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1e7d-158">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="a1e7d-159">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1e7d-159">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="a1e7d-160">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1e7d-160">System-Only</span></span>            | <span data-ttu-id="a1e7d-161">Falso</span><span class="sxs-lookup"><span data-stu-id="a1e7d-161">False</span></span>                                          |
| <span data-ttu-id="a1e7d-162">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1e7d-162">Is-Single-Valued</span></span>       | <span data-ttu-id="a1e7d-163">True</span><span class="sxs-lookup"><span data-stu-id="a1e7d-163">True</span></span>                                           |
| <span data-ttu-id="a1e7d-164">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1e7d-164">Is Indexed</span></span>             | <span data-ttu-id="a1e7d-165">Falso</span><span class="sxs-lookup"><span data-stu-id="a1e7d-165">False</span></span>                                          |
| <span data-ttu-id="a1e7d-166">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1e7d-166">In Global Catalog</span></span>      | <span data-ttu-id="a1e7d-167">True</span><span class="sxs-lookup"><span data-stu-id="a1e7d-167">True</span></span>                                           |
| <span data-ttu-id="a1e7d-168">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1e7d-168">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1e7d-169">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1e7d-169">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="a1e7d-170">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1e7d-170">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="a1e7d-171">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1e7d-171">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="a1e7d-172">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e7d-172">Search-Flags</span></span>           | <span data-ttu-id="a1e7d-173">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1e7d-173">0x00000000</span></span>                                     |
| <span data-ttu-id="a1e7d-174">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e7d-174">System-Flags</span></span>           | <span data-ttu-id="a1e7d-175">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1e7d-175">0x00000010</span></span>                                     |
| <span data-ttu-id="a1e7d-176">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1e7d-176">Classes used in</span></span>        | [<span data-ttu-id="a1e7d-177">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="a1e7d-177">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="a1e7d-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="a1e7d-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="a1e7d-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1e7d-179">Entry</span></span> | <span data-ttu-id="a1e7d-180">Valor</span><span class="sxs-lookup"><span data-stu-id="a1e7d-180">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="a1e7d-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1e7d-181">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="a1e7d-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1e7d-182">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="a1e7d-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1e7d-183">System-Only</span></span>            | <span data-ttu-id="a1e7d-184">Falso</span><span class="sxs-lookup"><span data-stu-id="a1e7d-184">False</span></span>                                          |
| <span data-ttu-id="a1e7d-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1e7d-185">Is-Single-Valued</span></span>       | <span data-ttu-id="a1e7d-186">True</span><span class="sxs-lookup"><span data-stu-id="a1e7d-186">True</span></span>                                           |
| <span data-ttu-id="a1e7d-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1e7d-187">Is Indexed</span></span>             | <span data-ttu-id="a1e7d-188">Falso</span><span class="sxs-lookup"><span data-stu-id="a1e7d-188">False</span></span>                                          |
| <span data-ttu-id="a1e7d-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1e7d-189">In Global Catalog</span></span>      | <span data-ttu-id="a1e7d-190">True</span><span class="sxs-lookup"><span data-stu-id="a1e7d-190">True</span></span>                                           |
| <span data-ttu-id="a1e7d-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1e7d-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1e7d-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1e7d-192">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="a1e7d-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1e7d-193">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="a1e7d-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1e7d-194">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="a1e7d-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e7d-195">Search-Flags</span></span>           | <span data-ttu-id="a1e7d-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1e7d-196">0x00000000</span></span>                                     |
| <span data-ttu-id="a1e7d-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e7d-197">System-Flags</span></span>           | <span data-ttu-id="a1e7d-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1e7d-198">0x00000010</span></span>                                     |
| <span data-ttu-id="a1e7d-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1e7d-199">Classes used in</span></span>        | [<span data-ttu-id="a1e7d-200">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="a1e7d-200">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="a1e7d-201">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1e7d-201">Windows Server 2008</span></span>



| <span data-ttu-id="a1e7d-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1e7d-202">Entry</span></span> | <span data-ttu-id="a1e7d-203">Valor</span><span class="sxs-lookup"><span data-stu-id="a1e7d-203">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="a1e7d-204">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1e7d-204">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="a1e7d-205">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1e7d-205">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="a1e7d-206">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1e7d-206">System-Only</span></span>            | <span data-ttu-id="a1e7d-207">Falso</span><span class="sxs-lookup"><span data-stu-id="a1e7d-207">False</span></span>                                          |
| <span data-ttu-id="a1e7d-208">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1e7d-208">Is-Single-Valued</span></span>       | <span data-ttu-id="a1e7d-209">True</span><span class="sxs-lookup"><span data-stu-id="a1e7d-209">True</span></span>                                           |
| <span data-ttu-id="a1e7d-210">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1e7d-210">Is Indexed</span></span>             | <span data-ttu-id="a1e7d-211">Falso</span><span class="sxs-lookup"><span data-stu-id="a1e7d-211">False</span></span>                                          |
| <span data-ttu-id="a1e7d-212">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1e7d-212">In Global Catalog</span></span>      | <span data-ttu-id="a1e7d-213">True</span><span class="sxs-lookup"><span data-stu-id="a1e7d-213">True</span></span>                                           |
| <span data-ttu-id="a1e7d-214">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1e7d-214">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1e7d-215">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1e7d-215">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="a1e7d-216">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1e7d-216">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="a1e7d-217">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1e7d-217">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="a1e7d-218">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e7d-218">Search-Flags</span></span>           | <span data-ttu-id="a1e7d-219">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1e7d-219">0x00000000</span></span>                                     |
| <span data-ttu-id="a1e7d-220">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e7d-220">System-Flags</span></span>           | <span data-ttu-id="a1e7d-221">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1e7d-221">0x00000010</span></span>                                     |
| <span data-ttu-id="a1e7d-222">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1e7d-222">Classes used in</span></span>        | [<span data-ttu-id="a1e7d-223">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="a1e7d-223">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="a1e7d-224">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a1e7d-224">Windows Server 2008 R2</span></span>



| <span data-ttu-id="a1e7d-225">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1e7d-225">Entry</span></span> | <span data-ttu-id="a1e7d-226">Valor</span><span class="sxs-lookup"><span data-stu-id="a1e7d-226">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="a1e7d-227">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1e7d-227">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="a1e7d-228">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1e7d-228">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="a1e7d-229">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1e7d-229">System-Only</span></span>            | <span data-ttu-id="a1e7d-230">Falso</span><span class="sxs-lookup"><span data-stu-id="a1e7d-230">False</span></span>                                          |
| <span data-ttu-id="a1e7d-231">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1e7d-231">Is-Single-Valued</span></span>       | <span data-ttu-id="a1e7d-232">True</span><span class="sxs-lookup"><span data-stu-id="a1e7d-232">True</span></span>                                           |
| <span data-ttu-id="a1e7d-233">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1e7d-233">Is Indexed</span></span>             | <span data-ttu-id="a1e7d-234">Falso</span><span class="sxs-lookup"><span data-stu-id="a1e7d-234">False</span></span>                                          |
| <span data-ttu-id="a1e7d-235">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1e7d-235">In Global Catalog</span></span>      | <span data-ttu-id="a1e7d-236">True</span><span class="sxs-lookup"><span data-stu-id="a1e7d-236">True</span></span>                                           |
| <span data-ttu-id="a1e7d-237">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1e7d-237">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1e7d-238">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1e7d-238">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="a1e7d-239">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1e7d-239">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="a1e7d-240">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1e7d-240">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="a1e7d-241">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e7d-241">Search-Flags</span></span>           | <span data-ttu-id="a1e7d-242">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1e7d-242">0x00000000</span></span>                                     |
| <span data-ttu-id="a1e7d-243">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e7d-243">System-Flags</span></span>           | <span data-ttu-id="a1e7d-244">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1e7d-244">0x00000010</span></span>                                     |
| <span data-ttu-id="a1e7d-245">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1e7d-245">Classes used in</span></span>        | [<span data-ttu-id="a1e7d-246">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="a1e7d-246">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="a1e7d-247">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a1e7d-247">Windows Server 2012</span></span>



| <span data-ttu-id="a1e7d-248">Entrada</span><span class="sxs-lookup"><span data-stu-id="a1e7d-248">Entry</span></span> | <span data-ttu-id="a1e7d-249">Valor</span><span class="sxs-lookup"><span data-stu-id="a1e7d-249">Value</span></span> |
|------------------------|------------------------------------------------|
| <span data-ttu-id="a1e7d-250">ID do link</span><span class="sxs-lookup"><span data-stu-id="a1e7d-250">Link-Id</span></span>                | \-                                             |
| <span data-ttu-id="a1e7d-251">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="a1e7d-251">MAPI-Id</span></span>                | \-                                             |
| <span data-ttu-id="a1e7d-252">System-Only</span><span class="sxs-lookup"><span data-stu-id="a1e7d-252">System-Only</span></span>            | <span data-ttu-id="a1e7d-253">Falso</span><span class="sxs-lookup"><span data-stu-id="a1e7d-253">False</span></span>                                          |
| <span data-ttu-id="a1e7d-254">É de valor único</span><span class="sxs-lookup"><span data-stu-id="a1e7d-254">Is-Single-Valued</span></span>       | <span data-ttu-id="a1e7d-255">True</span><span class="sxs-lookup"><span data-stu-id="a1e7d-255">True</span></span>                                           |
| <span data-ttu-id="a1e7d-256">É indexado</span><span class="sxs-lookup"><span data-stu-id="a1e7d-256">Is Indexed</span></span>             | <span data-ttu-id="a1e7d-257">Falso</span><span class="sxs-lookup"><span data-stu-id="a1e7d-257">False</span></span>                                          |
| <span data-ttu-id="a1e7d-258">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="a1e7d-258">In Global Catalog</span></span>      | <span data-ttu-id="a1e7d-259">True</span><span class="sxs-lookup"><span data-stu-id="a1e7d-259">True</span></span>                                           |
| <span data-ttu-id="a1e7d-260">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="a1e7d-260">NT-Security-Descriptor</span></span> | <span data-ttu-id="a1e7d-261">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="a1e7d-261">O:BAG:BAD:S:</span></span>                                   |
| <span data-ttu-id="a1e7d-262">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="a1e7d-262">Range-Lower</span></span>            | \-                                             |
| <span data-ttu-id="a1e7d-263">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="a1e7d-263">Range-Upper</span></span>            | \-                                             |
| <span data-ttu-id="a1e7d-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e7d-264">Search-Flags</span></span>           | <span data-ttu-id="a1e7d-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="a1e7d-265">0x00000000</span></span>                                     |
| <span data-ttu-id="a1e7d-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="a1e7d-266">System-Flags</span></span>           | <span data-ttu-id="a1e7d-267">0x00000010</span><span class="sxs-lookup"><span data-stu-id="a1e7d-267">0x00000010</span></span>                                     |
| <span data-ttu-id="a1e7d-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="a1e7d-268">Classes used in</span></span>        | [<span data-ttu-id="a1e7d-269">**Fila de impressão**</span><span class="sxs-lookup"><span data-stu-id="a1e7d-269">**Print-Queue**</span></span>](c-printqueue.md)<br/> |



 

 





