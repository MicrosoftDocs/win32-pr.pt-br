---
description: Sinalizador que especifica se o objeto fornece amostras em lotes exatos.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: 'Membro COutputQueue:: m_bBatchExact (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bBatchExact
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5f38d8a0e7335025688f52015ff9ed4d4892820
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750470"
---
# <a name="coutputqueuem_bbatchexact-member"></a>Membro de COutputQueue:: m \_ bBatchExact

Sinalizador que especifica se o objeto fornece amostras em lotes exatos.

## <a name="syntax"></a>Sintaxe


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a>Comentários

Se o valor for **true**, o objeto aguardará até que ele tenha um lote completo de amostras de mídia antes de entregar qualquer. Caso contrário, ele fornece exemplos à medida que eles chegam. A variável de membro [**COutputQueue:: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md) define o tamanho do lote.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




