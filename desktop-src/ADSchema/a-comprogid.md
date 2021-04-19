---
title: COM-ProgID atributo
description: Esse atributo armazena a lista de IDs de programa de objeto COM que são implementadas neste pacote de aplicativo.
ms.assetid: 9d2945e4-f236-48f6-bed3-145d445ff653
ms.tgt_platform: multiple
keywords:
- Esquema de COM-ProgID do atributo AD
- Esquema de AD do atributo corprogid
topic_type:
- apiref
api_name:
- COM-ProgID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 686976732bedf2c4ba486186634720568d3b6c3c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "105749119"
---
# <a name="com-progid-attribute"></a><span data-ttu-id="e95d3-105">COM-ProgID atributo</span><span class="sxs-lookup"><span data-stu-id="e95d3-105">COM-ProgID attribute</span></span>

<span data-ttu-id="e95d3-106">Esse atributo armazena a lista de IDs de programa de objeto COM que são implementadas neste pacote de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e95d3-106">This attribute stores the list of COM object program IDs that are implemented in this application package.</span></span>



| <span data-ttu-id="e95d3-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="e95d3-107">Entry</span></span> | <span data-ttu-id="e95d3-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e95d3-108">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e95d3-109">CN</span><span class="sxs-lookup"><span data-stu-id="e95d3-109">CN</span></span>                | <span data-ttu-id="e95d3-110">COM-ProgID</span><span class="sxs-lookup"><span data-stu-id="e95d3-110">COM-ProgID</span></span>                                                                       |
| <span data-ttu-id="e95d3-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="e95d3-111">Ldap-Display-Name</span></span> | <span data-ttu-id="e95d3-112">corprogid</span><span class="sxs-lookup"><span data-stu-id="e95d3-112">cOMProgID</span></span>                                                                        |
| <span data-ttu-id="e95d3-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="e95d3-113">Size</span></span>              | \-                                                                               |
| <span data-ttu-id="e95d3-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="e95d3-114">Update Privilege</span></span>  | <span data-ttu-id="e95d3-115">Qualquer pessoa pode atualizar esse objeto com base na segurança do objeto que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="e95d3-115">Anyone may update this object based on the security of the object being created.</span></span> |
| <span data-ttu-id="e95d3-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="e95d3-116">Update Frequency</span></span>  | \-                                                                               |
| <span data-ttu-id="e95d3-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="e95d3-117">Attribute-Id</span></span>      | <span data-ttu-id="e95d3-118">1.2.840.113556.1.4.21</span><span class="sxs-lookup"><span data-stu-id="e95d3-118">1.2.840.113556.1.4.21</span></span>                                                            |
| <span data-ttu-id="e95d3-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="e95d3-119">System-Id-Guid</span></span>    | <span data-ttu-id="e95d3-120">bf96793d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="e95d3-120">bf96793d-0de6-11d0-a285-00aa003049e2</span></span>                                             |
| <span data-ttu-id="e95d3-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="e95d3-121">Syntax</span></span>            | [<span data-ttu-id="e95d3-122">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="e95d3-122">**String(Unicode)**</span></span>](s-string-unicode.md)                                      |



## <a name="implementations"></a><span data-ttu-id="e95d3-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="e95d3-123">Implementations</span></span>

-   [<span data-ttu-id="e95d3-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="e95d3-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="e95d3-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="e95d3-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="e95d3-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="e95d3-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="e95d3-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="e95d3-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="e95d3-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="e95d3-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="e95d3-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="e95d3-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="e95d3-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e95d3-130">Windows 2000 Server</span></span>



| <span data-ttu-id="e95d3-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="e95d3-131">Entry</span></span> | <span data-ttu-id="e95d3-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e95d3-132">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e95d3-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="e95d3-133">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="e95d3-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e95d3-134">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="e95d3-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="e95d3-135">System-Only</span></span>            | <span data-ttu-id="e95d3-136">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-136">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e95d3-137">Is-Single-Valued</span></span>       | <span data-ttu-id="e95d3-138">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-138">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="e95d3-139">Is Indexed</span></span>             | <span data-ttu-id="e95d3-140">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-140">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e95d3-141">In Global Catalog</span></span>      | <span data-ttu-id="e95d3-142">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-142">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e95d3-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="e95d3-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e95d3-144">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="e95d3-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e95d3-145">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="e95d3-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e95d3-146">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="e95d3-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e95d3-147">Search-Flags</span></span>           | <span data-ttu-id="e95d3-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e95d3-148">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="e95d3-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e95d3-149">System-Flags</span></span>           | <span data-ttu-id="e95d3-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e95d3-150">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="e95d3-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e95d3-151">Classes used in</span></span>        | [<span data-ttu-id="e95d3-152">**Registro de classe**</span><span class="sxs-lookup"><span data-stu-id="e95d3-152">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="e95d3-153">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="e95d3-153">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="e95d3-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e95d3-154">Windows Server 2003</span></span>



| <span data-ttu-id="e95d3-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="e95d3-155">Entry</span></span> | <span data-ttu-id="e95d3-156">Valor</span><span class="sxs-lookup"><span data-stu-id="e95d3-156">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e95d3-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="e95d3-157">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="e95d3-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e95d3-158">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="e95d3-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="e95d3-159">System-Only</span></span>            | <span data-ttu-id="e95d3-160">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-160">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e95d3-161">Is-Single-Valued</span></span>       | <span data-ttu-id="e95d3-162">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-162">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="e95d3-163">Is Indexed</span></span>             | <span data-ttu-id="e95d3-164">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-164">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e95d3-165">In Global Catalog</span></span>      | <span data-ttu-id="e95d3-166">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-166">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e95d3-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="e95d3-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e95d3-168">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="e95d3-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e95d3-169">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="e95d3-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e95d3-170">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="e95d3-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e95d3-171">Search-Flags</span></span>           | <span data-ttu-id="e95d3-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e95d3-172">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="e95d3-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e95d3-173">System-Flags</span></span>           | <span data-ttu-id="e95d3-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e95d3-174">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="e95d3-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e95d3-175">Classes used in</span></span>        | [<span data-ttu-id="e95d3-176">**Registro de classe**</span><span class="sxs-lookup"><span data-stu-id="e95d3-176">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="e95d3-177">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="e95d3-177">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="e95d3-178">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="e95d3-178">Windows Server 2003 R2</span></span>



| <span data-ttu-id="e95d3-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="e95d3-179">Entry</span></span> | <span data-ttu-id="e95d3-180">Valor</span><span class="sxs-lookup"><span data-stu-id="e95d3-180">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e95d3-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="e95d3-181">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="e95d3-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e95d3-182">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="e95d3-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="e95d3-183">System-Only</span></span>            | <span data-ttu-id="e95d3-184">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-184">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e95d3-185">Is-Single-Valued</span></span>       | <span data-ttu-id="e95d3-186">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-186">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="e95d3-187">Is Indexed</span></span>             | <span data-ttu-id="e95d3-188">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-188">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e95d3-189">In Global Catalog</span></span>      | <span data-ttu-id="e95d3-190">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-190">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e95d3-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="e95d3-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e95d3-192">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="e95d3-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e95d3-193">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="e95d3-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e95d3-194">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="e95d3-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e95d3-195">Search-Flags</span></span>           | <span data-ttu-id="e95d3-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e95d3-196">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="e95d3-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e95d3-197">System-Flags</span></span>           | <span data-ttu-id="e95d3-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e95d3-198">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="e95d3-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e95d3-199">Classes used in</span></span>        | [<span data-ttu-id="e95d3-200">**Registro de classe**</span><span class="sxs-lookup"><span data-stu-id="e95d3-200">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="e95d3-201">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="e95d3-201">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="e95d3-202">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e95d3-202">Windows Server 2008</span></span>



| <span data-ttu-id="e95d3-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="e95d3-203">Entry</span></span> | <span data-ttu-id="e95d3-204">Valor</span><span class="sxs-lookup"><span data-stu-id="e95d3-204">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e95d3-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="e95d3-205">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="e95d3-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e95d3-206">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="e95d3-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="e95d3-207">System-Only</span></span>            | <span data-ttu-id="e95d3-208">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-208">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e95d3-209">Is-Single-Valued</span></span>       | <span data-ttu-id="e95d3-210">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-210">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="e95d3-211">Is Indexed</span></span>             | <span data-ttu-id="e95d3-212">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-212">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e95d3-213">In Global Catalog</span></span>      | <span data-ttu-id="e95d3-214">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-214">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e95d3-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="e95d3-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e95d3-216">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="e95d3-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e95d3-217">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="e95d3-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e95d3-218">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="e95d3-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e95d3-219">Search-Flags</span></span>           | <span data-ttu-id="e95d3-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e95d3-220">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="e95d3-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e95d3-221">System-Flags</span></span>           | <span data-ttu-id="e95d3-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e95d3-222">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="e95d3-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e95d3-223">Classes used in</span></span>        | [<span data-ttu-id="e95d3-224">**Registro de classe**</span><span class="sxs-lookup"><span data-stu-id="e95d3-224">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="e95d3-225">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="e95d3-225">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="e95d3-226">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e95d3-226">Windows Server 2008 R2</span></span>



| <span data-ttu-id="e95d3-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="e95d3-227">Entry</span></span> | <span data-ttu-id="e95d3-228">Valor</span><span class="sxs-lookup"><span data-stu-id="e95d3-228">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e95d3-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="e95d3-229">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="e95d3-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e95d3-230">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="e95d3-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="e95d3-231">System-Only</span></span>            | <span data-ttu-id="e95d3-232">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-232">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e95d3-233">Is-Single-Valued</span></span>       | <span data-ttu-id="e95d3-234">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-234">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="e95d3-235">Is Indexed</span></span>             | <span data-ttu-id="e95d3-236">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-236">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e95d3-237">In Global Catalog</span></span>      | <span data-ttu-id="e95d3-238">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-238">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e95d3-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="e95d3-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e95d3-240">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="e95d3-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e95d3-241">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="e95d3-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e95d3-242">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="e95d3-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e95d3-243">Search-Flags</span></span>           | <span data-ttu-id="e95d3-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e95d3-244">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="e95d3-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e95d3-245">System-Flags</span></span>           | <span data-ttu-id="e95d3-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e95d3-246">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="e95d3-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e95d3-247">Classes used in</span></span>        | [<span data-ttu-id="e95d3-248">**Registro de classe**</span><span class="sxs-lookup"><span data-stu-id="e95d3-248">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="e95d3-249">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="e95d3-249">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="e95d3-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e95d3-250">Windows Server 2012</span></span>



| <span data-ttu-id="e95d3-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="e95d3-251">Entry</span></span> | <span data-ttu-id="e95d3-252">Valor</span><span class="sxs-lookup"><span data-stu-id="e95d3-252">Value</span></span> |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e95d3-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="e95d3-253">Link-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="e95d3-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="e95d3-254">MAPI-Id</span></span>                | \-                                                                                                                            |
| <span data-ttu-id="e95d3-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="e95d3-255">System-Only</span></span>            | <span data-ttu-id="e95d3-256">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-256">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="e95d3-257">Is-Single-Valued</span></span>       | <span data-ttu-id="e95d3-258">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-258">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="e95d3-259">Is Indexed</span></span>             | <span data-ttu-id="e95d3-260">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-260">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="e95d3-261">In Global Catalog</span></span>      | <span data-ttu-id="e95d3-262">Falso</span><span class="sxs-lookup"><span data-stu-id="e95d3-262">False</span></span>                                                                                                                         |
| <span data-ttu-id="e95d3-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="e95d3-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="e95d3-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="e95d3-264">O:BAG:BAD:S:</span></span>                                                                                                                  |
| <span data-ttu-id="e95d3-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="e95d3-265">Range-Lower</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="e95d3-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="e95d3-266">Range-Upper</span></span>            | \-                                                                                                                            |
| <span data-ttu-id="e95d3-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="e95d3-267">Search-Flags</span></span>           | <span data-ttu-id="e95d3-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="e95d3-268">0x00000000</span></span>                                                                                                                    |
| <span data-ttu-id="e95d3-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="e95d3-269">System-Flags</span></span>           | <span data-ttu-id="e95d3-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e95d3-270">0x00000010</span></span>                                                                                                                    |
| <span data-ttu-id="e95d3-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="e95d3-271">Classes used in</span></span>        | [<span data-ttu-id="e95d3-272">**Registro de classe**</span><span class="sxs-lookup"><span data-stu-id="e95d3-272">**Class-Registration**</span></span>](c-classregistration.md)<br/> [<span data-ttu-id="e95d3-273">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="e95d3-273">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





