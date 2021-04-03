---
title: Como os pacotes de download do Windows Media funcionam (preteridos)
description: Como os pacotes de download do Windows Media funcionam (preteridos)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Metaarquivos do Windows Media, pacotes de download do Windows Media
- Windows Media Player, pacotes de download do Windows Media
- metaarquivos, pacotes de download do Windows Media
- Windows Media, pacotes de download do Windows Media
- Pacotes de download do Windows Media, sobre
- Pacotes de download do Windows Media, como os pacotes funcionam
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084062"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a>Como os pacotes de download do Windows Media funcionam (preteridos)

Esta página documenta um recurso que pode não estar disponível em versões futuras do Windows Media Player e no SDK do Windows Media Player.

Um pacote de download do Windows Media é iniciado em um site quando um usuário clica em um link em um navegador da Web, como o Microsoft Internet Explorer. Essa ação abre o Windows Media Player e, em seguida, baixa e cancela pacotes do pacote de download do Windows Media no disco rígido do usuário em uma pasta padrão.

Depois que os arquivos tiverem sido extraídos do pacote de download do Windows Media, o Windows Media Player localizará uma lista de reprodução do metarquivo do Windows Media com uma extensão de nome de arquivo. asx entre os arquivos empacotados. Se encontrar uma, o Player criará uma lista de reprodução com base no metarquivo incluído. Os arquivos que contêm conteúdo multimídia são então adicionados à biblioteca.

O Windows Media Player também procura um elemento **Skin** no metarquivo. Se o elemento **Skin** contiver uma referência a um arquivo de borda com uma extensão de nome de arquivo. WMZ, o Player carregará a borda no painel **agora em execução** . Em seguida, o Player começa a reproduzir o conteúdo fornecido no pacote.

O diagrama a seguir mostra como o conteúdo é empacotado em um arquivo de download do Windows Media, Postado em um site, baixado e reproduzido em um computador cliente usando o Windows Media Player.

![como um arquivo de download do Windows Media é obtido e reproduzido.](images/wmd-image.png) Download do Windows Media

A tabela a seguir descreve os três elementos que compõem um pacote de download do Windows Media.



| Elemento Package    | Função                                                                                                                                                                                                                                        | Extensões de nome de arquivo                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Borda             | Uma interface de usuário fixa e personalizada criada pelo proprietário do conteúdo para exibir, vincular e reproduzir todas as mídias empacotadas no pacote de download do Windows Media. As técnicas usadas para criar bordas são semelhantes às usadas para criar capas. | .wmz                                     |
| Playlist de metarquivo  | Um metarquivo do Windows Media que contém elementos de **entrada** , informações de playlist e uma identidade de elemento de **capa** para arquivos de conteúdo.                                                                                                             | .asx                                     |
| Conteúdo multimídia | Um arquivo que contém qualquer formato de áudio ou vídeo com suporte no Windows Media Player.                                                                                                                                                          | . WMA,. wmv,. ASF,. wav,. avi,. mpg,. mp3 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Pacotes de download do Windows Media (preterido)**](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




