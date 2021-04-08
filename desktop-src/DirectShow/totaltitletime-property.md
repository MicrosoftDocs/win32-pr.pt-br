---
description: A propriedade TotalTitleTime recupera o tempo de reprodução total para o título atual.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Propriedade TotalTitleTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a300a2da8de2698a74e0d72362818bd8a2a5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828724"
---
# <a name="totaltitletime-property"></a>Propriedade TotalTitleTime

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

A `TotalTitleTime` propriedade recupera o tempo total de reprodução para o título atual.

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a>Valor Retornado

Retorna o tempo de execução total do título atual como uma cadeia de caracteres no formato "hh: mm: SS: FF".

## <a name="remarks"></a>Comentários

Esta propriedade é somente leitura sem valor padrão. A cadeia de caracteres retornada terá 11 caracteres de comprimento no formato "hh: mm: SS: FF" (horas, minutos, segundos, quadros).

## <a name="see-also"></a>Confira também

<dl> <dt>

[**PlayAtTime**](playattime-method.md)
</dt> <dt>

[**PlayAtTimeInTitle**](playattimeintitle-method.md)
</dt> </dl>

 

 



