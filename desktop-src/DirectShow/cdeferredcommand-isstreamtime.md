---
description: O método IsStreamTime especifica se o comando deve ser executado em tempo de transmissão ou em tempo de apresentação.
ms.assetid: 4fb315a4-1bc6-49c8-a47f-0a8a46f3f790
title: Método CDeferredCommand.IsStreamTime (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.IsStreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82c541220a2b89ecdd23e4676175f4c7b2aacd93aac008546349b38e7bc2455a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657198"
---
# <a name="cdeferredcommandisstreamtime-method"></a>Método CDeferredCommand.IsStreamTime

O `IsStreamTime` método especifica se o comando deve ser executado em tempo de transmissão ou em tempo de apresentação.

## <a name="syntax"></a>Sintaxe


```C++
BOOL IsStreamTime();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará **TRUE** se definido como tempo de fluxo; caso contrário, **retornará FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CDeferredCommand**](cdeferredcommand.md)
</dt> </dl>

 

 




