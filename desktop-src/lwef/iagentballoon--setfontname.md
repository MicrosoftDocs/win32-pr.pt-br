---
title: IAgentBalloon setnomedafonte
description: IAgentBalloon setnomedafonte
ms.assetid: 6babf5f6-2abd-46c2-ade0-899a8e4488bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f983064c5df8cde8322658bbd0c713bbf238ecf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006103"
---
# <a name="iagentballoonsetfontname"></a><span data-ttu-id="15d75-103">IAgentBalloon:: setnomedafontename</span><span class="sxs-lookup"><span data-stu-id="15d75-103">IAgentBalloon::SetFontName</span></span>

<span data-ttu-id="15d75-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="15d75-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font displayed in word balloon
);
                   
```

<span data-ttu-id="15d75-105">Define a fonte exibida no balão de palavras.</span><span class="sxs-lookup"><span data-stu-id="15d75-105">Sets the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="15d75-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="15d75-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="15d75-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span><span class="sxs-lookup"><span data-stu-id="15d75-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="15d75-108">Um BSTR que define a fonte exibida no balão de palavras.</span><span class="sxs-lookup"><span data-stu-id="15d75-108">A BSTR that sets the font displayed in the word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="15d75-109">A fonte padrão usada no balão de palavras de um caractere é definida no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="15d75-109">The default font used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="15d75-110">Você pode alterá-lo com **IAgentBalloon:: setnomedafonte**.</span><span class="sxs-lookup"><span data-stu-id="15d75-110">You can change it with **IAgentBalloon::SetFontName**.</span></span> <span data-ttu-id="15d75-111">No entanto, o usuário pode substituir a configuração de fonte para todos os caracteres usando a folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="15d75-111">However, the user can override the font setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="15d75-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="15d75-112">See Also</span></span>

[<span data-ttu-id="15d75-113">**IAgentBalloon:: getVisible**</span><span class="sxs-lookup"><span data-stu-id="15d75-113">**IAgentBalloon::GetVisible**</span></span>](iagentballoon--getvisible.md)


 

 




