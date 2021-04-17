---
description: O método OnActivate é chamado quando a janela da caixa de diálogo é destruída.
ms.assetid: 47320e61-324f-4f64-abe1-38fe70e82787
title: Método CBasePropertyPage. Deactivate (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDeactivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27191e4895c911d3d13a795306eee2b0ad6989ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811753"
---
# <a name="cbasepropertypageondeactivate-method"></a>Método CBasePropertyPage. Deactivate

O `OnDeactivate` método é chamado quando a janela da caixa de diálogo é destruída.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT OnDeactivate();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

A implementação da classe base retorna S \_ OK.

## <a name="remarks"></a>Comentários

O método [**CBasePropertyPage::D eactivate**](cbasepropertypage-deactivate.md) chama o `OnDeactivate` método. Substitua `OnDeactivate` para liberar os recursos que a classe derivada obteve no método [**CBasePropertyPage:: onactiva**](cbasepropertypage-onactivate.md) ou para executar outras tarefas, conforme necessário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>CProp. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




