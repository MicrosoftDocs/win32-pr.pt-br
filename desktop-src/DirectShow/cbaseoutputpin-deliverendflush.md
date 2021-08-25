---
description: Método CBaseOutputPin.DeliverEndFlush – o método DeliverEndFlush solicita o pino de entrada conectado para encerrar uma operação de liberação.
ms.assetid: 9f1fd76c-dba7-41c5-b098-9735e4f2571b
title: Método CBaseOutputPin.DeliverEndFlush (Amfilter.h)
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
ms.openlocfilehash: 6225406d23dd409c9d2b1ff3dcb7669fa468d8f8cba6c49773dbe057c4545cc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076556"
---
# <a name="cbaseoutputpindeliverendflush-method"></a>Método CBaseOutputPin.DeliverEndFlush

O `DeliverEndFlush` método solicita o pino de entrada conectado para encerrar uma operação de liberação.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT DeliverEndFlush();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles listados na tabela a seguir.



| Código de retorno                                                                                           | Descrição                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Êxito.<br/>              |
| <dl> <dt>**VFW \_ E \_ NÃO \_ CONECTADO**</dt> </dl> | O pino não está conectado.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método chama o [**método IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) no pino de entrada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




