---
title: IAgentCommand GetConfidenceThreshold
description: IAgentCommand GetConfidenceThreshold
ms.assetid: dfbaba7c-ed45-464e-82ab-39e33c023e89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e4297012db2118da2fe5db79dbe8e969d9b4006b4078198a0d384898fc9fa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976376"
---
# <a name="iagentcommandgetconfidencethreshold"></a>IAgentCommand::GetConfidenceThreshold

\[o Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]

``` syntax
HRESULT GetConfidenceThreshold(
long * plConfidenceThreshold  // address of ConfidenceThreshold 
);                            // setting for Command
```

Recupera o valor da propriedade [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) para um [**comando**](/windows/desktop/lwef/the-command-object).

-   Retorna S \_ OK para indicar que a operação foi bem-sucedida.

<dl> <dt>

<span id="plConfidenceThreshold"></span><span id="plconfidencethreshold"></span><span id="PLCONFIDENCETHRESHOLD"></span>*plConfidenceThreshold*
</dt> <dd>

O endereço de uma variável que recebe o valor da propriedade [**ConfidenceThreshold**](/windows/desktop/lwef/confidence-property) para um comando.

</dd> </dl>

## <a name="see-also"></a>Consulte Também

[**IAgentCommand:: SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md), [**IAgentCommand:: SetConfidenceText**](iagentcommand--setconfidencetext.md), [**IAgentUserInput:: GetItemConfidence**](iagentuserinput--getitemconfidence.md)


 

 