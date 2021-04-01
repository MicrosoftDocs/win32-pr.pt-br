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
# <a name="proxy-addresses-attribute"></a><span data-ttu-id="1cf78-106">Proxy-Addresses atributo</span><span class="sxs-lookup"><span data-stu-id="1cf78-106">Proxy-Addresses attribute</span></span>

<span data-ttu-id="1cf78-107">Um endereço de proxy é o endereço pelo qual um objeto de destinatário do Microsoft Exchange Server é reconhecido em um sistema de email externo.</span><span class="sxs-lookup"><span data-stu-id="1cf78-107">A proxy address is the address by which a Microsoft Exchange Server recipient object is recognized in a foreign mail system.</span></span> <span data-ttu-id="1cf78-108">Os endereços proxy são necessários para todos os objetos de destinatário, como destinatários personalizados e listas de distribuição.</span><span class="sxs-lookup"><span data-stu-id="1cf78-108">Proxy addresses are required for all recipient objects, such as custom recipients and distribution lists.</span></span>



| <span data-ttu-id="1cf78-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cf78-109">Entry</span></span> | <span data-ttu-id="1cf78-110">Valor</span><span class="sxs-lookup"><span data-stu-id="1cf78-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf78-111">CN</span><span class="sxs-lookup"><span data-stu-id="1cf78-111">CN</span></span>                | <span data-ttu-id="1cf78-112">Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="1cf78-112">Proxy-Addresses</span></span>                                                                                      |
| <span data-ttu-id="1cf78-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1cf78-113">Ldap-Display-Name</span></span> | <span data-ttu-id="1cf78-114">proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="1cf78-114">proxyAddresses</span></span>                                                                                       |
| <span data-ttu-id="1cf78-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="1cf78-115">Size</span></span>              | \-                                                                                                   |
| <span data-ttu-id="1cf78-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="1cf78-116">Update Privilege</span></span>  | <span data-ttu-id="1cf78-117">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="1cf78-117">This value is set by the system.</span></span>                                                                     |
| <span data-ttu-id="1cf78-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="1cf78-118">Update Frequency</span></span>  | <span data-ttu-id="1cf78-119">Criado por uma DLL fornecida com o objeto Address-Type Directory quando o tipo de endereço é instalado.</span><span class="sxs-lookup"><span data-stu-id="1cf78-119">Created by a DLL provided with the Address-Type directory object when the address type is installed.</span></span> |
| <span data-ttu-id="1cf78-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1cf78-120">Attribute-Id</span></span>      | <span data-ttu-id="1cf78-121">1.2.840.113556.1.2.210</span><span class="sxs-lookup"><span data-stu-id="1cf78-121">1.2.840.113556.1.2.210</span></span>                                                                               |
| <span data-ttu-id="1cf78-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1cf78-122">System-Id-Guid</span></span>    | <span data-ttu-id="1cf78-123">bf967a06-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1cf78-123">bf967a06-0de6-11d0-a285-00aa003049e2</span></span>                                                                 |
| <span data-ttu-id="1cf78-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cf78-124">Syntax</span></span>            | [<span data-ttu-id="1cf78-125">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1cf78-125">**String(Unicode)**</span></span>](s-string-unicode.md)                                                          |



## <a name="implementations"></a><span data-ttu-id="1cf78-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="1cf78-126">Implementations</span></span>

-   [<span data-ttu-id="1cf78-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1cf78-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1cf78-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1cf78-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1cf78-129">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="1cf78-129">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="1cf78-130">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1cf78-130">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1cf78-131">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1cf78-131">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1cf78-132">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1cf78-132">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1cf78-133">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1cf78-133">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1cf78-134">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1cf78-134">Windows 2000 Server</span></span>



| <span data-ttu-id="1cf78-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cf78-135">Entry</span></span> | <span data-ttu-id="1cf78-136">Valor</span><span class="sxs-lookup"><span data-stu-id="1cf78-136">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1cf78-137">ID do link</span><span class="sxs-lookup"><span data-stu-id="1cf78-137">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1cf78-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cf78-138">MAPI-Id</span></span>                | <span data-ttu-id="1cf78-139">0x800F</span><span class="sxs-lookup"><span data-stu-id="1cf78-139">0x800F</span></span>                          |
| <span data-ttu-id="1cf78-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cf78-140">System-Only</span></span>            | <span data-ttu-id="1cf78-141">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-141">False</span></span>                           |
| <span data-ttu-id="1cf78-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1cf78-142">Is-Single-Valued</span></span>       | <span data-ttu-id="1cf78-143">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-143">False</span></span>                           |
| <span data-ttu-id="1cf78-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="1cf78-144">Is Indexed</span></span>             | <span data-ttu-id="1cf78-145">True</span><span class="sxs-lookup"><span data-stu-id="1cf78-145">True</span></span>                            |
| <span data-ttu-id="1cf78-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1cf78-146">In Global Catalog</span></span>      | <span data-ttu-id="1cf78-147">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-147">False</span></span>                           |
| <span data-ttu-id="1cf78-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1cf78-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cf78-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1cf78-149">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1cf78-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cf78-150">Range-Lower</span></span>            | <span data-ttu-id="1cf78-151">1</span><span class="sxs-lookup"><span data-stu-id="1cf78-151">1</span></span>                               |
| <span data-ttu-id="1cf78-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cf78-152">Range-Upper</span></span>            | <span data-ttu-id="1cf78-153">1123</span><span class="sxs-lookup"><span data-stu-id="1cf78-153">1123</span></span>                            |
| <span data-ttu-id="1cf78-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf78-154">Search-Flags</span></span>           | <span data-ttu-id="1cf78-155">0x00000005</span><span class="sxs-lookup"><span data-stu-id="1cf78-155">0x00000005</span></span>                      |
| <span data-ttu-id="1cf78-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf78-156">System-Flags</span></span>           | <span data-ttu-id="1cf78-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cf78-157">0x00000010</span></span>                      |
| <span data-ttu-id="1cf78-158">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1cf78-158">Classes used in</span></span>        | [<span data-ttu-id="1cf78-159">**Início**</span><span class="sxs-lookup"><span data-stu-id="1cf78-159">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1cf78-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1cf78-160">Windows Server 2003</span></span>



| <span data-ttu-id="1cf78-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cf78-161">Entry</span></span> | <span data-ttu-id="1cf78-162">Valor</span><span class="sxs-lookup"><span data-stu-id="1cf78-162">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1cf78-163">ID do link</span><span class="sxs-lookup"><span data-stu-id="1cf78-163">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1cf78-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cf78-164">MAPI-Id</span></span>                | <span data-ttu-id="1cf78-165">0x800F</span><span class="sxs-lookup"><span data-stu-id="1cf78-165">0x800F</span></span>                          |
| <span data-ttu-id="1cf78-166">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cf78-166">System-Only</span></span>            | <span data-ttu-id="1cf78-167">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-167">False</span></span>                           |
| <span data-ttu-id="1cf78-168">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1cf78-168">Is-Single-Valued</span></span>       | <span data-ttu-id="1cf78-169">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-169">False</span></span>                           |
| <span data-ttu-id="1cf78-170">É indexado</span><span class="sxs-lookup"><span data-stu-id="1cf78-170">Is Indexed</span></span>             | <span data-ttu-id="1cf78-171">True</span><span class="sxs-lookup"><span data-stu-id="1cf78-171">True</span></span>                            |
| <span data-ttu-id="1cf78-172">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1cf78-172">In Global Catalog</span></span>      | <span data-ttu-id="1cf78-173">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-173">False</span></span>                           |
| <span data-ttu-id="1cf78-174">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1cf78-174">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cf78-175">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1cf78-175">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1cf78-176">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cf78-176">Range-Lower</span></span>            | <span data-ttu-id="1cf78-177">1</span><span class="sxs-lookup"><span data-stu-id="1cf78-177">1</span></span>                               |
| <span data-ttu-id="1cf78-178">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cf78-178">Range-Upper</span></span>            | <span data-ttu-id="1cf78-179">1123</span><span class="sxs-lookup"><span data-stu-id="1cf78-179">1123</span></span>                            |
| <span data-ttu-id="1cf78-180">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf78-180">Search-Flags</span></span>           | <span data-ttu-id="1cf78-181">0x00000005</span><span class="sxs-lookup"><span data-stu-id="1cf78-181">0x00000005</span></span>                      |
| <span data-ttu-id="1cf78-182">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf78-182">System-Flags</span></span>           | <span data-ttu-id="1cf78-183">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cf78-183">0x00000010</span></span>                      |
| <span data-ttu-id="1cf78-184">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1cf78-184">Classes used in</span></span>        | [<span data-ttu-id="1cf78-185">**Início**</span><span class="sxs-lookup"><span data-stu-id="1cf78-185">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="1cf78-186">ADAM</span><span class="sxs-lookup"><span data-stu-id="1cf78-186">ADAM</span></span>



| <span data-ttu-id="1cf78-187">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cf78-187">Entry</span></span> | <span data-ttu-id="1cf78-188">Valor</span><span class="sxs-lookup"><span data-stu-id="1cf78-188">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1cf78-189">ID do link</span><span class="sxs-lookup"><span data-stu-id="1cf78-189">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1cf78-190">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cf78-190">MAPI-Id</span></span>                | <span data-ttu-id="1cf78-191">0x800F</span><span class="sxs-lookup"><span data-stu-id="1cf78-191">0x800F</span></span>                          |
| <span data-ttu-id="1cf78-192">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cf78-192">System-Only</span></span>            | <span data-ttu-id="1cf78-193">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-193">False</span></span>                           |
| <span data-ttu-id="1cf78-194">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1cf78-194">Is-Single-Valued</span></span>       | <span data-ttu-id="1cf78-195">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-195">False</span></span>                           |
| <span data-ttu-id="1cf78-196">É indexado</span><span class="sxs-lookup"><span data-stu-id="1cf78-196">Is Indexed</span></span>             | <span data-ttu-id="1cf78-197">True</span><span class="sxs-lookup"><span data-stu-id="1cf78-197">True</span></span>                            |
| <span data-ttu-id="1cf78-198">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1cf78-198">In Global Catalog</span></span>      | <span data-ttu-id="1cf78-199">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-199">False</span></span>                           |
| <span data-ttu-id="1cf78-200">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1cf78-200">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cf78-201">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1cf78-201">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1cf78-202">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cf78-202">Range-Lower</span></span>            | <span data-ttu-id="1cf78-203">1</span><span class="sxs-lookup"><span data-stu-id="1cf78-203">1</span></span>                               |
| <span data-ttu-id="1cf78-204">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cf78-204">Range-Upper</span></span>            | <span data-ttu-id="1cf78-205">1123</span><span class="sxs-lookup"><span data-stu-id="1cf78-205">1123</span></span>                            |
| <span data-ttu-id="1cf78-206">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf78-206">Search-Flags</span></span>           | <span data-ttu-id="1cf78-207">0x00000005</span><span class="sxs-lookup"><span data-stu-id="1cf78-207">0x00000005</span></span>                      |
| <span data-ttu-id="1cf78-208">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf78-208">System-Flags</span></span>           | <span data-ttu-id="1cf78-209">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cf78-209">0x00000010</span></span>                      |
| <span data-ttu-id="1cf78-210">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1cf78-210">Classes used in</span></span>        | [<span data-ttu-id="1cf78-211">**Início**</span><span class="sxs-lookup"><span data-stu-id="1cf78-211">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1cf78-212">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1cf78-212">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1cf78-213">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cf78-213">Entry</span></span> | <span data-ttu-id="1cf78-214">Valor</span><span class="sxs-lookup"><span data-stu-id="1cf78-214">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1cf78-215">ID do link</span><span class="sxs-lookup"><span data-stu-id="1cf78-215">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1cf78-216">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cf78-216">MAPI-Id</span></span>                | <span data-ttu-id="1cf78-217">0x800F</span><span class="sxs-lookup"><span data-stu-id="1cf78-217">0x800F</span></span>                          |
| <span data-ttu-id="1cf78-218">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cf78-218">System-Only</span></span>            | <span data-ttu-id="1cf78-219">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-219">False</span></span>                           |
| <span data-ttu-id="1cf78-220">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1cf78-220">Is-Single-Valued</span></span>       | <span data-ttu-id="1cf78-221">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-221">False</span></span>                           |
| <span data-ttu-id="1cf78-222">É indexado</span><span class="sxs-lookup"><span data-stu-id="1cf78-222">Is Indexed</span></span>             | <span data-ttu-id="1cf78-223">True</span><span class="sxs-lookup"><span data-stu-id="1cf78-223">True</span></span>                            |
| <span data-ttu-id="1cf78-224">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1cf78-224">In Global Catalog</span></span>      | <span data-ttu-id="1cf78-225">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-225">False</span></span>                           |
| <span data-ttu-id="1cf78-226">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1cf78-226">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cf78-227">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1cf78-227">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1cf78-228">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cf78-228">Range-Lower</span></span>            | <span data-ttu-id="1cf78-229">1</span><span class="sxs-lookup"><span data-stu-id="1cf78-229">1</span></span>                               |
| <span data-ttu-id="1cf78-230">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cf78-230">Range-Upper</span></span>            | <span data-ttu-id="1cf78-231">1123</span><span class="sxs-lookup"><span data-stu-id="1cf78-231">1123</span></span>                            |
| <span data-ttu-id="1cf78-232">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf78-232">Search-Flags</span></span>           | <span data-ttu-id="1cf78-233">0x00000005</span><span class="sxs-lookup"><span data-stu-id="1cf78-233">0x00000005</span></span>                      |
| <span data-ttu-id="1cf78-234">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf78-234">System-Flags</span></span>           | <span data-ttu-id="1cf78-235">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cf78-235">0x00000010</span></span>                      |
| <span data-ttu-id="1cf78-236">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1cf78-236">Classes used in</span></span>        | [<span data-ttu-id="1cf78-237">**Início**</span><span class="sxs-lookup"><span data-stu-id="1cf78-237">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1cf78-238">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1cf78-238">Windows Server 2008</span></span>



| <span data-ttu-id="1cf78-239">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cf78-239">Entry</span></span> | <span data-ttu-id="1cf78-240">Valor</span><span class="sxs-lookup"><span data-stu-id="1cf78-240">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1cf78-241">ID do link</span><span class="sxs-lookup"><span data-stu-id="1cf78-241">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1cf78-242">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cf78-242">MAPI-Id</span></span>                | <span data-ttu-id="1cf78-243">0x800F</span><span class="sxs-lookup"><span data-stu-id="1cf78-243">0x800F</span></span>                          |
| <span data-ttu-id="1cf78-244">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cf78-244">System-Only</span></span>            | <span data-ttu-id="1cf78-245">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-245">False</span></span>                           |
| <span data-ttu-id="1cf78-246">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1cf78-246">Is-Single-Valued</span></span>       | <span data-ttu-id="1cf78-247">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-247">False</span></span>                           |
| <span data-ttu-id="1cf78-248">É indexado</span><span class="sxs-lookup"><span data-stu-id="1cf78-248">Is Indexed</span></span>             | <span data-ttu-id="1cf78-249">True</span><span class="sxs-lookup"><span data-stu-id="1cf78-249">True</span></span>                            |
| <span data-ttu-id="1cf78-250">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1cf78-250">In Global Catalog</span></span>      | <span data-ttu-id="1cf78-251">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-251">False</span></span>                           |
| <span data-ttu-id="1cf78-252">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1cf78-252">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cf78-253">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1cf78-253">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1cf78-254">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cf78-254">Range-Lower</span></span>            | <span data-ttu-id="1cf78-255">1</span><span class="sxs-lookup"><span data-stu-id="1cf78-255">1</span></span>                               |
| <span data-ttu-id="1cf78-256">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cf78-256">Range-Upper</span></span>            | <span data-ttu-id="1cf78-257">1123</span><span class="sxs-lookup"><span data-stu-id="1cf78-257">1123</span></span>                            |
| <span data-ttu-id="1cf78-258">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf78-258">Search-Flags</span></span>           | <span data-ttu-id="1cf78-259">0x00000005</span><span class="sxs-lookup"><span data-stu-id="1cf78-259">0x00000005</span></span>                      |
| <span data-ttu-id="1cf78-260">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf78-260">System-Flags</span></span>           | <span data-ttu-id="1cf78-261">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cf78-261">0x00000010</span></span>                      |
| <span data-ttu-id="1cf78-262">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1cf78-262">Classes used in</span></span>        | [<span data-ttu-id="1cf78-263">**Início**</span><span class="sxs-lookup"><span data-stu-id="1cf78-263">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1cf78-264">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1cf78-264">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1cf78-265">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cf78-265">Entry</span></span> | <span data-ttu-id="1cf78-266">Valor</span><span class="sxs-lookup"><span data-stu-id="1cf78-266">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1cf78-267">ID do link</span><span class="sxs-lookup"><span data-stu-id="1cf78-267">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1cf78-268">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cf78-268">MAPI-Id</span></span>                | <span data-ttu-id="1cf78-269">0x800F</span><span class="sxs-lookup"><span data-stu-id="1cf78-269">0x800F</span></span>                          |
| <span data-ttu-id="1cf78-270">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cf78-270">System-Only</span></span>            | <span data-ttu-id="1cf78-271">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-271">False</span></span>                           |
| <span data-ttu-id="1cf78-272">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1cf78-272">Is-Single-Valued</span></span>       | <span data-ttu-id="1cf78-273">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-273">False</span></span>                           |
| <span data-ttu-id="1cf78-274">É indexado</span><span class="sxs-lookup"><span data-stu-id="1cf78-274">Is Indexed</span></span>             | <span data-ttu-id="1cf78-275">True</span><span class="sxs-lookup"><span data-stu-id="1cf78-275">True</span></span>                            |
| <span data-ttu-id="1cf78-276">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1cf78-276">In Global Catalog</span></span>      | <span data-ttu-id="1cf78-277">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-277">False</span></span>                           |
| <span data-ttu-id="1cf78-278">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1cf78-278">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cf78-279">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1cf78-279">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1cf78-280">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cf78-280">Range-Lower</span></span>            | <span data-ttu-id="1cf78-281">1</span><span class="sxs-lookup"><span data-stu-id="1cf78-281">1</span></span>                               |
| <span data-ttu-id="1cf78-282">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cf78-282">Range-Upper</span></span>            | <span data-ttu-id="1cf78-283">1123</span><span class="sxs-lookup"><span data-stu-id="1cf78-283">1123</span></span>                            |
| <span data-ttu-id="1cf78-284">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf78-284">Search-Flags</span></span>           | <span data-ttu-id="1cf78-285">0x00000005</span><span class="sxs-lookup"><span data-stu-id="1cf78-285">0x00000005</span></span>                      |
| <span data-ttu-id="1cf78-286">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf78-286">System-Flags</span></span>           | <span data-ttu-id="1cf78-287">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cf78-287">0x00000010</span></span>                      |
| <span data-ttu-id="1cf78-288">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1cf78-288">Classes used in</span></span>        | [<span data-ttu-id="1cf78-289">**Início**</span><span class="sxs-lookup"><span data-stu-id="1cf78-289">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1cf78-290">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1cf78-290">Windows Server 2012</span></span>



| <span data-ttu-id="1cf78-291">Entrada</span><span class="sxs-lookup"><span data-stu-id="1cf78-291">Entry</span></span> | <span data-ttu-id="1cf78-292">Valor</span><span class="sxs-lookup"><span data-stu-id="1cf78-292">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="1cf78-293">ID do link</span><span class="sxs-lookup"><span data-stu-id="1cf78-293">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="1cf78-294">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1cf78-294">MAPI-Id</span></span>                | <span data-ttu-id="1cf78-295">0x800F</span><span class="sxs-lookup"><span data-stu-id="1cf78-295">0x800F</span></span>                          |
| <span data-ttu-id="1cf78-296">System-Only</span><span class="sxs-lookup"><span data-stu-id="1cf78-296">System-Only</span></span>            | <span data-ttu-id="1cf78-297">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-297">False</span></span>                           |
| <span data-ttu-id="1cf78-298">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1cf78-298">Is-Single-Valued</span></span>       | <span data-ttu-id="1cf78-299">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-299">False</span></span>                           |
| <span data-ttu-id="1cf78-300">É indexado</span><span class="sxs-lookup"><span data-stu-id="1cf78-300">Is Indexed</span></span>             | <span data-ttu-id="1cf78-301">True</span><span class="sxs-lookup"><span data-stu-id="1cf78-301">True</span></span>                            |
| <span data-ttu-id="1cf78-302">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1cf78-302">In Global Catalog</span></span>      | <span data-ttu-id="1cf78-303">Falso</span><span class="sxs-lookup"><span data-stu-id="1cf78-303">False</span></span>                           |
| <span data-ttu-id="1cf78-304">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1cf78-304">NT-Security-Descriptor</span></span> | <span data-ttu-id="1cf78-305">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1cf78-305">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="1cf78-306">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1cf78-306">Range-Lower</span></span>            | <span data-ttu-id="1cf78-307">1</span><span class="sxs-lookup"><span data-stu-id="1cf78-307">1</span></span>                               |
| <span data-ttu-id="1cf78-308">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1cf78-308">Range-Upper</span></span>            | <span data-ttu-id="1cf78-309">1123</span><span class="sxs-lookup"><span data-stu-id="1cf78-309">1123</span></span>                            |
| <span data-ttu-id="1cf78-310">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf78-310">Search-Flags</span></span>           | <span data-ttu-id="1cf78-311">0x00000005</span><span class="sxs-lookup"><span data-stu-id="1cf78-311">0x00000005</span></span>                      |
| <span data-ttu-id="1cf78-312">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1cf78-312">System-Flags</span></span>           | <span data-ttu-id="1cf78-313">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1cf78-313">0x00000010</span></span>                      |
| <span data-ttu-id="1cf78-314">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1cf78-314">Classes used in</span></span>        | [<span data-ttu-id="1cf78-315">**Início**</span><span class="sxs-lookup"><span data-stu-id="1cf78-315">**Top**</span></span>](c-top.md)<br/> |



 

 





