---
title: IAgentCommandsEx setnomedafonte
description: IAgentCommandsEx setnomedafonte
ms.assetid: c676ceb6-c098-4ac0-9103-ece469317ad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e9a4b76a58fc3651c02bedc43f8d372f607c2df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635121"
---
# <a name="iagentcommandsexsetfontname"></a><span data-ttu-id="8dce1-103">IAgentCommandsEx:: setnomedafontename</span><span class="sxs-lookup"><span data-stu-id="8dce1-103">IAgentCommandsEx::SetFontName</span></span>

<span data-ttu-id="8dce1-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8dce1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontName(
   BSTR bszFontName  // font to be displayed in character's pop-up menu
);
```

<span data-ttu-id="8dce1-105">Define a fonte exibida no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="8dce1-105">Sets the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="8dce1-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8dce1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8dce1-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span><span class="sxs-lookup"><span data-stu-id="8dce1-107"><span id="bszFontName"></span><span id="bszfontname"></span><span id="BSZFONTNAME"></span>*bszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="8dce1-108">Um BSTR que define a fonte exibida no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="8dce1-108">A BSTR that sets the font displayed in the character's pop-up menu.</span></span>

</dd> </dl>

<span data-ttu-id="8dce1-109">Essa propriedade determina a fonte usada para exibir o texto no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="8dce1-109">This property determines the font used to display text in the character's pop-up menu.</span></span> <span data-ttu-id="8dce1-110">O valor padrão para a configuração de fonte é baseado na configuração de fonte do menu para a configuração de ID de idioma do caractere-ou se não estiver definido, a configuração de ID de idioma padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="8dce1-110">The default value for the font setting is based on the menu font setting for the character's language ID setting-or if that's not set-the user default language ID setting.</span></span>

<span data-ttu-id="8dce1-111">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="8dce1-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="8dce1-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="8dce1-112">See Also</span></span>

<span data-ttu-id="8dce1-113">[**IAgentCommandsEx:: getnomedafonte**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx:: getfonts**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx:: setfontize**](iagentcommandsex--setfontsize.md)</span><span class="sxs-lookup"><span data-stu-id="8dce1-113">[**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)</span></span>


 

 




