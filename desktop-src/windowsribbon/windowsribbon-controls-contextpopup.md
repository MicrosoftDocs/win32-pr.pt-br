---
title: Pop-up de contexto
description: Um Pop-up de contexto é o controle principal na Exibição ContextPopup da estrutura Windows Faixa de Opções.
ms.assetid: c41b888a-15aa-4c47-ad73-5dc30b5fa6f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15424aa8b2b82580218eb3663e4b157bce321fdde027e03101ce2cf38626aac2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118964405"
---
# <a name="context-popup"></a>Pop-up de contexto

Um Pop-up de contexto é o controle principal na [**Exibição ContextPopup**](windowsribbon-element-contextpopup.md) da estrutura Windows Faixa de Opções. É um sistema de menu de contexto rico que só é exposto pela estrutura como uma extensão para uma implementação da Faixa de Opções — a estrutura não expõe o Pop-up de Contexto como um controle independente.

-   [Componentes do pop-up de contexto](#context-popup)
-   [Implementar o pop-up de contexto](#implement-the-context-popup)
    -   [Marcação](#markup)
    -   [Código](#code)
-   [Propriedades pop-up de contexto](#context-popup-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="components-of-the-context-popup"></a>Componentes do pop-up de contexto

O Pop-up de Contexto é um contêiner lógico para o Menu de Contexto e Mini-Toolbar sub-controles que são expostos por meio dos elementos de marcação [**ContextMenu**](windowsribbon-element-contextmenu.md) e [**MiniToolbar,**](windowsribbon-element-minitoolbar.md) respectivamente:

-   O [**ContextMenu expõe**](windowsribbon-element-contextmenu.md) um menu de Comandos e galerias.
-   O [**MiniToolbar**](windowsribbon-element-minitoolbar.md) expõe uma barra de ferramentas flutuante de vários comandos, galerias e controles complexos, como o Controle de Fonte e a [Caixa de Combinação](windowsribbon-controls-combobox.md). [](windowsribbon-controls-fontcontrol.md)

Cada subcontrole pode aparecer no máximo uma vez em um Pop-up de contexto.

A captura de tela a seguir ilustra o Pop-up de Contexto e seus sub-controles constituintes.

![captura de tela com explicações mostrando os componentes contextuais da interface do usuário da faixa de opções.](images/controls/contextpopup.png)

O Pop-up de Contexto é puramente conceitual e não expõe nenhuma funcionalidade da interface do usuário em si, como posicionamento ou tamanho.

> [!Note]  
> O Pop-up de Contexto normalmente é exibido clicando com o botão direito do mouse (ou por meio do atalho de teclado SHIFT+F10) em um objeto de interesse. No entanto, as etapas necessárias para exibir o Pop-up de Contexto são definidas pelo aplicativo.

 

## <a name="implement-the-context-popup"></a>Implementar o pop-up de contexto

De maneira semelhante a outros controles de estrutura Windows Ribbon, o Pop-up de Contexto é implementado por meio de um componente de marcação que especifica seus detalhes de apresentação e um componente de código que rege sua funcionalidade.

A tabela a seguir lista os controles que têm suporte em cada subcontrole pop-up de contexto.



| Control                                                                  | Mini-Toolbar | Menu de contexto |
|--------------------------------------------------------------------------|--------------|--------------|
| [Botão](windowsribbon-controls-button.md)                              | x            | x            |
| [Caixa de seleção](windowsribbon-controls-checkbox.md)                         | x            | x            |
| [Caixa de combinação](windowsribbon-controls-combobox.md)                         | x            |              |
| [Botão de lista listada](windowsribbon-controls-dropdownbutton.md)            | x            | x            |
| [Lista Seletor de Cor](windowsribbon-controls-dropdowncolorpicker.md) | x            | x            |
| [Galeria de lista listada](windowsribbon-controls-dropdowngallery.md)          | x            | x            |
| [Controle de fonte](windowsribbon-controls-fontcontrol.md)                   | x            |              |
| [Botão Ajuda](windowsribbon-controls-helpbutton.md)                     |              |              |
| [Galeria na Faixa de Opções](windowsribbon-controls-inribbongallery.md)          |              |              |
| [Controle giratório](windowsribbon-controls-spinner.md)                            |              |              |
| [Botão Dividir](windowsribbon-controls-splitbutton.md)                   | x            | x            |
| [Galeria de Botões divididos](windowsribbon-controls-splitbuttongallery.md)    | x            | x            |
| [Botão de alternância](windowsribbon-controls-togglebutton.md)                 | x            | x            |



 

### <a name="markup"></a>Marcação

Cada subcontrole pop-up de contexto deve ser declarado individualmente na marcação.

### <a name="mini-toolbar"></a>Mini-Toolbar

Ao adicionar controles a uma minibar de ferramentas pop-up de contexto, as duas recomendações a seguir devem ser consideradas:

-   Os controles devem ser altamente reconhecíveis e fornecer funcionalidade óbvia. A familiaridade é fundamental, pois rótulos e dicas de ferramenta não são expostos para Mini-Toolbar controles.
-   Cada comando exposto por um controle deve ser apresentado em outro lugar na interface do usuário da faixa de opções. O Mini-Toolbar não dá suporte à navegação por teclado.

O exemplo a seguir demonstra a marcação básica para um [**elemento MiniToolbar**](windowsribbon-element-minitoolbar.md) que contém três controles [Button.](windowsribbon-controls-button.md)

> [!Note]  
> Um [**elemento MenuGroup**](windowsribbon-element-menugroup.md) é especificado para cada linha de controles na barra de ferramentas mini.

 


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

O exemplo a seguir demonstra a marcação básica para um [**elemento ContextMenu**](windowsribbon-element-contextmenu.md) que contém três controles [Button.](windowsribbon-controls-button.md)

> [!Note]  
> Cada conjunto de controles no [**elemento MenuGroup**](windowsribbon-element-menugroup.md) é separado por uma barra horizontal no Menu de Contexto.

 


```C++
<ContextMenu Name="ContextMenu">
  <MenuGroup>
    <Button CommandName="cmdCut" />
    <Button CommandName="cmdCopy" />
    <Button CommandName="cmdPaste" />
  </MenuGroup>
</ContextMenu>
```



Embora um Pop-up de Contexto possa conter no máximo um de cada subcontrole, várias declarações de elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) e [**MiniToolbar**](windowsribbon-element-minitoolbar.md) na marcação Ribbon são válidas. Isso permite que um aplicativo dá suporte a várias combinações de menu de contexto e controles Mini-Toolbar, com base em critérios definidos pelo aplicativo, como contexto de workspace.

Para obter mais informações, consulte o [**elemento ContextMap.**](windowsribbon-element-contextmap.md)

O exemplo a seguir demonstra a marcação básica para o [**elemento ContextPopup.**](windowsribbon-element-contextpopup.md)


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

Para invocar um Pop-up de Contexto, o método [**IUIContextualUI::ShowAtLocation**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation) é chamado quando a janela de nível superior do aplicativo ribbon recebe uma notificação WM \_ CONTEXTMENU.

Este exemplo demonstra como manipular a notificação \_ CONTEXTMENU wm no método WndProc() do aplicativo Ribbon.


```C++
case WM_CONTEXTMENU:
  POINT pt;
  POINTSTOPOINT(pt, lParam);

  // ShowContextualUI method defined by the application.
  ShowContextualUI (pt, hWnd);
  break;
```



O exemplo a seguir demonstra como um aplicativo de Faixa de Opções pode mostrar o Pop-up de Contexto em um local de tela específico usando o [**método IUIContextualUI::ShowAtLocation.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicontextualui-showatlocation)

GetCurrentContext() tem um valor de `cmdContextMap` conforme definido no exemplo de marcação anterior.

g \_ pApplication é uma referência à interface [**IUIFramework.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiframework)


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



A referência a [**IUIContextualUI**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicontextualui) pode ser liberada antes que o Pop-up de Contexto seja ignorado, conforme mostrado no exemplo anterior. No entanto, a referência deve ser liberada em algum momento para evitar vazamentos de memória.

> [!Caution]  
> O Mini-Toolbar tem um efeito de esmaeçando integrado que se baseia na proximidade do ponteiro do mouse. Por esse motivo, é recomendável que o Mini-Toolbar seja exibido o mais próximo possível do ponteiro do mouse. Caso contrário, devido aos mecanismos de exibição conflitantes, o Mini-Toolbar pode não renderizar conforme o esperado.

 

## <a name="context-popup-properties"></a>Propriedades pop-up de contexto

Não há nenhuma chave de propriedade associada ao controle Pop-up de Contexto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Biblioteca de Controle da Estrutura de Faixa de Opções](windowsribbon-controls-entry.md)
</dt> <dt>

[Exemplo de ContextPopup](windowsribbon-contextpopupsample.md)
</dt> </dl>

 

 