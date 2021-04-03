---
title: Níveis de suporte a SNMP
description: A implementação do Microsoft WinSNMP fornece suporte a comunicações SNMP de nível 2.
ms.assetid: 9874ad9b-4eb9-4d63-816b-fe444c5b4d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92b48c930266073f10e5cb8019a7462317bd798c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084040"
---
# <a name="levels-of-snmp-support"></a><span data-ttu-id="87556-103">Níveis de suporte a SNMP</span><span class="sxs-lookup"><span data-stu-id="87556-103">Levels of SNMP Support</span></span>

<span data-ttu-id="87556-104">A implementação do Microsoft WinSNMP fornece suporte a comunicações SNMP de nível 2.</span><span class="sxs-lookup"><span data-stu-id="87556-104">The Microsoft WinSNMP implementation provides level 2 SNMP communications support.</span></span> <span data-ttu-id="87556-105">O nível 2 dá suporte ao protocolo SNMPv2 padrão de Internet Engineering Task Force (IETF), conforme definido nas RFCs 1902-1908.</span><span class="sxs-lookup"><span data-stu-id="87556-105">Level 2 supports the Internet Engineering Task Force (IETF) standard SNMPv2 protocol as defined in RFCs 1902-1908.</span></span> <span data-ttu-id="87556-106">Ele também dá suporte ao wrapper de mensagens baseado na Comunidade, conforme definido no RFC 1901 (SNMPv2C).</span><span class="sxs-lookup"><span data-stu-id="87556-106">It also supports the community-based message wrapper as defined in RFC 1901 (SNMPv2C).</span></span>

<span data-ttu-id="87556-107">O suporte de comunicações de nível 2 inclui codificação de mensagens e serviços de decodificação, anteriormente chamados de suporte de comunicações de nível 0 no WinSNMP versão 1.1 a.</span><span class="sxs-lookup"><span data-stu-id="87556-107">Level 2 communications support includes message encoding and decoding services, previously called Level 0 communications support in WinSNMP version 1.1a.</span></span> <span data-ttu-id="87556-108">O nível 2 também dá suporte a todas as operações de protocolo SNMPv1, anteriormente chamadas de suporte de comunicações de nível 1 no WinSNMP versão 1.1 a.</span><span class="sxs-lookup"><span data-stu-id="87556-108">Level 2 also supports all SNMPv1 protocol operations, previously called Level 1 communications support in WinSNMP version 1.1a.</span></span>

<span data-ttu-id="87556-109">A implementação retorna o nível máximo de comunicações SNMP que ele dá suporte em resposta a uma chamada pelo aplicativo WinSNMP para a função [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) .</span><span class="sxs-lookup"><span data-stu-id="87556-109">The implementation returns the maximum level of SNMP communications it supports in response to a call by the WinSNMP application to the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function.</span></span>

<span data-ttu-id="87556-110">Se o aplicativo WinSNMP usar a implementação para codificação e decodificação de mensagens SNMP somente, o aplicativo deverá executar as transformações necessárias que a implementação teria feito.</span><span class="sxs-lookup"><span data-stu-id="87556-110">If the WinSNMP application uses the implementation for SNMP message encoding and decoding only, the application must perform required transformations that the implementation would have performed.</span></span> <span data-ttu-id="87556-111">Isso inclui a conversão de desvios de SNMPv1 retornados por uma chamada à função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) , para interceptações de SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="87556-111">This includes translating SNMPv1 traps returned by a call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function, to SNMPv2C traps.</span></span> <span data-ttu-id="87556-112">Ele também inclui a tradução de tipos de PDU definidos por SNMPv1 para o tipo de PDU relevante definido pelo SNMPv2C, de acordo com a RFC 1908.</span><span class="sxs-lookup"><span data-stu-id="87556-112">It also includes translating PDU types defined by SNMPv1 to the relevant PDU type defined by SNMPv2C, in accordance with RFC 1908.</span></span>

 

 




