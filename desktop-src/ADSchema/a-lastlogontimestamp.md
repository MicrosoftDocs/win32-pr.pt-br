---
title: Atributo Last-login-timestamp
description: Esta é a hora em que o usuário fez o último logon no domínio.
ms.assetid: 6c94bccb-1e0a-421c-a00c-5f6e6389690f
ms.tgt_platform: multiple
keywords:
- Atributo do AD do último logon-carimbo de data/hora
- Esquema de AD do atributo lastLogonTimestamp
topic_type:
- apiref
api_name:
- Last-Logon-Timestamp
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6d7668891d008e1b16b7dc148462498e9210b4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104086742"
---
# <a name="last-logon-timestamp-attribute"></a><span data-ttu-id="72658-105">Atributo Last-login-timestamp</span><span class="sxs-lookup"><span data-stu-id="72658-105">Last-Logon-Timestamp attribute</span></span>

<span data-ttu-id="72658-106">Esta é a hora em que o usuário fez o último logon no domínio.</span><span class="sxs-lookup"><span data-stu-id="72658-106">This is the time that the user last logged into the domain.</span></span> <span data-ttu-id="72658-107">Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="72658-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="72658-108">Sempre que um usuário faz logon, o valor desse atributo é lido no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="72658-108">Whenever a user logs on, the value of this attribute is read from the DC.</span></span> <span data-ttu-id="72658-109">Se o valor for mais antigo \[ `current_time - msDS-LogonTimeSyncInterval` \] , o valor será atualizado.</span><span class="sxs-lookup"><span data-stu-id="72658-109">If the value is older \[ `current_time - msDS-LogonTimeSyncInterval` \], the value is updated.</span></span> <span data-ttu-id="72658-110">A atualização inicial após o aumento do nível funcional do domínio é calculada como 14 dias menos o percentual aleatório de 5 dias.</span><span class="sxs-lookup"><span data-stu-id="72658-110">The initial update after the raise of the domain functional level is calculated as 14 days minus random percentage of 5 days.</span></span>



| <span data-ttu-id="72658-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="72658-111">Entry</span></span> | <span data-ttu-id="72658-112">Valor</span><span class="sxs-lookup"><span data-stu-id="72658-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72658-113">CN</span><span class="sxs-lookup"><span data-stu-id="72658-113">CN</span></span>                | <span data-ttu-id="72658-114">Último logon-carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="72658-114">Last-Logon-Timestamp</span></span>                                                                                                   |
| <span data-ttu-id="72658-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="72658-115">Ldap-Display-Name</span></span> | <span data-ttu-id="72658-116">lastLogonTimestamp</span><span class="sxs-lookup"><span data-stu-id="72658-116">lastLogonTimestamp</span></span>                                                                                                     |
| <span data-ttu-id="72658-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="72658-117">Size</span></span>              | \-                                                                                                                     |
| <span data-ttu-id="72658-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="72658-118">Update Privilege</span></span>  | <span data-ttu-id="72658-119">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="72658-119">This value is set by the system.</span></span>                                                                                       |
| <span data-ttu-id="72658-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="72658-120">Update Frequency</span></span>  | <span data-ttu-id="72658-121">Quando o usuário fizer logon, e se esse valor for mais antigo que a hora atual menos o valor de msDS-LogonTimeSyncInterval.</span><span class="sxs-lookup"><span data-stu-id="72658-121">When the user logs on, and if this value is older than the current time minus the value of msDS-LogonTimeSyncInterval.</span></span> |
| <span data-ttu-id="72658-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="72658-122">Attribute-Id</span></span>      | <span data-ttu-id="72658-123">1.2.840.113556.1.4.1696</span><span class="sxs-lookup"><span data-stu-id="72658-123">1.2.840.113556.1.4.1696</span></span>                                                                                                |
| <span data-ttu-id="72658-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="72658-124">System-Id-Guid</span></span>    | <span data-ttu-id="72658-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span><span class="sxs-lookup"><span data-stu-id="72658-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span></span>                                                                                   |
| <span data-ttu-id="72658-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="72658-126">Syntax</span></span>            | [<span data-ttu-id="72658-127">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="72658-127">**Interval**</span></span>](s-interval.md)                                                                                         |



## <a name="implementations"></a><span data-ttu-id="72658-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="72658-128">Implementations</span></span>

-   [<span data-ttu-id="72658-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="72658-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="72658-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="72658-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="72658-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="72658-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="72658-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="72658-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="72658-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="72658-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="72658-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="72658-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="72658-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72658-135">Windows Server 2003</span></span>



| <span data-ttu-id="72658-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="72658-136">Entry</span></span> | <span data-ttu-id="72658-137">Valor</span><span class="sxs-lookup"><span data-stu-id="72658-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72658-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="72658-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72658-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72658-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72658-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="72658-140">System-Only</span></span>            | <span data-ttu-id="72658-141">Falso</span><span class="sxs-lookup"><span data-stu-id="72658-141">False</span></span>                             |
| <span data-ttu-id="72658-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72658-142">Is-Single-Valued</span></span>       | <span data-ttu-id="72658-143">True</span><span class="sxs-lookup"><span data-stu-id="72658-143">True</span></span>                              |
| <span data-ttu-id="72658-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="72658-144">Is Indexed</span></span>             | <span data-ttu-id="72658-145">Falso</span><span class="sxs-lookup"><span data-stu-id="72658-145">False</span></span>                             |
| <span data-ttu-id="72658-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72658-146">In Global Catalog</span></span>      | <span data-ttu-id="72658-147">Falso</span><span class="sxs-lookup"><span data-stu-id="72658-147">False</span></span>                             |
| <span data-ttu-id="72658-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72658-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="72658-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72658-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72658-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72658-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72658-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72658-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72658-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72658-152">Search-Flags</span></span>           | <span data-ttu-id="72658-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72658-153">0x00000000</span></span>                        |
| <span data-ttu-id="72658-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72658-154">System-Flags</span></span>           | <span data-ttu-id="72658-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72658-155">0x00000010</span></span>                        |
| <span data-ttu-id="72658-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72658-156">Classes used in</span></span>        | [<span data-ttu-id="72658-157">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="72658-157">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="72658-158">ADAM</span><span class="sxs-lookup"><span data-stu-id="72658-158">ADAM</span></span>



| <span data-ttu-id="72658-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="72658-159">Entry</span></span> | <span data-ttu-id="72658-160">Valor</span><span class="sxs-lookup"><span data-stu-id="72658-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="72658-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="72658-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="72658-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72658-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="72658-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="72658-163">System-Only</span></span>            | <span data-ttu-id="72658-164">True</span><span class="sxs-lookup"><span data-stu-id="72658-164">True</span></span>                                                              |
| <span data-ttu-id="72658-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72658-165">Is-Single-Valued</span></span>       | <span data-ttu-id="72658-166">True</span><span class="sxs-lookup"><span data-stu-id="72658-166">True</span></span>                                                              |
| <span data-ttu-id="72658-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="72658-167">Is Indexed</span></span>             | <span data-ttu-id="72658-168">Falso</span><span class="sxs-lookup"><span data-stu-id="72658-168">False</span></span>                                                             |
| <span data-ttu-id="72658-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72658-169">In Global Catalog</span></span>      | <span data-ttu-id="72658-170">Falso</span><span class="sxs-lookup"><span data-stu-id="72658-170">False</span></span>                                                             |
| <span data-ttu-id="72658-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72658-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="72658-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72658-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="72658-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72658-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="72658-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72658-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="72658-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72658-175">Search-Flags</span></span>           | <span data-ttu-id="72658-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72658-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="72658-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72658-177">System-Flags</span></span>           | <span data-ttu-id="72658-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72658-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="72658-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72658-179">Classes used in</span></span>        | [<span data-ttu-id="72658-180">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="72658-180">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="72658-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="72658-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="72658-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="72658-182">Entry</span></span> | <span data-ttu-id="72658-183">Valor</span><span class="sxs-lookup"><span data-stu-id="72658-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72658-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="72658-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72658-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72658-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72658-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="72658-186">System-Only</span></span>            | <span data-ttu-id="72658-187">Falso</span><span class="sxs-lookup"><span data-stu-id="72658-187">False</span></span>                             |
| <span data-ttu-id="72658-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72658-188">Is-Single-Valued</span></span>       | <span data-ttu-id="72658-189">True</span><span class="sxs-lookup"><span data-stu-id="72658-189">True</span></span>                              |
| <span data-ttu-id="72658-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="72658-190">Is Indexed</span></span>             | <span data-ttu-id="72658-191">Falso</span><span class="sxs-lookup"><span data-stu-id="72658-191">False</span></span>                             |
| <span data-ttu-id="72658-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72658-192">In Global Catalog</span></span>      | <span data-ttu-id="72658-193">Falso</span><span class="sxs-lookup"><span data-stu-id="72658-193">False</span></span>                             |
| <span data-ttu-id="72658-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72658-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="72658-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72658-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72658-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72658-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72658-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72658-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72658-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72658-198">Search-Flags</span></span>           | <span data-ttu-id="72658-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="72658-199">0x00000000</span></span>                        |
| <span data-ttu-id="72658-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72658-200">System-Flags</span></span>           | <span data-ttu-id="72658-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72658-201">0x00000010</span></span>                        |
| <span data-ttu-id="72658-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72658-202">Classes used in</span></span>        | [<span data-ttu-id="72658-203">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="72658-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="72658-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72658-204">Windows Server 2008</span></span>



| <span data-ttu-id="72658-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="72658-205">Entry</span></span> | <span data-ttu-id="72658-206">Valor</span><span class="sxs-lookup"><span data-stu-id="72658-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72658-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="72658-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72658-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72658-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72658-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="72658-209">System-Only</span></span>            | <span data-ttu-id="72658-210">Falso</span><span class="sxs-lookup"><span data-stu-id="72658-210">False</span></span>                             |
| <span data-ttu-id="72658-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72658-211">Is-Single-Valued</span></span>       | <span data-ttu-id="72658-212">True</span><span class="sxs-lookup"><span data-stu-id="72658-212">True</span></span>                              |
| <span data-ttu-id="72658-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="72658-213">Is Indexed</span></span>             | <span data-ttu-id="72658-214">True</span><span class="sxs-lookup"><span data-stu-id="72658-214">True</span></span>                              |
| <span data-ttu-id="72658-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72658-215">In Global Catalog</span></span>      | <span data-ttu-id="72658-216">True</span><span class="sxs-lookup"><span data-stu-id="72658-216">True</span></span>                              |
| <span data-ttu-id="72658-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72658-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="72658-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72658-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72658-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72658-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72658-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72658-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72658-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72658-221">Search-Flags</span></span>           | <span data-ttu-id="72658-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72658-222">0x00000001</span></span>                        |
| <span data-ttu-id="72658-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72658-223">System-Flags</span></span>           | <span data-ttu-id="72658-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72658-224">0x00000010</span></span>                        |
| <span data-ttu-id="72658-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72658-225">Classes used in</span></span>        | [<span data-ttu-id="72658-226">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="72658-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="72658-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="72658-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="72658-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="72658-228">Entry</span></span> | <span data-ttu-id="72658-229">Valor</span><span class="sxs-lookup"><span data-stu-id="72658-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72658-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="72658-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72658-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72658-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72658-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="72658-232">System-Only</span></span>            | <span data-ttu-id="72658-233">Falso</span><span class="sxs-lookup"><span data-stu-id="72658-233">False</span></span>                             |
| <span data-ttu-id="72658-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72658-234">Is-Single-Valued</span></span>       | <span data-ttu-id="72658-235">True</span><span class="sxs-lookup"><span data-stu-id="72658-235">True</span></span>                              |
| <span data-ttu-id="72658-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="72658-236">Is Indexed</span></span>             | <span data-ttu-id="72658-237">True</span><span class="sxs-lookup"><span data-stu-id="72658-237">True</span></span>                              |
| <span data-ttu-id="72658-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72658-238">In Global Catalog</span></span>      | <span data-ttu-id="72658-239">True</span><span class="sxs-lookup"><span data-stu-id="72658-239">True</span></span>                              |
| <span data-ttu-id="72658-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72658-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="72658-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72658-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72658-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72658-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72658-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72658-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72658-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72658-244">Search-Flags</span></span>           | <span data-ttu-id="72658-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72658-245">0x00000001</span></span>                        |
| <span data-ttu-id="72658-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72658-246">System-Flags</span></span>           | <span data-ttu-id="72658-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72658-247">0x00000010</span></span>                        |
| <span data-ttu-id="72658-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72658-248">Classes used in</span></span>        | [<span data-ttu-id="72658-249">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="72658-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="72658-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72658-250">Windows Server 2012</span></span>



| <span data-ttu-id="72658-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="72658-251">Entry</span></span> | <span data-ttu-id="72658-252">Valor</span><span class="sxs-lookup"><span data-stu-id="72658-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="72658-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="72658-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="72658-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="72658-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="72658-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="72658-255">System-Only</span></span>            | <span data-ttu-id="72658-256">Falso</span><span class="sxs-lookup"><span data-stu-id="72658-256">False</span></span>                             |
| <span data-ttu-id="72658-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="72658-257">Is-Single-Valued</span></span>       | <span data-ttu-id="72658-258">True</span><span class="sxs-lookup"><span data-stu-id="72658-258">True</span></span>                              |
| <span data-ttu-id="72658-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="72658-259">Is Indexed</span></span>             | <span data-ttu-id="72658-260">True</span><span class="sxs-lookup"><span data-stu-id="72658-260">True</span></span>                              |
| <span data-ttu-id="72658-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="72658-261">In Global Catalog</span></span>      | <span data-ttu-id="72658-262">True</span><span class="sxs-lookup"><span data-stu-id="72658-262">True</span></span>                              |
| <span data-ttu-id="72658-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="72658-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="72658-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="72658-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="72658-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="72658-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="72658-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="72658-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="72658-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="72658-267">Search-Flags</span></span>           | <span data-ttu-id="72658-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="72658-268">0x00000001</span></span>                        |
| <span data-ttu-id="72658-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="72658-269">System-Flags</span></span>           | <span data-ttu-id="72658-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="72658-270">0x00000010</span></span>                        |
| <span data-ttu-id="72658-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="72658-271">Classes used in</span></span>        | [<span data-ttu-id="72658-272">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="72658-272">**User**</span></span>](c-user.md)<br/> |



 

 





