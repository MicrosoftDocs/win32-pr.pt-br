---
title: Suporte ao balão do Word
description: Suporte ao balão do Word
ms.assetid: deac032f-0480-4a0d-bc69-e26f12666bbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78316c509ece6fc8f9b0cefd50b1564a50697a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159576"
---
# <a name="word-balloon-support"></a><span data-ttu-id="94427-103">Suporte ao balão do Word</span><span class="sxs-lookup"><span data-stu-id="94427-103">Word Balloon Support</span></span>

<span data-ttu-id="94427-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="94427-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="94427-105">A saída falada também pode aparecer como saída textual na forma de um balão de palavras de desenho.</span><span class="sxs-lookup"><span data-stu-id="94427-105">Spoken output can also appear as textual output in the form of a cartoon word balloon.</span></span> <span data-ttu-id="94427-106">Isso pode ser usado para complementar a saída falada de um caractere ou como uma alternativa à saída de áudio quando você usa o método [**Speak**](speak-method.md) .</span><span class="sxs-lookup"><span data-stu-id="94427-106">This can be used to supplement the spoken output of a character or as an alternative to audio output when you use the [**Speak**](speak-method.md) method.</span></span>

![Sim balão de palavras mestras](images/f3ballon.gif)

<span data-ttu-id="94427-108">Você também pode usar um balão de palavra para comunicar o que um caractere está "pensando" usando o método [**Think**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="94427-108">You can also use a word balloon to communicate what a character is "thinking" using the [**Think**](think-method.md) method.</span></span> <span data-ttu-id="94427-109">Isso exibe o texto que você fornece em um balão ainda "pensado".</span><span class="sxs-lookup"><span data-stu-id="94427-109">This displays the text you supply in a still "thought" balloon.</span></span> <span data-ttu-id="94427-110">O método **Think** também difere do método [**Speak**](speak-method.md) , pois ele não produz nenhuma saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="94427-110">The **Think** method also differs from the [**Speak**](speak-method.md) method in that it produces no audio output.</span></span>

<span data-ttu-id="94427-111">Os balões de palavras dão suporte apenas à comunicação com legendas do caractere, não à entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="94427-111">Word balloons support only captioned communication from the character, not user input.</span></span> <span data-ttu-id="94427-112">Portanto, o balão de palavras não dá suporte a controles de entrada.</span><span class="sxs-lookup"><span data-stu-id="94427-112">Therefore, the word balloon does not support input controls.</span></span> <span data-ttu-id="94427-113">No entanto, você pode fornecer facilmente a entrada do usuário para um caractere, usando interfaces da linguagem de programação ou outros serviços de entrada fornecidos pelo Microsoft Agent, como o menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="94427-113">However, you can easily provide user input for a character, using interfaces from your programming language or the other input services provided by Microsoft Agent, such as the pop-up menu.</span></span>

<span data-ttu-id="94427-114">Ao definir um caractere, você pode especificar se deseja incluir o suporte ao balão do Word.</span><span class="sxs-lookup"><span data-stu-id="94427-114">When you define a character, you can specify whether to include word balloon support.</span></span> <span data-ttu-id="94427-115">No entanto, se você usar um caractere que inclua suporte a balão de palavras, não será possível desabilitar o suporte.</span><span class="sxs-lookup"><span data-stu-id="94427-115">However, if you use a character that includes word balloon support, you cannot disable the support.</span></span>

 

 




