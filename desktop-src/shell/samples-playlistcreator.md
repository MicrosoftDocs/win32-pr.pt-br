---
description: Demonstra como criar um verbo que opera em um contêiner ou item de shell selecionado para criar uma lista de reprodução.
title: Exemplo de criador de playlist
ms.topic: article
ms.date: 05/31/2018
ms.assetid: B35B7A18-2163-4860-BC50-8918056C9F4A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 086cb0f3fbb4cb009cd156013ce3ea16a2a7dee3b2346824d51b79094c06c45e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592886"
---
# <a name="playlist-creator-sample"></a>Exemplo de criador de playlist

Demonstra como criar um verbo que opera em um contêiner ou item de shell selecionado para criar uma lista de reprodução.

Este tópico inclui as seções a seguir.

-   [Requirements](#requirements)
-   [Baixando o exemplo](#downloading-the-sample)
-   [Compilando o exemplo](#building-the-sample)
-   [Executando o exemplo](#running-the-sample)

## <a name="requirements"></a>Requisitos



| Produto                                | Versão mínima do produto |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

| Localização      | URL do caminho                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Exemplo de PlaylistCreator](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/PlaylistCreator) |

## <a name="building-the-sample"></a>Compilando o exemplo

Para criar o exemplo do prompt de comando:

1.  Abra a janela do prompt de comando e navegue até o diretório do projeto **PlaylistCreator** .
2.  Digite `msbuild PlaylistCreator.sln`.

para criar o exemplo usando Microsoft Visual Studio (preferencial):

> [!Note]  
> esse exemplo também pode ser usado com o Visual C++ Express Edition se o Visual Studio completo não estiver disponível.

 

1.  abra Windows Explorer e navegue até o diretório do projeto **PlaylistCreator** .
2.  Clique duas vezes no ícone do arquivo PlaylistCreator. sln para abrir o projeto no Visual Studio.
3.  No menu **Compilar**, selecione **Compilar Solução**.
    > [!Note]  
    > se você estiver compilando 64 bits usando o Visual C++ Express Edition, deverá usar o compilador cruzado x64 fornecido com o SDK do Windows.

     

## <a name="running-the-sample"></a>Executando o exemplo

1.  navegue até o diretório que contém o novo executável, usando o prompt de comando ou o gerenciador de Windows.
2.  Na linha de comando, digite `PlaylistCreator.exe` . como alternativa, no Windows Explorer, clique duas vezes no ícone para PlaylistCreator.exe.
3.  clique com o botão direito do mouse em qualquer arquivo ou pasta de música que contenha arquivos de música no Windows Explorer para criar uma lista de reprodução para abrir o menu de contexto
4.  Você pode criar uma lista de reprodução. m3u ou. wpl. As listas de reprodução são criadas na `%userprofile%\Music\Playlists` pasta.
    > [!Note]  
    > Novos verbos no menu de contexto podem ser encontrados na pasta **música** , pilhas de músicas, pilhas na **biblioteca de músicas** e coleções de arquivos de música.

     

 

 



