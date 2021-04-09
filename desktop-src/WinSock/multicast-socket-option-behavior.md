---
description: Esta página descreve o comportamento das opções de soquete multicast com base em vários Estados de configurações de opção de soquete.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Comportamento da opção de soquete multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd10094750bea59b844ad1fcdac70be0c7f9646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010486"
---
# <a name="multicast-socket-option-behavior"></a><span data-ttu-id="5b17b-103">Comportamento da opção de soquete multicast</span><span class="sxs-lookup"><span data-stu-id="5b17b-103">Multicast Socket Option Behavior</span></span>

<span data-ttu-id="5b17b-104">Esta página descreve o comportamento das opções de soquete multicast com base em vários Estados de configurações de opção de soquete.</span><span class="sxs-lookup"><span data-stu-id="5b17b-104">This page describes the behavior of multicast socket options based on various socket option settings states.</span></span>

<span data-ttu-id="5b17b-105">Por exemplo, esta página descreve o comportamento quando a opção de soquete de associação de origem de adição de IP \_ \_ \_ é definida em um soquete para o qual a \_ opção de associação de origem Adicionar IP \_ \_ já foi definida com o par de grupo/origem especificado na mesma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5b17b-105">For example, this page describes the behavior when the IP\_ADD\_SOURCE\_MEMBERSHIP socket option is set on a socket for which the IP\_ADD\_SOURCE\_MEMBERSHIP option has already been set with the specified group/source pair on the same network interface.</span></span> <span data-ttu-id="5b17b-106">É permitido chamar IP \_ Adicionar Associação de \_ origem \_ no mesmo grupo em uma interface de rede diferente.</span><span class="sxs-lookup"><span data-stu-id="5b17b-106">It is permitted to call IP\_ADD\_SOURCE\_MEMBERSHIP on the same group on a different network interface.</span></span>

<span data-ttu-id="5b17b-107">Esta página ajuda a projetar e solucionar corretamente os aplicativos de multicast do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="5b17b-107">This page assists in properly designing and troubleshooting Windows Sockets multicast applications.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="5b17b-108">Opção de soquete inicial</span><span class="sxs-lookup"><span data-stu-id="5b17b-108">Initial socket option</span></span></th>
<th><span data-ttu-id="5b17b-109">Opção de soquete subsequente em conflito</span><span class="sxs-lookup"><span data-stu-id="5b17b-109">Conflicting subsequent socket option</span></span></th>
<th><span data-ttu-id="5b17b-110">Erro retornado</span><span class="sxs-lookup"><span data-stu-id="5b17b-110">Error returned</span></span></th>
<th><span data-ttu-id="5b17b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="5b17b-111">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="5b17b-112">IP_ADD_MEMBERSHIP $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="5b17b-112">IP_ADD_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5b17b-113">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="5b17b-113">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="5b17b-114">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="5b17b-114">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="5b17b-115">Não chame IP_ADD_MEMBERSHIP com o mesmo grupo mais de uma vez na mesma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5b17b-115">Do not call IP_ADD_MEMBERSHIP with the same group more than once on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b17b-116">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="5b17b-116">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="5b17b-117">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="5b17b-117">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="5b17b-118">Não chame IP_ADD_SOURCE_MEMBERSHIP com o mesmo grupo chamado anteriormente com IP_ADD_MEMBERSHIP na mesma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5b17b-118">Do not call IP_ADD_SOURCE_MEMBERSHIP with the same group previously called with IP_ADD_MEMBERSHIP on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5b17b-119">IP_DROP_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="5b17b-119">IP_DROP_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="5b17b-120">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="5b17b-120">WSAEINVAL</span></span></td>
<td><span data-ttu-id="5b17b-121">Em vez disso, use IP_BLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="5b17b-121">Use IP_BLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5b17b-122">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="5b17b-122">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="5b17b-123">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="5b17b-123">WSAEINVAL</span></span></td>
<td><span data-ttu-id="5b17b-124">Retorna um erro ao tentar desbloquear um par de grupo/fonte que não foi bloqueado anteriormente na mesma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5b17b-124">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5b17b-125">IP_DROP_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="5b17b-125">IP_DROP_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="5b17b-126">Qualquer chamada subsequente no mesmo grupo ou par de origem/grupo</span><span class="sxs-lookup"><span data-stu-id="5b17b-126">Any subsequent call on the same group or group/source pair</span></span></td>
<td><span data-ttu-id="5b17b-127">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="5b17b-127">WSAEINVAL</span></span></td>
<td><span data-ttu-id="5b17b-128">Fazer chamadas de opção de soquete em um grupo ou par de origem que não está atualmente na lista de inclusão (devido à remoção de associação, ou de outra forma) resulta em um erro.</span><span class="sxs-lookup"><span data-stu-id="5b17b-128">Making socket option calls on a group or group/source pair not currently in the inclusion list (due to dropping membership, or otherwise) results in an error.</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="5b17b-129">IP_ADD_SOURCE_MEMBERSHIP $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="5b17b-129">IP_ADD_SOURCE_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5b17b-130">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="5b17b-130">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="5b17b-131">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="5b17b-131">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="5b17b-132">Não chame IP_ADD_MEMBERSHIP com o mesmo grupo chamado anteriormente com IP_ADD_SOURCE_MEMBERSHIP na mesma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5b17b-132">Do not call IP_ADD_MEMBERSHIP with the same group previously called with IP_ADD_SOURCE_MEMBERSHIP on the same network interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b17b-133">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="5b17b-133">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="5b17b-134">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="5b17b-134">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="5b17b-135">Não chame IP_ADD_SOURCE_MEMBERSHIP com o mesmo par de grupo/fonte chamado anteriormente com IP_ADD_SOURCE_MEMBERSHIP na mesma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5b17b-135">Do not call IP_ADD_SOURCE_MEMBERSHIP with the same group/source pair previously called with IP_ADD_SOURCE_MEMBERSHIP on the same network interface.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5b17b-136">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="5b17b-136">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="5b17b-137">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="5b17b-137">WSAEINVAL</span></span></td>
<td><span data-ttu-id="5b17b-138">Retorna um erro ao tentar desbloquear um par de grupo/fonte que não foi bloqueado anteriormente na mesma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5b17b-138">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="5b17b-139">IP_DROP_SOURCE_MEMBERSHIP $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="5b17b-139">IP_DROP_SOURCE_MEMBERSHIP${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5b17b-140">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="5b17b-140">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="5b17b-141">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="5b17b-141">WSAEINVAL</span></span></td>
<td><span data-ttu-id="5b17b-142">Retorna um erro ao tentar desbloquear um par de grupo/fonte que não foi bloqueado anteriormente na mesma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5b17b-142">Returns an error when attempting to unblock a group/source pair that has not previously been blocked on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b17b-143">IP_DROP_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="5b17b-143">IP_DROP_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="5b17b-144">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="5b17b-144">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="5b17b-145">Retorna um erro ao tentar descartar um par de grupo/fonte que não está na lista de inclusão na mesma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5b17b-145">Returns an error when attempting to drop a group/source pair that is not in the inclusion list on the same network interface.</span></span></td>

</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="5b17b-146">IP_BLOCK_SOURCE $ {REMOVER} $</span><span class="sxs-lookup"><span data-stu-id="5b17b-146">IP_BLOCK_SOURCE${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="5b17b-147">IP_BLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="5b17b-147">IP_BLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="5b17b-148">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="5b17b-148">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="5b17b-149">Retorna um erro ao tentar bloquear um par de grupo/fonte que já está bloqueado na mesma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5b17b-149">Returns an error when attempting to block a group/source pair that is already blocked on the same network interface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b17b-150">IP_ADD_SOURCE_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="5b17b-150">IP_ADD_SOURCE_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="5b17b-151">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="5b17b-151">WSAEINVAL</span></span></td>
<td><span data-ttu-id="5b17b-152">Em vez disso, use IP_UNBLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="5b17b-152">Use IP_UNBLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="5b17b-153">IP_ADD_MEMBERSHIP</span><span class="sxs-lookup"><span data-stu-id="5b17b-153">IP_ADD_MEMBERSHIP</span></span></td>
<td><span data-ttu-id="5b17b-154">WSAEINVAL</span><span class="sxs-lookup"><span data-stu-id="5b17b-154">WSAEINVAL</span></span></td>
<td><span data-ttu-id="5b17b-155">Em vez disso, use IP_UNBLOCK_SOURCE.</span><span class="sxs-lookup"><span data-stu-id="5b17b-155">Use IP_UNBLOCK_SOURCE instead.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="5b17b-156">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="5b17b-156">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="5b17b-157">IP_UNBLOCK_SOURCE</span><span class="sxs-lookup"><span data-stu-id="5b17b-157">IP_UNBLOCK_SOURCE</span></span></td>
<td><span data-ttu-id="5b17b-158">WSAEADDRNOTAVAIL</span><span class="sxs-lookup"><span data-stu-id="5b17b-158">WSAEADDRNOTAVAIL</span></span></td>
<td><span data-ttu-id="5b17b-159">Retorna um erro ao tentar desbloquear um par de grupo/fonte que não está na lista bloqueada na mesma interface de rede.</span><span class="sxs-lookup"><span data-stu-id="5b17b-159">Returns an error when attempting to unblock a group/source pair that is not in the blocked list on the same network interface.</span></span></td>
</tr>
</tbody>
</table>



 

 

 



