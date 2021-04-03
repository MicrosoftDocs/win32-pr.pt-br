---
title: IAgentBalloon GetNumCharsPerLine
description: IAgentBalloon GetNumCharsPerLine
ms.assetid: ae0c7fff-8c58-465e-9b4f-3260f7574b57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 887167584c46f075bc0696c46b2dde52eb27f8d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006104"
---
# <a name="iagentballoongetnumcharsperline"></a><span data-ttu-id="3a3ef-103">IAgentBalloon::GetNumCharsPerLine</span><span class="sxs-lookup"><span data-stu-id="3a3ef-103">IAgentBalloon::GetNumCharsPerLine</span></span>

<span data-ttu-id="3a3ef-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3a3ef-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetNumCharsPerLine(
   long * plCharsPerLine  // address of variable for characters per line
);                        // displayed in word balloon
```

<span data-ttu-id="3a3ef-105">Recupera o valor para o número médio de caracteres por linha exibidos em um balão de palavras.</span><span class="sxs-lookup"><span data-stu-id="3a3ef-105">Retrieves the value for the average number of characters per line displayed in a word balloon.</span></span>

-   <span data-ttu-id="3a3ef-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="3a3ef-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3a3ef-107"><span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*</span><span class="sxs-lookup"><span data-stu-id="3a3ef-107"><span id="pbCharsPerLine"></span><span id="pbcharsperline"></span><span id="PBCHARSPERLINE"></span>*pbCharsPerLine*</span></span>
</dt> <dd>

<span data-ttu-id="3a3ef-108">O endereço de uma variável que recebe o número de caracteres por linha.</span><span class="sxs-lookup"><span data-stu-id="3a3ef-108">The address of a variable that receives the number of characters per line.</span></span>

</dd> </dl>

<span data-ttu-id="3a3ef-109">O servidor do Microsoft Agent rola automaticamente as linhas exibidas para a saída falada na palavra balão.</span><span class="sxs-lookup"><span data-stu-id="3a3ef-109">The Microsoft Agent server automatically scrolls the lines displayed for spoken output in the word balloon.</span></span> <span data-ttu-id="3a3ef-110">O número médio de caracteres por linha para o balão de palavras de um caractere é definido no editor de caracteres do agente da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3a3ef-110">The average number of characters per line for a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="3a3ef-111">Ele não pode ser alterado por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3a3ef-111">It cannot be changed by an application.</span></span>

## <a name="see-also"></a><span data-ttu-id="3a3ef-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="3a3ef-112">See Also</span></span>

[<span data-ttu-id="3a3ef-113">**IAgentBalloon::GetNumLines**</span><span class="sxs-lookup"><span data-stu-id="3a3ef-113">**IAgentBalloon::GetNumLines**</span></span>](iagentballoon--getnumlines.md)


 

 




