---
title: Convertendo solicitações de mensagem
description: Este tópico descreve o processo de conversão de solicitações de SNMPv1 em solicitações de SNMPv2.
ms.assetid: 7671ae36-99b1-47b1-930a-f376021d56a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2a67ecb78b16f818ea50158faf827e19d4eba5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498641"
---
# <a name="translating-message-requests"></a><span data-ttu-id="12788-103">Convertendo solicitações de mensagem</span><span class="sxs-lookup"><span data-stu-id="12788-103">Translating Message Requests</span></span>

<span data-ttu-id="12788-104">Este tópico descreve o processo de conversão de solicitações de SNMPv1 em solicitações de SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="12788-104">This topic describes the process of translating SNMPv1 requests into SNMPv2 requests.</span></span>

<span data-ttu-id="12788-105">Se um aplicativo de WinSNMP solicitar uma funcionalidade que esteja disponível na estrutura do SNMP versão 2C (SNMPv2C), mas a entidade de destino der suporte apenas ao SNMPv1 (SNMP versão 1 Framework), a implementação do Microsoft WinSNMP tentará converter a solicitação para o formato SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="12788-105">If a WinSNMP application requests functionality that is available under the SNMP version 2C framework (SNMPv2C), but the target entity supports only the SNMP version 1 framework (SNMPv1), the Microsoft WinSNMP implementation attempts to translate the request to the SNMPv1 format.</span></span> <span data-ttu-id="12788-106">Para fazer isso, a implementação usa os procedimentos definidos na RFC 1908, "coexistência entre a versão 1 e a versão 2 do Internet-Standard estrutura de gerenciamento de rede".</span><span class="sxs-lookup"><span data-stu-id="12788-106">To do this, the implementation uses the procedures defined in RFC 1908, "Coexistence Between Version 1 and Version 2 of the Internet-Standard Network Management Framework."</span></span> <span data-ttu-id="12788-107">Se a conversão não for possível, a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) falhará com o código de erro estendido snmpapi \_ operação \_ inválida.</span><span class="sxs-lookup"><span data-stu-id="12788-107">If translation is not possible, the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function fails with the extended error code SNMPAPI\_OPERATION\_INVALID.</span></span>

 

 




