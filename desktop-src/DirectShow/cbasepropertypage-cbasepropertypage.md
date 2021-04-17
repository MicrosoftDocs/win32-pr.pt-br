---
description: Método de construtor.
ms.assetid: 5d9863e7-fdd9-4df2-a603-34a240a2286c
title: Construtor CBasePropertyPage. CBasePropertyPage (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.CBasePropertyPage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 915bc42cfb7f152cc061dab76caede6c998edf8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783202"
---
# <a name="cbasepropertypagecbasepropertypage-constructor"></a>Construtor CBasePropertyPage. CBasePropertyPage

Método de construtor.

## <a name="syntax"></a>Sintaxe


```C++
CBasePropertyPage(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   int       DialogId,
   int       TitleId
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pName* 
</dt> <dd>

Cadeia de caracteres que contém o nome do objeto, para fins de depuração. Para obter mais informações, consulte [**CBaseObject:: CBaseObject**](cbaseobject-cbaseobject.md).

</dd> <dt>

*pUnk* 
</dt> <dd>

Ponteiro para a interface **IUnknown** de agregação.

</dd> <dt>

*Caixa de diálogo* 
</dt> <dd>

ID do recurso da caixa de diálogo.

</dd> <dt>

*Título da* 
</dt> <dd>

ID de recurso da cadeia de caracteres que contém o título da caixa de diálogo.

</dd> </dl>

## <a name="examples"></a>Exemplos


```C++
CMyProp::CMyProp(IUnknown *pUnk) : 
    CBasePropertyPage(NAME("MyPropPage"), pUnk, IDD_PROPPAGE, IDS_TITLE),
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>CProp. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




