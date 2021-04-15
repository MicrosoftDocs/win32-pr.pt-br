---
description: Os provedores de eventos SNMP recebem pacotes de eventos SNMP da pilha WINSNMP e convertem as informações incluídas nos pacotes em eventos WMI.
ms.assetid: 4ae0a734-39b0-4418-b55c-6d8f093806a8
ms.tgt_platform: multiple
title: Escolhendo entre provedores de eventos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dabd8f6d432025406a5faecc3ace423cd6671e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768335"
---
# <a name="choosing-between-snmp-event-providers"></a><span data-ttu-id="fa6c7-103">Escolhendo entre provedores de eventos SNMP</span><span class="sxs-lookup"><span data-stu-id="fa6c7-103">Choosing Between SNMP Event Providers</span></span>

<span data-ttu-id="fa6c7-104">Os provedores de eventos SNMP recebem pacotes de eventos SNMP da pilha WINSNMP e convertem as informações incluídas nos pacotes em eventos WMI.</span><span class="sxs-lookup"><span data-stu-id="fa6c7-104">SNMP event providers receive SNMP event packets from the WINSNMP stack and translate the information included in the packets into WMI events.</span></span>

<span data-ttu-id="fa6c7-105">O WMI inclui os dois provedores de eventos SNMP a seguir:</span><span class="sxs-lookup"><span data-stu-id="fa6c7-105">WMI includes the following two SNMP event providers:</span></span>

-   <span data-ttu-id="fa6c7-106">Provedor de eventos encapsulados SNMP (SEEP)</span><span class="sxs-lookup"><span data-stu-id="fa6c7-106">SNMP Encapsulated Event provider (SEEP)</span></span>

    <span data-ttu-id="fa6c7-107">O provisionamento encapsulado significa que a instância de evento tem propriedades simples que descrevem as informações mapeadas diretamente da interceptação SNMP.</span><span class="sxs-lookup"><span data-stu-id="fa6c7-107">Encapsulated provision means that the event instance has simple properties describing the information mapped directly from the SNMP trap.</span></span>

-   <span data-ttu-id="fa6c7-108">Provedor de eventos Referent SNMP (SREP)</span><span class="sxs-lookup"><span data-stu-id="fa6c7-108">SNMP Referent Event provider (SREP)</span></span>

    <span data-ttu-id="fa6c7-109">O provisionamento de Referent abstrai as informações presentes dentro da interceptação SNMP para que as propriedades que compartilham a mesma classe e instância sejam apresentadas como objetos incorporados.</span><span class="sxs-lookup"><span data-stu-id="fa6c7-109">Referent provision abstracts the information present within the SNMP trap so that properties which share the same class and instance are presented as embedded objects.</span></span> <span data-ttu-id="fa6c7-110">Isso permite a instância exclusiva, com a qual a interceptação está associada, a ser recuperada após o recebimento do evento, usando o SNMP \_ \_ RelPath.</span><span class="sxs-lookup"><span data-stu-id="fa6c7-110">This allows for the unique instance, with which the trap is associated, to be retrieved after the receipt of the event, using the SNMP \_\_RELPATH.</span></span>

> [!Note]  
> <span data-ttu-id="fa6c7-111">Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="fa6c7-111">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="fa6c7-112">Independentemente de o evento SNMP ser um Trap de SNMPv1 ou uma notificação de SNMPv2C, a pilha o relatará como uma notificação de SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="fa6c7-112">Regardless of whether the SNMP event is an SNMPv1 trap or an SNMPv2C notification, the stack reports it as an SNMPv2 notification.</span></span> <span data-ttu-id="fa6c7-113">Portanto, os provedores de eventos processam todos os eventos SNMP como notificações de SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="fa6c7-113">Therefore, the event providers process all SNMP events as SNMPv2 notifications.</span></span>

<span data-ttu-id="fa6c7-114">Para descrever os eventos SNMP para consumidores do WMI, cada provedor de eventos dá suporte a uma hierarquia de classes que deriva da classe de sistema [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md) .</span><span class="sxs-lookup"><span data-stu-id="fa6c7-114">To describe the SNMP events to WMI consumers, each event provider supports a hierarchy of classes that derives from the [**\_\_ExtrinsicEvent**](--extrinsicevent.md) system class.</span></span> <span data-ttu-id="fa6c7-115">A classe [SNMPNotification](snmpnotification.md) é a classe pai da hierarquia seep; a classe [SNMPExtendedNotification](snmpextendednotification.md) é a classe pai da hierarquia SREP.</span><span class="sxs-lookup"><span data-stu-id="fa6c7-115">The [SNMPNotification](snmpnotification.md) class is the parent class for the SEEP hierarchy; the [SNMPExtendedNotification](snmpextendednotification.md) class is the parent class for the SREP hierarchy.</span></span>

 

 



