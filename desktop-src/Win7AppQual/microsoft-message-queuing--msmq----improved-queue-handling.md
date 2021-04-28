---
description: MSMQ (enfileiramento de mensagens da Microsoft)-manipulação de fila aprimorada
ms.assetid: 49bdfdfa-c77e-4a57-8079-bf4ff6b5010b
title: MSMQ (enfileiramento de mensagens da Microsoft)-manipulação de fila aprimorada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f7b7b00cfce68a183d7925f7cfab5ff7ab54b9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088154"
---
# <a name="microsoft-message-queuing-msmq---improved-queue-handling"></a><span data-ttu-id="89296-103">MSMQ (enfileiramento de mensagens da Microsoft)-manipulação de fila aprimorada</span><span class="sxs-lookup"><span data-stu-id="89296-103">Microsoft Message Queuing (MSMQ) - Improved Queue Handling</span></span>

## <a name="platforms"></a><span data-ttu-id="89296-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="89296-104">Platforms</span></span>

<span data-ttu-id="89296-105">**Clientes** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="89296-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="89296-106">**Servidores** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="89296-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="89296-107">Impacto do recurso</span><span class="sxs-lookup"><span data-stu-id="89296-107">Feature Impact</span></span>

 <span data-ttu-id="89296-108">**Severidade** -baixa</span><span class="sxs-lookup"><span data-stu-id="89296-108">**Severity** - Low</span></span>  
<span data-ttu-id="89296-109">**Frequência** -baixa</span><span class="sxs-lookup"><span data-stu-id="89296-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="89296-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="89296-110">Description</span></span>

<span data-ttu-id="89296-111">O serviço MSMQ não coloca um limite rígido no número de filas que podem ser criadas em um sistema.</span><span class="sxs-lookup"><span data-stu-id="89296-111">MSMQ Service does not put a hard limit on the number of queues that can be created on a system.</span></span> <span data-ttu-id="89296-112">No entanto, o desempenho do sistema é afetado quando um grande número de filas é criado.</span><span class="sxs-lookup"><span data-stu-id="89296-112">However, the performance of the system is impacted when a large number of queues is created.</span></span> <span data-ttu-id="89296-113">Especificamente, quando há mais de algumas mil filas, o tempo de inicialização do serviço MSMQ aumenta exponencialmente resultando em um impacto visível.</span><span class="sxs-lookup"><span data-stu-id="89296-113">Specifically, when there are more than a few thousand queues, the start-up time of the MSMQ Service increases exponentially resulting in a visible impact.</span></span>

<span data-ttu-id="89296-114">A Microsoft otimizou a inicialização do serviço MSMQ no Windows 7 para reduzir a sobrecarga de pesquisa para carregar as filas na memória.</span><span class="sxs-lookup"><span data-stu-id="89296-114">Microsoft has optimized the MSMQ Service start-up in Windows 7 to reduce the lookup overhead for loading the queues into memory.</span></span> <span data-ttu-id="89296-115">Essa otimização levou a uma melhoria drástica do tempo de inicialização do serviço MSMQ, mesmo quando várias filas de milhares são criadas no sistema.</span><span class="sxs-lookup"><span data-stu-id="89296-115">This optimization has led to a dramatic improvement of the start-up time of the MSMQ Service even when several thousand queues are created in the system.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="89296-116">Manifestação do impacto</span><span class="sxs-lookup"><span data-stu-id="89296-116">Manifestation of Impact</span></span>

<span data-ttu-id="89296-117">Essa melhoria de desempenho não afeta a funcionalidade de nenhum aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="89296-117">This performance improvement does not impact the functionality of any existing application.</span></span>

## <a name="leveraging-the-changed-feature"></a><span data-ttu-id="89296-118">Aproveitando o recurso alterado</span><span class="sxs-lookup"><span data-stu-id="89296-118">Leveraging the Changed Feature</span></span>

<span data-ttu-id="89296-119">Os desenvolvedores de aplicativos que usam o MSMQ no Windows 7 agora podem arquitetar suas soluções sem limitar o número de filas.</span><span class="sxs-lookup"><span data-stu-id="89296-119">Application developers using MSMQ on Windows 7 can now architect their solutions without limiting the number of queues.</span></span> <span data-ttu-id="89296-120">Observe que o número de filas ainda afeta o desempenho geral do servidor MSMQ, mas o impacto no desempenho agora está em uma escala linear em vez de exponencial.</span><span class="sxs-lookup"><span data-stu-id="89296-120">Note that the number of queues still affects overall performance of the MSMQ Server, but the performance impact is now on a linear rather than exponential scale.</span></span>

## <a name="compatibility-performance-reliability-and-usability-tests"></a><span data-ttu-id="89296-121">Compatibilidade, desempenho, confiabilidade e testes de usabilidade</span><span class="sxs-lookup"><span data-stu-id="89296-121">Compatibility, Performance, Reliability, and Usability Tests</span></span>

<span data-ttu-id="89296-122">Se você usar um grande número de filas, simule o ambiente de produção em uma base de teste, monitore o desempenho e analise o tempo de inicialização do serviço e a taxa de transferência da mensagem com um grande número de filas e mensagens presentes no sistema de teste.</span><span class="sxs-lookup"><span data-stu-id="89296-122">If you use a large number of queues, simulate the production environment on a test bed, monitor performance, and analyze the service start-up time and the message throughput with a large number of queues and messages present in the test system.</span></span>

 

 



