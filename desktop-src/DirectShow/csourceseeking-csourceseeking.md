---
description: Construtor de CSourceSeeking. CSourceSeeking-método de construtor.
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: Construtor CSourceSeeking. CSourceSeeking (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7fcca70408e76466a88c620e3907271d49930973
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098814"
---
# <a name="csourceseekingcsourceseeking-constructor"></a>Construtor CSourceSeeking. CSourceSeeking

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do objeto. Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para o proprietário deste objeto. Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação. Caso contrário, defina esse parâmetro como **NULL**.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para um valor **HRESULT** . Ignorado.

</dd> <dt>

*pLock* 
</dt> <dd>

Ponteiro para um objeto [**CCritSec**](ccritsec.md) . Na classe derivada, declare uma variável de membro **CCritSec** e use o endereço dela para esse parâmetro. A `CSourceSeeking` classe usa essa seção crítica para sincronizar o acesso às horas de início e parada, à duração e à taxa de reprodução. Sempre que você acessar essas variáveis em sua classe derivada, mantenha esse bloqueio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Ctlutil. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CSourceSeeking**](csourceseeking.md)
</dt> </dl>

 

 




