---
title: Grupo de menus
description: O grupo de menus organiza comandos e controles relacionados em um menu ou barra de ferramentas.
ms.assetid: 5454f2a3-275b-47f4-ae97-d10dd12da5ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9862e78cbedf84b92c7540bec4de58288af5c9ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917571"
---
# <a name="menu-group"></a>Grupo de menus

O grupo de menus organiza comandos e controles relacionados em um menu ou barra de ferramentas.

-   [Introdução](#introduction)
-   [Propriedades do grupo de menus](#menu-group-properties)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

O controle de grupo de menu, exposto por meio do elemento de marcação de [**menu**](windowsribbon-element-menugroup.md) , é um contêiner lógico para grupos de itens ou comandos em controles baseados em menus, incluindo a mini-barra de ferramentas [Popup de contexto](windowsribbon-controls-contextpopup.md) .

Um rótulo pode ser especificado para um grupo de menus por meio do atributo *LabelTitle* ou da propriedade [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) de uma declaração de comando associada. O valor atribuído a *LabelTitle* é renderizado como um cabeçalho de categoria.

O exemplo a seguir demonstra a marcação de comando para um controle de [botão de divisão](windowsribbon-controls-splitbutton.md) que inclui duas declarações de comando de grupo de menus.


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



O exemplo a seguir demonstra a marcação necessária para um elemento [**SplitButton**](windowsribbon-element-splitbutton.md) com três declarações de elemento de [**menu**](windowsribbon-element-menugroup.md) , duas das quais são associadas aos comandos de grupo de menus do exemplo anterior. O atributo de *classe* do elemento de **menu** é usado para especificar o tamanho dos itens de menu.


```XML
<Group CommandName="cmdSplitButtonGroup">
  <SplitButton CommandName="cmdSplitButton">
    <SplitButton.ButtonItem>
      <Button CommandName="cmdSBButtonItem"/>
    </SplitButton.ButtonItem>
    <SplitButton.MenuGroups>
      <MenuGroup CommandName="cmdSBMajorItems" 
                 Class="MajorItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup CommandName="cmdSBStandardItems"
                 Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
      <MenuGroup Class="StandardItems">
        <Button CommandName="cmdSBButton1"/>
        <Button CommandName="cmdSBButton1"/>
      </MenuGroup>
    </SplitButton.MenuGroups>
  </SplitButton>
</Group>
```



A captura de tela a seguir ilustra o menu (com três controles de grupo de menus) que é gerado a partir da marcação nos exemplos anteriores.

![captura de tela de um menu com três controles de grupo de menus.](images/controls/menugroup.png)

## <a name="menu-group-properties"></a>Propriedades do grupo de menus

A estrutura da faixa de faixas define uma coleção de [chaves de propriedade](windowsribbon-reference-properties.md) para o controle de grupo de menus.

Normalmente, uma propriedade de grupo de menus é atualizada na interface do usuário da faixa de forma invalidando o comando associado ao controle por meio de uma chamada para o método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) . O evento Invalidation é tratado e as atualizações de propriedade são definidas pelo método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .

O método de retorno de chamada [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) não é executado e o aplicativo consultou um valor de propriedade atualizado, até que a propriedade seja exigida pela estrutura. Por exemplo, quando uma guia é ativada e um controle revelado na interface do usuário da faixa de ferramentas, ou quando uma dica de ferramenta é exibida.

> [!Note]  
> Em alguns casos, uma propriedade pode ser recuperada por meio do método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e definida com o método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .

 

A tabela a seguir lista as chaves de propriedade que estão associadas ao controle de grupo de menu.



| Chave de propriedade                                                                                     | Observações                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Interface do usuário \_ PKEY \_ habilitada](windowsribbon-reference-properties-uipkey-enabled.md)                       | Dá suporte a [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) e [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). |
| [\_KeyTip PKEY \_ UI](windowsribbon-reference-properties-uipkey-keytip.md)                         | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [\_Rótulo de PKEY da interface do usuário \_](windowsribbon-reference-properties-uipkey-label.md)                           | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [\_TooltipDescription PKEY \_ UI](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |
| [\_TooltipTitle PKEY \_ UI](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | Só pode ser atualizado por meio de invalidação.                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Biblioteca de controle do Windows Ribbon Framework](windowsribbon-controls-entry.md)
</dt> <dt>

[**Elemento de marcação de menu**](windowsribbon-element-menugroup.md)
</dt> </dl>

 

 