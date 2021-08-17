---
description: O método PlayAtTimeInTitle inicia a reprodução no momento especificado dentro do título especificado.
ms.assetid: 82726885-8393-409b-b8a1-29a8e9e9ac65
title: Método PlayAtTimeInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33640733f7333395a4affc4dedc0ae8db3e3558bf066584cb603dfc5f906f73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119291264"
---
# <a name="playattimeintitle-method"></a>Método PlayAtTimeInTitle

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `PlayAtTimeInTitle` método inicia a reprodução no momento especificado dentro do título especificado.

``` syntax
MSWebDVD.PlayAtTimeInTitle(sTime, iTitle)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*Stime*
</dt> <dd>

Especifica a hora em que iniciar a reprodução como uma cadeia de caracteres. A cadeia de caracteres deve estar no formato "hh:mm:ss:ff" (especificando horas, minutos, segundos, quadros).

</dd> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Especifica o índice do título como um Inteiro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**CurrentTitle**](currenttitle-property.md)
</dt> <dt>

[**PlayAtTime**](playattime-method.md)
</dt> <dt>

[**TitlesAvailable**](titlesavailable-property.md)
</dt> </dl>

 

 



