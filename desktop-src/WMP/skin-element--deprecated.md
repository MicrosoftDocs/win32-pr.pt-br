---
title: Elemento SKIN (preterido)
description: Esta página documenta um recurso que pode não estar disponível em versões futuras do Windows Media Player e no SDK do Windows Media Player.
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
ms.openlocfilehash: abf503706dec131eef411ebaf3625071e2b31098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811243"
---
# <a name="skin-element-deprecated"></a>Elemento SKIN (preterido)

Esta página documenta um recurso que pode não estar disponível em versões futuras do Windows Media Player e no SDK do Windows Media Player.

O elemento **Skin** especifica uma URL para uma borda.

``` syntax
<SKIN
   HREF = "URL"
/>
```

## <a name="attributes"></a>Atributos

**Href** (obrigatório)

URL para um arquivo de borda compactado com uma extensão de nome de arquivo. wmz. Para o Windows Media Player 9 Series ou posterior, esse valor pode fazer referência somente a arquivos de borda no disco rígido do usuário localizado no mesmo diretório que a playlist de metarquivo. Consulte o código de exemplo.

## <a name="parentchild-elements"></a>Elementos pai/filho



| Hierarquia       | Elementos |
|-----------------|----------|
| Elementos pai | **ASX**  |
| Elementos filho  | Nenhum     |



 

## <a name="remarks"></a>Comentários

O elemento **Skin** é usado para criar uma borda, que é semelhante a uma capa, mas é exibido na área em **execução** do modo completo do Windows Media Player. O elemento **Skin** é usado apenas para bordas, que aparecem dentro do modo completo do Windows Media Player e não para capas regulares, que substituem totalmente o Windows Media Player do modo compacto.

Em um pacote de download do Windows Media (com uma extensão de nome de arquivo. WMD), o elemento **Skin** permite que uma borda tenha conteúdo e seja vinculada a outros sites. O pacote de download do Windows Media é um arquivo compactado que contém um arquivo de borda e um metarquivo do Windows Media. O arquivo de borda (com uma extensão de nome de arquivo. wmz) é compactado e inclui um arquivo de definição de capa (com uma extensão de nome de arquivo. WMS).

Um elemento **Skin** tem três componentes:

-   Uma capa
-   Algum conteúdo
-   Um metarquivo

As capas incluídas nos pacotes de download de mídia do Windows devem ser retangulares em forma. A criação de bordas com capas que não são retangulares pode gerar resultados inesperados.

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

[**Bordas do Windows Media Player (preterido)**](borders-for-windows-media-player--deprecated.md)
</dt> <dt>

[**Referência de elementos de metarquivo do Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referência do metarquivo do Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





