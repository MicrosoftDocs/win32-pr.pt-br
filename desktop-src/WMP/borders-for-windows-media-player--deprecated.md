---
title: Bordas do Windows Media Player (preterido)
description: Bordas do Windows Media Player (preterido)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Windows Media Player, bordas
- Capas do Windows Media Player, bordas
- capas, bordas
- bordas, em comparação com as capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a48ff3ec17230002e9c6b4a1eb17e3024375a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292160"
---
# <a name="borders-for-windows-media-player-deprecated"></a>Bordas do Windows Media Player (preterido)

Esta página documenta um recurso que pode não estar disponível em versões futuras do Windows Media Player e no SDK do Windows Media Player.

Uma borda é semelhante a uma capa, mas em vez de substituir a interface do usuário pelo modo compacto do Windows Media Player, uma borda é inserida no painel em execução do modo completo do Windows Media Player.

Usando um pacote de download do Windows Media, você pode incluir conteúdo com uma borda, abrindondo a maneira de aplicativos multimídia.

Um exemplo de pacote de download do Windows Media que inclui uma borda e conteúdo inserido está incluído no diretório de exemplos deste SDK.

## <a name="creating-a-border"></a>Criando uma borda

Uma borda é criada da mesma maneira que uma capa. A única diferença é que a capa é inserida dentro do painel **agora em execução** . Isso significa que o tamanho da capa não pode ser calculado e que todos os elementos de capa devem ser relativos. Se o usuário redimensionar o Windows Media Player, partes da borda poderão ser recortadas e não vistas.

## <a name="loading-a-border"></a>Carregando uma borda

Uma borda é carregada quando um metarquivo do Windows Media que usa o elemento **Skin** é carregado. O atributo **href** do elemento **Skin** deve fazer referência a uma capa. Um elemento típico de **Skin** ficaria assim:


```C++
<SKIN HREF="myborder.wmz">

```



Para obter mais informações, consulte [elemento Skin (preterido)](skin-element--deprecated.md).

## <a name="including-content-with-a-border"></a>Incluindo conteúdo com uma borda

Você pode incluir conteúdo com uma borda usando um arquivo de download do Windows Media (com uma extensão de nome de arquivo. WMD). Siga estas etapas:

1.  Crie a borda. Tome cuidado para criá-lo de tal forma que o redimensionamento não arruinará a composição da borda. Por exemplo, não inclua um arquivo de plano de fundo; tornar o plano de fundo transparente para que uma visualização possa ser executada por trás dela.
2.  Compacte o conteúdo da capa (arte, arquivos JScript e arquivo de definição de capa) em um arquivo com uma extensão de nome de arquivo. wmz.
3.  Crie um metarquivo do Windows Media (com uma extensão de nome de arquivo. asx) que referencie o arquivo de borda compactado (com uma extensão de nome de arquivo. wmz). O metarquivo pode incluir informações de playlist com metadados para arte e URLs para conteúdo específico.
4.  Monte o conteúdo de mídia digital.
5.  Compacte a borda, o metarquivo e o conteúdo em um arquivo e dê a ele uma extensão de nome de arquivo. WMD.

## <a name="using-a-border"></a>Usando uma borda

Depois de criar o arquivo de download do Windows Media, tudo o que o usuário precisa fazer é clicar duas vezes nele. O arquivo será baixado para o computador do usuário. Os arquivos dentro do pacote serão desempacotados, a lista de reprodução será adicionada às listas de reprodução, a borda aparecerá no painel em **execução** do modo completo do Windows Media Player e o primeiro item na nova lista de reprodução começará a ser reproduzido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre as capas**](about-skins.md)
</dt> <dt>

[**Exemplos**](samples.md)
</dt> <dt>

[**Pacotes de download do Windows Media (preterido)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




