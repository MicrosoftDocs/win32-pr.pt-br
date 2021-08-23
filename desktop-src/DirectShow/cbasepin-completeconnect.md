---
description: Método CBasePin.CompleteConnect – o método CompleteConnect conclui uma conexão com outro pin.
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Método CBasePin.CompleteConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e31829829a99dc613cfeeeda7ad8a9871c1a3ec4fee99220b804b171bbdcdc29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074780"
---
# <a name="cbasepincompleteconnect-method"></a>Método CBasePin.CompleteConnect

O `CompleteConnect` método conclui uma conexão com outro pin.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro pino.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método é chamado em ambos os pinos no final do processo de conexão. O pino de conexão chama-o de dentro do método [**CBasePin::Conexão**](cbasepin-connect.md) e o pin receptor o chama de dentro do [**método CBasePin::ReceiveConnection.**](cbasepin-receiveconnection.md)

Na classe base, esse método simplesmente retorna S \_ OK. Se uma classe derivada tiver requisitos para concluir uma conexão, ela deverá substituir esse método. Por exemplo, a [**classe CBaseOutputPin**](cbaseoutputpin.md) usa esse método para decidir o alocador de memória.

Se esse método falhar, a tentativa de conexão geral também falhará e o pino se desconecta do pino de recebimento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




