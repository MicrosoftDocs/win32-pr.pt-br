---
title: Proxy-Addresses atributo
description: Um endereço de proxy é o endereço pelo qual um objeto de destinatário do Microsoft Exchange Server é reconhecido em um sistema de email externo. Os endereços proxy são necessários para todos os objetos de destinatário, como destinatários personalizados e listas de distribuição.
ms.assetid: 7bb299d8-e67a-4062-91a3-b579fd71d5c9
ms.tgt_platform: multiple
keywords:
- Esquema de Proxy-Addresses do atributo AD
- Esquema de AD do atributo proxyAddresses
topic_type:
- apiref
api_name:
- Proxy-Addresses
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03542cef9bca48dbba1585e3837056b53673f34
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825285"
---
# <a name="proxy-addresses-attribute"></a><span data-ttu-id="79f18-106">Proxy-Addresses atributo</span><span class="sxs-lookup"><span data-stu-id="79f18-106">Proxy-Addresses attribute</span></span>

<span data-ttu-id="79f18-107">Um endereço de proxy é o endereço pelo qual um objeto de destinatário do Microsoft Exchange Server é reconhecido em um sistema de email externo.</span><span class="sxs-lookup"><span data-stu-id="79f18-107">A proxy address is the address by which a Microsoft Exchange Server recipient object is recognized in a foreign mail system.</span></span> <span data-ttu-id="79f18-108">Os endereços proxy são necessários para todos os objetos de destinatário, como destinatários personalizados e listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="79f18-108">Proxy addresses are required for all recipient objects, such as custom recipients and distribution lists.</span></span>



| <span data-ttu-id="79f18-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="79f18-109">Entry</span></span> | <span data-ttu-id="79f18-110">Valor</span><span class="sxs-lookup"><span data-stu-id="79f18-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79f18-111">CN</span><span class="sxs-lookup"><span data-stu-id="79f18-111">CN</span></span>                | <span data-ttu-id="79f18-112">Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="79f18-112">Proxy-Addresses</span></span>                                                                                      |
| <span data-ttu-id="79f18-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="79f18-113">Ldap-Display-Name</span></span> | <span data-ttu-id="79f18-114">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="79f18-114">proxyAddresses</span></span>                                                                                       |
| <span data-ttu-id="79f18-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="79f18-115">Size</span></span>              | \-                                                                                                   |
| <span data-ttu-id="79f18-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="79f18-116">Update Privilege</span></span>  | <span data-ttu-id="79f18-117">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="79f18-117">This value is set by the system.</span></span>                                                                     |
| <span data-ttu-id="79f18-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="79f18-118">Update Frequency</span></span>  | <span data-ttu-id="79f18-119">Criado por uma DLL fornecida com o objeto Address-Type Directory quando o tipo de endereço é instalado.</span><span class="sxs-lookup"><span data-stu-id="79f18-119">Created by a DLL provided with the Address-Type directory object when the address type is installed.</span></span> |
| <span data-ttu-id="79f18-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="79f18-120">Attribute-Id</span></span>      | <span data-ttu-id="79f18-121">1.2.840.113556.1.2.210</span><span class="sxs-lookup"><span data-stu-id="79f18-121">1.2.840.113556.1.2.210</span></span>                                                                               |
| <span data-ttu-id="79f18-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="79f18-122">System-Id-Guid</span></span>    | <span data-ttu-id="79f18-123">bf967a06-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="79f18-123">bf967a06-0de6-11d0-a285-00aa003049e2</span></span>                                                                 |
| <span data-ttu-id="79f18-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="79f18-124">Syntax</span></span>            | [<span data-ttu-id="79f18-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="79f18-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                                          |



## <a name="implementations"></a><span data-ttu-id="79f18-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="79f18-126">Implementations</span></span>

-   [<span data-ttu-id="79f18-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="79f18-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="79f18-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="79f18-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="79f18-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="79f18-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="79f18-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="79f18-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="79f18-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="79f18-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="79f18-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="79f18-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="79f18-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="79f18-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="79f18-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="79f18-134">Windows 2000 Server</span></span>



| <span data-ttu-id="79f18-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="79f18-135">Entry</span></span> | <span data-ttu-id="79f18-136">Valor</span><span class="sxs-lookup"><span data-stu-id="79f18-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="79f18-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="79f18-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="79f18-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79f18-138">MAPI-Id</span></span>                | <span data-ttu-id="79f18-139">0x800F</span><span class="sxs-lookup"><span data-stu-id="79f18-139">0x800F</span></span>                          |
| <span data-ttu-id="79f18-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="79f18-140">System-Only</span></span>            | <span data-ttu-id="79f18-141">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-141">False</span></span>                           |
| <span data-ttu-id="79f18-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79f18-142">Is-Single-Valued</span></span>       | <span data-ttu-id="79f18-143">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-143">False</span></span>                           |
| <span data-ttu-id="79f18-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="79f18-144">Is Indexed</span></span>             | <span data-ttu-id="79f18-145">True</span><span class="sxs-lookup"><span data-stu-id="79f18-145">True</span></span>                            |
| <span data-ttu-id="79f18-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79f18-146">In Global Catalog</span></span>      | <span data-ttu-id="79f18-147">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-147">False</span></span>                           |
| <span data-ttu-id="79f18-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79f18-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="79f18-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79f18-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="79f18-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79f18-150">Range-Lower</span></span>            | <span data-ttu-id="79f18-151">1</span><span class="sxs-lookup"><span data-stu-id="79f18-151">1</span></span>                               |
| <span data-ttu-id="79f18-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79f18-152">Range-Upper</span></span>            | <span data-ttu-id="79f18-153">1123</span><span class="sxs-lookup"><span data-stu-id="79f18-153">1123</span></span>                            |
| <span data-ttu-id="79f18-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79f18-154">Search-Flags</span></span>           | <span data-ttu-id="79f18-155">0x00000005</span><span class="sxs-lookup"><span data-stu-id="79f18-155">0x00000005</span></span>                      |
| <span data-ttu-id="79f18-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79f18-156">System-Flags</span></span>           | <span data-ttu-id="79f18-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79f18-157">0x00000010</span></span>                      |
| <span data-ttu-id="79f18-158">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79f18-158">Classes used in</span></span>        | [<span data-ttu-id="79f18-159">**Início**</span><span class="sxs-lookup"><span data-stu-id="79f18-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="79f18-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="79f18-160">Windows Server 2003</span></span>



| <span data-ttu-id="79f18-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="79f18-161">Entry</span></span> | <span data-ttu-id="79f18-162">Valor</span><span class="sxs-lookup"><span data-stu-id="79f18-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="79f18-163">ID do link</span><span class="sxs-lookup"><span data-stu-id="79f18-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="79f18-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79f18-164">MAPI-Id</span></span>                | <span data-ttu-id="79f18-165">0x800F</span><span class="sxs-lookup"><span data-stu-id="79f18-165">0x800F</span></span>                          |
| <span data-ttu-id="79f18-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="79f18-166">System-Only</span></span>            | <span data-ttu-id="79f18-167">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-167">False</span></span>                           |
| <span data-ttu-id="79f18-168">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79f18-168">Is-Single-Valued</span></span>       | <span data-ttu-id="79f18-169">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-169">False</span></span>                           |
| <span data-ttu-id="79f18-170">É indexado</span><span class="sxs-lookup"><span data-stu-id="79f18-170">Is Indexed</span></span>             | <span data-ttu-id="79f18-171">True</span><span class="sxs-lookup"><span data-stu-id="79f18-171">True</span></span>                            |
| <span data-ttu-id="79f18-172">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79f18-172">In Global Catalog</span></span>      | <span data-ttu-id="79f18-173">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-173">False</span></span>                           |
| <span data-ttu-id="79f18-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79f18-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="79f18-175">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79f18-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="79f18-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79f18-176">Range-Lower</span></span>            | <span data-ttu-id="79f18-177">1</span><span class="sxs-lookup"><span data-stu-id="79f18-177">1</span></span>                               |
| <span data-ttu-id="79f18-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79f18-178">Range-Upper</span></span>            | <span data-ttu-id="79f18-179">1123</span><span class="sxs-lookup"><span data-stu-id="79f18-179">1123</span></span>                            |
| <span data-ttu-id="79f18-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79f18-180">Search-Flags</span></span>           | <span data-ttu-id="79f18-181">0x00000005</span><span class="sxs-lookup"><span data-stu-id="79f18-181">0x00000005</span></span>                      |
| <span data-ttu-id="79f18-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79f18-182">System-Flags</span></span>           | <span data-ttu-id="79f18-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79f18-183">0x00000010</span></span>                      |
| <span data-ttu-id="79f18-184">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79f18-184">Classes used in</span></span>        | [<span data-ttu-id="79f18-185">**Início**</span><span class="sxs-lookup"><span data-stu-id="79f18-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="79f18-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="79f18-186">ADAM</span></span>



| <span data-ttu-id="79f18-187">Entrada</span><span class="sxs-lookup"><span data-stu-id="79f18-187">Entry</span></span> | <span data-ttu-id="79f18-188">Valor</span><span class="sxs-lookup"><span data-stu-id="79f18-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="79f18-189">ID do link</span><span class="sxs-lookup"><span data-stu-id="79f18-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="79f18-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79f18-190">MAPI-Id</span></span>                | <span data-ttu-id="79f18-191">0x800F</span><span class="sxs-lookup"><span data-stu-id="79f18-191">0x800F</span></span>                          |
| <span data-ttu-id="79f18-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="79f18-192">System-Only</span></span>            | <span data-ttu-id="79f18-193">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-193">False</span></span>                           |
| <span data-ttu-id="79f18-194">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79f18-194">Is-Single-Valued</span></span>       | <span data-ttu-id="79f18-195">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-195">False</span></span>                           |
| <span data-ttu-id="79f18-196">É indexado</span><span class="sxs-lookup"><span data-stu-id="79f18-196">Is Indexed</span></span>             | <span data-ttu-id="79f18-197">True</span><span class="sxs-lookup"><span data-stu-id="79f18-197">True</span></span>                            |
| <span data-ttu-id="79f18-198">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79f18-198">In Global Catalog</span></span>      | <span data-ttu-id="79f18-199">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-199">False</span></span>                           |
| <span data-ttu-id="79f18-200">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79f18-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="79f18-201">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79f18-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="79f18-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79f18-202">Range-Lower</span></span>            | <span data-ttu-id="79f18-203">1</span><span class="sxs-lookup"><span data-stu-id="79f18-203">1</span></span>                               |
| <span data-ttu-id="79f18-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79f18-204">Range-Upper</span></span>            | <span data-ttu-id="79f18-205">1123</span><span class="sxs-lookup"><span data-stu-id="79f18-205">1123</span></span>                            |
| <span data-ttu-id="79f18-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79f18-206">Search-Flags</span></span>           | <span data-ttu-id="79f18-207">0x00000005</span><span class="sxs-lookup"><span data-stu-id="79f18-207">0x00000005</span></span>                      |
| <span data-ttu-id="79f18-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79f18-208">System-Flags</span></span>           | <span data-ttu-id="79f18-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79f18-209">0x00000010</span></span>                      |
| <span data-ttu-id="79f18-210">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79f18-210">Classes used in</span></span>        | [<span data-ttu-id="79f18-211">**Início**</span><span class="sxs-lookup"><span data-stu-id="79f18-211">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="79f18-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="79f18-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="79f18-213">Entrada</span><span class="sxs-lookup"><span data-stu-id="79f18-213">Entry</span></span> | <span data-ttu-id="79f18-214">Valor</span><span class="sxs-lookup"><span data-stu-id="79f18-214">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="79f18-215">ID do link</span><span class="sxs-lookup"><span data-stu-id="79f18-215">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="79f18-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79f18-216">MAPI-Id</span></span>                | <span data-ttu-id="79f18-217">0x800F</span><span class="sxs-lookup"><span data-stu-id="79f18-217">0x800F</span></span>                          |
| <span data-ttu-id="79f18-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="79f18-218">System-Only</span></span>            | <span data-ttu-id="79f18-219">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-219">False</span></span>                           |
| <span data-ttu-id="79f18-220">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79f18-220">Is-Single-Valued</span></span>       | <span data-ttu-id="79f18-221">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-221">False</span></span>                           |
| <span data-ttu-id="79f18-222">É indexado</span><span class="sxs-lookup"><span data-stu-id="79f18-222">Is Indexed</span></span>             | <span data-ttu-id="79f18-223">True</span><span class="sxs-lookup"><span data-stu-id="79f18-223">True</span></span>                            |
| <span data-ttu-id="79f18-224">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79f18-224">In Global Catalog</span></span>      | <span data-ttu-id="79f18-225">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-225">False</span></span>                           |
| <span data-ttu-id="79f18-226">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79f18-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="79f18-227">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79f18-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="79f18-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79f18-228">Range-Lower</span></span>            | <span data-ttu-id="79f18-229">1</span><span class="sxs-lookup"><span data-stu-id="79f18-229">1</span></span>                               |
| <span data-ttu-id="79f18-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79f18-230">Range-Upper</span></span>            | <span data-ttu-id="79f18-231">1123</span><span class="sxs-lookup"><span data-stu-id="79f18-231">1123</span></span>                            |
| <span data-ttu-id="79f18-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79f18-232">Search-Flags</span></span>           | <span data-ttu-id="79f18-233">0x00000005</span><span class="sxs-lookup"><span data-stu-id="79f18-233">0x00000005</span></span>                      |
| <span data-ttu-id="79f18-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79f18-234">System-Flags</span></span>           | <span data-ttu-id="79f18-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79f18-235">0x00000010</span></span>                      |
| <span data-ttu-id="79f18-236">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79f18-236">Classes used in</span></span>        | [<span data-ttu-id="79f18-237">**Início**</span><span class="sxs-lookup"><span data-stu-id="79f18-237">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="79f18-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="79f18-238">Windows Server 2008</span></span>



| <span data-ttu-id="79f18-239">Entrada</span><span class="sxs-lookup"><span data-stu-id="79f18-239">Entry</span></span> | <span data-ttu-id="79f18-240">Valor</span><span class="sxs-lookup"><span data-stu-id="79f18-240">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="79f18-241">ID do link</span><span class="sxs-lookup"><span data-stu-id="79f18-241">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="79f18-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79f18-242">MAPI-Id</span></span>                | <span data-ttu-id="79f18-243">0x800F</span><span class="sxs-lookup"><span data-stu-id="79f18-243">0x800F</span></span>                          |
| <span data-ttu-id="79f18-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="79f18-244">System-Only</span></span>            | <span data-ttu-id="79f18-245">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-245">False</span></span>                           |
| <span data-ttu-id="79f18-246">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79f18-246">Is-Single-Valued</span></span>       | <span data-ttu-id="79f18-247">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-247">False</span></span>                           |
| <span data-ttu-id="79f18-248">É indexado</span><span class="sxs-lookup"><span data-stu-id="79f18-248">Is Indexed</span></span>             | <span data-ttu-id="79f18-249">True</span><span class="sxs-lookup"><span data-stu-id="79f18-249">True</span></span>                            |
| <span data-ttu-id="79f18-250">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79f18-250">In Global Catalog</span></span>      | <span data-ttu-id="79f18-251">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-251">False</span></span>                           |
| <span data-ttu-id="79f18-252">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79f18-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="79f18-253">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79f18-253">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="79f18-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79f18-254">Range-Lower</span></span>            | <span data-ttu-id="79f18-255">1</span><span class="sxs-lookup"><span data-stu-id="79f18-255">1</span></span>                               |
| <span data-ttu-id="79f18-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79f18-256">Range-Upper</span></span>            | <span data-ttu-id="79f18-257">1123</span><span class="sxs-lookup"><span data-stu-id="79f18-257">1123</span></span>                            |
| <span data-ttu-id="79f18-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79f18-258">Search-Flags</span></span>           | <span data-ttu-id="79f18-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="79f18-259">0x00000005</span></span>                      |
| <span data-ttu-id="79f18-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79f18-260">System-Flags</span></span>           | <span data-ttu-id="79f18-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79f18-261">0x00000010</span></span>                      |
| <span data-ttu-id="79f18-262">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79f18-262">Classes used in</span></span>        | [<span data-ttu-id="79f18-263">**Início**</span><span class="sxs-lookup"><span data-stu-id="79f18-263">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="79f18-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="79f18-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="79f18-265">Entrada</span><span class="sxs-lookup"><span data-stu-id="79f18-265">Entry</span></span> | <span data-ttu-id="79f18-266">Valor</span><span class="sxs-lookup"><span data-stu-id="79f18-266">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="79f18-267">ID do link</span><span class="sxs-lookup"><span data-stu-id="79f18-267">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="79f18-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79f18-268">MAPI-Id</span></span>                | <span data-ttu-id="79f18-269">0x800F</span><span class="sxs-lookup"><span data-stu-id="79f18-269">0x800F</span></span>                          |
| <span data-ttu-id="79f18-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="79f18-270">System-Only</span></span>            | <span data-ttu-id="79f18-271">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-271">False</span></span>                           |
| <span data-ttu-id="79f18-272">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79f18-272">Is-Single-Valued</span></span>       | <span data-ttu-id="79f18-273">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-273">False</span></span>                           |
| <span data-ttu-id="79f18-274">É indexado</span><span class="sxs-lookup"><span data-stu-id="79f18-274">Is Indexed</span></span>             | <span data-ttu-id="79f18-275">True</span><span class="sxs-lookup"><span data-stu-id="79f18-275">True</span></span>                            |
| <span data-ttu-id="79f18-276">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79f18-276">In Global Catalog</span></span>      | <span data-ttu-id="79f18-277">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-277">False</span></span>                           |
| <span data-ttu-id="79f18-278">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79f18-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="79f18-279">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79f18-279">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="79f18-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79f18-280">Range-Lower</span></span>            | <span data-ttu-id="79f18-281">1</span><span class="sxs-lookup"><span data-stu-id="79f18-281">1</span></span>                               |
| <span data-ttu-id="79f18-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79f18-282">Range-Upper</span></span>            | <span data-ttu-id="79f18-283">1123</span><span class="sxs-lookup"><span data-stu-id="79f18-283">1123</span></span>                            |
| <span data-ttu-id="79f18-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79f18-284">Search-Flags</span></span>           | <span data-ttu-id="79f18-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="79f18-285">0x00000005</span></span>                      |
| <span data-ttu-id="79f18-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79f18-286">System-Flags</span></span>           | <span data-ttu-id="79f18-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79f18-287">0x00000010</span></span>                      |
| <span data-ttu-id="79f18-288">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79f18-288">Classes used in</span></span>        | [<span data-ttu-id="79f18-289">**Início**</span><span class="sxs-lookup"><span data-stu-id="79f18-289">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="79f18-290">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="79f18-290">Windows Server 2012</span></span>



| <span data-ttu-id="79f18-291">Entrada</span><span class="sxs-lookup"><span data-stu-id="79f18-291">Entry</span></span> | <span data-ttu-id="79f18-292">Valor</span><span class="sxs-lookup"><span data-stu-id="79f18-292">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="79f18-293">ID do link</span><span class="sxs-lookup"><span data-stu-id="79f18-293">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="79f18-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="79f18-294">MAPI-Id</span></span>                | <span data-ttu-id="79f18-295">0x800F</span><span class="sxs-lookup"><span data-stu-id="79f18-295">0x800F</span></span>                          |
| <span data-ttu-id="79f18-296">System-Only</span><span class="sxs-lookup"><span data-stu-id="79f18-296">System-Only</span></span>            | <span data-ttu-id="79f18-297">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-297">False</span></span>                           |
| <span data-ttu-id="79f18-298">É de valor único</span><span class="sxs-lookup"><span data-stu-id="79f18-298">Is-Single-Valued</span></span>       | <span data-ttu-id="79f18-299">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-299">False</span></span>                           |
| <span data-ttu-id="79f18-300">É indexado</span><span class="sxs-lookup"><span data-stu-id="79f18-300">Is Indexed</span></span>             | <span data-ttu-id="79f18-301">True</span><span class="sxs-lookup"><span data-stu-id="79f18-301">True</span></span>                            |
| <span data-ttu-id="79f18-302">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="79f18-302">In Global Catalog</span></span>      | <span data-ttu-id="79f18-303">Falso</span><span class="sxs-lookup"><span data-stu-id="79f18-303">False</span></span>                           |
| <span data-ttu-id="79f18-304">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="79f18-304">NT-Security-Descriptor</span></span> | <span data-ttu-id="79f18-305">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="79f18-305">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="79f18-306">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="79f18-306">Range-Lower</span></span>            | <span data-ttu-id="79f18-307">1</span><span class="sxs-lookup"><span data-stu-id="79f18-307">1</span></span>                               |
| <span data-ttu-id="79f18-308">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="79f18-308">Range-Upper</span></span>            | <span data-ttu-id="79f18-309">1123</span><span class="sxs-lookup"><span data-stu-id="79f18-309">1123</span></span>                            |
| <span data-ttu-id="79f18-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="79f18-310">Search-Flags</span></span>           | <span data-ttu-id="79f18-311">0x00000005</span><span class="sxs-lookup"><span data-stu-id="79f18-311">0x00000005</span></span>                      |
| <span data-ttu-id="79f18-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="79f18-312">System-Flags</span></span>           | <span data-ttu-id="79f18-313">0x00000010</span><span class="sxs-lookup"><span data-stu-id="79f18-313">0x00000010</span></span>                      |
| <span data-ttu-id="79f18-314">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="79f18-314">Classes used in</span></span>        | [<span data-ttu-id="79f18-315">**Início**</span><span class="sxs-lookup"><span data-stu-id="79f18-315">**Top**</span></span>](c-top.md)<br/> |



 

 





