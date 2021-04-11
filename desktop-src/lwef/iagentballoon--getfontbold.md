---
title: IAgentBalloon GetFontBold
description: IAgentBalloon GetFontBold
ms.assetid: 5a55f771-d68e-4f66-8001-47c141661b06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858f6f42964db1bdd7ae548d308c6f6668b05631
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159985"
---
# <a name="iagentballoongetfontbold"></a><span data-ttu-id="bceb7-103">IAgentBalloon::GetFontBold</span><span class="sxs-lookup"><span data-stu-id="bceb7-103">IAgentBalloon::GetFontBold</span></span>

<span data-ttu-id="bceb7-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="bceb7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontBold(
   long * pbFontBold  // address of variable for bold setting for
);                    // font displayed in word balloon 
```

<span data-ttu-id="bceb7-105">Indica se a fonte usada em um balão de palavra está em negrito.</span><span class="sxs-lookup"><span data-stu-id="bceb7-105">Indicates whether the font used in a word balloon is bold.</span></span>

-   <span data-ttu-id="bceb7-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bceb7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bceb7-107"><span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*</span><span class="sxs-lookup"><span data-stu-id="bceb7-107"><span id="pbFontBold"></span><span id="pbfontbold"></span><span id="PBFONTBOLD"></span>*pbFontBold*</span></span>
</dt> <dd>

<span data-ttu-id="bceb7-108">O endereço de um valor que recebe **true** se a fonte for Bold e **false** se não estiver em negrito.</span><span class="sxs-lookup"><span data-stu-id="bceb7-108">The address of a value that receives **True** if the font is bold and **False** if not bold.</span></span>

</dd> </dl>

<span data-ttu-id="bceb7-109">O estilo de fonte usado em um balão de palavras de caracteres é definido no editor de caracteres do agente da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="bceb7-109">The font style used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="bceb7-110">Ele não pode ser alterado por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bceb7-110">It cannot be changed by an application.</span></span> <span data-ttu-id="bceb7-111">No entanto, o usuário pode substituir as configurações de fonte de todos os caracteres por meio da folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="bceb7-111">However, the user can override the font settings for all characters through the Microsoft Agent property sheet.</span></span>

 

 




