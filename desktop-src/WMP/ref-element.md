---
title: Elemento REF
description: O elemento REF especifica uma URL para o conteúdo de mídia digital.
ms.assetid: 0ba11a1e-3802-4156-83ca-f1bae1eb366c
keywords:
- Elemento REF do Windows Media Player
topic_type:
- apiref
api_name:
- REF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 739ac61007e619055c28732c5c5aa763e84054fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786234"
---
# <a name="ref-element"></a>Elemento REF

O elemento **ref** especifica uma URL para o conteúdo de mídia digital.

``` syntax
<REF
   HREF = "URL"
>
</REF>
```

## <a name="attributes"></a>Atributos

**Href** (obrigatório)

URL para qualquer parte do conteúdo de mídia com suporte no Windows Media Player.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos                                                                         |
|-----------------|----------------------------------------------------------------------------------|
| Elementos pai | **INICIAL**                                                                        |
| Elementos filho  | **duração**, **endmarcador**, **PREVIEWDURATION**, **STARTMARKER**, **StartTime** |



 

## <a name="remarks"></a>Comentários

Esse elemento Especifica uma URL para uma parte do conteúdo de mídia. A URL pode apontar para qualquer tipo de mídia com suporte, usando qualquer protocolo suportado pelo Windows Media Player.

Os tipos de mídia com suporte incluem imagens ainda, como imagens. gif e. jpg e arquivos flash com uma extensão de nome de arquivo. swf. Esses tipos de mídia são úteis para incluir conteúdo de publicidade em uma lista de reprodução. Com arquivos de imagem e arquivos flash que são executados em um loop, você também deve especificar a quantidade de tempo para exibir o item de mídia, incluindo um elemento **Duration** dentro do elemento **ref** . Se você quiser que uma imagem continue a ser exibida enquanto a próxima entrada na lista de reprodução estiver armazenada em buffer, inclua um elemento **param** dentro do elemento **entry** , defina seu atributo **Name** como ShowWhileBuffering e defina seu atributo **Value** como true.

Para fazer referência ao conteúdo em um CD ou DVD que permita, os protocolos Wmpcd e wmpdvd são fornecidos. Por exemplo, definir o atributo **href** como "wmpdvd://f/5/3" executará o capítulo 3 do título 5 em um DVD, mas somente se o DVD tiver sido criado para permiti-lo.

Os aplicativos que abrirem mídia digital por trás de um firewall terão um desempenho melhor ao abrir os itens de mídia se o endereço for especificado usando o nome DNS (servidor de nomes de domínio) em vez do endereço IP.

O uso mais comum desse elemento é para substituição de URL. Se o Windows Media Player não puder abrir uma parte da mídia definida em um elemento **ref** , ele tentará a URL no próximo elemento **ref** . Depois que o Windows Media Player abre o conteúdo de mídia de uma URL definida no escopo de um elemento de **entrada** , ele ignora as marcas de **referência** subsequentes dentro desse elemento de **entrada** . Depois que a parte do conteúdo é executada, o Windows Media Player passa para o próximo elemento de **entrada** , se houver.

-   **Importante** Depois que o Windows Media Player estabelece uma conexão com uma parte de conteúdo referenciada, ele ignora todos os outros elementos **ref** nessa **entrada**, independentemente de a conexão ser encerrada normalmente ou de forma anormal.

Se o item de mídia referenciado for um arquivo de imagem, o elemento **Duration** deverá ser usado para especificar o tempo de exibição da imagem.

**Observação**

A tentativa de reproduzir mídia flash que inclui som com o primeiro quadro pode gerar resultados inesperados. Você deve criar o conteúdo do flash para tocar no som, começando no início do segundo quadro.

## <a name="examples"></a>Exemplos


```XML
<ASX VERSION="3.0">
   <ENTRY>
   <TITLE>Example Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/selection1.asf" />
      <REF HREF="mms://sample.microsoft.com/mirror/selection1.asf" />
   </ENTRY>
</ASX>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Tipos de arquivos e protocolos com suporte**](supported-protocols-and-file-types.md)
</dt> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





