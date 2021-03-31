---
title: Criando uma PDU
description: Para criar e inicializar uma PDU, um aplicativo WinSNMP chama a função SnmpCreatePdu.
ms.assetid: 7f02a2c6-19bc-456f-bf04-3297d19000f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aba7a4ca42e2a5d63169d2521410773ca018c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822653"
---
# <a name="creating-a-pdu"></a><span data-ttu-id="0a692-103">Criando uma PDU</span><span class="sxs-lookup"><span data-stu-id="0a692-103">Creating a PDU</span></span>

<span data-ttu-id="0a692-104">Para criar e inicializar uma PDU, um aplicativo WinSNMP chama a função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) .</span><span class="sxs-lookup"><span data-stu-id="0a692-104">To create and initialize a PDU a WinSNMP application calls the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function.</span></span> <span data-ttu-id="0a692-105">O aplicativo deve chamar **SnmpCreatePdu** antes de chamar a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) para solicitar que a implementação do Microsoft WINSNMP transmita uma PDU.</span><span class="sxs-lookup"><span data-stu-id="0a692-105">The application must call **SnmpCreatePdu** before it calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function to request that the Microsoft WinSNMP implementation transmit a PDU.</span></span> <span data-ttu-id="0a692-106">O aplicativo também deve chamar [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) antes de chamar a função [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) para solicitar codificação de uma mensagem SNMP.</span><span class="sxs-lookup"><span data-stu-id="0a692-106">The application must also call [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) before it calls the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function to request encoding of an SNMP message.</span></span>

<span data-ttu-id="0a692-107">O aplicativo deve chamar a função [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) para liberar os recursos que a função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) aloca para uma nova PDUs.</span><span class="sxs-lookup"><span data-stu-id="0a692-107">The application must call the [**SnmpFreePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpfreepdu) function to release the resources that the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function allocates for new PDUs.</span></span>

 

 




