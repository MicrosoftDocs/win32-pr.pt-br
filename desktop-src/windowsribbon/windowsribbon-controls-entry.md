---
title: Biblioteca de controle do Windows Ribbon Framework
description: Os tópicos contidos nesta seção descrevem o conjunto de controles incluídos no Windows Ribbon Framework. Os controles listados aqui são os objetos de interface do usuário em uma faixa de faixas que expõem a funcionalidade do comando.
ms.assetid: bda13e51-7e5f-4600-a6bd-9388bffd6ce2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 840b07bafe0c43cb7ab148a4413657b9722c409b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105786947"
---
# <a name="windows-ribbon-framework-control-library"></a>Biblioteca de controle do Windows Ribbon Framework

Os tópicos contidos nesta seção descrevem o conjunto de controles incluídos no Windows Ribbon Framework. Os controles listados aqui são os objetos de interface do usuário em uma faixa de faixas que expõem a funcionalidade do comando.

-   [Introdução](#introduction)
-   [Os controles](#windows-ribbon-framework-control-library)
    -   [Controles básicos](#basic-controls)
    -   [Controles de contêiner](#container-controls)
    -   [Controles especializados](#specialized-controls)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction"></a>Introdução

A estrutura da faixa de faixas é composta de componentes como [guias](windowsribbon-controls-tab.md) e a [barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md), que funcionam em conjunto para fornecer uma experiência de interface do usuário rica. Individualmente, esses componentes expõem tipos diferentes de comandos para proporcionar aos clientes uma experiência organizada e previsível em aplicativos de faixa de das faixas. Por exemplo, cada guia expõe comandos relacionados à criação e à ação de partes específicas do conteúdo no espaço de trabalho do aplicativo, enquanto o [menu do aplicativo](windowsribbon-controls-applicationmenu.md) expõe a funcionalidade relacionada a um projeto completo, como um documento, imagem ou filme inteiro.

Este tópico fornece uma lista abrangente de controles de faixa de faixas e inclui uma breve descrição de cada controle, com links para uma documentação mais detalhada, quando disponível.

## <a name="the-controls"></a>Os controles

A estrutura da faixa de visão é composta de duas [exibições](windowsribbon-reference-elements-view.md): a exibição [**da faixa**](windowsribbon-element-ribbon.md) de forma e a exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) . Cada exibição pode hospedar vários componentes que atuam como contêineres de apresentação para todos os controles que são renderizados e gerenciados pela estrutura.

A exibição [**da faixa**](windowsribbon-element-ribbon.md) de opções hospeda o elemento [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) , o elemento [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) e a barra de comandos da faixa de opções, enquanto a exibição [**ContextPopup**](windowsribbon-element-contextpopup.md) hospeda um elemento [**ContextMenu**](windowsribbon-element-contextmenu.md) , um elemento [**Minibarra**](windowsribbon-element-minitoolbar.md) ou ambos.

Cada controle de estrutura é diferenciado pela funcionalidade associada ao seu [**tipo de comando**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype).

### <a name="basic-controls"></a>Controles básicos

Os controles básicos consistem em um ou mais botões que podem ser invocados por um único clique do mouse para executar uma ação simples.

> [!Note]  
> O [**controle giratório**](windowsribbon-element-spinner.md) é uma exceção, pois contém um controle de edição.

 

A tabela a seguir lista os controles básicos na estrutura da faixa de opções.



| Control                                                  | Elemento de marcação                                             |
|----------------------------------------------------------|------------------------------------------------------------|
| [Botão](windowsribbon-controls-button.md)              | [**Button**](windowsribbon-element-button.md)             |
| [Caixa de seleção](windowsribbon-controls-checkbox.md)         | [**CheckBox**](windowsribbon-element-checkbox.md)         |
| [Botão ajuda](windowsribbon-controls-helpbutton.md)     | [**HelpButton**](windowsribbon-element-helpbutton.md)     |
| [Controle giratório](windowsribbon-controls-spinner.md)            | [**Controle giratório**](windowsribbon-element-spinner.md)           |
| [Botão de alternância](windowsribbon-controls-togglebutton.md) | [**ToggleButton**](windowsribbon-element-togglebutton.md) |



 

### <a name="container-controls"></a>Controles de contêiner

Os controles de contêiner são compostos por grupos de controles, menus, listas ou coleções de comandos e itens.

A estrutura distingue entre dois tipos de contêineres, estático e dinâmico.

### <a name="static-containers"></a>Contêineres estáticos

Os contêineres estáticos são declarados e preenchidos, juntamente com todos os recursos associados, no arquivo de marcação da faixa de lista. Esses controles não podem ser modificados em tempo de execução.

As vantagens dos controles estáticos incluem o seguinte:

-   Rápida criando protótipos. Os controles estáticos possibilitam a criação rápida de uma simulação de faixa de uma forma semelhante a um design de faixa de forma final que não requer código complicado.
-   Modificações fáceis. A maioria dos elementos, atributos, recursos e layouts de controles estáticos pode ser modificada na marcação.
-   Interface do usuário consistente. Os aplicativos bem projetados fornecem uma interface do usuário consistente e estável que evita alterações em menus e listas em tempo de execução.

A tabela a seguir descreve os controles de contêiner estáticos na estrutura da faixa de opções.



| Control                                                        | Elemento de marcação                                                   |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [Menu do aplicativo](windowsribbon-controls-applicationmenu.md) | [**ApplicationMenu**](windowsribbon-element-applicationmenu.md) |
| [Pop-up de contexto](windowsribbon-controls-contextpopup.md)       | [**ContextPopup**](windowsribbon-element-contextpopup.md)       |
| [Botão suspenso](windowsribbon-controls-dropdownbutton.md)  | [**DropDownButton**](windowsribbon-element-dropdownbutton.md)   |
| [Grupo](windowsribbon-controls-group.md)                      | [**Grupo**](windowsribbon-element-group.md)                     |
| [Grupo de menus](windowsribbon-controls-menugroup.md)             | [**Grupo Backstage**](windowsribbon-element-menugroup.md)             |
| [Botão de divisão](windowsribbon-controls-splitbutton.md)         | [**SplitButton**](windowsribbon-element-splitbutton.md)         |
| [Tab](windowsribbon-controls-tab.md)                          | [**Tab**](windowsribbon-element-tab.md)                         |
| [Grupo de guias](windowsribbon-controls-tabgroup.md)               | [**TabGroup**](windowsribbon-element-tabgroup.md)               |



 

### <a name="dynamic-containers"></a>Contêineres dinâmicos

Os contêineres dinâmicos são declarados no arquivo de marcação da faixa de lista. Eles apresentam um grupo de itens ou comandos que são criados ou modificados em tempo de execução.

Uma subclasse de contêineres dinâmicos, chamadas galerias, é diferenciada por sua implementação da interface [**IUICollection**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection) . Essa interface permite que um controle exponha seu item ou lista de comandos como uma coleção e para dar suporte a atualizações com base na interação do usuário e nas condições de tempo de execução. Para obter mais informações, consulte [trabalhando com galerias](ribbon-controls-galleries.md).

A tabela a seguir lista os controles de contêiner dinâmicos na estrutura da faixa de opções.



| Control                                                               | Elemento de marcação                                                         |
|-----------------------------------------------------------------------|------------------------------------------------------------------------|
| [Caixa de combinação](windowsribbon-controls-combobox.md)                      | [**ComboBox**](windowsribbon-element-combobox.md)                     |
| [Galeria suspensa](windowsribbon-controls-dropdowngallery.md)       | [**DropDownGallery**](windowsribbon-element-dropdowngallery.md)       |
| [Galeria de faixa de bits](windowsribbon-controls-inribbongallery.md)       | [**InRibbonGallery**](windowsribbon-element-inribbongallery.md)       |
| [Barra de ferramentas de acesso rápido](windowsribbon-controls-quickaccesstoolbar.md) | [**QuickAccessToolbar**](windowsribbon-element-quickaccesstoolbar.md) |
| [Itens recentes](windowsribbon-controls-recentitems.md)                | [**RecentItems**](windowsribbon-element-recentitems.md)               |
| [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md) | [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) |



 

### <a name="specialized-controls"></a>Controles especializados

A estrutura da faixa de das faixas contém vários controles especializados para a funcionalidade específica da interface do usuário.

A tabela a seguir lista os controles especializados na estrutura da faixa de opções.



| Control                                                                  | Elemento de marcação                                                           |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [Seletor de cores suspensa](windowsribbon-controls-dropdowncolorpicker.md) | [**DropDownColorPicker**](windowsribbon-element-dropdowncolorpicker.md) |
| [Controle de fonte](windowsribbon-controls-fontcontrol.md)                   | [**FontControl**](windowsribbon-element-fontcontrol.md)                 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Noções básicas sobre comandos e controles](windowsribbon-commandscontrols.md)
</dt> </dl>

 

 