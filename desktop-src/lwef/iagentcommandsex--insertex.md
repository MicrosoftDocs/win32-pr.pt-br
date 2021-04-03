---
title: IAgentCommandsEx InsertEx
description: IAgentCommandsEx InsertEx
ms.assetid: 037c47df-f026-42dc-8c37-2704518d3fd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d59b504cfa475c3ac63888796d7df8d800bfd72
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007465"
---
# <a name="iagentcommandsexinsertex"></a><span data-ttu-id="f3355-103">IAgentCommandsEx::InsertEx</span><span class="sxs-lookup"><span data-stu-id="f3355-103">IAgentCommandsEx::InsertEx</span></span>

<span data-ttu-id="f3355-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f3355-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT InsertEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long dwRefID,          // reference Command for insertion
   long dBefore,          // insertion position flag
   long * pdwID           // address for variable for Command ID
);
```

<span data-ttu-id="f3355-105">Insere um objeto de [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="f3355-105">Inserts a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="f3355-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f3355-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="f3355-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span><span class="sxs-lookup"><span data-stu-id="f3355-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="f3355-108">Um BSTR que especifica o valor do texto de [**legenda**](caption-property.md) exibido para o [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="f3355-108">A BSTR that specifies the value of the [**Caption**](caption-property.md) text displayed for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> <dt>

<span data-ttu-id="f3355-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span><span class="sxs-lookup"><span data-stu-id="f3355-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="f3355-110">Um BSTR que especifica o valor da configuração de texto de [**voz**](voice-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="f3355-110">A BSTR that specifies the value of the [**Voice**](voice-property.md) text setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> <dt>

<span data-ttu-id="f3355-111"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="f3355-111"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="f3355-112">Um BSTR que especifica o valor do texto [**VoiceCaption**](voicecaption-property.md) exibido para um [**comando**](/windows/desktop/lwef/the-command-object) em uma coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="f3355-112">A BSTR that specifies the value of the [**VoiceCaption**](voicecaption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="f3355-113"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="f3355-113"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="f3355-114">Uma expressão booliana que especifica a configuração [**habilitada**](enabled-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="f3355-114">A Boolean expression that specifies the [**Enabled**](enabled-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="f3355-115">Se o parâmetro for **true**, o **comando** será habilitado e poderá ser selecionado; Se for **false**, o **comando** será desabilitado.</span><span class="sxs-lookup"><span data-stu-id="f3355-115">If the parameter is **True**, the **Command** is enabled and can be selected; if **False**, the **Command** is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="f3355-116"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="f3355-116"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="f3355-117">Uma expressão booliana que especifica a configuração [**visível**](visible-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="f3355-117">A Boolean expression that specifies the [**Visible**](visible-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="f3355-118">Se o parâmetro for **true**, o **comando** ficará visível no menu pop-up do caractere (se a propriedade [**Caption**](caption-property.md) também estiver definida).</span><span class="sxs-lookup"><span data-stu-id="f3355-118">If the parameter is **True**, the **Command** will be visible in the character's pop-up menu (if the [**Caption**](caption-property.md) property is also set).</span></span>

</dd> <dt>

<span data-ttu-id="f3355-119"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span><span class="sxs-lookup"><span data-stu-id="f3355-119"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="f3355-120">O número de contexto do tópico da ajuda associado ao objeto de [**comando**](/windows/desktop/lwef/the-command-object) ; usado para fornecer ajuda contextual para o comando.</span><span class="sxs-lookup"><span data-stu-id="f3355-120">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> <dt>

<span data-ttu-id="f3355-121"><span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*</span><span class="sxs-lookup"><span data-stu-id="f3355-121"><span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*</span></span>
</dt> <dd>

<span data-ttu-id="f3355-122">A ID de um [**comando**](/windows/desktop/lwef/the-command-object) usado como uma referência para a inserção relativa do novo **comando**.</span><span class="sxs-lookup"><span data-stu-id="f3355-122">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) used as a reference for the relative insertion of the new **Command**.</span></span>

</dd> <dt>

<span data-ttu-id="f3355-123"><span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*</span><span class="sxs-lookup"><span data-stu-id="f3355-123"><span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*</span></span>
</dt> <dd>

<span data-ttu-id="f3355-124">Uma expressão booliana que especifica onde posicionar o [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="f3355-124">A Boolean expression that specifies where to place the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="f3355-125">Se esse parâmetro for **true**, o novo **comando** será inserido antes do **comando** referenciado; Se for **false**, o novo **comando** será colocado após o **comando** referenciado.</span><span class="sxs-lookup"><span data-stu-id="f3355-125">If this parameter is **True**, the new **Command** is inserted before the referenced **Command**; if **False**, the new **Command** is placed after the referenced **Command**.</span></span>

</dd> <dt>

<span data-ttu-id="f3355-126"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="f3355-126"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span></span> 
</dt> <dd>

<span data-ttu-id="f3355-127">Endereço de uma variável que recebe a ID do [**comando**](/windows/desktop/lwef/the-command-object)inserido.</span><span class="sxs-lookup"><span data-stu-id="f3355-127">Address of a variable that receives the ID for the inserted [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="f3355-128">[**IAgentCommandsEx:: InsertEx**](https://www.bing.com/search?q=**IAgentCommandsEx::InsertEx**) estende [**IAgentCommands:: Insert**](iagentcommands--insert.md) , incluindo a propriedade [**HelpContextId**](helpcontextid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="f3355-128">[**IAgentCommandsEx::InsertEx**](https://www.bing.com/search?q=**IAgentCommandsEx::InsertEx**) extends [**IAgentCommands::Insert**](iagentcommands--insert.md) by including the [**HelpContextID**](helpcontextid-property.md) property.</span></span> <span data-ttu-id="f3355-129">Você também pode definir a propriedade usando [ **IAgentCommandsEx:: setidentificaçãodocontextodaajuda**](iagentcommandsex--sethelpcontextid.md)</span><span class="sxs-lookup"><span data-stu-id="f3355-129">You can also set the property using [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="f3355-130">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="f3355-130">See Also</span></span>

<span data-ttu-id="f3355-131">[**IAgentCommandsEx:: AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx:: setidentificaçãodocontextodaajuda**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="f3355-131">[**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 