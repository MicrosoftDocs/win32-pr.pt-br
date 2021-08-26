---
title: Trabalhando com galerias
description: A Windows Ribbon fornece aos desenvolvedores um modelo robusto e consistente para gerenciar conteúdo dinâmico em uma variedade de controles baseados em coleção.
ms.assetid: 447039f3-1428-4b6f-94cf-78cf81974041
keywords:
- Windows Faixa de opções, galerias
- Faixa de opções, galerias
- Windows Faixa de opções, controle DropDownGallery
- Faixa de opções, controle DropDownGallery
- Windows Faixa de opções, controle SplitButtonGallery
- Faixa de opções, controle SplitButtonGallery
- Controle DropDownGallery
- Controle SplitButtonGallery
- galerias para Windows faixa de opções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce142c1159d7a7c4129f402716ed7e394ebb4829f043d7c58dd23221b1479720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119933437"
---
# <a name="working-with-galleries"></a>Trabalhando com galerias

A Windows Ribbon fornece aos desenvolvedores um modelo robusto e consistente para gerenciar conteúdo dinâmico em uma variedade de controles baseados em coleção. Ao adaptar e reconfigurar a interface do usuário da Faixa de Opções, esses controles dinâmicos permitem que a estrutura responda à interação do usuário no aplicativo host e na própria Faixa de Opções e forneça a flexibilidade para lidar com vários ambientes de tempo de run time.

-   [Introdução](#introduction)
-   [Galerias](#working-with-galleries)
    -   [Galerias de itens](#item-galleries)
    -   [Galerias de Comandos](#command-galleries)
    -   [Controles da Galeria](#working-with-galleries)
-   [Como implementar uma galeria](#how-to-implement-a-gallery)
    -   [Os componentes básicos](#the-basic-components)
    -   [Declarar os controles na marcação](#declare-the-controls-in-markup)
    -   [Criar um manipulador de comandos](#create-a-command-handler)
    -   [Vincular o manipulador de comandos](#bind-the-command-handler)
    -   [Inicializar uma coleção](#initialize-a-collection)
    -   [Manipular eventos de coleção](#handle-collection-events)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

Essa capacidade da estrutura da Faixa de Opções de se adaptar dinamicamente às condições de tempo de run-time, aos requisitos de aplicativo e à entrada do usuário final realça os recursos avançados da interface do usuário da estrutura e fornece aos desenvolvedores a flexibilidade para atender a uma ampla variedade de necessidades do cliente.

O foco deste guia é descrever os controles de galeria dinâmicos com suporte da estrutura, explicar suas diferenças, discutir quando e onde eles podem ser melhor usados e demonstrar como eles podem ser incorporados em um aplicativo de Faixa de Opções.

## <a name="galleries"></a>Galerias

As galerias são controles de caixa de listagem funcional e graficamente rich. A coleção de itens de uma galeria pode ser organizada por categorias, exibida em layouts flexíveis baseados em colunas e linhas, representadas com imagens e texto e, dependendo do tipo de galeria, dar suporte à visualização ao vivo.

As galerias são funcionalmente diferentes de outros controles de Faixa de Opções dinâmicos pelos seguintes motivos:

-   As galerias implementam a interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) que define os vários métodos para manipular coleções de itens da galeria.
-   As galerias podem ser atualizadas em tempo de operação, com base na atividade que ocorre diretamente na Faixa de Opções, como quando um usuário adiciona um Comando à QAT (Barra de Ferramentas de Acesso Rápido).
-   As galerias podem ser atualizadas em tempo de operação, com base na atividade que ocorre indiretamente do ambiente de tempo de executar, como quando um driver de impressora dá suporte apenas a layouts de página retrato.
-   As galerias podem ser atualizadas em tempo de operação, com base na atividade que ocorre indiretamente no aplicativo host, como quando um usuário seleciona um item em um documento.

A estrutura ribbon expõe dois tipos de galerias: galerias de itens e galerias de comandos.

### <a name="item-galleries"></a>Galerias de itens

As galerias de itens contêm uma coleção baseada em índice de itens relacionados em que cada item é representado por uma imagem, uma cadeia de caracteres ou ambos. O controle é vinculado a um único manipulador de comandos que se baseia no valor de índice identificado pela propriedade [ \_ PKEY \_ SelectedItem da](windowsribbon-reference-properties-uipkey-selecteditem.md) interface do usuário.

As galerias de itens são suportadas com visualização ao vivo, o que significa exibir um resultado de Comando, com base no mouse ou no foco, sem se comprometer ou realmente invocar o comando.

> [!IMPORTANT]
> A estrutura não dá suporte a galerias de itens de hospedagem no Menu do Aplicativo.

 

### <a name="command-galleries"></a>Galerias de Comandos

As galerias de comandos contêm uma coleção de itens distintos e não indexados. Cada item é representado por um único controle vinculado a um manipulador de comandos por meio de uma ID de comando. Assim como os controles autônomos, cada item em uma galeria de comandos encaminha eventos de entrada para um manipulador de comandos associado– a galeria de comandos em si não escuta eventos.

As galerias de comandos não são suportadas com visualização ao vivo.

### <a name="gallery-controls"></a>Controles da Galeria

Há quatro controles da galeria na estrutura da Faixa de Opções: [**DropDownGallery,**](windowsribbon-element-dropdowngallery.md) [**SplitButtonGallery,**](windowsribbon-element-splitbuttongallery.md) [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)e [**ComboBox.**](windowsribbon-element-combobox.md) Todos, exceto **o ComboBox,** podem ser implementados como uma galeria de itens ou uma galeria de comandos.

### <a name="dropdowngallery"></a>DropDownGallery

Um [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) é um botão que exibe uma lista suspenso que contém uma coleção de itens ou comandos mutuamente exclusivos.

A captura de tela a seguir ilustra o controle [galeria](windowsribbon-controls-dropdowngallery.md) de lista Microsoft Paint faixa de opções Windows 7.

![captura de tela de um controle de galeria listada no Microsoft Paint para Windows 7.](images/controls/dropdowngallery.png)

### <a name="splitbuttongallery"></a>SplitButtonGallery

[**Um SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) é um controle composto que expõe um único item padrão ou Comando de sua coleção em um botão primário e exibe outros itens ou comandos em uma lista de lista de listas listadas mutuamente exclusivas que é exibida quando um botão secundário é clicado.

A captura de tela a seguir ilustra o controle [Galeria](windowsribbon-controls-splitbuttongallery.md) de Botões de Divisão de Faixa de Opções Microsoft Paint para Windows 7.

![captura de tela de um controle de galeria de botões divididos no Microsoft Paint para Windows 7.](images/controls/splitbuttongallery.png)

### <a name="inribbongallery"></a>InRibbonGallery

Uma [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) é uma galeria que exibe uma coleção de itens relacionados ou Comandos na Faixa de Opções. Se houver muitos itens na galeria, uma seta de expansão será fornecida para exibir o restante da coleção em um painel expandido.

A captura de tela a seguir ilustra o controle [Galeria](windowsribbon-controls-inribbongallery.md) na Faixa de Opções na Faixa de Opções Microsoft Paint para Windows 7.

![captura de tela de um controle na galeria na faixa de opções na faixa de opções do Microsoft Paint.](images/controls/inribbongallery.png)

### <a name="combobox"></a>ComboBox

Uma [**ComboBox é**](windowsribbon-element-combobox.md) uma caixa de listagem de coluna única que contém uma coleção de itens com um controle estático ou controle de edição e seta para baixo. A parte da caixa de listagem do controle é exibida quando o usuário clica na seta para baixo.

A captura de tela a seguir ilustra um controle [Caixa de Combinação](windowsribbon-controls-combobox.md) da Faixa de Opções Windows Live Movie Maker.

![captura de tela de um controle de caixa de combinação na faixa de opções de pintura da Microsoft.](images/controls/combobox.png)

Como o [**ComboBox**](windowsribbon-element-combobox.md) é exclusivamente uma galeria de itens, ele não dá suporte a itens command. Ele também é o único controle de galeria que não dá suporte a um Espaço de Comando. (Um Espaço de Comando é uma coleção de Comandos que são declarados na marcação e listados na parte inferior de uma galeria de itens ou galeria de comandos.)

O exemplo de código a seguir mostra a marcação necessária para declarar um Espaço de Comando de três botões em [**um DropDownGallery**](windowsribbon-element-dropdowngallery.md).


```C++
<DropDownGallery 
  CommandName="cmdSizeAndColor" 
  TextPosition="Hide" 
  Type="Commands"
  ItemHeight="32"
  ItemWidth="32">
  <DropDownGallery.MenuLayout>
    <FlowMenuLayout Rows="2" Columns="3" Gripper="None"/>
  </DropDownGallery.MenuLayout>
  <Button CommandName="cmdCommandSpace1"/>
  <Button CommandName="cmdCommandSpace2"/>
  <Button CommandName="cmdCommandSpace3"/>
</DropDownGallery>
```



A captura de tela a seguir ilustra o Espaço de Comando de três botões do exemplo de código anterior.

![captura de tela de um espaço de comando de três botões em uma dropdowngallery.](images/markup/gallerysample-commandspace.png)

## <a name="how-to-implement-a-gallery"></a>Como implementar uma galeria

Esta seção discute os detalhes de implementação das galerias da Faixa de Opções e explica como incorporá-las em um aplicativo de Faixa de Opções.

### <a name="the-basic-components"></a>Os componentes básicos

Esta seção descreve o conjunto de propriedades e métodos que formam o backbone do conteúdo dinâmico na estrutura da Faixa de Opções e suportam adicionar, excluir, atualizar e manipular o conteúdo e o layout visual das galerias da Faixa de Opções em tempo de operação.

### <a name="iuicollection"></a>IUICollection

As galerias exigem um conjunto básico de métodos para acessar e manipular os itens individuais em suas coleções.

A interface [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) define esses métodos e a estrutura complementa sua funcionalidade com métodos adicionais definidos na interface [**IUICollection.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) **IUICollection é** implementado pela estrutura para cada declaração da galeria na marcação Faixa de Opções.

Se for necessária uma funcionalidade adicional que não seja fornecida pela interface [**IUICollection,**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) um objeto de coleção personalizado implementado pelo aplicativo host e derivado de [IEnumUnknown](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown) poderá ser substituído pela coleção de estruturas.

### <a name="iuicollectionchangedevent"></a>IUICollectionChangedEvent

Para que um aplicativo responda às alterações em uma coleção da galeria, ele deve implementar a interface [**IUICollectionChangedEvent.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollectionchangedevent) Os aplicativos podem assinar notificações de um objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) por meio do ouvinte de eventos [**IUICollectionChangedEvent::OnChanged.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged)

Quando o aplicativo substitui a coleção da galeria fornecida pela estrutura por uma coleção personalizada, o aplicativo deve implementar a interface [IConnectionPointContainer.](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) Se [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) não for implementado, o aplicativo não poderá notificar a estrutura das alterações na coleção personalizada que exigem atualizações dinâmicas para o controle da galeria.

Nos casos em que [IConnectionPointContainer](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) não é implementado, o controle da galeria pode ser atualizado somente por invalidação por meio de [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) e [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty)ou chamando [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).

### <a name="iuisimplepropertyset"></a>IUISimplePropertySet

Os aplicativos devem implementar IUISimplePropertySet para cada item ou Comando em uma coleção da galeria. No entanto, as propriedades que podem ser solicitadas com [**IUISimplePropertySet::GetValue variam.**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue)

Os itens são definidos e vinculados a uma galeria por meio da chave de propriedade [ \_ PKEY \_ ItemsSource](windowsribbon-reference-properties-uipkey-itemssource.md) da interface do usuário e expõem propriedades com [**um objeto IUICollection.**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection)

As propriedades válidas para itens em galerias de itens ([**UI \_ COMMANDTYPE \_ COLLECTION**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) são descritas na tabela a seguir.

> [!Note]  
> Algumas propriedades de item, como [o rótulo \_ PKEY \_ da](windowsribbon-reference-properties-uipkey-label.md)interface do usuário, podem ser definidas na marcação. Para obter mais detalhes, consulte a [documentação de referência de Chaves](windowsribbon-reference-properties.md) de Propriedade.

 



Control

Propriedades

[**ComboBox**](windowsribbon-element-combobox.md)

[Interface do usuário \_ \_Rótulo PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[**DropDownGallery**](windowsribbon-element-dropdowngallery.md)

[Interface do usuário \_ \_Rótulo PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY, \_ MyImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[**InRibbonGallery**](windowsribbon-element-inribbongallery.md)

[Interface do usuário \_ \_Rótulo PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY, \_ MyImage](windowsribbon-reference-properties-uipkey-itemimage.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md)

[Interface do usuário \_ \_Rótulo PKEY](windowsribbon-reference-properties-uipkey-label.md), [UI \_ PKEY, \_ MyImage](windowsribbon-reference-properties-uipkey-itemimage.md), [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)

[Interface do usuário \_ PKEY \_ SelectedItem](windowsribbon-reference-properties-uipkey-selecteditem.md) é uma propriedade da Galeria de itens.



 

As propriedades de item válidas para galerias de comando ([**interface do usuário de \_ COMMANDTYPE \_**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype)) são descritas na tabela a seguir.



| Control                                                                | Propriedades                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)       | [Interface do usuário \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [interface do usuário \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)       | [Interface do usuário \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [interface do usuário \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md) , [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) |
| [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) | [Interface do usuário \_ PKEY \_ CommandID](windowsribbon-reference-properties-uipkey-commandid.md), [interface do usuário \_ PKEY \_ CommandType](windowsribbon-reference-properties-uipkey-commandtype.md), [UI \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md)  |



 

As categorias são usadas para organizar itens e comandos em galerias. As categorias são definidas e associadas a uma Galeria por meio da chave de propriedade [ \_ \_ categorias de PKEY de interface do usuário](windowsribbon-reference-properties-uipkey-categories.md) e expõem propriedades com um objeto [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) específico à categoria.

As categorias não têm um CommandType e não dão suporte à interação do usuário. Por exemplo, as categorias não podem se tornar SelectedItem em uma galeria de itens e não estão associadas a um comando em uma galeria de comandos. Assim como outras propriedades de item da galeria, as propriedades de categoria, como o [ \_ \_ rótulo PKEY da interface do](windowsribbon-reference-properties-uipkey-label.md) usuário e a [interface do usuário \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) , podem ser recuperadas chamando [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue).

> [!IMPORTANT]
> [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) deve retornar [**a \_ coleção \_ de interface do usuário INVALIDINDEX**](/windows/desktop/windowsribbon/windowsribbon-ui-collection-invalidindex) quando a [interface do usuário \_ PKEY \_ CategoryID](windowsribbon-reference-properties-uipkey-categoryid.md) é solicitada para um item que não tem uma categoria associada.

 

### <a name="declare-the-controls-in-markup"></a>Declarar os controles na marcação

As galerias, como todos os controles de faixa de faixas, devem ser declaradas na marcação. Uma galeria é identificada na marcação como uma galeria de itens ou galeria de comandos e vários detalhes de apresentação são declarados. Ao contrário de outros controles, as galerias exigem somente o controle base ou o contêiner de coleção para serem declarados na marcação. As coleções reais são populadas em tempo de execução. Quando uma galeria é declarada em marcação, o atributo *Type* é usado para especificar se a galeria é uma galeria de itens de uma galeria de comandos.

Há vários atributos de layout opcionais disponíveis para cada um dos controles discutidos aqui. Esses atributos fornecem preferências do desenvolvedor para a estrutura seguir que afetam diretamente como um controle é populado e exibido em uma faixa de opções. As preferências aplicáveis na marcação estão relacionadas aos modelos de exibição e de layout e aos comportamentos discutidos na [personalização de uma faixa de opções por meio de definições de tamanho e políticas de dimensionamento](windowsribbon-templates.md).

Se um controle específico não permitir preferências de layout diretamente na marcação ou se as preferências de layout não forem especificadas, a estrutura definirá as convenções de exibição específicas do controle com base na quantidade de espaço disponível na tela.

Os exemplos a seguir demonstram como incorporar um conjunto de galerias em uma faixa de opções.

### <a name="command-declarations"></a>Declarações de comando

Os comandos devem ser declarados com um atributo *CommandName* que é usado para associar um controle ou conjunto de controles, com o comando.

Um atributo *CommandID* usado para associar um comando a um manipulador de comando quando a marcação é compilada também pode ser especificado aqui. Se nenhuma ID for fornecida, uma será gerada pela estrutura.


```XML
<!-- ComboBox -->
<Command Name="cmdComboBoxGroup"
         Symbol="cmdComboBoxGroup"
         Comment="ComboBox Group"
         LabelTitle="ComboBox"/>
<Command Name="cmdComboBox"
         Symbol="cmdComboBox"
         Comment="ComboBox"
         LabelTitle="ComboBox"/>
```


```XML

<!-- DropDownGallery -->
<Command Name="cmdDropDownGalleryGroup"
         Symbol="cmdDropDownGalleryGroup"
         Comment="DropDownGallery Group"
         LabelTitle="DropDownGallery"/>
<Command Name="cmdDropDownGallery"
         Symbol="cmdDropDownGallery"
         Comment="DropDownGallery"
         LabelTitle="DropDownGallery"/>
```




```XML

<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"
```



```XML

<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"
```



### <a name="control-declarations"></a>Declarações de controle

Esta seção contém exemplos que demonstram a marcação de controle básico necessária para os vários tipos de galeria. Eles mostram como declarar os controles da galeria e associá-los a um comando por meio do atributo *CommandName* .

O exemplo a seguir mostra uma declaração de controle para o [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) em que o atributo *Type* é usado para especificar que esta é uma galeria de comandos.


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



O exemplo a seguir mostra uma declaração de controle para o [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md).


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



O exemplo a seguir mostra uma declaração de controle para o [**InRibbonGallery**](windowsribbon-element-inribbongallery.md).

> [!Note]  
> Como o [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) foi projetado para exibir um subconjunto de sua coleção de itens na faixa de opção sem ativar um menu suspenso, ele fornece vários atributos opcionais que regem seu tamanho e o layout do item na inicialização da faixa de opção. Esses atributos são exclusivos do **InRibbonGallery** e não estão disponíveis nos outros controles dinâmicos.

 


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



O exemplo a seguir mostra uma declaração de controle para a [**ComboBox**](windowsribbon-element-combobox.md).


```XML
<!-- ComboBox -->
<Group CommandName="cmdComboBoxGroup">
  <ComboBox CommandName="cmdComboBox">              
  </ComboBox>
</Group>
```



### <a name="create-a-command-handler"></a>Criar um manipulador de comandos

Para cada comando, a estrutura da faixa de faixas requer um manipulador de comandos correspondente no aplicativo host. Os manipuladores de comandos são implementados pelo aplicativo host da faixa de faixas e são derivados da interface [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .

> [!Note]  
> Vários comandos podem ser associados a um único manipulador de comando.

 

Um manipulador de comandos tem duas finalidades:

-   [**IUICommandHandler:: updateproperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) responde às solicitações de atualização de propriedade. Os valores das propriedades de comando, como [interface do usuário \_ PKEY \_ habilitada](windowsribbon-reference-properties-uipkey-enabled.md) ou [ \_ \_ rótulo de PKEY da interface do usuário](windowsribbon-reference-properties-uipkey-label.md), são definidos por meio de chamadas para [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) ou [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand).
-   [**IUICommandHandler:: execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) responde a executar eventos. Esse método dá suporte aos três Estados de execução a seguir que são especificados pelo parâmetro [**\_ EXECUTIONVERB da interface do usuário**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb) .
    -   O estado de execução é executado ou confirma todos os comandos aos quais o manipulador está associado.
    -   O estado de visualização visualiza todos os comandos aos quais o manipulador está associado. Isso essencialmente executa os comandos sem confirmar o resultado.
    -   O estado CancelPreview cancela qualquer comando visualizado. Isso é necessário para dar suporte à passagem por meio de um menu ou lista e Visualizar sequencialmente e desfazer os resultados conforme necessário.

O exemplo a seguir demonstra um manipulador de comando da galeria.


```C++
/*
 * GALLERY COMMAND HANDLER IMPLEMENTATION
 */
class CGalleryCommandHandler
      : public CComObjectRootEx<CComMultiThreadModel>
      , public IUICommandHandler
{
public:
  BEGIN_COM_MAP(CGalleryCommandHandler)
    COM_INTERFACE_ENTRY(IUICommandHandler)
  END_COM_MAP()

  // Gallery command handler's Execute method
  STDMETHODIMP Execute(UINT nCmdID,
                       UI_EXECUTIONVERB verb, 
                       const PROPERTYKEY* key,
                       const PROPVARIANT* ppropvarValue,
                       IUISimplePropertySet* pCommandExecutionProperties)
  {
    HRESULT hr = S_OK;
        
    // Switch on manner of execution (Execute/Preview/CancelPreview)
    switch (verb)
    {
      case UI_EXECUTIONVERB_EXECUTE:
        if(nCmdID == cmdTextSizeGallery || 
           nCmdID == cmdTextSizeGallery2 || 
           nCmdID == cmdTextSizeGallery3)
        {
          if (pCommandExecutionProperties != NULL)
          {
            CItemProperties *pItem = 
              static_cast<CItemProperties *>(pCommandExecutionProperties);
            g_prevSelection = g_index = pItem->GetIndex();
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
          else
          {
            g_prevSelection = g_index = 0;
            UpdateGallerySelectedItems();
            ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
          }
        }           
        break;
      case UI_EXECUTIONVERB_PREVIEW:
        CItemProperties *pItem = 
          static_cast<CItemProperties *>(pCommandExecutionProperties);
        g_index = pItem->GetIndex();
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
      case UI_EXECUTIONVERB_CANCELPREVIEW:
        g_index = g_prevSelection;
        ::InvalidateRect(g_hWindowFrame, NULL, TRUE);
        break;
    }   
    return hr;
  }

  // Gallery command handler's UpdateProperty method
  STDMETHODIMP UpdateProperty(UINT nCmdID,
                              REFPROPERTYKEY key,
                              const PROPVARIANT* ppropvarCurrentValue,
                              PROPVARIANT* ppropvarNewValue)
  {
    UNREFERENCED_PARAMETER(ppropvarCurrentValue);

    HRESULT hr = E_NOTIMPL;         

    if (key == UI_PKEY_ItemsSource) // Gallery items requested
    {
      if (nCmdID == cmdTextSizeGallery || 
          nCmdID == cmdTextSizeGallery2 || 
          nCmdID == cmdTextSizeGallery3)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = _countof(g_labels);

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->Initialize(i);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
      if (nCmdID == cmdCommandGallery1)
      {
        CComQIPtr<IUICollection> spCollection(ppropvarCurrentValue->punkVal);

        int count = 12;
        int commands[] = {cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2, 
                          cmdButton1, 
                          cmdButton2, 
                          cmdBoolean1, 
                          cmdBoolean2};

        for (int i = 0; i < count; i++)
        {
          CComObject<CItemProperties> * pItem;
          CComObject<CItemProperties>::CreateInstance(&pItem);
                    
          pItem->AddRef();
          pItem->InitializeAsCommand(commands[i]);

          spCollection->Add(pItem);
        }
        return S_OK;
      }
    }        
    else if (key == UI_PKEY_SelectedItem) // Selected item requested
    {           
      hr = UIInitPropertyFromUInt32(UI_PKEY_SelectedItem, g_index, ppropvarNewValue);           
    }
    return hr;
  }
};

```



### <a name="bind-the-command-handler"></a>Associar o manipulador de comandos

Depois de definir um manipulador de comando, o comando deve ser associado ao manipulador.

O exemplo a seguir demonstra como associar um comando da galeria a um manipulador de comandos específico. Nesse caso, os controles [**ComboBox**](windowsribbon-element-combobox.md) e Gallery são associados aos respectivos manipuladores de comandos.


```C++
// Called for each Command in markup. 
// Application will return a Command handler for each Command.
STDMETHOD(OnCreateUICommand)(UINT32 nCmdID,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler** ppCommandHandler) 
{   
  // CommandType for ComboBox and galleries
  if (typeID == UI_COMMANDTYPE_COLLECTION || typeID == UI_COMMANDTYPE_COMMANDCOLLECTION) 
  {
    switch (nCmdID)
    {
      case cmdComboBox:
        CComObject<CComboBoxCommandHandler> * pComboBoxCommandHandler;
        CComObject<CComboBoxCommandHandler>::CreateInstance(&pComboBoxCommandHandler);
        return pComboBoxCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
      default:
        CComObject<CGalleryCommandHandler> * pGalleryCommandHandler;
        CComObject<CGalleryCommandHandler>::CreateInstance(&pGalleryCommandHandler);
        return pGalleryCommandHandler->QueryInterface(IID_PPV_ARGS(ppCommandHandler));
    }
    return E_NOTIMPL; // Command is not implemented, so do not pass a handler back.
  }
}
```



### <a name="initialize-a-collection"></a>Inicializar uma coleção

O exemplo a seguir demonstra uma implementação personalizada de [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) para galerias de item e de comando.

A classe CItemProperties neste exemplo é derivada de [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset). Além do método necessário [**IUISimplePropertySet:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue), a classe CItemProperties implementa um conjunto de funções auxiliares para o rastreamento de inicialização e de índice.


```C++
//
//  PURPOSE:    Implementation of IUISimplePropertySet.
//
//  COMMENTS:
//              Three gallery-specific helper functions included. 
//

class CItemProperties
  : public CComObjectRootEx<CComMultiThreadModel>
  , public IUISimplePropertySet
{
  public:

  // COM map for QueryInterface of IUISimplePropertySet.
  BEGIN_COM_MAP(CItemProperties)
    COM_INTERFACE_ENTRY(IUISimplePropertySet)
  END_COM_MAP()

  // Required method that enables property key values to be 
  // retrieved on gallery collection items.
  STDMETHOD(GetValue)(REFPROPERTYKEY key, PROPVARIANT *ppropvar)
  {
    HRESULT hr;

    // No category is associated with this item.
    if (key == UI_PKEY_CategoryId)
    {
      return UIInitiPropertyFromUInt32(UI_PKEY_CategoryId, 
                                       UI_COLLECTION_INVALIDINDEX, 
                                       pprovar);
    }

    // A Command gallery.
    // _isCommandGallery is set on initialization.
    if (_isCommandGallery)
    {           
      if(key == UI_PKEY_CommandId && _isCommandGallery)
      {
        // Return a pointer to the CommandId of the item.
        return InitPropVariantFromUInt32(_cmdID, ppropvar);
      }         
    }
    // An item gallery.
    else
    {
      if (key == UI_PKEY_Label)
      {
        // Return a pointer to the item label string.
        return UIInitPropertyFromString(UI_PKEY_Label, ppropvar);
      }
      else if(key == UI_PKEY_ItemImage)
      {
        // Return a pointer to the item image.
        return UIInitPropertyFromImage(UI_PKEY_ItemImage, ppropvar);
      }         
    }
    return E_NOTIMPL;
  }

  // Initialize an item in an item gallery collection at the specified index.
  void Initialize(int index)
  {
    _index = index;
    _cmdID = 0;
    _isCommandGallery = false;
  }

  // Initialize a Command in a Command gallery.
  void InitializeAsCommand(__in UINT cmdID)
  {
    _index = 0;
    _cmdID = cmdID;
    _isCommandGallery = true;
  }

  // Gets the index of the selected item in an item gallery.
  int GetIndex()
  {
    return _index;
  }

private:
  int _index;
  int _cmdID;
  bool _isCommandGallery;   
};
```



### <a name="handle-collection-events"></a>Manipular eventos de coleta

O exemplo a seguir demonstra uma implementação de IUICollectionChangedEvent.


```C++
class CQATChangedEvent
  : public CComObjectRootEx<CComSingleThreadModel>
  , public IUICollectionChangedEvent
{
  public:

  HRESULT FinalConstruct()
  {
    _pSite = NULL;
    return S_OK;
  }

  void Initialize(__in CQATSite* pSite)
  {
    if (pSite != NULL)
    {
      _pSite = pSite;
    }
  }

  void Uninitialize()
  {
    _pSite = NULL;
  }

  BEGIN_COM_MAP(CQATChangedEvent)
    COM_INTERFACE_ENTRY(IUICollectionChangedEvent)
  END_COM_MAP()

  // IUICollectionChangedEvent interface
  STDMETHOD(OnChanged)(UI_COLLECTIONCHANGE action, 
                       UINT32 oldIndex, 
                       IUnknown *pOldItem, 
                       UINT32 newIndex, 
                       IUnknown *pNewItem)
  {
    if (_pSite)
    {
      _pSite->OnCollectionChanged(action, oldIndex, pOldItem, newIndex, pNewItem);
    }
    return S_OK;
  }

  protected:
  virtual ~CQATChangedEvent(){}

  private:
  CQATSite* _pSite; // Weak ref to avoid circular refcounts
};

HRESULT CQATHandler::EnsureCollectionEventListener(__in IUICollection* pUICollection)
{
  // Check if listener already exists.
  if (_spQATChangedEvent)
  {
    return S_OK;
  }

  HRESULT hr = E_FAIL;

  // Create an IUICollectionChangedEvent listener.
  hr = CreateInstanceWithRefCountOne(&_spQATChangedEvent);
    
  if (SUCCEEDED(hr))
  {
    CComPtr<IUnknown> spUnknown;
    _spQATChangedEvent->QueryInterface(IID_PPV_ARGS(&spUnknown));

    // Create a connection between the collection connection point and the sink.
    AtlAdvise(pUICollection, spUnknown, __uuidof(IUICollectionChangedEvent), &_dwCookie);
    _spQATChangedEvent->Initialize(this);
  }
  return hr;
}

HRESULT CQATHandler::OnCollectionChanged(
             UI_COLLECTIONCHANGE action, 
          UINT32 oldIndex, 
             IUnknown *pOldItem, 
          UINT32 newIndex, 
          IUnknown *pNewItem)
{
    UNREFERENCED_PARAMETER(oldIndex);
    UNREFERENCED_PARAMETER(newIndex);

    switch (action)
    {
      case UI_COLLECTIONCHANGE_INSERT:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pNewItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Added to QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
      case UI_COLLECTIONCHANGE_REMOVE:
      {
        CComQIPtr<IUISimplePropertySet> spProperties(pOldItem);
                
        PROPVARIANT var;
        if (SUCCEEDED(spProperties->GetValue(UI_PKEY_CommandId, &var)))
        {
          UINT tcid;
          if (SUCCEEDED(UIPropertyToUInt32(UI_PKEY_CommandId, var, &tcid)))
          {
            FireETWEvent(tcid, L"Removed from QAT");
            PropVariantClear(&var);
          }
        }
      }
      break;
    default:
  }
  return S_OK;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades da coleção](windowsribbon-reference-properties-collection.md)
</dt> <dt>

[Criando um aplicativo de faixa de faixas](windowsribbon-stepbystep.md)
</dt> <dt>

[Noções básicas sobre comandos e controles](windowsribbon-commandscontrols.md)
</dt> <dt>

[Diretrizes de experiência do usuário da faixa de das](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[Processo de design da faixa de das](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> <dt>

[Exemplo de galeria](windowsribbon-gallerysample.md)
</dt> </dl>

 

 