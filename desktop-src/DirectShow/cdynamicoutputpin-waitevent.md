---
description: O método WaitEvent aguarda até que o evento especificado seja sinalizado.
ms.assetid: 64880f46-7b8f-4823-9d50-052e30ecf04b
title: Método CDynamicOutputPin.WaitEvent (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.WaitEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3797c9127d3e931cd64fa35e822eac3151acc7fa1a8c4c0c9e93d6a36c0dfe99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871925"
---
# <a name="cdynamicoutputpinwaitevent-method"></a>Método CDynamicOutputPin.WaitEvent

O `WaitEvent` método aguarda até que o evento especificado seja sinalizado.

## <a name="syntax"></a>Sintaxe


```C++
static HRESULT WaitEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hevent* 
</dt> <dd>

Manipular para um evento.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os valores possíveis incluem aqueles mostrados na tabela a seguir.



| Código de retorno                                                                                  | Descrição                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>          |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Erro inesperado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> </dl>

 

 




