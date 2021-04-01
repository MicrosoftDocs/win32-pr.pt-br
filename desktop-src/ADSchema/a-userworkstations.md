---
title: User-Workstations atributo
description: Contém os nomes NetBIOS ou DNS dos computadores que executam o Windows NT Workstation ou o Windows 2000 Professional do qual o usuário pode fazer logon.
ms.assetid: 92af070b-dadd-404d-8305-d85974639958
ms.tgt_platform: multiple
keywords:
- Esquema de User-Workstations do atributo AD
- Esquema de AD de atributos do userworkstations
topic_type:
- apiref
api_name:
- User-Workstations
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cad59905dbf24c8baa13969d9a2ce5452767163
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103825067"
---
# <a name="user-workstations-attribute"></a><span data-ttu-id="1725a-105">User-Workstations atributo</span><span class="sxs-lookup"><span data-stu-id="1725a-105">User-Workstations attribute</span></span>

<span data-ttu-id="1725a-106">Contém os nomes NetBIOS ou DNS dos computadores que executam o Windows NT Workstation ou o Windows 2000 Professional do qual o usuário pode fazer logon.</span><span class="sxs-lookup"><span data-stu-id="1725a-106">Contains the NetBIOS or DNS names of the computers running Windows NT Workstation or Windows 2000 Professional from which the user can log on.</span></span> <span data-ttu-id="1725a-107">Cada nome NetBIOS é separado por uma vírgula.</span><span class="sxs-lookup"><span data-stu-id="1725a-107">Each NetBIOS name is separated by a comma.</span></span> <span data-ttu-id="1725a-108">Vários nomes devem ser separados por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="1725a-108">Multiple names should be separated by commas.</span></span>

>[!Note]
><span data-ttu-id="1725a-109">Este atributo de usuário não deve mais ser usado.</span><span class="sxs-lookup"><span data-stu-id="1725a-109">This user attribute should not be used anymore.</span></span> <span data-ttu-id="1725a-110">Para gerenciar quais contas podem fazer logon em quais estações de trabalho, é recomendável usar "permitir logon local" e "Negar logon localmente" ou "permitir logon por meio de Serviços de Área de Trabalho Remota" e "Negar logon por meio de Serviços de Área de Trabalho Remota".</span><span class="sxs-lookup"><span data-stu-id="1725a-110">To manage what accounts can logon to which workstations, we recommend using the “Allow Log on locally” and “Deny Log on locally” or “Allow log on through Remote Desktop Services” and “Deny log on through Remote Desktop Services”.</span></span>

| <span data-ttu-id="1725a-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="1725a-111">Entry</span></span> | <span data-ttu-id="1725a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="1725a-112">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="1725a-113">CN</span><span class="sxs-lookup"><span data-stu-id="1725a-113">CN</span></span>                | <span data-ttu-id="1725a-114">User-Workstations</span><span class="sxs-lookup"><span data-stu-id="1725a-114">User-Workstations</span></span>                                                                          |
| <span data-ttu-id="1725a-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="1725a-115">Ldap-Display-Name</span></span> | <span data-ttu-id="1725a-116">userestações de trabalho</span><span class="sxs-lookup"><span data-stu-id="1725a-116">userWorkstations</span></span>                                                                           |
| <span data-ttu-id="1725a-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="1725a-117">Size</span></span>              | \-                                                                                         |
| <span data-ttu-id="1725a-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="1725a-118">Update Privilege</span></span>  | <span data-ttu-id="1725a-119">Administrador de domínio ou proprietário da conta.</span><span class="sxs-lookup"><span data-stu-id="1725a-119">Domain administrator or account owner.</span></span>                                                     |
| <span data-ttu-id="1725a-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="1725a-120">Update Frequency</span></span>  | <span data-ttu-id="1725a-121">Quando o registro do usuário é criado e sempre que o privilégio de logon do usuário precisa ser alterado.</span><span class="sxs-lookup"><span data-stu-id="1725a-121">When the user's record is created and whenever the user's login privilege needs to change.</span></span> |
| <span data-ttu-id="1725a-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="1725a-122">Attribute-Id</span></span>      | <span data-ttu-id="1725a-123">1.2.840.113556.1.4.86</span><span class="sxs-lookup"><span data-stu-id="1725a-123">1.2.840.113556.1.4.86</span></span>                                                                      |
| <span data-ttu-id="1725a-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="1725a-124">System-Id-Guid</span></span>    | <span data-ttu-id="1725a-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="1725a-125">bf9679d7-0de6-11d0-a285-00aa003049e2</span></span>                                                       |
| <span data-ttu-id="1725a-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="1725a-126">Syntax</span></span>            | [<span data-ttu-id="1725a-127">**Cadeia de caracteres (Unicode)**</span><span class="sxs-lookup"><span data-stu-id="1725a-127">**String(Unicode)**</span></span>](s-string-unicode.md)                                                |



## <a name="implementations"></a><span data-ttu-id="1725a-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="1725a-128">Implementations</span></span>

-   [<span data-ttu-id="1725a-129">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="1725a-129">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="1725a-130">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="1725a-130">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="1725a-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="1725a-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="1725a-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="1725a-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="1725a-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="1725a-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="1725a-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="1725a-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="1725a-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1725a-135">Windows 2000 Server</span></span>



| <span data-ttu-id="1725a-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="1725a-136">Entry</span></span> | <span data-ttu-id="1725a-137">Valor</span><span class="sxs-lookup"><span data-stu-id="1725a-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1725a-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="1725a-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1725a-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1725a-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1725a-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="1725a-140">System-Only</span></span>            | <span data-ttu-id="1725a-141">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-141">False</span></span>                             |
| <span data-ttu-id="1725a-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1725a-142">Is-Single-Valued</span></span>       | <span data-ttu-id="1725a-143">True</span><span class="sxs-lookup"><span data-stu-id="1725a-143">True</span></span>                              |
| <span data-ttu-id="1725a-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="1725a-144">Is Indexed</span></span>             | <span data-ttu-id="1725a-145">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-145">False</span></span>                             |
| <span data-ttu-id="1725a-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1725a-146">In Global Catalog</span></span>      | <span data-ttu-id="1725a-147">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-147">False</span></span>                             |
| <span data-ttu-id="1725a-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1725a-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="1725a-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1725a-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1725a-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1725a-150">Range-Lower</span></span>            | <span data-ttu-id="1725a-151">0</span><span class="sxs-lookup"><span data-stu-id="1725a-151">0</span></span>                                 |
| <span data-ttu-id="1725a-152">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1725a-152">Range-Upper</span></span>            | <span data-ttu-id="1725a-153">1024</span><span class="sxs-lookup"><span data-stu-id="1725a-153">1024</span></span>                              |
| <span data-ttu-id="1725a-154">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1725a-154">Search-Flags</span></span>           | <span data-ttu-id="1725a-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1725a-155">0x00000010</span></span>                        |
| <span data-ttu-id="1725a-156">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1725a-156">System-Flags</span></span>           | <span data-ttu-id="1725a-157">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1725a-157">0x00000010</span></span>                        |
| <span data-ttu-id="1725a-158">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1725a-158">Classes used in</span></span>        | [<span data-ttu-id="1725a-159">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="1725a-159">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="1725a-160">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1725a-160">Windows Server 2003</span></span>



| <span data-ttu-id="1725a-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="1725a-161">Entry</span></span> | <span data-ttu-id="1725a-162">Valor</span><span class="sxs-lookup"><span data-stu-id="1725a-162">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1725a-163">ID do link</span><span class="sxs-lookup"><span data-stu-id="1725a-163">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1725a-164">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1725a-164">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1725a-165">System-Only</span><span class="sxs-lookup"><span data-stu-id="1725a-165">System-Only</span></span>            | <span data-ttu-id="1725a-166">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-166">False</span></span>                             |
| <span data-ttu-id="1725a-167">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1725a-167">Is-Single-Valued</span></span>       | <span data-ttu-id="1725a-168">True</span><span class="sxs-lookup"><span data-stu-id="1725a-168">True</span></span>                              |
| <span data-ttu-id="1725a-169">É indexado</span><span class="sxs-lookup"><span data-stu-id="1725a-169">Is Indexed</span></span>             | <span data-ttu-id="1725a-170">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-170">False</span></span>                             |
| <span data-ttu-id="1725a-171">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1725a-171">In Global Catalog</span></span>      | <span data-ttu-id="1725a-172">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-172">False</span></span>                             |
| <span data-ttu-id="1725a-173">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1725a-173">NT-Security-Descriptor</span></span> | <span data-ttu-id="1725a-174">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1725a-174">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1725a-175">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1725a-175">Range-Lower</span></span>            | <span data-ttu-id="1725a-176">0</span><span class="sxs-lookup"><span data-stu-id="1725a-176">0</span></span>                                 |
| <span data-ttu-id="1725a-177">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1725a-177">Range-Upper</span></span>            | <span data-ttu-id="1725a-178">1024</span><span class="sxs-lookup"><span data-stu-id="1725a-178">1024</span></span>                              |
| <span data-ttu-id="1725a-179">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1725a-179">Search-Flags</span></span>           | <span data-ttu-id="1725a-180">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1725a-180">0x00000010</span></span>                        |
| <span data-ttu-id="1725a-181">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1725a-181">System-Flags</span></span>           | <span data-ttu-id="1725a-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1725a-182">0x00000010</span></span>                        |
| <span data-ttu-id="1725a-183">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1725a-183">Classes used in</span></span>        | [<span data-ttu-id="1725a-184">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="1725a-184">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="1725a-185">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="1725a-185">Windows Server 2003 R2</span></span>



| <span data-ttu-id="1725a-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="1725a-186">Entry</span></span> | <span data-ttu-id="1725a-187">Valor</span><span class="sxs-lookup"><span data-stu-id="1725a-187">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1725a-188">ID do link</span><span class="sxs-lookup"><span data-stu-id="1725a-188">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1725a-189">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1725a-189">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1725a-190">System-Only</span><span class="sxs-lookup"><span data-stu-id="1725a-190">System-Only</span></span>            | <span data-ttu-id="1725a-191">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-191">False</span></span>                             |
| <span data-ttu-id="1725a-192">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1725a-192">Is-Single-Valued</span></span>       | <span data-ttu-id="1725a-193">True</span><span class="sxs-lookup"><span data-stu-id="1725a-193">True</span></span>                              |
| <span data-ttu-id="1725a-194">É indexado</span><span class="sxs-lookup"><span data-stu-id="1725a-194">Is Indexed</span></span>             | <span data-ttu-id="1725a-195">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-195">False</span></span>                             |
| <span data-ttu-id="1725a-196">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1725a-196">In Global Catalog</span></span>      | <span data-ttu-id="1725a-197">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-197">False</span></span>                             |
| <span data-ttu-id="1725a-198">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1725a-198">NT-Security-Descriptor</span></span> | <span data-ttu-id="1725a-199">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1725a-199">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1725a-200">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1725a-200">Range-Lower</span></span>            | <span data-ttu-id="1725a-201">0</span><span class="sxs-lookup"><span data-stu-id="1725a-201">0</span></span>                                 |
| <span data-ttu-id="1725a-202">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1725a-202">Range-Upper</span></span>            | <span data-ttu-id="1725a-203">1024</span><span class="sxs-lookup"><span data-stu-id="1725a-203">1024</span></span>                              |
| <span data-ttu-id="1725a-204">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1725a-204">Search-Flags</span></span>           | <span data-ttu-id="1725a-205">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1725a-205">0x00000010</span></span>                        |
| <span data-ttu-id="1725a-206">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1725a-206">System-Flags</span></span>           | <span data-ttu-id="1725a-207">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1725a-207">0x00000010</span></span>                        |
| <span data-ttu-id="1725a-208">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1725a-208">Classes used in</span></span>        | [<span data-ttu-id="1725a-209">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="1725a-209">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="1725a-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1725a-210">Windows Server 2008</span></span>



| <span data-ttu-id="1725a-211">Entrada</span><span class="sxs-lookup"><span data-stu-id="1725a-211">Entry</span></span> | <span data-ttu-id="1725a-212">Valor</span><span class="sxs-lookup"><span data-stu-id="1725a-212">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1725a-213">ID do link</span><span class="sxs-lookup"><span data-stu-id="1725a-213">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1725a-214">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1725a-214">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1725a-215">System-Only</span><span class="sxs-lookup"><span data-stu-id="1725a-215">System-Only</span></span>            | <span data-ttu-id="1725a-216">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-216">False</span></span>                             |
| <span data-ttu-id="1725a-217">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1725a-217">Is-Single-Valued</span></span>       | <span data-ttu-id="1725a-218">True</span><span class="sxs-lookup"><span data-stu-id="1725a-218">True</span></span>                              |
| <span data-ttu-id="1725a-219">É indexado</span><span class="sxs-lookup"><span data-stu-id="1725a-219">Is Indexed</span></span>             | <span data-ttu-id="1725a-220">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-220">False</span></span>                             |
| <span data-ttu-id="1725a-221">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1725a-221">In Global Catalog</span></span>      | <span data-ttu-id="1725a-222">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-222">False</span></span>                             |
| <span data-ttu-id="1725a-223">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1725a-223">NT-Security-Descriptor</span></span> | <span data-ttu-id="1725a-224">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1725a-224">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1725a-225">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1725a-225">Range-Lower</span></span>            | <span data-ttu-id="1725a-226">0</span><span class="sxs-lookup"><span data-stu-id="1725a-226">0</span></span>                                 |
| <span data-ttu-id="1725a-227">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1725a-227">Range-Upper</span></span>            | <span data-ttu-id="1725a-228">1024</span><span class="sxs-lookup"><span data-stu-id="1725a-228">1024</span></span>                              |
| <span data-ttu-id="1725a-229">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1725a-229">Search-Flags</span></span>           | <span data-ttu-id="1725a-230">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1725a-230">0x00000010</span></span>                        |
| <span data-ttu-id="1725a-231">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1725a-231">System-Flags</span></span>           | <span data-ttu-id="1725a-232">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1725a-232">0x00000010</span></span>                        |
| <span data-ttu-id="1725a-233">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1725a-233">Classes used in</span></span>        | [<span data-ttu-id="1725a-234">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="1725a-234">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="1725a-235">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1725a-235">Windows Server 2008 R2</span></span>



| <span data-ttu-id="1725a-236">Entrada</span><span class="sxs-lookup"><span data-stu-id="1725a-236">Entry</span></span> | <span data-ttu-id="1725a-237">Valor</span><span class="sxs-lookup"><span data-stu-id="1725a-237">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1725a-238">ID do link</span><span class="sxs-lookup"><span data-stu-id="1725a-238">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1725a-239">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1725a-239">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1725a-240">System-Only</span><span class="sxs-lookup"><span data-stu-id="1725a-240">System-Only</span></span>            | <span data-ttu-id="1725a-241">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-241">False</span></span>                             |
| <span data-ttu-id="1725a-242">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1725a-242">Is-Single-Valued</span></span>       | <span data-ttu-id="1725a-243">True</span><span class="sxs-lookup"><span data-stu-id="1725a-243">True</span></span>                              |
| <span data-ttu-id="1725a-244">É indexado</span><span class="sxs-lookup"><span data-stu-id="1725a-244">Is Indexed</span></span>             | <span data-ttu-id="1725a-245">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-245">False</span></span>                             |
| <span data-ttu-id="1725a-246">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1725a-246">In Global Catalog</span></span>      | <span data-ttu-id="1725a-247">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-247">False</span></span>                             |
| <span data-ttu-id="1725a-248">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1725a-248">NT-Security-Descriptor</span></span> | <span data-ttu-id="1725a-249">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1725a-249">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1725a-250">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1725a-250">Range-Lower</span></span>            | <span data-ttu-id="1725a-251">0</span><span class="sxs-lookup"><span data-stu-id="1725a-251">0</span></span>                                 |
| <span data-ttu-id="1725a-252">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1725a-252">Range-Upper</span></span>            | <span data-ttu-id="1725a-253">1024</span><span class="sxs-lookup"><span data-stu-id="1725a-253">1024</span></span>                              |
| <span data-ttu-id="1725a-254">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1725a-254">Search-Flags</span></span>           | <span data-ttu-id="1725a-255">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1725a-255">0x00000010</span></span>                        |
| <span data-ttu-id="1725a-256">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1725a-256">System-Flags</span></span>           | <span data-ttu-id="1725a-257">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1725a-257">0x00000010</span></span>                        |
| <span data-ttu-id="1725a-258">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1725a-258">Classes used in</span></span>        | [<span data-ttu-id="1725a-259">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="1725a-259">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="1725a-260">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1725a-260">Windows Server 2012</span></span>



| <span data-ttu-id="1725a-261">Entrada</span><span class="sxs-lookup"><span data-stu-id="1725a-261">Entry</span></span> | <span data-ttu-id="1725a-262">Valor</span><span class="sxs-lookup"><span data-stu-id="1725a-262">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="1725a-263">ID do link</span><span class="sxs-lookup"><span data-stu-id="1725a-263">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="1725a-264">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="1725a-264">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="1725a-265">System-Only</span><span class="sxs-lookup"><span data-stu-id="1725a-265">System-Only</span></span>            | <span data-ttu-id="1725a-266">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-266">False</span></span>                             |
| <span data-ttu-id="1725a-267">É de valor único</span><span class="sxs-lookup"><span data-stu-id="1725a-267">Is-Single-Valued</span></span>       | <span data-ttu-id="1725a-268">True</span><span class="sxs-lookup"><span data-stu-id="1725a-268">True</span></span>                              |
| <span data-ttu-id="1725a-269">É indexado</span><span class="sxs-lookup"><span data-stu-id="1725a-269">Is Indexed</span></span>             | <span data-ttu-id="1725a-270">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-270">False</span></span>                             |
| <span data-ttu-id="1725a-271">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="1725a-271">In Global Catalog</span></span>      | <span data-ttu-id="1725a-272">Falso</span><span class="sxs-lookup"><span data-stu-id="1725a-272">False</span></span>                             |
| <span data-ttu-id="1725a-273">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="1725a-273">NT-Security-Descriptor</span></span> | <span data-ttu-id="1725a-274">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="1725a-274">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="1725a-275">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="1725a-275">Range-Lower</span></span>            | <span data-ttu-id="1725a-276">0</span><span class="sxs-lookup"><span data-stu-id="1725a-276">0</span></span>                                 |
| <span data-ttu-id="1725a-277">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="1725a-277">Range-Upper</span></span>            | <span data-ttu-id="1725a-278">1024</span><span class="sxs-lookup"><span data-stu-id="1725a-278">1024</span></span>                              |
| <span data-ttu-id="1725a-279">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="1725a-279">Search-Flags</span></span>           | <span data-ttu-id="1725a-280">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1725a-280">0x00000010</span></span>                        |
| <span data-ttu-id="1725a-281">System-Flags</span><span class="sxs-lookup"><span data-stu-id="1725a-281">System-Flags</span></span>           | <span data-ttu-id="1725a-282">0x00000010</span><span class="sxs-lookup"><span data-stu-id="1725a-282">0x00000010</span></span>                        |
| <span data-ttu-id="1725a-283">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="1725a-283">Classes used in</span></span>        | [<span data-ttu-id="1725a-284">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="1725a-284">**User**</span></span>](c-user.md)<br/> |



 

 





