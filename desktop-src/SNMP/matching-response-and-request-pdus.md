---
title: Resposta correspondente e PDUs de solicitação
description: A ordem na qual o aplicativo WinSNMP recebe respostas SNMP pode não corresponder à ordem em que o aplicativo envia solicitações de operação SNMP.
ms.assetid: cd09cc4b-2ef6-4d2f-8f0f-b83d8df8599a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75a05f4a450ac1712d7cdd01a3c0e79dfddeb2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916449"
---
# <a name="matching-response-and-request-pdus"></a><span data-ttu-id="1e8c3-103">Resposta correspondente e PDUs de solicitação</span><span class="sxs-lookup"><span data-stu-id="1e8c3-103">Matching Response and Request PDUs</span></span>

<span data-ttu-id="1e8c3-104">A ordem na qual o aplicativo WinSNMP recebe respostas SNMP pode não corresponder à ordem em que o aplicativo envia solicitações de operação SNMP.</span><span class="sxs-lookup"><span data-stu-id="1e8c3-104">The order in which the WinSNMP application receives SNMP responses may not match the order in which the application submits SNMP operation requests.</span></span> <span data-ttu-id="1e8c3-105">Para corresponder à resposta com a solicitação, o aplicativo deve usar o campo identificador de solicitação ( **a \_ ID da solicitação**) da resposta.</span><span class="sxs-lookup"><span data-stu-id="1e8c3-105">To match the response with the request, the application must use the request identifier field (the **request\_id**) of the response.</span></span>

<span data-ttu-id="1e8c3-106">O **campo \_ ID da solicitação** é um valor numérico exclusivo que identifica a PDU.</span><span class="sxs-lookup"><span data-stu-id="1e8c3-106">The **request\_id** field is a unique numeric value that identifies the PDU.</span></span> <span data-ttu-id="1e8c3-107">Os aplicativos podem atribuir identificadores de solicitação chamando a função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) ou a função [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) .</span><span class="sxs-lookup"><span data-stu-id="1e8c3-107">Applications can assign request identifiers by calling the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function or the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function.</span></span> <span data-ttu-id="1e8c3-108">Chame a função [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) para recuperar a ID de **solicitação \_** de uma PDU.</span><span class="sxs-lookup"><span data-stu-id="1e8c3-108">Call the [**SnmpGetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetpdudata) function to retrieve a PDU's **request\_id**.</span></span>

 

 




