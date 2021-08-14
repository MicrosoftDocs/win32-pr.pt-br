---
title: Declarando comandos e controles com marcação de faixa de opções
description: A Windows ribbon usa uma linguagem de marcação baseada em Extensible Application Markup Language (XAML) para implementar declarativamente a aparência de um aplicativo de Faixa de Opções.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Windows Faixa de opções, estrutura de marcação
- Faixa de opções, estrutura de marcação
- Windows Faixa de opções, separando a apresentação da lógica de comando
- Faixa de opções, separando a apresentação da lógica de comando
- Windows Faixa de opções, componentes
- Faixa de opções, componentes
- sistema de comandos para Windows faixa de opções
- controles para Windows faixa de opções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20ae6c8d62012fac240c6d044c688295d89d8d5899e3673a3b914d8d142111d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201318"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a>Declarando comandos e controles com marcação de faixa de opções

A Windows ribbon usa uma linguagem de marcação baseada em Extensible Application Markup Language (XAML) para implementar declarativamente a aparência de um aplicativo de Faixa de Opções.

-   [Separando a apresentação da lógica de comando](#separating-presentation-from-command-logic)
-   [Estrutura de marcação](#markup-structure)
-   [Componentes da faixa de opções](#ribbon-components)
-   [Tópicos relacionados](#related-topics)

## <a name="separating-presentation-from-command-logic"></a>Separando a apresentação da lógica de comando

A separação de atributos visuais e de apresentação da lógica de comando na estrutura da Faixa de Opções é realizada por meio de duas plataformas de desenvolvimento distintas, mas dependentes. Layouts de controle, comportamentos de dimensionamento, declarações de comando e especificações de recurso são o domínio de tempo de design de uma sintaxe de marcação declarativa com base [na especificação Extensible Application Markup Language (XAML).](/dotnet/framework/wpf/advanced/xaml-in-wpf) A funcionalidade de baixo nível, os ganchos de aplicativo e os manipuladores de comando são definidos em implementações de interface baseadas Component Object Model (COM).

Essa separação de apresentação e lógica oferece os seguintes benefícios:

-   Um ciclo de desenvolvimento de aplicativos mais eficiente que permite que desenvolvedores e designers de interface do usuário implementem a GUI do aplicativo da Faixa de Opções independentemente da funcionalidade principal do aplicativo. Essa funcionalidade principal pode ser deixada para desenvolvedores de software dedicados.
-   Manutenção menos custosa porque as alterações na GUI são possíveis sem alterações na funcionalidade principal (e vice-versa).
-   Especificação simples de recursos de cadeia de caracteres e imagem por meio de marcação.
-   Facilidade de criação de protótipos.

## <a name="markup-structure"></a>Estrutura de marcação

Existem dois branches distintos dentro da estrutura de marcação da estrutura ribbon.

O primeiro branch contém um manifesto de declarações de comando e de recurso (cadeias de caracteres e imagens). Cada entrada Command é usada pela estrutura para vincular um controle ribbon, por meio de uma ID de comando, a um manipulador de comandos definido no código do aplicativo.

O segundo branch contém as declarações de controle reais. Cada controle é associado a um Comando por meio de um atributo *CommandName* que mapeia para um *atributo Name* especificado em cada declaração command.

## <a name="ribbon-components"></a>Componentes da faixa de opções

A funcionalidade de interface do usuário da estrutura de faixa de opções é exposta por meio de [Exibições](windowsribbon-reference-elements-view.md). Uma Exibição é essencialmente um [](windowsribbon-element-ribbon.md) contêiner, como a Faixa de Opções e [**ContextPopup**](windowsribbon-element-contextpopup.md), que é usado para apresentar controles de estrutura e os Comandos aos qual eles estão vinculados.

A [](windowsribbon-element-ribbon.md) Exibição da Faixa de Opções é composta por vários componentes que incluem um [Menu](windowsribbon-controls-applicationmenu.md)de Aplicativos, a [QAT (Barra](windowsribbon-controls-quickaccesstoolbar.md) de Ferramentas de Acesso Rápido) para exibir Comandos comumente usados da interface do usuário da faixa de opções, guias principais e contextuais que contêm grupos de [controles](windowsribbon-controls-tab.md) e o sistema de menus de contexto avançados [**do ContextPopup.**](windowsribbon-element-contextpopup.md) [](windowsribbon-controls-group.md)

Todos os componentes da Faixa de Opções são declarados em um arquivo de marcação autônomo que:

-   Especifica as propriedades básicas para cada elemento.
-   Mostra relações hierárquicas claramente.
-   Fornece preferências de layout e dicas de dimensionamento. Para obter mais informações sobre modelos de layout de estrutura de faixa de opções, consulte Personalização de uma faixa de opções por definições [de tamanho e políticas de dimensionamento](windowsribbon-templates.md).
-   Fornece uma maneira de definir recursos como imagens e rótulos. Para obter mais informações sobre recursos de imagem, consulte [Especificando recursos de](windowsribbon-imageformats.md)imagem da faixa de opções .

Os dois exemplos de marcação da Faixa de Opções a seguir demonstram como um conjunto de itens de Menu do Aplicativo da Faixa de Opções está associado a um nome de comando e uma ID.

1.  Esta seção mostra as declarações de comando necessárias para um Menu de Aplicativo com comandos básicos, como Novo, Abrir e Salvar.
    ```XML
    <!-- Command declarations for the Application Menu. -->
    <Command Name="cmdFileMenu"
             Symbol="ID_FILE_MENU"
             Id="25000" />
    <!-- Command declaration for most recently used items. -->
    <Command Name="cmdMRUItems"
             Symbol="ID_FILE_MRUITEMS"
             Id="25050"/>
    <!-- Command declarations for Application Menu items. -->
    <Command Name="cmdNew"
             Symbol="ID_FILE_NEW"
             Comment="New"
             Id="25001"
             LabelTitle="&amp;New"/>
    <Command Name="cmdOpen"
             Symbol="ID_FILE_OPEN"
             Comment="Open"
             Id="25002"
             LabelTitle="&amp;&amp;Open"/>
    <Command>
      <Command.Name>cmdSave</Command.Name>
      <Command.Symbol>ID_FILE_SAVE</Command.Symbol>
      <Command.Comment>Save</Command.Comment>
      <Command.Id>25003</Command.Id>
      <Command.LabelTitle>
        <String>
          <String.Content>Label for Save</String.Content>
          <String.Id>59999</String.Id>
          <String.Symbol>strSave</String.Symbol>
        </String>
      </Command.LabelTitle>
      <Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
      <Command.TooltipDescription>Tooltip description for Save Command.</Command.TooltipDescription>
      <Command.Keytip>s1</Command.Keytip>
    </Command>
    <Command Name="cmdPrint"
             Symbol="ID_FILE_PRINT"
             Comment="Save"
             Id="25004"
             LabelTitle="Print" />
    <Command Name="cmdExit"
             Symbol="ID_FILE_EXIT"
             Comment="Exit"
             Id="25005"
             LabelTitle="Exit" />
    ```

    

2.  Esta seção mostra as declarações de Controle associadas.
    ```XML
    <!-- Control declarations for Application Menu items. -->
    <Ribbon.ApplicationMenu>
      <ApplicationMenu CommandName="cmdFileMenu">
        <!-- Most recently used items collection. -->
        <ApplicationMenu.RecentItems>
          <RecentItems CommandName="cmdMRUItems"/>
        </ApplicationMenu.RecentItems>
        <!-- Menu items collection. -->
        <MenuGroup>
          <Button CommandName="cmdNew" />
          <Button CommandName="cmdOpen" />
          <Button CommandName="cmdSave" />
        </MenuGroup>
        <MenuGroup>
          <Button CommandName="cmdPrint" />
          <Button CommandName="cmdExit" />
        </MenuGroup>
      </ApplicationMenu>
    </Ribbon.ApplicationMenu>
    ```

    

Quando a marcação é compilada com a ferramenta UICC (Compilador de Comando da Interface do Usuário), os nomes de comando e as IDs são colocados em um arquivo de header usado pelo aplicativo host da Faixa de Opções.

A seguir está um exemplo de um arquivo de header gerado pelo UICC.


```
// *****************************************************************************
// * This is an automatically generated header file for UI Element definition  *
// * resource symbols and values. Please do not modify manually.               *
// *****************************************************************************

#pragma once

#define cmdFileMenu 25000 
#define cmdNew 22001  /* New */ 
#define cmdNew_LabelTitle_RESID 60005
#define cmdOpen 22002  /* Open */ 
#define cmdOpen_LabelTitle_RESID 60006
#define cmdSave 22003  /* Save */ 
#define cmdSave_LabelTitle_RESID 60007
#define cmdSave_TooltipTitle_RESID 60008
#define cmdSave_TooltipDescription_RESID 60009
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Extensible Application Markup Language (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[Compilando marcação de faixa de opções](windowsribbon-intentcl.md)
</dt> </dl>

 

 