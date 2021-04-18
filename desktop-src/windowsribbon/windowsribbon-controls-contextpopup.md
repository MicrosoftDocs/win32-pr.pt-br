---
title: Pop-up de contexto
description: Um popup de contexto é o controle principal na exibição ContextPopup da estrutura da faixa de visão do Windows.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77441cc3cdcc9212d27d2230d76d2618f1831ab
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105767005"
---
# <a name="context-popup"></a><span data-ttu-id="ac2bb-103">Pop-up de contexto</span><span class="sxs-lookup"><span data-stu-id="ac2bb-103">Context Popup</span></span>

<span data-ttu-id="ac2bb-104">Um popup de contexto é o controle principal na [**exibição ContextPopup**](windowsribbon-element-contextpopup.md) da estrutura da faixa de visão do Windows.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-104">A Context Popup is the principal control in the [**ContextPopup View**](windowsribbon-element-contextpopup.md) of the Windows Ribbon framework.</span></span> <span data-ttu-id="ac2bb-105">É um sistema de menus de contexto avançado que só é exposto pela estrutura como uma extensão para uma implementação da faixa de uma. a estrutura não expõe o popup do contexto como um controle independente.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-105">It is a rich context menu system that is only exposed by the framework as an extension to a Ribbon implementation—the framework does not expose the Context Popup as an independent control.</span></span>

-   [<span data-ttu-id="ac2bb-106">Componentes do Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="ac2bb-106">Components of the Context Popup</span></span>](#context-popup)
-   [<span data-ttu-id="ac2bb-107">Implementar o Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="ac2bb-107">Implement the Context Popup</span></span>](#implement-the-context-popup)
    -   [<span data-ttu-id="ac2bb-108">Marcação</span><span class="sxs-lookup"><span data-stu-id="ac2bb-108">Markup</span></span>](#markup)
    -   [<span data-ttu-id="ac2bb-109">Código</span><span class="sxs-lookup"><span data-stu-id="ac2bb-109">Code</span></span>](#code)
-   [<span data-ttu-id="ac2bb-110">Propriedades de pop-up de contexto</span><span class="sxs-lookup"><span data-stu-id="ac2bb-110">Context Popup Properties</span></span>](#context-popup-properties)
-   [<span data-ttu-id="ac2bb-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac2bb-111">Related topics</span></span>](#related-topics)

## <a name="components-of-the-context-popup"></a><span data-ttu-id="ac2bb-112">Componentes do Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="ac2bb-112">Components of the Context Popup</span></span>

<span data-ttu-id="ac2bb-113">O Popup de contexto é um contêiner lógico para o menu de contexto e Mini-Toolbar os subcontroles que são expostos por meio dos elementos de marcação [**ContextMenu**](windowsribbon-element-contextmenu.md) e [**Minibarra**](windowsribbon-element-minitoolbar.md) , respectivamente:</span><span class="sxs-lookup"><span data-stu-id="ac2bb-113">The Context Popup is a logical container for the Context Menu and Mini-Toolbar sub-controls that are exposed through the [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) markup elements, respectively:</span></span>

-   <span data-ttu-id="ac2bb-114">O [**ContextMenu**](windowsribbon-element-contextmenu.md) expõe um menu de comandos e galerias.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-114">The [**ContextMenu**](windowsribbon-element-contextmenu.md) exposes a menu of Commands and galleries.</span></span>
-   <span data-ttu-id="ac2bb-115">O [**Minibarra**](windowsribbon-element-minitoolbar.md) expõe uma barra de ferramentas flutuante de vários comandos, galerias e controles complexos, como o [controle de fonte](windowsribbon-controls-fontcontrol.md) e a caixa de [combinação](windowsribbon-controls-combobox.md).</span><span class="sxs-lookup"><span data-stu-id="ac2bb-115">The [**MiniToolbar**](windowsribbon-element-minitoolbar.md) exposes a floating toolbar of various Commands, galleries, and complex controls such as the [Font Control](windowsribbon-controls-fontcontrol.md) and the [Combo Box](windowsribbon-controls-combobox.md).</span></span>

<span data-ttu-id="ac2bb-116">Cada subcontrole pode aparecer no máximo uma vez em um pop-up de contexto.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-116">Each sub-control can appear at most once in a Context Popup.</span></span>

<span data-ttu-id="ac2bb-117">A captura de tela a seguir ilustra o Popup de contexto e seus subcontroles constituintes.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-117">The following screen shot illustrates the Context Popup and its constituent sub-controls.</span></span>

![captura de tela com textos explicativos mostrando os componentes da interface do usuário contextual da faixa de e.](images/controls/contextpopup.png)

<span data-ttu-id="ac2bb-119">O Popup de contexto é puramente conceitual e não expõe nenhuma funcionalidade de interface do usuário, como o posicionamento ou o dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-119">The Context Popup is purely conceptual and does not expose any UI functionality itself, such as positioning or sizing.</span></span>

> [!Note]  
> <span data-ttu-id="ac2bb-120">O pop-up de contexto é normalmente exibido clicando com o botão direito do mouse (ou por meio do atalho de teclado SHIFT + F10) em um objeto de interesse.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-120">The Context Popup is typically displayed by right-clicking the mouse (or through the keyboard shortcut SHIFT+F10) on an object of interest.</span></span> <span data-ttu-id="ac2bb-121">No entanto, as etapas necessárias para exibir o Popup de contexto são definidas pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-121">However, the steps required to display the Context Popup are defined by the application.</span></span>

 

## <a name="implement-the-context-popup"></a><span data-ttu-id="ac2bb-122">Implementar o Popup de contexto</span><span class="sxs-lookup"><span data-stu-id="ac2bb-122">Implement the Context Popup</span></span>

<span data-ttu-id="ac2bb-123">De maneira semelhante a outros controles de estrutura da faixa de tipos do Windows, o Popup de contexto é implementado por meio de um componente de marcação que especifica seus detalhes de apresentação e um componente de código que governa sua funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-123">In similar fashion to other Windows Ribbon framework controls, the Context Popup is implemented through a markup component that specifies its presentation details and a code component that governs its functionality.</span></span>

<span data-ttu-id="ac2bb-124">A tabela a seguir lista os controles com suporte em cada subcontrole Popup de contexto.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-124">The following table lists the controls that are supported by each Context Popup sub-control.</span></span>



| <span data-ttu-id="ac2bb-125">Control</span><span class="sxs-lookup"><span data-stu-id="ac2bb-125">Control</span></span>                                                                  | <span data-ttu-id="ac2bb-126">Mini-Toolbar</span><span class="sxs-lookup"><span data-stu-id="ac2bb-126">Mini-Toolbar</span></span> | <span data-ttu-id="ac2bb-127">Menu de contexto</span><span class="sxs-lookup"><span data-stu-id="ac2bb-127">Context Menu</span></span> |
|--------------------------------------------------------------------------|--------------|--------------|
| [<span data-ttu-id="ac2bb-128">Botão</span><span class="sxs-lookup"><span data-stu-id="ac2bb-128">Button</span></span>](windowsribbon-controls-button.md)                              | <span data-ttu-id="ac2bb-129">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-129">x</span></span>            | <span data-ttu-id="ac2bb-130">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-130">x</span></span>            |
| [<span data-ttu-id="ac2bb-131">Caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="ac2bb-131">Check Box</span></span>](windowsribbon-controls-checkbox.md)                         | <span data-ttu-id="ac2bb-132">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-132">x</span></span>            | <span data-ttu-id="ac2bb-133">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-133">x</span></span>            |
| [<span data-ttu-id="ac2bb-134">Caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="ac2bb-134">Combo Box</span></span>](windowsribbon-controls-combobox.md)                         | <span data-ttu-id="ac2bb-135">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-135">x</span></span>            |              |
| [<span data-ttu-id="ac2bb-136">Botão suspenso</span><span class="sxs-lookup"><span data-stu-id="ac2bb-136">Drop-Down Button</span></span>](windowsribbon-controls-dropdownbutton.md)            | <span data-ttu-id="ac2bb-137">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-137">x</span></span>            | <span data-ttu-id="ac2bb-138">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-138">x</span></span>            |
| [<span data-ttu-id="ac2bb-139">Seletor de cores suspensa</span><span class="sxs-lookup"><span data-stu-id="ac2bb-139">Drop-Down Color Picker</span></span>](windowsribbon-controls-dropdowncolorpicker.md) | <span data-ttu-id="ac2bb-140">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-140">x</span></span>            | <span data-ttu-id="ac2bb-141">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-141">x</span></span>            |
| [<span data-ttu-id="ac2bb-142">Galeria suspensa</span><span class="sxs-lookup"><span data-stu-id="ac2bb-142">Drop-Down Gallery</span></span>](windowsribbon-controls-dropdowngallery.md)          | <span data-ttu-id="ac2bb-143">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-143">x</span></span>            | <span data-ttu-id="ac2bb-144">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-144">x</span></span>            |
| [<span data-ttu-id="ac2bb-145">Controle de fonte</span><span class="sxs-lookup"><span data-stu-id="ac2bb-145">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)                   | <span data-ttu-id="ac2bb-146">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-146">x</span></span>            |              |
| [<span data-ttu-id="ac2bb-147">Botão ajuda</span><span class="sxs-lookup"><span data-stu-id="ac2bb-147">Help Button</span></span>](windowsribbon-controls-helpbutton.md)                     |              |              |
| [<span data-ttu-id="ac2bb-148">Galeria de faixa de bits</span><span class="sxs-lookup"><span data-stu-id="ac2bb-148">In-Ribbon Gallery</span></span>](windowsribbon-controls-inribbongallery.md)          |              |              |
| [<span data-ttu-id="ac2bb-149">Controle giratório</span><span class="sxs-lookup"><span data-stu-id="ac2bb-149">Spinner</span></span>](windowsribbon-controls-spinner.md)                            |              |              |
| [<span data-ttu-id="ac2bb-150">Botão de divisão</span><span class="sxs-lookup"><span data-stu-id="ac2bb-150">Split Button</span></span>](windowsribbon-controls-splitbutton.md)                   | <span data-ttu-id="ac2bb-151">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-151">x</span></span>            | <span data-ttu-id="ac2bb-152">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-152">x</span></span>            |
| [<span data-ttu-id="ac2bb-153">Galeria de botões de divisão</span><span class="sxs-lookup"><span data-stu-id="ac2bb-153">Split Button Gallery</span></span>](windowsribbon-controls-splitbuttongallery.md)    | <span data-ttu-id="ac2bb-154">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-154">x</span></span>            | <span data-ttu-id="ac2bb-155">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-155">x</span></span>            |
| [<span data-ttu-id="ac2bb-156">Botão de alternância</span><span class="sxs-lookup"><span data-stu-id="ac2bb-156">Toggle Button</span></span>](windowsribbon-controls-togglebutton.md)                 | <span data-ttu-id="ac2bb-157">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-157">x</span></span>            | <span data-ttu-id="ac2bb-158">x</span><span class="sxs-lookup"><span data-stu-id="ac2bb-158">x</span></span>            |



 

### <a name="markup"></a><span data-ttu-id="ac2bb-159">Marcação</span><span class="sxs-lookup"><span data-stu-id="ac2bb-159">Markup</span></span>

<span data-ttu-id="ac2bb-160">Cada subcontrole Popup de contexto deve ser declarado individualmente na marcação.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-160">Each Context Popup sub-control must be declared individually in markup.</span></span>

### <a name="mini-toolbar"></a><span data-ttu-id="ac2bb-161">Mini-Toolbar</span><span class="sxs-lookup"><span data-stu-id="ac2bb-161">Mini-Toolbar</span></span>

<span data-ttu-id="ac2bb-162">Ao adicionar controles a uma mini-barra de ferramentas Popup de contexto, as duas recomendações a seguir devem ser consideradas:</span><span class="sxs-lookup"><span data-stu-id="ac2bb-162">When adding controls to a Context Popup Mini-Toolbar, the following two recommendations should be considered:</span></span>

-   <span data-ttu-id="ac2bb-163">Os controles devem ser altamente reconhecidos e fornecer uma funcionalidade óbvia.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-163">Controls should be highly recognizable and provide obvious functionality.</span></span> <span data-ttu-id="ac2bb-164">A familiaridade é a chave, pois rótulos e dicas de ferramentas não são expostos para controles de Mini-Toolbar.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-164">Familiarity is key, as labels and tooltips are not exposed for Mini-Toolbar controls.</span></span>
-   <span data-ttu-id="ac2bb-165">Cada comando exposto por um controle deve ser apresentado em outro lugar na interface do usuário da faixa de para.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-165">Each Command exposed by a control should be presented elsewhere in the ribbon UI.</span></span> <span data-ttu-id="ac2bb-166">O Mini-Toolbar não dá suporte à navegação de teclado.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-166">The Mini-Toolbar does not support keyboard navigation.</span></span>

<span data-ttu-id="ac2bb-167">O exemplo a seguir demonstra a marcação básica para um elemento [**Minibarra**](windowsribbon-element-minitoolbar.md) que contém três controles [Button](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="ac2bb-167">The following example demonstrates the basic markup for a [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element that contains three [Button](windowsribbon-controls-button.md) controls.</span></span>

> [!Note]  
> <span data-ttu-id="ac2bb-168">Um elemento de um [**menu**](windowsribbon-element-menugroup.md) é especificado para cada linha de controles na Minibarra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-168">One [**MenuGroup**](windowsribbon-element-menugroup.md) element is specified for each row of controls in the Mini-Toolbar.</span></span>

 


```C++
<MiniToolbar Name="MiniToolbar">
  <MenuGroup>
    <Button CommandName="cmdButton1" />
    <Button CommandName="cmdButton2" />
    <Button CommandName="cmdButton3" />
  </MenuGroup>
</MiniToolbar>
```



### <a name="context-menu"></a><span data-ttu-id="ac2bb-169">Menu de contexto</span><span class="sxs-lookup"><span data-stu-id="ac2bb-169">Context Menu</span></span>

<span data-ttu-id="ac2bb-170">O exemplo a seguir demonstra a marcação básica para um elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) que contém três controles [Button](windowsribbon-controls-button.md) .</span><span class="sxs-lookup"><span data-stu-id="ac2bb-170">The following example demonstrates the basic markup for a [**ContextMenu**](windowsribbon-element-contextmenu.md) element that contains three [Button](windowsribbon-controls-button.md) controls.</span></span>

> [!Note]  
> <span data-ttu-id="ac2bb-171">Cada conjunto de controles no elemento de [**menu**](windowsribbon-element-menugroup.md) é separado por uma barra horizontal no menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-171">Each set of controls in the [**MenuGroup**](windowsribbon-element-menugroup.md) element is separated by a horizontal bar in the Context Menu.</span></span>

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



<span data-ttu-id="ac2bb-172">Embora um popup de contexto possa conter no máximo um de cada subcontrole, várias declarações de elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) e [**Minibarra**](windowsribbon-element-minitoolbar.md) na marcação da faixa de bits são válidas.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-172">Although a Context Popup can contain at most one of each sub-control, multiple [**ContextMenu**](windowsribbon-element-contextmenu.md) and [**MiniToolbar**](windowsribbon-element-minitoolbar.md) element declarations in the Ribbon markup are valid.</span></span> <span data-ttu-id="ac2bb-173">Isso permite que um aplicativo ofereça suporte a várias combinações de menu de contexto e controles de Mini-Toolbar, com base nos critérios definidos pelo aplicativo, como o contexto do espaço de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-173">This allows an application to support various combinations of Context Menu and Mini-Toolbar controls, based on criteria defined by the application, such as workspace context.</span></span>

<span data-ttu-id="ac2bb-174">Para obter mais informações, consulte o elemento [**ContextMap**](windowsribbon-element-contextmap.md) .</span><span class="sxs-lookup"><span data-stu-id="ac2bb-174">For more information, see the [**ContextMap**](windowsribbon-element-contextmap.md) element.</span></span>

<span data-ttu-id="ac2bb-175">O exemplo a seguir demonstra a marcação básica para o elemento [**ContextPopup**](windowsribbon-element-contextpopup.md) .</span><span class="sxs-lookup"><span data-stu-id="ac2bb-175">The following example demonstrates the basic markup for the [**ContextPopup**](windowsribbon-element-contextpopup.md) element.</span></span>


```C++
<ContextPopup>
  <ContextPopup.MiniToolbars>
    <MiniToolbar Name="MiniToolbar">
      <MenuGroup>
        <Button CommandName="cmdButton1" />
        <Button CommandName="cmdButton2" />
        <Button CommandName="cmdButton3" />
      </MenuGroup>
    </MiniToolbar>
  </ContextPopup.MiniToolbars>
  <ContextPopup.ContextMenus>
    <ContextMenu Name="ContextMenu">
      <MenuGroup>
        <Button CommandName="cmdCut" />
        <Button CommandName="cmdCopy" />
        <Button CommandName="cmdPaste" />
      </MenuGroup>
    </ContextMenu>
  </ContextPopup.ContextMenus>
  <ContextPopup.ContextMaps>
    <ContextMap CommandName="cmdContextMap" ContextMenu="ContextMenu" MiniToolbar="MiniToolbar"/>
  </ContextPopup.ContextMaps>
</ContextPopup>
```



### <a name="code"></a><span data-ttu-id="ac2bb-176">Código</span><span class="sxs-lookup"><span data-stu-id="ac2bb-176">Code</span></span>

<span data-ttu-id="ac2bb-177">Para invocar um pop-up de contexto, o método [**IUIContextualUI:: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) é chamado quando a janela de nível superior do aplicativo da faixa de faixas recebe uma notificação de CONTEXTMENU do WM \_ .</span><span class="sxs-lookup"><span data-stu-id="ac2bb-177">To invoke a Context Popup, the [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) method is called when the top-level window of the Ribbon application receives a WM\_CONTEXTMENU notification.</span></span>

<span data-ttu-id="ac2bb-178">Este exemplo demonstra como tratar a \_ notificação CONTEXTMENU do WM no método WndProc () do aplicativo Ribbon.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-178">This example demonstrates how to handle the WM\_CONTEXTMENU notification in the WndProc() method of the Ribbon application.</span></span>


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



<span data-ttu-id="ac2bb-179">O exemplo a seguir demonstra como um aplicativo de faixa de opções pode mostrar o Popup de contexto em um local de tela específico usando o método [**IUIContextualUI:: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) .</span><span class="sxs-lookup"><span data-stu-id="ac2bb-179">The following example demonstrates how a Ribbon application can show the Context Popup at a specific screen location using the [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) method.</span></span>

<span data-ttu-id="ac2bb-180">GetCurrentContext () tem um valor de `cmdContextMap` , conforme definido no exemplo de marcação anterior.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-180">GetCurrentContext() has a value of `cmdContextMap` as defined in the preceding markup example.</span></span>

<span data-ttu-id="ac2bb-181">g \_ pApplication é uma referência à interface [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) .</span><span class="sxs-lookup"><span data-stu-id="ac2bb-181">g\_pApplication is a reference to the [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) interface.</span></span>


```C++
HRESULT ShowContextualUI(POINT& ptLocation, HWND hWnd)
{
  GetDisplayLocation(ptLocation, hWnd);

  HRESULT hr = E_FAIL;

  IUIContextualUI* pContextualUI = NULL;
 
  if (SUCCEEDED(g_pFramework->GetView(
                                g_pApplication->GetCurrentContext(), 
                                IID_PPV_ARGS(&pContextualUI))))
  {
    hr = pContextualUI->ShowAtLocation(ptLocation.x, ptLocation.y);
    pContextualUI->Release();
  }

  return hr;
}
```



<span data-ttu-id="ac2bb-182">A referência a [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) pode ser liberada antes que o popup do contexto seja descartado, conforme mostrado no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-182">The reference to [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) can be released before the Context Popup is dismissed, as shown in the preceding example.</span></span> <span data-ttu-id="ac2bb-183">No entanto, a referência deve ser liberada em algum ponto para evitar vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-183">However, the reference must be released at some point to avoid memory leaks.</span></span>

> [!Caution]  
> <span data-ttu-id="ac2bb-184">O Mini-Toolbar tem um efeito de esmaecimento interno baseado na proximidade do ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-184">The Mini-Toolbar has a built-in fade effect that is based on the proximity of the mouse pointer.</span></span> <span data-ttu-id="ac2bb-185">Por esse motivo, é recomendável que o Mini-Toolbar seja exibido o mais próximo possível do ponteiro do mouse.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-185">For this reason, it is recommended that the Mini-Toolbar be displayed as close to the mouse pointer as possible.</span></span> <span data-ttu-id="ac2bb-186">Caso contrário, devido aos mecanismos de exibição conflitantes, o Mini-Toolbar pode não ser renderizado conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-186">Otherwise, due to the conflicting display mechanisms, the Mini-Toolbar may not render as expected.</span></span>

 

## <a name="context-popup-properties"></a><span data-ttu-id="ac2bb-187">Propriedades de pop-up de contexto</span><span class="sxs-lookup"><span data-stu-id="ac2bb-187">Context Popup Properties</span></span>

<span data-ttu-id="ac2bb-188">Não há nenhuma chave de propriedade associada ao controle Popup de contexto.</span><span class="sxs-lookup"><span data-stu-id="ac2bb-188">There are no property keys associated with the Context Popup control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac2bb-189">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac2bb-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac2bb-190">Biblioteca de controle do Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="ac2bb-190">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="ac2bb-191">Exemplo de ContextPopup</span><span class="sxs-lookup"><span data-stu-id="ac2bb-191">ContextPopup Sample</span></span>](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 