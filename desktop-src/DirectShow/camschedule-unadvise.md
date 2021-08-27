---
description: O método Unadvise remove uma solicitação de consultoria.
ms.assetid: b3dfda82-577e-4499-a114-1c8721e4af9e
title: Método CAMSchedule.Unadvise (Dsschedule.h)
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
ms.openlocfilehash: 6bc9b1c964d698e1c1323846c7a25a29f60c0cd71009fbb60f1a09a6757b50b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057596"
---
# <a name="camscheduleunadvise-method"></a>Método CAMSchedule.Unadvise

O `Unadvise` método remove uma solicitação de consultoria.

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

Identificador da solicitação de consultoria, retornado pelo [**método CAMSchedule::AddAdvisePacket.**](camschedule-addadvisepacket.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um dos **valores HRESULT** mostrados na tabela a seguir.



| Código de retorno                                                                             | Descrição          |
|-----------------------------------------------------------------------------------------|----------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Não encontrado<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Êxito<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Dsschedule.h (incluir Fluxos.h)</dt> </dl>                                                                                |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMSchedule**](camschedule.md)
</dt> </dl>

 

 




