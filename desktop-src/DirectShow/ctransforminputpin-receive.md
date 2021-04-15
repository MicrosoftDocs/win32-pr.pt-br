---
description: 'O método Receive recebe o exemplo de próxima mídia no fluxo. Esse método implementa o método IMemInputPin:: Receive.'
ms.assetid: 65e4f8f5-2aa2-435b-84b4-e65af3f51afc
title: Método CTransformInputPin. Receive (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 59b087c4b783305b831871a030d1006d576e7d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747370"
---
# <a name="ctransforminputpinreceive-method"></a>Método CTransformInputPin. Receive

O `Receive` método recebe o próximo exemplo de mídia no fluxo. Esse método implementa o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Receive(
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

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição                                                |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl> | O PIN está sendo liberado no momento; o exemplo foi rejeitado.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito.<br/>                                        |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) do PIN, que verifica o estado de streaming do PIN e verifica se há alterações de formato no tipo de mídia. Em seguida, ele chama o método [**CTransformFilter:: Receive**](ctransformfilter-receive.md) do filtro, que processa o exemplo e o entrega downstream.

Se o filtro precisar acessar o exemplo depois que esse método retornar, ele deverá conter uma contagem de referência chamando o método **IUnknown:: AddRef** no exemplo. Por exemplo, alguns filtros de decodificador precisam do exemplo atual para decodificar a próxima amostra.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transfrm. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




