---
title: Propriedade QuickAccessToolbar.ApplicationDefaults
description: Representa um contêiner para comandos padrão na QAT (Barra de Ferramentas de Acesso Rápido).
ms.assetid: 8f44d7c0-1a39-4a88-ae01-7d7d1bb6bf7e
keywords:
- Propriedade QuickAccessToolbar.ApplicationDefaults Windows Faixa de Opções
topic_type:
- apiref
api_name:
- QuickAccessToolbar.ApplicationDefaults
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701a7c72e40b1efe9104d6794fa739c556b0fb4b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473742"
---
# <a name="quickaccesstoolbarapplicationdefaults-property"></a>Propriedade QuickAccessToolbar.ApplicationDefaults

Representa um contêiner para comandos padrão na [QAT (Barra de](windowsribbon-controls-quickaccesstoolbar.md)Ferramentas de Acesso Rápido).

## <a name="usage"></a>Uso

``` syntax
<QuickAccessToolbar.ApplicationDefaults>
  child elements
</QuickAccessToolbar.ApplicationDefaults>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho




| Elemento | Descrição | 
|---------|-------------|
| <a href="windowsribbon-element-button.md"><strong>Botão</strong></a><br /> | Deve ocorrer pelo menos uma vez.<br /><br /> | 
| <a href="windowsribbon-element-checkbox.md"><strong>Checkbox</strong></a><br /> | Deve ocorrer pelo menos uma vez.<br /><br /> | 
| <a href="windowsribbon-element-combobox.md"><strong>ComboBox</strong></a><br /> | Deve ocorrer pelo menos uma vez.<br /><blockquote>[!Note]<br />Windows 8 e mais novos.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-dropdowngallery.md"><strong>DropDownGallery</strong></a><br /> | Deve ocorrer pelo menos uma vez.<br /><blockquote>[!Note]<br />Windows 8 e mais novos.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-inribbongallery.md"><strong>InRibbonGallery</strong></a><br /> | Deve ocorrer pelo menos uma vez.<br /><blockquote>[!Note]<br />Windows 8 e mais novos.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-splitbuttongallery.md"><strong>SplitButtonGallery</strong></a><br /> | Deve ocorrer pelo menos uma vez.<br /><blockquote>[!Note]<br />Windows 8 e mais novos.</blockquote><br /><br /> | 
| <a href="windowsribbon-element-togglebutton.md"><strong>ToggleButton</strong></a><br /> | Deve ocorrer pelo menos uma vez.<br /><br /> | 




## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                           |
|-----------------------------------------------------------------------------------|
| [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para [**cada QuickAccessToolbar.**](windowsribbon-element-quickaccesstoolbar.md)

Um mínimo de um elemento filho deve ser especificado.

Um máximo de 20 elementos filho pode ser especificado.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para [**o QuickAccessToolbar.**](windowsribbon-element-quickaccesstoolbar.md)

Esta seção de código mostra a declaração de controle **QuickAccessToolbar.ApplicationDefaults.**


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle da Barra de Ferramentas de Acesso Rápido](windowsribbon-controls-quickaccesstoolbar.md)
</dt> </dl>

 

 





