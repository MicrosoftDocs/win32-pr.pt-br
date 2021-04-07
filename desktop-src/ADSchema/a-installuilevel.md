---
title: Instalar-atributo de nível de interface do usuário
description: Esse atributo contém informações para o tipo (nível) de instalação que é usado para a interface do usuário.
ms.assetid: 718e04c7-ea96-4519-b312-12534ffd66df
ms.tgt_platform: multiple
keywords:
- Install-esquema de atributos de atributo de nível de interface do usuário
- Esquema de AD do atributo installUiLevel
topic_type:
- apiref
api_name:
- Install-Ui-Level
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b93900bb401d1bdcd72f8881fb78026745c4e8f6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103919319"
---
# <a name="install-ui-level-attribute"></a><span data-ttu-id="c254b-105">Instalar-atributo de nível de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="c254b-105">Install-Ui-Level attribute</span></span>

<span data-ttu-id="c254b-106">Esse atributo contém informações para o tipo (nível) de instalação que é usado para a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c254b-106">This attribute contains information for the type (level) of installation that is used for the user interface.</span></span> <span data-ttu-id="c254b-107">Os níveis de instalação possíveis são os seguintes: 2 INSTALLUILEVEL \_ None (instalação silenciosa) 3 INSTALLUILEVEL \_ Basic (instalação simples com tratamento de erros) 4 INSTALLUILEVEL \_ reduzido (interface do usuário criada, caixas de diálogo de assistente suprimidas) 5 INSTALLUILEVEL \_ completo (IU criada com assistentes, progresso, erros)</span><span class="sxs-lookup"><span data-stu-id="c254b-107">Possible installation levels are as follows: 2 INSTALLUILEVEL\_NONE (silent installation) 3 INSTALLUILEVEL\_BASIC (simple installation with error handling) 4 INSTALLUILEVEL\_REDUCED (authored UI, wizard dialog boxes suppressed) 5 INSTALLUILEVEL\_FULL (authored UI with wizards, progress, errors)</span></span>



| <span data-ttu-id="c254b-108">Entrada</span><span class="sxs-lookup"><span data-stu-id="c254b-108">Entry</span></span> | <span data-ttu-id="c254b-109">Valor</span><span class="sxs-lookup"><span data-stu-id="c254b-109">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="c254b-110">CN</span><span class="sxs-lookup"><span data-stu-id="c254b-110">CN</span></span>                | <span data-ttu-id="c254b-111">Instalar-nível da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="c254b-111">Install-Ui-Level</span></span>                     |
| <span data-ttu-id="c254b-112">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="c254b-112">Ldap-Display-Name</span></span> | <span data-ttu-id="c254b-113">installUiLevel</span><span class="sxs-lookup"><span data-stu-id="c254b-113">installUiLevel</span></span>                       |
| <span data-ttu-id="c254b-114">Tamanho</span><span class="sxs-lookup"><span data-stu-id="c254b-114">Size</span></span>              | \-                                   |
| <span data-ttu-id="c254b-115">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="c254b-115">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="c254b-116">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="c254b-116">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="c254b-117">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="c254b-117">Attribute-Id</span></span>      | <span data-ttu-id="c254b-118">1.2.840.113556.1.4.847</span><span class="sxs-lookup"><span data-stu-id="c254b-118">1.2.840.113556.1.4.847</span></span>               |
| <span data-ttu-id="c254b-119">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="c254b-119">System-Id-Guid</span></span>    | <span data-ttu-id="c254b-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span><span class="sxs-lookup"><span data-stu-id="c254b-120">96a7dd64-9118-11d1-aebc-0000f80367c1</span></span> |
| <span data-ttu-id="c254b-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="c254b-121">Syntax</span></span>            | [<span data-ttu-id="c254b-122">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="c254b-122">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="c254b-123">Implementações</span><span class="sxs-lookup"><span data-stu-id="c254b-123">Implementations</span></span>

-   [<span data-ttu-id="c254b-124">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="c254b-124">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="c254b-125">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="c254b-125">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="c254b-126">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="c254b-126">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="c254b-127">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="c254b-127">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="c254b-128">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="c254b-128">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="c254b-129">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="c254b-129">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="c254b-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c254b-130">Windows 2000 Server</span></span>



| <span data-ttu-id="c254b-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="c254b-131">Entry</span></span> | <span data-ttu-id="c254b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c254b-132">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c254b-133">ID do link</span><span class="sxs-lookup"><span data-stu-id="c254b-133">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c254b-134">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c254b-134">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c254b-135">System-Only</span><span class="sxs-lookup"><span data-stu-id="c254b-135">System-Only</span></span>            | <span data-ttu-id="c254b-136">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-136">False</span></span>                                                            |
| <span data-ttu-id="c254b-137">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c254b-137">Is-Single-Valued</span></span>       | <span data-ttu-id="c254b-138">True</span><span class="sxs-lookup"><span data-stu-id="c254b-138">True</span></span>                                                             |
| <span data-ttu-id="c254b-139">É indexado</span><span class="sxs-lookup"><span data-stu-id="c254b-139">Is Indexed</span></span>             | <span data-ttu-id="c254b-140">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-140">False</span></span>                                                            |
| <span data-ttu-id="c254b-141">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c254b-141">In Global Catalog</span></span>      | <span data-ttu-id="c254b-142">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-142">False</span></span>                                                            |
| <span data-ttu-id="c254b-143">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c254b-143">NT-Security-Descriptor</span></span> | <span data-ttu-id="c254b-144">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c254b-144">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c254b-145">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c254b-145">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c254b-146">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c254b-146">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c254b-147">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c254b-147">Search-Flags</span></span>           | <span data-ttu-id="c254b-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c254b-148">0x00000000</span></span>                                                       |
| <span data-ttu-id="c254b-149">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c254b-149">System-Flags</span></span>           | <span data-ttu-id="c254b-150">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c254b-150">0x00000010</span></span>                                                       |
| <span data-ttu-id="c254b-151">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c254b-151">Classes used in</span></span>        | [<span data-ttu-id="c254b-152">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="c254b-152">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="c254b-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c254b-153">Windows Server 2003</span></span>



| <span data-ttu-id="c254b-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="c254b-154">Entry</span></span> | <span data-ttu-id="c254b-155">Valor</span><span class="sxs-lookup"><span data-stu-id="c254b-155">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c254b-156">ID do link</span><span class="sxs-lookup"><span data-stu-id="c254b-156">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c254b-157">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c254b-157">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c254b-158">System-Only</span><span class="sxs-lookup"><span data-stu-id="c254b-158">System-Only</span></span>            | <span data-ttu-id="c254b-159">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-159">False</span></span>                                                            |
| <span data-ttu-id="c254b-160">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c254b-160">Is-Single-Valued</span></span>       | <span data-ttu-id="c254b-161">True</span><span class="sxs-lookup"><span data-stu-id="c254b-161">True</span></span>                                                             |
| <span data-ttu-id="c254b-162">É indexado</span><span class="sxs-lookup"><span data-stu-id="c254b-162">Is Indexed</span></span>             | <span data-ttu-id="c254b-163">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-163">False</span></span>                                                            |
| <span data-ttu-id="c254b-164">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c254b-164">In Global Catalog</span></span>      | <span data-ttu-id="c254b-165">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-165">False</span></span>                                                            |
| <span data-ttu-id="c254b-166">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c254b-166">NT-Security-Descriptor</span></span> | <span data-ttu-id="c254b-167">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c254b-167">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c254b-168">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c254b-168">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c254b-169">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c254b-169">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c254b-170">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c254b-170">Search-Flags</span></span>           | <span data-ttu-id="c254b-171">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c254b-171">0x00000000</span></span>                                                       |
| <span data-ttu-id="c254b-172">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c254b-172">System-Flags</span></span>           | <span data-ttu-id="c254b-173">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c254b-173">0x00000010</span></span>                                                       |
| <span data-ttu-id="c254b-174">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c254b-174">Classes used in</span></span>        | [<span data-ttu-id="c254b-175">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="c254b-175">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="c254b-176">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="c254b-176">Windows Server 2003 R2</span></span>



| <span data-ttu-id="c254b-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="c254b-177">Entry</span></span> | <span data-ttu-id="c254b-178">Valor</span><span class="sxs-lookup"><span data-stu-id="c254b-178">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c254b-179">ID do link</span><span class="sxs-lookup"><span data-stu-id="c254b-179">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c254b-180">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c254b-180">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c254b-181">System-Only</span><span class="sxs-lookup"><span data-stu-id="c254b-181">System-Only</span></span>            | <span data-ttu-id="c254b-182">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-182">False</span></span>                                                            |
| <span data-ttu-id="c254b-183">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c254b-183">Is-Single-Valued</span></span>       | <span data-ttu-id="c254b-184">True</span><span class="sxs-lookup"><span data-stu-id="c254b-184">True</span></span>                                                             |
| <span data-ttu-id="c254b-185">É indexado</span><span class="sxs-lookup"><span data-stu-id="c254b-185">Is Indexed</span></span>             | <span data-ttu-id="c254b-186">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-186">False</span></span>                                                            |
| <span data-ttu-id="c254b-187">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c254b-187">In Global Catalog</span></span>      | <span data-ttu-id="c254b-188">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-188">False</span></span>                                                            |
| <span data-ttu-id="c254b-189">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c254b-189">NT-Security-Descriptor</span></span> | <span data-ttu-id="c254b-190">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c254b-190">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c254b-191">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c254b-191">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c254b-192">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c254b-192">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c254b-193">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c254b-193">Search-Flags</span></span>           | <span data-ttu-id="c254b-194">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c254b-194">0x00000000</span></span>                                                       |
| <span data-ttu-id="c254b-195">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c254b-195">System-Flags</span></span>           | <span data-ttu-id="c254b-196">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c254b-196">0x00000010</span></span>                                                       |
| <span data-ttu-id="c254b-197">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c254b-197">Classes used in</span></span>        | [<span data-ttu-id="c254b-198">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="c254b-198">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="c254b-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c254b-199">Windows Server 2008</span></span>



| <span data-ttu-id="c254b-200">Entrada</span><span class="sxs-lookup"><span data-stu-id="c254b-200">Entry</span></span> | <span data-ttu-id="c254b-201">Valor</span><span class="sxs-lookup"><span data-stu-id="c254b-201">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c254b-202">ID do link</span><span class="sxs-lookup"><span data-stu-id="c254b-202">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c254b-203">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c254b-203">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c254b-204">System-Only</span><span class="sxs-lookup"><span data-stu-id="c254b-204">System-Only</span></span>            | <span data-ttu-id="c254b-205">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-205">False</span></span>                                                            |
| <span data-ttu-id="c254b-206">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c254b-206">Is-Single-Valued</span></span>       | <span data-ttu-id="c254b-207">True</span><span class="sxs-lookup"><span data-stu-id="c254b-207">True</span></span>                                                             |
| <span data-ttu-id="c254b-208">É indexado</span><span class="sxs-lookup"><span data-stu-id="c254b-208">Is Indexed</span></span>             | <span data-ttu-id="c254b-209">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-209">False</span></span>                                                            |
| <span data-ttu-id="c254b-210">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c254b-210">In Global Catalog</span></span>      | <span data-ttu-id="c254b-211">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-211">False</span></span>                                                            |
| <span data-ttu-id="c254b-212">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c254b-212">NT-Security-Descriptor</span></span> | <span data-ttu-id="c254b-213">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c254b-213">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c254b-214">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c254b-214">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c254b-215">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c254b-215">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c254b-216">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c254b-216">Search-Flags</span></span>           | <span data-ttu-id="c254b-217">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c254b-217">0x00000000</span></span>                                                       |
| <span data-ttu-id="c254b-218">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c254b-218">System-Flags</span></span>           | <span data-ttu-id="c254b-219">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c254b-219">0x00000010</span></span>                                                       |
| <span data-ttu-id="c254b-220">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c254b-220">Classes used in</span></span>        | [<span data-ttu-id="c254b-221">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="c254b-221">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="c254b-222">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c254b-222">Windows Server 2008 R2</span></span>



| <span data-ttu-id="c254b-223">Entrada</span><span class="sxs-lookup"><span data-stu-id="c254b-223">Entry</span></span> | <span data-ttu-id="c254b-224">Valor</span><span class="sxs-lookup"><span data-stu-id="c254b-224">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c254b-225">ID do link</span><span class="sxs-lookup"><span data-stu-id="c254b-225">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c254b-226">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c254b-226">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c254b-227">System-Only</span><span class="sxs-lookup"><span data-stu-id="c254b-227">System-Only</span></span>            | <span data-ttu-id="c254b-228">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-228">False</span></span>                                                            |
| <span data-ttu-id="c254b-229">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c254b-229">Is-Single-Valued</span></span>       | <span data-ttu-id="c254b-230">True</span><span class="sxs-lookup"><span data-stu-id="c254b-230">True</span></span>                                                             |
| <span data-ttu-id="c254b-231">É indexado</span><span class="sxs-lookup"><span data-stu-id="c254b-231">Is Indexed</span></span>             | <span data-ttu-id="c254b-232">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-232">False</span></span>                                                            |
| <span data-ttu-id="c254b-233">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c254b-233">In Global Catalog</span></span>      | <span data-ttu-id="c254b-234">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-234">False</span></span>                                                            |
| <span data-ttu-id="c254b-235">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c254b-235">NT-Security-Descriptor</span></span> | <span data-ttu-id="c254b-236">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c254b-236">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c254b-237">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c254b-237">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c254b-238">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c254b-238">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c254b-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c254b-239">Search-Flags</span></span>           | <span data-ttu-id="c254b-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c254b-240">0x00000000</span></span>                                                       |
| <span data-ttu-id="c254b-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c254b-241">System-Flags</span></span>           | <span data-ttu-id="c254b-242">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c254b-242">0x00000010</span></span>                                                       |
| <span data-ttu-id="c254b-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c254b-243">Classes used in</span></span>        | [<span data-ttu-id="c254b-244">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="c254b-244">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="c254b-245">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c254b-245">Windows Server 2012</span></span>



| <span data-ttu-id="c254b-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="c254b-246">Entry</span></span> | <span data-ttu-id="c254b-247">Valor</span><span class="sxs-lookup"><span data-stu-id="c254b-247">Value</span></span> |
|------------------------|------------------------------------------------------------------|
| <span data-ttu-id="c254b-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="c254b-248">Link-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c254b-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="c254b-249">MAPI-Id</span></span>                | \-                                                               |
| <span data-ttu-id="c254b-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="c254b-250">System-Only</span></span>            | <span data-ttu-id="c254b-251">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-251">False</span></span>                                                            |
| <span data-ttu-id="c254b-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="c254b-252">Is-Single-Valued</span></span>       | <span data-ttu-id="c254b-253">True</span><span class="sxs-lookup"><span data-stu-id="c254b-253">True</span></span>                                                             |
| <span data-ttu-id="c254b-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="c254b-254">Is Indexed</span></span>             | <span data-ttu-id="c254b-255">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-255">False</span></span>                                                            |
| <span data-ttu-id="c254b-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="c254b-256">In Global Catalog</span></span>      | <span data-ttu-id="c254b-257">Falso</span><span class="sxs-lookup"><span data-stu-id="c254b-257">False</span></span>                                                            |
| <span data-ttu-id="c254b-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="c254b-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="c254b-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="c254b-259">O:BAG:BAD:S:</span></span>                                                     |
| <span data-ttu-id="c254b-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="c254b-260">Range-Lower</span></span>            | \-                                                               |
| <span data-ttu-id="c254b-261">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="c254b-261">Range-Upper</span></span>            | \-                                                               |
| <span data-ttu-id="c254b-262">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="c254b-262">Search-Flags</span></span>           | <span data-ttu-id="c254b-263">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c254b-263">0x00000000</span></span>                                                       |
| <span data-ttu-id="c254b-264">System-Flags</span><span class="sxs-lookup"><span data-stu-id="c254b-264">System-Flags</span></span>           | <span data-ttu-id="c254b-265">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c254b-265">0x00000010</span></span>                                                       |
| <span data-ttu-id="c254b-266">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="c254b-266">Classes used in</span></span>        | [<span data-ttu-id="c254b-267">**Registro de pacote**</span><span class="sxs-lookup"><span data-stu-id="c254b-267">**Package-Registration**</span></span>](c-packageregistration.md)<br/> |



 

 





