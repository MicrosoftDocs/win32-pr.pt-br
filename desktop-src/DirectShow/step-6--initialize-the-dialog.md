---
description: Etapa 6.
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: Etapa 6. Inicializar a caixa de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 282eb03db38c543678fb2c4ef1155e1150b419bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760874"
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

 

 



