---
title: IAgentCommand GetConfidenceText
description: IAgentCommand GetConfidenceText
ms.assetid: d98339eb-0986-497c-b43c-4e4a952328e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987dca39016a20d185fbd4b8fd2b554c8bec02f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293901"
---
# <a name="iagentcommandgetconfidencetext"></a><span data-ttu-id="92217-103">IAgentCommand::GetConfidenceText</span><span class="sxs-lookup"><span data-stu-id="92217-103">IAgentCommand::GetConfidenceText</span></span>

<span data-ttu-id="92217-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="92217-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetConfidenceText(
   BSTR * pbszTipText  // address of ConfidenceText setting for Command 
);
```

<span data-ttu-id="92217-105">Recupera o texto da dica de escuta definido anteriormente para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="92217-105">Retrieves the Listening Tip text previously set for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="92217-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="92217-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="92217-107"><span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*pbszTipText*</span><span class="sxs-lookup"><span data-stu-id="92217-107"><span id="pbszTipText"></span><span id="pbsztiptext"></span><span id="PBSZTIPTEXT"></span>*pbszTipText*</span></span>
</dt> <dd>

<span data-ttu-id="92217-108">O endereço de um BSTR que recebe o valor do texto da dica de escuta para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="92217-108">The address of a BSTR that receives the value of the Listening Tip text for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="92217-109">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="92217-109">See Also</span></span>

<span data-ttu-id="92217-110">[**IAgentCommand:: SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand:: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand:: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="92217-110">[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 