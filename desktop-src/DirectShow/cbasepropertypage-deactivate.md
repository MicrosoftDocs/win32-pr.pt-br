---
description: O método Deactivate destrói a janela da caixa de diálogo. Esse método implementa o método IPropertyPage::D eactivate.
ms.assetid: f2d2f15f-15f6-4902-bafc-f58a684ff193
title: Método CBasePropertyPage. Deactivate (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.Deactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 63a843502fc735cc41ff3656e83ef3d6cb839a19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748221"
---
# <a name="cbasepropertypagedeactivate-method"></a>Método CBasePropertyPage. Deactivate

O `Deactivate` método destrói a janela da caixa de diálogo. Esse método implementa o método **IPropertyPage::D eactivate** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Deactivate();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes.



| Código de retorno                                                                                  | Descrição                    |
|----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Êxito.<br/>            |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | Falha inesperada.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>CProp. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> <dt>

[**CBasePropertyPage:: OnActivate**](cbasepropertypage-ondeactivate.md)
</dt> </dl>

 

 




