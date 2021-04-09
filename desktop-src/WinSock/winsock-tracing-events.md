---
description: Detalhes de eventos de rastreamento do Winsock.
ms.assetid: 246AE0BE-E8E2-4291-8BF4-577F889F055B
title: Eventos de rastreamento de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeabd2d06741f8dfa1f47b513a09c941ee1490b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090348"
---
# <a name="winsock-tracing-events"></a><span data-ttu-id="ae85c-103">Eventos de rastreamento de Winsock</span><span class="sxs-lookup"><span data-stu-id="ae85c-103">Winsock Tracing Events</span></span>

<span data-ttu-id="ae85c-104">Esta seção descreve informações detalhadas sobre os detalhes específicos de eventos de rastreamento do Winsock.</span><span class="sxs-lookup"><span data-stu-id="ae85c-104">This section describes detailed information on specific Winsock Tracing Events details.</span></span>

<span data-ttu-id="ae85c-105">O rastreamento do Winsock é um recurso de solução de problemas que pode ser habilitado em binários de varejo para rastrear certos eventos de soquete do Windows com sobrecarga mínima.</span><span class="sxs-lookup"><span data-stu-id="ae85c-105">Winsock tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain Windows socket events with minimal overhead.</span></span> <span data-ttu-id="ae85c-106">Esse recurso permite melhores recursos de diagnóstico para desenvolvedores e suporte a produtos.</span><span class="sxs-lookup"><span data-stu-id="ae85c-106">This feature allows for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="ae85c-107">O rastreamento de eventos de rede do Winsock dá suporte a operações de soquete de rastreamento para aplicativos IPv4 e IPv6.</span><span class="sxs-lookup"><span data-stu-id="ae85c-107">Winsock network event tracing supports tracing socket operations for IPv4 and IPv6 applications.</span></span> <span data-ttu-id="ae85c-108">O rastreamento de alterações do catálogo Winsock dá suporte a alterações de rastreamento feitas no catálogo Winsock por provedores de serviço em camadas (LSPs).</span><span class="sxs-lookup"><span data-stu-id="ae85c-108">Winsock catalog change tracing supports tracing changes made to the Winsock catalog by layered service providers (LSPs).</span></span>

> [!Note]  
> <span data-ttu-id="ae85c-109">Os provedores de serviço em camadas são preteridos.</span><span class="sxs-lookup"><span data-stu-id="ae85c-109">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="ae85c-110">A partir do Windows 8 e do Windows Server 2012, use a [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).</span><span class="sxs-lookup"><span data-stu-id="ae85c-110">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="ae85c-111">O rastreamento do Winsock usa o ETW (rastreamento de eventos para Windows), um recurso de rastreamento de uso geral de alta velocidade fornecido pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="ae85c-111">Winsock tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="ae85c-112">O ETW fornece um mecanismo de rastreamento para eventos gerados por aplicativos de modo de usuário e drivers de dispositivo em modo kernel.</span><span class="sxs-lookup"><span data-stu-id="ae85c-112">ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="ae85c-113">O ETW pode habilitar e desabilitar o registro em log dinamicamente, facilitando a execução de rastreamento detalhado em ambientes de produção sem a necessidade de reinicializações ou reinicializações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ae85c-113">ETW can enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="ae85c-114">O suporte ao rastreamento do Winsock usando o ETW foi adicionado ao Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="ae85c-114">Support for Winsock tracing using ETW was added on Windows Vista and later.</span></span> <span data-ttu-id="ae85c-115">Para obter informações gerais sobre o ETW, consulte [melhorar a depuração e ajuste de desempenho com o ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span><span class="sxs-lookup"><span data-stu-id="ae85c-115">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="ae85c-116">A lista a seguir fornece informações detalhadas para cada evento de rastreamento do Winsock.</span><span class="sxs-lookup"><span data-stu-id="ae85c-116">The following list provides detailed information for each Winsock tracing event.</span></span> <span data-ttu-id="ae85c-117">Para obter informações adicionais sobre qualquer evento, clique no nome do evento.</span><span class="sxs-lookup"><span data-stu-id="ae85c-117">For additional information on any event, click the event name.</span></span>



| <span data-ttu-id="ae85c-118">Nome do evento</span><span class="sxs-lookup"><span data-stu-id="ae85c-118">Event Name</span></span>                                                            | <span data-ttu-id="ae85c-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae85c-119">Description</span></span>                                                                               |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae85c-120">**\_criar evento de AFD \_**</span><span class="sxs-lookup"><span data-stu-id="ae85c-120">**AFD\_EVENT\_CREATE**</span></span>](afd-event-create.md)                        | <span data-ttu-id="ae85c-121">Evento de rastreamento de rede Winsock para uma operação de criação de soquete.</span><span class="sxs-lookup"><span data-stu-id="ae85c-121">Winsock network tracing event for a socket creation operation.</span></span>                            |
| [<span data-ttu-id="ae85c-122">**\_fechamento do evento de AFD \_**</span><span class="sxs-lookup"><span data-stu-id="ae85c-122">**AFD\_EVENT\_CLOSE**</span></span>](afd-event-close.md)                          | <span data-ttu-id="ae85c-123">Evento de rastreamento de rede Winsock para operação de fechamento de soquete.</span><span class="sxs-lookup"><span data-stu-id="ae85c-123">Winsock network tracing event for socket close operation.</span></span>                                 |
| [<span data-ttu-id="ae85c-124">**Instalação do WINSOCK \_ ws2help \_ LSP \_**</span><span class="sxs-lookup"><span data-stu-id="ae85c-124">**WINSOCK\_WS2HELP\_LSP\_INSTALL**</span></span>](winsock-ws2help-lsp-install.md) | <span data-ttu-id="ae85c-125">Evento de alteração de catálogo Winsock para uma operação de instalação do LSP (provedor de serviço em camadas).</span><span class="sxs-lookup"><span data-stu-id="ae85c-125">Winsock catalog change event for a layered service provider (LSP) installation operation.</span></span> |
| [<span data-ttu-id="ae85c-126">**\_Remoção de \_ LSP \_ ws2help do Winsock**</span><span class="sxs-lookup"><span data-stu-id="ae85c-126">**WINSOCK\_WS2HELP\_LSP\_REMOVE**</span></span>](winsock-ws2help-lsp-remove.md)   | <span data-ttu-id="ae85c-127">Evento de alteração de catálogo Winsock para uma operação de remoção de LSP (provedor de serviço em camadas).</span><span class="sxs-lookup"><span data-stu-id="ae85c-127">Winsock catalog change event for a layered service provider (LSP) removal operation.</span></span>      |
| [<span data-ttu-id="ae85c-128">**\_ \_ Desabilitação de LSP ws2help do Winsock \_**</span><span class="sxs-lookup"><span data-stu-id="ae85c-128">**WINSOCK\_WS2HELP\_LSP\_DISABLE**</span></span>](winsock-ws2help-lsp-disable.md) | <span data-ttu-id="ae85c-129">Evento de alteração de catálogo Winsock para uma operação de desabilitação de LSP (provedor de serviço em camadas).</span><span class="sxs-lookup"><span data-stu-id="ae85c-129">Winsock catalog change event for a layered service provider (LSP) disable operation.</span></span>      |
| [<span data-ttu-id="ae85c-130">**Redefinição de \_ LSP ws2help Winsock \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ae85c-130">**WINSOCK\_WS2HELP\_LSP\_RESET**</span></span>](winsock-ws2help-lsp-reset.md)     | <span data-ttu-id="ae85c-131">Evento de alteração de catálogo Winsock para uma operação de redefinição de catálogo Winsock.</span><span class="sxs-lookup"><span data-stu-id="ae85c-131">Winsock catalog change event for a Winsock catalog reset operation.</span></span>                       |



 

## <a name="related-topics"></a><span data-ttu-id="ae85c-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae85c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae85c-133">Melhore o ajuste de depuração e desempenho com o ETW</span><span class="sxs-lookup"><span data-stu-id="ae85c-133">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> <dt>

[<span data-ttu-id="ae85c-134">Rastreamento de Winsock</span><span class="sxs-lookup"><span data-stu-id="ae85c-134">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="ae85c-135">Níveis de rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="ae85c-135">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="ae85c-136">Controle do rastreamento do Winsock</span><span class="sxs-lookup"><span data-stu-id="ae85c-136">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="ae85c-137">Detalhes de rastreamento de eventos de rede do Winsock</span><span class="sxs-lookup"><span data-stu-id="ae85c-137">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="ae85c-138">Detalhes de rastreamento de alteração do catálogo Winsock</span><span class="sxs-lookup"><span data-stu-id="ae85c-138">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
