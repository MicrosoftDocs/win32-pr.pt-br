---
title: IAgentBalloon GetFontItalic
description: IAgentBalloon GetFontItalic
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c1a0e1e649e325e84d4a78eee087e102e8d1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105772563"
---
# <a name="iagentballoongetfontitalic"></a><span data-ttu-id="fb851-103">IAgentBalloon::GetFontItalic</span><span class="sxs-lookup"><span data-stu-id="fb851-103">IAgentBalloon::GetFontItalic</span></span>

<span data-ttu-id="fb851-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="fb851-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

<span data-ttu-id="fb851-105">Indica se a fonte usada em um balão de palavras está em itálico.</span><span class="sxs-lookup"><span data-stu-id="fb851-105">Indicates whether the font used in a word balloon is italic.</span></span>

-   <span data-ttu-id="fb851-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="fb851-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="fb851-107"><span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*</span><span class="sxs-lookup"><span data-stu-id="fb851-107"><span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*</span></span>
</dt> <dd>

<span data-ttu-id="fb851-108">O endereço de um valor que recebe **true** se a fonte for Italic e **false** se não estiver em itálico.</span><span class="sxs-lookup"><span data-stu-id="fb851-108">The address of a value that receives **True** if the font is italic and **False** if not italic.</span></span>

</dd> </dl>

<span data-ttu-id="fb851-109">O estilo de fonte usado no balão de palavras de um caractere é definido no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="fb851-109">The font style used in a character's word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="fb851-110">Ele não pode ser alterado por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fb851-110">It cannot be changed by an application.</span></span> <span data-ttu-id="fb851-111">No entanto, o usuário pode substituir as configurações de fonte de todos os caracteres por meio da folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="fb851-111">However, the user can override the font settings for all characters through the Microsoft Agent property sheet.</span></span>

 

 




