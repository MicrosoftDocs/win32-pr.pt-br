---
title: IAgentCommand SetConfidenceThreshold
description: IAgentCommand SetConfidenceThreshold
ms.assetid: f62d646a-895d-468c-9397-0495680109a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a6ba352f9385c57d0f3d1f01070f4b46e147d3
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104084531"
---
# <a name="iagentcommandsetconfidencethreshold"></a><span data-ttu-id="c5ef3-103">IAgentCommand::SetConfidenceThreshold</span><span class="sxs-lookup"><span data-stu-id="c5ef3-103">IAgentCommand::SetConfidenceThreshold</span></span>

<span data-ttu-id="c5ef3-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c5ef3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetConfidenceThreshold(
   long lConfidence  // Confidence setting for Command
);
```

<span data-ttu-id="c5ef3-105">Define o valor da propriedade de [**confiança**](confidence-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="c5ef3-105">Sets the value of the [**Confidence**](confidence-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="c5ef3-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c5ef3-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c5ef3-107"><span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*</span><span class="sxs-lookup"><span data-stu-id="c5ef3-107"><span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*</span></span>
</dt> <dd>

<span data-ttu-id="c5ef3-108">O valor da propriedade de [**confiança**](confidence-property.md) de um [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="c5ef3-108">The value for the [**Confidence**](confidence-property.md) property of a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="c5ef3-109">Se o valor de confiança retornado da melhor correspondência retornada no evento de [**comando**](/windows/desktop/lwef/the-command-object) não exceder o valor definido para a propriedade [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) , o texto fornecido em [**SetConfidenceText**](iagentcommand--setconfidencetext.md) será exibido na dica de escuta.</span><span class="sxs-lookup"><span data-stu-id="c5ef3-109">If the confidence value returned of the best match returned in the [**Command**](/windows/desktop/lwef/the-command-object) event does not exceed the value set for the [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) property, the text supplied in [**SetConfidenceText**](iagentcommand--setconfidencetext.md) is displayed in the Listening Tip.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5ef3-110">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="c5ef3-110">See Also</span></span>

<span data-ttu-id="c5ef3-111">[**IAgentCommand:: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand:: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span><span class="sxs-lookup"><span data-stu-id="c5ef3-111">[**IAgentCommand::GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand::SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md)</span></span>


 

 