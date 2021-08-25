---
description: 'substitua o método CBasePropertyPage:: onactivate para inicializar a caixa de diálogo como parte da criação de uma página de propriedades de filtro para um filtro de DirectShow personalizado.'
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: Etapa 6. Inicializar a caixa de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2ac2dbc4e8ed59317db3db46079b087e4afcf0fa8dce315aa2a0cbd45d502a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102306"
---
# <a name="step-6-initialize-the-dialog"></a>Etapa 6. Inicializar a caixa de diálogo

Substitua o método [**CBasePropertyPage:: OnActivate**](cbasepropertypage-onactivate.md) para inicializar a caixa de diálogo. Neste exemplo, a página de propriedades usa um controle deslizante, portanto, a primeira etapa em **OnActivate** é inicializar a biblioteca de controle comum. Em seguida, o método inicializa o controle deslizante usando o valor atual da propriedade de saturação do filtro:


```C++
HRESULT CGrayProp::OnActivate(void)
{
    INITCOMMONCONTROLSEX icc;
    icc.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icc.dwICC = ICC_BAR_CLASSES;
    if (InitCommonControlsEx(&icc) == FALSE)
    {
        return E_FAIL;
    }

    ASSERT(m_pGray != NULL);
    HRESULT hr = m_pGray->GetSaturation(&m_lVal);
    if (SUCCEEDED(hr))
    {
        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETRANGE, 0,
            MAKELONG(SATURATION_MIN, SATURATION_MAX));

        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETTICFREQ, 
            (SATURATION_MAX - SATURATION_MIN) / 10, 0);

        SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1, m_lVal);
    }
    return hr;
}
```



Em seguida: [etapa 7. Processar mensagens de janela](step-7--handle-window-messages.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma página de propriedades de filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



