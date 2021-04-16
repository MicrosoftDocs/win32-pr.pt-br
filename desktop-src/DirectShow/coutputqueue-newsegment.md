---
description: O método NewSegment entrega um novo segmento ao pino de entrada.
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: Método COutputQueue. NewSegment (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e682211a98f4409fda35687160c88b121fa93898
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758539"
---
# <a name="coutputqueuenewsegment-method"></a>Método COutputQueue. NewSegment

O `NewSegment` método entrega um novo segmento ao PIN de entrada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tStart* 
</dt> <dd>

Iniciando a posição de mídia do segmento, em unidades de 100 a nanossegundos.

</dd> <dt>

*tStop* 
</dt> <dd>

Terminar a posição de mídia do segmento, em unidades de 100 a nanossegundos.

</dd> <dt>

*dRate* 
</dt> <dd>

Taxa na qual esse segmento deve ser processado, como uma porcentagem da taxa original.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** .

## <a name="remarks"></a>Comentários

Se o objeto estiver usando um thread, ele enfileirará os seguintes itens, na ordem:

-   Uma nova \_ mensagem de controle de segmento.
-   Os dados do segmento.

A nova \_ mensagem de segmento notifica o thread de que o próximo item na fila conterá dados de segmento. Os dados de segmento são agrupados em uma estrutura, declarados da seguinte maneira:


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



O thread chama o método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) no pino de entrada, usando os dados fornecidos na estrutura.

Se o objeto não estiver usando um thread, ele chamará o método [**COutputQueue:: SendAnyway**](coutputqueue-sendanyway.md) para entregar quaisquer exemplos pendentes. Em seguida, ele chama **IPin:: NewSegment** no pino de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




