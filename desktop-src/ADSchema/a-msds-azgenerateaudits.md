---
title: atributo ms-DS-AZ-Generate-Auditions
description: Um campo booliano que indica se as auditorias de tempo de execução precisam ser ativadas (incluir auditorias para verificações de acesso e assim por diante).
ms.assetid: 23578f6a-7e7f-4871-9503-73f2ce598173
ms.tgt_platform: multiple
keywords:
- ms-DS-AZ-Generate-auditas atributo AD Schema
- atributo msDS-AzGenerateAudits do AD Schema
topic_type:
- apiref
api_name:
- ms-DS-Az-Generate-Audits
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645bdfd2f822139072391d401ecedfedee8680b8
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825372"
---
# <a name="ms-ds-az-generate-audits-attribute"></a><span data-ttu-id="57ccf-105">atributo ms-DS-AZ-Generate-Auditions</span><span class="sxs-lookup"><span data-stu-id="57ccf-105">ms-DS-Az-Generate-Audits attribute</span></span>

<span data-ttu-id="57ccf-106">Um campo booliano que indica se as auditorias de tempo de execução precisam ser ativadas (incluir auditorias para verificações de acesso e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="57ccf-106">A Boolean field that indicates whether runtime audits need to be turned on (include audits for access checks, and so on).</span></span>



| <span data-ttu-id="57ccf-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="57ccf-107">Entry</span></span> | <span data-ttu-id="57ccf-108">Valor</span><span class="sxs-lookup"><span data-stu-id="57ccf-108">Value</span></span> |
|-------------------|-----------------------------------------|
| <span data-ttu-id="57ccf-109">CN</span><span class="sxs-lookup"><span data-stu-id="57ccf-109">CN</span></span>                | <span data-ttu-id="57ccf-110">ms-DS-AZ-Generate-Auditions</span><span class="sxs-lookup"><span data-stu-id="57ccf-110">ms-DS-Az-Generate-Audits</span></span>                |
| <span data-ttu-id="57ccf-111">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="57ccf-111">Ldap-Display-Name</span></span> | <span data-ttu-id="57ccf-112">msDS-AzGenerateAudits</span><span class="sxs-lookup"><span data-stu-id="57ccf-112">msDS-AzGenerateAudits</span></span>                   |
| <span data-ttu-id="57ccf-113">Tamanho</span><span class="sxs-lookup"><span data-stu-id="57ccf-113">Size</span></span>              | \-                                      |
| <span data-ttu-id="57ccf-114">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="57ccf-114">Update Privilege</span></span>  | <span data-ttu-id="57ccf-115">Administrador do AzRoles</span><span class="sxs-lookup"><span data-stu-id="57ccf-115">AzRoles admin</span></span>                           |
| <span data-ttu-id="57ccf-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="57ccf-116">Update Frequency</span></span>  | <span data-ttu-id="57ccf-117">Durante a inicialização ou a alteração da política.</span><span class="sxs-lookup"><span data-stu-id="57ccf-117">During initialization or policy change.</span></span> |
| <span data-ttu-id="57ccf-118">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="57ccf-118">Attribute-Id</span></span>      | <span data-ttu-id="57ccf-119">1.2.840.113556.1.4.1805</span><span class="sxs-lookup"><span data-stu-id="57ccf-119">1.2.840.113556.1.4.1805</span></span>                 |
| <span data-ttu-id="57ccf-120">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="57ccf-120">System-Id-Guid</span></span>    | <span data-ttu-id="57ccf-121">f90abab0-186C-4418-bb85-88447c87222a</span><span class="sxs-lookup"><span data-stu-id="57ccf-121">f90abab0-186c-4418-bb85-88447c87222a</span></span>    |
| <span data-ttu-id="57ccf-122">Syntax</span><span class="sxs-lookup"><span data-stu-id="57ccf-122">Syntax</span></span>            | [<span data-ttu-id="57ccf-123">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="57ccf-123">**Boolean**</span></span>](s-boolean.md)            |



## <a name="implementations"></a><span data-ttu-id="57ccf-124">Implementações</span><span class="sxs-lookup"><span data-stu-id="57ccf-124">Implementations</span></span>

-   [<span data-ttu-id="57ccf-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="57ccf-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="57ccf-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="57ccf-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="57ccf-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="57ccf-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="57ccf-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="57ccf-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="57ccf-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="57ccf-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="57ccf-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="57ccf-130">Windows Server 2003</span></span>



| <span data-ttu-id="57ccf-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="57ccf-131">Entry</span></span> | <span data-ttu-id="57ccf-132">Valor</span><span class="sxs-lookup"><span data-stu-id="57ccf-132">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ccf-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="57ccf-133">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57ccf-134">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="57ccf-135">System-Only</span></span>            | <span data-ttu-id="57ccf-136">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-136">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="57ccf-137">Is-Single-Valued</span></span>       | <span data-ttu-id="57ccf-138">True</span><span class="sxs-lookup"><span data-stu-id="57ccf-138">True</span></span>                                                                                                                               |
| <span data-ttu-id="57ccf-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="57ccf-139">Is Indexed</span></span>             | <span data-ttu-id="57ccf-140">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-140">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="57ccf-141">In Global Catalog</span></span>      | <span data-ttu-id="57ccf-142">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-142">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57ccf-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="57ccf-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="57ccf-144">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="57ccf-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57ccf-145">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57ccf-146">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57ccf-147">Search-Flags</span></span>           | <span data-ttu-id="57ccf-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57ccf-148">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="57ccf-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57ccf-149">System-Flags</span></span>           | <span data-ttu-id="57ccf-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57ccf-150">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="57ccf-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="57ccf-151">Classes used in</span></span>        | [<span data-ttu-id="57ccf-152">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="57ccf-152">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="57ccf-153">**ms-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="57ccf-153">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="57ccf-154">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="57ccf-154">Windows Server 2003 R2</span></span>



| <span data-ttu-id="57ccf-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="57ccf-155">Entry</span></span> | <span data-ttu-id="57ccf-156">Valor</span><span class="sxs-lookup"><span data-stu-id="57ccf-156">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ccf-157">ID do link</span><span class="sxs-lookup"><span data-stu-id="57ccf-157">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-158">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57ccf-158">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-159">System-Only</span><span class="sxs-lookup"><span data-stu-id="57ccf-159">System-Only</span></span>            | <span data-ttu-id="57ccf-160">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-160">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-161">É de valor único</span><span class="sxs-lookup"><span data-stu-id="57ccf-161">Is-Single-Valued</span></span>       | <span data-ttu-id="57ccf-162">True</span><span class="sxs-lookup"><span data-stu-id="57ccf-162">True</span></span>                                                                                                                               |
| <span data-ttu-id="57ccf-163">É indexado</span><span class="sxs-lookup"><span data-stu-id="57ccf-163">Is Indexed</span></span>             | <span data-ttu-id="57ccf-164">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-164">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-165">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="57ccf-165">In Global Catalog</span></span>      | <span data-ttu-id="57ccf-166">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-166">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-167">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57ccf-167">NT-Security-Descriptor</span></span> | <span data-ttu-id="57ccf-168">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="57ccf-168">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="57ccf-169">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57ccf-169">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-170">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57ccf-170">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-171">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57ccf-171">Search-Flags</span></span>           | <span data-ttu-id="57ccf-172">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57ccf-172">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="57ccf-173">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57ccf-173">System-Flags</span></span>           | <span data-ttu-id="57ccf-174">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57ccf-174">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="57ccf-175">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="57ccf-175">Classes used in</span></span>        | [<span data-ttu-id="57ccf-176">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="57ccf-176">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="57ccf-177">**ms-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="57ccf-177">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="57ccf-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="57ccf-178">Windows Server 2008</span></span>



| <span data-ttu-id="57ccf-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="57ccf-179">Entry</span></span> | <span data-ttu-id="57ccf-180">Valor</span><span class="sxs-lookup"><span data-stu-id="57ccf-180">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ccf-181">ID do link</span><span class="sxs-lookup"><span data-stu-id="57ccf-181">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-182">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57ccf-182">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-183">System-Only</span><span class="sxs-lookup"><span data-stu-id="57ccf-183">System-Only</span></span>            | <span data-ttu-id="57ccf-184">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-184">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-185">É de valor único</span><span class="sxs-lookup"><span data-stu-id="57ccf-185">Is-Single-Valued</span></span>       | <span data-ttu-id="57ccf-186">True</span><span class="sxs-lookup"><span data-stu-id="57ccf-186">True</span></span>                                                                                                                               |
| <span data-ttu-id="57ccf-187">É indexado</span><span class="sxs-lookup"><span data-stu-id="57ccf-187">Is Indexed</span></span>             | <span data-ttu-id="57ccf-188">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-188">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-189">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="57ccf-189">In Global Catalog</span></span>      | <span data-ttu-id="57ccf-190">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-190">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-191">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57ccf-191">NT-Security-Descriptor</span></span> | <span data-ttu-id="57ccf-192">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="57ccf-192">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="57ccf-193">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57ccf-193">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-194">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57ccf-194">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-195">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57ccf-195">Search-Flags</span></span>           | <span data-ttu-id="57ccf-196">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57ccf-196">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="57ccf-197">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57ccf-197">System-Flags</span></span>           | <span data-ttu-id="57ccf-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57ccf-198">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="57ccf-199">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="57ccf-199">Classes used in</span></span>        | [<span data-ttu-id="57ccf-200">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="57ccf-200">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="57ccf-201">**ms-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="57ccf-201">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="57ccf-202">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="57ccf-202">Windows Server 2008 R2</span></span>



| <span data-ttu-id="57ccf-203">Entrada</span><span class="sxs-lookup"><span data-stu-id="57ccf-203">Entry</span></span> | <span data-ttu-id="57ccf-204">Valor</span><span class="sxs-lookup"><span data-stu-id="57ccf-204">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ccf-205">ID do link</span><span class="sxs-lookup"><span data-stu-id="57ccf-205">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-206">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57ccf-206">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-207">System-Only</span><span class="sxs-lookup"><span data-stu-id="57ccf-207">System-Only</span></span>            | <span data-ttu-id="57ccf-208">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-208">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-209">É de valor único</span><span class="sxs-lookup"><span data-stu-id="57ccf-209">Is-Single-Valued</span></span>       | <span data-ttu-id="57ccf-210">True</span><span class="sxs-lookup"><span data-stu-id="57ccf-210">True</span></span>                                                                                                                               |
| <span data-ttu-id="57ccf-211">É indexado</span><span class="sxs-lookup"><span data-stu-id="57ccf-211">Is Indexed</span></span>             | <span data-ttu-id="57ccf-212">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-212">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-213">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="57ccf-213">In Global Catalog</span></span>      | <span data-ttu-id="57ccf-214">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-214">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-215">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57ccf-215">NT-Security-Descriptor</span></span> | <span data-ttu-id="57ccf-216">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="57ccf-216">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="57ccf-217">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57ccf-217">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-218">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57ccf-218">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-219">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57ccf-219">Search-Flags</span></span>           | <span data-ttu-id="57ccf-220">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57ccf-220">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="57ccf-221">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57ccf-221">System-Flags</span></span>           | <span data-ttu-id="57ccf-222">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57ccf-222">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="57ccf-223">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="57ccf-223">Classes used in</span></span>        | [<span data-ttu-id="57ccf-224">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="57ccf-224">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="57ccf-225">**ms-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="57ccf-225">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="57ccf-226">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="57ccf-226">Windows Server 2012</span></span>



| <span data-ttu-id="57ccf-227">Entrada</span><span class="sxs-lookup"><span data-stu-id="57ccf-227">Entry</span></span> | <span data-ttu-id="57ccf-228">Valor</span><span class="sxs-lookup"><span data-stu-id="57ccf-228">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57ccf-229">ID do link</span><span class="sxs-lookup"><span data-stu-id="57ccf-229">Link-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-230">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="57ccf-230">MAPI-Id</span></span>                | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-231">System-Only</span><span class="sxs-lookup"><span data-stu-id="57ccf-231">System-Only</span></span>            | <span data-ttu-id="57ccf-232">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-232">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-233">É de valor único</span><span class="sxs-lookup"><span data-stu-id="57ccf-233">Is-Single-Valued</span></span>       | <span data-ttu-id="57ccf-234">True</span><span class="sxs-lookup"><span data-stu-id="57ccf-234">True</span></span>                                                                                                                               |
| <span data-ttu-id="57ccf-235">É indexado</span><span class="sxs-lookup"><span data-stu-id="57ccf-235">Is Indexed</span></span>             | <span data-ttu-id="57ccf-236">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-236">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-237">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="57ccf-237">In Global Catalog</span></span>      | <span data-ttu-id="57ccf-238">Falso</span><span class="sxs-lookup"><span data-stu-id="57ccf-238">False</span></span>                                                                                                                              |
| <span data-ttu-id="57ccf-239">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="57ccf-239">NT-Security-Descriptor</span></span> | <span data-ttu-id="57ccf-240">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="57ccf-240">O:BAG:BAD:S:</span></span>                                                                                                                       |
| <span data-ttu-id="57ccf-241">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="57ccf-241">Range-Lower</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-242">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="57ccf-242">Range-Upper</span></span>            | \-                                                                                                                                 |
| <span data-ttu-id="57ccf-243">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="57ccf-243">Search-Flags</span></span>           | <span data-ttu-id="57ccf-244">0x00000000</span><span class="sxs-lookup"><span data-stu-id="57ccf-244">0x00000000</span></span>                                                                                                                         |
| <span data-ttu-id="57ccf-245">System-Flags</span><span class="sxs-lookup"><span data-stu-id="57ccf-245">System-Flags</span></span>           | <span data-ttu-id="57ccf-246">0x00000010</span><span class="sxs-lookup"><span data-stu-id="57ccf-246">0x00000010</span></span>                                                                                                                         |
| <span data-ttu-id="57ccf-247">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="57ccf-247">Classes used in</span></span>        | [<span data-ttu-id="57ccf-248">**ms-DS-AZ-admin-Manager**</span><span class="sxs-lookup"><span data-stu-id="57ccf-248">**ms-DS-Az-Admin-Manager**</span></span>](c-msds-azadminmanager.md)<br/> [<span data-ttu-id="57ccf-249">**ms-DS-AZ-Application**</span><span class="sxs-lookup"><span data-stu-id="57ccf-249">**ms-DS-Az-Application**</span></span>](c-msds-azapplication.md)<br/> |



 

 





