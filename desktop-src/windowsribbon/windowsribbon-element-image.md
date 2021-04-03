---
title: Elemento Image (Windows Ribbon Framework)
description: Representa uma imagem.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Faixa de imagens do elemento Image do Windows
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d33f6710da2261a359aa7fd0a3b493871155cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104084247"
---
# <a name="image-element"></a>Elemento Image

Representa uma imagem.

## <a name="usage"></a>Uso

``` syntax
<Image
  Source = "xs:anyURI"
  MinDPI = "xs:positiveInteger"
  Symbol = "xs:string"
  Id = "xs:positiveInteger union xs:string">
  child elements
</Image>
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
<td><strong>Id</strong><br/></td>
<td>xs: positiveInteger Union xs: String<br/></td>
<td>No<br/></td>
<td>A ID de recurso exclusiva. <br/> <br/>
<dt><span></span><span></span><strong></strong> (A União de xs: positiveInteger e xs: String)<br/> </dt> <dd> Um valor inteiro entre 2 e 59999, inclusivo, ou 0x2 e 0xea5f em hexadecimal, inclusive. <br/> O comprimento máximo é de 10 caracteres, incluindo zeros à esquerda opcionais. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinDPI</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: positiveInteger)<br/> </dt> <dd> Qualquer sequência de dígitos com um valor mínimo de 96. <br/> Se MinDPI for omitido, o valor padrão será 96. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Origem</strong><br/></td>
<td>xs:anyURI<br/></td>
<td>No<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs: anyURI)<br/> </dt> <dd> Qualquer sequência de caracteres que representa um URI. O valor do URI é um caminho absoluto ou relativo (para o arquivo de marcação da faixa de tipos) para um recurso de imagem do tipo BMP. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Símbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>No<br/></td>
<td>O símbolo de recurso para a imagem.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs: String)<br/> </dt> <dd> Uma cadeia de caracteres composta de uma letra ou sublinhado seguida por qualquer sequência de letras, dígitos ou sublinhados até um máximo de 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                               | Descrição                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Imagem. origem**](windowsribbon-element-image-source.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [**Comando. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [**Comando. LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         |
| [**Comando. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [**Comando. SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer uma ou mais vezes para cada [**comando. SmallImages**](windowsribbon-element-command-smallimages.md), [**Command. SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command. LargeImages**](windowsribbon-element-command-largeimages.md)ou [**Command. LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md) elemento.

Quando uma coleção de recursos de imagem que são projetados para dar suporte a configurações de pontos de tela específicos por polegada (DPI) é fornecida à estrutura da faixa de opções por meio de um conjunto de elementos **Image** , a estrutura usa a **imagem** com um valor de atributo *MinDPI* que corresponde à configuração de dpi de tela atual.

Se nenhum elemento **Image** for declarado com um valor *MinDPI* que corresponda à configuração de dpi de tela atual, a estrutura selecionará a **imagem** que tem o valor de *MinDPI* mais próximo menor que a configuração de dpi de tela atual e dimensionará o recurso de imagem para cima. Caso contrário, se nenhum elemento **Image** for declarado com um valor de atributo *MinDPI* menor que a configuração de dpi de tela atual, a estrutura escolherá o valor de *MinDPI* mais próximo maior que a configuração de dpi de tela atual e dimensionará o recurso de imagem para baixo.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra a marcação necessária para declarar, por meio de um conjunto de elementos **Image** , uma coleção de recursos de imagem que são projetados para dar suporte a quatro configurações específicas de dpi de tela.


```XML
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">res/sizeAndColor_96.bmp</Image>
    <Image Id="252" MinDPI="120">res/sizeAndColor_120.bmp</Image>
    <Image Id="253" MinDPI="144">res/sizeAndColor_144.bmp</Image>
    <Image Id="254" MinDPI="192">res/sizeAndColor_192.bmp</Image>
  </Command.LargeImages>
</Command>
```



## <a name="element-information"></a>Informações do elemento



|                                     |           |
|-------------------------------------|-----------|
| Sistema mínimo com suporte<br/> | Windows 7 |
| Pode estar vazio                        | Não        |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Especificando recursos de imagem da faixa de uma](windowsribbon-imageformats.md)
</dt> </dl>

 

 





