---
title: IAgentBalloon getnomedafonte
description: IAgentBalloon getnomedafonte
ms.assetid: 7d057571-bb6e-4b79-bc4a-5691779ace51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73f29ad981fb4b10249b17e55c92fb286552eedc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364410"
---
# <a name="iagentballoongetfontname"></a><span data-ttu-id="baa21-103">IAgentBalloon:: getnomedafonte</span><span class="sxs-lookup"><span data-stu-id="baa21-103">IAgentBalloon::GetFontName</span></span>

<span data-ttu-id="baa21-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="baa21-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in word balloon
```

<span data-ttu-id="baa21-105">Recupera o valor da fonte exibida em um balão de palavras.</span><span class="sxs-lookup"><span data-stu-id="baa21-105">Retrieves the value for the font displayed in a word balloon.</span></span>

-   <span data-ttu-id="baa21-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="baa21-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="baa21-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span><span class="sxs-lookup"><span data-stu-id="baa21-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="baa21-108">O endereço de um BSTR que recebe o nome da fonte exibido em um balão de palavra.</span><span class="sxs-lookup"><span data-stu-id="baa21-108">The address of a BSTR that receives the font name displayed in a word balloon.</span></span>

</dd> </dl>

<span data-ttu-id="baa21-109">A fonte padrão usada em um balão de palavras de caracteres é definida no editor de caracteres do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="baa21-109">The default font used in a character word balloon is defined in the Microsoft Agent Character Editor.</span></span> <span data-ttu-id="baa21-110">Você pode alterá-lo com [**IAgentBalloon:: setnomedafonte**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**).</span><span class="sxs-lookup"><span data-stu-id="baa21-110">You can change it with [**IAgentBalloon::SetFontName**](https://www.bing.com/search?q=**IAgentBalloon::SetFontName**).</span></span> <span data-ttu-id="baa21-111">O usuário pode substituir a configuração de fonte para todos os caracteres usando a folha de propriedades do Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="baa21-111">The user can override the font setting for all characters using the Microsoft Agent property sheet.</span></span>

 

 




