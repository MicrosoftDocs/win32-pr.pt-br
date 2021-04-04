---
title: IAgentCommands adicionar
description: IAgentCommands adicionar
ms.assetid: f6be7773-77fa-4c59-8feb-c2ebf54fd2e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee56854c302a096143e58fe6c21ef75fedfbf59
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084464"
---
# <a name="iagentcommandsadd"></a><span data-ttu-id="24649-103">IAgentCommands:: Adicionar</span><span class="sxs-lookup"><span data-stu-id="24649-103">IAgentCommands::Add</span></span>

<span data-ttu-id="24649-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="24649-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Add(
   BSTR bszCaption,  // Caption setting for Command
   BSTR bszVoice,    // Voice setting for Command
   long bEnabled,    // Enabled setting for Command
   long bVisible,    // Visible setting for Command
   long * pdwID      // address for variable for ID
);
```

<span data-ttu-id="24649-105">Adiciona um [**comando**](/windows/desktop/lwef/the-command-object) a uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="24649-105">Adds a [**Command**](/windows/desktop/lwef/the-command-object) to a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="24649-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="24649-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="24649-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span><span class="sxs-lookup"><span data-stu-id="24649-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="24649-108">Um BSTR que especifica o valor do texto de [**legenda**](caption-property.md) exibido para um [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="24649-108">A BSTR that specifies the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="24649-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span><span class="sxs-lookup"><span data-stu-id="24649-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="24649-110">Um BSTR que especifica o valor da configuração de texto de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="24649-110">A BSTR that specifies the value of the [**Voice**](voice-property.md) text setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="24649-111"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="24649-111"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="24649-112">Uma expressão booliana que especifica a configuração [**habilitada**](enabled-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="24649-112">A Boolean expression that specifies the [**Enabled**](enabled-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="24649-113">Se o parâmetro for **true**, o **comando** será habilitado e poderá ser selecionado; Se for **false**, o **comando** será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="24649-113">If the parameter is **True**, the **Command** is enabled and can be selected; if **False**, the **Command** is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="24649-114"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="24649-114"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="24649-115">Uma expressão booliana que especifica a configuração [**visível**](visible-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="24649-115">A Boolean expression that specifies the [**Visible**](visible-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="24649-116">Se o parâmetro for **true**, o **comando** ficará visível no menu pop-up do caractere (se a propriedade [**Caption**](caption-property.md) também estiver definida).</span><span class="sxs-lookup"><span data-stu-id="24649-116">If the parameter is **True**, the **Command** will be visible in the character's pop-up menu (if the [**Caption**](caption-property.md) property is also set).</span></span>

</dd> <dt>

<span data-ttu-id="24649-117"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="24649-117"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span></span> 
</dt> <dd>

<span data-ttu-id="24649-118">Endereço de uma variável que recebe a ID para o [**comando**](/windows/desktop/lwef/the-command-object)adicionado.</span><span class="sxs-lookup"><span data-stu-id="24649-118">Address of a variable that receives the ID for the added [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="24649-119">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="24649-119">See Also</span></span>

<span data-ttu-id="24649-120">[**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand:: sethabilitated**](iagentcommand--setenabled.md), [**IAgentCommand:: setvisível**](iagentcommand--setvisible.md), [**IAgentCommand:: setvoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="24649-120">[**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 