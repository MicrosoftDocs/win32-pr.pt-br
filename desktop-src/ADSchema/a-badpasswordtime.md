---
title: Atributo de tempo de senha inválido
description: A última data e hora em que uma tentativa de fazer logon nesta conta foi feita com uma senha que não é válida.
ms.assetid: 8e8c5b73-b42d-4a62-89af-c0ff2fe106d8
ms.tgt_platform: multiple
keywords:
- Atributo do AD de atributos de tempo de senha inválidos
- Esquema de AD do atributo badPasswordTime
topic_type:
- apiref
api_name:
- Bad-Password-Time
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47df09d0ff2d82a9180c43721aa09e5363884e24
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456311"
---
# <a name="bad-password-time-attribute"></a><span data-ttu-id="634eb-105">Atributo de tempo de senha inválido</span><span class="sxs-lookup"><span data-stu-id="634eb-105">Bad-Password-Time attribute</span></span>

<span data-ttu-id="634eb-106">A última data e hora em que uma tentativa de fazer logon nesta conta foi feita com uma senha que não é válida.</span><span class="sxs-lookup"><span data-stu-id="634eb-106">The last time and date that an attempt to log on to this account was made with a password that is not valid.</span></span> <span data-ttu-id="634eb-107">Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601 (UTC).</span><span class="sxs-lookup"><span data-stu-id="634eb-107">This value is stored as a large integer that represents the number of 100-nanosecond intervals since January 1, 1601 (UTC).</span></span> <span data-ttu-id="634eb-108">Um valor de zero significa que a última vez que uma senha incorreta foi usada é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="634eb-108">A value of zero means that the last time a incorrect password was used is unknown.</span></span>



| <span data-ttu-id="634eb-109">Entrada</span><span class="sxs-lookup"><span data-stu-id="634eb-109">Entry</span></span> | <span data-ttu-id="634eb-110">Valor</span><span class="sxs-lookup"><span data-stu-id="634eb-110">Value</span></span> |
|-------------------|-------------------------------------------|
| <span data-ttu-id="634eb-111">CN</span><span class="sxs-lookup"><span data-stu-id="634eb-111">CN</span></span>                | <span data-ttu-id="634eb-112">Má-hora-senha</span><span class="sxs-lookup"><span data-stu-id="634eb-112">Bad-Password-Time</span></span>                         |
| <span data-ttu-id="634eb-113">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="634eb-113">Ldap-Display-Name</span></span> | <span data-ttu-id="634eb-114">badPasswordTime</span><span class="sxs-lookup"><span data-stu-id="634eb-114">badPasswordTime</span></span>                           |
| <span data-ttu-id="634eb-115">Tamanho</span><span class="sxs-lookup"><span data-stu-id="634eb-115">Size</span></span>              | <span data-ttu-id="634eb-116">8 bytes</span><span class="sxs-lookup"><span data-stu-id="634eb-116">8 bytes</span></span>                                   |
| <span data-ttu-id="634eb-117">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="634eb-117">Update Privilege</span></span>  | <span data-ttu-id="634eb-118">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="634eb-118">This value is set by the system.</span></span>          |
| <span data-ttu-id="634eb-119">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="634eb-119">Update Frequency</span></span>  | <span data-ttu-id="634eb-120">Cada vez que o usuário insere uma senha inadequada.</span><span class="sxs-lookup"><span data-stu-id="634eb-120">Each time the user enters a bad password.</span></span> |
| <span data-ttu-id="634eb-121">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="634eb-121">Attribute-Id</span></span>      | <span data-ttu-id="634eb-122">1.2.840.113556.1.4.49</span><span class="sxs-lookup"><span data-stu-id="634eb-122">1.2.840.113556.1.4.49</span></span>                     |
| <span data-ttu-id="634eb-123">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="634eb-123">System-Id-Guid</span></span>    | <span data-ttu-id="634eb-124">bf96792d-0de6-11d0-a285-00aa003049e2</span><span class="sxs-lookup"><span data-stu-id="634eb-124">bf96792d-0de6-11d0-a285-00aa003049e2</span></span>      |
| <span data-ttu-id="634eb-125">Syntax</span><span class="sxs-lookup"><span data-stu-id="634eb-125">Syntax</span></span>            | [<span data-ttu-id="634eb-126">**Intervalo**</span><span class="sxs-lookup"><span data-stu-id="634eb-126">**Interval**</span></span>](s-interval.md)            |



## <a name="implementations"></a><span data-ttu-id="634eb-127">Implementações</span><span class="sxs-lookup"><span data-stu-id="634eb-127">Implementations</span></span>

-   [<span data-ttu-id="634eb-128">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="634eb-128">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="634eb-129">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="634eb-129">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="634eb-130">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="634eb-130">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="634eb-131">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="634eb-131">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="634eb-132">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="634eb-132">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="634eb-133">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="634eb-133">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="634eb-134">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="634eb-134">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="634eb-135">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="634eb-135">Windows 2000 Server</span></span>



| <span data-ttu-id="634eb-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="634eb-136">Entry</span></span> | <span data-ttu-id="634eb-137">Valor</span><span class="sxs-lookup"><span data-stu-id="634eb-137">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="634eb-138">ID do link</span><span class="sxs-lookup"><span data-stu-id="634eb-138">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="634eb-139">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="634eb-139">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="634eb-140">System-Only</span><span class="sxs-lookup"><span data-stu-id="634eb-140">System-Only</span></span>            | <span data-ttu-id="634eb-141">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-141">False</span></span>                             |
| <span data-ttu-id="634eb-142">É de valor único</span><span class="sxs-lookup"><span data-stu-id="634eb-142">Is-Single-Valued</span></span>       | <span data-ttu-id="634eb-143">True</span><span class="sxs-lookup"><span data-stu-id="634eb-143">True</span></span>                              |
| <span data-ttu-id="634eb-144">É indexado</span><span class="sxs-lookup"><span data-stu-id="634eb-144">Is Indexed</span></span>             | <span data-ttu-id="634eb-145">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-145">False</span></span>                             |
| <span data-ttu-id="634eb-146">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="634eb-146">In Global Catalog</span></span>      | <span data-ttu-id="634eb-147">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-147">False</span></span>                             |
| <span data-ttu-id="634eb-148">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="634eb-148">NT-Security-Descriptor</span></span> | <span data-ttu-id="634eb-149">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="634eb-149">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="634eb-150">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="634eb-150">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="634eb-151">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="634eb-151">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="634eb-152">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="634eb-152">Search-Flags</span></span>           | <span data-ttu-id="634eb-153">0x00000000</span><span class="sxs-lookup"><span data-stu-id="634eb-153">0x00000000</span></span>                        |
| <span data-ttu-id="634eb-154">System-Flags</span><span class="sxs-lookup"><span data-stu-id="634eb-154">System-Flags</span></span>           | <span data-ttu-id="634eb-155">0x00000011</span><span class="sxs-lookup"><span data-stu-id="634eb-155">0x00000011</span></span>                        |
| <span data-ttu-id="634eb-156">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="634eb-156">Classes used in</span></span>        | [<span data-ttu-id="634eb-157">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="634eb-157">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="634eb-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="634eb-158">Windows Server 2003</span></span>



| <span data-ttu-id="634eb-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="634eb-159">Entry</span></span> | <span data-ttu-id="634eb-160">Valor</span><span class="sxs-lookup"><span data-stu-id="634eb-160">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="634eb-161">ID do link</span><span class="sxs-lookup"><span data-stu-id="634eb-161">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="634eb-162">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="634eb-162">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="634eb-163">System-Only</span><span class="sxs-lookup"><span data-stu-id="634eb-163">System-Only</span></span>            | <span data-ttu-id="634eb-164">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-164">False</span></span>                             |
| <span data-ttu-id="634eb-165">É de valor único</span><span class="sxs-lookup"><span data-stu-id="634eb-165">Is-Single-Valued</span></span>       | <span data-ttu-id="634eb-166">True</span><span class="sxs-lookup"><span data-stu-id="634eb-166">True</span></span>                              |
| <span data-ttu-id="634eb-167">É indexado</span><span class="sxs-lookup"><span data-stu-id="634eb-167">Is Indexed</span></span>             | <span data-ttu-id="634eb-168">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-168">False</span></span>                             |
| <span data-ttu-id="634eb-169">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="634eb-169">In Global Catalog</span></span>      | <span data-ttu-id="634eb-170">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-170">False</span></span>                             |
| <span data-ttu-id="634eb-171">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="634eb-171">NT-Security-Descriptor</span></span> | <span data-ttu-id="634eb-172">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="634eb-172">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="634eb-173">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="634eb-173">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="634eb-174">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="634eb-174">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="634eb-175">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="634eb-175">Search-Flags</span></span>           | <span data-ttu-id="634eb-176">0x00000000</span><span class="sxs-lookup"><span data-stu-id="634eb-176">0x00000000</span></span>                        |
| <span data-ttu-id="634eb-177">System-Flags</span><span class="sxs-lookup"><span data-stu-id="634eb-177">System-Flags</span></span>           | <span data-ttu-id="634eb-178">0x00000011</span><span class="sxs-lookup"><span data-stu-id="634eb-178">0x00000011</span></span>                        |
| <span data-ttu-id="634eb-179">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="634eb-179">Classes used in</span></span>        | [<span data-ttu-id="634eb-180">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="634eb-180">**User**</span></span>](c-user.md)<br/> |



## <a name="adam"></a><span data-ttu-id="634eb-181">ADAM</span><span class="sxs-lookup"><span data-stu-id="634eb-181">ADAM</span></span>



| <span data-ttu-id="634eb-182">Entrada</span><span class="sxs-lookup"><span data-stu-id="634eb-182">Entry</span></span> | <span data-ttu-id="634eb-183">Valor</span><span class="sxs-lookup"><span data-stu-id="634eb-183">Value</span></span> |
|------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="634eb-184">ID do link</span><span class="sxs-lookup"><span data-stu-id="634eb-184">Link-Id</span></span>                | \-                                                                |
| <span data-ttu-id="634eb-185">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="634eb-185">MAPI-Id</span></span>                | \-                                                                |
| <span data-ttu-id="634eb-186">System-Only</span><span class="sxs-lookup"><span data-stu-id="634eb-186">System-Only</span></span>            | <span data-ttu-id="634eb-187">True</span><span class="sxs-lookup"><span data-stu-id="634eb-187">True</span></span>                                                              |
| <span data-ttu-id="634eb-188">É de valor único</span><span class="sxs-lookup"><span data-stu-id="634eb-188">Is-Single-Valued</span></span>       | <span data-ttu-id="634eb-189">True</span><span class="sxs-lookup"><span data-stu-id="634eb-189">True</span></span>                                                              |
| <span data-ttu-id="634eb-190">É indexado</span><span class="sxs-lookup"><span data-stu-id="634eb-190">Is Indexed</span></span>             | <span data-ttu-id="634eb-191">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-191">False</span></span>                                                             |
| <span data-ttu-id="634eb-192">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="634eb-192">In Global Catalog</span></span>      | <span data-ttu-id="634eb-193">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-193">False</span></span>                                                             |
| <span data-ttu-id="634eb-194">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="634eb-194">NT-Security-Descriptor</span></span> | <span data-ttu-id="634eb-195">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="634eb-195">O:BAG:BAD:S:</span></span>                                                      |
| <span data-ttu-id="634eb-196">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="634eb-196">Range-Lower</span></span>            | \-                                                                |
| <span data-ttu-id="634eb-197">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="634eb-197">Range-Upper</span></span>            | \-                                                                |
| <span data-ttu-id="634eb-198">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="634eb-198">Search-Flags</span></span>           | <span data-ttu-id="634eb-199">0x00000000</span><span class="sxs-lookup"><span data-stu-id="634eb-199">0x00000000</span></span>                                                        |
| <span data-ttu-id="634eb-200">System-Flags</span><span class="sxs-lookup"><span data-stu-id="634eb-200">System-Flags</span></span>           | <span data-ttu-id="634eb-201">0x00000011</span><span class="sxs-lookup"><span data-stu-id="634eb-201">0x00000011</span></span>                                                        |
| <span data-ttu-id="634eb-202">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="634eb-202">Classes used in</span></span>        | [<span data-ttu-id="634eb-203">**ms-DS-Vinculed-Object**</span><span class="sxs-lookup"><span data-stu-id="634eb-203">**ms-DS-Bindable-Object**</span></span>](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="634eb-204">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="634eb-204">Windows Server 2003 R2</span></span>



| <span data-ttu-id="634eb-205">Entrada</span><span class="sxs-lookup"><span data-stu-id="634eb-205">Entry</span></span> | <span data-ttu-id="634eb-206">Valor</span><span class="sxs-lookup"><span data-stu-id="634eb-206">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="634eb-207">ID do link</span><span class="sxs-lookup"><span data-stu-id="634eb-207">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="634eb-208">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="634eb-208">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="634eb-209">System-Only</span><span class="sxs-lookup"><span data-stu-id="634eb-209">System-Only</span></span>            | <span data-ttu-id="634eb-210">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-210">False</span></span>                             |
| <span data-ttu-id="634eb-211">É de valor único</span><span class="sxs-lookup"><span data-stu-id="634eb-211">Is-Single-Valued</span></span>       | <span data-ttu-id="634eb-212">True</span><span class="sxs-lookup"><span data-stu-id="634eb-212">True</span></span>                              |
| <span data-ttu-id="634eb-213">É indexado</span><span class="sxs-lookup"><span data-stu-id="634eb-213">Is Indexed</span></span>             | <span data-ttu-id="634eb-214">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-214">False</span></span>                             |
| <span data-ttu-id="634eb-215">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="634eb-215">In Global Catalog</span></span>      | <span data-ttu-id="634eb-216">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-216">False</span></span>                             |
| <span data-ttu-id="634eb-217">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="634eb-217">NT-Security-Descriptor</span></span> | <span data-ttu-id="634eb-218">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="634eb-218">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="634eb-219">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="634eb-219">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="634eb-220">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="634eb-220">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="634eb-221">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="634eb-221">Search-Flags</span></span>           | <span data-ttu-id="634eb-222">0x00000000</span><span class="sxs-lookup"><span data-stu-id="634eb-222">0x00000000</span></span>                        |
| <span data-ttu-id="634eb-223">System-Flags</span><span class="sxs-lookup"><span data-stu-id="634eb-223">System-Flags</span></span>           | <span data-ttu-id="634eb-224">0x00000011</span><span class="sxs-lookup"><span data-stu-id="634eb-224">0x00000011</span></span>                        |
| <span data-ttu-id="634eb-225">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="634eb-225">Classes used in</span></span>        | [<span data-ttu-id="634eb-226">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="634eb-226">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="634eb-227">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="634eb-227">Windows Server 2008</span></span>



| <span data-ttu-id="634eb-228">Entrada</span><span class="sxs-lookup"><span data-stu-id="634eb-228">Entry</span></span> | <span data-ttu-id="634eb-229">Valor</span><span class="sxs-lookup"><span data-stu-id="634eb-229">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="634eb-230">ID do link</span><span class="sxs-lookup"><span data-stu-id="634eb-230">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="634eb-231">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="634eb-231">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="634eb-232">System-Only</span><span class="sxs-lookup"><span data-stu-id="634eb-232">System-Only</span></span>            | <span data-ttu-id="634eb-233">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-233">False</span></span>                             |
| <span data-ttu-id="634eb-234">É de valor único</span><span class="sxs-lookup"><span data-stu-id="634eb-234">Is-Single-Valued</span></span>       | <span data-ttu-id="634eb-235">True</span><span class="sxs-lookup"><span data-stu-id="634eb-235">True</span></span>                              |
| <span data-ttu-id="634eb-236">É indexado</span><span class="sxs-lookup"><span data-stu-id="634eb-236">Is Indexed</span></span>             | <span data-ttu-id="634eb-237">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-237">False</span></span>                             |
| <span data-ttu-id="634eb-238">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="634eb-238">In Global Catalog</span></span>      | <span data-ttu-id="634eb-239">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-239">False</span></span>                             |
| <span data-ttu-id="634eb-240">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="634eb-240">NT-Security-Descriptor</span></span> | <span data-ttu-id="634eb-241">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="634eb-241">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="634eb-242">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="634eb-242">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="634eb-243">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="634eb-243">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="634eb-244">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="634eb-244">Search-Flags</span></span>           | <span data-ttu-id="634eb-245">0x00000000</span><span class="sxs-lookup"><span data-stu-id="634eb-245">0x00000000</span></span>                        |
| <span data-ttu-id="634eb-246">System-Flags</span><span class="sxs-lookup"><span data-stu-id="634eb-246">System-Flags</span></span>           | <span data-ttu-id="634eb-247">0x00000011</span><span class="sxs-lookup"><span data-stu-id="634eb-247">0x00000011</span></span>                        |
| <span data-ttu-id="634eb-248">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="634eb-248">Classes used in</span></span>        | [<span data-ttu-id="634eb-249">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="634eb-249">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="634eb-250">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="634eb-250">Windows Server 2008 R2</span></span>



| <span data-ttu-id="634eb-251">Entrada</span><span class="sxs-lookup"><span data-stu-id="634eb-251">Entry</span></span> | <span data-ttu-id="634eb-252">Valor</span><span class="sxs-lookup"><span data-stu-id="634eb-252">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="634eb-253">ID do link</span><span class="sxs-lookup"><span data-stu-id="634eb-253">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="634eb-254">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="634eb-254">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="634eb-255">System-Only</span><span class="sxs-lookup"><span data-stu-id="634eb-255">System-Only</span></span>            | <span data-ttu-id="634eb-256">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-256">False</span></span>                             |
| <span data-ttu-id="634eb-257">É de valor único</span><span class="sxs-lookup"><span data-stu-id="634eb-257">Is-Single-Valued</span></span>       | <span data-ttu-id="634eb-258">True</span><span class="sxs-lookup"><span data-stu-id="634eb-258">True</span></span>                              |
| <span data-ttu-id="634eb-259">É indexado</span><span class="sxs-lookup"><span data-stu-id="634eb-259">Is Indexed</span></span>             | <span data-ttu-id="634eb-260">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-260">False</span></span>                             |
| <span data-ttu-id="634eb-261">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="634eb-261">In Global Catalog</span></span>      | <span data-ttu-id="634eb-262">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-262">False</span></span>                             |
| <span data-ttu-id="634eb-263">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="634eb-263">NT-Security-Descriptor</span></span> | <span data-ttu-id="634eb-264">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="634eb-264">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="634eb-265">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="634eb-265">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="634eb-266">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="634eb-266">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="634eb-267">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="634eb-267">Search-Flags</span></span>           | <span data-ttu-id="634eb-268">0x00000000</span><span class="sxs-lookup"><span data-stu-id="634eb-268">0x00000000</span></span>                        |
| <span data-ttu-id="634eb-269">System-Flags</span><span class="sxs-lookup"><span data-stu-id="634eb-269">System-Flags</span></span>           | <span data-ttu-id="634eb-270">0x00000011</span><span class="sxs-lookup"><span data-stu-id="634eb-270">0x00000011</span></span>                        |
| <span data-ttu-id="634eb-271">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="634eb-271">Classes used in</span></span>        | [<span data-ttu-id="634eb-272">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="634eb-272">**User**</span></span>](c-user.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="634eb-273">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="634eb-273">Windows Server 2012</span></span>



| <span data-ttu-id="634eb-274">Entrada</span><span class="sxs-lookup"><span data-stu-id="634eb-274">Entry</span></span> | <span data-ttu-id="634eb-275">Valor</span><span class="sxs-lookup"><span data-stu-id="634eb-275">Value</span></span> |
|------------------------|-----------------------------------|
| <span data-ttu-id="634eb-276">ID do link</span><span class="sxs-lookup"><span data-stu-id="634eb-276">Link-Id</span></span>                | \-                                |
| <span data-ttu-id="634eb-277">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="634eb-277">MAPI-Id</span></span>                | \-                                |
| <span data-ttu-id="634eb-278">System-Only</span><span class="sxs-lookup"><span data-stu-id="634eb-278">System-Only</span></span>            | <span data-ttu-id="634eb-279">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-279">False</span></span>                             |
| <span data-ttu-id="634eb-280">É de valor único</span><span class="sxs-lookup"><span data-stu-id="634eb-280">Is-Single-Valued</span></span>       | <span data-ttu-id="634eb-281">True</span><span class="sxs-lookup"><span data-stu-id="634eb-281">True</span></span>                              |
| <span data-ttu-id="634eb-282">É indexado</span><span class="sxs-lookup"><span data-stu-id="634eb-282">Is Indexed</span></span>             | <span data-ttu-id="634eb-283">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-283">False</span></span>                             |
| <span data-ttu-id="634eb-284">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="634eb-284">In Global Catalog</span></span>      | <span data-ttu-id="634eb-285">Falso</span><span class="sxs-lookup"><span data-stu-id="634eb-285">False</span></span>                             |
| <span data-ttu-id="634eb-286">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="634eb-286">NT-Security-Descriptor</span></span> | <span data-ttu-id="634eb-287">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="634eb-287">O:BAG:BAD:S:</span></span>                      |
| <span data-ttu-id="634eb-288">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="634eb-288">Range-Lower</span></span>            | \-                                |
| <span data-ttu-id="634eb-289">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="634eb-289">Range-Upper</span></span>            | \-                                |
| <span data-ttu-id="634eb-290">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="634eb-290">Search-Flags</span></span>           | <span data-ttu-id="634eb-291">0x00000000</span><span class="sxs-lookup"><span data-stu-id="634eb-291">0x00000000</span></span>                        |
| <span data-ttu-id="634eb-292">System-Flags</span><span class="sxs-lookup"><span data-stu-id="634eb-292">System-Flags</span></span>           | <span data-ttu-id="634eb-293">0x00000011</span><span class="sxs-lookup"><span data-stu-id="634eb-293">0x00000011</span></span>                        |
| <span data-ttu-id="634eb-294">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="634eb-294">Classes used in</span></span>        | [<span data-ttu-id="634eb-295">**Usuário**</span><span class="sxs-lookup"><span data-stu-id="634eb-295">**User**</span></span>](c-user.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="634eb-296">Comentários</span><span class="sxs-lookup"><span data-stu-id="634eb-296">Remarks</span></span>

<span data-ttu-id="634eb-297">A parte superior desse inteiro grande corresponde ao membro **dwHighDateTime** da estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e a parte inferior corresponde ao membro **dwLowDateTime** da estrutura **FILETIME** .</span><span class="sxs-lookup"><span data-stu-id="634eb-297">The high part of this large integer corresponds to the **dwHighDateTime** member of the [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure and the low part corresponds to the **dwLowDateTime** member of the **FILETIME** structure.</span></span>

<span data-ttu-id="634eb-298">Esse atributo não é replicado e é mantido separadamente em cada controlador de domínio no domínio.</span><span class="sxs-lookup"><span data-stu-id="634eb-298">This attribute is not replicated and is maintained separately on each domain controller in the domain.</span></span> <span data-ttu-id="634eb-299">Para obter um valor preciso para o último tempo de senha incorreto do usuário no domínio, cada controlador de domínio no domínio deve ser consultado.</span><span class="sxs-lookup"><span data-stu-id="634eb-299">To get an accurate value for the user's last bad password time in the domain, each domain controller in the domain must be queried.</span></span> <span data-ttu-id="634eb-300">O maior valor obtido representa o verdadeiro tempo de senha inválida.</span><span class="sxs-lookup"><span data-stu-id="634eb-300">The largest value that is obtained represents the true bad password time.</span></span>

 

