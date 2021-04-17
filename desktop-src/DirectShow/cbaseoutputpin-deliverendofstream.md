---
description: O método DeliverEndOfStream entrega uma notificação de fim de fluxo para o pino de entrada conectado.
ms.assetid: 5b564675-a1e0-4010-b35d-28315c262bcc
title: Método CBaseOutputPin. DeliverEndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 334101c9b61631a35c5da91bd398cb7742d39235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752715"
---
# <a name="cbaseoutputpindeliverendofstream-method"></a>Método CBaseOutputPin. DeliverEndOfStream

O `DeliverEndOfStream` método fornece uma notificação de fim de fluxo para o PIN de entrada conectado.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT DeliverEndOfStream();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>              |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O PIN não está conectado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) no pino de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




