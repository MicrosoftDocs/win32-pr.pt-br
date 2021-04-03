---
title: Novidades no SNMP
description: O SNMP dá suporte ao uso de IPv6 a partir do Windows Vista.
ms.assetid: 38d71c0a-8de1-45a7-958c-aa44411451bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913f71cdf0b23800340f2c43f7b7fa22f45883a2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641720"
---
# <a name="new-in-snmp"></a><span data-ttu-id="6d7b2-103">Novidades no SNMP</span><span class="sxs-lookup"><span data-stu-id="6d7b2-103">New in SNMP</span></span>

<span data-ttu-id="6d7b2-104">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="6d7b2-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6d7b2-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="6d7b2-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="6d7b2-106">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="6d7b2-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="6d7b2-107">O SNMP dá suporte ao uso de IPv6 a partir do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6d7b2-107">SNMP supports the use of IPv6 starting with Windows Vista.</span></span> <span data-ttu-id="6d7b2-108">No entanto, o SNMP dá suporte a IPv6 somente para redes que executam o Windows Server 2008 e o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6d7b2-108">However, SNMP supports IPv6 only for networks running Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="6d7b2-109">Isso ocorre porque o SNMP requer a pilha de protocolos atualizada disponível nesses sistemas operacionais para seu suporte IPv6.</span><span class="sxs-lookup"><span data-stu-id="6d7b2-109">This is because SNMP requires the updated protocol stack available in these operating systems for its IPv6 support.</span></span>

<span data-ttu-id="6d7b2-110">A menos que sua rede seja exclusivamente uma rede do Windows Server 2008, as comunicações IPv6 falharão, mesmo que uma pilha de protocolo IPv6 seja instalada separadamente nesses computadores que executam versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="6d7b2-110">Unless your network is solely a Windows Server 2008 network, IPv6 communications will fail, even if an IPv6 protocol stack is separately installed on those computers that run earlier versions of Windows.</span></span> <span data-ttu-id="6d7b2-111">Por exemplo, agentes SNMP executados no Windows Server 2003, ou Windows XP ou Windows 2000, respondem somente a consultas feitas em seus endereços IPv4.</span><span class="sxs-lookup"><span data-stu-id="6d7b2-111">For example, SNMP agents that run on Windows Server 2003, or Windows XP, or Windows 2000, respond only to queries that are made to their IPv4 addresses.</span></span>

 

 