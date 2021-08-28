---
title: Elemento InRibbonGallery
description: Representa a In-Ribbon, um controle baseado em galeria que expõe um subconjunto padrão de itens diretamente na Faixa de Opções. Todos os itens restantes são exibidos quando um botão de menu suspenso é clicado.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- Elemento InRibbonGallery Windows Ribbon
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b1a1d992a9a9ad000a3a6e658b513bf8246657dd
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625132"
---
# <a name="inribbongallery-element"></a>Elemento InRibbonGallery

Representa a [Galeria na Faixa de Opções](windowsribbon-controls-inribbongallery.md), um controle baseado em galeria que expõe um subconjunto padrão de itens diretamente na Faixa de Opções. Todos os itens restantes são exibidos quando um botão de menu suspenso é clicado.

## <a name="usage"></a>Uso

``` syntax
<InRibbonGallery
  CommandName = "xs:positiveInteger or xs:string"
  HasLargeItems = "Boolean"
  ItemHeight = "xs:integer"
  ItemWidth = "xs:integer"
  MinColumnsLarge = "xs:integer"
  MaxColumnsMedium = "xs:integer"
  MinColumnsMedium = "xs:integer"
  MaxColumns = "xs:integer"
  MaxRows = "xs:integer"
  TextPosition = "TextPositionType"
  Type = "xs:string">
  child elements
</InRibbonGallery>
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
<td><strong>CommandName</strong><br/></td>
<td>xs:positiveInteger ou xs:string<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo dentro do documento XML da Faixa de Opções. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
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
<tr class="odd">
<td><strong>Itemheight</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Junto com <em>ItemWidth</em>, determina o tamanho da imagem do item que é exibida no controle da galeria. <br/>
<blockquote>
[!Note]<br />
Aplica-se somente a galerias em que o valor do <em>atributo Type</em> é igual a <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> O padrão é -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Itemwidth</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Junto com <em>ItemHeight</em>, determina o tamanho da imagem do item que é exibida no controle da galeria. <br/>
<blockquote>
[!Note]<br />
Aplica-se somente a galerias em que o valor do <em>atributo Type</em> é igual a <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> O padrão é -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxColumns</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Especifica o número máximo de colunas que a <strong>InRibbonGallery</strong> <em></em> exibe, por exemplo, na lista de layouts de grupo grande.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MaxColumnsMedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Especifica o número máximo de colunas que a <strong>InRibbonGallery</strong> exibe no layout do grupo Médio, antes de alternar para <em>Layout Grande.</em> <em></em> <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxRows</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Especifica o número máximo de linhas para o layout de <strong>itens InRibbonGallery.</strong> <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd> O padrão é 1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinColumnsLarge</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Especifica o número mínimo de colunas que a <strong>InRibbonGallery</strong> exibe no layout <em>do</em> grupo Grande, antes de alternar para <em>Médio.</em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MinColumnsMedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Especifica o número mínimo de colunas que a <strong>InRibbonGallery</strong> exibe no layout do grupo Médio, antes de alternar para <em>Pequeno.</em> <em></em><br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>TextPositionType<br/></td>
<td>Não<br/></td>
<td>Especifica onde o rótulo do item é exibido, em relação à imagem. <br/> Restrito a um dos seguintes valores:<br/> <br/>
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
| [**Checkbox**](windowsribbon-element-checkbox.md)<br/>                                     | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/> | Deve ocorrer exatamente uma vez<br/> <br/>     |
| [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/>      |
| [**Botão**](windowsribbon-element-button.md)<br/>                                       | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                               | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                             | Pode ocorrer uma ou mais vezes<br/> <br/> |



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
<td><a href="windowsribbon-element-controlgroup.md"><strong>Controlador de controle</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Grupo</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 e mais recente.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada elemento [**Control**](windowsribbon-element-controlgroup.md) ou [**Group**](windowsribbon-element-group.md) .

a captura de tela a seguir ilustra o controle da [galeria de faixa de](windowsribbon-controls-inribbongallery.md) opções na Microsoft Paint para Windows 7.

![captura de tela de um controle da galeria na faixa de faixas na faixa de bits do Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para uma [Galeria na faixa de](windowsribbon-controls-inribbongallery.md)opções.

Esta seção de código mostra as declarações de comando **InRibbonGallery** , com um [**grupo**](windowsribbon-element-group.md) associado que atua como o contêiner pai para o elemento **InRibbonGallery** .


```XML
<!-- InRibbonGallery -->
<Command Name="cmdInRibbonGalleryGroup"
         Symbol="cmdInRibbonGalleryGroup"
         Comment="InRibbonGallery Group"
         LabelTitle="InRibbonGallery"/>
<Command Name="cmdInRibbonGallery"
         Symbol="cmdInRibbonGallery"
         Comment="InRibbonGallery"
         LabelTitle="InRibbonGallery"/>
```



Esta seção de código mostra as declarações de controle **InRibbonGallery** .


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



## <a name="element-information"></a>Informações do elemento


* **sistema mínimo com suporte**: Windows 7
* **Pode estar vazio**: não



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle da Galeria de faixa de bits](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Trabalhando com galerias](ribbon-controls-galleries.md)
</dt> <dt>

[Exemplo de galeria](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





