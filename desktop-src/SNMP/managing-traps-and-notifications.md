---
title: Gerenciando interceptações e notificações
description: O aplicativo WinSNMP deve se registrar para receber interceptações e notificações chamando a função SnmpRegister com SNMPAPI \_ em. O aplicativo pode cancelar o registro e desabilitar interceptações e notificações chamando a função com SNMPAPI \_ off.
ms.assetid: 2bccba35-bf5c-4e5c-94e4-59980f2b9776
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e3a2d9fed1f7c34dd8191550d1dbc68ed984e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822876"
---
# <a name="managing-traps-and-notifications"></a><span data-ttu-id="107c7-104">Gerenciando interceptações e notificações</span><span class="sxs-lookup"><span data-stu-id="107c7-104">Managing Traps and Notifications</span></span>

<span data-ttu-id="107c7-105">O aplicativo WinSNMP deve se registrar para receber interceptações e notificações chamando a função [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) com snmpapi \_ em.</span><span class="sxs-lookup"><span data-stu-id="107c7-105">The WinSNMP application must register to receive traps and notifications by calling the [**SnmpRegister**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpregister) function with SNMPAPI\_ON.</span></span> <span data-ttu-id="107c7-106">O aplicativo pode cancelar o registro e desabilitar interceptações e notificações chamando a função com SNMPAPI \_ off.</span><span class="sxs-lookup"><span data-stu-id="107c7-106">The application can unregister and disable traps and notifications by calling the function with SNMPAPI\_OFF.</span></span>

<span data-ttu-id="107c7-107">Várias opções estão disponíveis quando o aplicativo chama **SnmpRegister**.</span><span class="sxs-lookup"><span data-stu-id="107c7-107">Several options are available when the application calls **SnmpRegister**.</span></span> <span data-ttu-id="107c7-108">O aplicativo pode registrar ou cancelar o registro para as seguintes interceptações e notificações:</span><span class="sxs-lookup"><span data-stu-id="107c7-108">The application can register or unregister for the following traps and notifications:</span></span>

-   <span data-ttu-id="107c7-109">Um tipo de interceptação ou notificação</span><span class="sxs-lookup"><span data-stu-id="107c7-109">One type of trap or notification</span></span>
-   <span data-ttu-id="107c7-110">Todas as interceptações e notificações</span><span class="sxs-lookup"><span data-stu-id="107c7-110">All traps and notifications</span></span>
-   <span data-ttu-id="107c7-111">Todas as fontes de solicitações de interceptação e notificação</span><span class="sxs-lookup"><span data-stu-id="107c7-111">All sources of trap and notification requests</span></span>
-   <span data-ttu-id="107c7-112">Interceptações e notificações de todas as entidades de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="107c7-112">Traps and notifications from all management entities</span></span>
-   <span data-ttu-id="107c7-113">Interceptações e notificações para cada contexto</span><span class="sxs-lookup"><span data-stu-id="107c7-113">Traps and notifications for every context</span></span>

<span data-ttu-id="107c7-114">Para registrar e receber uma interceptação predefinida ou um tipo de notificação, o aplicativo deve definir um identificador de objeto (uma estrutura [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) ) para cada tipo predefinido.</span><span class="sxs-lookup"><span data-stu-id="107c7-114">To register and receive a predefined trap or notification type, the application must define an object identifier (an [**smiOID**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioid) structure) for each predefined type.</span></span> <span data-ttu-id="107c7-115">A estrutura deve conter uma sequência de correspondência de padrões para o tipo de interceptação ou notificação.</span><span class="sxs-lookup"><span data-stu-id="107c7-115">The structure must contain a pattern-matching sequence for the type of trap or notification.</span></span> <span data-ttu-id="107c7-116">A RFC 1907, "base de informações de gerenciamento para a versão 2 do protocolo SNMPv2 (Simple Network Management Protocol)", define os identificadores de objeto de interceptação e de notificação.</span><span class="sxs-lookup"><span data-stu-id="107c7-116">RFC 1907, "Management Information Base for Version 2 of the Simple Network Management Protocol (SNMPv2)," defines trap and notification object identifiers.</span></span>

<span data-ttu-id="107c7-117">Para recuperar dados de interceptação pendentes e notificações para uma sessão de WinSNMP, um aplicativo WinSNMP deve chamar a função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) com o identificador de sessão retornado pela função [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) .</span><span class="sxs-lookup"><span data-stu-id="107c7-117">To retrieve outstanding trap data and notifications for a WinSNMP session, a WinSNMP application must call the [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function with the session handle returned by the [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function.</span></span>

<span data-ttu-id="107c7-118">Para obter mais informações, consulte [enviando mensagens SNMP](sending-snmp-messages.md) e [recebendo mensagens SNMP](receiving-snmp-messages.md).</span><span class="sxs-lookup"><span data-stu-id="107c7-118">For more information, see [Sending SNMP Messages](sending-snmp-messages.md) and [Receiving SNMP Messages](receiving-snmp-messages.md).</span></span> <span data-ttu-id="107c7-119">Para obter informações adicionais sobre alocação e desalocação de recursos para interceptações e notificações, consulte [alocando objetos de memória WinSNMP](allocating-winsnmp-memory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="107c7-119">For additional information about allocation and deallocation of resources for traps and notifications, see [Allocating WinSNMP Memory Objects](allocating-winsnmp-memory-objects.md).</span></span>

 

 




