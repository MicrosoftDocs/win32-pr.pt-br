---
title: Elemento FontControl
description: Representa um Controle de Fonte, que é um contêiner especializado de controles individuais dedicados à manipulação de fontes.
ms.assetid: 98eddab5-28cb-4b9d-a788-ee28dd6055b1
keywords:
- Faixa de Opções do Windows do elemento FontControl
topic_type:
- apiref
api_name:
- FontControl
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 42c9d900c2af4f7f8ba26f5ac8dbbdc0d055668d
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443397"
---
# <a name="fontcontrol-element"></a>Elemento FontControl

Representa um [Controle de Fonte](windowsribbon-controls-fontcontrol.md), que é um contêiner especializado de controles individuais dedicados à manipulação de fontes.

## <a name="usage"></a>Uso

``` syntax
<FontControl
  CommandName = "xs:positiveInteger or xs:string"
  FontType = "xs:string"
  IsGrowShrinkButtonGroupVisible = "Boolean"
  IsStrikethroughButtonVisible = "Boolean"
  IsUnderlineButtonVisible = "Boolean"
  IsHighlightButtonVisible = "Boolean"
  ShowVerticalFonts = "Boolean"
  ShowTrueTypeOnly = "Boolean"
  MinimumFontSize = "xs:positiveInteger"
  MaximumFontSize = "xs:positiveInteger"/>
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
<td>xs:positiveInteger ou xs:string<br/></td>
<td>Não<br/></td>
<td>Associa o elemento a um <a href="windowsribbon-element-command.md"><strong>Comando</strong></a>.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger ou xs:string)<br/> </dt> <dd> Uma cadeia de caracteres, um valor inteiro entre 2 e 59999, inclusive ou um valor hexadecimal entre 0x2 e 0xea5f, inclusive. <br/> O valor deve ser exclusivo dentro do documento XML da Faixa de Opções. <br/> Comprimento máximo: 100 caracteres. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>FontType</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>Restrito a um dos seguintes valores: <br/> <br/>
<dt><span></span><span></span><strong></strong> (FontOnly)<br/> </dt> <dd> Padrão. <br/> <img src="images/markup/screenshot-fonttype-fontonly.png" alt="Screen shot of the FontControl element with the FontOnly attribute set to true." /><br/> Definir o <em>atributo FontType</em> como <code>FontOnly</code> habilita a seguinte funcionalidade:<br/>
<ul>
<li><strong>Caixa de combinação</strong> da família de fontes.</li>
<li><strong>Caixa de combinação</strong> Tamanho da Fonte.</li>
<li><p><strong>Botões</strong>de alternância Negrito, <strong>Itálico,</strong> <strong>Sublinhado</strong>e <strong>Tachado.</strong></p>
<blockquote>
[!Note]<br />
Os botões <strong></strong> <strong>de</strong> alternância Tachado e Sublinhado são exibidos por padrão, mas podem ser ocultos definindo os atributos <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> como <code>false</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (FontWithColor)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-fontwithcolor.png" alt="Screen shot of the FontControl element with the FontWithColor attribute set to true." /><br/> Definir o <em>atributo FontType</em> como <code>FontWithColor</code> habilita a seguinte funcionalidade:<br/>
<ul>
<li><strong>Caixa de combinação</strong> da família de fontes.</li>
<li><strong>Caixa de combinação</strong> tamanho da fonte.</li>
<li><strong>Aumentar a fonte</strong> e <strong>reduzir o incremento</strong> de tamanho da fonte e os botões de decremento.</li>
<li><p><strong>Botões</strong>de alternância Negrito, <strong>Itálico,</strong> <strong>Sublinhado</strong>e <strong>Tachado.</strong></p>
<blockquote>
[!Note]<br />
Os botões <strong></strong> <strong>de</strong> alternância Tachado e Sublinhado são exibidos por padrão, mas podem ser ocultos definindo os atributos <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> como <code>false</code> .
</blockquote>
<p><br/></p></li>
<li><strong>Selador de cor</strong> de texto.</li>
<li><p><strong>Selador de cor de realçada</strong> de texto.</p>
<blockquote>
[!Note]<br />
Esse controle está oculto por padrão, mas pode ser exibido definindo o atributo <em>IsHighlightButtonVisible</em> como <code>true</code> .
</blockquote>
<p><br/></p></li>
</ul>
</dd> <dt><span></span><span></span><strong></strong> (RichFont)<br/> </dt> <dd> <img src="images/markup/screenshot-fonttype-richfont.png" alt="Screen shot of the FontControl element with the RichFont attribute set to true." /><br/> Definir o <em>atributo FontType</em> como <code>RichFont</code> habilita a seguinte funcionalidade:<br/>
<ul>
<li><strong>Caixa de combinação</strong> da família de fontes.</li>
<li><strong>Caixa de combinação</strong> tamanho da fonte.</li>
<li><strong>Aumentar a fonte</strong> e <strong>reduzir o incremento</strong> de tamanho da fonte e os botões de decremento.</li>
<li><p><strong>Botões</strong>de alternância Negrito, <strong>Itálico,</strong> <strong>Sublinhado</strong>e <strong>Tachado.</strong></p>
<blockquote>
[!Note]<br />
Os botões <strong></strong> <strong>de</strong> alternância Tachado e Sublinhado são exibidos por padrão e não podem ser ocultos definindo os atributos <em>IsStrikethroughButtonVisible</em> e <em>IsUnderlineButtonVisible</em> como <code>false</code> .
</blockquote>
<p><br/></p></li>
<li><strong>Selador de cor</strong> de texto.</li>
<li><p><strong>Selador de cor de realçada</strong> de texto.</p>
<blockquote>
[!Note]<br />
Esse controle é exibido por padrão e não pode ser ocultado definindo o atributo <em>IsHighlightButtonVisible</em> como <code>false</code> .
</blockquote>
<p><br/></p></li>
<li><strong>Botões de alternância</strong> <strong>de subscrito</strong> e Superscrito.</li>
</ul>
</dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsGrowShrinkButtonGroupVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td><strong>Windows 8 e mais novos</strong><br/> Restrito a um dos seguintes valores: <br/>
<blockquote>
[!Note]<br />
Os botões Aumentar/Reduzir nunca são exibidos na <a href="windowsribbon-element-minitoolbar.md"><strong>MiniToolbar</strong></a>.
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Padrão quando o valor de <em>FontType</em> é igual <code>FontWithColor</code> ou <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Padrão quando o valor de <em>FontType</em> é igual a <code>FontOnly</code> .<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsHighlightButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Restrito a um dos seguintes valores (0 e 1 não são válidos): <br/>
<blockquote>
[!Note]<br />
O realçamento de cores só está disponível em <strong>um FontControl</strong> quando o valor do atributo <em>FontType</em> é igual <code>FontWithColor</code> a ou <code>RichFont</code> .
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Padrão quando o valor de <em>FontType</em> é igual <code>FontWithColor</code> ou <code>RichFont</code> .<br/> Válido somente quando o valor de <em>FontType</em> for <code>FontWithColor</code> igual a ou <code>RichFont</code> .<br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Padrão quando o valor de <em>FontType</em> é igual a <code>FontOnly</code> .<br/> Válido somente quando o valor de <em>FontType</em> for <code>FontOnly</code> igual a ou <code>FontWithColor</code> .<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>IsStrikethroughButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Restrito a um dos seguintes valores (0 e 1 não são válidos): <br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Padrão. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Válido somente quando o valor de <em>FontType</em> for <code>FontOnly</code> igual a ou <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>IsUnderlineButtonVisible</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Restrito a um dos seguintes valores (0 e 1 não são válidos): <br/> <br/>
<dt><span></span><span></span><strong></strong> (true)<br/> </dt> <dd> Padrão. <br/> </dd> <dt><span></span><span></span><strong></strong> (false)<br/> </dt> <dd> Válido somente quando o valor de <em>FontType</em> for <code>FontOnly</code> igual a ou <code>FontWithColor</code> . <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>MaximumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Não<br/></td>
<td>O tamanho máximo de ponto a ser exibido.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Um valor inteiro entre 1 e 9999, inclusive.<br/> O padrão é <strong>9999</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinimumFontSize</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Não<br/></td>
<td>O tamanho mínimo do ponto a ser exibido.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Um valor inteiro entre 1 e 9999, inclusive.<br/> O padrão é <strong>1</strong>.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>ShowTrueTypeOnly</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Restrito a um dos valores a seguir (0 e 1 não são válidos):<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd> Exibe somente as fontes TrueType e OpenType. <br/> </dd> <dt><span></span><span></span><strong></strong> for<br/> </dt> <dd> Padrão. Nenhuma restrição é colocada no tipo de fontes exibidas.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>ShowVerticalFonts</strong><br/></td>
<td>Boolean<br/></td>
<td>Não<br/></td>
<td>Restrito a um dos valores a seguir (0 e 1 não são válidos):<br/>
<blockquote>
[!Note]<br />
As fontes verticais são precedidas por um símbolo @ na lista <strong>família de fontes</strong> .
</blockquote>
<br/> <br/>
<dt><span></span><span></span><strong></strong> true<br/> </dt> <dd> Padrão. Exibe as fontes verticais que estão definidas para <strong>Mostrar</strong> no painel de controle <strong>fontes</strong> . <br/> </dd> <dt><span></span><span></span><strong></strong> for<br/> </dt> <dd> Permite que um aplicativo que não dá suporte a texto vertical oculte quaisquer fontes verticais definidas para <strong>Mostrar</strong> no painel de controle <strong>fontes</strong> .<br/>
<blockquote>
[!Note]<br />
No Windows Vista, o painel de controle de <strong>fontes</strong> não oferece a funcionalidade de <strong>Mostrar</strong> ou <strong>ocultar</strong> . Nesse caso, o atributo <em>ShowVerticalFonts</em> deve ser definido como <code>False</code> .
</blockquote>
<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                               |
|-----------------------------------------------------------------------|
| [**Controlador de controle**](windowsribbon-element-controlgroup.md)<br/> |
| [**Grupo**](windowsribbon-element-group.md)<br/>               |
| [**Grupo Backstage**](windowsribbon-element-menugroup.md)<br/>       |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para [](windowsribbon-element-controlgroup.md)cada elemento Control [**Group, grupo**](windowsribbon-element-group.md)ou [**menu**](windowsribbon-element-menugroup.md) .

Quaisquer atributos de comando **FontControl** declarados na marcação, como [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) ou [**Command. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md), são substituídos pelos atributos dos controles individuais que compõem o **FontControl**.

Qualquer tentativa de selecionar uma amostra de cor do seletor de cores de um [controle de fonte](windowsribbon-controls-fontcontrol.md) pode resultar em uma violação de acesso se nenhum manipulador de comando estiver associado ao controle.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação básica para os três tipos de [controle de fonte](windowsribbon-controls-fontcontrol.md).

Esta seção de código mostra as declarações de comando **FontControl** , cada uma com uma declaração de contêiner de [**grupo**](windowsribbon-element-group.md) .


```XML
<!-- A FontOnly FontControl -->
<Command Name="cmdFontOnlyGroup"
         Symbol="cmdFontOnlyGroup"
         Comment="FontOnlyGroup"
         Id="50001"
         LabelTitle="FontOnly"/>
<Command Name="cmdFontOnly"
         Symbol="cmdFontOnly"
         Comment="FontOnly"
         Id="50010"/>

<!-- A FontWithColor FontControl -->
<Command Name="cmdFontWithColorGroup"
         Symbol="cmdFontWithColorGroup"
         Comment="FontWithColorGroup"
         Id="50002"
         LabelTitle="FontWithColor"/>
<Command Name="cmdFontWithColor"
         Symbol="cmdFontWithColor"
         Comment="FontWithColor"
         Id="50020"/>

<!-- A RichFont FontControl -->
<Command Name="cmdRichFontGroup"
         Symbol="cmdRichFontGroup"
         Comment="RichFontGroup"
         Id="50003"
         LabelTitle="RichFont"
         Keytip="ZF"/>
<Command Name="cmdRichFont"
         Symbol="cmdRichFont"
         Comment="RichFont"
         Id="50030"
         Keytip="RF"
         LabelTitle="test"
         TooltipTitle="test"/>
```



Esta seção de código mostra as declarações de controle **FontControl** em que cada **FontControl** e [**grupo**](windowsribbon-element-group.md) é declarado em uma única guia.


```XML
<Tab CommandName="cmdTab1">
  <Group CommandName="cmdFontOnlyGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontOnly"
                 FontType="FontOnly"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdFontWithColorGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdFontWithColor"
                 FontType="FontWithColor"
                 IsUnderlineButtonVisible="false"
                 IsStrikethroughButtonVisible="false"
                 IsHighlightButtonVisible="true"
                 MinimumFontSize="15"/>
  </Group>
  <Group CommandName="cmdRichFontGroup"
         SizeDefinition="OneFontControl">
    <FontControl CommandName="cmdRichFont"
                 FontType="RichFont"
                 IsHighlightButtonVisible="true"
                 IsUnderlineButtonVisible="true"
                 IsStrikethroughButtonVisible="true"
                 ShowVerticalFonts="true"
                 MinimumFontSize="15"/>
  </Group>
```



## <a name="element-information"></a>Informações do elemento

* **Sistema mínimo com suporte**: Windows 7
* **Pode estar vazio**: Sim



## <a name="see-also"></a>Confira também

<dl> <dt>

[Controle de controle de fonte](windowsribbon-controls-fontcontrol.md)
</dt> <dt>

[Propriedades de controle de fonte](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[Exemplo de FontControl](windowsribbon-fontcontrolsample.md)
</dt> </dl>

 

 





