---
title: Funções auxiliares de WPAD IPv6-Aware e Legacy
description: Diferenças entre IPv6-Aware funções auxiliares WPAD e funções auxiliares WPAD herdadas
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511b7f04aa0a2abe04b99562c15aeb3a53bdaadf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771648"
---
# <a name="ipv6-aware-and-legacy-wpad-helper-functions"></a><span data-ttu-id="8fe36-103">Funções auxiliares de WPAD IPv6-Aware e Legacy</span><span class="sxs-lookup"><span data-stu-id="8fe36-103">IPv6-Aware and Legacy WPAD helper functions</span></span>

<span data-ttu-id="8fe36-104">As tabelas a seguir explicam as diferenças entre as novas funções auxiliares WPAD e as funções auxiliares WPAD herdadas.</span><span class="sxs-lookup"><span data-stu-id="8fe36-104">The following tables explain the differences between the new WPAD helper functions and the legacy WPAD helper functions.</span></span> <span data-ttu-id="8fe36-105">As novas funções são marcadas com um asterisco.</span><span class="sxs-lookup"><span data-stu-id="8fe36-105">The new functions are marked with an asterisk.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8fe36-106">Funções</span><span class="sxs-lookup"><span data-stu-id="8fe36-106">Functions</span></span></th>
<th><span data-ttu-id="8fe36-107">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fe36-107">Input</span></span></th>
<th><span data-ttu-id="8fe36-108">Saída</span><span class="sxs-lookup"><span data-stu-id="8fe36-108">Output</span></span></th>
<th><span data-ttu-id="8fe36-109">Motivo da alteração</span><span class="sxs-lookup"><span data-stu-id="8fe36-109">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8fe36-110">dnsResolve</span><span class="sxs-lookup"><span data-stu-id="8fe36-110">dnsResolve</span></span></td>
<td><span data-ttu-id="8fe36-111">Host</span><span class="sxs-lookup"><span data-stu-id="8fe36-111">Host</span></span></td>
<td><span data-ttu-id="8fe36-112">Endereço IPv4</span><span class="sxs-lookup"><span data-stu-id="8fe36-112">IPv4 address</span></span></td>
<td rowspan="2"><span data-ttu-id="8fe36-113">A função ex retornará uma lista de IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="8fe36-113">Ex function will return a list of IPv6/IPv4.</span></span> <span data-ttu-id="8fe36-114">Necessário, uma vez que os endereços IPv6 ou IPv4 podem ter vários endereços unicast para uma única interface. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="8fe36-114">Necessary since IPv6 or IPv4 addresses can have multiple unicast addresses for a single interface.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8fe36-115">dnsResolveEx\*</span><span class="sxs-lookup"><span data-stu-id="8fe36-115">dnsResolveEx\*</span></span></td>
<td><span data-ttu-id="8fe36-116">Host</span><span class="sxs-lookup"><span data-stu-id="8fe36-116">Host</span></span></td>
<td><span data-ttu-id="8fe36-117">Lista de endereços IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="8fe36-117">List of IPv6/IPv4 addresses</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8fe36-118">Funções</span><span class="sxs-lookup"><span data-stu-id="8fe36-118">Functions</span></span></th>
<th><span data-ttu-id="8fe36-119">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fe36-119">Input</span></span></th>
<th><span data-ttu-id="8fe36-120">Saída</span><span class="sxs-lookup"><span data-stu-id="8fe36-120">Output</span></span></th>
<th><span data-ttu-id="8fe36-121">Motivo da alteração</span><span class="sxs-lookup"><span data-stu-id="8fe36-121">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8fe36-122">isresolveble</span><span class="sxs-lookup"><span data-stu-id="8fe36-122">isResolveable</span></span></td>
<td><span data-ttu-id="8fe36-123">Host IPv4</span><span class="sxs-lookup"><span data-stu-id="8fe36-123">IPv4 host</span></span></td>
<td><span data-ttu-id="8fe36-124">VERDADEIRO/FALSO</span><span class="sxs-lookup"><span data-stu-id="8fe36-124">TRUE / FALSE</span></span></td>
<td rowspan="2"><span data-ttu-id="8fe36-125">A função ex retornará TRUE se um host puder resolver para um endereço IPv6 ou IPv4.</span><span class="sxs-lookup"><span data-stu-id="8fe36-125">The Ex function will return TRUE if a host can resolve to an IPv6 or IPv4 address.</span></span> <span data-ttu-id="8fe36-126">A função Legacy retornará TRUE se o host for resolvido para um endereço IPv4. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="8fe36-126">The legacy function only returns TRUE if the host resolves to an IPv4 address.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8fe36-127">isResolveableEx\*</span><span class="sxs-lookup"><span data-stu-id="8fe36-127">isResolveableEx\*</span></span></td>
<td><span data-ttu-id="8fe36-128">Host IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="8fe36-128">IPv6/IPv4 host</span></span></td>
<td><span data-ttu-id="8fe36-129">VERDADEIRO/FALSO</span><span class="sxs-lookup"><span data-stu-id="8fe36-129">TRUE / FALSE</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8fe36-130">Funções</span><span class="sxs-lookup"><span data-stu-id="8fe36-130">Functions</span></span></th>
<th><span data-ttu-id="8fe36-131">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fe36-131">Input</span></span></th>
<th><span data-ttu-id="8fe36-132">Saída</span><span class="sxs-lookup"><span data-stu-id="8fe36-132">Output</span></span></th>
<th><span data-ttu-id="8fe36-133">Motivo da alteração</span><span class="sxs-lookup"><span data-stu-id="8fe36-133">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8fe36-134">myIPAddress</span><span class="sxs-lookup"><span data-stu-id="8fe36-134">myIPAddress</span></span></td>
<td><span data-ttu-id="8fe36-135">nenhum</span><span class="sxs-lookup"><span data-stu-id="8fe36-135">none</span></span></td>
<td><span data-ttu-id="8fe36-136">Endereço IPv4</span><span class="sxs-lookup"><span data-stu-id="8fe36-136">IPv4 address</span></span></td>
<td rowspan="2"><span data-ttu-id="8fe36-137">A função ex retornará uma lista de IPv6/IPv4.</span><span class="sxs-lookup"><span data-stu-id="8fe36-137">Ex function will return a list of IPv6/IPv4.</span></span> <span data-ttu-id="8fe36-138">Necessário, uma vez que os endereços IPv6 ou IPv4 podem ter vários endereços unicast para uma única interface $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="8fe36-138">Necessary since IPv6 or IPv4 addresses can have multiple unicast addresses for a single interface ${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8fe36-139">myIPAddressEx\*</span><span class="sxs-lookup"><span data-stu-id="8fe36-139">myIPAddressEx\*</span></span></td>
<td><span data-ttu-id="8fe36-140">nenhum</span><span class="sxs-lookup"><span data-stu-id="8fe36-140">none</span></span></td>
<td><span data-ttu-id="8fe36-141">Lista de endereços IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="8fe36-141">List of IPv6/IPv4 addresses</span></span></td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8fe36-142">Funções</span><span class="sxs-lookup"><span data-stu-id="8fe36-142">Functions</span></span></th>
<th><span data-ttu-id="8fe36-143">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fe36-143">Input</span></span></th>
<th><span data-ttu-id="8fe36-144">Saída</span><span class="sxs-lookup"><span data-stu-id="8fe36-144">Output</span></span></th>
<th><span data-ttu-id="8fe36-145">Motivo da alteração</span><span class="sxs-lookup"><span data-stu-id="8fe36-145">Reason for Change</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8fe36-146">isInNet</span><span class="sxs-lookup"><span data-stu-id="8fe36-146">isInNet</span></span></td>
<td><span data-ttu-id="8fe36-147">Host, padrão de endereço IP separado por pontos, máscara de endereço IP</span><span class="sxs-lookup"><span data-stu-id="8fe36-147">Host, Dot separated IP address pattern, IP address Mask</span></span></td>
<td><span data-ttu-id="8fe36-148">VERDADEIRO/FALSO</span><span class="sxs-lookup"><span data-stu-id="8fe36-148">TRUE / FALSE</span></span></td>
<td rowspan="2"><span data-ttu-id="8fe36-149">Forneça uma forma independente da versão do IP para descobrir se um endereço IP está em uma determinada sub-rede.</span><span class="sxs-lookup"><span data-stu-id="8fe36-149">Provide an IP version agnostic way to find if an IP address is in a given subnet.</span></span> <span data-ttu-id="8fe36-150">Além disso, a notação de máscara no IPv4 é preterida. $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="8fe36-150">Also, the mask notation in IPv4 is deprecated.${REMOVE}$</span></span><br />
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="8fe36-151">isInNetEx\*</span><span class="sxs-lookup"><span data-stu-id="8fe36-151">isInNetEx\*</span></span></td>
<td><span data-ttu-id="8fe36-152">Prefixo IP do endereço IP</span><span class="sxs-lookup"><span data-stu-id="8fe36-152">IP Address IP Prefix</span></span></td>
<td><span data-ttu-id="8fe36-153">VERDADEIRO/FALSO</span><span class="sxs-lookup"><span data-stu-id="8fe36-153">TRUE / FALSE</span></span></td>

</tr>
</tbody>
</table>



 



| <span data-ttu-id="8fe36-154">Funções</span><span class="sxs-lookup"><span data-stu-id="8fe36-154">Functions</span></span>           | <span data-ttu-id="8fe36-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fe36-155">Input</span></span>                       | <span data-ttu-id="8fe36-156">Saída</span><span class="sxs-lookup"><span data-stu-id="8fe36-156">Output</span></span>                             | <span data-ttu-id="8fe36-157">Motivo da alteração</span><span class="sxs-lookup"><span data-stu-id="8fe36-157">Reason for Change</span></span>                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe36-158">sortIPAddressList\*</span><span class="sxs-lookup"><span data-stu-id="8fe36-158">sortIPAddressList\*</span></span> | <span data-ttu-id="8fe36-159">Lista de endereços IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="8fe36-159">List of IPv6/IPv4 addresses</span></span> | <span data-ttu-id="8fe36-160">Lista classificada de endereços IPv6/IPv4</span><span class="sxs-lookup"><span data-stu-id="8fe36-160">Sorted List of IPv6/IPv4 addresses</span></span> | <span data-ttu-id="8fe36-161">Não há nenhuma função herdada equivalente porque as funções herdadas retornaram apenas um único endereço IPv4, portanto, não havia necessidade de classificar.</span><span class="sxs-lookup"><span data-stu-id="8fe36-161">There is no counterpart legacy function because legacy functions only returned a single IPv4 address, therefore there was no need to sort .</span></span> |



 



| <span data-ttu-id="8fe36-162">Funções</span><span class="sxs-lookup"><span data-stu-id="8fe36-162">Functions</span></span>          | <span data-ttu-id="8fe36-163">Entrada</span><span class="sxs-lookup"><span data-stu-id="8fe36-163">Input</span></span> | <span data-ttu-id="8fe36-164">Saída</span><span class="sxs-lookup"><span data-stu-id="8fe36-164">Output</span></span>                     | <span data-ttu-id="8fe36-165">Motivo da alteração</span><span class="sxs-lookup"><span data-stu-id="8fe36-165">Reason for Change</span></span>                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe36-166">getClientVersion\*</span><span class="sxs-lookup"><span data-stu-id="8fe36-166">getClientVersion\*</span></span> | <span data-ttu-id="8fe36-167">nenhum</span><span class="sxs-lookup"><span data-stu-id="8fe36-167">none</span></span>  | <span data-ttu-id="8fe36-168">Número de versão do mecanismo WPAD</span><span class="sxs-lookup"><span data-stu-id="8fe36-168">WPAD engine version number</span></span> | <span data-ttu-id="8fe36-169">Atualmente, essa função retorna a versão 1,0.</span><span class="sxs-lookup"><span data-stu-id="8fe36-169">Currently this function returns version 1.0.</span></span> <span data-ttu-id="8fe36-170">Adicionamos essa função para permitir que os administradores de ti atualizem seu WPAD para funcionar com versões diferentes do mecanismo WPAD sem causar interrupções em sua implantação existente.</span><span class="sxs-lookup"><span data-stu-id="8fe36-170">We added this function to allow IT administrators to update their WPAD to work with different versions of the WPAD engine without causing breaks to their existent deployment.</span></span> |



 

> [!Note]  
> <span data-ttu-id="8fe36-171">Essa funcionalidade requer o Windows Internet Explorer 7 ou superior.</span><span class="sxs-lookup"><span data-stu-id="8fe36-171">This functionality requires Windows Internet Explorer 7 or greater.</span></span>

 

 

 



