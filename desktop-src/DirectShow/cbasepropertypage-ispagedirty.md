---
description: 'O método IsPageDirty indica se a página de propriedades foi alterada desde que foi ativada ou desde a chamada mais recente para IPropertyPage:: apply. Esse método implementa o método IPropertyPage:: IsPageDirty.'
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Método CBasePropertyPage. IsPageDirty (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.IsPageDirty
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c69c2e7d480f63542e146c73e56b9e692693f665
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750064"
---
# <a name="cbasepropertypageispagedirty-method"></a>Método CBasePropertyPage. IsPageDirty

O `IsPageDirty` método indica se a página de propriedades foi alterada desde que foi ativada ou desde a chamada mais recente para **IPropertyPage:: apply**. Esse método implementa o método **IPropertyPage:: IsPageDirty** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Retorna S \_ OK se [**CBasePropertyPage:: m \_ bDirty**](cbasepropertypage-m-bdirty.md) for **true** ou S \_ false, caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>CProp. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




