---
description: O evento ReadyStateChange é enviado quando a propriedade ReadyState do controle MSWebDVD é alterada.
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f73e0b5b7cd7178df31b3f6efda56e398d8cb406598355a3c49702714686af3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697116"
---
# <a name="readystatechange"></a>ReadyStateChange

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

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

 

 



