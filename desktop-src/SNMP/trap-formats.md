---
title: Formatos de interceptação
description: O formato de PDUs de interceptação é diferente daquele de outra PDUs. O formato de armadilhas de SNMPv1 e interceptações de SNMPv2C também é diferente.
ms.assetid: 2d2b4520-28b7-4a2e-8dee-456e17d9d6f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87adc3222808fcc7e81904ade07c09afa13bc6d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005173"
---
# <a name="trap-formats"></a><span data-ttu-id="889d3-104">Formatos de interceptação</span><span class="sxs-lookup"><span data-stu-id="889d3-104">Trap Formats</span></span>

<span data-ttu-id="889d3-105">O formato de PDUs de interceptação é diferente daquele de outra PDUs.</span><span class="sxs-lookup"><span data-stu-id="889d3-105">The format of trap PDUs is different than that of other PDUs.</span></span> <span data-ttu-id="889d3-106">O formato de armadilhas de SNMPv1 e interceptações de SNMPv2C também é diferente.</span><span class="sxs-lookup"><span data-stu-id="889d3-106">The format of SNMPv1 traps and SNMPv2C traps is also different.</span></span>

<span data-ttu-id="889d3-107">Na estrutura do SNMPv2C, o formato de interceptação de PDU é uma lista de associações de variáveis de *n* entradas de associação de variáveis organizadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="889d3-107">Under the SNMPv2C framework, the PDU trap format is a variable binding list of *n* variable binding entries organized in the following manner:</span></span>

-   <span data-ttu-id="889d3-108">A primeira entrada de associação de variável contém um carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="889d3-108">The first variable binding entry contains a time-stamp.</span></span>
-   <span data-ttu-id="889d3-109">A segunda entrada de associação de variável é um identificador de objeto que identifica a interceptação.</span><span class="sxs-lookup"><span data-stu-id="889d3-109">The second variable binding entry is an object identifier that identifies the trap.</span></span>
-   <span data-ttu-id="889d3-110">O terceiro a *n* entradas de associação de variável, se presente, contêm informações adicionais associadas à interceptação.</span><span class="sxs-lookup"><span data-stu-id="889d3-110">The third through *n* variable binding entries, if present, contain additional information associated with the trap.</span></span>

<span data-ttu-id="889d3-111">Na estrutura SNMPv1, o formato de interceptação PDU é o seguinte.</span><span class="sxs-lookup"><span data-stu-id="889d3-111">Under the SNMPv1 framework, the PDU trap format is as follows.</span></span>

| <span data-ttu-id="889d3-112">Campo</span><span class="sxs-lookup"><span data-stu-id="889d3-112">Field</span></span>                      | <span data-ttu-id="889d3-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="889d3-113">Description</span></span>                                                      |
|----------------------------|------------------------------------------------------------------|
| <span data-ttu-id="889d3-114">corporativo</span><span class="sxs-lookup"><span data-stu-id="889d3-114">enterprise</span></span>                 | <span data-ttu-id="889d3-115">Identifica o tipo de dispositivo que gerou a interceptação.</span><span class="sxs-lookup"><span data-stu-id="889d3-115">Identifies the type of device that generated the trap.</span></span>           |
| <span data-ttu-id="889d3-116">Agente-addr</span><span class="sxs-lookup"><span data-stu-id="889d3-116">agent-addr</span></span>                 | <span data-ttu-id="889d3-117">Identifica o endereço IP do dispositivo que gerou a interceptação.</span><span class="sxs-lookup"><span data-stu-id="889d3-117">Identifies the IP address of the device that generated the trap.</span></span> |
| <span data-ttu-id="889d3-118">desvio genérico/interceptação específica</span><span class="sxs-lookup"><span data-stu-id="889d3-118">generic-trap/specific-trap</span></span> | <span data-ttu-id="889d3-119">Identifica um tipo de interceptação predefinida.</span><span class="sxs-lookup"><span data-stu-id="889d3-119">Identifies a predefined trap type.</span></span>                               |
| <span data-ttu-id="889d3-120">carimbo de data/hora</span><span class="sxs-lookup"><span data-stu-id="889d3-120">time-stamp</span></span>                 | <span data-ttu-id="889d3-121">Identifica quando a interceptação foi gerada.</span><span class="sxs-lookup"><span data-stu-id="889d3-121">Identifies when the trap was generated.</span></span>                          |
| <span data-ttu-id="889d3-122">associações de variáveis</span><span class="sxs-lookup"><span data-stu-id="889d3-122">variable-bindings</span></span>          | <span data-ttu-id="889d3-123">Contém informações adicionais associadas à interceptação.</span><span class="sxs-lookup"><span data-stu-id="889d3-123">Contains additional information associated with the trap.</span></span>        |



 

<span data-ttu-id="889d3-124">A função [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) sempre retorna uma mensagem no formato SNMPv2c.</span><span class="sxs-lookup"><span data-stu-id="889d3-124">The [**SnmpRecvMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmprecvmsg) function always returns a message in the SNMPv2C format.</span></span> <span data-ttu-id="889d3-125">Se a mensagem contiver o tipo de operação **\_ \_ interceptação de PDU SNMP**, o aplicativo poderá ler as entradas de associação de variável da mensagem e recuperar as informações associadas à interceptação.</span><span class="sxs-lookup"><span data-stu-id="889d3-125">If the message contains the operation type **SNMP\_PDU\_TRAP**, the application can read the variable binding entries of the message and retrieve the information associated with the trap.</span></span>

 

 




