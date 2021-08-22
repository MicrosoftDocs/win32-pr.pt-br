---
description: Construtor CBaseInputPin.CBaseInputPin – Método de construtor.
ms.assetid: a853813d-cdf6-4cb4-8288-62685a883b56
title: Construtor CBaseInputPin.CBaseInputPin (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 526c10dc0cda2f9b4d4cee6a955620f2aa1aae697522aaf3e14e57c3317ca325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017064"
---
# <a name="cbaseinputpincbaseinputpin-constructor"></a>Construtor CBaseInputPin.CBaseInputPin

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pPinName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pObjectName* 
</dt> <dd>

Cadeia de caracteres que contém o nome de depuração do objeto. Para obter mais informações, [**consulte CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Ponteiro para o filtro que criou esse pino.

</dd> <dt>

*Plock* 
</dt> <dd>

Ponteiro para um [**bloqueio CCritSec,**](ccritsec.md) usado para serializar alterações de estado. Essa pode ser a mesma seção crítica que o bloqueio de filtro, [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md).

</dd> <dt>

*Phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um **valor HRESULT** que indica o êxito ou a falha do método.

</dd> <dt>

*pPinName* 
</dt> <dd>

Cadeia de caracteres largos que contém o nome do pino (também usado como o identificador de pino).

</dd> </dl>

## <a name="remarks"></a>Comentários

Todos os parâmetros são passados diretamente para o construtor [**CBasePin.**](cbasepin-cbasepin.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseInputPin**](cbaseinputpin.md)
</dt> </dl>

 

 




