---
description: 'O método NotifyAllocator especifica um alocador para a conexão. Esse método implementa o método IMemInputPin:: NotifyAllocator.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: Método CTransInPlaceInputPin. NotifyAllocator (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74578243ce780e09d7435f9dd4b70bd9497e1e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751477"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a>Método CTransInPlaceInputPin. NotifyAllocator

O `NotifyAllocator` método especifica um alocador para a conexão. Esse método implementa o método [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pAllocator* 
</dt> <dd>

Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.

</dd> <dt>

*bReadOnly* 
</dt> <dd>

Sinalizador que especifica se os exemplos deste alocador são somente leitura. Se **for true**, os exemplos serão somente leitura.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os valores possíveis incluem os mostrados na tabela a seguir.



| Código de retorno                                                                               | Descrição                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Êxito<br/>                   |
| <dl> <dt>**E \_ falha**</dt> </dl>    | Falha<br/>                   |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Argumento de ponteiro **nulo**<br/> |



 

## <a name="remarks"></a>Comentários

O filtro tenta usar o mesmo alocador para ambas as conexões de PIN.

-   Se o pino de saída não estiver conectado, o PIN de entrada aceitará automaticamente o alocador. Quando o pino de saída estiver conectado, o filtro reconectará o PIN de entrada. Nesse ponto, o filtro tentará novamente usar um único alocador.
-   Se o pino de saída estiver conectado, o PIN de entrada aceitará o alocador. O PIN de saída também usa o mesmo alocador. Ele chama `NotifyAllocator` o pino de entrada downstream.

O caso anterior tem a seguinte exceção:

-   Se o alocador proposto for somente leitura (ou seja, o parâmetro *bReadOnly* for **true**) e o filtro precisar modificar os exemplos, o filtro deverá usar dois alocadores diferentes. Nesse caso, se o filtro upstream estiver propondo para usar o alocador do filtro downstream, o método retornará E \_ falhará.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceInputPin**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




