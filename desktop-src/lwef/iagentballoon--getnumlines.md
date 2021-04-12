---
title: IAgentBalloon GetNumLines
description: IAgentBalloon GetNumLines
ms.assetid: 82deeed0-d4a7-46e4-9077-edd933dcf4e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d66c18d75af77a2559efc86f775710fb32e6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364407"
---
# <a name="iagentballoongetnumlines"></a><span data-ttu-id="e7d62-103">IAgentBalloon::GetNumLines</span><span class="sxs-lookup"><span data-stu-id="e7d62-103">IAgentBalloon::GetNumLines</span></span>

<span data-ttu-id="e7d62-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e7d62-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetNumLines(
   long * pcLines  // address of variable for number of lines 
);                  // displayed in word balloon
```

<span data-ttu-id="e7d62-105">Recupera o valor do número de linhas exibidas em um balão de palavras.</span><span class="sxs-lookup"><span data-stu-id="e7d62-105">Retrieves the value of the number of lines displayed in a word balloon.</span></span>

-   <span data-ttu-id="e7d62-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e7d62-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e7d62-107"><span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*</span><span class="sxs-lookup"><span data-stu-id="e7d62-107"><span id="pcLines"></span><span id="pclines"></span><span id="PCLINES"></span>*pcLines*</span></span>
</dt> <dd>

<span data-ttu-id="e7d62-108">O endereço de uma variável que recebe o número de linhas exibidas.</span><span class="sxs-lookup"><span data-stu-id="e7d62-108">The address of a variable that receives the number of lines displayed.</span></span>

</dd> </dl>

<span data-ttu-id="e7d62-109">O servidor do Microsoft Agent rola automaticamente as linhas exibidas para a saída falada na palavra balão.</span><span class="sxs-lookup"><span data-stu-id="e7d62-109">The Microsoft Agent server automatically scrolls the lines displayed for spoken output in the word balloon.</span></span> <span data-ttu-id="e7d62-110">O número de linhas para um balão de palavras de caracteres é definido no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="e7d62-110">The number of lines for a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="e7d62-111">Ele não pode ser alterado por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e7d62-111">It cannot be changed by an application.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7d62-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="e7d62-112">See Also</span></span>

[<span data-ttu-id="e7d62-113">**IAgentBalloon::GetNumCharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="e7d62-113">**IAgentBalloon::GetNumCharsPerLine**</span></span>](iagentballoon--getnumcharsperline.md)


 

 




