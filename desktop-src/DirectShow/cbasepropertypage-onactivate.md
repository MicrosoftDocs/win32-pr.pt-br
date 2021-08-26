---
description: O método OnActivate é chamado quando a página de propriedades é ativada.
ms.assetid: aff843d4-cfb2-4255-a59c-0579f1cd24bd
title: Método CBasePropertyPage. OnActivate (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnActivate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f779f5bc6c33f15b5e2b1da83a72d38b91c1785564e9cace99b91469e9fdfc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052566"
---
# <a name="cbasepropertypageonactivate-method"></a>Método CBasePropertyPage. OnActivate

O `OnActivate` método é chamado quando a página de propriedades é ativada.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

A implementação da classe base retorna S \_ OK.

## <a name="remarks"></a>Comentários

O método [**CBasePropertyPage:: Activate**](cbasepropertypage-activate.md) chama o `OnActivate` método. Em sua classe derivada, substitua `OnActivate` para inicializar a caixa de diálogo.

## <a name="examples"></a>Exemplos

O exemplo a seguir inicializa um controle TrackBar. Este exemplo supõe que **m \_ pOwningFilter** seja um ponteiro para uma interface personalizada no filtro associado à página de propriedades. (Use o método [**CBasePropertyPage:: OnConnect**](cbasepropertypage-onconnect.md) para inicializar tais ponteiros.)


```C++
HRESULT CMyProp::OnActivate(void)
{
    ASSERT(m_pOwningFilter != NULL);
    m_pOwningFilter->GetSomeProperty(&m_lOldVal);
    
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0, MAKELONG(0, 100));
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 10, 0);
    SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lOldVal);
    return S_OK;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Cprop. h (incluir Fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




