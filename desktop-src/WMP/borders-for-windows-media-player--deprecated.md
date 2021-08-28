---
title: Bordas para Windows Media Player (preterido)
description: Bordas para Windows Media Player (preterido)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Windows Media Player,bordas
- Windows Media Player capas, bordas
- capas, bordas
- bordas, em comparação com capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32e16fa6e334c5c47f24feadc777b82cee1a12477211bc4e613d22e8fdc4521
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123846"
---
# <a name="borders-for-windows-media-player-deprecated"></a>Bordas para Windows Media Player (preterido)

Esta página documenta um recurso que pode estar indisponível em versões futuras do Windows Media Player e do SDK do Windows Media Player.

Uma borda é semelhante a uma capa, mas em vez de substituir a interface do usuário para o modo compacto do Windows Media Player, uma borda é inserida no painel Agora Em reprodução do modo completo Windows Media Player.

Usando um pacote Windows de Download de Mídia, você pode incluir conteúdo com uma borda, abrindo o caminho para aplicativos multimídia.

Um exemplo Windows de Download de Mídia que inclui uma borda e conteúdo inserido está incluído no diretório de exemplos deste SDK.

## <a name="creating-a-border"></a>Criando uma borda

Uma borda é criada da mesma maneira que uma capa. A única diferença é que a capa é inserida dentro do **painel Agora Em** reprodução. Isso significa que o tamanho da capa não pode ser calculado e que todos os elementos de capa devem ser relativos. Se o usuário reessutar Windows Media Player, partes da borda poderão ser cortadas e não vistas.

## <a name="loading-a-border"></a>Carregando uma borda

Uma borda é carregada quando um Windows media que usa o **elemento SKIN** é carregado. O **atributo HREF** do elemento **SKIN** deve referenciar uma capa. Um elemento **SKIN** típico teria esta aparência:


```C++
<SKIN HREF="myborder.wmz">

```



Para obter mais informações, [consulte Elemento SKIN (preterido).](skin-element--deprecated.md)

## <a name="including-content-with-a-border"></a>Incluindo conteúdo com uma borda

Você pode incluir o conteúdo com uma borda usando um arquivo Windows de Download de Mídia (com uma extensão de nome de arquivo .wmd). Siga estas etapas:

1.  Crie a borda. Tome cuidado para criar isso de forma que o resizing não destruirá a composição da borda. Por exemplo, não inclua um arquivo em segundo plano; tornar a plano de fundo transparente para que uma visualização possa ser executado por trás dela.
2.  Compactar o conteúdo da capa (arte, JScript arquivos e arquivo de definição de capa) em um arquivo com uma extensão de nome de arquivo .wmz.
3.  Crie um metadado Windows Media (com uma extensão de nome de arquivo .asx) que referencia o arquivo de borda compactado (com uma extensão de nome de arquivo .wmz). O metadado pode incluir informações de playlist com metadados para arte e URLs para conteúdo específico.
4.  Montar o conteúdo da mídia digital.
5.  Compactar a borda, o metafile e o conteúdo em um arquivo e dar a ele uma extensão de nome de arquivo .wmd.

## <a name="using-a-border"></a>Usando uma borda

Depois de criar o arquivo Windows de Download de Mídia, tudo o que o usuário precisa fazer é clicar duas vezes nele. O arquivo será baixado no computador do usuário. Os arquivos dentro do pacote serão desempacodados, a playlist será  adicionada às playlists, a borda aparecerá no painel Agora Em reprodução do modo completo Windows Media Player e o primeiro item na nova playlist começará a ser exibido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre capas**](about-skins.md)
</dt> <dt>

[**Exemplos**](samples.md)
</dt> <dt>

[**Windows Pacotes de Download de Mídia (preterido)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




