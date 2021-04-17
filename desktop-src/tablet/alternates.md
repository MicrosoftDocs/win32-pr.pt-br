---
description: Uma alternativa é uma correspondência de palavra potencial para um segmento de reconhecimento. Um reconhecedor gera alternativas e as baseia em correspondências aceitáveis da entrada de tinta ou áudio em um dicionário ou um factor.
ms.assetid: 69327f1d-f240-4b8a-8bee-0a96a0c425c2
title: Alternativos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350c9ac97f0af1451a0ded6445cf658dad4ee4c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756110"
---
# <a name="alternates"></a><span data-ttu-id="a8202-104">Alternativos</span><span class="sxs-lookup"><span data-stu-id="a8202-104">Alternates</span></span>

<span data-ttu-id="a8202-105">Uma alternativa é uma correspondência de palavra potencial para um segmento de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="a8202-105">An alternate is a potential word match for a recognition segment.</span></span> <span data-ttu-id="a8202-106">Um reconhecedor gera alternativas e as baseia em correspondências aceitáveis da entrada de tinta ou áudio em um dicionário ou um factor.</span><span class="sxs-lookup"><span data-stu-id="a8202-106">A recognizer generates alternates and bases them on acceptable matches of the ink or audio input against a dictionary or factoid.</span></span>

> [!Note]  
> <span data-ttu-id="a8202-107">Atualmente, a avaliação de confiança está disponível apenas para os reconhecedores de gestos (Estados Unidos) e em inglês da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a8202-107">Confidence evaluation is currently available only for the Microsoft English (United States) and gesture recognizers.</span></span>

 

<span data-ttu-id="a8202-108">Às vezes, a tinta pode ter distinções ambíguas entre segmentos.</span><span class="sxs-lookup"><span data-stu-id="a8202-108">Sometimes the ink may have ambiguous distinctions between segments.</span></span> <span data-ttu-id="a8202-109">O reconhecedor compara esses segmentos com um dicionário do reconhecedor para determinar possíveis correspondências.</span><span class="sxs-lookup"><span data-stu-id="a8202-109">The recognizer compares these segments to a recognizer dictionary to determine possible matches.</span></span> <span data-ttu-id="a8202-110">Quando o reconhecedor compara os segmentos, ele mantém uma lista de possíveis correspondências alternativas e atribui um nível de confiança a cada um, selecionando uma escolha superior.</span><span class="sxs-lookup"><span data-stu-id="a8202-110">When the recognizer compares the segments, it maintains a list of possible alternate matches and assigns a confidence level to each one, picking a top choice.</span></span>

> [!Note]  
> <span data-ttu-id="a8202-111">O reconhecedor não pode fornecer alternativas para uma parte da tinta que seja menor do que um segmento de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="a8202-111">The recognizer cannot provide alternates for a portion of ink that is smaller than a recognition segment.</span></span>

 

 

 



