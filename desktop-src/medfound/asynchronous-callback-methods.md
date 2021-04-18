---
description: Métodos de retorno de chamada assíncrono
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Métodos de retorno de chamada assíncrono
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0064873a5b026b6910597ebc9911f56f00584b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760634"
---
# <a name="asynchronous-callback-methods"></a><span data-ttu-id="c8432-103">Métodos de retorno de chamada assíncrono</span><span class="sxs-lookup"><span data-stu-id="c8432-103">Asynchronous Callback Methods</span></span>

<span data-ttu-id="c8432-104">Media Foundation fornece uma maneira consistente de implementar métodos assíncronos, usando uma interface de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="c8432-104">Media Foundation provides a consistent way to implement asynchronous methods, using a callback interface.</span></span>

<span data-ttu-id="c8432-105">Esta seção descreve como implementar a interface de retorno de chamada e como escrever métodos assíncronos que usam essa interface.</span><span class="sxs-lookup"><span data-stu-id="c8432-105">This section describes how to implement the callback interface and how to write asynchronous methods that use this interface.</span></span> <span data-ttu-id="c8432-106">Ele contém os tópicos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c8432-106">It contains the following topics.</span></span>



| <span data-ttu-id="c8432-107">Tópico</span><span class="sxs-lookup"><span data-stu-id="c8432-107">Topic</span></span>                                                                                | <span data-ttu-id="c8432-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8432-108">Description</span></span>                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8432-109">Chamando métodos assíncronos</span><span class="sxs-lookup"><span data-stu-id="c8432-109">Calling Asynchronous Methods</span></span>](calling-asynchronous-methods.md)                     | <span data-ttu-id="c8432-110">Como chamar métodos assíncronos no Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c8432-110">How to call asynchronous methods in Media Foundation.</span></span>                                               |
| [<span data-ttu-id="c8432-111">Implementando o retorno de chamada assíncrono</span><span class="sxs-lookup"><span data-stu-id="c8432-111">Implementing the Asynchronous Callback</span></span>](implementing-the-asynchronous-callback.md) | <span data-ttu-id="c8432-112">Como implementar o método de retorno de chamada na interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="c8432-112">How to implement the callback method in the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> |
| [<span data-ttu-id="c8432-113">Dando suporte a vários retornos de chamada</span><span class="sxs-lookup"><span data-stu-id="c8432-113">Supporting Multiple Callbacks</span></span>](supporting-multiple-callbacks.md)                   | <span data-ttu-id="c8432-114">Como dar suporte a vários retornos de chamada dentro da mesma classe C++.</span><span class="sxs-lookup"><span data-stu-id="c8432-114">How to support multiple callbacks within the same C++ class.</span></span>                                        |
| [<span data-ttu-id="c8432-115">Filas de trabalho</span><span class="sxs-lookup"><span data-stu-id="c8432-115">Work Queues</span></span>](work-queues.md)                                                       | <span data-ttu-id="c8432-116">As filas de trabalho fornecem uma maneira eficiente de executar operações assíncronas em outro thread.</span><span class="sxs-lookup"><span data-stu-id="c8432-116">Work queues provide an efficient way to perform asynchronous operations on another thread.</span></span>          |
| [<span data-ttu-id="c8432-117">Escrevendo um método assíncrono</span><span class="sxs-lookup"><span data-stu-id="c8432-117">Writing an Asynchronous Method</span></span>](writing-an-asynchronous-method.md)                 | <span data-ttu-id="c8432-118">Como implementar métodos assíncronos no Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c8432-118">How to implement asynchronous methods in Media Foundation.</span></span>                                          |
| [<span data-ttu-id="c8432-119">Objetos de resultados assíncronos personalizados</span><span class="sxs-lookup"><span data-stu-id="c8432-119">Custom Asynchronous Result Objects</span></span>](custom-asynchronous-result-objects.md)         | <span data-ttu-id="c8432-120">Como fornecer uma implementação personalizada da interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="c8432-120">How to provide a custom implementation of the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="c8432-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c8432-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8432-122">**Interface IMFAsyncCallback**</span><span class="sxs-lookup"><span data-stu-id="c8432-122">**IMFAsyncCallback Interface**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[<span data-ttu-id="c8432-123">**Interface IMFAsyncResult**</span><span class="sxs-lookup"><span data-stu-id="c8432-123">**IMFAsyncResult Interface**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[<span data-ttu-id="c8432-124">APIs da plataforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c8432-124">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



