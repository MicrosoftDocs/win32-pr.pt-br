---
description: 'Saiba mais sobre: eventos de rastreamento de gerenciamento de memória'
ms.assetid: D53BD414-F140-496E-884F-5A4EC4F0AAC4
title: Eventos de rastreamento de gerenciamento de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73ca05260b6c29ecae765c047691b81a26116fb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766886"
---
# <a name="memory-management-tracing-events"></a><span data-ttu-id="a877f-103">Eventos de rastreamento de gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="a877f-103">Memory Management Tracing Events</span></span>

<span data-ttu-id="a877f-104">Esta seção descreve informações detalhadas sobre detalhes específicos do evento de rastreamento de gerenciamento de memória.</span><span class="sxs-lookup"><span data-stu-id="a877f-104">This section describes detailed information on specific Memory management tracing event details.</span></span>

<span data-ttu-id="a877f-105">O rastreamento de gerenciamento de memória é um recurso de solução de problemas que pode ser habilitado em binários de varejo para rastrear determinados eventos de gerenciamento de memória com sobrecarga mínima.</span><span class="sxs-lookup"><span data-stu-id="a877f-105">Memory management tracing is a troubleshooting feature that can be enabled in retail binaries to trace certain memory management events with minimal overhead.</span></span> <span data-ttu-id="a877f-106">Esse recurso permite melhores recursos de diagnóstico para desenvolvedores e suporte a produtos.</span><span class="sxs-lookup"><span data-stu-id="a877f-106">This feature allows for better diagnostic capabilities for developers and product support.</span></span> <span data-ttu-id="a877f-107">O rastreamento de eventos de gerenciamento de memória dá suporte à alocação de heap de rastreamento, realocação e operações gratuitas.</span><span class="sxs-lookup"><span data-stu-id="a877f-107">Memory management event tracing supports tracing heap allocation, reallocation, and free operations.</span></span>

<span data-ttu-id="a877f-108">O rastreamento de eventos de gerenciamento de memória usa o ETW (rastreamento de eventos para Windows), um recurso de rastreamento de alta velocidade e uso geral fornecido pelo sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a877f-108">Memory management event tracing uses Event Tracing for Windows (ETW), a general-purpose, high-speed tracing facility provided by the operating system.</span></span> <span data-ttu-id="a877f-109">O ETW fornece um mecanismo de rastreamento para eventos gerados por aplicativos de modo de usuário e drivers de dispositivo em modo kernel.</span><span class="sxs-lookup"><span data-stu-id="a877f-109">ETW provides a tracing mechanism for events raised by both user-mode applications and kernel-mode device drivers.</span></span> <span data-ttu-id="a877f-110">O ETW pode habilitar e desabilitar o registro em log dinamicamente, facilitando a execução de rastreamento detalhado em ambientes de produção sem a necessidade de reinicializações ou reinicializações do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a877f-110">ETW can enable and disable logging dynamically, making it easy to perform detailed tracing in production environments without requiring reboots or application restarts.</span></span> <span data-ttu-id="a877f-111">O rastreamento de eventos de gerenciamento de memória usando o ETW tem suporte no Windows 7, Windows Server 2008 R2 e posterior.</span><span class="sxs-lookup"><span data-stu-id="a877f-111">Memory management event tracing using ETW is supported on Windows 7 , Windows Server 2008 R2, and later.</span></span> <span data-ttu-id="a877f-112">Para obter informações gerais sobre o ETW, consulte [melhorar a depuração e ajuste de desempenho com o ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span><span class="sxs-lookup"><span data-stu-id="a877f-112">For general information on ETW, see [Improve Debugging And Performance Tuning With ETW](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw).</span></span>

<span data-ttu-id="a877f-113">A lista a seguir fornece informações detalhadas para cada evento de rastreamento de gerenciamento de memória.</span><span class="sxs-lookup"><span data-stu-id="a877f-113">The following list provides detailed information for each memory management tracing event.</span></span> <span data-ttu-id="a877f-114">Para obter informações adicionais sobre qualquer evento, clique no nome do evento.</span><span class="sxs-lookup"><span data-stu-id="a877f-114">For additional information on any event, click the event name.</span></span>



| <span data-ttu-id="a877f-115">Nome do evento</span><span class="sxs-lookup"><span data-stu-id="a877f-115">Event Name</span></span>                                                  | <span data-ttu-id="a877f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a877f-116">Description</span></span>                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------|
| [<span data-ttu-id="a877f-117">**\_alocação de \_ evento de heap do ETW \_**</span><span class="sxs-lookup"><span data-stu-id="a877f-117">**ETW\_HEAP\_EVENT\_ALLOC**</span></span>](etw-heap-event-alloc.md)     | <span data-ttu-id="a877f-118">Evento de rastreamento de gerenciamento de memória para uma operação de alocação de heap.</span><span class="sxs-lookup"><span data-stu-id="a877f-118">Memory management tracing event for a heap allocation operation.</span></span>    |
| [<span data-ttu-id="a877f-119">**evento de heap de ETW \_ \_ \_ gratuito**</span><span class="sxs-lookup"><span data-stu-id="a877f-119">**ETW\_HEAP\_EVENT\_FREE**</span></span>](etw-heap-event-free.md)       | <span data-ttu-id="a877f-120">Evento de rastreamento de gerenciamento de memória para uma operação de heap livre.</span><span class="sxs-lookup"><span data-stu-id="a877f-120">Memory management tracing event for a heap free operation.</span></span>          |
| [<span data-ttu-id="a877f-121">**realocação de evento de \_ heap ETW \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a877f-121">**ETW\_HEAP\_EVENT\_REALLOC**</span></span>](etw-heap-event-realloc.md) | <span data-ttu-id="a877f-122">Evento de rastreamento de gerenciamento de memória para uma operação de realocação de heap.</span><span class="sxs-lookup"><span data-stu-id="a877f-122">Memory management tracing event for a heap re-allocation operation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="a877f-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a877f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a877f-124">Melhore o ajuste de depuração e desempenho com o ETW</span><span class="sxs-lookup"><span data-stu-id="a877f-124">Improve Debugging And Performance Tuning With ETW</span></span>](/archive/msdn-magazine/2007/april/event-tracing-improve-debugging-and-performance-tuning-with-etw)
</dt> </dl>

 

 
