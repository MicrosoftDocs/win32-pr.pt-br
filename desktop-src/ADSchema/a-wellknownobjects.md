---
title: Atributo well-known-Objects
description: Esse atributo contém uma lista de contêineres de objeto conhecidos por GUID e nome diferenciado.
ms.assetid: e3c2d243-6734-4c2f-9ead-bc4ec071d1f1
ms.tgt_platform: multiple
keywords:
- Esquema do AD do atributo well-known-Objects
- Esquema de AD do atributo wellKnownObjects
topic_type:
- apiref
api_name:
- Well-Known-Objects
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e21df3db14a29de137af4792f0e9ca6df27b90
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456243"
---
# <a name="well-known-objects-attribute"></a><span data-ttu-id="d7729-105">Atributo well-known-Objects</span><span class="sxs-lookup"><span data-stu-id="d7729-105">Well-Known-Objects attribute</span></span>

<span data-ttu-id="d7729-106">Esse atributo contém uma lista de contêineres de objeto conhecidos por GUID e nome diferenciado.</span><span class="sxs-lookup"><span data-stu-id="d7729-106">This attribute contains a list of well-known object containers by GUID and distinguished name.</span></span> <span data-ttu-id="d7729-107">Os objetos bem conhecidos são contêineres do sistema.</span><span class="sxs-lookup"><span data-stu-id="d7729-107">The well-known objects are system containers.</span></span> <span data-ttu-id="d7729-108">Essas informações são usadas para recuperar um objeto depois que ele é movido usando apenas o GUID e o nome de domínio.</span><span class="sxs-lookup"><span data-stu-id="d7729-108">This information is used to retrieve an object after it has been moved by using just the GUID and the domain name.</span></span> <span data-ttu-id="d7729-109">Sempre que o objeto for movido, o sistema atualizará automaticamente a parte do nome distinto dos valores de objetos conhecidos que referenciaram o objeto.</span><span class="sxs-lookup"><span data-stu-id="d7729-109">Whenever the object is moved, the system automatically updates the Distinguished Name portion of the Well-Known-Objects values that referred to the object.</span></span> <span data-ttu-id="d7729-110">O arquivo NTDSAPI. h contém as seguintes definições, que podem ser usadas para recuperar um objeto (os GUIDs associados a esses objetos estão contidos em NTDSAPI. h):</span><span class="sxs-lookup"><span data-stu-id="d7729-110">The file Ntdsapi.h contains the following definitions, which can be used to retrieve an object (the GUIDs that are associated to these objects are contained in Ntdsapi.h):</span></span>

-   <span data-ttu-id="d7729-111">\_contêiner de usuários GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="d7729-111">GUID\_USERS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d7729-112">\_contêiner COMPUTRS \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="d7729-112">GUID\_COMPUTRS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d7729-113">contêiner de sistemas de GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="d7729-113">GUID\_SYSTEMS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d7729-114">contêiner de controladores de domínio do GUID \_ \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="d7729-114">GUID\_DOMAIN\_CONTROLLERS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d7729-115">contêiner de infraestrutura de GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="d7729-115">GUID\_INFRASTRUCTURE\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d7729-116">\_contêiner de objetos excluídos de GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="d7729-116">GUID\_DELETED\_OBJECTS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d7729-117">contêiner de LOSTANDFOUND de GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="d7729-117">GUID\_LOSTANDFOUND\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d7729-118">\_contêiner FOREIGNSECURITYPRINCIPALS \_ GUID \_ W</span><span class="sxs-lookup"><span data-stu-id="d7729-118">GUID\_FOREIGNSECURITYPRINCIPALS\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d7729-119">\_contêiner de dados do programa GUID \_ \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="d7729-119">GUID\_PROGRAM\_DATA\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d7729-120">GUID \_ do \_ \_ contêiner de dados do programa \_ Microsoft \_</span><span class="sxs-lookup"><span data-stu-id="d7729-120">GUID\_MICROSOFT\_PROGRAM\_DATA\_CONTAINER\_W</span></span>
-   <span data-ttu-id="d7729-121">\_contêiner de \_ cotas NTDS de GUID \_ \_ W</span><span class="sxs-lookup"><span data-stu-id="d7729-121">GUID\_NTDS\_QUOTAS\_CONTAINER\_W</span></span>



| <span data-ttu-id="d7729-122">Entrada</span><span class="sxs-lookup"><span data-stu-id="d7729-122">Entry</span></span> | <span data-ttu-id="d7729-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d7729-123">Value</span></span> |
|-------------------|-------------------------------------------------|
| <span data-ttu-id="d7729-124">CN</span><span class="sxs-lookup"><span data-stu-id="d7729-124">CN</span></span>                | <span data-ttu-id="d7729-125">Objetos bem conhecidos</span><span class="sxs-lookup"><span data-stu-id="d7729-125">Well-Known-Objects</span></span>                              |
| <span data-ttu-id="d7729-126">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="d7729-126">Ldap-Display-Name</span></span> | <span data-ttu-id="d7729-127">wellKnownObjects</span><span class="sxs-lookup"><span data-stu-id="d7729-127">wellKnownObjects</span></span>                                |
| <span data-ttu-id="d7729-128">Tamanho</span><span class="sxs-lookup"><span data-stu-id="d7729-128">Size</span></span>              | \-                                              |
| <span data-ttu-id="d7729-129">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="d7729-129">Update Privilege</span></span>  | <span data-ttu-id="d7729-130">Esse valor é definido pelo sistema.</span><span class="sxs-lookup"><span data-stu-id="d7729-130">This value is set by the system.</span></span>                |
| <span data-ttu-id="d7729-131">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="d7729-131">Update Frequency</span></span>  | <span data-ttu-id="d7729-132">Sempre que um dos contêineres do sistema for movido.</span><span class="sxs-lookup"><span data-stu-id="d7729-132">Whenever one of the system containers is moved.</span></span> |
| <span data-ttu-id="d7729-133">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="d7729-133">Attribute-Id</span></span>      | <span data-ttu-id="d7729-134">1.2.840.113556.1.4.618</span><span class="sxs-lookup"><span data-stu-id="d7729-134">1.2.840.113556.1.4.618</span></span>                          |
| <span data-ttu-id="d7729-135">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="d7729-135">System-Id-Guid</span></span>    | <span data-ttu-id="d7729-136">05308983-7688-11d1-aded-00c04fd8d5cd</span><span class="sxs-lookup"><span data-stu-id="d7729-136">05308983-7688-11d1-aded-00c04fd8d5cd</span></span>            |
| <span data-ttu-id="d7729-137">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7729-137">Syntax</span></span>            | [<span data-ttu-id="d7729-138">**Objeto (DN-binário)**</span><span class="sxs-lookup"><span data-stu-id="d7729-138">**Object(DN-Binary)**</span></span>](s-object-dn-binary.md) |



## <a name="implementations"></a><span data-ttu-id="d7729-139">Implementações</span><span class="sxs-lookup"><span data-stu-id="d7729-139">Implementations</span></span>

-   [<span data-ttu-id="d7729-140">**Windows 2000 Server**</span><span class="sxs-lookup"><span data-stu-id="d7729-140">**Windows 2000 Server**</span></span>](#windows-2000-server)
-   [<span data-ttu-id="d7729-141">**Windows Server 2003**</span><span class="sxs-lookup"><span data-stu-id="d7729-141">**Windows Server 2003**</span></span>](#windows-server-2003)
-   [<span data-ttu-id="d7729-142">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="d7729-142">**ADAM**</span></span>](#adam)
-   [<span data-ttu-id="d7729-143">**Windows Server 2003 R2**</span><span class="sxs-lookup"><span data-stu-id="d7729-143">**Windows Server 2003 R2**</span></span>](#windows-server-2003-r2)
-   [<span data-ttu-id="d7729-144">**Windows Server 2008**</span><span class="sxs-lookup"><span data-stu-id="d7729-144">**Windows Server 2008**</span></span>](#windows-server-2008)
-   [<span data-ttu-id="d7729-145">**Windows Server 2008 R2**</span><span class="sxs-lookup"><span data-stu-id="d7729-145">**Windows Server 2008 R2**</span></span>](#windows-server-2008-r2)
-   [<span data-ttu-id="d7729-146">**Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="d7729-146">**Windows Server 2012**</span></span>](#windows-server-2012)

## <a name="windows-2000-server"></a><span data-ttu-id="d7729-147">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d7729-147">Windows 2000 Server</span></span>



| <span data-ttu-id="d7729-148">Entrada</span><span class="sxs-lookup"><span data-stu-id="d7729-148">Entry</span></span> | <span data-ttu-id="d7729-149">Valor</span><span class="sxs-lookup"><span data-stu-id="d7729-149">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d7729-150">ID do link</span><span class="sxs-lookup"><span data-stu-id="d7729-150">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d7729-151">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7729-151">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d7729-152">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7729-152">System-Only</span></span>            | <span data-ttu-id="d7729-153">True</span><span class="sxs-lookup"><span data-stu-id="d7729-153">True</span></span>                            |
| <span data-ttu-id="d7729-154">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d7729-154">Is-Single-Valued</span></span>       | <span data-ttu-id="d7729-155">Falso</span><span class="sxs-lookup"><span data-stu-id="d7729-155">False</span></span>                           |
| <span data-ttu-id="d7729-156">É indexado</span><span class="sxs-lookup"><span data-stu-id="d7729-156">Is Indexed</span></span>             | <span data-ttu-id="d7729-157">Falso</span><span class="sxs-lookup"><span data-stu-id="d7729-157">False</span></span>                           |
| <span data-ttu-id="d7729-158">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d7729-158">In Global Catalog</span></span>      | <span data-ttu-id="d7729-159">True</span><span class="sxs-lookup"><span data-stu-id="d7729-159">True</span></span>                            |
| <span data-ttu-id="d7729-160">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d7729-160">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7729-161">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d7729-161">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d7729-162">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7729-162">Range-Lower</span></span>            | \-                              |
| <span data-ttu-id="d7729-163">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7729-163">Range-Upper</span></span>            | \-                              |
| <span data-ttu-id="d7729-164">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7729-164">Search-Flags</span></span>           | <span data-ttu-id="d7729-165">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7729-165">0x00000000</span></span>                      |
| <span data-ttu-id="d7729-166">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7729-166">System-Flags</span></span>           | <span data-ttu-id="d7729-167">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d7729-167">0x00000012</span></span>                      |
| <span data-ttu-id="d7729-168">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d7729-168">Classes used in</span></span>        | [<span data-ttu-id="d7729-169">**Início**</span><span class="sxs-lookup"><span data-stu-id="d7729-169">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003"></a><span data-ttu-id="d7729-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d7729-170">Windows Server 2003</span></span>



| <span data-ttu-id="d7729-171">Entrada</span><span class="sxs-lookup"><span data-stu-id="d7729-171">Entry</span></span> | <span data-ttu-id="d7729-172">Valor</span><span class="sxs-lookup"><span data-stu-id="d7729-172">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d7729-173">ID do link</span><span class="sxs-lookup"><span data-stu-id="d7729-173">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d7729-174">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7729-174">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d7729-175">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7729-175">System-Only</span></span>            | <span data-ttu-id="d7729-176">True</span><span class="sxs-lookup"><span data-stu-id="d7729-176">True</span></span>                            |
| <span data-ttu-id="d7729-177">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d7729-177">Is-Single-Valued</span></span>       | <span data-ttu-id="d7729-178">Falso</span><span class="sxs-lookup"><span data-stu-id="d7729-178">False</span></span>                           |
| <span data-ttu-id="d7729-179">É indexado</span><span class="sxs-lookup"><span data-stu-id="d7729-179">Is Indexed</span></span>             | <span data-ttu-id="d7729-180">Falso</span><span class="sxs-lookup"><span data-stu-id="d7729-180">False</span></span>                           |
| <span data-ttu-id="d7729-181">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d7729-181">In Global Catalog</span></span>      | <span data-ttu-id="d7729-182">True</span><span class="sxs-lookup"><span data-stu-id="d7729-182">True</span></span>                            |
| <span data-ttu-id="d7729-183">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d7729-183">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7729-184">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d7729-184">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d7729-185">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7729-185">Range-Lower</span></span>            | <span data-ttu-id="d7729-186">16</span><span class="sxs-lookup"><span data-stu-id="d7729-186">16</span></span>                              |
| <span data-ttu-id="d7729-187">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7729-187">Range-Upper</span></span>            | <span data-ttu-id="d7729-188">16</span><span class="sxs-lookup"><span data-stu-id="d7729-188">16</span></span>                              |
| <span data-ttu-id="d7729-189">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7729-189">Search-Flags</span></span>           | <span data-ttu-id="d7729-190">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7729-190">0x00000000</span></span>                      |
| <span data-ttu-id="d7729-191">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7729-191">System-Flags</span></span>           | <span data-ttu-id="d7729-192">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d7729-192">0x00000012</span></span>                      |
| <span data-ttu-id="d7729-193">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d7729-193">Classes used in</span></span>        | [<span data-ttu-id="d7729-194">**Início**</span><span class="sxs-lookup"><span data-stu-id="d7729-194">**Top**</span></span>](c-top.md)<br/> |



## <a name="adam"></a><span data-ttu-id="d7729-195">ADAM</span><span class="sxs-lookup"><span data-stu-id="d7729-195">ADAM</span></span>



| <span data-ttu-id="d7729-196">Entrada</span><span class="sxs-lookup"><span data-stu-id="d7729-196">Entry</span></span> | <span data-ttu-id="d7729-197">Valor</span><span class="sxs-lookup"><span data-stu-id="d7729-197">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d7729-198">ID do link</span><span class="sxs-lookup"><span data-stu-id="d7729-198">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d7729-199">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7729-199">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d7729-200">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7729-200">System-Only</span></span>            | <span data-ttu-id="d7729-201">True</span><span class="sxs-lookup"><span data-stu-id="d7729-201">True</span></span>                            |
| <span data-ttu-id="d7729-202">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d7729-202">Is-Single-Valued</span></span>       | <span data-ttu-id="d7729-203">Falso</span><span class="sxs-lookup"><span data-stu-id="d7729-203">False</span></span>                           |
| <span data-ttu-id="d7729-204">É indexado</span><span class="sxs-lookup"><span data-stu-id="d7729-204">Is Indexed</span></span>             | <span data-ttu-id="d7729-205">Falso</span><span class="sxs-lookup"><span data-stu-id="d7729-205">False</span></span>                           |
| <span data-ttu-id="d7729-206">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d7729-206">In Global Catalog</span></span>      | <span data-ttu-id="d7729-207">True</span><span class="sxs-lookup"><span data-stu-id="d7729-207">True</span></span>                            |
| <span data-ttu-id="d7729-208">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d7729-208">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7729-209">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d7729-209">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d7729-210">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7729-210">Range-Lower</span></span>            | <span data-ttu-id="d7729-211">16</span><span class="sxs-lookup"><span data-stu-id="d7729-211">16</span></span>                              |
| <span data-ttu-id="d7729-212">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7729-212">Range-Upper</span></span>            | <span data-ttu-id="d7729-213">16</span><span class="sxs-lookup"><span data-stu-id="d7729-213">16</span></span>                              |
| <span data-ttu-id="d7729-214">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7729-214">Search-Flags</span></span>           | <span data-ttu-id="d7729-215">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7729-215">0x00000000</span></span>                      |
| <span data-ttu-id="d7729-216">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7729-216">System-Flags</span></span>           | <span data-ttu-id="d7729-217">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d7729-217">0x00000012</span></span>                      |
| <span data-ttu-id="d7729-218">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d7729-218">Classes used in</span></span>        | [<span data-ttu-id="d7729-219">**Início**</span><span class="sxs-lookup"><span data-stu-id="d7729-219">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a><span data-ttu-id="d7729-220">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="d7729-220">Windows Server 2003 R2</span></span>



| <span data-ttu-id="d7729-221">Entrada</span><span class="sxs-lookup"><span data-stu-id="d7729-221">Entry</span></span> | <span data-ttu-id="d7729-222">Valor</span><span class="sxs-lookup"><span data-stu-id="d7729-222">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d7729-223">ID do link</span><span class="sxs-lookup"><span data-stu-id="d7729-223">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d7729-224">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7729-224">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d7729-225">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7729-225">System-Only</span></span>            | <span data-ttu-id="d7729-226">True</span><span class="sxs-lookup"><span data-stu-id="d7729-226">True</span></span>                            |
| <span data-ttu-id="d7729-227">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d7729-227">Is-Single-Valued</span></span>       | <span data-ttu-id="d7729-228">Falso</span><span class="sxs-lookup"><span data-stu-id="d7729-228">False</span></span>                           |
| <span data-ttu-id="d7729-229">É indexado</span><span class="sxs-lookup"><span data-stu-id="d7729-229">Is Indexed</span></span>             | <span data-ttu-id="d7729-230">Falso</span><span class="sxs-lookup"><span data-stu-id="d7729-230">False</span></span>                           |
| <span data-ttu-id="d7729-231">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d7729-231">In Global Catalog</span></span>      | <span data-ttu-id="d7729-232">True</span><span class="sxs-lookup"><span data-stu-id="d7729-232">True</span></span>                            |
| <span data-ttu-id="d7729-233">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d7729-233">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7729-234">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d7729-234">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d7729-235">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7729-235">Range-Lower</span></span>            | <span data-ttu-id="d7729-236">16</span><span class="sxs-lookup"><span data-stu-id="d7729-236">16</span></span>                              |
| <span data-ttu-id="d7729-237">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7729-237">Range-Upper</span></span>            | <span data-ttu-id="d7729-238">16</span><span class="sxs-lookup"><span data-stu-id="d7729-238">16</span></span>                              |
| <span data-ttu-id="d7729-239">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7729-239">Search-Flags</span></span>           | <span data-ttu-id="d7729-240">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7729-240">0x00000000</span></span>                      |
| <span data-ttu-id="d7729-241">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7729-241">System-Flags</span></span>           | <span data-ttu-id="d7729-242">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d7729-242">0x00000012</span></span>                      |
| <span data-ttu-id="d7729-243">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d7729-243">Classes used in</span></span>        | [<span data-ttu-id="d7729-244">**Início**</span><span class="sxs-lookup"><span data-stu-id="d7729-244">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008"></a><span data-ttu-id="d7729-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7729-245">Windows Server 2008</span></span>



| <span data-ttu-id="d7729-246">Entrada</span><span class="sxs-lookup"><span data-stu-id="d7729-246">Entry</span></span> | <span data-ttu-id="d7729-247">Valor</span><span class="sxs-lookup"><span data-stu-id="d7729-247">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d7729-248">ID do link</span><span class="sxs-lookup"><span data-stu-id="d7729-248">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d7729-249">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7729-249">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d7729-250">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7729-250">System-Only</span></span>            | <span data-ttu-id="d7729-251">True</span><span class="sxs-lookup"><span data-stu-id="d7729-251">True</span></span>                            |
| <span data-ttu-id="d7729-252">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d7729-252">Is-Single-Valued</span></span>       | <span data-ttu-id="d7729-253">Falso</span><span class="sxs-lookup"><span data-stu-id="d7729-253">False</span></span>                           |
| <span data-ttu-id="d7729-254">É indexado</span><span class="sxs-lookup"><span data-stu-id="d7729-254">Is Indexed</span></span>             | <span data-ttu-id="d7729-255">Falso</span><span class="sxs-lookup"><span data-stu-id="d7729-255">False</span></span>                           |
| <span data-ttu-id="d7729-256">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d7729-256">In Global Catalog</span></span>      | <span data-ttu-id="d7729-257">True</span><span class="sxs-lookup"><span data-stu-id="d7729-257">True</span></span>                            |
| <span data-ttu-id="d7729-258">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d7729-258">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7729-259">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d7729-259">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d7729-260">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7729-260">Range-Lower</span></span>            | <span data-ttu-id="d7729-261">16</span><span class="sxs-lookup"><span data-stu-id="d7729-261">16</span></span>                              |
| <span data-ttu-id="d7729-262">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7729-262">Range-Upper</span></span>            | <span data-ttu-id="d7729-263">16</span><span class="sxs-lookup"><span data-stu-id="d7729-263">16</span></span>                              |
| <span data-ttu-id="d7729-264">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7729-264">Search-Flags</span></span>           | <span data-ttu-id="d7729-265">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7729-265">0x00000000</span></span>                      |
| <span data-ttu-id="d7729-266">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7729-266">System-Flags</span></span>           | <span data-ttu-id="d7729-267">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d7729-267">0x00000012</span></span>                      |
| <span data-ttu-id="d7729-268">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d7729-268">Classes used in</span></span>        | [<span data-ttu-id="d7729-269">**Início**</span><span class="sxs-lookup"><span data-stu-id="d7729-269">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a><span data-ttu-id="d7729-270">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d7729-270">Windows Server 2008 R2</span></span>



| <span data-ttu-id="d7729-271">Entrada</span><span class="sxs-lookup"><span data-stu-id="d7729-271">Entry</span></span> | <span data-ttu-id="d7729-272">Valor</span><span class="sxs-lookup"><span data-stu-id="d7729-272">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d7729-273">ID do link</span><span class="sxs-lookup"><span data-stu-id="d7729-273">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d7729-274">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7729-274">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d7729-275">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7729-275">System-Only</span></span>            | <span data-ttu-id="d7729-276">True</span><span class="sxs-lookup"><span data-stu-id="d7729-276">True</span></span>                            |
| <span data-ttu-id="d7729-277">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d7729-277">Is-Single-Valued</span></span>       | <span data-ttu-id="d7729-278">Falso</span><span class="sxs-lookup"><span data-stu-id="d7729-278">False</span></span>                           |
| <span data-ttu-id="d7729-279">É indexado</span><span class="sxs-lookup"><span data-stu-id="d7729-279">Is Indexed</span></span>             | <span data-ttu-id="d7729-280">Falso</span><span class="sxs-lookup"><span data-stu-id="d7729-280">False</span></span>                           |
| <span data-ttu-id="d7729-281">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d7729-281">In Global Catalog</span></span>      | <span data-ttu-id="d7729-282">True</span><span class="sxs-lookup"><span data-stu-id="d7729-282">True</span></span>                            |
| <span data-ttu-id="d7729-283">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d7729-283">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7729-284">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d7729-284">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d7729-285">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7729-285">Range-Lower</span></span>            | <span data-ttu-id="d7729-286">16</span><span class="sxs-lookup"><span data-stu-id="d7729-286">16</span></span>                              |
| <span data-ttu-id="d7729-287">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7729-287">Range-Upper</span></span>            | <span data-ttu-id="d7729-288">16</span><span class="sxs-lookup"><span data-stu-id="d7729-288">16</span></span>                              |
| <span data-ttu-id="d7729-289">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7729-289">Search-Flags</span></span>           | <span data-ttu-id="d7729-290">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7729-290">0x00000000</span></span>                      |
| <span data-ttu-id="d7729-291">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7729-291">System-Flags</span></span>           | <span data-ttu-id="d7729-292">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d7729-292">0x00000012</span></span>                      |
| <span data-ttu-id="d7729-293">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d7729-293">Classes used in</span></span>        | [<span data-ttu-id="d7729-294">**Início**</span><span class="sxs-lookup"><span data-stu-id="d7729-294">**Top**</span></span>](c-top.md)<br/> |



## <a name="windows-server-2012"></a><span data-ttu-id="d7729-295">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d7729-295">Windows Server 2012</span></span>



| <span data-ttu-id="d7729-296">Entrada</span><span class="sxs-lookup"><span data-stu-id="d7729-296">Entry</span></span> | <span data-ttu-id="d7729-297">Valor</span><span class="sxs-lookup"><span data-stu-id="d7729-297">Value</span></span> |
|------------------------|---------------------------------|
| <span data-ttu-id="d7729-298">ID do link</span><span class="sxs-lookup"><span data-stu-id="d7729-298">Link-Id</span></span>                | \-                              |
| <span data-ttu-id="d7729-299">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="d7729-299">MAPI-Id</span></span>                | \-                              |
| <span data-ttu-id="d7729-300">System-Only</span><span class="sxs-lookup"><span data-stu-id="d7729-300">System-Only</span></span>            | <span data-ttu-id="d7729-301">True</span><span class="sxs-lookup"><span data-stu-id="d7729-301">True</span></span>                            |
| <span data-ttu-id="d7729-302">É de valor único</span><span class="sxs-lookup"><span data-stu-id="d7729-302">Is-Single-Valued</span></span>       | <span data-ttu-id="d7729-303">Falso</span><span class="sxs-lookup"><span data-stu-id="d7729-303">False</span></span>                           |
| <span data-ttu-id="d7729-304">É indexado</span><span class="sxs-lookup"><span data-stu-id="d7729-304">Is Indexed</span></span>             | <span data-ttu-id="d7729-305">Falso</span><span class="sxs-lookup"><span data-stu-id="d7729-305">False</span></span>                           |
| <span data-ttu-id="d7729-306">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="d7729-306">In Global Catalog</span></span>      | <span data-ttu-id="d7729-307">True</span><span class="sxs-lookup"><span data-stu-id="d7729-307">True</span></span>                            |
| <span data-ttu-id="d7729-308">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="d7729-308">NT-Security-Descriptor</span></span> | <span data-ttu-id="d7729-309">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="d7729-309">O:BAG:BAD:S:</span></span>                    |
| <span data-ttu-id="d7729-310">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="d7729-310">Range-Lower</span></span>            | <span data-ttu-id="d7729-311">16</span><span class="sxs-lookup"><span data-stu-id="d7729-311">16</span></span>                              |
| <span data-ttu-id="d7729-312">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="d7729-312">Range-Upper</span></span>            | <span data-ttu-id="d7729-313">16</span><span class="sxs-lookup"><span data-stu-id="d7729-313">16</span></span>                              |
| <span data-ttu-id="d7729-314">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="d7729-314">Search-Flags</span></span>           | <span data-ttu-id="d7729-315">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d7729-315">0x00000000</span></span>                      |
| <span data-ttu-id="d7729-316">System-Flags</span><span class="sxs-lookup"><span data-stu-id="d7729-316">System-Flags</span></span>           | <span data-ttu-id="d7729-317">0x00000012</span><span class="sxs-lookup"><span data-stu-id="d7729-317">0x00000012</span></span>                      |
| <span data-ttu-id="d7729-318">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="d7729-318">Classes used in</span></span>        | [<span data-ttu-id="d7729-319">**Início**</span><span class="sxs-lookup"><span data-stu-id="d7729-319">**Top**</span></span>](c-top.md)<br/> |



 

 





