---
description: O método de entrega fornece um exemplo de mídia para o pino de entrada conectado.
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: Método CBaseOutputPin. entregue (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Deliver
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adc603e4cdd1f49e649264d2d82d6df0fb12569
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769246"
---
# <a name="cbaseoutputpindeliver-method"></a>Método CBaseOutputPin. entregue

O `Deliver` método entrega um exemplo de mídia para o pino de entrada conectado.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT Deliver(
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

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>              |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O PIN não está conectado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) no pino de entrada. **Receive** pode bloquear se o método [**IMemInputPin:: ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) retornar S \_ OK.

Libere o exemplo depois de chamar esse método. O PIN de entrada pode conter uma contagem de referência no exemplo, portanto, não reutilize o exemplo. Sempre chame o método [**CBaseOutputPin:: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) para obter um novo exemplo.

Mantenha a seção crítica do filtro antes de chamar este método. Caso contrário, o PIN poderá ser desconectado durante a chamada do método. Se o filtro usar um thread de trabalho para entregar exemplos, mantenha a seção crítica quando o filtro estiver pronto para entregar um exemplo. Caso contrário, você pode manter a seção crítica no método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) do filtro, em que o filtro processa amostras.

Os threads de trabalho podem criar um deadlock potencial. Quando o thread mantém a seção crítica, ele pode aguardar uma alteração de estado no filtro. Ao mesmo tempo, a alteração de estado pode estar aguardando a conclusão do thread. Para evitar isso, o código de alteração de Estado deve sinalizar um evento que encerra o thread e, em seguida, esperar que o thread sinalize a conclusão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




