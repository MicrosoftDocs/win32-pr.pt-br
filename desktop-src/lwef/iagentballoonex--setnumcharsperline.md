---
title: IAgentBalloonEx SetNumCharsPerLine
description: IAgentBalloonEx SetNumCharsPerLine
ms.assetid: 44025b6b-ed42-4476-b841-c244accf0f83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a44abe14de6bb1cef631a51b4516d083657016
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292651"
---
# <a name="iagentballoonexsetnumcharsperline"></a><span data-ttu-id="6bb74-103">IAgentBalloonEx::SetNumCharsPerLine</span><span class="sxs-lookup"><span data-stu-id="6bb74-103">IAgentBalloonEx::SetNumCharsPerLine</span></span>

<span data-ttu-id="6bb74-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6bb74-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetNumCharsPerLine(
   long lCharsPerLine,  // number of characters per line setting
);
```

<span data-ttu-id="6bb74-105">Define o número de caracteres por linha que podem ser exibidos no balão de palavras do caractere.</span><span class="sxs-lookup"><span data-stu-id="6bb74-105">Sets the number of characters per line that can be displayed in the character's word balloon.</span></span>

-   <span data-ttu-id="6bb74-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6bb74-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="6bb74-107">Retorna E \_ INVALIDARG se o parâmetro for menor que oito.</span><span class="sxs-lookup"><span data-stu-id="6bb74-107">Returns E\_INVALIDARG if the parameter is less than eight.</span></span>

<dl> <dt>

<span data-ttu-id="6bb74-108"><span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*</span><span class="sxs-lookup"><span data-stu-id="6bb74-108"><span id="lCharsPerLine"></span><span id="lcharsperline"></span><span id="LCHARSPERLINE"></span>*lCharsPerLine*</span></span>
</dt> <dd>

<span data-ttu-id="6bb74-109">Número de linhas a serem exibidas na palavra balão.</span><span class="sxs-lookup"><span data-stu-id="6bb74-109">Number of lines to display in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="6bb74-110">A configuração mínima é 8 e o máximo é 255.</span><span class="sxs-lookup"><span data-stu-id="6bb74-110">The minimum setting is 8 and the maximum is 255.</span></span> <span data-ttu-id="6bb74-111">Se o texto especificado no método [**Speak**](speak-method.md) ou [**Think**](think-method.md) exceder o tamanho do balão atual, o Agent rolará automaticamente o texto no balão.</span><span class="sxs-lookup"><span data-stu-id="6bb74-111">If the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method exceeds the size of the current balloon, Agent automatically scrolls the text in the balloon.</span></span>

<span data-ttu-id="6bb74-112">A configuração padrão é baseada em configurações quando o caractere é compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="6bb74-112">The default setting is based on settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="6bb74-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="6bb74-113">See Also</span></span>

[<span data-ttu-id="6bb74-114">**IAgentBalloon::GetNumCharsPerLine**</span><span class="sxs-lookup"><span data-stu-id="6bb74-114">**IAgentBalloon::GetNumCharsPerLine**</span></span>](iagentballoon--getnumcharsperline.md)


 

 




