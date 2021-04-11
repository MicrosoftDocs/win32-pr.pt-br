---
title: Elemento Command
description: Representa uma definição de comando.
ms.assetid: f332423d-d258-488d-9233-71687288b462
keywords:
- Faixa de das janelas do elemento de comando
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b684b361927180a4bb87d2d7814d2f26d4fdcd91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294394"
---
# <a name="command-element"></a>Elemento Command

Representa uma definição de comando.

## <a name="usage"></a>Uso

``` syntax
<Command
  Name = "xs:string"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string"
  Comment = "xs:string"
  LabelTitle = "xs:string"
  LabelDescription = "xs:string"
  TooltipTitle = "xs:string"
  TooltipDescription = "xs:string"
  Keytip = "xs:string">
  child elements
</Command>
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
<td><strong>Comentário</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Usado para anotar o elemento Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.<br/> Comprimento máximo: 250 caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Id</strong><br/></td>
<td>xs: positiveInteger Union xs: String<br/></td>
<td>No<br/></td>
<td>A ID de recurso exclusiva. <br/> <br/>
<dt><span></span><span></span><strong></strong> (A União de xs: positiveInteger e xs: String)<br/> </dt> <dd> Um valor inteiro entre 2 e 59999, inclusivo, ou 0x2 e 0xea5f em hexadecimal, inclusive. <br/> O comprimento máximo é de 10 caracteres, incluindo zeros à esquerda opcionais. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>KeyTip</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Uma cadeia de caracteres que representa o atalho de teclado de um elemento de comando.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo o espaço em branco.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>LabelDescription</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Uma cadeia de caracteres que representa o texto exibido em um elemento Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>LabelTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Uma cadeia de caracteres que representa o texto exibido em um elemento Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Nome</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Uma cadeia de caracteres que consiste em uma letra ou sublinhado seguido por qualquer sequência de dígitos, letras ou sublinhados.<br/> Comprimento máximo: 100 caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Símbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Uma cadeia de caracteres que consiste em uma letra ou sublinhado seguido por qualquer sequência de dígitos, letras ou sublinhados.<br/> Comprimento máximo: 100 caracteres.<br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>TooltipDescription</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Uma cadeia de caracteres que representa o texto exibido em um elemento Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.<br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>TooltipTitle</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>Uma cadeia de caracteres que representa o texto exibido em um elemento Command.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Uma cadeia de caracteres composta de qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.<br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                                                                     | Descrição                                   |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| [**Comando. Comment**](windowsribbon-element-command-comment.md)<br/>                                 | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Command.Id**](windowsribbon-element-command-id.md)<br/>                                           | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Comando. KeyTip**](windowsribbon-element-command-keytip.md)<br/>                                   | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Comando. LabelDescription**](windowsribbon-element-command-labeldescription.md)<br/>               | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Comando. LabelTitle**](windowsribbon-element-command-labeltitle.md)<br/>                           | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Comando. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Comando. LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Command.Name**](windowsribbon-element-command-name.md)<br/>                                       | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Comando. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Comando. SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Comando. Symbol**](windowsribbon-element-command-symbol.md)<br/>                                   | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Comando. TooltipDescription**](windowsribbon-element-command-tooltipdescription.md)<br/>           | Pode ocorrer no máximo uma vez<br/> <br/> |
| [**Comando. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)<br/>                       | Pode ocorrer no máximo uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                               |
|---------------------------------------------------------------------------------------|
| [**Application. Commands**](windowsribbon-element-application-commands.md)<br/> |



## <a name="remarks"></a>Comentários

Obrigatórios.

Pode ocorrer uma ou mais vezes para cada elemento [**Application. Commands**](windowsribbon-element-application-commands.md) .

Os elementos filho do elemento **Command** podem ocorrer em qualquer ordem.

Normalmente, os recursos de comando são declarados na marcação da faixa de medida, mas também podem ser definidos em tempo de execução com uma chamada para [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty). Por exemplo, é possível definir a propriedade [ \_ PKEY \_ KeyTip da interface do usuário](windowsribbon-reference-properties-uipkey-keytip.md) para um comando em vez de declarar um valor na marcação com o elemento [**Command. KeyTip**](windowsribbon-element-command-keytip.md) .

Nos casos em que as propriedades de comando, como rótulos e imagens, não podem ser definidas com [**SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) , elas podem ser invalidadas com uma chamada para [**InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand). Após a invalidação, a estrutura consulta o aplicativo host para obter os detalhes do recurso.

> [!Note]  
> Um recurso não pode ser restabelecido da tabela de recursos de marcação depois de ser invalidado.

 

Uma definição de comando é adicionada ao arquivo de cabeçalho de marcação da faixa de medida para cada **comando** declarado na marcação.

O valor de *KeyTip* atua como o acelerador de teclado para um comando, a menos que esse comando seja exposto por meio de um item de menu. Nesse caso, a estrutura ignora o valor de *KeyTip* e, em vez disso, usa um caractere precedido por um e comercial como especificado por *LabelTitle* ou [rótulo de \_ PKEY \_ de interface do usuário](windowsribbon-reference-properties-uipkey-label.md). Se nenhum e comercial for especificado por *LabelTitle* ou rótulo de PKEY da interface do usuário \_ \_ , nenhum KeyTip ou acelerador de teclado será exposto.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra um manifesto dos elementos **Command** para uma guia **Home** .


```XML
<Application.Commands>
```




```XML
<Command Name="cmdHomeTab"
         LabelTitle="Home"
         Keytip="H" />
<Command Name="cmdClipboardGroup"
         Symbol="IDR_CMD_CLIPBOARD"
         Id="10000"
         Comment="Command definition for clipboard group"
         LabelTitle="Clipboard"
         Keytip="CB" />
<Command Name="cmdCopy"
         Symbol="IDR_CMD_COPY"
         LabelTitle="Copy"
         LabelDescription="Copy"
         Keytip="C"
         TooltipTitle="Copy"
         TooltipDescription="Click to copy">
  <Command.SmallImages>
    <Image>res/copyS_16.bmp</Image>
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/copyL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdPaste"
         Symbol="IDR_CMD_PASTE" >
  <Command.LabelTitle>Paste</Command.LabelTitle>
  <Command.LabelDescription>
    <String Content="Paste contents of clipboard"
            Id="10001"
            Symbol="IDR_RES_LABELDESC_PASTE" />
  </Command.LabelDescription>
  <Command.Keytip>P</Command.Keytip>
  <Command.TooltipTitle>
    <String Content="Paste contents of clipboard"
            Id="10002"
            Symbol="IDR_RES_TOOLTIP_PASTE"/>
  </Command.TooltipTitle>
  <Command.TooltipDescription>
    <String Content="Click to paste contents of clipboard"/>
  </Command.TooltipDescription>
  <Command.SmallImages>
    <Image
      Id="10010"
      MinDPI="96"
      Symbol="IDR_RES_SMALL_IMAGE96">
      <Image.Source>res/pasteS_96bpp.bmp</Image.Source>
    </Image>
    <Image Source="res/pasteS_120bpp.bmp"
           Id="10011"
           MinDPI="120"
           Symbol="IDR_RES_SMALL_IMAGE120" />
  </Command.SmallImages>
  <Command.LargeImages>
    <Image>res/pasteL_32.bmp</Image>
  </Command.LargeImages>
</Command>
<Command Name="cmdMinimize"
         Symbol="IDR_CMD_MINIMIZE"
         Id="10001"
         LabelTitle="Minimize" />
```




```XML
</Application.Commands>
```



## <a name="element-information"></a>Informações do elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo com suporte<br/> | Windows 7 |
| Pode estar vazio                        | Não        |



 

