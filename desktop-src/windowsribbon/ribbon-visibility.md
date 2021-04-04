---
title: Exibindo a faixa de faixas
description: A estrutura da faixa de faixas do Windows expõe um conjunto de propriedades que permitem que um aplicativo especifique como a interface do usuário da faixa de Ribbon é exibida em tempo de execução.
ms.assetid: c6716183-ef32-4fb2-812a-2d8f27448db5
keywords:
- Faixa de-se do Windows, personalizando cores
- Faixa de faixas, personalizando cores
- Personalizando as cores da faixa de das janelas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 090c77c5b47afd673bc7132a87e3de336683d876
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007840"
---
# <a name="displaying-the-ribbon"></a><span data-ttu-id="b74bd-106">Exibindo a faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="b74bd-106">Displaying the Ribbon</span></span>

<span data-ttu-id="b74bd-107">A estrutura da faixa de faixas do Windows expõe um conjunto de propriedades que permitem que um aplicativo especifique como a interface do usuário da faixa de Ribbon é exibida em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="b74bd-107">The Windows Ribbon framework exposes a set of properties that allow an application to specify how the Ribbon UI is displayed at run time.</span></span>

-   [<span data-ttu-id="b74bd-108">Introdução</span><span class="sxs-lookup"><span data-stu-id="b74bd-108">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="b74bd-109">Minimizar a faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="b74bd-109">Minimize the Ribbon</span></span>](#minimize-the-ribbon)
-   [<span data-ttu-id="b74bd-110">Ocultar a faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="b74bd-110">Hide the Ribbon</span></span>](#hide-the-ribbon)
-   [<span data-ttu-id="b74bd-111">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b74bd-111">Example</span></span>](#example)
-   [<span data-ttu-id="b74bd-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b74bd-112">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="b74bd-113">Introdução</span><span class="sxs-lookup"><span data-stu-id="b74bd-113">Introduction</span></span>

<span data-ttu-id="b74bd-114">Para maximizar a área disponível para o espaço do documento (ou a porta de exibição) de um aplicativo da estrutura da faixa de faixas, um aplicativo pode especificar se a interface do usuário da faixa de visão está visível ou oculta e, quando visível, se a faixa de ' está em um estado expandido ou recolhido.</span><span class="sxs-lookup"><span data-stu-id="b74bd-114">To maximize the area available for the document space (or view port) of a Ribbon framework application, an application can specify whether the ribbon UI is visible or hidden and, when visible, whether the ribbon is in an expanded or collapsed state.</span></span>

<span data-ttu-id="b74bd-115">As [chaves de propriedade da estrutura](windowsribbon-reference-properties-framework.md) listadas na tabela a seguir são usadas para definir explicitamente as características de exibição da interface do usuário da faixa de opções em um aplicativo da estrutura da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="b74bd-115">The [framework property keys](windowsribbon-reference-properties-framework.md) listed in the following table are used to explicitly set the display characteristics of the ribbon UI in a Ribbon framework application.</span></span> <span data-ttu-id="b74bd-116">Essas propriedades não têm nenhum efeito na exibição do controle [Popup de contexto](windowsribbon-controls-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="b74bd-116">These properties have no effect on the display of the [Context Popup](windowsribbon-controls-contextpopup.md) control.</span></span>



| <span data-ttu-id="b74bd-117">Estado de exibição</span><span class="sxs-lookup"><span data-stu-id="b74bd-117">Display State</span></span>         | <span data-ttu-id="b74bd-118">Chave da propriedade da faixa de,</span><span class="sxs-lookup"><span data-stu-id="b74bd-118">Ribbon Property Key</span></span>                                                            |
|-----------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="b74bd-119">Expandido ou recolhido</span><span class="sxs-lookup"><span data-stu-id="b74bd-119">Expanded or collapsed</span></span> | [<span data-ttu-id="b74bd-120">PKEY da interface do usuário \_ \_ minimizada</span><span class="sxs-lookup"><span data-stu-id="b74bd-120">UI\_PKEY\_Minimized</span></span>](windowsribbon-reference-properties-uipkey-minimized.md) |
| <span data-ttu-id="b74bd-121">Visível ou oculto</span><span class="sxs-lookup"><span data-stu-id="b74bd-121">Visible or hidden</span></span>     | [<span data-ttu-id="b74bd-122">PKEY da interface do usuário \_ \_ visível</span><span class="sxs-lookup"><span data-stu-id="b74bd-122">UI\_PKEY\_Viewable</span></span>](windowsribbon-reference-properties-uipkey-viewable.md)   |



 

## <a name="minimize-the-ribbon"></a><span data-ttu-id="b74bd-123">Minimizar a faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="b74bd-123">Minimize the Ribbon</span></span>

<span data-ttu-id="b74bd-124">Um aplicativo da estrutura da faixa de opção pode definir dinamicamente o estado minimizado da barra de comandos da faixa de opção definindo o valor da chave de propriedade [ \_ PKEY \_ minimizada da interface do usuário](windowsribbon-reference-properties-uipkey-minimized.md) como **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="b74bd-124">A Ribbon framework application can dynamically set the minimized state of the ribbon command bar by setting the value of the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property key to **true** or **false**.</span></span>



| <span data-ttu-id="b74bd-125">Estado de exibição</span><span class="sxs-lookup"><span data-stu-id="b74bd-125">Display State</span></span> | <span data-ttu-id="b74bd-126">Valor da chave da propriedade</span><span class="sxs-lookup"><span data-stu-id="b74bd-126">Property Key Value</span></span> |
|---------------|--------------------|
| <span data-ttu-id="b74bd-127">Expanded</span><span class="sxs-lookup"><span data-stu-id="b74bd-127">Expanded</span></span>      | <span data-ttu-id="b74bd-128">**false**</span><span class="sxs-lookup"><span data-stu-id="b74bd-128">**false**</span></span>          |
| <span data-ttu-id="b74bd-129">Recolhido</span><span class="sxs-lookup"><span data-stu-id="b74bd-129">Collapsed</span></span>     | <span data-ttu-id="b74bd-130">**true**</span><span class="sxs-lookup"><span data-stu-id="b74bd-130">**true**</span></span>           |



 

<span data-ttu-id="b74bd-131">Quando a interface do usuário da faixa de visão está em um estado minimizado, a linha da guia da faixa de faixas permanece visível e totalmente funcional.</span><span class="sxs-lookup"><span data-stu-id="b74bd-131">When the ribbon UI is in a minimized state, the ribbon Tab row remains visible and fully functional.</span></span>

<span data-ttu-id="b74bd-132">A captura de tela a seguir mostra a faixa de opções no estado minimizado.</span><span class="sxs-lookup"><span data-stu-id="b74bd-132">The following screen shot shows the ribbon in the minimized state.</span></span>

![captura de tela mostrando a interface do usuário da faixa de faixas minimizada.](images/overviews/ribbon-minimized.png)

> [!Note]  
> <span data-ttu-id="b74bd-134">A estrutura da faixa de opção expõe essa funcionalidade ao usuário final por meio da seleção "minimizar a faixa de opção" do menu de contexto da faixa de modo.</span><span class="sxs-lookup"><span data-stu-id="b74bd-134">The Ribbon framework exposes this functionality to the end user through the "Minimize the Ribbon" selection of the ribbon context menu.</span></span>

 

## <a name="hide-the-ribbon"></a><span data-ttu-id="b74bd-135">Ocultar a faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="b74bd-135">Hide the Ribbon</span></span>

<span data-ttu-id="b74bd-136">Um aplicativo da estrutura da faixa de opção pode definir dinamicamente o estado visível da barra de comandos da faixa de opção, definindo o valor da chave de propriedade [ \_ PKEY \_ viewable da interface do usuário](windowsribbon-reference-properties-uipkey-viewable.md) como **true** ou **false**.</span><span class="sxs-lookup"><span data-stu-id="b74bd-136">A Ribbon framework application can dynamically set the viewable state of the ribbon command bar by setting the value of the [UI\_PKEY\_Viewable](windowsribbon-reference-properties-uipkey-viewable.md) property key to **true** or **false**.</span></span>



| <span data-ttu-id="b74bd-137">Estado de exibição</span><span class="sxs-lookup"><span data-stu-id="b74bd-137">Display State</span></span> | <span data-ttu-id="b74bd-138">Valor da chave da propriedade</span><span class="sxs-lookup"><span data-stu-id="b74bd-138">Property Key Value</span></span> |
|---------------|--------------------|
| <span data-ttu-id="b74bd-139">Visible</span><span class="sxs-lookup"><span data-stu-id="b74bd-139">Visible</span></span>       | <span data-ttu-id="b74bd-140">**false**</span><span class="sxs-lookup"><span data-stu-id="b74bd-140">**false**</span></span>          |
| <span data-ttu-id="b74bd-141">Hidden</span><span class="sxs-lookup"><span data-stu-id="b74bd-141">Hidden</span></span>        | <span data-ttu-id="b74bd-142">**true**</span><span class="sxs-lookup"><span data-stu-id="b74bd-142">**true**</span></span>           |



 

<span data-ttu-id="b74bd-143">Ao contrário da propriedade [ \_ PKEY \_ minimizada da interface do usuário](windowsribbon-reference-properties-uipkey-minimized.md) , definir a [interface do usuário \_ PKEY \_ visível](windowsribbon-reference-properties-uipkey-viewable.md) como **false** renderiza a interface do usuário da faixa de opção invisível e completamente inutilizável para um usuário final.</span><span class="sxs-lookup"><span data-stu-id="b74bd-143">In contrast to the [UI\_PKEY\_Minimized](windowsribbon-reference-properties-uipkey-minimized.md) property, setting [UI\_PKEY\_Viewable](windowsribbon-reference-properties-uipkey-viewable.md) to **false** renders the ribbon UI invisible and completely unusable to an end user.</span></span>

<span data-ttu-id="b74bd-144">A captura de tela a seguir mostra a faixa de opções no estado oculto.</span><span class="sxs-lookup"><span data-stu-id="b74bd-144">The following screen shot shows the ribbon in the hidden state.</span></span>

![captura de tela mostrando a interface do usuário da faixa de faixas oculta.](images/overviews/ribbon-viewable.png)

## <a name="example"></a><span data-ttu-id="b74bd-146">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b74bd-146">Example</span></span>

<span data-ttu-id="b74bd-147">O exemplo a seguir demonstra como definir o estado da interface do usuário da faixa de opções em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="b74bd-147">The following example demonstrates how to set the state of the ribbon UI at run time.</span></span>

<span data-ttu-id="b74bd-148">Nesse caso, a função [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) é usada para expandir ou recolher a interface do usuário da faixa de opção com base no estado de alternância de um [botão de alternância](windowsribbon-controls-togglebutton.md).</span><span class="sxs-lookup"><span data-stu-id="b74bd-148">In this case, the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) function is used to expand or collapse the ribbon UI based on the toggle state of a [Toggle Button](windowsribbon-controls-togglebutton.md).</span></span>


```C++
//
//  FUNCTION: Execute()
//
//  PURPOSE: Called by the Ribbon framework when a Command is executed 
//           by the user. 
//           This example demonstrates a handler for a Toggle Button
//           that sets the minimized state of the ribbon UI.
//
//  NOTES: g_pFramework is a global pointer to an IUIFramework object 
//         that is assigned when the Ribbon framework is initialized.
//
//         g_pRibbon is a global pointer to the IUIRibbon object
//         that is assigned when the Ribbon framework is initialized.
//
STDMETHODIMP CCommandHandler::Execute(
    UINT nCmdID,
    UI_EXECUTIONVERB verb,
    __in_opt const PROPERTYKEY* key,
    __in_opt const PROPVARIANT* ppropvarValue,
    __in_opt IUISimplePropertySet* pCommandExecutionProperties)
{
    HRESULT hr = E_FAIL;

    if (verb == UI_EXECUTIONVERB_EXECUTE)
    {
        switch (nCmdID)
        {
            // Minimize ribbon Command handler.
            case IDR_CMD_MINIMIZE:
                if (g_pFramework)
                {
                    IPropertyStore *pPropertyStore = NULL;
                    hr = g_pRibbon->QueryInterface(__uuidof(IPropertyStore), 
                                                   (void**)&pPropertyStore);
                    if (SUCCEEDED(hr))
                    {
                        if (ppropvarValue != NULL)
                        {
                            // Is the ToggleButton state on or off?
                            BOOL fToggled;
                            hr = UIPropertyToBoolean(*key, *ppropvarValue, &fToggled);

                            if (SUCCEEDED(hr))
                            {
                                // Set the ribbon display state based on the toggle state.
                                PROPVARIANT propvar;
                                PropVariantInit(&propvar);
                                UIInitPropertyFromBoolean(UI_PKEY_Minimized, 
                                                          fToggled, 
                                                          &propvar);
                                hr = pPropertyStore->SetValue(UI_PKEY_Minimized, 
                                                              propvar);
                                pPropertyStore->Commit();
                            }
                            pPropertyStore->Release();
                        }
                    }
                }
                break;
        }
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b74bd-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b74bd-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b74bd-150">Propriedades da faixa de faixas</span><span class="sxs-lookup"><span data-stu-id="b74bd-150">Ribbon Properties</span></span>](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

 