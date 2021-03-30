---
title: IAgentBalloon GetBackColor
description: IAgentBalloon GetBackColor
ms.assetid: 278ed645-0e6c-4a5d-bd85-3e3b7a1e3333
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cce886c9929892c89b56f162f784dc27a472209
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005716"
---
# <a name="iagentballoongetbackcolor"></a><span data-ttu-id="11e3d-103">IAgentBalloon:: GetBackColor</span><span class="sxs-lookup"><span data-stu-id="11e3d-103">IAgentBalloon::GetBackColor</span></span>

<span data-ttu-id="11e3d-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="11e3d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetBackColor(
   long * plBGColor  // address of variable for background color displayed
);                   // in word balloon
```

<span data-ttu-id="11e3d-105">Recupera o valor da cor do plano de fundo exibida em um balão de palavras.</span><span class="sxs-lookup"><span data-stu-id="11e3d-105">Retrieves the value for the background color displayed in a word balloon.</span></span>

-   <span data-ttu-id="11e3d-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="11e3d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="11e3d-107"><span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*</span><span class="sxs-lookup"><span data-stu-id="11e3d-107"><span id="plBGColor"></span><span id="plbgcolor"></span><span id="PLBGCOLOR"></span>*plBGColor*</span></span>
</dt> <dd>

<span data-ttu-id="11e3d-108">O endereço de uma variável que recebe a configuração de cor para o plano de fundo do balão.</span><span class="sxs-lookup"><span data-stu-id="11e3d-108">The address of a variable that receives the color setting for the balloon background.</span></span>

</dd> </dl>

<span data-ttu-id="11e3d-109">A cor do plano de fundo usada em um balão de palavras de caracteres é definida no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="11e3d-109">The background color used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="11e3d-110">Ele não pode ser alterado por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="11e3d-110">It cannot be changed by an application.</span></span> <span data-ttu-id="11e3d-111">No entanto, o usuário pode alterar a cor do plano de fundo dos balões de palavra para todos os caracteres por meio da folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="11e3d-111">However, the user can change the background color of the word balloons for all characters through the Microsoft Agent property sheet.</span></span>

## <a name="see-also"></a><span data-ttu-id="11e3d-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="11e3d-112">See Also</span></span>

[<span data-ttu-id="11e3d-113">**IAgentBalloon:: GetForeColor**</span><span class="sxs-lookup"><span data-stu-id="11e3d-113">**IAgentBalloon::GetForeColor**</span></span>](iagentballoon--getforecolor.md)


 

 




