---
title: O modelo WinSNMP
description: O modelo compatível com WinSNMP inclui os componentes básicos a seguir.
ms.assetid: 491df017-0b91-4fcf-97c3-4e296c3324bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff7ae4fa1c1ee56fc534e4aa4c9bffefb8d7f4d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005174"
---
# <a name="the-winsnmp-model"></a><span data-ttu-id="d3c39-103">O modelo WinSNMP</span><span class="sxs-lookup"><span data-stu-id="d3c39-103">The WinSNMP Model</span></span>

<span data-ttu-id="d3c39-104">O modelo compatível com WinSNMP inclui os seguintes componentes básicos:</span><span class="sxs-lookup"><span data-stu-id="d3c39-104">The WinSNMP-compliant model includes the following basic components:</span></span>

-   <span data-ttu-id="d3c39-105">Um aplicativo de gerenciamento de rede SNMP habilitado para WinSNMP, ou seja, um *aplicativo* compatível com WinSNMP</span><span class="sxs-lookup"><span data-stu-id="d3c39-105">A WinSNMP-enabled SNMP network management application, that is, a WinSNMP-compliant *application*</span></span>
-   <span data-ttu-id="d3c39-106">A camada de função WinSNMP</span><span class="sxs-lookup"><span data-stu-id="d3c39-106">The WinSNMP function layer</span></span>
-   <span data-ttu-id="d3c39-107">Um provedor de serviços SNMP habilitado para WinSNMP, ou seja, uma *implementação* compatível com o WinSNMP</span><span class="sxs-lookup"><span data-stu-id="d3c39-107">A WinSNMP-enabled SNMP service provider, that is, a WinSNMP-compliant *implementation*</span></span>

<span data-ttu-id="d3c39-108">Os aplicativos de gerenciamento de rede que devem transmitir mensagens SNMP operam com eficiência em um ambiente orientado a eventos.</span><span class="sxs-lookup"><span data-stu-id="d3c39-108">Network management applications that must convey SNMP messages operate efficiently in an event-driven environment.</span></span> <span data-ttu-id="d3c39-109">Isso ocorre porque o SNMP é um protocolo baseado em datagrama ou sem conexão entre entidades remotas que não estabelecem circuitos virtuais.</span><span class="sxs-lookup"><span data-stu-id="d3c39-109">This is because SNMP is a datagram-based or connectionless protocol between remote entities that do not establish virtual circuits.</span></span>

<span data-ttu-id="d3c39-110">Como os aplicativos do Microsoft Windows também são controlados por evento, o WinSNMP usa um modelo de programação no qual o recebimento e o processamento de *eventos de mensagens* assíncronas geram aplicativos de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d3c39-110">Since Microsoft Windows applications are also event-driven, WinSNMP uses a programming model in which the receipt and processing of asynchronous *message-events* drive management applications.</span></span> <span data-ttu-id="d3c39-111">Um evento de mensagem assíncrona pode ser uma solicitação de operação SNMP por um aplicativo de gerente ou a resposta a uma solicitação por um aplicativo do Agent.</span><span class="sxs-lookup"><span data-stu-id="d3c39-111">An asynchronous message-event can be an SNMP operation request by a manager application, or the response to a request by an agent application.</span></span>

<span data-ttu-id="d3c39-112">SNMP envia solicitações e respostas como mensagens SNMP.</span><span class="sxs-lookup"><span data-stu-id="d3c39-112">SNMP sends requests and responses as SNMP messages.</span></span> <span data-ttu-id="d3c39-113">Uma mensagem SNMP é uma PDU (unidade de dados de protocolo SNMP) e elementos de cabeçalho de mensagem adicionais definidos pela RFC relevante.</span><span class="sxs-lookup"><span data-stu-id="d3c39-113">An SNMP message is an SNMP protocol data unit (PDU) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="d3c39-114">Para obter mais informações, consulte [sobre mensagens SNMP](about-snmp-messages.md), [trabalhando com listas de associação de variáveis](working-with-variable-binding-lists.md) e [trabalhando com unidades de dados de protocolo](working-with-protocol-data-units.md).</span><span class="sxs-lookup"><span data-stu-id="d3c39-114">For more information, see [About SNMP Messages](about-snmp-messages.md), [Working with Variable Binding Lists](working-with-variable-binding-lists.md) and [Working with Protocol Data Units](working-with-protocol-data-units.md).</span></span>

 

 




