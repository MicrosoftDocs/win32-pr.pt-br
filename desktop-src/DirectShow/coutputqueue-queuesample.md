---
description: O método QueueSample enfileira um exemplo.
ms.assetid: f34c0689-5afb-4941-bc3a-e4765fbbe525
title: Método COutputQueue. QueueSample (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.QueueSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45b1295ea1a9ded145356e6b0495b7b873dff200
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758538"
---
# <a name="coutputqueuequeuesample-method"></a>Método COutputQueue. QueueSample

O `QueueSample` método enfileira um exemplo.

## <a name="syntax"></a>Sintaxe


```C++
void QueueSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSample* 
</dt> <dd>

Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método adiciona um exemplo à parte final da fila. Mantenha a seção crítica antes de chamar esse método e chame-a somente quando o objeto estiver usando um thread para fornecer exemplos. Para determinar se o objeto está usando um thread, chame o método [**COutputQueue:: IsQueued**](coutputqueue-isqueued.md) .

Esse método também pode ser usado para colocar as mensagens de controle na fila. Uma mensagem de controle é uma constante definida (conversão para um \_ tipo PTR longo) que instrui o thread a executar alguma ação. A classe **COutputQueue** define as mensagens de controle mostradas na tabela a seguir.



|               |                                        |
|---------------|----------------------------------------|
| Mensagem       | Ação                                 |
| \_pacote EOS   | Fornecer uma notificação de fim de fluxo. |
| NOVO \_ segmento  | Entregar um novo segmento.                 |
| REDEFINIR \_ pacote | Redefina o estado da fila.          |
| Enviar \_ pacote  | Envie um lote parcial de exemplos.       |



 

Esse é um método protegido, que a classe **COutputQueue** usa internamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




