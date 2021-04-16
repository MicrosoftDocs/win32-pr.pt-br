---
description: 'Matriz de amostras de tamanho COutputQueue:: m \_ lBatchSize.'
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: 'Membro COutputQueue:: m_ppSamples (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3659c4a71cacb839caaa1b6ac89e46cd4e42a249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754150"
---
# <a name="coutputqueuem_ppsamples-member"></a>Membro de COutputQueue:: m \_ ppSamples

Matriz de amostras de tamanho [**COutputQueue:: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).

## <a name="syntax"></a>Sintaxe


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a>Comentários

O thread de trabalho extrai amostras da fila e as coloca nessa matriz. Ele passa a matriz para o método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) . Se o objeto não estiver usando um thread de trabalho, o objeto colocará amostras diretamente nessa matriz. A variável de membro da [**\_ lista COutputQueue:: m**](coutputqueue-m-list.md) contém a fila.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




