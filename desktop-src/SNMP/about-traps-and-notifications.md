---
title: Sobre interceptações e notificações
description: Um tipo de mensagem que um aplicativo de agente SNMP pode enviar para um aplicativo WinSNMP é uma mensagem assíncrona que informa ao aplicativo um evento significativo.
ms.assetid: 5249c5a5-9260-4a67-b00f-a12214012bb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2bacc6a92de2cb5a12aaf09f5caa629f28338f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822656"
---
# <a name="about-traps-and-notifications"></a><span data-ttu-id="c4f31-103">Sobre interceptações e notificações</span><span class="sxs-lookup"><span data-stu-id="c4f31-103">About Traps and Notifications</span></span>

<span data-ttu-id="c4f31-104">Um tipo de mensagem que um aplicativo de agente SNMP pode enviar para um aplicativo WinSNMP é uma mensagem assíncrona que informa ao aplicativo um evento significativo.</span><span class="sxs-lookup"><span data-stu-id="c4f31-104">One type of message an SNMP agent application can send to a WinSNMP application is an asynchronous message that informs the application of a significant event.</span></span> <span data-ttu-id="c4f31-105">Um exemplo de um evento significativo é quando um link de rede é desligado ou quando ocorre uma falha de autenticação.</span><span class="sxs-lookup"><span data-stu-id="c4f31-105">An example of a significant event is when a network link shuts down or when an authentication failure occurs.</span></span>

<span data-ttu-id="c4f31-106">Esses tipos de mensagens são chamados de interceptações em SNMPv1 e notificações sob o SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="c4f31-106">These types of messages are called traps under SNMPv1 and notifications under SNMPv2C.</span></span> <span data-ttu-id="c4f31-107">A implementação do Microsoft WinSNMP sempre traduz as armadilhas de SNMPv1 para o formato SNMPv2C, conforme definido pelo RFC 1908.</span><span class="sxs-lookup"><span data-stu-id="c4f31-107">The Microsoft WinSNMP implementation always translates SNMPv1 traps to the SNMPv2C format, as defined by RFC 1908.</span></span>

<span data-ttu-id="c4f31-108">Ao chamar a função [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) para criar uma PDU de interceptação, você pode criar apenas um PDU de interceptação de SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="c4f31-108">When you call the [**SnmpCreatePdu**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatepdu) function to create a trap PDU, you can create only an SNMPv2C trap PDU.</span></span> <span data-ttu-id="c4f31-109">O único tipo de PDU de interceptação que você pode atualizar com uma chamada para a função [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) é um PDU de interceptação de SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="c4f31-109">The only type of trap PDU you can update with a call to the [**SnmpSetPduData**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetpdudata) function is an SNMPv2C trap PDU.</span></span>

<span data-ttu-id="c4f31-110">Para obter mais informações, consulte os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4f31-110">For more information, see the following topics.</span></span>



| <span data-ttu-id="c4f31-111">Tópico</span><span class="sxs-lookup"><span data-stu-id="c4f31-111">Topic</span></span>                                                                                    | <span data-ttu-id="c4f31-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4f31-112">Description</span></span> |
|------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="c4f31-113">Convertendo interceptações de SNMPv1 para SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="c4f31-113">Translating Traps from SNMPv1 to SNMPv2C</span></span>](translating-traps-from-snmpv1-to-snmpv2c.md) |             |
| [<span data-ttu-id="c4f31-114">Formatos de interceptação</span><span class="sxs-lookup"><span data-stu-id="c4f31-114">Trap Formats</span></span>](trap-formats.md)                                                         |             |



 

 

 




