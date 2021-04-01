---
description: O método PlayPeriodInTitleAutoStop inicia a reprodução na hora especificada no título especificado até a hora de parada especificada.
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: Método PlayPeriodInTitleAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05899b66b7f1a11f8f5b177d311b9634a52595b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825694"
---
# <a name="playperiodintitleautostop-method"></a>Método PlayPeriodInTitleAutoStop

> [!Note]  
> Esse componente está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003. Ele poderá ser alterado ou ficar indisponível em versões subsequentes.

 

O `PlayPeriodInTitleAutoStop` método inicia a reprodução na hora especificada no título especificado até a hora de parada especificada.

``` syntax
MSWebDVD.PlayPeriodInTitleAutoStop(iTitle, sStartTime, sEndTime)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

Especifica o título como um inteiro.

</dd> <dt>

<span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*
</dt> <dd>

Especifica a hora de início como uma cadeia de caracteres no formato "hh: mm: SS: FF" (especificando horas, minutos, segundos, quadros).

</dd> <dt>

<span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*Enviartime*
</dt> <dd>

Especifica a hora de término como uma cadeia de caracteres no formato "hh: mm: SS: FF".

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Sem valor de retorno.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**PlayChaptersAutoStop**](playchaptersautostop-method.md)
</dt> </dl>

 

 



