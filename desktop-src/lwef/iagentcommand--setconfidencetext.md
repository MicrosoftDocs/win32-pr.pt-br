---
title: IAgentCommand SetConfidenceText
description: IAgentCommand SetConfidenceText
ms.assetid: e776a2ba-3592-4f26-a3e3-2c044eed7f0c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cff1ae34c03f8ff67da61bea1834c25d6844ab2
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365852"
---
# <a name="iagentcommandsetconfidencetext"></a><span data-ttu-id="338c1-103">IAgentCommand::SetConfidenceText</span><span class="sxs-lookup"><span data-stu-id="338c1-103">IAgentCommand::SetConfidenceText</span></span>

<span data-ttu-id="338c1-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="338c1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetConfidenceText(
   BSTR bszTipText  // ConfidenceText setting for Command 
);
```

<span data-ttu-id="338c1-105">Define o valor do texto da dica de escuta para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="338c1-105">Sets the value of the Listening Tip text for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="338c1-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="338c1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="338c1-107"><span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bszTipText*</span><span class="sxs-lookup"><span data-stu-id="338c1-107"><span id="bszTipText"></span><span id="bsztiptext"></span><span id="BSZTIPTEXT"></span>*bszTipText*</span></span>
</dt> <dd>

<span data-ttu-id="338c1-108">Um BSTR que especifica o texto para a propriedade [**ConfidenceText**](confidencetext-property.md) de um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="338c1-108">A BSTR that specifies the text for the [**ConfidenceText**](confidencetext-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="338c1-109">Se o valor de confiança retornado da melhor correspondência retornada no evento de [**comando**](/windows/desktop/lwef/the-command-object) não exceder o valor definido para a propriedade [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) , o texto fornecido em *bszTipText* será exibido na dica de escuta.</span><span class="sxs-lookup"><span data-stu-id="338c1-109">If the confidence value returned of the best match returned in the [**Command**](/windows/desktop/lwef/the-command-object) event does not exceed the value set for the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property, the text supplied in *bszTipText* is displayed in the Listening Tip.</span></span>

## <a name="see-also"></a><span data-ttu-id="338c1-110">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="338c1-110">See Also</span></span>

<span data-ttu-id="338c1-111">[**IAgentCommand:: SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand:: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand:: GetConfidenceText**](iagentcommand--getconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="338c1-111">[**IAgentCommand::SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::GetConfidenceText**](iagentcommand--getconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 