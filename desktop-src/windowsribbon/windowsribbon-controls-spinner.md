---
title: Controle giratório
description: O spinner é um controle composto que consiste em um botão de incremento, um botão de decréscimo e um controle de edição, todos usados para fornecer valores decimais para o aplicativo.
ms.assetid: 63689ed3-7326-4f7a-b700-d89e9b501ef1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0875fb31d0dac73c88f3bd502746c473dc1c2b1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "105781533"
---
# <a name="spinner"></a>Controle giratório

O spinner é um controle composto que consiste em um botão de incremento, um botão de decréscimo e um controle de edição, todos usados para fornecer valores decimais para o aplicativo.

-   [Detalhes](#details)
-   [Propriedades de controle giratório](#spinner-properties)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="details"></a>Detalhes

A captura de tela a seguir ilustra o controle giratório da faixa de opções.

![captura de tela de um controle giratório na faixa de MovieMaker do Windows Live.](images/controls/spinner.png)

## <a name="spinner-properties"></a>Propriedades de controle giratório

A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle Spinner.

Normalmente, uma propriedade Spinner é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

A tabela a seguir lista as chaves de propriedade que estão associadas ao controle Spinner.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Chave de propriedade</th>
<th>Observações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-decimalplaces.md">UI_PKEY_DecimalPlaces</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-decimalvalue.md">UI_PKEY_DecimalValue</a></td>
<td>Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.
<blockquote>
[!Note]<br />
Se o comando associado ao controle for invalidado por meio de uma chamada para <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, a estrutura consultará essa propriedade quando <code>UI_INVALIDATIONS_VALUE</code> for passada como o valor de <em>flags</em>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></td>
<td>Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-formatstring.md">UI_PKEY_FormatString</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-increment.md">UI_PKEY_Increment</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-maxvalue.md">UI_PKEY_MaxValue</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-minvalue.md">UI_PKEY_MinValue</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-representativestring.md">UI_PKEY_RepresentativeString</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
<tr class="even">
<td><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></td>
<td>Só pode ser atualizado por meio de invalidação.</td>
</tr>
</tbody>
</table>



 

A seção de código a seguir demonstra como várias propriedades do controle Spinner são atualizadas no método [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .


```C++
//
//  FUNCTION:    UpdateProperty()
//
//  PURPOSE:    Called by the Ribbon framework when a command property needs 
//                to be updated.
//
//  COMMENTS:    This function is used to provide new command property values for 
//                the spinner when requested by the Ribbon framework.  
//    
STDMETHODIMP CCommandHandler::UpdateProperty(
    UINT nCmdID,
    REFPROPERTYKEY key,
    const PROPVARIANT* ppropvarCurrentValue,
    PROPVARIANT* ppropvarNewValue)
{
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;

    if (nCmdID == IDR_CMD_SPINNER_RESIZE)
    {
        // Set the minimum value
        if (IsEqualPropertyKey(key, UI_PKEY_MinValue))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(-10.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the maximum value
        else if (IsEqualPropertyKey(key, UI_PKEY_MaxValue))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(10.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the increment
        else if (IsEqualPropertyKey(key, UI_PKEY_Increment))
        {
            ZeroMemory(ppropvarNewValue, sizeof(*ppropvarNewValue));
            ppropvarNewValue->vt = VT_DECIMAL;
            VarDecFromR8(2.0, &ppropvarNewValue->decVal);
            hr = S_OK;
        }

        // Set the number of decimal places
        else if (IsEqualPropertyKey(key, UI_PKEY_DecimalPlaces))
        {
            hr = InitPropVariantFromUInt32(1, ppropvarNewValue);
            hr = S_OK;
        }

        // Set the format string
        else if (IsEqualPropertyKey(key, UI_PKEY_FormatString))
        {
            hr = InitPropVariantFromString(L"px", ppropvarNewValue);
            hr = S_OK;
        }

        // Set the representative string
        else if (IsEqualPropertyKey(key, UI_PKEY_RepresentativeString))
        {
            hr = InitPropVariantFromString(L"AAAAAAA", ppropvarNewValue);
            hr = S_OK;
        }
    }
    return hr;
}
```



## <a name="remarks"></a>Comentários

Se o valor mínimo ([UI \_ PKEY \_ MinValue](windowsribbon-reference-properties-uipkey-minvalue.md)) de um controle giratório for inicializado como 0,0, o aplicativo deverá garantir que qualquer valor subsequente fornecido pelo controle não seja igual a 0,0 (negativo zero). Se o controle giratório fornecer um valor de-0,0, o aplicativo deverá redefinir esse valor para 0,0 (zero positivo) usando o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) , conforme mostrado no exemplo a seguir de um método [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) para um controle giratório.

> [!Note]  
> Se esse teste não for executado e o valor deixado incorreto, o campo de edição do controle exibirá a cadeia de caracteres "auto".

 


```C++
//
//  FUNCTION:    Execute()
//
//  PURPOSE:    Called by the Ribbon framework when a command is executed by the user.  
//                For this sample, when an increment or decrement button is pressed or
//                a new value is entered in the Spinner edit field.
//
STDMETHODIMP CCommandHandler::Execute(
      UINT nCmdID,
      UI_EXECUTIONVERB verb,
      const PROPERTYKEY* key,
      const PROPVARIANT* ppropvarValue,
      IUISimplePropertySet* pCommandExecutionProperties)
{
    UNREFERENCED_PARAMETER(pCommandExecutionProperties);

    HRESULT hr = E_NOTIMPL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        RenderParam param;
        g_renderer.GetRenderParam(&param);

        if (nCmdID == IDR_CMD_SPINNER_RESIZE)
        {
            // Spinner value is negative.
            if (!(ppropvarValue->decVal.sign == 0))
            {
                // Check if the value supplied by the Spinner is -0
                // and correct the value if necessary.
                // If this value is left uncorrected, the edit field 
                // of the control will display the string "Auto" when 
                // UI_PKEY_MinValue is set to 0.
                if (ppropvarValue->decVal.Lo64 == 0)
                {
                    // Initialize a new PROPVARIANT structure.
                    PROPVARIANT m_varNewVal;
                    PropVariantInit(&m_varNewVal);

                    // The replacement DECIMAL value.
                    DECIMAL m_dVal;
                    hr = VarDecFromI4(0, &m_dVal);
                    if (FAILED(hr))
                    {
                        return hr;
                    }
                    
                    // Initialize the new DECIMAL value.
                    UIInitPropertyFromDecimal(UI_PKEY_DecimalValue, m_dVal, &m_varNewVal);

                    // Set the UI_PKEY_DecimalValue to the new DECIMAL value.
                    hr = g_pFramework->SetUICommandProperty(nCmdID, UI_PKEY_DecimalValue, m_varNewVal);
                    if (FAILED(hr))
                    {
                        return hr;
                    }
                }
                // Decrease size of shape in document space.
                param.iShapeSizeIncrement = -ppropvarValue->intVal;
            }
            // Spinner value is positive.
            else
            {
                // Increase size of shape in document space.
                param.iShapeSizeIncrement = ppropvarValue->intVal;
            }
        }
        g_renderer.UpdateRenderParam(param);
    }

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Biblioteca de controle do Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcação Spinner**](windowsribbon-element-spinner.md)
</dt> </dl>

