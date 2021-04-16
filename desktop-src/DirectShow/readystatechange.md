---
description: O evento ReadyStateChange é enviado quando a propriedade ReadyState do controle MSWebDVD é alterada.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46cc8d7ffdee650aac48839d49ed8162e10bb955
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500549"
---
# <a name="readystatechange"></a>ReadyStateChange

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `ReadyStateChange` evento é enviado quando a propriedade **ReadyState** do controle MSWebDVD é alterada.

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*Ready*
</dt> <dd>

Especifica o novo valor da propriedade [**ReadyState**](readystate-property.md) .



| Valor | Descrição               |
|-------|---------------------------|
| 0     | READYstate não \_ inicializado |
| 1     | carregamento de READYstate \_       |
| 2     | READYstate \_ carregado        |
| 3     | READYstate \_ interativo   |
| 4     | READYstate \_ concluído      |



 

</dd> </dl>

 

 



