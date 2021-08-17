---
title: Elemento Image (Windows Ribbon Framework)
description: Representa uma imagem.
ms.assetid: 2c71bb16-93ac-484f-b81b-1b95842472b3
keywords:
- Elemento Image Windows Ribbon
topic_type:
- apiref
api_name:
- Image
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aad95d62be63434653908d54a290c3213fd22bf644150b70fa995e86bf5e39af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931446"
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
<td>xs:positiveInteger union xs:string<br/></td>
<td>Não<br/></td>
<td>A ID de recurso exclusiva. <br/> <br/>
<dt><span></span><span></span><strong></strong> (A união de xs:positiveInteger e xs:string)<br/> </dt> <dd> Um valor inteiro entre 2 e 59999, inclusive ou 0x2 e 0xea5f em hexadecimal, inclusive. <br/> O comprimento máximo é de 10 caracteres, incluindo zeros à esquerda opcionais. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>MinDPI</strong><br/></td>
<td>xs:positiveInteger<br/></td>
<td>Não<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:positiveInteger)<br/> </dt> <dd> Qualquer sequência de dígitos com um valor mínimo de 96. <br/> Se MinDPI for omitido, o valor padrão será 96. <br/> </dd> </dl></td>
</tr>
<tr class="odd">
<td><strong>Origem</strong><br/></td>
<td>xs:anyURI<br/></td>
<td>Não<br/></td>
<td><dt><span></span><span></span><strong></strong> (xs:anyURI)<br/> </dt> <dd> Qualquer sequência de caracteres que representa um URI. O valor de URI é um caminho absoluto ou relativo (para o arquivo de marcação faixa de opções) para um recurso de imagem do tipo BMP. <br/> </dd> </dl></td>
</tr>
<tr class="even">
<td><strong>Símbolo</strong><br/></td>
<td>xs:string<br/></td>
<td>Não<br/></td>
<td>O símbolo de recurso para a imagem.<br/> <br/>
<dt><span></span><span></span><strong></strong> (xs:string)<br/> </dt> <dd> Uma cadeia de caracteres composta por uma letra ou sublinhado seguida por qualquer sequência de letras, dígitos ou sublinhados até um máximo de 100 caracteres. <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a>Elementos filho



| Elemento                                                               | Descrição                                   |
|-----------------------------------------------------------------------|-----------------------------------------------|
| [**Image.Source**](windowsribbon-element-image-source.md)<br/> | Pode ocorrer no máximo uma vez<br/> <br/> |



## <a name="parent-elements"></a>Elementos pai



| Elemento                                                                                                     |
|-------------------------------------------------------------------------------------------------------------|
| [**Command.LargeHighContrastImages**](windowsribbon-element-command-largehighcontrastimages.md)<br/> |
| [**Command.LargeImages**](windowsribbon-element-command-largeimages.md)<br/>                         |
| [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md)<br/> |
| [**Command.SmallImages**](windowsribbon-element-command-smallimages.md)<br/>                         |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer uma ou mais vezes para cada [**elemento Command.SmallImages**](windowsribbon-element-command-smallimages.md), [**Command.SmallHighContrastImages**](windowsribbon-element-command-smallhighcontrastimages.md), [**Command.LargeImages**](windowsribbon-element-command-largeimages.md)ou [**Command.LargeHighContrastImages.**](windowsribbon-element-command-largehighcontrastimages.md)

Quando uma coleção de recursos de imagem projetados para dar suporte a configurações específicas de dpi (pontos de  tela por polegada) é fornecida à estrutura de Faixa de Opções por meio de um conjunto de elementos Image, a estrutura usa a Imagem com um valor de atributo *MinDPI* que corresponde à configuração de dpi da tela atual. 

Se nenhum elemento **Image** for declarado com um valor *MinDPI* que corresponde à  configuração de dpi da tela atual, a estrutura escolherá a Imagem que tem o valor *minDPI* mais próximo menor que a configuração de dpi da tela atual e escalará o recurso de imagem para cima. Caso contrário, se nenhum elemento **Image** for declarado com um valor de atributo *MinDPI* menor que a configuração de dpi da tela atual, a estrutura escolherá o valor *minDPI* mais próximo maior que a configuração de dpi da tela atual e dimensiona o recurso de imagem para baixo.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra a marcação necessária para declarar, por meio de um conjunto de elementos **Image,** uma coleção de recursos de imagem projetados para dar suporte a quatro configurações específicas de dpi de tela.


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

* **Sistema mínimo com suporte:** Windows 7
* **Pode estar vazio:** Não



## <a name="see-also"></a>Confira também

<dl> <dt>

[Especificando recursos de imagem da faixa de opções](windowsribbon-imageformats.md)
</dt> </dl>

 

 





