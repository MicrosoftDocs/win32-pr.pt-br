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
# <a name="context-popup"></a>Pop-up de contexto

Um popup de contexto é o controle principal na [**exibição ContextPopup**](windowsribbon-element-contextpopup.md) da estrutura da faixa de visão do Windows. É um sistema de menus de contexto avançado que só é exposto pela estrutura como uma extensão para uma implementação da faixa de uma. a estrutura não expõe o popup do contexto como um controle independente.

-   [Componentes do Popup de contexto](#context-popup)
-   [Implementar o Popup de contexto](#implement-the-context-popup)
    -   [Marcação](#markup)
    -   [Código](#code)
-   [Propriedades de pop-up de contexto](#context-popup-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="components-of-the-context-popup"></a>Componentes do Popup de contexto

O Popup de contexto é um contêiner lógico para o menu de contexto e Mini-Toolbar os subcontroles que são expostos por meio dos elementos de marcação [**ContextMenu**](windowsribbon-element-contextmenu.md) e [**Minibarra**](windowsribbon-element-minitoolbar.md) , respectivamente:

-   O [**ContextMenu**](windowsribbon-element-contextmenu.md) expõe um menu de comandos e galerias.
-   O [**Minibarra**](windowsribbon-element-minitoolbar.md) expõe uma barra de ferramentas flutuante de vários comandos, galerias e controles complexos, como o [controle de fonte](windowsribbon-controls-fontcontrol.md) e a caixa de [combinação](windowsribbon-controls-combobox.md).

Cada subcontrole pode aparecer no máximo uma vez em um pop-up de contexto.

A captura de tela a seguir ilustra o Popup de contexto e seus subcontroles constituintes.

![captura de tela com textos explicativos mostrando os componentes da interface do usuário contextual da faixa de e.](images/controls/contextpopup.png)

O Popup de contexto é puramente conceitual e não expõe nenhuma funcionalidade de interface do usuário, como o posicionamento ou o dimensionamento.

> [!Note]  
> O pop-up de contexto é normalmente exibido clicando com o botão direito do mouse (ou por meio do atalho de teclado SHIFT + F10) em um objeto de interesse. No entanto, as etapas necessárias para exibir o Popup de contexto são definidas pelo aplicativo.

 

## <a name="implement-the-context-popup"></a>Implementar o Popup de contexto

De maneira semelhante a outros controles de estrutura da faixa de tipos do Windows, o Popup de contexto é implementado por meio de um componente de marcação que especifica seus detalhes de apresentação e um componente de código que governa sua funcionalidade.

A tabela a seguir lista os controles com suporte em cada subcontrole Popup de contexto.



| Control                                                                  | Mini-Toolbar | Menu de contexto |
|--------------------------------------------------------------------------|--------------|--------------|
| [Botão](windowsribbon-controls-button.md)                              | x            | x            |
| [Caixa de seleção](windowsribbon-controls-checkbox.md)                         | x            | x            |
| [Caixa de combinação](windowsribbon-controls-combobox.md)                         | x            |              |
| [Botão suspenso](windowsribbon-controls-dropdownbutton.md)            | x            | x            |
| [Seletor de cores suspensa](windowsribbon-controls-dropdowncolorpicker.md) | x            | x            |
| [Galeria suspensa](windowsribbon-controls-dropdowngallery.md)          | x            | x            |
| [Controle de fonte](windowsribbon-controls-fontcontrol.md)                   | x            |              |
| [Botão ajuda](windowsribbon-controls-helpbutton.md)                     |              |              |
| [Galeria de faixa de bits](windowsribbon-controls-inribbongallery.md)          |              |              |
| [Controle giratório](windowsribbon-controls-spinner.md)                            |              |              |
| [Botão de divisão](windowsribbon-controls-splitbutton.md)                   | x            | x            |
| [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md)    | x            | x            |
| [Botão de alternância](windowsribbon-controls-togglebutton.md)                 | x            | x            |



 

### <a name="markup"></a>Marcação

Cada subcontrole Popup de contexto deve ser declarado individualmente na marcação.

### <a name="mini-toolbar"></a>Mini-Toolbar

Ao adicionar controles a uma mini-barra de ferramentas Popup de contexto, as duas recomendações a seguir devem ser consideradas:

-   Os controles devem ser altamente reconhecidos e fornecer uma funcionalidade óbvia. A familiaridade é a chave, pois rótulos e dicas de ferramentas não são expostos para controles de Mini-Toolbar.
-   Cada comando exposto por um controle deve ser apresentado em outro lugar na interface do usuário da faixa de para. O Mini-Toolbar não dá suporte à navegação de teclado.

O exemplo a seguir demonstra a marcação básica para um elemento [**Minibarra**](windowsribbon-element-minitoolbar.md) que contém três controles [Button](windowsribbon-controls-button.md) .

> [!Note]  
> Um elemento de um [**menu**](windowsribbon-element-menugroup.md) é especificado para cada linha de controles na Minibarra de ferramentas.

 


```C++
<MiniToolbar Name="MiniToolbar">
  <MenuGroup>
    <Button CommandName="cmdButton1" />
    <Button CommandName="cmdButton2" />
    <Button CommandName="cmdButton3" />
  </MenuGroup>
</MiniToolbar>
```



### <a name="context-menu"></a>Menu de contexto

O exemplo a seguir demonstra a marcação básica para um elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) que contém três controles [Button](windowsribbon-controls-button.md) .

> [!Note]  
> Cada conjunto de controles no elemento de [**menu**](windowsribbon-element-menugroup.md) é separado por uma barra horizontal no menu de contexto.

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



Embora um popup de contexto possa conter no máximo um de cada subcontrole, várias declarações de elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) e [**Minibarra**](windowsribbon-element-minitoolbar.md) na marcação da faixa de bits são válidas. Isso permite que um aplicativo ofereça suporte a várias combinações de menu de contexto e controles de Mini-Toolbar, com base nos critérios definidos pelo aplicativo, como o contexto do espaço de trabalho.

Para obter mais informações, consulte o elemento [**ContextMap**](windowsribbon-element-contextmap.md) .

O exemplo a seguir demonstra a marcação básica para o elemento [**ContextPopup**](windowsribbon-element-contextpopup.md) .


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



### <a name="code"></a>Código

Para invocar um pop-up de contexto, o método [**IUIContextualUI:: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) é chamado quando a janela de nível superior do aplicativo da faixa de faixas recebe uma notificação de CONTEXTMENU do WM \_ .

Este exemplo demonstra como tratar a \_ notificação CONTEXTMENU do WM no método WndProc () do aplicativo Ribbon.


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



O exemplo a seguir demonstra como um aplicativo de faixa de opções pode mostrar o Popup de contexto em um local de tela específico usando o método [**IUIContextualUI:: ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) .

GetCurrentContext () tem um valor de `cmdContextMap` , conforme definido no exemplo de marcação anterior.

g \_ pApplication é uma referência à interface [**IUIFramework**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework) .


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



A referência a [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) pode ser liberada antes que o popup do contexto seja descartado, conforme mostrado no exemplo anterior. No entanto, a referência deve ser liberada em algum ponto para evitar vazamentos de memória.

> [!Caution]  
> O Mini-Toolbar tem um efeito de esmaecimento interno baseado na proximidade do ponteiro do mouse. Por esse motivo, é recomendável que o Mini-Toolbar seja exibido o mais próximo possível do ponteiro do mouse. Caso contrário, devido aos mecanismos de exibição conflitantes, o Mini-Toolbar pode não ser renderizado conforme o esperado.

 

## <a name="context-popup-properties"></a>Propriedades de pop-up de contexto

Não há nenhuma chave de propriedade associada ao controle Popup de contexto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Biblioteca de controle do Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[Exemplo de ContextPopup](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 