---
description: O método OnConnect fornece um ponteiro IUnknown para o objeto associado à página de propriedades.
ms.assetid: 74cae8e1-5347-4e3d-ba5f-6a4efec2ddae
title: Método CBasePropertyPage. OnConnect (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 38f83a7c491f1591cece8d5d85eb4525a1059d2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755607"
---
# <a name="cbasepropertypageonconnect-method"></a>Método CBasePropertyPage. OnConnect

O `OnConnect` método fornece um ponteiro **IUnknown** para o objeto associado à página de propriedades.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT OnConnect(
   IUnknown *pUnknown
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pUnknown* 
</dt> <dd>

Ponteiro para a interface **IUnknown** do objeto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

A implementação da classe base retorna S \_ OK.

## <a name="remarks"></a>Comentários

O método [**CBasePropertyPage:: SetObjects**](cbasepropertypage-setobjects.md) chama o `OnConnect` método. Substitua esse método para armazenar um ponteiro para o objeto especificado por *pUnknown*. Você pode armazenar o próprio ponteiro *pUnknown* ou consultar o ponteiro para outras interfaces. Se você armazenar o ponteiro *pUnknown* , chame **AddRef** antes de `OnConnect` retornar.

No método [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md) , use o ponteiro armazenado (ou ponteiros) para recuperar os valores iniciais das propriedades da caixa de diálogo. No método [**CBasePropertyPage:: OnApplyChanges**](cbasepropertypage-onapplychanges.md) , aplique as alterações de volta ao objeto. Libere todos os ponteiros no método [**CBasePropertyPage:: OnDisconnect**](cbasepropertypage-ondisconnect.md) .

## <a name="examples"></a>Exemplos


```C++
HRESULT CMyProp::OnConnect(IUnknown *pUnk)
{
    ASSERT(m_pOwningFilter == NULL);
    HRESULT hr;
    // Query pUnk for the filter's custom interface.
    hr = pUnk->QueryInterface(IID_ISomeCustomInterface,
             reinterpret_cast<void**>(&m_pOwningFilter));
    return hr;
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

 

 




