---
description: Construtor CRenderedInputPin.CRenderedInputPin – método construtor.
ms.assetid: bf335750-b776-47bc-978d-e84e8b5259f7
title: Construtor CRenderedInputPin.CRenderedInputPin (Amextra.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin.CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b75ce6b5f91f5bd9019a4bf6e46266269b72ac7a5e719f7a58b2f2e702375a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953825"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a>Construtor CRenderedInputPin.CRenderedInputPin

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
CRenderedInputPin(
   TCHAR       *pObjectName,
   CBaseFilter *pFilter,
   CCritSec    *pLock,
   HRESULT     *phr,
   LPCWSTR     pName
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pObjectName* 
</dt> <dd>

Cadeia de caracteres que contém o nome de depuração do objeto. Para obter mais informações, consulte [**Classe CBaseObject**](cbaseobject.md).

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

*Pname* 
</dt> <dd>

Cadeia de caracteres largos que contém o nome do pino (também usado como o identificador de pino).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amextra.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CRenderedInputPin**](crenderedinputpin.md)
</dt> </dl>

 

 




