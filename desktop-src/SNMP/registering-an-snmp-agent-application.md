---
title: Registrando um aplicativo de agente SNMP
description: Além das operações do Gerenciador SNMP, a versão de API WinSNMP 2,0 também dá suporte a operações de agente SNMP.
ms.assetid: 473560b5-4611-410e-aeae-764c9c76e765
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40922469c52e33e4b5c2f408c1c107b6784529f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916447"
---
# <a name="registering-an-snmp-agent-application"></a><span data-ttu-id="f6020-103">Registrando um aplicativo de agente SNMP</span><span class="sxs-lookup"><span data-stu-id="f6020-103">Registering an SNMP Agent Application</span></span>

<span data-ttu-id="f6020-104">Além das operações do Gerenciador SNMP, a versão de API WinSNMP 2,0 também dá suporte a operações de agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="f6020-104">In addition to SNMP manager operations, the WinSNMP API version 2.0 also supports SNMP agent operations.</span></span>

<span data-ttu-id="f6020-105">Para registrar um aplicativo WinSNMP como um agente SNMP, o aplicativo pode chamar a função [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) .</span><span class="sxs-lookup"><span data-stu-id="f6020-105">To register a WinSNMP application as an SNMP agent, the application can call the [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) function.</span></span> <span data-ttu-id="f6020-106">Essa função informa à implementação do Microsoft WinSNMP que uma entidade SNMP atuará na função de um agente SNMP.</span><span class="sxs-lookup"><span data-stu-id="f6020-106">This function informs the Microsoft WinSNMP implementation that an SNMP entity will be acting in the role of an SNMP agent.</span></span> <span data-ttu-id="f6020-107">O aplicativo também pode chamar **SnmpListen** para informar a implementação quando ela não funcionará mais como um agente.</span><span class="sxs-lookup"><span data-stu-id="f6020-107">The application can also call **SnmpListen** to inform the implementation when it will no longer be acting as an agent.</span></span>

<span data-ttu-id="f6020-108">Se um aplicativo chamar a função [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) e passar o valor snmpapi no \_ parâmetro *lStatus* , ocorrerão as seguintes ações:</span><span class="sxs-lookup"><span data-stu-id="f6020-108">If an application calls the [**SnmpListen**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmplisten) function and passes the value SNMPAPI\_ON in the *lStatus* parameter, the following actions occur:</span></span>

1.  <span data-ttu-id="f6020-109">A entidade que estará funcionando em uma função de agente SNMP será vinculada à sua porta atribuída e "escuta" para solicitações de mensagens SNMP de entrada.</span><span class="sxs-lookup"><span data-stu-id="f6020-109">The entity that will be functioning in an SNMP agent role binds to its assigned port, and "listens" for incoming SNMP message requests.</span></span>
2.  <span data-ttu-id="f6020-110">O agente usa a lógica específica do aplicativo para processar cada solicitação SNMP.</span><span class="sxs-lookup"><span data-stu-id="f6020-110">The agent uses application-specific logic to process each SNMP request.</span></span>
3.  <span data-ttu-id="f6020-111">O agente forma as respostas apropriadas a cada solicitação.</span><span class="sxs-lookup"><span data-stu-id="f6020-111">The agent forms appropriate responses to each request.</span></span>
4.  <span data-ttu-id="f6020-112">O agente transmite a resposta para a entidade solicitante chamando a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) .</span><span class="sxs-lookup"><span data-stu-id="f6020-112">The agent transmits the response to the requesting entity by calling the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function.</span></span> <span data-ttu-id="f6020-113">Quando o agente chama **SnmpSendMsg**, ele especifica o endereço do agente no parâmetro *srcEntity* e o endereço da entidade Gerenciador remoto no parâmetro *dstEntity* .</span><span class="sxs-lookup"><span data-stu-id="f6020-113">When the agent calls **SnmpSendMsg**, it specifies the address of the agent in the *srcEntity* parameter, and the address of the remote manager entity in the *dstEntity* parameter.</span></span> <span data-ttu-id="f6020-114">(Esses valores são o inverso dos valores que a entidade de agente recebeu nesses parâmetros quando ele chamou a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para recuperar uma solicitação de SNMP.)</span><span class="sxs-lookup"><span data-stu-id="f6020-114">(These values are the reverse of the values the agent entity received in these parameters when it called the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function to retrieve an SNMP request.)</span></span>

<span data-ttu-id="f6020-115">Para obter mais informações sobre aplicativos de gerenciamento SNMP e aplicativos de agente, consulte [sobre SNMP](about-snmp.md).</span><span class="sxs-lookup"><span data-stu-id="f6020-115">For more information about SNMP management applications and agent applications, see [About SNMP](about-snmp.md).</span></span>

 

 




