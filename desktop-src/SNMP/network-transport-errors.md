---
title: Erros de transporte de rede
description: A implementação do Microsoft WinSNMP pode detectar um erro de transporte de rede depois de transmitir uma mensagem SNMP.
ms.assetid: 2ff535b1-76cb-42aa-baeb-14c1a1bc41ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cf6b7610fbfe8d19a375bd3e3146263b9e9f0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823924"
---
# <a name="network-transport-errors"></a><span data-ttu-id="1a317-103">Erros de transporte de rede</span><span class="sxs-lookup"><span data-stu-id="1a317-103">Network Transport Errors</span></span>

<span data-ttu-id="1a317-104">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="1a317-104">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1a317-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="1a317-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="1a317-106">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="1a317-106">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="1a317-107">A implementação do Microsoft WinSNMP pode detectar um erro de transporte de rede depois de transmitir uma mensagem SNMP.</span><span class="sxs-lookup"><span data-stu-id="1a317-107">The Microsoft WinSNMP implementation can detect a network transport error after it transmits an SNMP message.</span></span> <span data-ttu-id="1a317-108">Quando isso ocorre, a implementação envia uma notificação de recebimento de dados para a sessão WinSNMP que iniciou a solicitação de comunicação.</span><span class="sxs-lookup"><span data-stu-id="1a317-108">When this occurs, the implementation sends a data receipt notification to the WinSNMP session that initiated the communication request.</span></span> <span data-ttu-id="1a317-109">A implementação também retorna falha de SNMPAPI \_ na próxima chamada para a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) para a sessão.</span><span class="sxs-lookup"><span data-stu-id="1a317-109">The implementation also returns SNMPAPI\_FAILURE on the next call to the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function for the session.</span></span> <span data-ttu-id="1a317-110">A função **SnmpRecvMsg** falha com um código de erro estendido que indica um erro de camada de transporte de rede.</span><span class="sxs-lookup"><span data-stu-id="1a317-110">The **SnmpRecvMsg** function fails with an extended error code that indicates a network transport layer error.</span></span>

<span data-ttu-id="1a317-111">Para obter uma lista de erros de camada de transporte específicos, consulte as páginas de referência para as funções [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg)e [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) .</span><span class="sxs-lookup"><span data-stu-id="1a317-111">For a list of specific transport layer errors, see the reference pages for the [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister), [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg), and [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) functions.</span></span>

 

 