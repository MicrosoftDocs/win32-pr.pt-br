---
description: O método OnDisconnect é chamado quando a página de propriedades deve liberar o objeto associado.
ms.assetid: 55bab0ca-587e-405c-9025-f391cf08a620
title: Método CBasePropertyPage. OnDisconnect (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnDisconnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: abd251d20ca82ad0374a613d9ee73f0eaee21d31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811752"
---
# <a name="cbasepropertypageondisconnect-method"></a>Método CBasePropertyPage. OnDisconnect

O `OnDisconnect` método é chamado quando a página de propriedades deve liberar o objeto associado.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT OnDisconnect();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

A implementação da classe base retorna S \_ OK.

## <a name="remarks"></a>Comentários

O método [**CBasePropertyPage:: SetObjects**](cbasepropertypage-setobjects.md) chama o `OnDisconnect` método. Substitua `OnDisconnect` para liberar quaisquer ponteiros que foram obtidos no método [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) .

## <a name="examples"></a>Exemplos


```C++
HRESULT CMyProp::OnDisconnect(void)
{
    if (m_pOwningFilter)
    {
        m_pOwningFilter->Release();
        m_pOwningFilter = NULL;
    }
    return S_OK;
}
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

 

 




