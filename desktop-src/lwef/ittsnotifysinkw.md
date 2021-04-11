---
title: ITTSNotifySinkW
description: ITTSNotifySinkW
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5820f262779f86deeeca9982d0551b16d3a3406
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365637"
---
# <a name="ittsnotifysinkw"></a><span data-ttu-id="4e7dc-103">ITTSNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="4e7dc-103">ITTSNotifySinkW</span></span>

<span data-ttu-id="4e7dc-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4e7dc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="4e7dc-105">O mecanismo deve chamar de [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**)e [**Visual**](https://www.bing.com/search?q=**Visual**).</span><span class="sxs-lookup"><span data-stu-id="4e7dc-105">The engine must call out through [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**), and [**Visual**](https://www.bing.com/search?q=**Visual**).</span></span> <span data-ttu-id="4e7dc-106">O retorno de chamada **Visual** deve fornecer fonemas IPA.</span><span class="sxs-lookup"><span data-stu-id="4e7dc-106">The **Visual** callback must provide IPA phonemes.</span></span> <span data-ttu-id="4e7dc-107">(O alfabeto \[ fonético internacional IPA \] é uma notação universal para descrever o conteúdo fonético da comunicação falada.</span><span class="sxs-lookup"><span data-stu-id="4e7dc-107">(The International Phonetic Alphabet \[IPA\] is a universal notation for describing the phonetic content of spoken communication.</span></span> <span data-ttu-id="4e7dc-108">Todos os fonemas de Altova que têm representações no IPA.</span><span class="sxs-lookup"><span data-stu-id="4e7dc-108">All speakable phonemes have representations in IPA.</span></span> <span data-ttu-id="4e7dc-109">Os detalhes de IPA estão na parte de especificação do Microsoft Speech API \[ do Speech SDK 4,0 download \] em [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) .)</span><span class="sxs-lookup"><span data-stu-id="4e7dc-109">Details of IPA are in the Microsoft Speech API specification \[part of the Speech SDK 4.0 download\] at [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx).)</span></span>

<span data-ttu-id="4e7dc-110">Embora a notificação [**Visual**](https://www.bing.com/search?q=**Visual**) seja bastante rica, o Microsoft Agent usa apenas o valor **cIPAPhoneme** para animar a boca à medida que o caractere fala.</span><span class="sxs-lookup"><span data-stu-id="4e7dc-110">Although the [**Visual**](https://www.bing.com/search?q=**Visual**) notification is fairly rich, Microsoft Agent uses only the **cIPAPhoneme** value to animate the mouth as the character speaks.</span></span> <span data-ttu-id="4e7dc-111">Qualquer mecanismo compatível com o Microsoft Agent deve fornecer um fluxo de notificações **visuais** bem sincronizado que reflete o conteúdo fonético do expressão produzido.</span><span class="sxs-lookup"><span data-stu-id="4e7dc-111">Any Microsoft Agent-compatible engine must provide a closely synchronized stream of **Visual** notifications reflecting the phonetic content of the produced utterance.</span></span> <span data-ttu-id="4e7dc-112">Nesse caso, "notificação relativamente oportuna" não é adequada, pois os ouvintes dos palestrantes são bastante sensíveis a discrepâncias entre a posição da boca e o conteúdo acústico.</span><span class="sxs-lookup"><span data-stu-id="4e7dc-112">In this case, "relatively timely notification" is not adequate, because speaker-hearers are fairly sensitive to discrepancies between mouth position and acoustic content.</span></span> <span data-ttu-id="4e7dc-113">As notificações **visuais** precisam ser retornadas imediatamente.</span><span class="sxs-lookup"><span data-stu-id="4e7dc-113">**Visual** notifications need to be returned promptly.</span></span>

 

 




