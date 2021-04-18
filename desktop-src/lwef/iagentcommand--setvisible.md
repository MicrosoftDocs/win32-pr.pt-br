---
title: IAgentCommand setVisible
description: IAgentCommand setVisible
ms.assetid: 58a383f4-6c98-4037-b469-ae68f06c852d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b583f79a93a5b13914486fb3e1a9cb513a682e63
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105813509"
---
# <a name="iagentcommandsetvisible"></a><span data-ttu-id="35f7b-103">IAgentCommand:: setVisible</span><span class="sxs-lookup"><span data-stu-id="35f7b-103">IAgentCommand::SetVisible</span></span>

<span data-ttu-id="35f7b-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="35f7b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // Visible setting for Command
);
```

<span data-ttu-id="35f7b-105">Define o valor da propriedade [**Visible**](visible-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="35f7b-105">Sets the value of the [**Visible**](visible-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="35f7b-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="35f7b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="35f7b-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="35f7b-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="35f7b-108">Um valor booliano que determina a propriedade [**visível**](visible-property.md) de um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="35f7b-108">A Boolean value that determines the [**Visible**](visible-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="35f7b-109">**Verdadeiro** mostra o **comando**; **False** oculta-o.</span><span class="sxs-lookup"><span data-stu-id="35f7b-109">**True** shows the **Command**; **False** hides it.</span></span>

</dd> </dl>

<span data-ttu-id="35f7b-110">Um [**comando**](/windows/desktop/lwef/the-command-object) deve ter sua propriedade [**visível**](visible-property.md) definida como **true** e sua propriedade [**Caption**](caption-property.md) definida como aparece no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="35f7b-110">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Visible**](visible-property.md) property set to **True** and its [**Caption**](caption-property.md) property set to appear in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="35f7b-111">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="35f7b-111">See Also</span></span>

<span data-ttu-id="35f7b-112">[**IAgentCommand:: getvisível**](iagentcommand--getvisible.md), [**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands:: Adicionar**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="35f7b-112">[**IAgentCommand::GetVisible**](iagentcommand--getvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 