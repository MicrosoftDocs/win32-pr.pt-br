---
title: IAgentCommandsEx getfontize
description: IAgentCommandsEx getfontize
ms.assetid: 8173e026-d28f-43d8-a8b4-96d1d97a8b68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48a2450d94e89dd9dddc00a11af7f37bf4837558
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364105"
---
# <a name="iagentcommandsexgetfontsize"></a><span data-ttu-id="d8147-103">IAgentCommandsEx:: getfontize</span><span class="sxs-lookup"><span data-stu-id="d8147-103">IAgentCommandsEx::GetFontSize</span></span>

<span data-ttu-id="d8147-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d8147-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetFontSize(
   long * plFontSize  // address of variable for font size 
);                    // for font displayed in character's pop-up menu
```

<span data-ttu-id="d8147-105">Recupera o valor do tamanho da fonte exibida no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="d8147-105">Retrieves the value for the size of the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="d8147-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d8147-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d8147-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span><span class="sxs-lookup"><span data-stu-id="d8147-107"><span id="plFontSize"></span><span id="plfontsize"></span><span id="PLFONTSIZE"></span>*plFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="d8147-108">O endereço de um valor que recebe o tamanho da fonte.</span><span class="sxs-lookup"><span data-stu-id="d8147-108">The address of a value that receives the size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="d8147-109">O tamanho do ponto da fonte retornado corresponde ao tamanho definido para exibir o texto no menu pop-up do caractere quando o cliente está na entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="d8147-109">The point size of the font returned corresponds to the size defined to display text in the character's pop-up menu when your client is input-active.</span></span> <span data-ttu-id="d8147-110">O valor padrão para a configuração de fonte é baseado na configuração de fonte do menu para a configuração de ID de idioma do caractere, ou se não estiver definido, a configuração de idioma padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="d8147-110">The default value for the font setting is based on the menu font setting for the character's language ID setting, or if not set, the user default language setting.</span></span>

<span data-ttu-id="d8147-111">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="d8147-111">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="d8147-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="d8147-112">See Also</span></span>

<span data-ttu-id="d8147-113">[**IAgentCommandsEx:: setfonts**](iagentcommandsex--setfontsize.md), [ **IAgentCommandsEx:: setnomedafontename**](iagentcommandsex--setfontname.md)</span><span class="sxs-lookup"><span data-stu-id="d8147-113">[**IAgentCommandsEx::SetFontSize**](iagentcommandsex--setfontsize.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)</span></span>


 

 




