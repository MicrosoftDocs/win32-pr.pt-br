---
title: Alterando a política de retransmissão
description: A implementação do Microsoft WinSNMP fornece suporte à política de retransmissão, armazenando um valor de tempo limite e uma contagem de repetição para o aplicativo WinSNMP em um banco de dados.
ms.assetid: 9ab45adc-12b7-40b1-8fec-40bf04302f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9f21fc479517b8844e9c1db75834b5b1c02edc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822654"
---
# <a name="changing-the-retransmission-policy"></a><span data-ttu-id="50ad3-103">Alterando a política de retransmissão</span><span class="sxs-lookup"><span data-stu-id="50ad3-103">Changing the Retransmission Policy</span></span>

<span data-ttu-id="50ad3-104">A implementação do Microsoft WinSNMP fornece suporte à política de retransmissão, armazenando um valor de tempo limite e uma contagem de repetição para o aplicativo WinSNMP em um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="50ad3-104">The Microsoft WinSNMP implementation provides retransmission policy support by storing a time-out value and a retry count for the WinSNMP application in a database.</span></span> <span data-ttu-id="50ad3-105">A implementação armazena valores para entidades de destino individuais.</span><span class="sxs-lookup"><span data-stu-id="50ad3-105">The implementation stores values for individual destination entities.</span></span> <span data-ttu-id="50ad3-106">A implementação inicialmente fornece valores padrão para esses elementos, mas um aplicativo pode adicionar ou modificar valores para entidades individuais.</span><span class="sxs-lookup"><span data-stu-id="50ad3-106">The implementation initially supplies default values for these elements, but an application can add or modify values for individual entities.</span></span>

<span data-ttu-id="50ad3-107">Uma chamada para as funções [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) e [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) retorna os valores de tempo limite e de contagem de repetição para uma entidade de destino específica.</span><span class="sxs-lookup"><span data-stu-id="50ad3-107">A call to the [**SnmpGetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgettimeout) and [**SnmpGetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetretry) functions returns the time-out and retry count values for a specific destination entity.</span></span> <span data-ttu-id="50ad3-108">Para alterar o valor de tempo limite, um aplicativo WinSNMP deve chamar a função [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) .</span><span class="sxs-lookup"><span data-stu-id="50ad3-108">To change the time-out value, a WinSNMP application must call the [**SnmpSetTimeout**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsettimeout) function.</span></span> <span data-ttu-id="50ad3-109">Para alterar o valor de contagem de repetição, o aplicativo deve chamar a função [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) .</span><span class="sxs-lookup"><span data-stu-id="50ad3-109">To change the retry count value the application must call the [**SnmpSetRetry**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsetretry) function.</span></span> <span data-ttu-id="50ad3-110">As configurações atualizadas afetam as novas solicitações de mensagens SNMP para a entidade de destino.</span><span class="sxs-lookup"><span data-stu-id="50ad3-110">The updated settings affect new SNMP message requests to the destination entity.</span></span>

 

 




