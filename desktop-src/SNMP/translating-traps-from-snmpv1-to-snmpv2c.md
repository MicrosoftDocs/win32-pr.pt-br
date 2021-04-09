---
title: Convertendo interceptações de SNMPv1 para SNMPv2C
description: Quando a implementação do Microsoft WinSNMP recebe interceptações de uma entidade operando na estrutura SNMPv1, ela converte as interceptações no formato SNMPv2C.
ms.assetid: 472f67ba-05d5-46f7-a2f1-1cef6182574e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d36870bda9b434bcc19f42332f2751020689591
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822433"
---
# <a name="translating-traps-from-snmpv1-to-snmpv2c"></a><span data-ttu-id="de24a-103">Convertendo interceptações de SNMPv1 para SNMPv2C</span><span class="sxs-lookup"><span data-stu-id="de24a-103">Translating Traps from SNMPv1 to SNMPv2C</span></span>

<span data-ttu-id="de24a-104">Quando a implementação do Microsoft WinSNMP recebe interceptações de uma entidade operando na estrutura SNMPv1, ela converte as interceptações no formato SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="de24a-104">When the Microsoft WinSNMP implementation receives traps from an entity operating under the SNMPv1 framework, it translates the traps to the SNMPv2C format.</span></span> <span data-ttu-id="de24a-105">Portanto, quando o [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) entrega uma interceptação, ele está sempre no formato SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="de24a-105">Therefore, when [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) delivers a trap it is always in the SNMPv2C format.</span></span> <span data-ttu-id="de24a-106">RFC 1908, "coexistência entre a versão 1 e a versão 2 da estrutura de gerenciamento de rede padrão da Internet", especifica as regras para a tradução do SNMPv1 para o formato de interceptação de SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="de24a-106">RFC 1908, "Coexistence between Version 1 and Version 2 of the Internet-standard Network Management Framework," specifies the rules for translating from the SNMPv1 to the SNMPv2C trap format.</span></span>

<span data-ttu-id="de24a-107">Um aplicativo WinSNMP pode verificar a última entrada de associação de variável em uma lista de associação de variável para determinar se a entrada é uma interceptação convertida de SNMPv1 para o formato SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="de24a-107">A WinSNMP application can check the last variable binding entry in a variable binding list to determine if the entry is a trap translated from the SNMPv1 to the SNMPv2C format.</span></span> <span data-ttu-id="de24a-108">Nesse caso, a última Associação de variável será sempre igual ao valor "snmpTrapEnterpriseOID. 0".</span><span class="sxs-lookup"><span data-stu-id="de24a-108">If so, the last variable binding will always be equal to the value "snmpTrapEnterpriseOID.0".</span></span>

<span data-ttu-id="de24a-109">Para obter mais informações, consulte [Gerenciando interceptações e notificações](managing-traps-and-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="de24a-109">For more information, see [Managing Traps and Notifications](managing-traps-and-notifications.md).</span></span>

 

 




