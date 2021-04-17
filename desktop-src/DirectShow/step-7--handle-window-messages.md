---
description: Etapa 7.
ms.assetid: 12bb1288-e764-4bc1-bea5-196e17cf3557
title: Etapa 7. Processar mensagens de janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd1c44dd65a4f9f430b4223f0a5a0e4763af981
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812812"
---
# <a name="step-7-handle-window-messages"></a>Etapa 7. Processar mensagens de janela

Substitua o método [**CBasePropertyPage:: OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) para atualizar os controles da caixa de diálogo em resposta à entrada do usuário. Se você não tratar uma mensagem específica, chame o método **OnReceiveMessage** na classe pai. Sempre que o usuário alterar uma propriedade, faça o seguinte:

-   Defina a variável **m \_ bDirty** da página de propriedades como **true**.
-   Chame o método **IPropertyPageSite:: OnStatusChange** do quadro de propriedade com o \_ sinalizador sujo PROPPAGESTATUS. Esse sinalizador informa ao quadro de propriedade que ele deve habilitar o botão **aplicar** . O membro [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) contém um ponteiro para a interface **IPropertyPageSite** .

Para simplificar essa etapa, você pode adicionar a seguinte função auxiliar à sua página de propriedades:


```C++
private:
    void SetDirty()
    {
        m_bDirty = TRUE;
        if (m_pPageSite)
        {
            m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
        }
    }
```



Chame esse método particular dentro de **OnReceiveMessage** sempre que uma ação do usuário alterar uma propriedade, conforme mostrado no exemplo a seguir:


```C++
BOOL CGrayProp::OnReceiveMessage(HWND hwnd,
    UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_DEFAULT)
        {
            // User clicked the 'Revert to Default' button.
            m_lNewVal = SATURATION_DEFAULT;
            m_pGray->SetSaturation(m_lNewVal);

            // Update the slider control.
            SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1,
                m_lNewVal);
            SetDirty();
            return (LRESULT) 1;
        }
        break;

    case WM_HSCROLL:
        {
            // User moved the slider.
            switch(LOWORD(wParam))
            {
            case TB_PAGEDOWN:
            case SB_THUMBTRACK:
            case TB_PAGEUP:
                m_lNewVal = SendDlgItemMessage(m_Dlg, IDC_SLIDER1,
                    TBM_GETPOS, 0, 0);
                m_pGray->SetSaturation(m_lNewVal);
                SetDirty();
            }
            return (LRESULT) 1;
        }
    } // Switch.
    
    // Let the parent class handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd,uMsg,wParam,lParam);
} 
```



A página de propriedades neste exemplo tem dois controles, uma barra deslizante e um botão **reverter para padrão** . Se o usuário rolar a barra deslizante, a página de propriedades definirá o valor de saturação no filtro. Se o usuário clicar no botão, a página de propriedades restaurará o valor de saturação padrão do filtro. Em cada caso, m \_ lNewVal mantém o valor atual e m \_ lVal contém o valor original. O valor de m \_ lVal não é atualizado até que o usuário confirme a alteração, o que acontece quando o usuário clica no botão **OK** ou **aplicar** no quadro de propriedade.

Em seguida: [etapa 8. Aplicar alterações de propriedade](step-8--apply-property-changes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma página de propriedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



