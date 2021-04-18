---
description: 'O método Apply aplica os valores da página de propriedades atual ao objeto associado à página de propriedades. Esse método implementa o método IPropertyPage:: apply.'
ms.assetid: 9fe759d1-2b46-4489-b7b8-b5a35330091d
title: Método CBasePropertyPage. Apply (cProp. h)
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
ms.openlocfilehash: 21d1208979cca167b059cb720c492ac51c362c39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749631"
---
# <a name="cbasepropertypageapply-method"></a>Método CBasePropertyPage. Apply

O `Apply` método aplica os valores da página de propriedades atual ao objeto associado à página de propriedades. Esse método implementa o método **IPropertyPage:: apply** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Apply();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                  | Descrição                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>            |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Falha inesperada.<br/> |



 

## <a name="remarks"></a>Comentários

Se o sinalizador [**CBasePropertyPage:: m \_ BDirty**](cbasepropertypage-m-bdirty.md) for **true**, esse método chamará o método [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) . Substitua **OnApplyChanges** para aplicar as alterações ao objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>CProp. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




