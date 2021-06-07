---
title: Elemento DropDownGallery
description: Representa um controle Drop-Down Galeria com um menu baseado na galeria.
ms.assetid: fee6b3ad-fc84-49da-97da-2d53ff4dd0d8
keywords:
- Faixa de Opções do Windows do elemento DropDownGallery
topic_type:
- apiref
api_name:
- DropDownGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befe0624dfef5910625a0aa067f3ad8cd9882ca2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443417"
---
# <a name="dropdowngallery-element"></a>Elemento DropDownGallery

Representa um [controle galeria de menu](windowsribbon-controls-dropdowngallery.md) suspenso com um menu baseado na galeria.

## <a name="usage"></a>Uso

``` syntax
<DropDownGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</DropDownGallery>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Type</th>
<th>Obrigatório</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>ApplicationModes</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Válido somente se <a href="windowsribbon-element-menugroup.md"><strong>MenuGroup</strong></a> for o elemento pai.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Uma cadeia de caracteres que contém uma lista separada por vírgulas de inteiros entre 0 e 31.<br/> O espaço em branco é válido e ignorado.<br/> Comprimento máximo: 250 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger ou xs:string<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo dentro do documento XML da Faixa de Opções. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>HasLargeItems</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Determina se o recurso de imagem grande ou pequeno do Comando é exibido no controle da galeria. <br/>
<blockquote>
[!Note]<br />
Aplica-se somente a galerias em que o valor do <em>atributo Type</em> é igual a <code>Command</code> .
</blockquote>
<br/> Restrito a um dos seguintes valores (0 e 1 não são válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Padrão. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Itemheight</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> O padrão é -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Itemwidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> O padrão é -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>TextPositionType<br/></td>
<td>Não<br/></td>
<td>Restrito a um dos seguintes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Inferior)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Ocultar)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Esquerda)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Sobreposição)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Direita)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Superior)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Tipo</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Restrito a um dos seguintes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> (Itens)<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> (Comandos)<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                           | Descrição                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Botão**](windowsribbon-element-button.md)<br/>                                         | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**Checkbox**](windowsribbon-element-checkbox.md)<br/>                                     | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**DropDownGallery.MenuGroups**](windowsribbon-element-dropdowngallery-menugroups.md)<br/> | Deve ocorrer exatamente uma vez<br/> <br/>     |
| [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/>      |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                               | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                             | Pode ocorrer uma ou mais vezes<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="windowsribbon-element-controlgroup.md"><strong>ControlGroup</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Grupo</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-menugroup.md"><strong>Menugroup</strong></a><br/></td>
<td>Quando contido em um <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu.</strong></a> Esse elemento só tem suporte no primeiro nível e não deve ter elementos filho.<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 e mais novos.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="windowsribbon-element-splitbutton.md"><strong>SplitButton</strong></a><br/></td>

</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer uma ou mais vezes para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**DropDownButton**](windowsribbon-element-dropdownbutton.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)ou [**SplitButton.**](windowsribbon-element-splitbutton.md)

**DropDownGallery dá suporte** [a modos de aplicativo](ribbon-applicationmodes.md).

A captura de tela a seguir ilustra o controle [galeria](windowsribbon-controls-dropdowngallery.md) de lista de opções no Microsoft Paint para Windows 7.

![captura de tela de um controle de galeria listada no Microsoft Paint para Windows 7.](images/controls/dropdowngallery.png)

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para **o DropDownGallery**.

Esta seção de código mostra as declarações de Comando **DropDownGallery,** com um Grupo associado que atua como o contêiner pai para o **elemento DropDownGallery.** [](windowsribbon-element-group.md)


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



Esta seção de código mostra as **declarações de controle DropDownGallery.**


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



## <a name="element-information"></a>Informações do elemento

* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Não



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Controle da Galeria De lista listada**](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[Trabalhando com galerias](ribbon-controls-galleries.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[Exemplo da Galeria](windowsribbon-gallerysample.md)
</dt> </dl>

 

