---
description: A propriedade TotalTitleTime recupera o tempo de reprodução total para o título atual.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Propriedade TotalTitleTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd809391394dc661745717ce7d173ad548dfd4d01206c07293024dc8e44a478
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650845"
---
# <a name="totaltitletime-property"></a>Propriedade TotalTitleTime

> [!Note]  
> esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

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

 

 



