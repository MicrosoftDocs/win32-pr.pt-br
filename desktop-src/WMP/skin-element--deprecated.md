---
title: Elemento SKIN (preterido)
description: Esta página documenta um recurso que pode estar indisponível em versões futuras do Windows Media Player e do SDK do Windows Media Player.
ms.assetid: 593244c1-f850-46d7-8b84-14dcd59b024e
keywords:
- Elemento SKIN (preterido) Windows Media Player
topic_type:
- apiref
api_name:
- SKIN Element (deprecated)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b868b756ed190301c66987b6e26249762bac71842f4a5425d6d7c6d4b16816a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507906"
---
# <a name="skin-element-deprecated"></a>Elemento SKIN (preterido)

Esta página documenta um recurso que pode estar indisponível em versões futuras do Windows Media Player e do SDK do Windows Media Player.

O **elemento SKIN** especifica uma URL para uma borda.

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a>Atributos

**HREF** (obrigatório)

URL para um arquivo de borda compactado com uma extensão de nome de arquivo .wmz. Para Windows Media Player Série 9 ou posterior, esse valor pode referenciar apenas arquivos de borda no disco rígido do usuário localizado no mesmo diretório que a playlist de metadados. Consulte o código de exemplo.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos |
|-----------------|----------|
| Elementos pai | **Asx**  |
| Elementos filho  | Nenhum     |



 

## <a name="remarks"></a>Comentários

O **elemento SKIN** é usado para criar uma borda, que é semelhante a uma capa, mas é exibida na área **Agora** Em reprodução do modo completo Windows Media Player. O **elemento SKIN** é usado apenas para bordas, que aparecem dentro do modo completo Windows Media Player e não para capas regulares, que substituem inteiramente o modo compacto Windows Media Player.

Em um Windows de Download de Mídia (com uma extensão de nome de arquivo .wmd), o elemento **SKIN** permite que uma borda tenha conteúdo e vincule a outros sites. O Windows de Download de Mídia é um arquivo compactado que contém um arquivo de borda e um Windows de mídia. O arquivo de borda (com uma extensão de nome de arquivo .wmz) é compactado e inclui um arquivo de definição de capa (com uma extensão de nome de arquivo .wms).

Um **elemento SKIN** tem três componentes:

-   Uma capa
-   Algum conteúdo
-   Um metadado

As capas incluídas Windows pacotes de download de mídia devem ser retangulares em forma. A criação de bordas com capas que não são retangulares pode gerar resultados inesperados.

## <a name="examples"></a>Exemplos


```XML
<ASX version = "3.0">
    <TITLE>A Skin Element</TITLE>
    <SKIN HREF = "YourTest.wmz" />

    <ENTRY>
        <PARAM name="YourAlbumTitle" value="YourTitle.jpg"/>
        <PARAM name="link" value="https://www.proseware.com"/>
        <TITLE>(The Artist)-YourTitle</TITLE>
        <REF HREF="(The Artist)-YourSongTitle.wma"/>
    </ENTRY>

</ASX>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------|
| Versão<br/> | Windows Media Player versão 70 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Bordas para Windows Media Player (preterido)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Windows Referência de elementos de metadados de mídia**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referência de metadados de mídia**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





