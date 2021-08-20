---
title: Como Windows pacotes de download de mídia funcionam (preterido)
description: Como Windows pacotes de download de mídia funcionam (preterido)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Windows Metadados de mídia, Windows de download de mídia
- Windows Media Player,Windows de download de mídia
- metafiles, Windows de download de mídia
- Windows Mídia, Windows de Download de Mídia
- Windows Pacotes de Download de Mídia,sobre
- Windows Pacotes de Download de Mídia, como os pacotes funcionam
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
# <a name="how-windows-media-download-packages-work-deprecated"></a>Como Windows pacotes de download de mídia funcionam (preterido)

Esta página documenta um recurso que pode estar indisponível em versões futuras do Windows Media Player e do SDK do Windows Media Player.

Um Windows de Download de Mídia é lançado de um site quando um usuário clica em um link em um navegador da Web, como o Microsoft Internet Explorer. Essa ação abre Windows Media Player e, em seguida, baixa e desembalda o pacote Windows Download de Mídia no disco rígido do usuário em uma pasta padrão.

Depois que os arquivos foram extraídos do pacote de Download de Mídia do Windows, o Windows Media Player localiza uma playlist de metadados de mídia do Windows com uma extensão de nome de arquivo .asx entre os arquivos empacotados. Se encontrar uma, o Player criará uma playlist com base no metadado incluído. Os arquivos que contêm conteúdo multimídia são adicionados à biblioteca.

Windows Media Player também procura um **elemento SKIN** no metadado. Se o **elemento SKIN** contiver uma referência a um arquivo de borda com uma extensão de nome de arquivo .wmz, o Player carregará a borda no painel **Agora Em** reprodução. Em seguida, o Player começa a reproduzir o conteúdo fornecido no pacote.

O diagrama a seguir mostra como o conteúdo é empacotado em um arquivo Windows Media Download, postado em um site, baixado e tocado em um computador cliente usando Windows Media Player.

![como um arquivo de download de mídia do Windows é obtido e interpretado.](images/wmd-image.png) Windows Download de mídia

A tabela a seguir descreve os três elementos que comem um Windows de Download de Mídia.



| Elemento Package    | Função                                                                                                                                                                                                                                        | Extensões de nome de arquivo                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Borda             | Uma interface do usuário fixa e personalizada criada pelo proprietário do conteúdo para exibir, vincular e tocar todas as mídias empacotadas no pacote Windows Download de Mídia. As técnicas usadas para criar bordas são semelhantes às usadas para criar capas. | .wmz                                     |
| Playlist de metadados  | Um Windows media que contém elementos **ENTRY,** informações de playlist e uma identidade **de elemento SKIN** para arquivos de conteúdo.                                                                                                             | .asx                                     |
| Conteúdo multimídia | Um arquivo que contém qualquer formato de áudio ou vídeo com suporte do Windows Media Player.                                                                                                                                                          | .wma, .wmv, .asf, .wav, .avi, .mpg, .mp3 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Windows Pacotes de Download de Mídia (preterido)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




