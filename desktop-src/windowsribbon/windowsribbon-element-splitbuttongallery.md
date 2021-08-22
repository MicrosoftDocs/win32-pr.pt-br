---
title: Elemento SplitButtonGallery
description: Representa um controle Dividir Galeria de Botões com um menu suspenso baseado em galeria.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- Elemento SplitButtonGallery Windows Ribbon
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c2f954d7b96d3ec2304cd63cd689241a46384fda
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626732"
---
# <a name="splitbuttongallery-element"></a>Elemento SplitButtonGallery

Representa um [controle Dividir Galeria de](windowsribbon-controls-splitbuttongallery.md) Botões com um menu suspenso baseado em galeria.

## <a name="usage"></a>Uso

``` syntax
<SplitButtonGallery
  ApplicationModes = "xs:string"
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</SplitButtonGallery>
```

## <a name="attributes"></a>Atributos



<table>
<colgroup>
<col  />
<col  />
<col  />
<col  />
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



| Elemento                                                                                                 | Descrição                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Botão**](windowsribbon-element-button.md)<br/>                                               | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**Checkbox**](windowsribbon-element-checkbox.md)<br/>                                           | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                     | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | Deve ocorrer exatamente uma vez<br/> <br/>     |
| [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/>      |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                                   | Pode ocorrer uma ou mais vezes<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



<table>
<colgroup>
<col  />
<col  />
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

Pode ocorrer uma ou mais vezes para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**MenuGroup**](windowsribbon-element-menugroup.md)ou [**SplitButton.**](windowsribbon-element-splitbutton.md)

**SplitButtonGallery dá suporte** [a modos de aplicativo](ribbon-applicationmodes.md).

[Interface do usuário \_ PKEY \_ BooleanValue](windowsribbon-reference-properties-uipkey-booleanvalue.md) é usado por um aplicativo para consultar o estado de alternância para o controle de botão de **um SplitButtonGallery**.

A captura de tela a seguir ilustra o controle [Galeria](windowsribbon-controls-splitbuttongallery.md) de Botões de Divisão de Faixa de Opções Microsoft Paint para Windows 7.

![captura de tela de um controle de galeria de botões divididos no Microsoft Paint para Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para a Galeria [de Botões divididos.](windowsribbon-controls-splitbuttongallery.md)

Esta seção de código mostra as declarações de Comando **SplitButtonGallery,** com um Grupo associado que funciona como o contêiner pai para o elemento **SplitButtonGallery.** [](windowsribbon-element-group.md)


```XML
<!-- SplitButtonGallery -->
<Command Name="cmdSplitButtonGalleryGroup"
         Symbol="cmdSplitButtonGalleryGroup"
         Comment="SplitButtonGallery Group"
         LabelTitle="SplitButtonGallery"/>
<Command Name="cmdSplitButtonGallery"
         Symbol="cmdSplitButtonGallery"
         Comment="SplitButtonGallery"
         LabelTitle="SplitButtonGallery"/>
```



Esta seção de código mostra as declarações **de controle SplitButtonGallery.**


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



## <a name="element-information"></a>Informações do elemento


- **Sistema mínimo com suporte:** Windows 7 
- **Pode estar vazio:** Não



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle Dividir Galeria de Botões](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[Trabalhando com galerias](ribbon-controls-galleries.md)
</dt> <dt>

[**SetModes**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setmodes)
</dt> <dt>

[Exemplo da Galeria](windowsribbon-gallerysample.md)
</dt> </dl>

 

