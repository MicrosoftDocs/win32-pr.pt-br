---
title: IAgentCommand getCaption
description: IAgentCommand getCaption
ms.assetid: e333faca-e2c2-478a-a803-cbc401793e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44540ba9105e79ba675f8bf78be20e8961f98d0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103823678"
---
# <a name="iagentcommandgetcaption"></a><span data-ttu-id="b862b-103">IAgentCommand:: getCaption</span><span class="sxs-lookup"><span data-stu-id="b862b-103">IAgentCommand::GetCaption</span></span>

<span data-ttu-id="b862b-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b862b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetCaption(
   BSTR * pbszCaption  // address of Caption for Command
);
```

<span data-ttu-id="b862b-105">Recupera a [**legenda**](caption-property.md) de um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="b862b-105">Retrieves the [**Caption**](caption-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="b862b-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b862b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b862b-107"><span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*</span><span class="sxs-lookup"><span data-stu-id="b862b-107"><span id="pbszCaption"></span><span id="pbszcaption"></span><span id="PBSZCAPTION"></span>*pbszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="b862b-108">O endereço de um BSTR que recebe o valor do texto de [**legenda**](caption-property.md) exibido para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="b862b-108">The address of a BSTR that receives the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="b862b-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="b862b-109">See Also</span></span>

<span data-ttu-id="b862b-110">[**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand:: sethabilitated**](iagentcommand--setenabled.md), [**IAgentCommand:: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand:: setvoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Adicionar**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="b862b-110">[**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 