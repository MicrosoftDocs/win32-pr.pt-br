---
title: IAgentBalloon setfontize
description: IAgentBalloon setfontize
ms.assetid: c38779a6-bd7f-4d3a-9cb0-9d9fac1c7996
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4984382408739e2d093226d04b1c99582a1a25d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292751"
---
# <a name="iagentballoonsetfontsize"></a><span data-ttu-id="a2254-103">IAgentBalloon:: setfontize</span><span class="sxs-lookup"><span data-stu-id="a2254-103">IAgentBalloon::SetFontSize</span></span>

<span data-ttu-id="a2254-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a2254-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in word balloon
); 
```

<span data-ttu-id="a2254-105">Define o tamanho da fonte exibida na palavra balão.</span><span class="sxs-lookup"><span data-stu-id="a2254-105">Sets the size of the font displayed in the word balloon.</span></span>

-   <span data-ttu-id="a2254-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a2254-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a2254-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span><span class="sxs-lookup"><span data-stu-id="a2254-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="a2254-108">Tamanho da fonte.</span><span class="sxs-lookup"><span data-stu-id="a2254-108">The size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="a2254-109">O tamanho de fonte padrão usado no balão de palavras de um caractere é definido no editor de caracteres do agente da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a2254-109">The default font size used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="a2254-110">Você pode alterá-lo com **IAgentBalloon:: Setfontize**.</span><span class="sxs-lookup"><span data-stu-id="a2254-110">You can change it with **IAgentBalloon::SetFontSize**.</span></span> <span data-ttu-id="a2254-111">No entanto, o usuário pode substituir a configuração de tamanho da fonte para todos os caracteres usando a folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="a2254-111">However, the user can override the font size setting for all characters using the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2254-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="a2254-112">See Also</span></span>

[<span data-ttu-id="a2254-113">**IAgentBalloon:: getfontize**</span><span class="sxs-lookup"><span data-stu-id="a2254-113">**IAgentBalloon::GetFontSize**</span></span>](iagentballoon--getfontsize.md)


 

 




