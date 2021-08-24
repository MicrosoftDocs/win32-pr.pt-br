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
ms.openlocfilehash: 4057cafa3962c85fbca9342debbf7bb0e92355fc083e693889df298e53509259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768136"
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

## <a name="return-value"></a>Valor retornado

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
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir Fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




