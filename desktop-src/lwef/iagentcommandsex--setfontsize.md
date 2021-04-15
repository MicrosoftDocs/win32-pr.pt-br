---
title: IAgentCommandsEx setfontize
description: IAgentCommandsEx setfontize
ms.assetid: 095f78d2-ef91-4880-ad49-dd9a94f02891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19bb9a638141dc3cebe683748500510ea848a664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454000"
---
# <a name="iagentcommandsexsetfontsize"></a><span data-ttu-id="cbf1f-103">IAgentCommandsEx:: setfontize</span><span class="sxs-lookup"><span data-stu-id="cbf1f-103">IAgentCommandsEx::SetFontSize</span></span>

<span data-ttu-id="cbf1f-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cbf1f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetFontSize(
   long lFontSize  // font size displayed in character's pop-up menu
);
```

<span data-ttu-id="cbf1f-105">Define o tamanho da fonte exibida no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-105">Sets the size of the font displayed in the character's pop-up menu.</span></span>

-   <span data-ttu-id="cbf1f-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="cbf1f-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span><span class="sxs-lookup"><span data-stu-id="cbf1f-107"><span id="lFontSize"></span><span id="lfontsize"></span><span id="LFONTSIZE"></span>*lFontSize*</span></span>
</dt> <dd>

<span data-ttu-id="cbf1f-108">Tamanho da fonte.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-108">The size of the font.</span></span>

</dd> </dl>

<span data-ttu-id="cbf1f-109">Essa propriedade determina o tamanho do ponto da fonte usada para exibir o texto no menu pop-up do caractere quando o aplicativo cliente é de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-109">This property determines the point size of the font used to display text in the character's pop-up menu when your client application is input-active.</span></span> <span data-ttu-id="cbf1f-110">O valor padrão para a configuração de fonte é baseado na configuração de fonte do menu para a configuração de ID de idioma do caractere-ou se não estiver definido, a configuração de idioma padrão do usuário.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-110">The default value for the font setting is based on the menu font setting for the character's language ID setting-or if that's not set-the user default language setting.</span></span> <span data-ttu-id="cbf1f-111">Se não houver entrada-ativa, o texto da [](/windows/desktop/lwef/the-command-object) [**legenda**](caption-property.md) do comando do aplicativo cliente aparecerá no tamanho do ponto especificado para o cliente de entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-111">If not input-active, your client application's [**Command**](/windows/desktop/lwef/the-command-object) [**Caption**](caption-property.md) text appears in the point size specified for the input-active client.</span></span>

<span data-ttu-id="cbf1f-112">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="cbf1f-112">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="cbf1f-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="cbf1f-113">See Also</span></span>

<span data-ttu-id="cbf1f-114">[**IAgentCommandsEx:: Getfonte**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx:: getnomedafonte**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx:: setnomedafontename**](iagentcommandsex--setfontname.md)</span><span class="sxs-lookup"><span data-stu-id="cbf1f-114">[**IAgentCommandsEx::GetFontSize**](iagentcommandsex--getfontsize.md), [**IAgentCommandsEx::GetFontName**](iagentcommandsex--getfontname.md), [**IAgentCommandsEx::SetFontName**](iagentcommandsex--setfontname.md)</span></span>


 

 