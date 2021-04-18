---
description: O método AttemptConnection se conecta a outro PIN usando um tipo de mídia especificado.
ms.assetid: b80cf2c0-7266-4dac-8633-d30a871c57d9
title: Método CBasePin. AttemptConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.AttemptConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72f80d81b5f105f528292a23f8b58257066b425e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751266"
---
# <a name="cbasepinattemptconnection-method"></a>Método CBasePin. AttemptConnection

O `AttemptConnection` método se conecta a outro PIN usando um tipo de mídia especificado.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT AttemptConnection(
         IPin       *pReceivePin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de recebimento.

</dd> <dt>

*PMT* 
</dt> <dd>

Ponteiro para um objeto [**CMediaType**](cmediatype.md) que especifica o tipo de mídia.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os da tabela a seguir.



| Código de retorno                                                                                                | Descrição                                  |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Êxito.<br/>                          |
| <dl> <dt>**\_tipo E \_ VFW \_ não \_ aceito**</dt> </dl> | O tipo de mídia não é aceitável.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método tenta conectar os dois Pins com um tipo de mídia específico. Se o tipo não for aceitável, o método falhará sem tentar outros tipos de mídia.

Se o tipo de mídia for aceitável, esse método chamará o método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) do pino de recebimento. Em seguida, ele chama o método [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) para concluir a conexão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




