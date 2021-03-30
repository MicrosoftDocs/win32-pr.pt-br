---
title: Sobre plug-ins de conversão
description: Sobre plug-ins de conversão
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Windows Media Player, plug-ins de conversão
- Plug-ins do Windows Media Player, conversão
- plug-ins, conversão
- plug-ins de conversão, sobre
- Advanced Systems Format (ASF)
- ASF (formato de sistemas avançados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6e2a8fa41b657a593dc03082f871503b53eba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635086"
---
# <a name="about-conversion-plug-ins"></a>Sobre plug-ins de conversão

Você pode criar um plug-in do Windows Media Player para converter arquivos de mídia digital criados usando tecnologias não fornecidas pela Microsoft no formato ASF (Advanced Systems Format).

Os plug-ins de conversão são objetos de Component Object Model (COM) que são empacotados e distribuídos como arquivos executáveis (. exe). O Windows Media Player instancia os plug-ins de conversão para converter formatos de mídia digital de terceiros nos seguintes cenários:

-   O conteúdo de mídia digital é copiado para o computador de um dispositivo portátil.
-   O conteúdo de mídia digital é adicionado à biblioteca usando **IWMPMediaCollection:: Add**.
-   O conteúdo de mídia digital é adicionado à biblioteca usando o recurso de pesquisa do Windows Media Player.
-   O conteúdo de mídia digital é adicionado à biblioteca pelo recurso de monitoramento de pasta do Windows Media Player.
-   O conteúdo de mídia digital é adicionado à lista de sincronização quando o usuário arrasta e descarta um arquivo.

Depois que o Windows Media Player cria uma instância de um plug-in de conversão, o plug-in deve converter o arquivo fornecido em ASF ou WMA e adicionar metadados relevantes. (Não use o plug-in de conversão para transcodificar o arquivo.) O plug-in deve copiar o arquivo convertido para a pasta especificada e retornar o caminho para o novo arquivo para o Windows Media Player.

Os plug-ins de conversão devem implementar a interface **IWMPConvert** . Consulte [referência de programação de plug-ins de conversão](conversion-plug-ins-programming-reference.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o processo de conversão**](about-the-conversion-process.md)
</dt> <dt>

[**Adicionando metadados a arquivos convertidos**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Plug-ins de conversão do Windows Media Player**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




