---
title: Atributo de Gerenciador
description: Contém o nome distinto do usuário que é o gerente do usuário. O objeto de usuário do gerente contém uma propriedade directReports que contém referências a todos os objetos de usuário que têm suas propriedades de Gerenciador definidas para esse nome distinto.
ms.assetid: 40743784-a99c-4ec0-9140-9f865c073244
ms.tgt_platform: multiple
keywords:
- Esquema do atributo do Gerenciador de AD
- Esquema do atributo do Gerenciador de AD
topic_type:
- apiref
api_name:
- Manager
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f42c659a436f9798861f5c37df19f8d10db91127
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104369992"
---
# <a name="manager-attribute"></a><span data-ttu-id="00d56-106">Atributo de Gerenciador</span><span class="sxs-lookup"><span data-stu-id="00d56-106">Manager attribute</span></span>

<span data-ttu-id="00d56-107">Contém o nome distinto do usuário que é o gerente do usuário.</span><span class="sxs-lookup"><span data-stu-id="00d56-107">Contains the distinguished name of the user who is the user's manager.</span></span> <span data-ttu-id="00d56-108">O objeto de usuário do gerente contém uma propriedade directReports que contém referências a todos os objetos de usuário que têm suas propriedades de Gerenciador definidas para esse nome distinto.</span><span class="sxs-lookup"><span data-stu-id="00d56-108">The manager's user object contains a directReports property that contains references to all user objects that have their manager properties set to this distinguished name.</span></span>



| <span data-ttu-id="00d56-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="00d56-109">Entry</span></span> | <span data-ttu-id="00d56-110">Valor</span><span class="sxs-lookup"><span data-stu-id="00d56-110">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="00d56-111">CN</span><span class="sxs-lookup"><span data-stu-id="00d56-111">CN</span></span>                | <span data-ttu-id="00d56-112">Gerente</span><span class="sxs-lookup"><span data-stu-id="00d56-112">Manager</span></span>                                                                     |
| <span data-ttu-id="00d56-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="00d56-113">Ldap-Display-Name</span></span> | <span data-ttu-id="00d56-114">manager</span><span class="sxs-lookup"><span data-stu-id="00d56-114">manager</span></span>                                                                     |
| <span data-ttu-id="00d56-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="00d56-115">Size</span></span>              | \-                                                                          |
| <span data-ttu-id="00d56-116">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="00d56-116">Update Privilege</span></span>  | <span data-ttu-id="00d56-117">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="00d56-117">Domain administrator or account owner.</span></span>                                      |
| <span data-ttu-id="00d56-118">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="00d56-118">Update Frequency</span></span>  | <span data-ttu-id="00d56-119">Quando o registro do usuário é criado e sempre que o gerente precisa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="00d56-119">When the user's record is created and whenever the manager needs to change.</span></span> |
| <span data-ttu-id="00d56-120">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="00d56-120">Attribute-Id</span></span>      | <span data-ttu-id="00d56-121">0.9.2342.19200300.100.1.10</span><span class="sxs-lookup"><span data-stu-id="00d56-121">0.9.2342.19200300.100.1.10</span></span>                                                  |
| <span data-ttu-id="00d56-122">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="00d56-122">System-Id-Guid</span></span>    | <span data-ttu-id="00d56-123">bf9679b5-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="00d56-123">bf9679b5-0de6-11d0-a285-00aa003049e2</span></span>                                        |
| <span data-ttu-id="00d56-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="00d56-124">Syntax</span></span>            | [<span data-ttu-id="00d56-125">**Objeto (DS-DN)**</span><span class="sxs-lookup"><span data-stu-id="00d56-125">**Object(DS-DN)**</span></span>](s-object-ds-dn.md)                                     |



## <a name="implementations"></a><span data-ttu-id="00d56-126">Implementações</span><span class="sxs-lookup"><span data-stu-id="00d56-126">Implementations</span></span>

-   [<span data-ttu-id="00d56-127">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="00d56-127">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="00d56-128">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="00d56-128">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="00d56-129">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="00d56-129">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="00d56-130">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="00d56-130">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="00d56-131">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="00d56-131">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="00d56-132">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="00d56-132">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="00d56-133">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="00d56-133">Windows 2000 Server</span></span>



| <span data-ttu-id="00d56-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="00d56-134">Entry</span></span> | <span data-ttu-id="00d56-135">Valor</span><span class="sxs-lookup"><span data-stu-id="00d56-135">Value</span></span> |
|------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="00d56-136">ID do link</span><span class="sxs-lookup"><span data-stu-id="00d56-136">Link-Id</span></span>                | <span data-ttu-id="00d56-137">42</span><span class="sxs-lookup"><span data-stu-id="00d56-137">42</span></span>                                                                 |
| <span data-ttu-id="00d56-138">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d56-138">MAPI-Id</span></span>                | <span data-ttu-id="00d56-139">0x8005</span><span class="sxs-lookup"><span data-stu-id="00d56-139">0x8005</span></span>                                                             |
| <span data-ttu-id="00d56-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d56-140">System-Only</span></span>            | <span data-ttu-id="00d56-141">Falso</span><span class="sxs-lookup"><span data-stu-id="00d56-141">False</span></span>                                                              |
| <span data-ttu-id="00d56-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="00d56-142">Is-Single-Valued</span></span>       | <span data-ttu-id="00d56-143">True</span><span class="sxs-lookup"><span data-stu-id="00d56-143">True</span></span>                                                               |
| <span data-ttu-id="00d56-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="00d56-144">Is Indexed</span></span>             | <span data-ttu-id="00d56-145">Falso</span><span class="sxs-lookup"><span data-stu-id="00d56-145">False</span></span>                                                              |
| <span data-ttu-id="00d56-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="00d56-146">In Global Catalog</span></span>      | <span data-ttu-id="00d56-147">True</span><span class="sxs-lookup"><span data-stu-id="00d56-147">True</span></span>                                                               |
| <span data-ttu-id="00d56-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="00d56-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d56-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="00d56-149">O:BAG:BAD:S:</span></span>                                                       |
| <span data-ttu-id="00d56-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d56-150">Range-Lower</span></span>            | \-                                                                 |
| <span data-ttu-id="00d56-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d56-151">Range-Upper</span></span>            | \-                                                                 |
| <span data-ttu-id="00d56-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d56-152">Search-Flags</span></span>           | <span data-ttu-id="00d56-153">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d56-153">0x00000010</span></span>                                                         |
| <span data-ttu-id="00d56-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d56-154">System-Flags</span></span>           | <span data-ttu-id="00d56-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d56-155">0x00000010</span></span>                                                         |
| <span data-ttu-id="00d56-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="00d56-156">Classes used in</span></span>        | [<span data-ttu-id="00d56-157">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="00d56-157">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="00d56-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="00d56-158">Windows Server 2003</span></span>



| <span data-ttu-id="00d56-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="00d56-159">Entry</span></span> | <span data-ttu-id="00d56-160">Valor</span><span class="sxs-lookup"><span data-stu-id="00d56-160">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d56-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="00d56-161">Link-Id</span></span>                | <span data-ttu-id="00d56-162">42</span><span class="sxs-lookup"><span data-stu-id="00d56-162">42</span></span>                                                                                                                     |
| <span data-ttu-id="00d56-163">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d56-163">MAPI-Id</span></span>                | <span data-ttu-id="00d56-164">0x8005</span><span class="sxs-lookup"><span data-stu-id="00d56-164">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="00d56-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d56-165">System-Only</span></span>            | <span data-ttu-id="00d56-166">Falso</span><span class="sxs-lookup"><span data-stu-id="00d56-166">False</span></span>                                                                                                                  |
| <span data-ttu-id="00d56-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="00d56-167">Is-Single-Valued</span></span>       | <span data-ttu-id="00d56-168">True</span><span class="sxs-lookup"><span data-stu-id="00d56-168">True</span></span>                                                                                                                   |
| <span data-ttu-id="00d56-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="00d56-169">Is Indexed</span></span>             | <span data-ttu-id="00d56-170">Falso</span><span class="sxs-lookup"><span data-stu-id="00d56-170">False</span></span>                                                                                                                  |
| <span data-ttu-id="00d56-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="00d56-171">In Global Catalog</span></span>      | <span data-ttu-id="00d56-172">True</span><span class="sxs-lookup"><span data-stu-id="00d56-172">True</span></span>                                                                                                                   |
| <span data-ttu-id="00d56-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="00d56-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d56-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="00d56-174">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="00d56-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d56-175">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="00d56-176">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d56-176">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="00d56-177">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d56-177">Search-Flags</span></span>           | <span data-ttu-id="00d56-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d56-178">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="00d56-179">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d56-179">System-Flags</span></span>           | <span data-ttu-id="00d56-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d56-180">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="00d56-181">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="00d56-181">Classes used in</span></span>        | [<span data-ttu-id="00d56-182">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="00d56-182">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="00d56-183">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="00d56-183">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="00d56-184">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="00d56-184">Windows Server 2003 R2</span></span>



| <span data-ttu-id="00d56-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="00d56-185">Entry</span></span> | <span data-ttu-id="00d56-186">Valor</span><span class="sxs-lookup"><span data-stu-id="00d56-186">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d56-187">ID do link</span><span class="sxs-lookup"><span data-stu-id="00d56-187">Link-Id</span></span>                | <span data-ttu-id="00d56-188">42</span><span class="sxs-lookup"><span data-stu-id="00d56-188">42</span></span>                                                                                                                     |
| <span data-ttu-id="00d56-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d56-189">MAPI-Id</span></span>                | <span data-ttu-id="00d56-190">0x8005</span><span class="sxs-lookup"><span data-stu-id="00d56-190">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="00d56-191">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d56-191">System-Only</span></span>            | <span data-ttu-id="00d56-192">Falso</span><span class="sxs-lookup"><span data-stu-id="00d56-192">False</span></span>                                                                                                                  |
| <span data-ttu-id="00d56-193">É de valor único</span><span class="sxs-lookup"><span data-stu-id="00d56-193">Is-Single-Valued</span></span>       | <span data-ttu-id="00d56-194">True</span><span class="sxs-lookup"><span data-stu-id="00d56-194">True</span></span>                                                                                                                   |
| <span data-ttu-id="00d56-195">É indexado</span><span class="sxs-lookup"><span data-stu-id="00d56-195">Is Indexed</span></span>             | <span data-ttu-id="00d56-196">Falso</span><span class="sxs-lookup"><span data-stu-id="00d56-196">False</span></span>                                                                                                                  |
| <span data-ttu-id="00d56-197">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="00d56-197">In Global Catalog</span></span>      | <span data-ttu-id="00d56-198">True</span><span class="sxs-lookup"><span data-stu-id="00d56-198">True</span></span>                                                                                                                   |
| <span data-ttu-id="00d56-199">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="00d56-199">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d56-200">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="00d56-200">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="00d56-201">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d56-201">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="00d56-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d56-202">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="00d56-203">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d56-203">Search-Flags</span></span>           | <span data-ttu-id="00d56-204">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d56-204">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="00d56-205">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d56-205">System-Flags</span></span>           | <span data-ttu-id="00d56-206">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d56-206">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="00d56-207">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="00d56-207">Classes used in</span></span>        | [<span data-ttu-id="00d56-208">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="00d56-208">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="00d56-209">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="00d56-209">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="00d56-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00d56-210">Windows Server 2008</span></span>



| <span data-ttu-id="00d56-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="00d56-211">Entry</span></span> | <span data-ttu-id="00d56-212">Valor</span><span class="sxs-lookup"><span data-stu-id="00d56-212">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d56-213">ID do link</span><span class="sxs-lookup"><span data-stu-id="00d56-213">Link-Id</span></span>                | <span data-ttu-id="00d56-214">42</span><span class="sxs-lookup"><span data-stu-id="00d56-214">42</span></span>                                                                                                                     |
| <span data-ttu-id="00d56-215">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d56-215">MAPI-Id</span></span>                | <span data-ttu-id="00d56-216">0x8005</span><span class="sxs-lookup"><span data-stu-id="00d56-216">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="00d56-217">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d56-217">System-Only</span></span>            | <span data-ttu-id="00d56-218">Falso</span><span class="sxs-lookup"><span data-stu-id="00d56-218">False</span></span>                                                                                                                  |
| <span data-ttu-id="00d56-219">É de valor único</span><span class="sxs-lookup"><span data-stu-id="00d56-219">Is-Single-Valued</span></span>       | <span data-ttu-id="00d56-220">True</span><span class="sxs-lookup"><span data-stu-id="00d56-220">True</span></span>                                                                                                                   |
| <span data-ttu-id="00d56-221">É indexado</span><span class="sxs-lookup"><span data-stu-id="00d56-221">Is Indexed</span></span>             | <span data-ttu-id="00d56-222">Falso</span><span class="sxs-lookup"><span data-stu-id="00d56-222">False</span></span>                                                                                                                  |
| <span data-ttu-id="00d56-223">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="00d56-223">In Global Catalog</span></span>      | <span data-ttu-id="00d56-224">True</span><span class="sxs-lookup"><span data-stu-id="00d56-224">True</span></span>                                                                                                                   |
| <span data-ttu-id="00d56-225">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="00d56-225">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d56-226">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="00d56-226">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="00d56-227">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d56-227">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="00d56-228">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d56-228">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="00d56-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d56-229">Search-Flags</span></span>           | <span data-ttu-id="00d56-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d56-230">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="00d56-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d56-231">System-Flags</span></span>           | <span data-ttu-id="00d56-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d56-232">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="00d56-233">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="00d56-233">Classes used in</span></span>        | [<span data-ttu-id="00d56-234">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="00d56-234">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="00d56-235">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="00d56-235">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="00d56-236">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="00d56-236">Windows Server 2008 R2</span></span>



| <span data-ttu-id="00d56-237">Entrada</span><span class="sxs-lookup"><span data-stu-id="00d56-237">Entry</span></span> | <span data-ttu-id="00d56-238">Valor</span><span class="sxs-lookup"><span data-stu-id="00d56-238">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d56-239">ID do link</span><span class="sxs-lookup"><span data-stu-id="00d56-239">Link-Id</span></span>                | <span data-ttu-id="00d56-240">42</span><span class="sxs-lookup"><span data-stu-id="00d56-240">42</span></span>                                                                                                                     |
| <span data-ttu-id="00d56-241">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d56-241">MAPI-Id</span></span>                | <span data-ttu-id="00d56-242">0x8005</span><span class="sxs-lookup"><span data-stu-id="00d56-242">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="00d56-243">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d56-243">System-Only</span></span>            | <span data-ttu-id="00d56-244">Falso</span><span class="sxs-lookup"><span data-stu-id="00d56-244">False</span></span>                                                                                                                  |
| <span data-ttu-id="00d56-245">É de valor único</span><span class="sxs-lookup"><span data-stu-id="00d56-245">Is-Single-Valued</span></span>       | <span data-ttu-id="00d56-246">True</span><span class="sxs-lookup"><span data-stu-id="00d56-246">True</span></span>                                                                                                                   |
| <span data-ttu-id="00d56-247">É indexado</span><span class="sxs-lookup"><span data-stu-id="00d56-247">Is Indexed</span></span>             | <span data-ttu-id="00d56-248">Falso</span><span class="sxs-lookup"><span data-stu-id="00d56-248">False</span></span>                                                                                                                  |
| <span data-ttu-id="00d56-249">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="00d56-249">In Global Catalog</span></span>      | <span data-ttu-id="00d56-250">True</span><span class="sxs-lookup"><span data-stu-id="00d56-250">True</span></span>                                                                                                                   |
| <span data-ttu-id="00d56-251">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="00d56-251">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d56-252">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="00d56-252">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="00d56-253">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d56-253">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="00d56-254">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d56-254">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="00d56-255">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d56-255">Search-Flags</span></span>           | <span data-ttu-id="00d56-256">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d56-256">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="00d56-257">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d56-257">System-Flags</span></span>           | <span data-ttu-id="00d56-258">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d56-258">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="00d56-259">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="00d56-259">Classes used in</span></span>        | [<span data-ttu-id="00d56-260">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="00d56-260">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="00d56-261">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="00d56-261">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="00d56-262">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="00d56-262">Windows Server 2012</span></span>



| <span data-ttu-id="00d56-263">Entrada</span><span class="sxs-lookup"><span data-stu-id="00d56-263">Entry</span></span> | <span data-ttu-id="00d56-264">Valor</span><span class="sxs-lookup"><span data-stu-id="00d56-264">Value</span></span> |
|------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00d56-265">ID do link</span><span class="sxs-lookup"><span data-stu-id="00d56-265">Link-Id</span></span>                | <span data-ttu-id="00d56-266">42</span><span class="sxs-lookup"><span data-stu-id="00d56-266">42</span></span>                                                                                                                     |
| <span data-ttu-id="00d56-267">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="00d56-267">MAPI-Id</span></span>                | <span data-ttu-id="00d56-268">0x8005</span><span class="sxs-lookup"><span data-stu-id="00d56-268">0x8005</span></span>                                                                                                                 |
| <span data-ttu-id="00d56-269">System-Only</span><span class="sxs-lookup"><span data-stu-id="00d56-269">System-Only</span></span>            | <span data-ttu-id="00d56-270">Falso</span><span class="sxs-lookup"><span data-stu-id="00d56-270">False</span></span>                                                                                                                  |
| <span data-ttu-id="00d56-271">É de valor único</span><span class="sxs-lookup"><span data-stu-id="00d56-271">Is-Single-Valued</span></span>       | <span data-ttu-id="00d56-272">True</span><span class="sxs-lookup"><span data-stu-id="00d56-272">True</span></span>                                                                                                                   |
| <span data-ttu-id="00d56-273">É indexado</span><span class="sxs-lookup"><span data-stu-id="00d56-273">Is Indexed</span></span>             | <span data-ttu-id="00d56-274">Falso</span><span class="sxs-lookup"><span data-stu-id="00d56-274">False</span></span>                                                                                                                  |
| <span data-ttu-id="00d56-275">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="00d56-275">In Global Catalog</span></span>      | <span data-ttu-id="00d56-276">True</span><span class="sxs-lookup"><span data-stu-id="00d56-276">True</span></span>                                                                                                                   |
| <span data-ttu-id="00d56-277">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="00d56-277">NT-Security-Descriptor</span></span> | <span data-ttu-id="00d56-278">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="00d56-278">O:BAG:BAD:S:</span></span>                                                                                                           |
| <span data-ttu-id="00d56-279">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="00d56-279">Range-Lower</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="00d56-280">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="00d56-280">Range-Upper</span></span>            | \-                                                                                                                     |
| <span data-ttu-id="00d56-281">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="00d56-281">Search-Flags</span></span>           | <span data-ttu-id="00d56-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d56-282">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="00d56-283">System-Flags</span><span class="sxs-lookup"><span data-stu-id="00d56-283">System-Flags</span></span>           | <span data-ttu-id="00d56-284">0x00000010</span><span class="sxs-lookup"><span data-stu-id="00d56-284">0x00000010</span></span>                                                                                                             |
| <span data-ttu-id="00d56-285">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="00d56-285">Classes used in</span></span>        | [<span data-ttu-id="00d56-286">**inetOrgPerson**</span><span class="sxs-lookup"><span data-stu-id="00d56-286">**inetOrgPerson**</span></span>](c-inetorgperson.md)<br/> [<span data-ttu-id="00d56-287">**Organizational-Person**</span><span class="sxs-lookup"><span data-stu-id="00d56-287">**Organizational-Person**</span></span>](c-organizationalperson.md)<br/> |



 

 





