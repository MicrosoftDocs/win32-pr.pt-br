---
title: como Windows pacotes de Download de mídia funcionam (preterido)
description: como Windows pacotes de Download de mídia funcionam (preterido)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Windows metaarquivos de mídia, Windows pacotes de Download de mídia
- Windows Media Player, Windows pacotes de Download de mídia
- metaarquivos, Windows pacotes de Download de mídia
- Windows pacotes de Download de mídia Windows mídia
- Windows Pacotes de download de mídia, sobre
- Windows Pacotes de download de mídia, como os pacotes funcionam
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8b1af3cd89ec5d9b232872747d53504a2ad07ddc15e740dc19fc4cb37e9322ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338962"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a>como Windows pacotes de Download de mídia funcionam (preterido)

esta página documenta um recurso que pode estar indisponível em versões futuras do Windows Media Player e o SDK do Windows Media Player.

um pacote de Download de mídia Windows é iniciado em um site quando um usuário clica em um link em um navegador da Web, como o Microsoft Internet Explorer. essa ação abre Windows Media Player e, em seguida, baixa e cancela pacotes do pacote de Download de mídia Windows no disco rígido do usuário em uma pasta padrão.

depois que os arquivos tiverem sido extraídos do pacote de Download de mídia Windows, Windows Media Player localizará uma lista de reprodução do metarquivo de mídia Windows com uma extensão de nome de arquivo. asx entre os arquivos empacotados. Se encontrar uma, o Player criará uma lista de reprodução com base no metarquivo incluído. Os arquivos que contêm conteúdo multimídia são então adicionados à biblioteca.

Windows Media Player também procura um elemento **SKIN** no metarquivo. Se o elemento **Skin** contiver uma referência a um arquivo de borda com uma extensão de nome de arquivo. WMZ, o Player carregará a borda no painel **agora em execução** . Em seguida, o Player começa a reproduzir o conteúdo fornecido no pacote.

o diagrama a seguir mostra como o conteúdo é empacotado em um Windows arquivo de Download de mídia, postado em um site, baixado e reproduzido em um computador cliente usando Windows Media Player.

![como um arquivo de download do Windows Media é obtido e reproduzido.](images/wmd-image.png) Windows Download de mídia

a tabela a seguir descreve os três elementos que compõem um pacote de Download de mídia Windows.



| Elemento Package    | Função                                                                                                                                                                                                                                        | Extensões de nome de arquivo                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Borda             | uma interface de usuário fixa e personalizada criada pelo proprietário do conteúdo para exibir, vincular e reproduzir todas as mídias empacotadas no pacote de Download de mídia Windows. As técnicas usadas para criar bordas são semelhantes às usadas para criar capas. | .wmz                                     |
| Playlist de metarquivo  | um Windows metarquivo de mídia que contém elementos de **entrada** , informações de playlist e uma identidade de elemento de **capa** para arquivos de conteúdo.                                                                                                             | .asx                                     |
| Conteúdo multimídia | Um arquivo que contém qualquer formato de áudio ou vídeo com suporte pelo Windows Media Player.                                                                                                                                                          | . WMA,. wmv,. ASF,. wav, .avi, .mpg, .mp3 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Windows Pacotes de download de mídia (preterido)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




