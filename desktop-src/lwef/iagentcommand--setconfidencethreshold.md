---
title: IAgentCommand SetConfidenceThreshold
description: IAgentCommand SetConfidenceThreshold
ms.assetid: f62d646a-895d-468c-9397-0495680109a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 244f181fb4d9e706271440797e1261fd381897e00a5a216d681e0f3984d24a6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976296"
---
# <a name="iagentcommandsetconfidencethreshold"></a>IAgentCommand::SetConfidenceThreshold

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT SetConfidenceThreshold(
   long lConfidence  // Confidence setting for Command
);
```

Define o valor da propriedade de [**confiança**](confidence-property.md) para um [**comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="lConfidence"></span><span id="lconfidence"></span><span id="LCONFIDENCE"></span>*lConfidence*
</dt> <dd>

O valor da propriedade de [**confiança**](confidence-property.md) de um [**comando**](/windows/desktop/lwef/the-command-object).

</dd> </dl>

Se o valor de confiança retornado da melhor correspondência retornada no evento de [**comando**](/windows/desktop/lwef/the-command-object) não exceder o valor definido para a propriedade [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) , o texto fornecido em [**SetConfidenceText**](iagentcommand--setconfidencetext.md) será exibido na dica de escuta.

## <a name="see-also"></a>Consulte Também

[**IAgentCommand:: GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md), [**IAgentCommand:: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 