---
title: Elemento SplitButtonGallery
description: Representa um controle da Galeria de botões de divisão com um menu suspenso baseado na galeria.
ms.assetid: 65b6af50-6d9a-4285-b2d9-26dfb904d0b8
keywords:
- elemento SplitButtonGallery da faixa de Windows
topic_type:
- apiref
api_name:
- SplitButtonGallery
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c28c2f87a1d8fb165f02ad71c96b38bcbb381bb3590bd9bff98b3feb364044bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117850806"
---
# <a name="splitbuttongallery-element"></a>Elemento SplitButtonGallery

Representa um controle da [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md) com um menu suspenso baseado na galeria.

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
<td>Válido somente se o <a href="windowsribbon-element-menugroup.md"><strong>MyMenu</strong></a> for o elemento pai.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Uma cadeia de caracteres que contém uma lista de inteiros separados por vírgulas entre 0 e 31.<br/> O espaço em branco é válido e ignorado.<br/> Comprimento máximo: 250 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>CommandName</strong><br/></td>
<td>xs: positiveInteger ou xs: String<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: positiveInteger ou xs: String)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive, ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo no documento XML da faixa de faixas. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
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
<tr class="even">
<td><strong>ItemHeight</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd> O padrão é -1. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>@ Width</strong><br/></td>
<td>xs:integer<br/></td>
<td>Não<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: Integer)<br/> </dt> <dd> O padrão é -1. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TextPosition</strong><br/></td>
<td>Textpositiontype<br/></td>
<td>Não<br/></td>
<td>Restrito a um dos seguintes valores:<br/> <br/>
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



| Elemento                                                                                                 | Descrição                                        |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| [**Botão**](windowsribbon-element-button.md)<br/>                                               | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**Verificação**](windowsribbon-element-checkbox.md)<br/>                                           | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**SplitButton**](windowsribbon-element-splitbutton.md)<br/>                                     | Pode ocorrer uma ou mais vezes<br/> <br/> |
| [**SplitButtonGallery.MenuGroups**](windowsribbon-element-splitbuttongallery-menugroups.md)<br/> | Deve ocorrer exatamente uma vez<br/> <br/>     |
| [**SplitButtonGallery.MenuLayout**](windowsribbon-element-splitbuttongallery-menulayout.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/>      |
| [**ToggleButton**](windowsribbon-element-togglebutton.md)<br/>                                   | Pode ocorrer uma ou mais vezes<br/> <br/> |



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
<td><a href="windowsribbon-element-controlgroup.md"><strong>Controlador de controle</strong></a><br/></td>

</tr>
<tr class="even">
<td><a href="windowsribbon-element-group.md"><strong>Grupo</strong></a><br/></td>

</tr>
<tr class="odd">
<td><a href="windowsribbon-element-menugroup.md"><strong>Grupo Backstage</strong></a><br/></td>
<td>Quando contido em um <a href="windowsribbon-element-applicationmenu.md"><strong>ApplicationMenu</strong></a>. Esse elemento só tem suporte no primeiro nível e não deve ter nenhum elemento filho.<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="windowsribbon-element-quickaccesstoolbar-applicationdefaults.md"><strong>QuickAccessToolbar.ApplicationDefaults</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Windows 8 e mais recente.
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

Pode ocorrer uma ou mais vezes para cada elemento [**Control**](windowsribbon-element-controlgroup.md), [**Group**](windowsribbon-element-group.md), [**menu**](windowsribbon-element-menugroup.md)ou [**SplitButton**](windowsribbon-element-splitbutton.md) .

O **SplitButtonGallery** dá suporte a [modos de aplicativo](ribbon-applicationmodes.md).

[Interface do usuário \_ PKEY \_ boolianvalue](windowsribbon-reference-properties-uipkey-booleanvalue.md) é usado por um aplicativo para consultar o estado de alternância para o controle de botão de um **SplitButtonGallery**.

a captura de tela a seguir ilustra o controle da [galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md) da faixa de opções no Microsoft Paint para Windows 7.

![captura de tela de um controle de galeria de botões de divisão no Microsoft Paint para Windows 7.](images/controls/splitbuttongallery.png)

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para a [Galeria de botões de divisão](windowsribbon-controls-splitbuttongallery.md).

Esta seção de código mostra as declarações de comando **SplitButtonGallery** , com um [**grupo**](windowsribbon-element-group.md) associado que funciona como o contêiner pai para o elemento **SplitButtonGallery** .


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



Esta seção de código mostra as declarações de controle **SplitButtonGallery** .


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

 

