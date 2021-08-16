---
title: Elemento InRibbonGallery
description: Representa a Galeria de In-Ribbon, um controle baseado na galeria que expõe um subconjunto padrão de itens diretamente na faixa de bits. Todos os itens restantes são exibidos quando um botão de menu suspenso é clicado.
ms.assetid: 07d035e2-e6db-49fa-b786-a37cbceb58f6
keywords:
- elemento InRibbonGallery da faixa de Windows
topic_type:
- apiref
api_name:
- InRibbonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1156c7a3b625496b0a4d50b750a3db5cda51a6b77745aaf26d4282de1be3443d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850816"
---
# <a name="inribbongallery-element"></a>Elemento InRibbonGallery

Representa a [Galeria na faixa de faixas](windowsribbon-controls-inribbongallery.md), um controle baseado na galeria que expõe um subconjunto padrão de itens diretamente na faixa de bits. Todos os itens restantes são exibidos quando um botão de menu suspenso é clicado.

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
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveInteger ou xs: String<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo no documento XML da faixa de faixas. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>HasLargeItems</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Determina se o recurso de imagem grande ou pequena do comando é exibido no controle galeria. <br/>
<blockquote>
[!Note]<br />
Aplica-se somente a galerias em que o valor do atributo <em>Type</em> é igual a <code>Command</code> .
</blockquote>
<br/> Restrito a um dos valores a seguir (0 e 1 não são válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd> Padrão. <br/> </dd> <dt><span></span><span></span><strong></strong> for<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ItemHeight</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Junto com o @ <em>Width</em>, determina o tamanho da imagem do item que é exibido no controle da galeria. <br/>
<blockquote>
[!Note]<br />
Aplica-se somente a galerias em que o valor do atributo de <em>tipo</em> é igual a <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd> O padrão é -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>@ Width</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Junto com <em>ItemHeight</em>, determina o tamanho da imagem do item que é exibida no controle da galeria. <br/>
<blockquote>
[!Note]<br />
Aplica-se somente a galerias em que o valor do atributo de <em>tipo</em> é igual a <code>Item</code>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd> O padrão é -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxColumns</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Especifica o número máximo de colunas que o <strong>InRibbonGallery</strong> exibe, por exemplo, na lista suspensa layout de grupo <em>grande</em> .<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MaxColumnsMedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Especifica o número máximo de colunas que o <strong>InRibbonGallery</strong> exibe no layout de grupo <em>médio</em> , antes de alternar para o layout <em>grande</em> . <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaxRows</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Especifica o número máximo de linhas para o layout dos itens <strong>InRibbonGallery</strong> . <br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd> O padrão é 1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinColumnsLarge</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Especifica o número mínimo de colunas que o <strong>InRibbonGallery</strong> exibe no layout de grupo <em>grande</em> , antes de passar para <em>médio</em>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MinColumnsMedium</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td>Especifica o número mínimo de colunas que o <strong>InRibbonGallery</strong> exibe no layout de grupo <em>médio</em> , antes de mudar para <em>pequeno</em>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>Textpositiontype<br/></td>
<td>Não<br/></td>
<td>Especifica onde o rótulo do item é exibido, em relação à imagem. <br/> Restrito a um dos seguintes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> Resultado<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Exibe<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Mantida<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Post<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Adequada<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Melhor<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Tipo</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Restrito a um dos seguintes valores:<br/> <br/>
<dt><span></span><span></span><strong></strong> Los<br/> </dt> <dd></dd> <dt><span></span><span></span><strong></strong> Comandos<br/> </dt> <dd></dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                           | Descrição                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Verificação**](windowsribbon-element-checkbox.md)<br/>                                     | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**InRibbonGallery.MenuGroups**](windowsribbon-element-inribbongallery-menugroups.md)<br/> | Deve ocorrer exatamente uma vez<br/> <br/>     |
| [**InRibbonGallery.MenuLayout**](windowsribbon-element-inribbongallery-menulayout.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/>      |
| [**Botão**](windowsribbon-element-button.md)<br/>                                       | Pode ocorrer uma ou mais vezes<br/> <br/> |
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
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 e mais novos.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**elemento ControlGroup**](windowsribbon-element-controlgroup.md) [**ou Group.**](windowsribbon-element-group.md)

A captura de tela a seguir ilustra o controle [Galeria](windowsribbon-controls-inribbongallery.md) na Faixa de Opções na Faixa de Opções Microsoft Paint para Windows 7.

![captura de tela de um controle na galeria na faixa de opções na faixa de opções do Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para uma [Galeria na Faixa de Opções](windowsribbon-controls-inribbongallery.md).

Esta seção de código mostra as declarações de Comando **InRibbonGallery,** com um Grupo associado que atua como o contêiner pai para o elemento **InRibbonGallery.** [](windowsribbon-element-group.md)


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



Esta seção de código mostra as **declarações de controle InRibbonGallery.**


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


* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Não



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle na Galeria na Faixa de Opções](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[Trabalhando com galerias](ribbon-controls-galleries.md)
</dt> <dt>

[Exemplo da Galeria](windowsribbon-gallerysample.md)
</dt> </dl>

 

 





