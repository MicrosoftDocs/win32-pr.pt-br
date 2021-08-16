---
description: O método Apply aplica os valores de página da propriedade atual ao objeto associado à página de propriedades. Esse método implementa o método IPropertyPage::Apply.
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: Método CBasePropertyPage.Apply (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Apply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9350aa7aaa4e2bfdcb72385d26b09b9d7a9bdf33deb05e273b0663485da1a5bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823222"
---
# <a name="cbasepropertypageapply-method"></a>Método CBasePropertyPage.Apply

O `Apply` método aplica os valores de página da propriedade atual ao objeto associado à página de propriedades. Esse método implementa o **método IPropertyPage::Apply.**

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Apply();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                  | Descrição                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>            |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Falha inesperada.<br/> |



 

## <a name="remarks"></a>Comentários

Se o [**sinalizador CBasePropertyPage::m \_ bDirty**](cbasepropertypage-m-bdirty.md) for **TRUE,** esse método chamará o [**método CBasePropertyPage::OnApplyChanges.**](cbasepropertypage-onapplychanges.md) Substitua **OnApplyChanges** para aplicar as alterações ao objeto .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Cprop.h (incluir Fluxos.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




