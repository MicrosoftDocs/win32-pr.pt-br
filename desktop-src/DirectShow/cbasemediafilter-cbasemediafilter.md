---
description: Método de construtor.
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Construtor CBaseMediaFilter. CBaseMediaFilter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498e9da88804291fc5cdb900ff1dbda212e8b0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753362"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a>Construtor CBaseMediaFilter. CBaseMediaFilter

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* 
</dt> <dd>

Ponteiro para uma cadeia de caracteres que contém o nome do objeto.

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

Identificador de classe do objeto.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se outro objeto contiver ou agregar o `CBaseMediaFilter` objeto, o bloqueio **CCritSec** poderá ser externo ao `CBaseMediaFilter` objeto. Nesse caso, passe um ponteiro para o bloqueio em *pLock*.

Caso contrário, você pode:

-   Derive uma classe que herda `CBaseMediaFilter` e **CCritSec**. Para *pLock*, passe o ponteiro.
-   Derive uma classe que herda `CBaseMediaFilter` e contém uma variável de membro **CCritSec** . Para *pLock*, passe o endereço dessa variável.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBaseMediaFilter**](cbasemediafilter.md)
</dt> </dl>

 

 




