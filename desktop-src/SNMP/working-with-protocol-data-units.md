---
title: Trabalhando com unidades de dados de protocolo
description: O SNMP (Simple Network Management Protocol) envia solicitações de operação e respostas como mensagens SNMP.
ms.assetid: 0928981c-4d60-4583-9eef-8127e05b1ba8
keywords:
- Trabalhando com unidades de dados de protocolo SNMP
- Unidades de dados de protocolo SNMP, trabalhando com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e40f36fa28f7ff17974d79f4f8ac29b8b6130b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005837"
---
# <a name="working-with-protocol-data-units"></a><span data-ttu-id="d4a7d-105">Trabalhando com unidades de dados de protocolo</span><span class="sxs-lookup"><span data-stu-id="d4a7d-105">Working with Protocol Data Units</span></span>

<span data-ttu-id="d4a7d-106">O SNMP (Simple Network Management Protocol) envia solicitações de operação e respostas como mensagens SNMP.</span><span class="sxs-lookup"><span data-stu-id="d4a7d-106">The Simple Network Management Protocol (SNMP) sends operation requests and responses as SNMP messages.</span></span> <span data-ttu-id="d4a7d-107">Uma mensagem SNMP é uma PDU (unidade de dados de protocolo SNMP) e elementos de cabeçalho de mensagem adicionais definidos pela RFC relevante.</span><span class="sxs-lookup"><span data-stu-id="d4a7d-107">An SNMP message is an SNMP protocol data unit (PDU) plus additional message header elements defined by the relevant RFC.</span></span> <span data-ttu-id="d4a7d-108">Uma PDU inclui uma lista de associações de variáveis.</span><span class="sxs-lookup"><span data-stu-id="d4a7d-108">A PDU includes a variable binding list.</span></span>

<span data-ttu-id="d4a7d-109">A estrutura de uma PDU é restrita à implementação do Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="d4a7d-109">The structure of a PDU is restricted to the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="d4a7d-110">Um aplicativo WinSNMP pode acessar uma PDU com um identificador do tipo **HSNMP \_ PDU**.</span><span class="sxs-lookup"><span data-stu-id="d4a7d-110">A WinSNMP application can access a PDU with a handle of the type **HSNMP\_PDU**.</span></span> <span data-ttu-id="d4a7d-111">O aplicativo WinSNMP deve criar um PDU antes de chamar a função [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) ou a função [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) .</span><span class="sxs-lookup"><span data-stu-id="d4a7d-111">The WinSNMP application must create a PDU before it calls the [**SnmpSendMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpsendmsg) function or the [**SnmpEncodeMsg**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpencodemsg) function.</span></span>

<span data-ttu-id="d4a7d-112">O aplicativo pode extrair e atualizar os elementos de dados de uma PDU e liberar recursos alocados para PDUs.</span><span class="sxs-lookup"><span data-stu-id="d4a7d-112">The application can extract and update the data elements of a PDU, and release resources allocated for PDUs.</span></span> <span data-ttu-id="d4a7d-113">Para executar essas operações, o aplicativo usa as [funções de PDU](winsnmp-functions.md)de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="d4a7d-113">To perform these operations, the application uses the WinSNMP [PDU functions](winsnmp-functions.md).</span></span> <span data-ttu-id="d4a7d-114">A tabela a seguir lista os tópicos que abordam o trabalho com PDUs no ambiente de programação WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="d4a7d-114">The following table lists topics that discuss working with PDUs in the WinSNMP programming environment.</span></span>



| <span data-ttu-id="d4a7d-115">Tópico</span><span class="sxs-lookup"><span data-stu-id="d4a7d-115">Topic</span></span>                                                                        | <span data-ttu-id="d4a7d-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d4a7d-116">Description</span></span>                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="d4a7d-117">Criando uma PDU</span><span class="sxs-lookup"><span data-stu-id="d4a7d-117">Creating a PDU</span></span>](creating-a-pdu.md)                                         | <span data-ttu-id="d4a7d-118">Descreve como criar uma PDU.</span><span class="sxs-lookup"><span data-stu-id="d4a7d-118">Describes how to create a PDU.</span></span>                                     |
| [<span data-ttu-id="d4a7d-119">Atualizando uma PDU</span><span class="sxs-lookup"><span data-stu-id="d4a7d-119">Updating a PDU</span></span>](updating-a-pdu.md)                                         | <span data-ttu-id="d4a7d-120">Descreve como recuperar e atualizar campos de PDU.</span><span class="sxs-lookup"><span data-stu-id="d4a7d-120">Describes how to retrieve and update PDU fields.</span></span>                   |
| [<span data-ttu-id="d4a7d-121">Duplicando uma PDU</span><span class="sxs-lookup"><span data-stu-id="d4a7d-121">Duplicating a PDU</span></span>](duplicating-a-pdu.md)                                   | <span data-ttu-id="d4a7d-122">Descreve como duplicar uma PDU.</span><span class="sxs-lookup"><span data-stu-id="d4a7d-122">Describes how to duplicate a PDU.</span></span>                                  |
| [<span data-ttu-id="d4a7d-123">Validando uma PDU</span><span class="sxs-lookup"><span data-stu-id="d4a7d-123">Validating a PDU</span></span>](validating-a-pdu.md)                                     | <span data-ttu-id="d4a7d-124">Descreve a validação de uma PDU.</span><span class="sxs-lookup"><span data-stu-id="d4a7d-124">Describes the validation of a PDU.</span></span>                                 |
| [<span data-ttu-id="d4a7d-125">Resposta correspondente e PDUs de solicitação</span><span class="sxs-lookup"><span data-stu-id="d4a7d-125">Matching Response and Request PDUs</span></span>](matching-response-and-request-pdus.md) | <span data-ttu-id="d4a7d-126">Descreve o processo de correspondência de uma PDU de resposta para uma PDU de solicitação.</span><span class="sxs-lookup"><span data-stu-id="d4a7d-126">Describes the process of matching a response PDU to a request PDU.</span></span> |



 

<span data-ttu-id="d4a7d-127">Para obter mais informações, consulte [trabalhando com as listas de associação de variáveis](working-with-variable-binding-lists.md) e objetos de identificador de [recurso](resource-handle-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d4a7d-127">For more information, see [Working with Variable Binding Lists](working-with-variable-binding-lists.md) and [Resource Handle Objects](resource-handle-objects.md).</span></span>

 

 




