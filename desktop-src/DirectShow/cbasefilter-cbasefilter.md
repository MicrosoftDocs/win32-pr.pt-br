---
description: Método de construtor de Construtor CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec, \* REFCLSID, HRESULT \* ).
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: Construtor CBaseFilter. CBaseFilter (const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID, HRESULT *) (Amfilter. h)
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
ms.openlocfilehash: f85fc666d299d5e120f71cfeaec5fc2f88e72761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120104"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a>Construtor CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec, \* REFCLSID, HRESULT \* )

Método de construtor.

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

*pName* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do filtro, para fins de depuração.

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para o proprietário deste objeto. Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação. Caso contrário, defina esse parâmetro como **NULL**.

</dd> <dt>

*pLock* 
</dt> <dd>

Ponteiro para um bloqueio de [**CCritSec**](ccritsec.md) , usado para serializar alterações de estado.

</dd> <dt>

*CLSID* 
</dt> <dd>

Identificador de classe (CLSID) do filtro.

</dd> <dt>

*phr* 
</dt> <dd>

Ponteiro para um valor **HRESULT** . O Construtor ignora esse parâmetro.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para o objeto seção crítica, você normalmente faria um dos seguintes:

-   Derive uma classe que herde **CBaseFilter** e **CCritSec**. Para *pLock*, passe o `this` ponteiro.
-   Derive uma classe que herda **CBaseFilter** e contém uma variável de membro **CCritSec** . Para *pLock*, passe o endereço dessa variável.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CBaseFilter**](cbasefilter.md)
</dt> </dl>

 

 




