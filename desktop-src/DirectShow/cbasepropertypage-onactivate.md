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
ms.openlocfilehash: 5093cb2ac71e8010bc689e4517b3d8bb758c8436
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749843"
---
# <a name="cbasepropertypageonactivate-method"></a>Método CBasePropertyPage. OnActivate

O `OnActivate` método é chamado quando a página de propriedades é ativada.

## <a name="syntax"></a>Sintaxe


```C++
virtual HRESULT OnActivate();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

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
| parâmetro<br/>  | <dl> <dt>CProp. h (incluir fluxos. h)</dt> </dl>                                                                                     |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




