---
title: Elemento MiniToolbar
description: Representa uma barra de ferramentas contextual.
ms.assetid: bb50890d-554a-4add-a583-d4fd48b823bf
keywords:
- Elemento MiniToolbar Windows Faixa de Opções
topic_type:
- apiref
api_name:
- MiniToolbar
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e47fee9fbf2b6b0bc95153fd512f6484129dc7f3edebd56e1d97664ecc2bbef0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119881736"
---
# <a name="minitoolbar-element"></a>Elemento MiniToolbar

Representa uma barra de ferramentas contextual.

## <a name="usage"></a>Uso

``` syntax
<MiniToolbar
  Name = "xs:string">
  child elements
</MiniToolbar>
```

## <a name="attributes"></a>Atributos



| Atributo           | Type                 | Obrigatório       | Descrição                                                                                                                                                                                                                |
|---------------------|----------------------|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome**<br/> | xs:string<br/> | Sim<br/> | <dt> (xs:string)<br/> </dt> <dd> Uma cadeia de caracteres composta por qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.<br/> </dd> </dl> |



## <a name="child-elements"></a>Elementos filho



| Elemento                                                         | Descrição                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [**Menugroup**](windowsribbon-element-menugroup.md)<br/> | Deve ocorrer pelo menos uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                                         |
|-------------------------------------------------------------------------------------------------|
| [**ContextPopup.MiniToolbars**](windowsribbon-element-contextpopup-minitoolbars.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer uma ou mais vezes para cada [**ContextPopup.MiniToolbars.**](windowsribbon-element-contextpopup-minitoolbars.md)

Ao contrário [**do elemento ContextMenu,**](windowsribbon-element-contextmenu.md) a **MiniToolbar** permanece visível quando um item na barra de ferramentas é clicado.

Se exibido sem um [**ContextMenu,**](windowsribbon-element-contextmenu.md)a **MiniToolbar** esmaece à medida que o ponteiro do mouse é movido para fora.

> [!Note]  
> Devido a esse comportamento de esbotão, [**um ContextMenu**](windowsribbon-element-contextmenu.md) deve ser exibido próximo ao ponteiro do mouse.

 

Como os controles no **MiniToolbar** não são acessíveis ao teclado, os comandos que eles expõem devem estar disponíveis em outro lugar na interface do usuário da Faixa de Opções.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para uma [**Exibição contextpopup.**](windowsribbon-element-contextpopup.md)

Esta seção de código mostra um conjunto de declarações **de controle MiniToolbar.**


```XML
    <ContextPopup>
      <!--
        The MiniToolbars and Context Menus are the basic ingredients for 
        the contextual UI popup. 
        Mix-and-match and associate each combination with a ContextMap Command 
        invoked in code.
      -->
      <ContextPopup.MiniToolbars>
        <MiniToolbar Name="MiniToolbar1">
          <MenuGroup Class="MajorItems">
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
            <DropDownButton CommandName="cmdButtons">
              <MenuGroup>
                <Button CommandName="cmdButton1" />
                <Button CommandName="cmdButton2" />
                <Button CommandName="cmdButton3" />
              </MenuGroup>
            </DropDownButton>
          </MenuGroup>
        </MiniToolbar>
        <MiniToolbar Name="MiniToolbar2">
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </MiniToolbar>
      </ContextPopup.MiniToolbars>
      <ContextPopup.ContextMenus>
        <ContextMenu Name="ContextMenu1">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu2">
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
        <ContextMenu Name="ContextMenu4">
          <MenuGroup>
            <Button CommandName="cmdCut" />
            <Button CommandName="cmdCopy" />
            <Button CommandName="cmdPaste" />
          </MenuGroup>
          <MenuGroup>
            <ToggleButton CommandName="cmdToggleButton" />
          </MenuGroup>
          <MenuGroup>
            <Button CommandName="cmdButton1" />
            <Button CommandName="cmdButton2" />
            <Button CommandName="cmdButton3" />
          </MenuGroup>
        </ContextMenu>
      </ContextPopup.ContextMenus>
      <ContextPopup.ContextMaps>
        <ContextMap CommandName="cmdContextMap1"
                    ContextMenu="ContextMenu1"/>
        <ContextMap CommandName="cmdContextMap2"
                    ContextMenu="ContextMenu2"
                    MiniToolbar="MiniToolbar1"/>
        <ContextMap CommandName="cmdContextMap3"
                    MiniToolbar="MiniToolbar2"/>
        <ContextMap CommandName="cmdContextMap4"
                    ContextMenu="ContextMenu4"/>
      </ContextPopup.ContextMaps>
    </ContextPopup>
```



## <a name="element-information"></a>Informações do elemento

* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Não



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle pop-up de contexto](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





