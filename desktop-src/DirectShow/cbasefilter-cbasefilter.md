---
description: Construtor CBaseFilter.CBaseFilter(const \* TCHAR, LPUNKNOWN, CCritSec, \* REFCLSID, HRESULT \* ) – método constructor.
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: Construtor CBaseFilter.CBaseFilter(const *TCHAR, LPUNKNOWN, CCritSec,* REFCLSID, HRESULT*) (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 023de6fd8df37930954b59114e4e00fa409b7803a83ae15b31f6816c4dfdffbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640706"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a>Construtor CBaseFilter.CBaseFilter(const \* TCHAR, LPUNKNOWN, CCritSec, \* REFCLSID, HRESULT \* )

Método do construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid,
         HRESULT   *phr
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pname* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do filtro, para fins de depuração.

</dd> <dt>

*Punk* 
</dt> <dd>

Ponteiro para o proprietário desse objeto. Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação. Caso contrário, de definido esse parâmetro como **NULL.**

</dd> <dt>

*Plock* 
</dt> <dd>

Ponteiro para um [**bloqueio CCritSec,**](ccritsec.md) usado para serializar alterações de estado.

</dd> <dt>

*Clsid* 
</dt> <dd>

CLSID (identificador de classe) do filtro.

</dd> <dt>

*Phr* 
</dt> <dd>

Ponteiro para um **valor HRESULT.** O construtor ignora esse parâmetro.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para o objeto de seção crítico, normalmente você faria um dos seguintes:

-   Derive uma classe que herda **CBaseFilter** e **CCritSec.** Para *pLock,* passe o `this` ponteiro .
-   Derive uma classe que herda **CBaseFilter** e contém uma variável de membro **CCritSec.** Para *pLock*, passe o endereço dessa variável.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter.h (incluir Fluxos.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




