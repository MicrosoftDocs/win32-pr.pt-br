---
title: Ativando e desativando a retransmissão
description: Um aplicativo pode definir o modo de retransmissão com uma chamada para a função SnmpSetRetransmitMode. O novo modo de retransmissão se aplica às chamadas subsequentes para a função SnmpSendMsg.
ms.assetid: 0e167014-2703-4942-91f0-c60a5c0d8e12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24936bcc90ed0debf66eb9040334fff3bceee2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105779965"
---
# <a name="turning-retransmission-on-and-off"></a><span data-ttu-id="9be10-104">Ativando e desativando a retransmissão</span><span class="sxs-lookup"><span data-stu-id="9be10-104">Turning Retransmission On and Off</span></span>

<span data-ttu-id="9be10-105">Um aplicativo pode definir o modo de retransmissão com uma chamada para a função [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) .</span><span class="sxs-lookup"><span data-stu-id="9be10-105">An application can set the retransmission mode with a call to the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function.</span></span> <span data-ttu-id="9be10-106">O novo modo de retransmissão se aplica às chamadas subsequentes para a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .</span><span class="sxs-lookup"><span data-stu-id="9be10-106">The new retransmission mode applies to subsequent calls to the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function.</span></span>

<span data-ttu-id="9be10-107">Quando o aplicativo chama **SnmpSetRetransmitMode** com o valor do modo de retransmissão snmpapi \_ , a implementação do Microsoft WinSNMP começa a execução da política de retransmissão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9be10-107">When the application calls **SnmpSetRetransmitMode** with the retransmission mode value SNMPAPI\_ON, the Microsoft WinSNMP implementation begins execution of the application's retransmission policy.</span></span> <span data-ttu-id="9be10-108">O novo modo de retransmissão não afeta mensagens do SNMP pendentes.</span><span class="sxs-lookup"><span data-stu-id="9be10-108">The new retransmission mode does not affect outstanding SNMP messages.</span></span> <span data-ttu-id="9be10-109">Uma mensagem pendente é aquela que não tem resposta no momento em que o aplicativo altera o modo de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="9be10-109">An outstanding message is one that has no response at the time the application changes the retransmission mode.</span></span>

<span data-ttu-id="9be10-110">Quando o aplicativo WinSNMP chama a função [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) com o valor de modo de retransmissão snmpapi \_ desativado, a implementação para de executar a política de retransmissão.</span><span class="sxs-lookup"><span data-stu-id="9be10-110">When the WinSNMP application calls the [**SnmpSetRetransmitMode**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretransmitmode) function with the retransmission mode value SNMPAPI\_OFF, the implementation stops executing the retransmission policy.</span></span> <span data-ttu-id="9be10-111">A implementação cancela as tentativas de retransmissão para mensagens SNMP pendentes.</span><span class="sxs-lookup"><span data-stu-id="9be10-111">The implementation cancels retransmission attempts for outstanding SNMP messages.</span></span> <span data-ttu-id="9be10-112">Isso ocorre porque talvez não seja possível que a implementação manipule todas as solicitações e operações SNMP pendentes, além de novas solicitações, antes que um contador de tempo limite de aplicativo ou de repetição sinalize um evento.</span><span class="sxs-lookup"><span data-stu-id="9be10-112">This is because it may not be possible for the implementation to handle all outstanding SNMP requests and operations plus new requests, before an application time-out or retry counter signals an event.</span></span>

 

 




