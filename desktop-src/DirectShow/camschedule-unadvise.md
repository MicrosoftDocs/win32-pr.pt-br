---
description: O método Unadvise remove uma solicitação de aviso.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: Método CAMSchedule. Unadvise (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Unadvise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25dd70a46fcc2b6572500b3164b64fd0facbcbe0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752115"
---
# <a name="camscheduleunadvise-method"></a>Método CAMSchedule. Unadvise

O `Unadvise` método remove uma solicitação de aviso.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Unadvise(
   DWORD_PTR dwAdviseCookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwAdviseCookie* 
</dt> <dd>

Identificador da solicitação de aviso, retornado pelo método [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um dos valores **HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <dt>**\_falso**</dt> </dl> | Não encontrado<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Sucesso<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dsschedule. h (incluir fluxos. h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




