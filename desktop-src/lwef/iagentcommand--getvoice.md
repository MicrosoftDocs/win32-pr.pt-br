---
title: Getvoice IAgentCommand
description: Getvoice IAgentCommand
ms.assetid: 69f3c91b-2ccf-4bea-8034-0c3e0a5e4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2365019f71447e9d9c5a560c6506ee1dae7423df
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105782663"
---
# <a name="iagentcommandgetvoice"></a><span data-ttu-id="886b1-103">IAgentCommand:: getvoice</span><span class="sxs-lookup"><span data-stu-id="886b1-103">IAgentCommand::GetVoice</span></span>

<span data-ttu-id="886b1-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="886b1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoice(
   BSTR * pbszVoice  // address of Voice setting for Command
);
```

<span data-ttu-id="886b1-105">Recupera o valor da propriedade de texto de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="886b1-105">Retrieves the value of the [**Voice**](voice-property.md) text property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="886b1-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="886b1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="886b1-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span><span class="sxs-lookup"><span data-stu-id="886b1-107"><span id="pbszVoice"></span><span id="pbszvoice"></span><span id="PBSZVOICE"></span>*pbszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="886b1-108">O endereço de um BSTR que recebe a propriedade de texto de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="886b1-108">The address of a BSTR that receives the [**Voice**](voice-property.md) text property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="886b1-109">Um [**comando**](/windows/desktop/lwef/the-command-object) com seu conjunto de propriedades de [**voz**](voice-property.md) e sua propriedade [**Enabled**](enabled-property.md) definida como **true** serão acessíveis por voz.</span><span class="sxs-lookup"><span data-stu-id="886b1-109">A [**Command**](/windows/desktop/lwef/the-command-object) with its [**Voice**](voice-property.md) property set and its [**Enabled**](enabled-property.md) property set to **True** will be voice-accessible.</span></span> <span data-ttu-id="886b1-110">Se sua propriedade [**Caption**](caption-property.md) também for definida, ela aparecerá na janela comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="886b1-110">If its [**Caption**](caption-property.md) property is also set it appears in the Voice Commands Window.</span></span> <span data-ttu-id="886b1-111">Se sua propriedade [**Visible**](visible-property.md) for definida como **true**, ela aparecerá no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="886b1-111">If its [**Visible**](visible-property.md) property is set to **True**, it appears in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="886b1-112">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="886b1-112">See Also</span></span>

<span data-ttu-id="886b1-113">[**IAgentCommand:: setvoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Adicionar**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="886b1-113">[**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 