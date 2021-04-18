---
description: Método de construtor.
ms.assetid: bf335750-b776-47bc-978d-e84e8b5259f7
title: Construtor CRenderedInputPin. CRenderedInputPin (Amextra. h)
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
ms.openlocfilehash: ee1ec8944d56d2aa6f46e59ac5034969ca77ea19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749616"
---
# <a name="crenderedinputpincrenderedinputpin-constructor"></a>Construtor CRenderedInputPin. CRenderedInputPin

Método de construtor.

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

Cadeia de caracteres que contém o nome de depuração do objeto. Para obter mais informações, consulte [**classe CBaseObject**](cbaseobject.md).

</dd> <dt>

*pFilter* 
</dt> <dd>

Ponteiro para o filtro que criou este pin.

</dd> <dt>

*pLock* 
</dt> <dd>

Ponteiro para um bloqueio de [**CCritSec**](ccritsec.md) , usado para serializar alterações de estado. Essa pode ser a mesma seção crítica que o bloqueio de filtro, [**CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md).

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para uma variável que recebe um valor **HRESULT** que indica o êxito ou a falha do método.

</dd> <dt>

*pName* 
</dt> <dd>

Cadeia de caracteres largos contendo o nome do PIN (também usado como o identificador do PIN).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amextra. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CRenderedInputPin**](crenderedinputpin.md)
</dt> </dl>

 

 




