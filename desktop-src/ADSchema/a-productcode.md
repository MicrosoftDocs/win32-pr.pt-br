---
title: Product-Code atributo
description: Esse atributo contém um identificador exclusivo para um aplicativo para uma versão específica do produto, representado como um GUID de cadeia de caracteres, por exemplo, \ 0034; 12345678-1234-1234-1234-123456789012 \ 0034;.
ms.assetid: 1fb50a4c-1a6a-4231-a6b2-92f6bc4a1ead
ms.tgt_platform: multiple
keywords:
- Esquema de Product-Code do atributo AD
- Esquema de AD do atributo productCode
topic_type:
- apiref
api_name:
- Product-Code
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51dc874552fc819de4f9c58b23809b9f5662ee6e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919301"
---
# <a name="product-code-attribute"></a><span data-ttu-id="04d26-105">Product-Code atributo</span><span class="sxs-lookup"><span data-stu-id="04d26-105">Product-Code attribute</span></span>

<span data-ttu-id="04d26-106">Esse atributo contém um identificador exclusivo para um aplicativo para uma versão específica do produto, representado como um GUID de cadeia de caracteres, por exemplo " {12345678-1234-1234-1234-123456789012} ".</span><span class="sxs-lookup"><span data-stu-id="04d26-106">This attribute contains a unique identifier for an application for a particular product release, represented as a string GUID, for example "{12345678-1234-1234-1234-123456789012}".</span></span> <span data-ttu-id="04d26-107">As letras usadas neste GUID devem estar em letras maiúsculas.</span><span class="sxs-lookup"><span data-stu-id="04d26-107">Letters used in this GUID must be uppercase.</span></span> <span data-ttu-id="04d26-108">Essa ID deve variar para diferentes versões e idiomas.</span><span class="sxs-lookup"><span data-stu-id="04d26-108">This ID must vary for different versions and languages.</span></span>



| <span data-ttu-id="04d26-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="04d26-109">Entry</span></span> | <span data-ttu-id="04d26-110">Valor</span><span class="sxs-lookup"><span data-stu-id="04d26-110">Value</span></span> |
|-------------------|-------------------------------------------------------|
| <span data-ttu-id="04d26-111">CN</span><span class="sxs-lookup"><span data-stu-id="04d26-111">CN</span></span>                | <span data-ttu-id="04d26-112">Product-Code</span><span class="sxs-lookup"><span data-stu-id="04d26-112">Product-Code</span></span>                                          |
| <span data-ttu-id="04d26-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="04d26-113">Ldap-Display-Name</span></span> | <span data-ttu-id="04d26-114">productCode</span><span class="sxs-lookup"><span data-stu-id="04d26-114">productCode</span></span>                                           |
| <span data-ttu-id="04d26-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="04d26-115">Size</span></span>              | \-                                                    |
| <span data-ttu-id="04d26-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="04d26-116">Update Privilege</span></span>  | \-                                                    |
| <span data-ttu-id="04d26-117">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="04d26-117">Update Frequency</span></span>  | \-                                                    |
| <span data-ttu-id="04d26-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="04d26-118">Attribute-Id</span></span>      | <span data-ttu-id="04d26-119">1.2.840.113556.1.4.818</span><span class="sxs-lookup"><span data-stu-id="04d26-119">1.2.840.113556.1.4.818</span></span>                                |
| <span data-ttu-id="04d26-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="04d26-120">System-Id-Guid</span></span>    | <span data-ttu-id="04d26-121">d9e18317-8939-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="04d26-121">d9e18317-8939-11d1-aebc-0000f80367c1</span></span>                  |
| <span data-ttu-id="04d26-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="04d26-122">Syntax</span></span>            | [<span data-ttu-id="04d26-123">**Objeto (link de réplica)**</span><span class="sxs-lookup"><span data-stu-id="04d26-123">**Object(Replica-Link)**</span></span>](s-object-replica-link.md) |



## <a name="implementations"></a><span data-ttu-id="04d26-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="04d26-124">Implementations</span></span>

-   [<span data-ttu-id="04d26-125">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="04d26-125">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="04d26-126">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="04d26-126">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="04d26-127">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="04d26-127">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="04d26-128">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="04d26-128">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="04d26-129">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="04d26-129">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="04d26-130">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="04d26-130">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="04d26-131">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="04d26-131">Windows 2000 Server</span></span>



| <span data-ttu-id="04d26-132">Entrada</span><span class="sxs-lookup"><span data-stu-id="04d26-132">Entry</span></span> | <span data-ttu-id="04d26-133">Valor</span><span class="sxs-lookup"><span data-stu-id="04d26-133">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="04d26-134">ID do link</span><span class="sxs-lookup"><span data-stu-id="04d26-134">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="04d26-135">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04d26-135">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="04d26-136">System-Only</span><span class="sxs-lookup"><span data-stu-id="04d26-136">System-Only</span></span>            | <span data-ttu-id="04d26-137">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-137">False</span></span>                                                            |
| <span data-ttu-id="04d26-138">É de valor único</span><span class="sxs-lookup"><span data-stu-id="04d26-138">Is-Single-Valued</span></span>       | <span data-ttu-id="04d26-139">True</span><span class="sxs-lookup"><span data-stu-id="04d26-139">True</span></span>                                                             |
| <span data-ttu-id="04d26-140">É indexado</span><span class="sxs-lookup"><span data-stu-id="04d26-140">Is Indexed</span></span>             | <span data-ttu-id="04d26-141">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-141">False</span></span>                                                            |
| <span data-ttu-id="04d26-142">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="04d26-142">In Global Catalog</span></span>      | <span data-ttu-id="04d26-143">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-143">False</span></span>                                                            |
| <span data-ttu-id="04d26-144">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04d26-144">NT-Security-Descriptor</span></span> | <span data-ttu-id="04d26-145">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="04d26-145">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="04d26-146">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04d26-146">Range-Lower</span></span>            | <span data-ttu-id="04d26-147">0</span><span class="sxs-lookup"><span data-stu-id="04d26-147">0</span></span>                                                                |
| <span data-ttu-id="04d26-148">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04d26-148">Range-Upper</span></span>            | <span data-ttu-id="04d26-149">16</span><span class="sxs-lookup"><span data-stu-id="04d26-149">16</span></span>                                                               |
| <span data-ttu-id="04d26-150">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04d26-150">Search-Flags</span></span>           | <span data-ttu-id="04d26-151">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04d26-151">0x00000000</span></span>                                                       |
| <span data-ttu-id="04d26-152">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04d26-152">System-Flags</span></span>           | <span data-ttu-id="04d26-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04d26-153">0x00000010</span></span>                                                       |
| <span data-ttu-id="04d26-154">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="04d26-154">Classes used in</span></span>        | [<span data-ttu-id="04d26-155">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="04d26-155">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="04d26-156">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="04d26-156">Windows Server 2003</span></span>



| <span data-ttu-id="04d26-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="04d26-157">Entry</span></span> | <span data-ttu-id="04d26-158">Valor</span><span class="sxs-lookup"><span data-stu-id="04d26-158">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="04d26-159">ID do link</span><span class="sxs-lookup"><span data-stu-id="04d26-159">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="04d26-160">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04d26-160">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="04d26-161">System-Only</span><span class="sxs-lookup"><span data-stu-id="04d26-161">System-Only</span></span>            | <span data-ttu-id="04d26-162">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-162">False</span></span>                                                            |
| <span data-ttu-id="04d26-163">É de valor único</span><span class="sxs-lookup"><span data-stu-id="04d26-163">Is-Single-Valued</span></span>       | <span data-ttu-id="04d26-164">True</span><span class="sxs-lookup"><span data-stu-id="04d26-164">True</span></span>                                                             |
| <span data-ttu-id="04d26-165">É indexado</span><span class="sxs-lookup"><span data-stu-id="04d26-165">Is Indexed</span></span>             | <span data-ttu-id="04d26-166">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-166">False</span></span>                                                            |
| <span data-ttu-id="04d26-167">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="04d26-167">In Global Catalog</span></span>      | <span data-ttu-id="04d26-168">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-168">False</span></span>                                                            |
| <span data-ttu-id="04d26-169">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04d26-169">NT-Security-Descriptor</span></span> | <span data-ttu-id="04d26-170">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="04d26-170">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="04d26-171">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04d26-171">Range-Lower</span></span>            | <span data-ttu-id="04d26-172">0</span><span class="sxs-lookup"><span data-stu-id="04d26-172">0</span></span>                                                                |
| <span data-ttu-id="04d26-173">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04d26-173">Range-Upper</span></span>            | <span data-ttu-id="04d26-174">16</span><span class="sxs-lookup"><span data-stu-id="04d26-174">16</span></span>                                                               |
| <span data-ttu-id="04d26-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04d26-175">Search-Flags</span></span>           | <span data-ttu-id="04d26-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04d26-176">0x00000000</span></span>                                                       |
| <span data-ttu-id="04d26-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04d26-177">System-Flags</span></span>           | <span data-ttu-id="04d26-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04d26-178">0x00000010</span></span>                                                       |
| <span data-ttu-id="04d26-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="04d26-179">Classes used in</span></span>        | [<span data-ttu-id="04d26-180">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="04d26-180">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="04d26-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="04d26-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="04d26-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="04d26-182">Entry</span></span> | <span data-ttu-id="04d26-183">Valor</span><span class="sxs-lookup"><span data-stu-id="04d26-183">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="04d26-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="04d26-184">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="04d26-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04d26-185">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="04d26-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="04d26-186">System-Only</span></span>            | <span data-ttu-id="04d26-187">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-187">False</span></span>                                                            |
| <span data-ttu-id="04d26-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="04d26-188">Is-Single-Valued</span></span>       | <span data-ttu-id="04d26-189">True</span><span class="sxs-lookup"><span data-stu-id="04d26-189">True</span></span>                                                             |
| <span data-ttu-id="04d26-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="04d26-190">Is Indexed</span></span>             | <span data-ttu-id="04d26-191">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-191">False</span></span>                                                            |
| <span data-ttu-id="04d26-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="04d26-192">In Global Catalog</span></span>      | <span data-ttu-id="04d26-193">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-193">False</span></span>                                                            |
| <span data-ttu-id="04d26-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04d26-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="04d26-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="04d26-195">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="04d26-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04d26-196">Range-Lower</span></span>            | <span data-ttu-id="04d26-197">0</span><span class="sxs-lookup"><span data-stu-id="04d26-197">0</span></span>                                                                |
| <span data-ttu-id="04d26-198">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04d26-198">Range-Upper</span></span>            | <span data-ttu-id="04d26-199">16</span><span class="sxs-lookup"><span data-stu-id="04d26-199">16</span></span>                                                               |
| <span data-ttu-id="04d26-200">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04d26-200">Search-Flags</span></span>           | <span data-ttu-id="04d26-201">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04d26-201">0x00000000</span></span>                                                       |
| <span data-ttu-id="04d26-202">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04d26-202">System-Flags</span></span>           | <span data-ttu-id="04d26-203">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04d26-203">0x00000010</span></span>                                                       |
| <span data-ttu-id="04d26-204">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="04d26-204">Classes used in</span></span>        | [<span data-ttu-id="04d26-205">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="04d26-205">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="04d26-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="04d26-206">Windows Server 2008</span></span>



| <span data-ttu-id="04d26-207">Entrada</span><span class="sxs-lookup"><span data-stu-id="04d26-207">Entry</span></span> | <span data-ttu-id="04d26-208">Valor</span><span class="sxs-lookup"><span data-stu-id="04d26-208">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="04d26-209">ID do link</span><span class="sxs-lookup"><span data-stu-id="04d26-209">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="04d26-210">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04d26-210">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="04d26-211">System-Only</span><span class="sxs-lookup"><span data-stu-id="04d26-211">System-Only</span></span>            | <span data-ttu-id="04d26-212">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-212">False</span></span>                                                            |
| <span data-ttu-id="04d26-213">É de valor único</span><span class="sxs-lookup"><span data-stu-id="04d26-213">Is-Single-Valued</span></span>       | <span data-ttu-id="04d26-214">True</span><span class="sxs-lookup"><span data-stu-id="04d26-214">True</span></span>                                                             |
| <span data-ttu-id="04d26-215">É indexado</span><span class="sxs-lookup"><span data-stu-id="04d26-215">Is Indexed</span></span>             | <span data-ttu-id="04d26-216">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-216">False</span></span>                                                            |
| <span data-ttu-id="04d26-217">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="04d26-217">In Global Catalog</span></span>      | <span data-ttu-id="04d26-218">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-218">False</span></span>                                                            |
| <span data-ttu-id="04d26-219">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04d26-219">NT-Security-Descriptor</span></span> | <span data-ttu-id="04d26-220">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="04d26-220">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="04d26-221">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04d26-221">Range-Lower</span></span>            | <span data-ttu-id="04d26-222">0</span><span class="sxs-lookup"><span data-stu-id="04d26-222">0</span></span>                                                                |
| <span data-ttu-id="04d26-223">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04d26-223">Range-Upper</span></span>            | <span data-ttu-id="04d26-224">16</span><span class="sxs-lookup"><span data-stu-id="04d26-224">16</span></span>                                                               |
| <span data-ttu-id="04d26-225">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04d26-225">Search-Flags</span></span>           | <span data-ttu-id="04d26-226">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04d26-226">0x00000000</span></span>                                                       |
| <span data-ttu-id="04d26-227">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04d26-227">System-Flags</span></span>           | <span data-ttu-id="04d26-228">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04d26-228">0x00000010</span></span>                                                       |
| <span data-ttu-id="04d26-229">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="04d26-229">Classes used in</span></span>        | [<span data-ttu-id="04d26-230">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="04d26-230">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="04d26-231">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04d26-231">Windows Server 2008 R2</span></span>



| <span data-ttu-id="04d26-232">Entrada</span><span class="sxs-lookup"><span data-stu-id="04d26-232">Entry</span></span> | <span data-ttu-id="04d26-233">Valor</span><span class="sxs-lookup"><span data-stu-id="04d26-233">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="04d26-234">ID do link</span><span class="sxs-lookup"><span data-stu-id="04d26-234">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="04d26-235">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04d26-235">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="04d26-236">System-Only</span><span class="sxs-lookup"><span data-stu-id="04d26-236">System-Only</span></span>            | <span data-ttu-id="04d26-237">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-237">False</span></span>                                                            |
| <span data-ttu-id="04d26-238">É de valor único</span><span class="sxs-lookup"><span data-stu-id="04d26-238">Is-Single-Valued</span></span>       | <span data-ttu-id="04d26-239">True</span><span class="sxs-lookup"><span data-stu-id="04d26-239">True</span></span>                                                             |
| <span data-ttu-id="04d26-240">É indexado</span><span class="sxs-lookup"><span data-stu-id="04d26-240">Is Indexed</span></span>             | <span data-ttu-id="04d26-241">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-241">False</span></span>                                                            |
| <span data-ttu-id="04d26-242">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="04d26-242">In Global Catalog</span></span>      | <span data-ttu-id="04d26-243">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-243">False</span></span>                                                            |
| <span data-ttu-id="04d26-244">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04d26-244">NT-Security-Descriptor</span></span> | <span data-ttu-id="04d26-245">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="04d26-245">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="04d26-246">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04d26-246">Range-Lower</span></span>            | <span data-ttu-id="04d26-247">0</span><span class="sxs-lookup"><span data-stu-id="04d26-247">0</span></span>                                                                |
| <span data-ttu-id="04d26-248">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04d26-248">Range-Upper</span></span>            | <span data-ttu-id="04d26-249">16</span><span class="sxs-lookup"><span data-stu-id="04d26-249">16</span></span>                                                               |
| <span data-ttu-id="04d26-250">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04d26-250">Search-Flags</span></span>           | <span data-ttu-id="04d26-251">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04d26-251">0x00000000</span></span>                                                       |
| <span data-ttu-id="04d26-252">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04d26-252">System-Flags</span></span>           | <span data-ttu-id="04d26-253">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04d26-253">0x00000010</span></span>                                                       |
| <span data-ttu-id="04d26-254">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="04d26-254">Classes used in</span></span>        | [<span data-ttu-id="04d26-255">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="04d26-255">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="04d26-256">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04d26-256">Windows Server 2012</span></span>



| <span data-ttu-id="04d26-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="04d26-257">Entry</span></span> | <span data-ttu-id="04d26-258">Valor</span><span class="sxs-lookup"><span data-stu-id="04d26-258">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="04d26-259">ID do link</span><span class="sxs-lookup"><span data-stu-id="04d26-259">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="04d26-260">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="04d26-260">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="04d26-261">System-Only</span><span class="sxs-lookup"><span data-stu-id="04d26-261">System-Only</span></span>            | <span data-ttu-id="04d26-262">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-262">False</span></span>                                                            |
| <span data-ttu-id="04d26-263">É de valor único</span><span class="sxs-lookup"><span data-stu-id="04d26-263">Is-Single-Valued</span></span>       | <span data-ttu-id="04d26-264">True</span><span class="sxs-lookup"><span data-stu-id="04d26-264">True</span></span>                                                             |
| <span data-ttu-id="04d26-265">É indexado</span><span class="sxs-lookup"><span data-stu-id="04d26-265">Is Indexed</span></span>             | <span data-ttu-id="04d26-266">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-266">False</span></span>                                                            |
| <span data-ttu-id="04d26-267">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="04d26-267">In Global Catalog</span></span>      | <span data-ttu-id="04d26-268">Falso</span><span class="sxs-lookup"><span data-stu-id="04d26-268">False</span></span>                                                            |
| <span data-ttu-id="04d26-269">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="04d26-269">NT-Security-Descriptor</span></span> | <span data-ttu-id="04d26-270">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="04d26-270">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="04d26-271">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="04d26-271">Range-Lower</span></span>            | <span data-ttu-id="04d26-272">0</span><span class="sxs-lookup"><span data-stu-id="04d26-272">0</span></span>                                                                |
| <span data-ttu-id="04d26-273">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="04d26-273">Range-Upper</span></span>            | <span data-ttu-id="04d26-274">16</span><span class="sxs-lookup"><span data-stu-id="04d26-274">16</span></span>                                                               |
| <span data-ttu-id="04d26-275">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="04d26-275">Search-Flags</span></span>           | <span data-ttu-id="04d26-276">0x00000000</span><span class="sxs-lookup"><span data-stu-id="04d26-276">0x00000000</span></span>                                                       |
| <span data-ttu-id="04d26-277">System-Flags</span><span class="sxs-lookup"><span data-stu-id="04d26-277">System-Flags</span></span>           | <span data-ttu-id="04d26-278">0x00000010</span><span class="sxs-lookup"><span data-stu-id="04d26-278">0x00000010</span></span>                                                       |
| <span data-ttu-id="04d26-279">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="04d26-279">Classes used in</span></span>        | [<span data-ttu-id="04d26-280">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="04d26-280">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





