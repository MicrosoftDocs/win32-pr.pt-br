---
description: Número de threads de streaming usando esse pino.
ms.assetid: f8650a17-edab-4d69-91da-78107c3c60b9
title: Membro CDynamicOutputPin::m_dwNumOutstandingOutputPinUsers (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwNumOutstandingOutputPinUsers
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 29fc593065af4252f58ce4bb08dd41fac82926dc11490377f6a8af614794b22a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688706"
---
# <a name="cdynamicoutputpinm_dwnumoutstandingoutputpinusers-member"></a>Membro CDynamicOutputPin::m \_ dwNumOutstandingOutputPinUsers

Número de threads de streaming usando esse pino.

## <a name="syntax"></a>Sintaxe


```C++
DWORD m_dwNumOutstandingOutputPinUsers;
```



## <a name="remarks"></a>Comentários

O [**método CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) incrementa essa variável e o método [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) a decrementa. Quando o valor é maior que zero, algum thread está usando esse pin para transmitir dados ou para alterar o tipo de conexão. O pino não pode ser bloqueado enquanto esse é o caso.

Antes de acessar essa variável, mantenha a [**seção crítica CDynamicOutputPin::m \_ BlockStateLock.**](cdynamicoutputpin-m-blockstatelock.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDynamicOutputPin**](cdynamicoutputpin.md)
</dt> <dt>

[**CDynamicOutputPin::StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)
</dt> </dl>

 

 




