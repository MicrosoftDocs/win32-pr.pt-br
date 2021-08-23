---
description: Construtor CAMMsgEvent.CAMMsgEvent – método construtor.
ms.assetid: 7871a624-70c0-4f21-b62a-2c4c2eaa762b
title: Construtor CAMMsgEvent.CAMMsgEvent (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fc2eeaab10134022388e6a57628d1c3c5a87fc0e0a443efab19f016a1e5c27b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955495"
---
# <a name="cammsgeventcammsgevent-constructor"></a>Construtor CAMMsgEvent.CAMMsgEvent

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
CAMMsgEvent(
   HRESULT *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Phr* 
</dt> <dd>

Ponteiro para um **valor HRESULT.** Se o construtor falhar, esse parâmetro receberá um código de erro. Se isso ocorrer, o objeto não está em um estado válido.

Para compatibilidade com versões anteriores do strmbase.lib, esse parâmetro assume null como **padrão.** No entanto, é preferível passar **um valor** não NULL para que o chamador possa verificar o status do objeto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Wxutil.h (incluir Fluxos.h)</dt> </dl>                                                                                    |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CAMMsgEvent**](cammsgevent.md)
</dt> </dl>

 

 




