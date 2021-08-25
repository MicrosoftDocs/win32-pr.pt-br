---
title: Sobre plug-ins de conversão
description: Sobre plug-ins de conversão
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Windows Media Player,plug-ins de conversão
- Windows Media Player plug-ins, conversão
- plug-ins, conversão
- plug-ins de conversão, sobre
- Advanced Systems Format (ASF)
- ASF (formato de sistemas avançados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4331f2cc0cdf8726e2ba26e834c56546ee614e012a9dd6acdad56906d450b66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903546"
---
# <a name="about-conversion-plug-ins"></a>Sobre plug-ins de conversão

Você pode criar um plug-in Windows Media Player para converter arquivos de mídia digital criados usando tecnologias não fornecidas pela Microsoft em FORMATO DE SISTEMAS Avançados (ASF).

Plug-ins de conversão são Component Object Model (COM) que são empacotados e distribuídos como arquivos executáveis (.exe). Windows Media Player instala plug-ins de conversão para converter formatos de mídia digital de terceiros nos seguintes cenários:

-   O conteúdo da mídia digital é copiado para o computador de um dispositivo portátil.
-   O conteúdo da mídia digital é adicionado à biblioteca usando **IWMPMediaCollection::add**.
-   O conteúdo da mídia digital é adicionado à biblioteca usando o recurso de pesquisa Windows Media Player.
-   O conteúdo da mídia digital é adicionado à biblioteca pelo recurso de monitoramento de pasta Windows Media Player.
-   O conteúdo da mídia digital é adicionado à lista de sincronização quando o usuário arrasta e descarta um arquivo.

Depois Windows Media Player criar uma instância de um plug-in de conversão, o plug-in deverá converter o arquivo fornecido em ASF ou WMA e adicionar metadados relevantes. (Não use o plug-in de conversão para transcodificar o arquivo.) O plug-in deve copiar o arquivo convertido para a pasta especificada e retornar o caminho para o novo arquivo para Windows Media Player.

Os plug-ins de conversão devem implementar a interface **IWMPConvert.** Consulte [Referência de programação de plug-ins de conversão](conversion-plug-ins-programming-reference.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o processo de conversão**](about-the-conversion-process.md)
</dt> <dt>

[**Adicionando metadados a arquivos convertidos**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Windows Media Player Plug-ins de conversão**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




