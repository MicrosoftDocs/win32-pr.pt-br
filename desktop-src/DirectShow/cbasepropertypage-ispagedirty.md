---
description: O método IsPageDirty indica se a página de propriedades foi alterada desde que foi ativada ou desde a chamada mais recente para IPropertyPage::Apply. Esse método implementa o método IPropertyPage::IsPageDirty.
ms.assetid: 95eeec26-7dbb-4add-a827-6505b40afe48
title: Método CBasePropertyPage.IsPageDirty (Cprop.h)
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
ms.openlocfilehash: 72b818ce117990f6f91ee58b8605e9d8cff9734fa9114d7f6114ed11d53a9521
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108496"
---
# <a name="cbasepropertypageispagedirty-method"></a>Método CBasePropertyPage.IsPageDirty

O método indica se a página de propriedades foi alterada desde que foi ativada ou desde a chamada mais `IsPageDirty` recente para **IPropertyPage::Apply.** Esse método implementa o **método IPropertyPage::IsPageDirty.**

## <a name="syntax"></a>Sintaxe


```C++
HRESULT IsPageDirty();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retornará S \_ OK [**se CBasePropertyPage::m \_ bDirty**](cbasepropertypage-m-bdirty.md) for **TRUE** ou S FALSE \_ caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Cprop.h (incluir Fluxos.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




