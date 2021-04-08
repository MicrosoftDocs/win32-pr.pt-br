---
description: Monitore as notificações de eventos do sistema de programas executados em computadores móveis para determinar a largura de banda e a latência da conexão de rede. Crie aplicativos otimizados para computação móvel e LANs de alta latência.
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: Serviço de Notificação de Eventos do Sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3238441f82c26a33370c37fe09b3e4007639f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922428"
---
# <a name="system-event-notification-service"></a><span data-ttu-id="380ba-104">Serviço de Notificação de Eventos do Sistema</span><span class="sxs-lookup"><span data-stu-id="380ba-104">System Event Notification Service</span></span>

## <a name="purpose"></a><span data-ttu-id="380ba-105">Finalidade</span><span class="sxs-lookup"><span data-stu-id="380ba-105">Purpose</span></span>

<span data-ttu-id="380ba-106">Os aplicativos projetados para uso por usuários móveis exigem um conjunto exclusivo de funções e notificações de conectividade.</span><span class="sxs-lookup"><span data-stu-id="380ba-106">Applications designed for use by mobile users require a unique set of connectivity functions and notifications.</span></span> <span data-ttu-id="380ba-107">No passado, esses aplicativos individuais eram necessários para implementar esses recursos internamente.</span><span class="sxs-lookup"><span data-stu-id="380ba-107">In the past these individual applications were required to implement these features internally.</span></span> <span data-ttu-id="380ba-108">O SENS (serviço de notificação de eventos do sistema) agora fornece esses recursos no sistema operacional, criando uma interface de notificação e conectividade uniforme para aplicativos.</span><span class="sxs-lookup"><span data-stu-id="380ba-108">The System Event Notification Service (SENS) now provides these capabilities in the operating system, creating a uniform connectivity and notification interface for applications.</span></span> <span data-ttu-id="380ba-109">O uso de desenvolvedores de sensores pode determinar a largura de banda de conexão e informações de latência de dentro de seu aplicativo e otimizar a operação do aplicativo com base nessas condições.</span><span class="sxs-lookup"><span data-stu-id="380ba-109">Using SENS developers can determine connection bandwidth and latency information from within their application and optimize the application's operation based on those conditions.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="380ba-110">Quando aplicável</span><span class="sxs-lookup"><span data-stu-id="380ba-110">Where applicable</span></span>

<span data-ttu-id="380ba-111">As funções de conectividade e as notificações do SENS são úteis para aplicativos escritos para computadores móveis ou computadores conectados a redes locais de alta latência.</span><span class="sxs-lookup"><span data-stu-id="380ba-111">The connectivity functions and notifications of SENS are useful for applications written for mobile computers or computers connected to high latency local area networks.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="380ba-112">Público de desenvolvedores</span><span class="sxs-lookup"><span data-stu-id="380ba-112">Developer audience</span></span>

<span data-ttu-id="380ba-113">Este documento destina-se a desenvolvedores de software que desenvolvem aplicativos para computação móvel e redes locais de alta latência.</span><span class="sxs-lookup"><span data-stu-id="380ba-113">This document is intended for software developers who develop applications for mobile computing and high latency local area networks.</span></span> <span data-ttu-id="380ba-114">Este documento fornece uma referência completa de todas as partes do serviço de notificação de eventos do sistema, incluindo o objeto SENS e os métodos de suporte.</span><span class="sxs-lookup"><span data-stu-id="380ba-114">This document provides a complete reference of all parts of the System Event Notification Service including the SENS object and supporting methods.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="380ba-115">Requisitos de tempo de execução</span><span class="sxs-lookup"><span data-stu-id="380ba-115">Run-time requirements</span></span>

<span data-ttu-id="380ba-116">Requer o Microsoft Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="380ba-116">Requires Microsoft Windows XP or later.</span></span> <span data-ttu-id="380ba-117">Para obter informações sobre quais sistemas operacionais são necessários para usar uma interface ou função específica, consulte a seção requisitos da documentação.</span><span class="sxs-lookup"><span data-stu-id="380ba-117">For information about which operating systems are required to use a particular interface or function, see the Requirements section of the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="380ba-118">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="380ba-118">In this section</span></span>



| <span data-ttu-id="380ba-119">Tópico</span><span class="sxs-lookup"><span data-stu-id="380ba-119">Topic</span></span>                                                              | <span data-ttu-id="380ba-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="380ba-120">Description</span></span>                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="380ba-121">Visão geral</span><span class="sxs-lookup"><span data-stu-id="380ba-121">Overview</span></span>](about-system-event-notification-service.md)<br/> | <span data-ttu-id="380ba-122">Informações gerais sobre o serviço de notificação de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="380ba-122">General information about System Event Notification Service.</span></span><br/>               |
| [<span data-ttu-id="380ba-123">Referência</span><span class="sxs-lookup"><span data-stu-id="380ba-123">Reference</span></span>](sens-reference.md)<br/>                         | <span data-ttu-id="380ba-124">Documentação de métodos e interfaces do serviço de notificação de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="380ba-124">Documentation of System Event Notification Service methods and interfaces.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="380ba-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="380ba-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="380ba-126">**IEventSubscription**</span><span class="sxs-lookup"><span data-stu-id="380ba-126">**IEventSubscription**</span></span>](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 
