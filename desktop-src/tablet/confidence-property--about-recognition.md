---
description: Para obter um nível de confiança para cada resultado de reconhecimento, você pode obter a propriedade int do objeto RecognitionAlternate ou a propriedade int do objeto Gesture.
ms.assetid: b2495c5b-6db4-401c-ab7a-6556c55bbe46
title: Propriedade de confiança [sobre reconhecimento]
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f436d17d5cb83901c7d19ef4beb6dfb7ce6199
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826788"
---
# <a name="confidence-property-about-recognition"></a><span data-ttu-id="1cfd1-103">Propriedade de confiança \[ sobre reconhecimento\]</span><span class="sxs-lookup"><span data-stu-id="1cfd1-103">Confidence Property \[About Recognition\]</span></span>

<span data-ttu-id="1cfd1-104">Para obter um nível de confiança para cada resultado de reconhecimento, você pode obter a propriedade [**int**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) do objeto [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) ou a propriedade [**int**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) do objeto [**Gesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) .</span><span class="sxs-lookup"><span data-stu-id="1cfd1-104">To obtain a level of confidence for each recognition result, you can get either the [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence) property of the [**RecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) object or the [**Confidence**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkgesture-get_confidence) property of the [**Gesture**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkgesture) object.</span></span> <span data-ttu-id="1cfd1-105">O nível de confiança é um número que indica o grau de confiança para cada resultado de reconhecimento alternativo que o reconhecedor retorna para um segmento de reconhecimento correspondente.</span><span class="sxs-lookup"><span data-stu-id="1cfd1-105">The confidence level is a number that indicates the degree of confidence for each alternate recognition result that the recognizer returns for a corresponding recognition segment.</span></span>

<span data-ttu-id="1cfd1-106">A confiança é retornada como baixa, média ou alta.</span><span class="sxs-lookup"><span data-stu-id="1cfd1-106">Confidence is returned as low, average, or high.</span></span> <span data-ttu-id="1cfd1-107">O aplicativo usa esses resultados para:</span><span class="sxs-lookup"><span data-stu-id="1cfd1-107">The application uses these results to:</span></span>

-   <span data-ttu-id="1cfd1-108">Indique ao usuário que existem várias possibilidades.</span><span class="sxs-lookup"><span data-stu-id="1cfd1-108">Indicate to the user that multiple possibilities exist.</span></span>
-   <span data-ttu-id="1cfd1-109">Classifique as alternativas por nível de confiança.</span><span class="sxs-lookup"><span data-stu-id="1cfd1-109">Rank the alternates by confidence level.</span></span>

## <a name="what-affects-confidence"></a><span data-ttu-id="1cfd1-110">O que afeta a confiança</span><span class="sxs-lookup"><span data-stu-id="1cfd1-110">What Affects Confidence</span></span>

<span data-ttu-id="1cfd1-111">Algumas das coisas que dificultam o reconhecimento de manuscrito e que afetam a confiança incluem:</span><span class="sxs-lookup"><span data-stu-id="1cfd1-111">Some of the things that make handwriting recognition difficult and affect confidence include:</span></span>

-   <span data-ttu-id="1cfd1-112">Dificuldade para determinar a segmentação de palavras</span><span class="sxs-lookup"><span data-stu-id="1cfd1-112">Difficulty determining word segmentation</span></span>

![imagem mostrando a gravação que está muito próxima](images/5c5d1c42-cbd1-46d0-a6f8-653f204f52cd.jpg)

-   <span data-ttu-id="1cfd1-114">Dificuldades de caso</span><span class="sxs-lookup"><span data-stu-id="1cfd1-114">Case difficulties</span></span>

![imagem mostrando dificuldades com versões manuscritas da palavra "Case"](images/1bdfb2e3-06ac-4c49-a39b-f0be51aed0e8.jpg)

-   <span data-ttu-id="1cfd1-116">Estilos de escrita incomuns</span><span class="sxs-lookup"><span data-stu-id="1cfd1-116">Uncommon writing styles</span></span>
-   <span data-ttu-id="1cfd1-117">Pontuação isolada</span><span class="sxs-lookup"><span data-stu-id="1cfd1-117">Isolated punctuation</span></span>

![imagem mostrando aspas que estão muito longe do texto](images/743364b3-af62-4775-9d0d-f13f6e36c922.jpg)

-   <span data-ttu-id="1cfd1-119">Caracteres acentuados em reconhecedores em inglês</span><span class="sxs-lookup"><span data-stu-id="1cfd1-119">Accented characters in English recognizers</span></span>

> [!Note]  
> <span data-ttu-id="1cfd1-120">A avaliação de confiança está disponível somente para o Estados Unidos Inglês e todos os reconhecedores de gesto nesta versão.</span><span class="sxs-lookup"><span data-stu-id="1cfd1-120">Confidence evaluation is available only for United States English and all gesture recognizers in this release.</span></span> <span data-ttu-id="1cfd1-121">Os métodos que fornecem a propriedade de confiança para qualquer outro reconhecedor retornarão **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="1cfd1-121">Methods that provide the confidence property for any other recognizer will return **E\_NOTIMPL**.</span></span>

 

 

 



