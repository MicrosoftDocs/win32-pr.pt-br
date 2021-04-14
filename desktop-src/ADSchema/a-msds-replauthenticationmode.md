---
title: ms-DS-repl-atributo de modo de autenticação
description: O atributo ms-DS-repl-authentication-mode é usado para especificar qual método de autenticação é usado para autenticar parceiros de replicação.
ms.assetid: b7e77b40-7aa7-4990-93fd-c8068e35fcf9
ms.tgt_platform: multiple
keywords:
- Esquema de AD do atributo ms-DS-repl-authentication-mode
- Esquema de AD do atributo msDS-ReplAuthenticationMode
topic_type:
- apiref
api_name:
- ms-DS-Repl-Authentication-Mode
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b88c7e3223b946b56962b710b036ee6e0c36dc
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104456283"
---
# <a name="ms-ds-repl-authentication-mode-attribute"></a><span data-ttu-id="6fb87-105">ms-DS-repl-atributo de modo de autenticação</span><span class="sxs-lookup"><span data-stu-id="6fb87-105">ms-DS-Repl-Authentication-Mode attribute</span></span>

<span data-ttu-id="6fb87-106">O atributo **MS-DS-repl-authentication-mode** é usado para especificar qual método de autenticação é usado para autenticar parceiros de replicação.</span><span class="sxs-lookup"><span data-stu-id="6fb87-106">The **ms-DS-Repl-Authentication-Mode** attribute is used to specify which authentication method is used to authenticate replication partners.</span></span> <span data-ttu-id="6fb87-107">Esse atributo se aplica à partição de configuração de uma instância do ADAM.</span><span class="sxs-lookup"><span data-stu-id="6fb87-107">This attribute applies to the configuration partition of an ADAM instance.</span></span>

<span data-ttu-id="6fb87-108">Os valores a seguir são os possíveis valores para esse atributo.</span><span class="sxs-lookup"><span data-stu-id="6fb87-108">The following values are the possible values for this attribute.</span></span>

| <span data-ttu-id="6fb87-109">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb87-109">Value</span></span>        | <span data-ttu-id="6fb87-110">Método de autenticação</span><span class="sxs-lookup"><span data-stu-id="6fb87-110">Authentication method</span></span>                          | <span data-ttu-id="6fb87-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fb87-111">Description</span></span>                                                                                                                                                                    |
|--------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb87-112">0</span><span class="sxs-lookup"><span data-stu-id="6fb87-112">0</span></span><br/> | <span data-ttu-id="6fb87-113">Passagem negociada</span><span class="sxs-lookup"><span data-stu-id="6fb87-113">Negotiated pass-through</span></span><br/>             | <span data-ttu-id="6fb87-114">Todas as instâncias do ADAM no conjunto de configuração usam um nome de conta e senha idênticos como a conta de serviço do ADAM.</span><span class="sxs-lookup"><span data-stu-id="6fb87-114">All ADAM instances in the configuration set use an identical account name and password as the ADAM service account.</span></span><br/>                                                 |
| <span data-ttu-id="6fb87-115">1</span><span class="sxs-lookup"><span data-stu-id="6fb87-115">1</span></span><br/> | <span data-ttu-id="6fb87-116">Negociado</span><span class="sxs-lookup"><span data-stu-id="6fb87-116">Negotiated</span></span><br/>                          | <span data-ttu-id="6fb87-117">A tentativa com a autenticação Kerberos (usando SPNs) é feita primeiro.</span><span class="sxs-lookup"><span data-stu-id="6fb87-117">Kerberos authentication (using SPNs) is attempted first.</span></span> <span data-ttu-id="6fb87-118">Se essa tentativa falhar, a tentativa com a autenticação NTLM será realizada.</span><span class="sxs-lookup"><span data-stu-id="6fb87-118">If Kerberos fails, NTLM authentication is attempted.</span></span> <span data-ttu-id="6fb87-119">Se o NTLM falhar, as instâncias do ADAM não serão replicadas.</span><span class="sxs-lookup"><span data-stu-id="6fb87-119">If NTLM fails, the ADAM instances will not replicate.</span></span><br/> |
| <span data-ttu-id="6fb87-120">2</span><span class="sxs-lookup"><span data-stu-id="6fb87-120">2</span></span><br/> | <span data-ttu-id="6fb87-121">Autenticação mútua com o Kerberos</span><span class="sxs-lookup"><span data-stu-id="6fb87-121">Mutual authentication with Kerberos</span></span><br/> | <span data-ttu-id="6fb87-122">Autenticação Kerberos usando SPNs (nomes principais de serviços) necessária.</span><span class="sxs-lookup"><span data-stu-id="6fb87-122">Kerberos authentication, using service principal names (SPNs), is required.</span></span> <span data-ttu-id="6fb87-123">Se a autenticação Kerberos falhar, as instâncias do ADAM não serão replicadas.</span><span class="sxs-lookup"><span data-stu-id="6fb87-123">If Kerberos authentication fails, the ADAM instances will not replicate.</span></span><br/>                |



 

<span data-ttu-id="6fb87-124">A tabela a seguir contém os identificadores programáticos para os valores desse atributo.</span><span class="sxs-lookup"><span data-stu-id="6fb87-124">The following table contains the programmatic identifiers for the values of this attribute.</span></span>

| <span data-ttu-id="6fb87-125">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb87-125">Value</span></span>        | <span data-ttu-id="6fb87-126">Identificador (de NTDSAPI. h)</span><span class="sxs-lookup"><span data-stu-id="6fb87-126">Identifier (from Ntdsapi.h)</span></span>                                               |
|--------------|---------------------------------------------------------------------------|
| <span data-ttu-id="6fb87-127">0</span><span class="sxs-lookup"><span data-stu-id="6fb87-127">0</span></span><br/> | <span data-ttu-id="6fb87-128">**modo de autenticação de repl do ADAM \_ \_ \_ \_ negociar \_ passagem \_**</span><span class="sxs-lookup"><span data-stu-id="6fb87-128">**ADAM\_REPL\_AUTHENTICATION\_MODE\_NEGOTIATE\_PASS\_THROUGH**</span></span><br/> |
| <span data-ttu-id="6fb87-129">1</span><span class="sxs-lookup"><span data-stu-id="6fb87-129">1</span></span><br/> | <span data-ttu-id="6fb87-130">**modo de autenticação do ADAM \_ repl \_ \_ \_ Negotiate**</span><span class="sxs-lookup"><span data-stu-id="6fb87-130">**ADAM\_REPL\_AUTHENTICATION\_MODE\_NEGOTIATE**</span></span><br/>                |
| <span data-ttu-id="6fb87-131">2</span><span class="sxs-lookup"><span data-stu-id="6fb87-131">2</span></span><br/> | <span data-ttu-id="6fb87-132">**autorização mútua do modo de autenticação do ADAM \_ repl \_ \_ \_ \_ \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="6fb87-132">**ADAM\_REPL\_AUTHENTICATION\_MODE\_MUTUAL\_AUTH\_REQUIRED**</span></span><br/>   |



 



| <span data-ttu-id="6fb87-133">Entrada</span><span class="sxs-lookup"><span data-stu-id="6fb87-133">Entry</span></span> | <span data-ttu-id="6fb87-134">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb87-134">Value</span></span> |
|-------------------|--------------------------------------|
| <span data-ttu-id="6fb87-135">CN</span><span class="sxs-lookup"><span data-stu-id="6fb87-135">CN</span></span>                | <span data-ttu-id="6fb87-136">ms-DS-repl-authentication-mode</span><span class="sxs-lookup"><span data-stu-id="6fb87-136">ms-DS-Repl-Authentication-Mode</span></span>       |
| <span data-ttu-id="6fb87-137">LDAP-Display-Name</span><span class="sxs-lookup"><span data-stu-id="6fb87-137">Ldap-Display-Name</span></span> | <span data-ttu-id="6fb87-138">msDS-ReplAuthenticationMode</span><span class="sxs-lookup"><span data-stu-id="6fb87-138">msDS-ReplAuthenticationMode</span></span>          |
| <span data-ttu-id="6fb87-139">Tamanho</span><span class="sxs-lookup"><span data-stu-id="6fb87-139">Size</span></span>              | \-                                   |
| <span data-ttu-id="6fb87-140">Privilégio de atualização</span><span class="sxs-lookup"><span data-stu-id="6fb87-140">Update Privilege</span></span>  | \-                                   |
| <span data-ttu-id="6fb87-141">Frequência de atualização</span><span class="sxs-lookup"><span data-stu-id="6fb87-141">Update Frequency</span></span>  | \-                                   |
| <span data-ttu-id="6fb87-142">Attribute-Id</span><span class="sxs-lookup"><span data-stu-id="6fb87-142">Attribute-Id</span></span>      | <span data-ttu-id="6fb87-143">1.2.840.113556.1.4.1861</span><span class="sxs-lookup"><span data-stu-id="6fb87-143">1.2.840.113556.1.4.1861</span></span>              |
| <span data-ttu-id="6fb87-144">System-ID-GUID</span><span class="sxs-lookup"><span data-stu-id="6fb87-144">System-Id-Guid</span></span>    | <span data-ttu-id="6fb87-145">6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50</span><span class="sxs-lookup"><span data-stu-id="6fb87-145">6e124d4f-1a3f-4cc6-8e09-4a54c81b1d50</span></span> |
| <span data-ttu-id="6fb87-146">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fb87-146">Syntax</span></span>            | [<span data-ttu-id="6fb87-147">**Enumeração**</span><span class="sxs-lookup"><span data-stu-id="6fb87-147">**Enumeration**</span></span>](s-enumeration.md) |



## <a name="implementations"></a><span data-ttu-id="6fb87-148">Implementações</span><span class="sxs-lookup"><span data-stu-id="6fb87-148">Implementations</span></span>

-   [<span data-ttu-id="6fb87-149">**ADAM**</span><span class="sxs-lookup"><span data-stu-id="6fb87-149">**ADAM**</span></span>](#adam)

## <a name="adam"></a><span data-ttu-id="6fb87-150">ADAM</span><span class="sxs-lookup"><span data-stu-id="6fb87-150">ADAM</span></span>



| <span data-ttu-id="6fb87-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="6fb87-151">Entry</span></span> | <span data-ttu-id="6fb87-152">Valor</span><span class="sxs-lookup"><span data-stu-id="6fb87-152">Value</span></span> |
|------------------------|-----------------------------------------------------|
| <span data-ttu-id="6fb87-153">ID do link</span><span class="sxs-lookup"><span data-stu-id="6fb87-153">Link-Id</span></span>                | \-                                                  |
| <span data-ttu-id="6fb87-154">MAPI-Id</span><span class="sxs-lookup"><span data-stu-id="6fb87-154">MAPI-Id</span></span>                | \-                                                  |
| <span data-ttu-id="6fb87-155">System-Only</span><span class="sxs-lookup"><span data-stu-id="6fb87-155">System-Only</span></span>            | <span data-ttu-id="6fb87-156">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb87-156">False</span></span>                                               |
| <span data-ttu-id="6fb87-157">É de valor único</span><span class="sxs-lookup"><span data-stu-id="6fb87-157">Is-Single-Valued</span></span>       | <span data-ttu-id="6fb87-158">True</span><span class="sxs-lookup"><span data-stu-id="6fb87-158">True</span></span>                                                |
| <span data-ttu-id="6fb87-159">É indexado</span><span class="sxs-lookup"><span data-stu-id="6fb87-159">Is Indexed</span></span>             | <span data-ttu-id="6fb87-160">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb87-160">False</span></span>                                               |
| <span data-ttu-id="6fb87-161">No catálogo global</span><span class="sxs-lookup"><span data-stu-id="6fb87-161">In Global Catalog</span></span>      | <span data-ttu-id="6fb87-162">Falso</span><span class="sxs-lookup"><span data-stu-id="6fb87-162">False</span></span>                                               |
| <span data-ttu-id="6fb87-163">NT-Security-Descriptor</span><span class="sxs-lookup"><span data-stu-id="6fb87-163">NT-Security-Descriptor</span></span> | <span data-ttu-id="6fb87-164">O:BAG: INADEQUADO: S:</span><span class="sxs-lookup"><span data-stu-id="6fb87-164">O:BAG:BAD:S:</span></span>                                        |
| <span data-ttu-id="6fb87-165">Range-Lower</span><span class="sxs-lookup"><span data-stu-id="6fb87-165">Range-Lower</span></span>            | \-                                                  |
| <span data-ttu-id="6fb87-166">Range-Upper</span><span class="sxs-lookup"><span data-stu-id="6fb87-166">Range-Upper</span></span>            | \-                                                  |
| <span data-ttu-id="6fb87-167">Search-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb87-167">Search-Flags</span></span>           | <span data-ttu-id="6fb87-168">0x00000000</span><span class="sxs-lookup"><span data-stu-id="6fb87-168">0x00000000</span></span>                                          |
| <span data-ttu-id="6fb87-169">System-Flags</span><span class="sxs-lookup"><span data-stu-id="6fb87-169">System-Flags</span></span>           | <span data-ttu-id="6fb87-170">0x00000010</span><span class="sxs-lookup"><span data-stu-id="6fb87-170">0x00000010</span></span>                                          |
| <span data-ttu-id="6fb87-171">Classes usadas em</span><span class="sxs-lookup"><span data-stu-id="6fb87-171">Classes used in</span></span>        | [<span data-ttu-id="6fb87-172">**Configuração**</span><span class="sxs-lookup"><span data-stu-id="6fb87-172">**Configuration**</span></span>](c-configuration.md)<br/> |



 

 





