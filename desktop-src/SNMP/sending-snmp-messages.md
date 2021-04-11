---
title: Enviando mensagens SNMP
description: Um aplicativo WinSNMP inicia uma solicitação de transmissão enviando uma mensagem SNMP. As mensagens SNMP incluem uma unidade de dados do protocolo SNMP. Para obter mais informações, consulte trabalhando com unidades de dados de protocolo.
ms.assetid: a7439cd2-af13-4e2b-a0a6-5cc271a011e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613ac7079f7dc206280b8d8077d2d5ea8db7151c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292526"
---
# <a name="sending-snmp-messages"></a><span data-ttu-id="a959b-105">Enviando mensagens SNMP</span><span class="sxs-lookup"><span data-stu-id="a959b-105">Sending SNMP Messages</span></span>

<span data-ttu-id="a959b-106">Um aplicativo WinSNMP inicia uma solicitação de transmissão enviando uma mensagem SNMP.</span><span class="sxs-lookup"><span data-stu-id="a959b-106">A WinSNMP application initiates a transmission request by sending an SNMP message.</span></span> <span data-ttu-id="a959b-107">As mensagens SNMP incluem uma unidade de dados do protocolo SNMP.</span><span class="sxs-lookup"><span data-stu-id="a959b-107">SNMP messages include an SNMP protocol data unit.</span></span> <span data-ttu-id="a959b-108">Para obter mais informações, consulte [trabalhando com unidades de dados de protocolo](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="a959b-108">For more information, see [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>

<span data-ttu-id="a959b-109">Um aplicativo WinSNMP deve chamar a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) para solicitar que a implementação do Microsoft WinSNMP transmita a PDU, com os outros elementos de mensagem necessários definidos pela RFC relevante.</span><span class="sxs-lookup"><span data-stu-id="a959b-109">A WinSNMP application must call the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function to request that the Microsoft WinSNMP implementation transmit the PDU, with the other required message elements defined by the relevant RFC.</span></span> <span data-ttu-id="a959b-110">Além da entidade de destino, o aplicativo deve especificar a entidade de origem e um contexto para a solicitação.</span><span class="sxs-lookup"><span data-stu-id="a959b-110">In addition to the destination entity, the application must specify the source entity and a context for the request.</span></span> <span data-ttu-id="a959b-111">A função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) é executada de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="a959b-111">The [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function executes asynchronously.</span></span>

<span data-ttu-id="a959b-112">O aplicativo WinSNMP deve chamar a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar a resposta a uma solicitação **SnmpSendMsg** .</span><span class="sxs-lookup"><span data-stu-id="a959b-112">The WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve the response to an **SnmpSendMsg** request.</span></span>

<span data-ttu-id="a959b-113">A implementação verifica a validade da PDU e os outros elementos de mensagem quando um aplicativo chama [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span><span class="sxs-lookup"><span data-stu-id="a959b-113">The implementation verifies the validity of the PDU and the other message elements when an application calls [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg).</span></span>

 

 




