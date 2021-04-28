---
description: Método CBaseOutputPin. DeliverBeginFlush – o método DeliverBeginFlush solicita o pino de entrada conectado para iniciar uma operação de liberação.
ms.assetid: 0d7c7bd7-2a7a-42a4-a0de-60205b62e49c
title: Método CBaseOutputPin. DeliverBeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverBeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 22dbd2bccf33d9f203d1505106184500b8cae3ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099514"
---
# <a name="cbaseoutputpindeliverbeginflush-method"></a>Método CBaseOutputPin. DeliverBeginFlush

O `DeliverBeginFlush` método solicita o PIN de entrada conectado para iniciar uma operação de liberação.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT DeliverBeginFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um valor **HRESULT** . Os valores possíveis incluem os listados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Sucesso.<br/>              |
| <dl> <dt>**VFW \_ E \_ não \_ conectado**</dt> </dl> | O PIN não está conectado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método chama o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) no pino de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




