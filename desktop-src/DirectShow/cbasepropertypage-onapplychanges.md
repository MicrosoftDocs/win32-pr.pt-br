---
description: O método OnApplyChanges é chamado quando o usuário aplica alterações à página de propriedades.
ms.assetid: 15a55644-b7bf-4c72-8e26-18fc4fb714b9
title: Método CBasePropertyPage.OnApplyChanges (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnApplyChanges
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f822bed433af6e3fab0250e06a04911ee10187039036211974b046b32df6b7b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823102"
---
# <a name="cbasepropertypageonapplychanges-method"></a>Método CBasePropertyPage.OnApplyChanges

O `OnApplyChanges` método é chamado quando o usuário aplica alterações à página de propriedades.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT OnApplyChanges();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

A implementação da classe base retorna S \_ OK.

## <a name="remarks"></a>Comentários

O [**método CBasePropertyPage::Apply**](cbasepropertypage-apply.md) chamará se o sinalizador `OnApplyChanges` [**CBasePropertyPage::m \_ bDirty**](cbasepropertypage-m-bdirty.md) for **TRUE.** Substitua `OnApplyChanges` para processar as alterações e **redefinir m \_ bDirty** para **FALSE.**

## <a name="examples"></a>Exemplos


```C++
HRESULT CMyProp::OnApplyChanges(void)
{
    ASSERT(m_pOwningFilter != NULL);
    return m_pOwningFilter->SetSomeProperty(&m_lNewVal);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Cprop.h (incluir Fluxos.h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




