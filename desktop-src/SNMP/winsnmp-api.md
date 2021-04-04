---
title: API WinSNMP
description: A interface de programação de aplicativo SNMP do Microsoft Windows (a API WinSNMP) versões 1.1 a e 2,0 permitem que você desenvolva aplicativos de gerenciamento de rede baseados em SNMP que são executados no ambiente do Windows.
ms.assetid: 54d9b61a-815a-41c3-9365-ec4478acc3f2
keywords:
- API WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d502060daa2931ca67c4476448347602159c98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007883"
---
# <a name="winsnmp-api"></a><span data-ttu-id="e7d27-104">API WinSNMP</span><span class="sxs-lookup"><span data-stu-id="e7d27-104">WinSNMP API</span></span>

<span data-ttu-id="e7d27-105">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="e7d27-105">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e7d27-106">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="e7d27-106">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="e7d27-107">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="e7d27-107">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

<span data-ttu-id="e7d27-108">A interface de programação de aplicativo SNMP do Microsoft Windows (a API WinSNMP) versões 1.1 a e 2,0 permitem que você desenvolva aplicativos de gerenciamento de rede baseados em SNMP que são executados no ambiente do Windows.</span><span class="sxs-lookup"><span data-stu-id="e7d27-108">The Microsoft Windows SNMP Application Programming Interface (the WinSNMP API) versions 1.1a and 2.0 allow you to develop SNMP-based network management applications that execute in the Windows environment.</span></span> <span data-ttu-id="e7d27-109">O SNMP (Simple Network Management Protocol) é um protocolo de solicitação-resposta que transfere informações de gerenciamento entre entidades de protocolo.</span><span class="sxs-lookup"><span data-stu-id="e7d27-109">The Simple Network Management Protocol (SNMP) is a request-response protocol that transfers management information between protocol entities.</span></span>

<span data-ttu-id="e7d27-110">O WinSNMP foi desenvolvido em conjunto com a cooperação, a entrada e o suporte de várias empresas, associações e indivíduos.</span><span class="sxs-lookup"><span data-stu-id="e7d27-110">WinSNMP has been jointly developed with the cooperation, input, and support from several companies, associations and individuals.</span></span>

<span data-ttu-id="e7d27-111">A primeira parte desta visão geral fornece informações sobre o adendo do WinSNMP 2,0, as versões SNMP e uma lista das solicitações relevantes de comentários (RFCs).</span><span class="sxs-lookup"><span data-stu-id="e7d27-111">The first part of this overview provides information about the WinSNMP 2.0 Addendum, SNMP versions, and a list of the relevant Requests for Comments (RFCs).</span></span> <span data-ttu-id="e7d27-112">Ele também descreve o modelo WinSNMP e os componentes e recursos da implementação do Microsoft WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="e7d27-112">It also describes the WinSNMP model, and the components and features of the Microsoft WinSNMP implementation.</span></span> <span data-ttu-id="e7d27-113">Ele também fornece informações sobre conceitos de comunicações e gerenciamento de dados de que você precisa para programar no ambiente WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="e7d27-113">It also provides information about data management and communications concepts you need to program in the WinSNMP environment.</span></span>

<span data-ttu-id="e7d27-114">A segunda seção discute as funções WinSNMP e as seguintes tarefas de programação de WinSNMP relacionadas:</span><span class="sxs-lookup"><span data-stu-id="e7d27-114">The second section discusses the WinSNMP functions and the following related WinSNMP programming tasks:</span></span>

-   [<span data-ttu-id="e7d27-115">Abrindo e fechando um aplicativo WinSNMP</span><span class="sxs-lookup"><span data-stu-id="e7d27-115">Opening and closing a WinSNMP application</span></span>](opening-and-closing-a-winsnmp-application.md)
-   [<span data-ttu-id="e7d27-116">Abrindo e fechando uma sessão WinSNMP</span><span class="sxs-lookup"><span data-stu-id="e7d27-116">Opening and closing a WinSNMP session</span></span>](opening-and-closing-a-winsnmp-session.md)
-   [<span data-ttu-id="e7d27-117">Gerenciando interceptações e notificações</span><span class="sxs-lookup"><span data-stu-id="e7d27-117">Managing traps and notifications</span></span>](managing-traps-and-notifications.md)
-   [<span data-ttu-id="e7d27-118">Trabalhando com listas de associação de variáveis</span><span class="sxs-lookup"><span data-stu-id="e7d27-118">Working with variable binding lists</span></span>](working-with-variable-binding-lists.md)
-   [<span data-ttu-id="e7d27-119">Trabalhando com unidades de dados de protocolo</span><span class="sxs-lookup"><span data-stu-id="e7d27-119">Working with protocol data units</span></span>](working-with-protocol-data-units.md)
-   [<span data-ttu-id="e7d27-120">Enviando mensagens SNMP</span><span class="sxs-lookup"><span data-stu-id="e7d27-120">Sending SNMP messages</span></span>](sending-snmp-messages.md)
-   [<span data-ttu-id="e7d27-121">Recebendo mensagens SNMP</span><span class="sxs-lookup"><span data-stu-id="e7d27-121">Receiving SNMP messages</span></span>](receiving-snmp-messages.md)
-   [<span data-ttu-id="e7d27-122">Gerenciando identificadores de objeto</span><span class="sxs-lookup"><span data-stu-id="e7d27-122">Managing object identifiers</span></span>](managing-object-identifiers.md)
-   [<span data-ttu-id="e7d27-123">Liberando descritores de WinSNMP</span><span class="sxs-lookup"><span data-stu-id="e7d27-123">Freeing WinSNMP descriptors</span></span>](freeing-winsnmp-descriptors.md)
-   [<span data-ttu-id="e7d27-124">Definindo a entidade e o modo de tradução de contexto</span><span class="sxs-lookup"><span data-stu-id="e7d27-124">Setting the entity and context translation mode</span></span>](setting-the-entity-and-context-translation-mode.md)
-   [<span data-ttu-id="e7d27-125">Gerenciando a política de retransmissão</span><span class="sxs-lookup"><span data-stu-id="e7d27-125">Managing the retransmission policy</span></span>](managing-the-retransmission-policy.md)
-   [<span data-ttu-id="e7d27-126">Escrevendo aplicativos WinSNMP com vários threads</span><span class="sxs-lookup"><span data-stu-id="e7d27-126">Writing WinSNMP applications with multiple threads</span></span>](writing-winsnmp-applications-with-multiple-threads.md)
-   [<span data-ttu-id="e7d27-127">Registrando um aplicativo de agente SNMP</span><span class="sxs-lookup"><span data-stu-id="e7d27-127">Registering an SNMP agent application</span></span>](registering-an-snmp-agent-application.md)

<span data-ttu-id="e7d27-128">Você deve estar familiarizado com os conceitos básicos do SNMP e da programação do Windows antes de ler esta visão geral.</span><span class="sxs-lookup"><span data-stu-id="e7d27-128">You should be familiar with the basic concepts of SNMP and Windows programming before reading this overview.</span></span> <span data-ttu-id="e7d27-129">Para obter mais informações sobre SNMP, consulte [protocolo de gerenciamento de rede simples](simple-network-management-protocol-snmp-.md) e as solicitações relevantes de comentários (RFCs) que são publicadas pela IETF (Internet Engineering Task Force).</span><span class="sxs-lookup"><span data-stu-id="e7d27-129">For more information about SNMP, see [Simple Network Management Protocol](simple-network-management-protocol-snmp-.md) and the relevant Requests for Comments (RFCs) which are published by the Internet Engineering Task Force (IETF).</span></span>

 

 