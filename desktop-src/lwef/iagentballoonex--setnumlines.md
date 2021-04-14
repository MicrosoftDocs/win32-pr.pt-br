---
title: IAgentBalloonEx SetNumLines
description: IAgentBalloonEx SetNumLines
ms.assetid: 350fd273-a941-4454-a309-045d19ed8f59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45c012d0193a0bd21ba203418920b87b2fac81b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453680"
---
# <a name="iagentballoonexsetnumlines"></a><span data-ttu-id="ea299-103">IAgentBalloonEx::SetNumLines</span><span class="sxs-lookup"><span data-stu-id="ea299-103">IAgentBalloonEx::SetNumLines</span></span>

<span data-ttu-id="ea299-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ea299-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetNumLines(
   long lLines,  // number of lines setting
);
```

<span data-ttu-id="ea299-105">Define o número de linhas de saída de texto que podem ser exibidas no balão de palavras do caractere.</span><span class="sxs-lookup"><span data-stu-id="ea299-105">Sets the number of lines of text output that can be displayed in the character's word balloon.</span></span>

-   <span data-ttu-id="ea299-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ea299-106">Returns S\_OK to indicate the operation was successful.</span></span>
-   <span data-ttu-id="ea299-107">Retorna E \_ INVALIDARG se o parâmetro for zero.</span><span class="sxs-lookup"><span data-stu-id="ea299-107">Returns E\_INVALIDARG if the parameter is zero.</span></span>

<dl> <dt>

<span data-ttu-id="ea299-108"><span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*</span><span class="sxs-lookup"><span data-stu-id="ea299-108"><span id="lLines"></span><span id="llines"></span><span id="LLINES"></span>*lLines*</span></span>
</dt> <dd>

<span data-ttu-id="ea299-109">Número de linhas a serem exibidas na palavra balão.</span><span class="sxs-lookup"><span data-stu-id="ea299-109">Number of lines to display in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="ea299-110">A configuração mínima é 1 e o máximo é 128.</span><span class="sxs-lookup"><span data-stu-id="ea299-110">The minimum setting is 1 and maximum is 128.</span></span> <span data-ttu-id="ea299-111">Se o texto especificado no método [**Speak**](speak-method.md) ou [**Think**](think-method.md) exceder o tamanho do balão atual, o Agent rolará automaticamente o texto no balão.</span><span class="sxs-lookup"><span data-stu-id="ea299-111">If the text specified in the [**Speak**](speak-method.md) or [**Think**](think-method.md) method exceeds the size of the current balloon, Agent automatically scrolls the text in the balloon.</span></span>

<span data-ttu-id="ea299-112">Esse método falhará se o bit do estilo de balão **SizeToText** estiver definido.</span><span class="sxs-lookup"><span data-stu-id="ea299-112">This method will fail if the **SizeToText** balloon style bit is set.</span></span>

<span data-ttu-id="ea299-113">A configuração padrão é baseada em configurações quando o caractere é compilado com o editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="ea299-113">The default setting is based on settings when the character is compiled with the Microsoft Agent Character Editor.</span></span>

## <a name="see-also"></a><span data-ttu-id="ea299-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ea299-114">See Also</span></span>

<span data-ttu-id="ea299-115">[**IAgentBalloon:: GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx:: GetStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx:: SetStyle**](iagentballoonex--setstyle.md)</span><span class="sxs-lookup"><span data-stu-id="ea299-115">[**IAgentBalloon::GetNumLines**](iagentballoon--getnumlines.md), [**IAgentBalloonEx::GetStyle**](iagentballoonex--getstyle.md), [**IAgentBalloonEx::SetStyle**](iagentballoonex--setstyle.md)</span></span>


 

 




