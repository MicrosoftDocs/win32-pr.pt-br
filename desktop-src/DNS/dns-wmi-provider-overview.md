---
title: Visão geral do provedor WMI de DNS
description: Um provedor é um elemento de arquitetura de Instrumentação de Gerenciamento do Windows (WMI).
ms.assetid: e6ada7b5-dd46-4c47-8db8-55f910429e31
keywords:
- Sistema de nomes de domínio, provedor WMI, arquitetura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aed54d0d9cbac4070483e8e72e9917607e824c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005389"
---
# <a name="dns-wmi-provider-overview"></a><span data-ttu-id="bf7d3-104">Visão geral do provedor WMI de DNS</span><span class="sxs-lookup"><span data-stu-id="bf7d3-104">DNS WMI Provider Overview</span></span>

<span data-ttu-id="bf7d3-105">Um provedor é um elemento de arquitetura de *Instrumentação de gerenciamento do Windows (WMI)*.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-105">A provider is an architectural element of *Windows Management Instrumentation (WMI)*.</span></span> <span data-ttu-id="bf7d3-106">O WMI define uma arquitetura unificada para descrever, acessar e instrumentar objetos.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-106">WMI defines a unified architecture for describing, accessing, and instrumenting objects.</span></span> <span data-ttu-id="bf7d3-107">Parte dessa arquitetura é um banco de dados grande de classes WMI usadas para realizar tarefas de gerenciamento remoto em objetos específicos.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-107">Part of this architecture is a large database of WMI classes used to carry out remote management tasks on specific objects.</span></span>

<span data-ttu-id="bf7d3-108">Os provedores de WMI atuam como intermediários entre o WMI e um ou mais objetos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-108">WMI providers act as intermediaries between WMI and one or more managed objects.</span></span> <span data-ttu-id="bf7d3-109">Quando o WMI recebe uma solicitação de um aplicativo de gerenciamento para dados que não estão disponíveis no repositório CIM ou para notificações de eventos que o WMI não dá suporte, ele encaminha a solicitação para um provedor.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-109">When WMI receives a request from a management application for data that is not available from the CIM repository or for notifications of events that WMI does not support, it forwards the request to a provider.</span></span> <span data-ttu-id="bf7d3-110">Os provedores fornecem dados e notificações de eventos para os objetos gerenciados que são específicos para seus domínios.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-110">Providers supply data and event notifications for managed objects that are specific to their particular domain.</span></span> <span data-ttu-id="bf7d3-111">Um provedor estende o esquema WMI de classes para permitir que o WMI trabalhe com novos tipos de objetos.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-111">A provider extends the WMI schema of classes to allow WMI to work with new types of objects.</span></span> <span data-ttu-id="bf7d3-112">O provedor WMI de DNS define classes para consultar e configurar um servidor DNS, juntamente com suas zonas DNS e registros DNS associados.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-112">The DNS WMI Provider defines classes for querying and configuring a DNS Server, along with its associated DNS zones and DNS records.</span></span>

<span data-ttu-id="bf7d3-113">O provedor WMI de DNS expõe vários objetos DNS para clientes, incluindo o servidor DNS, domínio DNS e objetos RR DNS.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-113">The DNS WMI provider exposes a number of DNS objects to clients, including DNS Server, DNS domain, and DNS RR objects.</span></span> <span data-ttu-id="bf7d3-114">Por meio desses objetos, os clientes podem executar atividades de gerenciamento de DNS.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-114">Through those objects, clients are able to perform DNS management activities.</span></span>

<span data-ttu-id="bf7d3-115">Usando o provedor WMI do DNS, você pode criar suas próprias ferramentas para executar a maioria das tarefas de administração do servidor DNS.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-115">Using the DNS WMI Provider, you can create your own tools to perform most DNS Server administration tasks.</span></span> <span data-ttu-id="bf7d3-116">Por exemplo, você pode criar, excluir e exibir zonas e registros; redefinir Propriedades de servidor e zona; e executar operações de administração rotineiras, como atualizar a zona, recarregar a zona, atualizar a zona, gravar a zona de volta em um arquivo ou Active Directory, pausar e retomar a zona, limpar o cache, parar e iniciar o serviço DNS e exibir estatísticas.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-116">For example, you can create, delete, and view zones and records; reset server and zone properties; and perform routine administration operations such as updating the zone, reloading the zone, refreshing the zone, writing the zone back to a file or Active Directory, pausing and resuming the zone, clearing the cache, stopping and starting the DNS service, and viewing statistics.</span></span>

<span data-ttu-id="bf7d3-117">O provedor WMI de DNS tem um conjunto de comportamentos exclusivos não encontrado em outros provedores.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-117">The DNS WMI Provider has a set of unique behaviors not found in other providers.</span></span> <span data-ttu-id="bf7d3-118">Consulte a [referência do provedor WMI do DNS](dns-wmi-provider-reference.md) para obter detalhes da classe.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-118">See the [DNS WMI Provider Reference](dns-wmi-provider-reference.md) for class details.</span></span>

 

 




