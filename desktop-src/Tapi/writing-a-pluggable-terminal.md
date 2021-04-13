---
description: Normalmente, um MSP (provedor de serviços de mídia) implementa a criação de terminal.
ms.assetid: 203fccc0-aa5a-4ec3-97d3-546c36018d52
title: Gravando um terminal conectável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cbfe2da0c121fcee820d47fd57216840d23c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501908"
---
# <a name="writing-a-pluggable-terminal"></a><span data-ttu-id="013a2-103">Gravando um terminal conectável</span><span class="sxs-lookup"><span data-stu-id="013a2-103">Writing a Pluggable Terminal</span></span>

<span data-ttu-id="013a2-104">Normalmente, um MSP (provedor de serviços de mídia) implementa a criação de terminal.</span><span class="sxs-lookup"><span data-stu-id="013a2-104">Normally, a media service provider (MSP) implements terminal creation.</span></span> <span data-ttu-id="013a2-105">A partir do Windows 2000 SP1, a TAPI 3 inclui terminais conectáveis para permitir que um aplicativo implemente a criação de terminal.</span><span class="sxs-lookup"><span data-stu-id="013a2-105">Starting with Windows 2000 SP1, TAPI 3 includes pluggable terminals to allow an application to implement terminal creation.</span></span> <span data-ttu-id="013a2-106">Consulte a visão geral sobre como [implementar terminais conectáveis](implementing-pluggable-terminals.md) para obter informações adicionais sobre como usar esses terminais.</span><span class="sxs-lookup"><span data-stu-id="013a2-106">Please see the overview on [implementing pluggable terminals](implementing-pluggable-terminals.md) for additional information on using these terminals.</span></span>

<span data-ttu-id="013a2-107">Você não deve usar os terminais conectáveis rotineiramente porque os recursos completos de um terminal só estarão disponíveis quando um MSP estiver totalmente ciente dele.</span><span class="sxs-lookup"><span data-stu-id="013a2-107">You should not use pluggable terminals routinely because the full capabilities of a terminal will only be available when an MSP is fully aware of it.</span></span> <span data-ttu-id="013a2-108">Além disso, você não deve tentar implementar terminais conectáveis, a menos que já esteja familiarizado com a gravação de provedores de serviços de mídia.</span><span class="sxs-lookup"><span data-stu-id="013a2-108">Further, you should not attempt to implement pluggable terminals unless you are already familiar with writing media service providers.</span></span> <span data-ttu-id="013a2-109">As técnicas e os possíveis problemas envolvidos são bastante semelhantes.</span><span class="sxs-lookup"><span data-stu-id="013a2-109">The techniques and potential problems involved are quite similar.</span></span>

<span data-ttu-id="013a2-110">A provisão para um caso especial de terminal conectável existe atualmente para a situação de um servidor de conferência que precisa adicionar clientes não Windows 2000 SP1 ou não multicast H. 323 a conferências de multicast/IP multipartes de antivírus 3.</span><span class="sxs-lookup"><span data-stu-id="013a2-110">Provision for a special case of pluggable terminal currently exists for the situation of a conferencing server that needs to add non-Windows 2000 SP1 or nonmulticast H.323 clients to TAPI 3 multiparty SDP/IP multicast conferences.</span></span>

 

 



