---
description: A tabela a seguir descreve quais threads os eventos do objeto RecognizerContext podem acionar. EventThreadsRecognitionFires no thread de reconhecimento em segundo plano ou no thread que chama o método Recognize do objeto RecognizerContext. RecognitionWithAlternatesFires no thread de reconhecimento em segundo plano.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: Eventos de objeto RecognizerContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc520801ae3391288966e6286d24449be4741b87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922265"
---
# <a name="recognizercontext-object-events"></a><span data-ttu-id="12813-103">Eventos de objeto RecognizerContext</span><span class="sxs-lookup"><span data-stu-id="12813-103">RecognizerContext Object Events</span></span>

<span data-ttu-id="12813-104">A tabela a seguir descreve quais threads os eventos do objeto [**RecognizerContext**](inkrecognizercontext-class.md) podem acionar.</span><span class="sxs-lookup"><span data-stu-id="12813-104">The following table describes which threads the [**RecognizerContext**](inkrecognizercontext-class.md) object events can fire on.</span></span>



| <span data-ttu-id="12813-105">Evento</span><span class="sxs-lookup"><span data-stu-id="12813-105">Event</span></span>                                                                               | <span data-ttu-id="12813-106">Threads</span><span class="sxs-lookup"><span data-stu-id="12813-106">Threads</span></span>                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12813-107">**Reconhecimento**</span><span class="sxs-lookup"><span data-stu-id="12813-107">**Recognition**</span></span>](inkrecognizercontext-recognition.md)                             | <span data-ttu-id="12813-108">Dispara no thread de reconhecimento em segundo plano ou no thread que chama o método [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) do objeto [**RecognizerContext**](inkrecognizercontext-class.md) .</span><span class="sxs-lookup"><span data-stu-id="12813-108">Fires on the background recognition thread, or on the thread which calls the [**RecognizerContext**](inkrecognizercontext-class.md) object's [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) method.</span></span><br/> |
| [<span data-ttu-id="12813-109">**RecognitionWithAlternates**</span><span class="sxs-lookup"><span data-stu-id="12813-109">**RecognitionWithAlternates**</span></span>](inkrecognizercontext-recognitionwithalternates.md) | <span data-ttu-id="12813-110">Acionado no thread de reconhecimento em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="12813-110">Fires on the background recognition thread.</span></span><br/>                                                                                                                                                               |



 

 

 




