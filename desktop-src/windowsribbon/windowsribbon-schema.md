---
title: Declarando comandos e controles com marcação de faixa de medida
description: O Windows Ribbon Framework usa uma linguagem de marcação baseada em linguagem XAML (XAML) para implementar de forma declarativa a aparência de um aplicativo da faixa de faixas.
ms.assetid: 76bacfb3-ecaf-47b3-be97-afa5e7e52330
keywords:
- Faixa de medida do Windows, estrutura de marcação
- Faixa de faixas, estrutura de marcação
- Faixa de-se do Windows, separando a apresentação da lógica de comando
- Faixa de faixas, separando a apresentação da lógica de comando
- Faixa de, componentes do Windows
- Faixa de, componentes
- sistema de comandos para Windows Ribbon
- controles para a faixa de faixas do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97c5c193332ce217709c825a58f0ae546c03c9c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366436"
---
# <a name="declaring-commands-and-controls-with-ribbon-markup"></a>Declarando comandos e controles com marcação de faixa de medida

O Windows Ribbon Framework usa uma linguagem de marcação baseada em linguagem XAML (XAML) para implementar de forma declarativa a aparência de um aplicativo da faixa de faixas.

-   [Separando apresentação da lógica de comando](#separating-presentation-from-command-logic)
-   [Estrutura de marcação](#markup-structure)
-   [Componentes da faixa de das](#ribbon-components)
-   [Tópicos relacionados](#related-topics)

## <a name="separating-presentation-from-command-logic"></a>Separando apresentação da lógica de comando

A separação dos atributos de apresentação e visuais da lógica de comando na estrutura da faixa de faixas é realizada por meio de duas plataformas de desenvolvimento diferentes, mas dependentes. Layouts de controle, comportamentos de dimensionamento, declarações de comando e especificações de recursos são o domínio de tempo de design de uma sintaxe de marcação declarativa com base na especificação de [linguagem XAML (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf) . Funcionalidade de nível baixo, ganchos de aplicativo e manipuladores de comando são definidos em implementações de interface com base em Component Object Model (COM).

Essa separação de apresentação e lógica oferece os seguintes benefícios:

-   Um ciclo de desenvolvimento de aplicativos mais eficiente que permite que desenvolvedores e designers da interface do usuário implementem a GUI do aplicativo da faixa de faixas independentemente da funcionalidade do aplicativo principal. Essa funcionalidade básica pode ser deixada para os desenvolvedores de software dedicados.
-   Manutenção menos dispendiosa porque as alterações na GUI são possíveis sem alterações na funcionalidade básica (e vice-versa).
-   Especificação simples de recursos de cadeia de caracteres e imagem por meio de marcação.
-   Facilidade de protótipos.

## <a name="markup-structure"></a>Estrutura de marcação

Existem duas ramificações distintas dentro da estrutura da marcação da estrutura da faixa de faixas.

A primeira ramificação contém um manifesto de declarações de comando e recurso (cadeias de caracteres e imagens). Cada entrada de comando é usada pela estrutura para associar um controle da faixa de faixas, por meio de uma ID de comando, a um manipulador de comandos definido no código do aplicativo.

A segunda ramificação contém as declarações de controle reais. Cada controle é associado a um comando por meio de um atributo *CommandName* que é mapeado para um atributo de *nome* especificado em cada declaração de comando.

## <a name="ribbon-components"></a>Componentes da faixa de das

A funcionalidade da interface do usuário do Framework é exposta por meio de [exibições](windowsribbon-reference-elements-view.md). Uma exibição é essencialmente um contêiner, como a [**faixa**](windowsribbon-element-ribbon.md) de e- [**ContextPopup**](windowsribbon-element-contextpopup.md), que é usada para apresentar os controles de estrutura e os comandos aos quais eles estão vinculados.

O modo de exibição da [**faixa**](windowsribbon-element-ribbon.md) de visão é composto por vários componentes que incluem um [menu de aplicativo](windowsribbon-controls-applicationmenu.md), a barra de [ferramentas de acesso rápido (qat)](windowsribbon-controls-quickaccesstoolbar.md) para exibir comandos comumente usados da interface do usuário da faixa de [guia, guias](windowsribbon-controls-tab.md) de núcleo e contextual que contêm [grupos](windowsribbon-controls-group.md) de controles e o sistema de menus de contexto avançado do [**ContextPopup**](windowsribbon-element-contextpopup.md).

Todos os componentes da faixa de faixas são declarados em um arquivo de marcação autônomo que:

-   Especifica as propriedades básicas para cada elemento.
-   Mostra as relações hierárquicas claramente.
-   Fornece preferências de layout e dicas de dimensionamento. Para obter mais informações sobre modelos de layout da faixa de faixas, consulte [Personalizando uma faixa de opção por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md).
-   Fornece uma maneira de definir recursos como imagens e rótulos. Para obter mais informações sobre recursos de imagem, consulte [especificando recursos de imagem da faixa de Ribbon](windowsribbon-imageformats.md).

Os dois exemplos de marcação da faixa de opções a seguir demonstram como um conjunto de itens de menu do aplicativo da faixa de opções é associado a um nome de comando e ID.

1.  Esta seção mostra as declarações de comando necessárias para um menu de aplicativo com comandos básicos, como novo, abrir e salvar.
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

    

2.  Esta seção mostra as declarações de controle associadas.
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

    

Quando a marcação é compilada com a ferramenta UICC (compilador de comando de interface do usuário), os nomes de comando e as IDs são colocados em um arquivo de cabeçalho usado pelo aplicativo host da faixa de faixas.

Veja a seguir um exemplo de um arquivo de cabeçalho gerado pelo UICC.


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

[Linguagem XAML (XAML)](/dotnet/framework/wpf/advanced/xaml-in-wpf)
</dt> <dt>

[Compilando marcação da faixa de medida](windowsribbon-intentcl.md)
</dt> </dl>

 

 