---
title: IAgentCommand sethabilitado
description: IAgentCommand sethabilitado
ms.assetid: e0a724b4-3613-400f-a801-efc8bf66e355
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8377307d66257f7a9b74ac82512edc6e4ec64034
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007422"
---
# <a name="iagentcommandsetenabled"></a><span data-ttu-id="4b3cb-103">IAgentCommand:: sethabilitado</span><span class="sxs-lookup"><span data-stu-id="4b3cb-103">IAgentCommand::SetEnabled</span></span>

<span data-ttu-id="4b3cb-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="4b3cb-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetEnabled(
   long bEnabled  // Enabled setting for Command
);
```

<span data-ttu-id="4b3cb-105">Define a propriedade [**Enabled**](enabled-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="4b3cb-105">Sets the [**Enabled**](enabled-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="4b3cb-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="4b3cb-107"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="4b3cb-107"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="4b3cb-108">Um valor booliano que define o valor da configuração [**habilitada**](enabled-property.md) de um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="4b3cb-108">A Boolean value that sets the value of the [**Enabled**](enabled-property.md) setting of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="4b3cb-109">**True** habilita o **comando**; **False** desabilita.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-109">**True** enables the **Command**; **False** disables it.</span></span> <span data-ttu-id="4b3cb-110">Um **comando** desabilitado não pode ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-110">A disabled **Command** cannot be selected.</span></span>

</dd> </dl>

<span data-ttu-id="4b3cb-111">Um [**comando**](/windows/desktop/lwef/the-command-object) deve ter sua propriedade [**Enabled**](enabled-property.md) definida como **true** para ser selecionável.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-111">A [**Command**](/windows/desktop/lwef/the-command-object) must have its [**Enabled**](enabled-property.md) property set to **True** to be selectable.</span></span> <span data-ttu-id="4b3cb-112">Ele também deve ter sua propriedade [**Caption**](caption-property.md) definida e sua propriedade [**Visible**](visible-property.md) definida como **true** para aparecer no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="4b3cb-112">It also must have its [**Caption**](caption-property.md) property set and its [**Visible**](visible-property.md) property set to **True** to appear in the character's pop-up menu.</span></span> <span data-ttu-id="4b3cb-113">Para fazer com que o **comando** apareça na **janela de comandos de voz**, você deve definir sua propriedade de [**voz**](voice-property.md).</span><span class="sxs-lookup"><span data-stu-id="4b3cb-113">To make the **Command** appear in the **Voice Commands Window**, you must set its [**Voice**](voice-property.md)property.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b3cb-114">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="4b3cb-114">See Also</span></span>

<span data-ttu-id="4b3cb-115">[**IAgentCommand:: getCaption**](iagentcommand--getcaption.md), [**IAgentCommand:: setvoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Adicionar**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="4b3cb-115">[**IAgentCommand::GetCaption**](iagentcommand--getcaption.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 