---
description: Substitua o método CBasePropertyPage::OnActivate para inicializar a caixa de diálogo como parte da criação de uma página de propriedades de filtro para um filtro DirectShow personalizado.
ms.assetid: 8462958d-3958-453b-8034-3cfc2fb5ae2e
title: Etapa 6. Inicializar a caixa de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbdf18e272ac548227626bc9da4f992786a4ab3
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404489"
---
# <a name="step-6-initialize-the-dialog"></a><span data-ttu-id="2db72-104">Etapa 6.</span><span class="sxs-lookup"><span data-stu-id="2db72-104">Step 6.</span></span> <span data-ttu-id="2db72-105">Inicializar a caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="2db72-105">Initialize the Dialog</span></span>

<span data-ttu-id="2db72-106">Substitua o [**método CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) para inicializar a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2db72-106">Override the [**CBasePropertyPage::OnActivate**](cbasepropertypage-onactivate.md) method to initialize the dialog.</span></span> <span data-ttu-id="2db72-107">Neste exemplo, a página de propriedades usa um controle deslizante, portanto, a primeira etapa em **OnActivate** é inicializar a biblioteca de controle comum.</span><span class="sxs-lookup"><span data-stu-id="2db72-107">In this example, the property page uses a slider control, so the first step in **OnActivate** is to initialize the common control library.</span></span> <span data-ttu-id="2db72-108">Em seguida, o método inicializa o controle deslizante usando o valor atual da propriedade de saturação do filtro:</span><span class="sxs-lookup"><span data-stu-id="2db72-108">The method then initializes the slider control using the current value of the filter's saturation property:</span></span>


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



<span data-ttu-id="2db72-109">Próximo: [Etapa 7. Manipular mensagens de janela](step-7--handle-window-messages.md)</span><span class="sxs-lookup"><span data-stu-id="2db72-109">Next: [Step 7. Handle Window Messages](step-7--handle-window-messages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="2db72-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2db72-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2db72-111">Criando uma página de propriedades de filtro</span><span class="sxs-lookup"><span data-stu-id="2db72-111">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



