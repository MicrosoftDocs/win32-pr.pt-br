---
description: Sinalizador que especifica se o objeto fornece amostras em lotes exatos.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: Membro COutputQueue::m_bBatchExact (Outputq.h)
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
ms.openlocfilehash: 6b5859744c3670ccc789ae5d87a619b3b32c3731580d473ff8cc6d775348771f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087246"
---
# <a name="coutputqueuem_bbatchexact-member"></a>Membro COutputQueue::m \_ bBatchExact

Sinalizador que especifica se o objeto fornece amostras em lotes exatos.

## <a name="syntax"></a>Sintaxe


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a>Comentários

Se o valor for **TRUE,** o objeto aguardará até que tenha um lote completo de exemplos de mídia antes de entregar qualquer um. Caso contrário, ele fornecerá exemplos conforme eles chegam. A [**variável membro COutputQueue::m \_ lBatchSize**](coutputqueue-m-lbatchsize.md) define o tamanho do lote.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




