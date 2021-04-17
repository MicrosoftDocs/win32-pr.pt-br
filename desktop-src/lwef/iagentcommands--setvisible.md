---
title: IAgentCommands setVisible
description: IAgentCommands setVisible
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a4bdb3c1a7f1e11c9548eb1e1af415d0f5d18f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105812044"
---
# <a name="iagentcommandssetvisible"></a><span data-ttu-id="c3a4e-103">IAgentCommands:: setVisible</span><span class="sxs-lookup"><span data-stu-id="c3a4e-103">IAgentCommands::SetVisible</span></span>

<span data-ttu-id="c3a4e-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c3a4e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

<span data-ttu-id="c3a4e-105">Define o valor da propriedade [**Visible**](visible-property.md) para uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="c3a4e-105">Sets the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="c3a4e-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c3a4e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c3a4e-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="c3a4e-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="c3a4e-108">Um valor booliano que determina a propriedade [**visível**](visible-property.md) de uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="c3a4e-108">A Boolean value that determines the [**Visible**](visible-property.md) property of a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="c3a4e-109">**Verdadeiro** define a [**legenda**](caption-property.md) da coleção de **comandos** como visível quando o menu pop-up do caractere é exibido; *False* não exibe.</span><span class="sxs-lookup"><span data-stu-id="c3a4e-109">**True** sets the **Commands** collection's [**Caption**](caption-property.md) to be visible when the character's pop-up menu is displayed; *False* does not display it.</span></span>

</dd> </dl>

<span data-ttu-id="c3a4e-110">Uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) deve ter sua propriedade [**Caption**](caption-property.md) definida e sua propriedade [**Visible**](visible-property.md) definida como **true** para aparecer no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="c3a4e-110">A [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection must have its [**Caption**](caption-property.md) property set and its [**Visible**](visible-property.md) property set to **True** to appear on the character's pop-up menu.</span></span> <span data-ttu-id="c3a4e-111">A propriedade **Visible** também deve ser definida como **true** para que os comandos na coleção apareçam quando o aplicativo cliente está na entrada-ativo.</span><span class="sxs-lookup"><span data-stu-id="c3a4e-111">The **Visible** property must also be set to **True** for commands in the collection to appear when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3a4e-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c3a4e-112">See Also</span></span>

<span data-ttu-id="c3a4e-113">[**IAgentCommands:: getvisível**](iagentcommands--getvisible.md), [ **IAgentCommand:: SetCaption**](iagentcommand--setcaption.md)</span><span class="sxs-lookup"><span data-stu-id="c3a4e-113">[**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md)</span></span>


 

 