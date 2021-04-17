---
description: O método CompleteConnect conclui uma conexão com outro PIN.
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Método CBasePin. CompleteConnect (Amfilter. h)
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
ms.openlocfilehash: 9068bf63d3168a8c6d9e1bca2ef709f63e80a3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811758"
---
# <a name="cbasepincompleteconnect-method"></a>Método CBasePin. CompleteConnect

O `CompleteConnect` método conclui uma conexão com outro PIN.

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

Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do outro PIN.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Esse método é chamado em ambos os Pins no final do processo de conexão. O PIN de conexão o chama de dentro do método [**CBasePin:: Connect**](cbasepin-connect.md) e o PIN de recebimento o chama de dentro do método [**CBasePin:: ReceiveConnection**](cbasepin-receiveconnection.md) .

Na classe base, esse método simplesmente retorna S \_ OK. Se uma classe derivada tiver quaisquer requisitos para concluir uma conexão, ela deverá substituir esse método. Por exemplo, a classe [**CBaseOutputPin**](cbaseoutputpin.md) usa esse método para decidir o alocador de memória.

Se esse método falhar, a tentativa de conexão geral também falhará e o PIN desconectará do PIN de recebimento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePin**](cbasepin.md)
</dt> </dl>

 

 




