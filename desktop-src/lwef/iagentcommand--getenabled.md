---
title: IAgentCommand getabilited
description: IAgentCommand getabilited
ms.assetid: b4ec25d2-b2e0-4b1b-8dc5-10fbb44149b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238844a70ea7fde3ef0c07cad1a6f3abab5613d1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454018"
---
# <a name="iagentcommandgetenabled"></a><span data-ttu-id="196e8-103">IAgentCommand:: getabilited</span><span class="sxs-lookup"><span data-stu-id="196e8-103">IAgentCommand::GetEnabled</span></span>

<span data-ttu-id="196e8-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="196e8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetEnabled(
   long * pbEnabled  // address of Enabled setting for Command
);
```

<span data-ttu-id="196e8-105">Recupera o valor da propriedade [**Enabled**](enabled-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="196e8-105">Retrieves the value of the [**Enabled**](enabled-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="196e8-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="196e8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="196e8-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="196e8-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="196e8-108">O endereço de uma variável que recebe **true** se o [**comando**](/windows/desktop/lwef/the-command-object) estiver habilitado ou **false** se estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="196e8-108">The address of a variable that receives **True** if the [**Command**](/windows/desktop/lwef/the-command-object) is enabled, or **False** if it is disabled.</span></span> <span data-ttu-id="196e8-109">Um **comando** desabilitado não pode ser selecionado.</span><span class="sxs-lookup"><span data-stu-id="196e8-109">A disabled **Command** cannot be selected.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="196e8-110">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="196e8-110">See Also</span></span>

<span data-ttu-id="196e8-111">[**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand:: setvisível**](iagentcommand--setvisible.md), [**IAgentCommand:: setvoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Adicionar**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="196e8-111">[**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 