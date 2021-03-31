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
# <a name="last-logon-timestamp-attribute"></a><span data-ttu-id="db587-105">Atributo Last-login-timestamp</span><span class="sxs-lookup"><span data-stu-id="db587-105">Last-Logon-Timestamp attribute</span></span>

<span data-ttu-id="db587-106">Esta é a hora em que o usuário fez o último logon no domínio.</span><span class="sxs-lookup"><span data-stu-id="db587-106">This is the time that the user last logged into the domain.</span></span> <span data-ttu-id="db587-107">Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="db587-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="db587-108">Sempre que um usuário faz logon, o valor desse atributo é lido no controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="db587-108">Whenever a user logs on, the value of this attribute is read from the DC.</span></span> <span data-ttu-id="db587-109">Se o valor for mais antigo \[ `current_time - msDS-LogonTimeSyncInterval` \] , o valor será atualizado.</span><span class="sxs-lookup"><span data-stu-id="db587-109">If the value is older \[ `current_time - msDS-LogonTimeSyncInterval` \], the value is updated.</span></span> <span data-ttu-id="db587-110">A atualização inicial após o aumento do nível funcional do domínio é calculada como 14 dias menos o percentual aleatório de 5 dias.</span><span class="sxs-lookup"><span data-stu-id="db587-110">The initial update after the raise of the domain functional level is calculated as 14 days minus random percentage of 5 days.</span></span>



| <span data-ttu-id="db587-111">Entrada</span><span class="sxs-lookup"><span data-stu-id="db587-111">Entry</span></span> | <span data-ttu-id="db587-112">Valor</span><span class="sxs-lookup"><span data-stu-id="db587-112">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db587-113">CN</span><span class="sxs-lookup"><span data-stu-id="db587-113">CN</span></span>                | <span data-ttu-id="db587-114">Último logon-carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="db587-114">Last-Logon-Timestamp</span></span>                                                                                                   |
| <span data-ttu-id="db587-115">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="db587-115">Ldap-Display-Name</span></span> | <span data-ttu-id="db587-116">lastLogonTimestamp</span><span class="sxs-lookup"><span data-stu-id="db587-116">lastLogonTimestamp</span></span>                                                                                                     |
| <span data-ttu-id="db587-117">Tamanho</span><span class="sxs-lookup"><span data-stu-id="db587-117">Size</span></span>              | \-                                                                                                                     |
| <span data-ttu-id="db587-118">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="db587-118">Update Privilege</span></span>  | <span data-ttu-id="db587-119">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="db587-119">This value is set by the system.</span></span>                                                                                       |
| <span data-ttu-id="db587-120">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="db587-120">Update Frequency</span></span>  | <span data-ttu-id="db587-121">Quando o usuário fizer logon, e se esse valor for mais antigo que a hora atual menos o valor de msDS-LogonTimeSyncInterval.</span><span class="sxs-lookup"><span data-stu-id="db587-121">When the user logs on, and if this value is older than the current time minus the value of msDS-LogonTimeSyncInterval.</span></span> |
| <span data-ttu-id="db587-122">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="db587-122">Attribute-Id</span></span>      | <span data-ttu-id="db587-123">1.2.840.113556.1.4.1696</span><span class="sxs-lookup"><span data-stu-id="db587-123">1.2.840.113556.1.4.1696</span></span>                                                                                                |
| <span data-ttu-id="db587-124">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="db587-124">System-Id-Guid</span></span>    | <span data-ttu-id="db587-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span><span class="sxs-lookup"><span data-stu-id="db587-125">c0e20a04-0e5a-4ff3-9482-5efeaecd7060</span></span>                                                                                   |
| <span data-ttu-id="db587-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="db587-126">Syntax</span></span>            | [<span data-ttu-id="db587-127">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="db587-127">**Interval**</span></span>](s-interval.md)                                                                                         |



## <a name="implementations"></a><span data-ttu-id="db587-128">Implementações</span><span class="sxs-lookup"><span data-stu-id="db587-128">Implementations</span></span>

-   [<span data-ttu-id="db587-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="db587-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="db587-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="db587-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="db587-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="db587-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="db587-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="db587-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="db587-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="db587-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="db587-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="db587-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-server-2003"></a><span data-ttu-id="db587-135">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="db587-135">Windows Server 2003</span></span>



| <span data-ttu-id="db587-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="db587-136">Entry</span></span> | <span data-ttu-id="db587-137">Valor</span><span class="sxs-lookup"><span data-stu-id="db587-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="db587-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="db587-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="db587-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db587-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="db587-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="db587-140">System-Only</span></span>            | <span data-ttu-id="db587-141">Falso</span><span class="sxs-lookup"><span data-stu-id="db587-141">False</span></span>                             |
| <span data-ttu-id="db587-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="db587-142">Is-Single-Valued</span></span>       | <span data-ttu-id="db587-143">True</span><span class="sxs-lookup"><span data-stu-id="db587-143">True</span></span>                              |
| <span data-ttu-id="db587-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="db587-144">Is Indexed</span></span>             | <span data-ttu-id="db587-145">Falso</span><span class="sxs-lookup"><span data-stu-id="db587-145">False</span></span>                             |
| <span data-ttu-id="db587-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="db587-146">In Global Catalog</span></span>      | <span data-ttu-id="db587-147">Falso</span><span class="sxs-lookup"><span data-stu-id="db587-147">False</span></span>                             |
| <span data-ttu-id="db587-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db587-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="db587-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="db587-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="db587-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db587-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="db587-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db587-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="db587-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db587-152">Search-Flags</span></span>           | <span data-ttu-id="db587-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db587-153">0x00000000</span></span>                        |
| <span data-ttu-id="db587-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db587-154">System-Flags</span></span>           | <span data-ttu-id="db587-155">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db587-155">0x00000010</span></span>                        |
| <span data-ttu-id="db587-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="db587-156">Classes used in</span></span>        | [<span data-ttu-id="db587-157">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="db587-157">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="db587-158">ADAM</span><span class="sxs-lookup"><span data-stu-id="db587-158">ADAM</span></span>



| <span data-ttu-id="db587-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="db587-159">Entry</span></span> | <span data-ttu-id="db587-160">Valor</span><span class="sxs-lookup"><span data-stu-id="db587-160">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="db587-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="db587-161">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="db587-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db587-162">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="db587-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="db587-163">System-Only</span></span>            | <span data-ttu-id="db587-164">True</span><span class="sxs-lookup"><span data-stu-id="db587-164">True</span></span>                                                              |
| <span data-ttu-id="db587-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="db587-165">Is-Single-Valued</span></span>       | <span data-ttu-id="db587-166">True</span><span class="sxs-lookup"><span data-stu-id="db587-166">True</span></span>                                                              |
| <span data-ttu-id="db587-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="db587-167">Is Indexed</span></span>             | <span data-ttu-id="db587-168">Falso</span><span class="sxs-lookup"><span data-stu-id="db587-168">False</span></span>                                                             |
| <span data-ttu-id="db587-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="db587-169">In Global Catalog</span></span>      | <span data-ttu-id="db587-170">Falso</span><span class="sxs-lookup"><span data-stu-id="db587-170">False</span></span>                                                             |
| <span data-ttu-id="db587-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db587-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="db587-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="db587-172">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="db587-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db587-173">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="db587-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db587-174">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="db587-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db587-175">Search-Flags</span></span>           | <span data-ttu-id="db587-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db587-176">0x00000000</span></span>                                                        |
| <span data-ttu-id="db587-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db587-177">System-Flags</span></span>           | <span data-ttu-id="db587-178">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db587-178">0x00000010</span></span>                                                        |
| <span data-ttu-id="db587-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="db587-179">Classes used in</span></span>        | [<span data-ttu-id="db587-180">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="db587-180">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="db587-181">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="db587-181">Windows Server 2003 R2</span></span>



| <span data-ttu-id="db587-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="db587-182">Entry</span></span> | <span data-ttu-id="db587-183">Valor</span><span class="sxs-lookup"><span data-stu-id="db587-183">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="db587-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="db587-184">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="db587-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db587-185">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="db587-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="db587-186">System-Only</span></span>            | <span data-ttu-id="db587-187">Falso</span><span class="sxs-lookup"><span data-stu-id="db587-187">False</span></span>                             |
| <span data-ttu-id="db587-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="db587-188">Is-Single-Valued</span></span>       | <span data-ttu-id="db587-189">True</span><span class="sxs-lookup"><span data-stu-id="db587-189">True</span></span>                              |
| <span data-ttu-id="db587-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="db587-190">Is Indexed</span></span>             | <span data-ttu-id="db587-191">Falso</span><span class="sxs-lookup"><span data-stu-id="db587-191">False</span></span>                             |
| <span data-ttu-id="db587-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="db587-192">In Global Catalog</span></span>      | <span data-ttu-id="db587-193">Falso</span><span class="sxs-lookup"><span data-stu-id="db587-193">False</span></span>                             |
| <span data-ttu-id="db587-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db587-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="db587-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="db587-195">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="db587-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db587-196">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="db587-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db587-197">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="db587-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db587-198">Search-Flags</span></span>           | <span data-ttu-id="db587-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="db587-199">0x00000000</span></span>                        |
| <span data-ttu-id="db587-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db587-200">System-Flags</span></span>           | <span data-ttu-id="db587-201">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db587-201">0x00000010</span></span>                        |
| <span data-ttu-id="db587-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="db587-202">Classes used in</span></span>        | [<span data-ttu-id="db587-203">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="db587-203">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="db587-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db587-204">Windows Server 2008</span></span>



| <span data-ttu-id="db587-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="db587-205">Entry</span></span> | <span data-ttu-id="db587-206">Valor</span><span class="sxs-lookup"><span data-stu-id="db587-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="db587-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="db587-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="db587-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db587-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="db587-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="db587-209">System-Only</span></span>            | <span data-ttu-id="db587-210">Falso</span><span class="sxs-lookup"><span data-stu-id="db587-210">False</span></span>                             |
| <span data-ttu-id="db587-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="db587-211">Is-Single-Valued</span></span>       | <span data-ttu-id="db587-212">True</span><span class="sxs-lookup"><span data-stu-id="db587-212">True</span></span>                              |
| <span data-ttu-id="db587-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="db587-213">Is Indexed</span></span>             | <span data-ttu-id="db587-214">True</span><span class="sxs-lookup"><span data-stu-id="db587-214">True</span></span>                              |
| <span data-ttu-id="db587-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="db587-215">In Global Catalog</span></span>      | <span data-ttu-id="db587-216">True</span><span class="sxs-lookup"><span data-stu-id="db587-216">True</span></span>                              |
| <span data-ttu-id="db587-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db587-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="db587-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="db587-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="db587-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db587-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="db587-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db587-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="db587-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db587-221">Search-Flags</span></span>           | <span data-ttu-id="db587-222">0x00000001</span><span class="sxs-lookup"><span data-stu-id="db587-222">0x00000001</span></span>                        |
| <span data-ttu-id="db587-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db587-223">System-Flags</span></span>           | <span data-ttu-id="db587-224">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db587-224">0x00000010</span></span>                        |
| <span data-ttu-id="db587-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="db587-225">Classes used in</span></span>        | [<span data-ttu-id="db587-226">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="db587-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="db587-227">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="db587-227">Windows Server 2008 R2</span></span>



| <span data-ttu-id="db587-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="db587-228">Entry</span></span> | <span data-ttu-id="db587-229">Valor</span><span class="sxs-lookup"><span data-stu-id="db587-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="db587-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="db587-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="db587-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db587-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="db587-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="db587-232">System-Only</span></span>            | <span data-ttu-id="db587-233">Falso</span><span class="sxs-lookup"><span data-stu-id="db587-233">False</span></span>                             |
| <span data-ttu-id="db587-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="db587-234">Is-Single-Valued</span></span>       | <span data-ttu-id="db587-235">True</span><span class="sxs-lookup"><span data-stu-id="db587-235">True</span></span>                              |
| <span data-ttu-id="db587-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="db587-236">Is Indexed</span></span>             | <span data-ttu-id="db587-237">True</span><span class="sxs-lookup"><span data-stu-id="db587-237">True</span></span>                              |
| <span data-ttu-id="db587-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="db587-238">In Global Catalog</span></span>      | <span data-ttu-id="db587-239">True</span><span class="sxs-lookup"><span data-stu-id="db587-239">True</span></span>                              |
| <span data-ttu-id="db587-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db587-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="db587-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="db587-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="db587-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db587-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="db587-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db587-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="db587-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db587-244">Search-Flags</span></span>           | <span data-ttu-id="db587-245">0x00000001</span><span class="sxs-lookup"><span data-stu-id="db587-245">0x00000001</span></span>                        |
| <span data-ttu-id="db587-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db587-246">System-Flags</span></span>           | <span data-ttu-id="db587-247">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db587-247">0x00000010</span></span>                        |
| <span data-ttu-id="db587-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="db587-248">Classes used in</span></span>        | [<span data-ttu-id="db587-249">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="db587-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="db587-250">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="db587-250">Windows Server 2012</span></span>



| <span data-ttu-id="db587-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="db587-251">Entry</span></span> | <span data-ttu-id="db587-252">Valor</span><span class="sxs-lookup"><span data-stu-id="db587-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="db587-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="db587-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="db587-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="db587-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="db587-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="db587-255">System-Only</span></span>            | <span data-ttu-id="db587-256">Falso</span><span class="sxs-lookup"><span data-stu-id="db587-256">False</span></span>                             |
| <span data-ttu-id="db587-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="db587-257">Is-Single-Valued</span></span>       | <span data-ttu-id="db587-258">True</span><span class="sxs-lookup"><span data-stu-id="db587-258">True</span></span>                              |
| <span data-ttu-id="db587-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="db587-259">Is Indexed</span></span>             | <span data-ttu-id="db587-260">True</span><span class="sxs-lookup"><span data-stu-id="db587-260">True</span></span>                              |
| <span data-ttu-id="db587-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="db587-261">In Global Catalog</span></span>      | <span data-ttu-id="db587-262">True</span><span class="sxs-lookup"><span data-stu-id="db587-262">True</span></span>                              |
| <span data-ttu-id="db587-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="db587-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="db587-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="db587-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="db587-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="db587-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="db587-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="db587-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="db587-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="db587-267">Search-Flags</span></span>           | <span data-ttu-id="db587-268">0x00000001</span><span class="sxs-lookup"><span data-stu-id="db587-268">0x00000001</span></span>                        |
| <span data-ttu-id="db587-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="db587-269">System-Flags</span></span>           | <span data-ttu-id="db587-270">0x00000010</span><span class="sxs-lookup"><span data-stu-id="db587-270">0x00000010</span></span>                        |
| <span data-ttu-id="db587-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="db587-271">Classes used in</span></span>        | [<span data-ttu-id="db587-272">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="db587-272">**User**</span></span>](c-user.md)<br/> |



 

 





