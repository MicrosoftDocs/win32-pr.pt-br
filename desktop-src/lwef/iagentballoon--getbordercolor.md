---
title: IAgentBalloon getbordercolor
description: IAgentBalloon getbordercolor
ms.assetid: e6c592c3-0e14-474f-a829-6028f2de5791
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f78bf9425cbb12c6a87f3ad64b6c5523dc7bbd8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636417"
---
# <a name="iagentballoongetbordercolor"></a><span data-ttu-id="96f94-103">IAgentBalloon:: getbordercolor</span><span class="sxs-lookup"><span data-stu-id="96f94-103">IAgentBalloon::GetBorderColor</span></span>

<span data-ttu-id="96f94-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="96f94-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetBorderColor (
  long * plBorderColor// address of variable for border color displayed
);                    // for word balloon
```

<span data-ttu-id="96f94-105">Recupera o valor da cor de borda exibida para um balão de palavras.</span><span class="sxs-lookup"><span data-stu-id="96f94-105">Retrieves the value for the border color displayed for a word balloon.</span></span>

-   <span data-ttu-id="96f94-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="96f94-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="96f94-107"><span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*</span><span class="sxs-lookup"><span data-stu-id="96f94-107"><span id="plBorderColor"></span><span id="plbordercolor"></span><span id="PLBORDERCOLOR"></span>*plBorderColor*</span></span>
</dt> <dd>

<span data-ttu-id="96f94-108">O endereço de uma variável que recebe a configuração de cor para a borda do balão.</span><span class="sxs-lookup"><span data-stu-id="96f94-108">The address of a variable that receives the color setting for the balloon border.</span></span>

</dd> </dl>

<span data-ttu-id="96f94-109">A cor da borda de um balão de palavras de caracteres é definida no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="96f94-109">The border color for a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="96f94-110">Ele não pode ser alterado por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="96f94-110">It cannot be changed by an application.</span></span> <span data-ttu-id="96f94-111">No entanto, o usuário pode alterar a cor da borda dos balões de palavras para todos os caracteres por meio da folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="96f94-111">However, the user can change the border color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="96f94-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="96f94-112">See Also</span></span>

<span data-ttu-id="96f94-113">[**IAgentBalloon:: GetBackColor**](iagentballoon--getbackcolor.md), [ **IAgentBalloon:: GetForeColor**](iagentballoon--getforecolor.md)</span><span class="sxs-lookup"><span data-stu-id="96f94-113">[**IAgentBalloon::GetBackColor**](iagentballoon--getbackcolor.md), [**IAgentBalloon::GetForeColor**](iagentballoon--getforecolor.md)</span></span>


 

 




