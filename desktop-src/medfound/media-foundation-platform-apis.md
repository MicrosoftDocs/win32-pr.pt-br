---
description: APIs da plataforma Media Foundation
ms.assetid: 1eb20c44-58cb-4e34-a108-1b3c27d54ff1
title: APIs da plataforma Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed1e8d8aa0dcd5d7b1184a406e09910a98892f4f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105812410"
---
# <a name="media-foundation-platform-apis"></a><span data-ttu-id="a55db-103">APIs da plataforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a55db-103">Media Foundation Platform APIs</span></span>

<span data-ttu-id="a55db-104">A camada de plataforma de Media Foundation contém primitivos e objetos auxiliares usados pelas outras camadas.</span><span class="sxs-lookup"><span data-stu-id="a55db-104">The platform layer of Media Foundation contains primitives and helper objects used by the other layers.</span></span>

<span data-ttu-id="a55db-105">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="a55db-105">This section contains the following topics:</span></span>



| <span data-ttu-id="a55db-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="a55db-106">Topic</span></span>                                                                           | <span data-ttu-id="a55db-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a55db-107">Description</span></span>                                                                                                                                                       |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a55db-108">Inicializando a plataforma de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a55db-108">Initializing the Media Foundation Platform</span></span>](initializing-media-foundation.md) | <span data-ttu-id="a55db-109">Como inicializar a plataforma de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a55db-109">How to initialize the Media Foundation platform.</span></span>                                                                                                                  |
| [<span data-ttu-id="a55db-110">Media Foundation e COM</span><span class="sxs-lookup"><span data-stu-id="a55db-110">Media Foundation and COM</span></span>](media-foundation-and-com.md)                        | <span data-ttu-id="a55db-111">Descreve a interação entre COM e Microsoft Media Foundation e define algumas práticas recomendadas a serem usadas ao desenvolver Media Foundation componentes de plug-in.</span><span class="sxs-lookup"><span data-stu-id="a55db-111">Describes the interaction between COM and Microsoft Media Foundation, and defines some best practices to use when developing Media Foundation plug-in components.</span></span> |
| [<span data-ttu-id="a55db-112">Métodos de retorno de chamada assíncrono</span><span class="sxs-lookup"><span data-stu-id="a55db-112">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)              | <span data-ttu-id="a55db-113">Como chamar métodos assíncronos e como implementar operações assíncronas no Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a55db-113">How to call asynchronous methods and how to implement asynchronous operations in Media Foundation.</span></span>                                                                |
| [<span data-ttu-id="a55db-114">Filas de trabalho</span><span class="sxs-lookup"><span data-stu-id="a55db-114">Work Queues</span></span>](work-queues.md)                                                  | <span data-ttu-id="a55db-115">Uma fila de trabalho é uma maneira eficiente de executar operações assíncronas em outro thread.</span><span class="sxs-lookup"><span data-stu-id="a55db-115">A work queue is an efficient way to perform asynchronous operations on another thread.</span></span>                                                                            |
| [<span data-ttu-id="a55db-116">Geradores de eventos de mídia</span><span class="sxs-lookup"><span data-stu-id="a55db-116">Media Event Generators</span></span>](media-event-generators.md)                            | <span data-ttu-id="a55db-117">Como receber eventos assíncronos e como gerar eventos no Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a55db-117">How to receive asynchronous events and how to raise events in Media Foundation.</span></span>                                                                                   |
| [<span data-ttu-id="a55db-118">Interfaces de serviço</span><span class="sxs-lookup"><span data-stu-id="a55db-118">Service Interfaces</span></span>](service-interfaces.md)                                    | <span data-ttu-id="a55db-119">Uma interface de serviço é uma interface COM fornecida por um objeto, mas exposta ao aplicativo por meio de outro objeto.</span><span class="sxs-lookup"><span data-stu-id="a55db-119">A service interface is a COM interface provided by one object, but exposed to the application through another object.</span></span>                                             |
| [<span data-ttu-id="a55db-120">Objetos de ativação</span><span class="sxs-lookup"><span data-stu-id="a55db-120">Activation Objects</span></span>](activation-objects.md)                                    | <span data-ttu-id="a55db-121">Um objeto de ativação é um objeto que cria outro objeto.</span><span class="sxs-lookup"><span data-stu-id="a55db-121">An activation object is an object that creates another object.</span></span>                                                                                                    |
| [<span data-ttu-id="a55db-122">Relógio de apresentação</span><span class="sxs-lookup"><span data-stu-id="a55db-122">Presentation Clock</span></span>](presentation-clock.md)                                    | <span data-ttu-id="a55db-123">O relógio de apresentação gera o tempo de relógio usado para controlar a reprodução e também para fluxos de áudio e vídeo síncronos.</span><span class="sxs-lookup"><span data-stu-id="a55db-123">The presentation clock generates the clock time that is used to control playback, and also to synchronous audio and video streams.</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="a55db-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a55db-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a55db-125">Arquitetura Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a55db-125">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="a55db-126">Guia de programação Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a55db-126">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 



