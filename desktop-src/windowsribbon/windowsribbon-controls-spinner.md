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
# <a name="spinner"></a><span data-ttu-id="40dc2-103">Controle giratório</span><span class="sxs-lookup"><span data-stu-id="40dc2-103">Spinner</span></span>

<span data-ttu-id="40dc2-104">O spinner é um controle composto que consiste em um botão de incremento, um botão de decréscimo e um controle de edição, todos usados para fornecer valores decimais para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="40dc2-104">The Spinner is a composite control that consists of an increment button, a decrement button, and an edit control, all of which are used to provide decimal values to the application.</span></span>

-   [<span data-ttu-id="40dc2-105">Detalhes</span><span class="sxs-lookup"><span data-stu-id="40dc2-105">Details</span></span>](#details)
-   [<span data-ttu-id="40dc2-106">Propriedades de controle giratório</span><span class="sxs-lookup"><span data-stu-id="40dc2-106">Spinner Properties</span></span>](#spinner-properties)
-   [<span data-ttu-id="40dc2-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="40dc2-107">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="40dc2-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40dc2-108">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="40dc2-109">Detalhes</span><span class="sxs-lookup"><span data-stu-id="40dc2-109">Details</span></span>

<span data-ttu-id="40dc2-110">A captura de tela a seguir ilustra o controle giratório da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="40dc2-110">The following screen shot illustrates the Ribbon Spinner.</span></span>

![captura de tela de um controle giratório na faixa de MovieMaker do Windows Live.](images/controls/spinner.png)

## <a name="spinner-properties"></a><span data-ttu-id="40dc2-112">Propriedades de controle giratório</span><span class="sxs-lookup"><span data-stu-id="40dc2-112">Spinner Properties</span></span>

<span data-ttu-id="40dc2-113">A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle Spinner.</span><span class="sxs-lookup"><span data-stu-id="40dc2-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Spinner control.</span></span>

<span data-ttu-id="40dc2-114">Normalmente, uma propriedade Spinner é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="40dc2-114">Typically, a Spinner property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="40dc2-115">O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="40dc2-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="40dc2-116">O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura.</span><span class="sxs-lookup"><span data-stu-id="40dc2-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="40dc2-117">Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.</span><span class="sxs-lookup"><span data-stu-id="40dc2-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="40dc2-118">Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="40dc2-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="40dc2-119">A tabela a seguir lista as chaves de propriedade que estão associadas ao controle Spinner.</span><span class="sxs-lookup"><span data-stu-id="40dc2-119">The following table lists the property keys that are associated with the Spinner control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40dc2-120">Chave de propriedade</span><span class="sxs-lookup"><span data-stu-id="40dc2-120">Property Key</span></span></th>
<th><span data-ttu-id="40dc2-121">Observações</span><span class="sxs-lookup"><span data-stu-id="40dc2-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40dc2-122"><a href="windowsribbon-reference-properties-uipkey-decimalplaces.md">UI_PKEY_DecimalPlaces</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-122"><a href="windowsribbon-reference-properties-uipkey-decimalplaces.md">UI_PKEY_DecimalPlaces</a></span></span></td>
<td><span data-ttu-id="40dc2-123">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="40dc2-123">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40dc2-124"><a href="windowsribbon-reference-properties-uipkey-decimalvalue.md">UI_PKEY_DecimalValue</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-124"><a href="windowsribbon-reference-properties-uipkey-decimalvalue.md">UI_PKEY_DecimalValue</a></span></span></td>
<td><span data-ttu-id="40dc2-125">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="40dc2-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="40dc2-126">Se o comando associado ao controle for invalidado por meio de uma chamada para <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, a estrutura consultará essa propriedade quando <code>UI_INVALIDATIONS_VALUE</code> for passada como o valor de <em>flags</em>.</span><span class="sxs-lookup"><span data-stu-id="40dc2-126">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40dc2-127"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-127"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="40dc2-128">Dá suporte a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> e <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="40dc2-128">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40dc2-129"><a href="windowsribbon-reference-properties-uipkey-formatstring.md">UI_PKEY_FormatString</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-129"><a href="windowsribbon-reference-properties-uipkey-formatstring.md">UI_PKEY_FormatString</a></span></span></td>
<td><span data-ttu-id="40dc2-130">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="40dc2-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40dc2-131"><a href="windowsribbon-reference-properties-uipkey-increment.md">UI_PKEY_Increment</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-131"><a href="windowsribbon-reference-properties-uipkey-increment.md">UI_PKEY_Increment</a></span></span></td>
<td><span data-ttu-id="40dc2-132">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="40dc2-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40dc2-133"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-133"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="40dc2-134">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="40dc2-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40dc2-135"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-135"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="40dc2-136">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="40dc2-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40dc2-137"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-137"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="40dc2-138">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="40dc2-138">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40dc2-139"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-139"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="40dc2-140">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="40dc2-140">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40dc2-141"><a href="windowsribbon-reference-properties-uipkey-maxvalue.md">UI_PKEY_MaxValue</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-141"><a href="windowsribbon-reference-properties-uipkey-maxvalue.md">UI_PKEY_MaxValue</a></span></span></td>
<td><span data-ttu-id="40dc2-142">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="40dc2-142">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40dc2-143"><a href="windowsribbon-reference-properties-uipkey-minvalue.md">UI_PKEY_MinValue</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-143"><a href="windowsribbon-reference-properties-uipkey-minvalue.md">UI_PKEY_MinValue</a></span></span></td>
<td><span data-ttu-id="40dc2-144">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="40dc2-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40dc2-145"><a href="windowsribbon-reference-properties-uipkey-representativestring.md">UI_PKEY_RepresentativeString</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-145"><a href="windowsribbon-reference-properties-uipkey-representativestring.md">UI_PKEY_RepresentativeString</a></span></span></td>
<td><span data-ttu-id="40dc2-146">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="40dc2-146">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40dc2-147"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-147"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="40dc2-148">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="40dc2-148">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40dc2-149"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-149"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="40dc2-150">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="40dc2-150">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="40dc2-151"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-151"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="40dc2-152">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="40dc2-152">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="40dc2-153"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="40dc2-153"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="40dc2-154">Só pode ser atualizado por meio de invalidação.</span><span class="sxs-lookup"><span data-stu-id="40dc2-154">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="40dc2-155">A seção de código a seguir demonstra como várias propriedades do controle Spinner são atualizadas no método [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="40dc2-155">The following section of code demonstrates how various properties of the Spinner control are updated in the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) method.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="40dc2-156">Comentários</span><span class="sxs-lookup"><span data-stu-id="40dc2-156">Remarks</span></span>

<span data-ttu-id="40dc2-157">Se o valor mínimo ([UI \_ PKEY \_ MinValue](windowsribbon-reference-properties-uipkey-minvalue.md)) de um controle giratório for inicializado como 0,0, o aplicativo deverá garantir que qualquer valor subsequente fornecido pelo controle não seja igual a 0,0 (negativo zero).</span><span class="sxs-lookup"><span data-stu-id="40dc2-157">If the minimum value ([UI\_PKEY\_MinValue](windowsribbon-reference-properties-uipkey-minvalue.md)) of a Spinner is initialized to 0.0, the application should ensure that any subsequent value supplied by the control does not equal -0.0 (negative zero).</span></span> <span data-ttu-id="40dc2-158">Se o controle giratório fornecer um valor de-0,0, o aplicativo deverá redefinir esse valor para 0,0 (zero positivo) usando o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) , conforme mostrado no exemplo a seguir de um método [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) para um controle giratório.</span><span class="sxs-lookup"><span data-stu-id="40dc2-158">If the Spinner supplies a value of -0.0, the application should reset this value to 0.0 (positive zero) using the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method as shown in the following example of an [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) method for a Spinner control.</span></span>

> [!Note]  
> <span data-ttu-id="40dc2-159">Se esse teste não for executado e o valor deixado incorreto, o campo de edição do controle exibirá a cadeia de caracteres "auto".</span><span class="sxs-lookup"><span data-stu-id="40dc2-159">If this test is not performed and the value left uncorrected, the edit field of the control displays the string "Auto".</span></span>

 


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



## <a name="related-topics"></a><span data-ttu-id="40dc2-160">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40dc2-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40dc2-161">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="40dc2-161">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="40dc2-162">**Elemento de marcação Spinner**</span><span class="sxs-lookup"><span data-stu-id="40dc2-162">**Spinner markup element**</span></span>](windowsribbon-element-spinner.md)
</dt> </dl>

