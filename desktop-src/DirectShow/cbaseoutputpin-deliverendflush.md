---
description: Método CBaseOutputPin. DeliverEndFlush – o método DeliverEndFlush solicita o pino de entrada conectado para finalizar uma operação de liberação.
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: Método CBaseOutputPin. DeliverEndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f3fd5c1bc686ee5c0b4ff0cd1285a5114b93049
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096174"
---
# <a name="cbaseoutputpindeliverendflush-method"></a>Método CBaseOutputPin. DeliverEndFlush

O `DeliverEndFlush` método solicita o PIN de entrada conectado para finalizar uma operação de liberação.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT DeliverEndFlush();
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

Esse método chama o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) no pino de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




