---
title: IAgentCommandsEx getnomedafonte
description: IAgentCommandsEx getnomedafonte
ms.assetid: cd0d0d93-839e-471c-9cfa-9f47dcce841b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215f08cbe1e5e97b218f9279baff5e3affd74956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364106"
---
# <a name="iagentcommandsexgetfontname"></a><span data-ttu-id="ef4f0-103">IAgentCommandsEx:: getnomedafonte</span><span class="sxs-lookup"><span data-stu-id="ef4f0-103">IAgentCommandsEx::GetFontName</span></span>

<span data-ttu-id="ef4f0-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ef4f0-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontName(
   BSTR * pbszFontName  // address of variable for font displayed 
);                      // in character's pop-up menu
```

<span data-ttu-id="ef4f0-105">Recupera o valor da fonte exibida no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="ef4f0-105">Retrieves the value for the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="ef4f0-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ef4f0-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ef4f0-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span><span class="sxs-lookup"><span data-stu-id="ef4f0-107"><span id="pbszFontName"></span><span id="pbszfontname"></span><span id="PBSZFONTNAME"></span>*pbszFontName*</span></span>
</dt> <dd>

<span data-ttu-id="ef4f0-108">O endereço de um BSTR que recebe o nome da fonte exibido no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="ef4f0-108">The address of a BSTR that receives the font name displayed in the character's pop-up menu.</span></span>

</dd> </dl>

<span data-ttu-id="ef4f0-109">O nome da fonte retornado corresponde à fonte usada para exibir o texto no menu pop-up do caractere quando o aplicativo cliente é de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="ef4f0-109">The font name returned corresponds to the font used to display text in the character's pop-up menu when your client application is input-active.</span></span> <span data-ttu-id="ef4f0-110">O valor padrão para a configuração de fonte é baseado na configuração de fonte do menu para a configuração de ID de idioma do caractere ou, se não estiver definido, a configuração de ID de idioma padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="ef4f0-110">The default value for the font setting is based on the menu font setting for the character's language ID setting, or if not set, the user default language ID setting.</span></span>

<span data-ttu-id="ef4f0-111">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="ef4f0-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="ef4f0-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="ef4f0-112">See Also</span></span>

<span data-ttu-id="ef4f0-113">[**IAgentCommandsEx:: setnomedafonte**](iagentcommandsex--setfontname.md), [ **IAgentCommandsEx:: setfontize**](iagentcommandsex--setfontsize.md)</span><span class="sxs-lookup"><span data-stu-id="ef4f0-113">[**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md), [**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md)</span></span>


 

 




