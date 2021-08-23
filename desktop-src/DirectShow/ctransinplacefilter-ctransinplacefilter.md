---
description: Construtor CTransInPlaceFilter.CTransInPlaceFilter – Método do construtor.
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: Construtor CTransInPlaceFilter.CTransInPlaceFilter (Transip.h)
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
ms.openlocfilehash: 98fb678a2df7c79e40c5ecf39b0a059ebc9e44f4f3f603e1d1a6551446204aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767576"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a>Construtor CTransInPlaceFilter.CTransInPlaceFilter

Método do construtor.

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

Cadeia de caracteres que contém o nome de depuração do filtro. Para obter mais informações, [**consulte CBaseObject**](cbaseobject.md).

</dd> <dt>

*lpUnk* 
</dt> <dd>

Ponteiro para o proprietário desse objeto. Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação. Caso contrário, de definido esse parâmetro como **NULL.**

</dd> <dt>

*Clsid* 
</dt> <dd>

Identificador de classe do filtro.

</dd> <dt>

*Phr* 
</dt> <dd>

Ignorado.

</dd> <dt>

*bModifiesData* 
</dt> <dd>

Valor booliana que especifica se o filtro modifica os dados de entrada. Se **TRUE**, o filtro modificará os dados. Caso contrário, o filtro passará os dados downstream inalterados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Transip.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CTransInPlaceFilter**](ctransinplacefilter.md)
</dt> </dl>

 

 




