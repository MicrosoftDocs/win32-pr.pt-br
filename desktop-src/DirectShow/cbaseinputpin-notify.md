---
description: Método CBaseInputPin.Notify – o método Notify notifica o pino de que uma alteração de qualidade é solicitada. Esse método implementa o método IQualityControl::Notify.
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: Método CBaseInputPin.Notify (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2067c7698c1af7d7295cffed552ab4f58d0402594dd13bfd82224c81652b9aff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659158"
---
# <a name="cbaseinputpinnotify-method"></a>Método CBaseInputPin.Notify

O `Notify` método notifica o pino de que uma alteração de qualidade é solicitada. Esse método implementa o [**método IQualityControl::Notify.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify)

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pSelf* 
</dt> <dd>

Ponteiro para o filtro que está enviando a mensagem de controle de qualidade.

</dd> <dt>

*Q* 
</dt> <dd>

[**Estrutura**](/windows/win32/api/strmif/ns-strmif-quality) de qualidade que contém a mensagem de controle de qualidade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Os filtros geralmente passam mensagens de controle de qualidade para um pino de saída upstream, não para um pino de entrada. Portanto, esse método retorna S \_ OK sem fazer nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> <dt>

[Gerenciamento de controle de qualidade](quality-control-management.md)
</dt> </dl>

 

 




