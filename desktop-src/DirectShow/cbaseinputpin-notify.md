---
description: 'Método CBaseInputPin. Notify – o método Notify notifica o PIN de que uma alteração de qualidade é solicitada. Esse método implementa o método IQualityControl:: Notify.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: Método CBaseInputPin. Notify (Amfilter. h)
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
ms.openlocfilehash: 610888193762618d427a0329a27d3019bd625e69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119994"
---
# <a name="cbaseinputpinnotify-method"></a>Método CBaseInputPin. Notify

O `Notify` método notifica o PIN de que uma alteração de qualidade é solicitada. Esse método implementa o método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .

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

*perguntas* 
</dt> <dd>

Estrutura de [**qualidade**](/windows/win32/api/strmif/ns-strmif-quality) que contém a mensagem de controle de qualidade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna S \_ OK.

## <a name="remarks"></a>Comentários

Os filtros normalmente passam mensagens de controle de qualidade para um pino de saída upstream, não para um pino de entrada. Portanto, esse método retorna S \_ OK sem fazer nada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> <dt>

[Gerenciamento de controle de qualidade](quality-control-management.md)
</dt> </dl>

 

 




