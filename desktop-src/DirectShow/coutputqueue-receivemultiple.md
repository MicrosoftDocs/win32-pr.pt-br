---
description: O método ReceiveMultiple entrega um lote de amostras de mídia para o pino de entrada.
ms.assetid: e9c7d6ed-fbf9-4c90-8e1e-3bad66cb5d4f
title: Método COutputQueue. ReceiveMultiple (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ReceiveMultiple
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e17e0a8a4856b067907622ec3c8437f5e73a7e38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766320"
---
# <a name="coutputqueuereceivemultiple-method"></a>Método COutputQueue. ReceiveMultiple

O `ReceiveMultiple` método entrega um lote de amostras de mídia para o pino de entrada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReceiveMultiple(
   IMediaSample **ppSamples,
   long         nSamples,
   long         *nSamplesProcessed
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppSamples* 
</dt> <dd>

Endereço de um ponteiro para uma matriz de amostras.

</dd> <dt>

*nSamples* 
</dt> <dd>

Número de amostras na matriz.

</dd> <dt>

*nSamplesProcessed* 
</dt> <dd>

Ponteiro para uma variável que recebe o número de amostras entregues com êxito.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                                                                   |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | Notificação de fim de fluxo recebida antes do processamento deste exemplo.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                                           |



 

## <a name="remarks"></a>Comentários

Se o objeto estiver usando um thread, esse método enfileirará todos os exemplos passados na matriz. Caso contrário, o método chama o método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) no pino de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Outputq. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe COutputQueue**](coutputqueue.md)
</dt> </dl>

 

 




