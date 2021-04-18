---
description: O método OnReceiveMessage é chamado quando a caixa de diálogo recebe uma mensagem.
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: Método CBasePropertyPage. OnReceiveMessage (cProp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69d9da708d45524d15f735273d47f242104ee22f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753350"
---
# <a name="cbasepropertypageonreceivemessage-method"></a>Método CBasePropertyPage. OnReceiveMessage

O `OnReceiveMessage` método é chamado quando a caixa de diálogo recebe uma mensagem.

## <a name="syntax"></a>Sintaxe


```C++
virtual INT_PTR OnReceiveMessage(
   HWND   hwnd,
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Identificador para a janela.

</dd> <dt>

*uMsg* 
</dt> <dd>

Message.

</dd> <dt>

*wParam* 
</dt> <dd>

Primeiro parâmetro de mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Segundo parâmetro de mensagem.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor booliano. O procedimento da caixa de diálogo retorna esse valor; para obter mais informações, consulte a documentação do Platform SDK.

## <a name="remarks"></a>Comentários

A implementação da classe base chama **DefWindowProc**. Substitua esse método para tratar mensagens relacionadas aos controles da caixa de diálogo. Se o método de substituição não tratar uma mensagem específica, ele deverá chamar o método de classe base.

Se o usuário alterar qualquer propriedade por meio dos controles da caixa de diálogo, defina o sinalizador [**CBasePropertyPage:: m \_ BDirty**](cbasepropertypage-m-bdirty.md) como **true**. Em seguida, chame o método **IPropertyPageSite:: OnStatusChange** no ponteiro [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) para informar o quadro.

## <a name="examples"></a>Exemplos

O exemplo a seguir responde a um clique de botão atualizando uma variável de membro, que é assumida para ser definida na classe derivada. Este exemplo também mostra uma função auxiliar para definir o status sujo da página de propriedades.


```C++
INT_PTR CMyProp::OnReceiveMessage(HWND hwnd,
  UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_BUTTON1)
        {
            m_lNewVal = GetDlgItemInt(m_Dlg, IDC_EDIT1, 0, TRUE);
            SetDirty();
            return (INT_PTR)TRUE;
        }
        break;
    } // switch

    // Did not handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd, uMsg, wParam, lParam);
}

// Helper function to update the dirty status.
void CMyProp::SetDirty()
{
    m_bDirty = TRUE;
    if (m_pPageSite)
    {
        m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
    }
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

 

 




