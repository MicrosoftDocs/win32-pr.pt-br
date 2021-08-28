---
title: Propriedade ContextPopup.MiniToolbars
description: Representa um contêiner para elementos MiniToolbar.
ms.assetid: 5c17e070-0520-44e6-a066-476107691205
keywords:
- Propriedade ContextPopup.MiniToolbars Windows Faixa de Opções
topic_type:
- apiref
api_name:
- ContextPopup.MiniToolbars
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18f4a083d894f798d83bd153fe74b9fb0560e2fbdb8132ec7874db0a2e533824
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772126"
---
# <a name="contextpopupminitoolbars-property"></a>Propriedade ContextPopup.MiniToolbars

Representa um contêiner para [**elementos MiniToolbar.**](windowsribbon-element-minitoolbar.md)

## <a name="usage"></a>Uso

``` syntax
<ContextPopup.MiniToolbars>
  child elements
</ContextPopup.MiniToolbars>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho



| Elemento                                                             | Descrição                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [**MiniToolbar**](windowsribbon-element-minitoolbar.md)<br/> | Pode ocorrer uma ou mais vezes<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                               |
|-----------------------------------------------------------------------|
| [**ContextPopup**](windowsribbon-element-contextpopup.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para [**cada ContextPopup.**](windowsribbon-element-contextpopup.md)

Como os controles no [**MiniToolbar**](windowsribbon-element-minitoolbar.md) não são acessíveis ao teclado, os comandos que eles expõem devem estar disponíveis em outro lugar na interface do usuário da Faixa de Opções.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para uma [**Exibição contextpopup.**](windowsribbon-element-contextpopup.md)

Esta seção de código mostra a **declaração de controle ContextPopup.MiniToolbars.**


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



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle pop-up de contexto](windowsribbon-controls-contextpopup.md)
</dt> </dl>

 

 





