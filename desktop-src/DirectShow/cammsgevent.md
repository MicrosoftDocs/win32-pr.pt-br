---
description: A classe CAMMsgEvent é um wrapper para objetos de evento que executam o processamento de mensagens.
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: Classe CAMMsgEvent (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ebac7aae11f7a7b7d6b846e262e93b5759210b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787433"
---
# <a name="cammsgevent-class"></a><span data-ttu-id="a8fad-103">Classe CAMMsgEvent</span><span class="sxs-lookup"><span data-stu-id="a8fad-103">CAMMsgEvent class</span></span>

![hierarquia de classe CAMMsgEvent](images/util06.png)

<span data-ttu-id="a8fad-105">A `CAMMsgEvent` classe é um wrapper para objetos de evento que executam o processamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a8fad-105">The `CAMMsgEvent` class is a wrapper for event objects that perform message processing.</span></span>

<span data-ttu-id="a8fad-106">Essa classe deriva do objeto [**CAMEvent**](camevent.md) .</span><span class="sxs-lookup"><span data-stu-id="a8fad-106">This class derives from the [**CAMEvent**](camevent.md) object.</span></span> <span data-ttu-id="a8fad-107">Ele adiciona um método, [**CAMMsgEvent:: WaitMsg**](cammsgevent-waitmsg.md), que despacha mensagens de entrada enquanto aguarda.</span><span class="sxs-lookup"><span data-stu-id="a8fad-107">It adds one method, [**CAMMsgEvent::WaitMsg**](cammsgevent-waitmsg.md), which dispatches incoming messages while waiting.</span></span>



| <span data-ttu-id="a8fad-108">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="a8fad-108">Public Methods</span></span>                                 | <span data-ttu-id="a8fad-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8fad-109">Description</span></span>                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="a8fad-110">**CAMMsgEvent**</span><span class="sxs-lookup"><span data-stu-id="a8fad-110">**CAMMsgEvent**</span></span>](cammsgevent-cammsgevent.md) | <span data-ttu-id="a8fad-111">Construtor.</span><span class="sxs-lookup"><span data-stu-id="a8fad-111">Constructor.</span></span>                                                         |
| [<span data-ttu-id="a8fad-112">**WaitMsg**</span><span class="sxs-lookup"><span data-stu-id="a8fad-112">**WaitMsg**</span></span>](cammsgevent-waitmsg.md)         | <span data-ttu-id="a8fad-113">Aguarda o evento ser sinalizado, durante a expedição de mensagens enviadas.</span><span class="sxs-lookup"><span data-stu-id="a8fad-113">Waits for the event to be signaled, while dispatching sent messages.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="a8fad-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8fad-114">Requirements</span></span>



| <span data-ttu-id="a8fad-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8fad-115">Requirement</span></span> | <span data-ttu-id="a8fad-116">Valor</span><span class="sxs-lookup"><span data-stu-id="a8fad-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8fad-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a8fad-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a8fad-118"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8fad-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a8fad-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a8fad-119">Library</span></span><br/> | <dl> <span data-ttu-id="a8fad-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a8fad-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




