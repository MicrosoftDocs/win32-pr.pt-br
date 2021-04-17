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
# <a name="step-7-handle-window-messages"></a><span data-ttu-id="86e6d-104">Etapa 7.</span><span class="sxs-lookup"><span data-stu-id="86e6d-104">Step 7.</span></span> <span data-ttu-id="86e6d-105">Processar mensagens de janela</span><span class="sxs-lookup"><span data-stu-id="86e6d-105">Handle Window Messages</span></span>

<span data-ttu-id="86e6d-106">Substitua o método [**CBasePropertyPage:: OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) para atualizar os controles da caixa de diálogo em resposta à entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="86e6d-106">Override the [**CBasePropertyPage::OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) method to update the dialog controls in response to user input.</span></span> <span data-ttu-id="86e6d-107">Se você não tratar uma mensagem específica, chame o método **OnReceiveMessage** na classe pai.</span><span class="sxs-lookup"><span data-stu-id="86e6d-107">If you don't handle a particular message, call the **OnReceiveMessage** method on the parent class.</span></span> <span data-ttu-id="86e6d-108">Sempre que o usuário alterar uma propriedade, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="86e6d-108">Whenever the user changes a property, do the following:</span></span>

-   <span data-ttu-id="86e6d-109">Defina a variável **m \_ bDirty** da página de propriedades como **true**.</span><span class="sxs-lookup"><span data-stu-id="86e6d-109">Set the **m\_bDirty** variable of the property page to **TRUE**.</span></span>
-   <span data-ttu-id="86e6d-110">Chame o método **IPropertyPageSite:: OnStatusChange** do quadro de propriedade com o \_ sinalizador sujo PROPPAGESTATUS.</span><span class="sxs-lookup"><span data-stu-id="86e6d-110">Call the **IPropertyPageSite::OnStatusChange** method of the property frame with the PROPPAGESTATUS\_DIRTY flag.</span></span> <span data-ttu-id="86e6d-111">Esse sinalizador informa ao quadro de propriedade que ele deve habilitar o botão **aplicar** .</span><span class="sxs-lookup"><span data-stu-id="86e6d-111">This flag informs the property frame that it should enable the **Apply** button.</span></span> <span data-ttu-id="86e6d-112">O membro [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) contém um ponteiro para a interface **IPropertyPageSite** .</span><span class="sxs-lookup"><span data-stu-id="86e6d-112">The [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) member holds a pointer to the **IPropertyPageSite** interface.</span></span>

<span data-ttu-id="86e6d-113">Para simplificar essa etapa, você pode adicionar a seguinte função auxiliar à sua página de propriedades:</span><span class="sxs-lookup"><span data-stu-id="86e6d-113">To simplify this step, you can add the following helper function to your property page:</span></span>


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



<span data-ttu-id="86e6d-114">Chame esse método particular dentro de **OnReceiveMessage** sempre que uma ação do usuário alterar uma propriedade, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="86e6d-114">Call this private method inside **OnReceiveMessage** whenever a user action changes a property, as shown in the following example:</span></span>


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



<span data-ttu-id="86e6d-115">A página de propriedades neste exemplo tem dois controles, uma barra deslizante e um botão **reverter para padrão** .</span><span class="sxs-lookup"><span data-stu-id="86e6d-115">The property page in this example has two controls, a slider bar and a **Revert to Default** button.</span></span> <span data-ttu-id="86e6d-116">Se o usuário rolar a barra deslizante, a página de propriedades definirá o valor de saturação no filtro.</span><span class="sxs-lookup"><span data-stu-id="86e6d-116">If the user scrolls the slider bar, the property page sets the saturation value on the filter.</span></span> <span data-ttu-id="86e6d-117">Se o usuário clicar no botão, a página de propriedades restaurará o valor de saturação padrão do filtro.</span><span class="sxs-lookup"><span data-stu-id="86e6d-117">If the user clicks the button, the property page restores the filter's default saturation value.</span></span> <span data-ttu-id="86e6d-118">Em cada caso, m \_ lNewVal mantém o valor atual e m \_ lVal contém o valor original.</span><span class="sxs-lookup"><span data-stu-id="86e6d-118">In each case, m\_lNewVal holds the current value and m\_lVal holds the original value.</span></span> <span data-ttu-id="86e6d-119">O valor de m \_ lVal não é atualizado até que o usuário confirme a alteração, o que acontece quando o usuário clica no botão **OK** ou **aplicar** no quadro de propriedade.</span><span class="sxs-lookup"><span data-stu-id="86e6d-119">The value of m\_lVal is not updated until the user commits the change, which happens when the user clicks the **OK** or **Apply** button on the property frame.</span></span>

<span data-ttu-id="86e6d-120">Em seguida: [etapa 8. Aplicar alterações de propriedade](step-8--apply-property-changes.md).</span><span class="sxs-lookup"><span data-stu-id="86e6d-120">Next: [Step 8. Apply Property Changes](step-8--apply-property-changes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="86e6d-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86e6d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86e6d-122">Criando uma página de propriedades de filtro</span><span class="sxs-lookup"><span data-stu-id="86e6d-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



