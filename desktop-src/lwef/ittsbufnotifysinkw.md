---
title: ITTSBufNotifySinkW
description: ITTSBufNotifySinkW
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a1ce3013ba1d8acf01f79b4f71d2d5088f4d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916574"
---
# <a name="ittsbufnotifysinkw"></a><span data-ttu-id="f5fd3-103">ITTSBufNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="f5fd3-103">ITTSBufNotifySinkW</span></span>

<span data-ttu-id="f5fd3-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f5fd3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="f5fd3-105">O mecanismo deve chamar o **indicador**.</span><span class="sxs-lookup"><span data-stu-id="f5fd3-105">The engine must call out through **BookMark**.</span></span> <span data-ttu-id="f5fd3-106">Durante o pré-processamento da saída de fala, o código do Microsoft Agent insere indicadores entre "palavras" e usa a chegada desses indicadores para impulsionar o ritmo do texto na palavra balão.</span><span class="sxs-lookup"><span data-stu-id="f5fd3-106">During preprocessing of speech output, Microsoft Agent code inserts bookmarks between "words" and uses the arrival of those bookmarks to drive the pacing of text in the word balloon.</span></span> <span data-ttu-id="f5fd3-107">Embora SAPI não exija nada mais do que a chegada desses indicadores em algum momento antes do final do expressão, os indicadores devem ser retornados de forma relativamente oportuna para dar suporte ao Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="f5fd3-107">While SAPI does not require anything more than the arrival of those bookmarks at some time before the end of the utterance, the bookmarks must be returned in a relatively timely fashion to support Microsoft Agent.</span></span>

<span data-ttu-id="f5fd3-108">Observe que não há um conceito estrito de "Word" em algumas linguagens, como o japonês.</span><span class="sxs-lookup"><span data-stu-id="f5fd3-108">Note that there is no strict concept of "word" in some languages, such as Japanese.</span></span> <span data-ttu-id="f5fd3-109">O método [**Speak**](speak-method.md) do Microsoft Agent define uma "palavra" como uma cadeia de caracteres conectada de símbolos que tem um significado e uma pronúncia isoladamente.</span><span class="sxs-lookup"><span data-stu-id="f5fd3-109">Microsoft Agent's [**Speak**](speak-method.md) method defines a "word" as a connected string of symbols that has a meaning and pronunciation in isolation.</span></span> <span data-ttu-id="f5fd3-110">O Microsoft Agent usa um código de análise bastante simples para determinar o que é uma "palavra": ele procura símbolos separados por espaço em branco.</span><span class="sxs-lookup"><span data-stu-id="f5fd3-110">Microsoft Agent uses fairly simple parsing code to determine what a "word" is: it looks for symbols separated by white space.</span></span> <span data-ttu-id="f5fd3-111">Portanto, há três "palavras" na cadeia de caracteres em inglês "The 101 Dalmatians": "," 101 "e" Dalmatians ".</span><span class="sxs-lookup"><span data-stu-id="f5fd3-111">Thus, there are three "words" in the English string "The 101 Dalmatians": "the", "one hundred and one", and "Dalmatians".</span></span> <span data-ttu-id="f5fd3-112">O texto incluído na marca de mapa do Microsoft Agent é tratado como uma única "palavra" para fins de exibição.</span><span class="sxs-lookup"><span data-stu-id="f5fd3-112">Text included in the Microsoft Agent Map tag is treated as a single "word" for display purposes.</span></span>

 

 




