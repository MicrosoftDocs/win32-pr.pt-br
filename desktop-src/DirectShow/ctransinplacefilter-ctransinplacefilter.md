---
description: Construtor de CTransInPlaceFilter. CTransInPlaceFilter-método de construtor.
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: Construtor CTransInPlaceFilter. CTransInPlaceFilter (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d6b14af4b0d1f33933db8ca2fd1835e9711edad9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084774"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a>Construtor CTransInPlaceFilter. CTransInPlaceFilter

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pObjectName* 
</dt> <dd>

Cadeia de caracteres que contém o nome de depuração do filtro. Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*lpUnk* 
</dt> <dd>

Ponteiro para o proprietário deste objeto. Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação. Caso contrário, defina esse parâmetro como **NULL**.

</dd> <dt>

*CLSID* 
</dt> <dd>

Identificador de classe do filtro.

</dd> <dt>

*phr* 
</dt> <dd>

Ignorado.

</dd> <dt>

*bModifiesData* 
</dt> <dd>

Valor booliano que especifica se o filtro modifica os dados de entrada. Se **for true**, o filtro modificará os dados. Caso contrário, o filtro passará o downstream de dados inalterado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>TRANSip. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




