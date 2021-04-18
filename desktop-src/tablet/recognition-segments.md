---
description: Um segmento de reconhecimento é a unidade de tinta básica que um reconhecedor usa internamente para produzir um resultado de reconhecimento para um objeto de tinta específico.
ms.assetid: 5215a0bd-6dff-4cda-b2e5-c54f64680e02
title: Segmentos de reconhecimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7037849378477950b906b85efe6980c4246421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768215"
---
# <a name="recognition-segments"></a><span data-ttu-id="31ad3-103">Segmentos de reconhecimento</span><span class="sxs-lookup"><span data-stu-id="31ad3-103">Recognition Segments</span></span>

<span data-ttu-id="31ad3-104">Um segmento de reconhecimento é a unidade de tinta básica que um reconhecedor usa internamente para produzir um resultado de reconhecimento para um objeto de tinta específico.</span><span class="sxs-lookup"><span data-stu-id="31ad3-104">A recognition segment is the basic ink unit that a recognizer uses internally to produce a recognition result for a particular Ink object.</span></span> <span data-ttu-id="31ad3-105">Um segmento de reconhecimento é uma coleção de traços de tinta.</span><span class="sxs-lookup"><span data-stu-id="31ad3-105">A recognition segment is a collection of ink strokes.</span></span> <span data-ttu-id="31ad3-106">Por exemplo, um reconhecedor capaz de reconhecer manuscritos cursivos em inglês pode usar uma palavra como o segmento de reconhecimento básico.</span><span class="sxs-lookup"><span data-stu-id="31ad3-106">For example, a recognizer that is capable of recognizing English cursive handwriting might use a word as the basic recognition segment.</span></span>

<span data-ttu-id="31ad3-107">Outros reconhecedores podem usar partes de palavras compostas como segmentos básicos.</span><span class="sxs-lookup"><span data-stu-id="31ad3-107">Other recognizers may use parts of composite words as basic segments.</span></span> <span data-ttu-id="31ad3-108">Por exemplo, em espanhol, as palavras curtas são normalmente combinadas para fornecer palavras compostas mais longas.</span><span class="sxs-lookup"><span data-stu-id="31ad3-108">For example, in Spanish, short words are commonly combined to provide longer composite words.</span></span> <span data-ttu-id="31ad3-109">"Damelo" é uma palavra em espanhol que é composta por três palavras "da minha mão" (Dê-me isso), mas é escrito como uma única palavra.</span><span class="sxs-lookup"><span data-stu-id="31ad3-109">"Damelo" is a Spanish word that is composed of three words "da me lo" (give me that), but it is written as a single word.</span></span> <span data-ttu-id="31ad3-110">Um reconhecedor de espanhol poderia reconhecer cada subpalavra como um segmento.</span><span class="sxs-lookup"><span data-stu-id="31ad3-110">A Spanish recognizer could recognize each subword as a segment.</span></span>

<span data-ttu-id="31ad3-111">Um reconhecedor pode encontrar várias maneiras de dividir uma amostra de tinta em segmentos de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="31ad3-111">A recognizer may find several ways to break an ink sample into recognition segments.</span></span> <span data-ttu-id="31ad3-112">Como a ambiguidade está envolvida no reconhecimento da entrada pretendida do usuário, o reconhecedor pode retornar muitas correspondências alternativas.</span><span class="sxs-lookup"><span data-stu-id="31ad3-112">Because ambiguity is involved in recognizing the user's intended input, the recognizer can return many alternate matches.</span></span>

<span data-ttu-id="31ad3-113">Para obter mais informações sobre alternativas, consulte [alternativas](alternates.md).</span><span class="sxs-lookup"><span data-stu-id="31ad3-113">For more information about alternates, see [Alternates](alternates.md).</span></span>

 

 



