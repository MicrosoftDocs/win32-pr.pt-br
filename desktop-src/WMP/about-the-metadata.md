---
title: Sobre os metadados
description: Sobre os metadados
ms.assetid: bdb35606-7861-4f97-aae5-4f7f3ed48106
keywords:
- Windows Media Player, metadados
- metadados, sobre
- metadados, atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a1c2e9782b52adc274a5b3dbaf16c48ed1a892e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291819"
---
# <a name="about-the-metadata"></a>Sobre os metadados

O Windows Media Player 10 ou posterior tenta sincronizar os seguintes atributos de metadados.



| Atributo do Player | Constante global WMDM  | Descrição                                                                                                 | Versão necessária                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| AlbumArtist      | g \_ wszWMDMAlbumArtist | **Cadeia de caracteres** terminada em nulo que contém o nome do artista principal para o álbum.                         | Windows Media Player 11 ou posterior. |
| Álbuns            | g \_ wszWMDMAlbumTitle  | **Cadeia de caracteres** terminada em nulo que contém o título do álbum no qual o conteúdo foi originalmente lançado.  | Windows Media Player 11 ou posterior. |
| Autor           | g \_ wszWMDMAuthor      | **Cadeia de caracteres** terminada em nulo que contém o nome do artista de mídia ou ator associado ao conteúdo.    | Windows Media Player 11 ou posterior. |
| BuyNow           | g \_ wszWMDMBuyNow      | **Booliano** que indica se o usuário optou por comprar o conteúdo.                                 | Windows Media Player 10 ou posterior. |
| WM/gênero         | g \_ wszWMDMGenre       | **Cadeia de caracteres** terminada em nulo que contém o gênero do conteúdo.                                             | Windows Media Player 11 ou posterior. |
| UserPlayCount    | g \_ wszWMDMPlayCount   | **DWORD** que contém o número de vezes que o usuário reproduziu o arquivo de mídia digital.                        | Windows Media Player 10 ou posterior. |
| Liberado      | g \_ wszWMDMYear        | A data da versão original do item.                                                               | Windows Media Player 11 ou posterior. |
| Título            | g \_ wszWMDMTitle       | **Cadeia de caracteres** terminada em nulo que contém o título.                                                            | Windows Media Player 11 ou posterior. |
| WM/TrackNumber   | g \_ wszWMDMTrack       | **DWORD** que contém o número de faixa do item no álbum no qual ele foi originalmente lançado.         | Windows Media Player 11 ou posterior. |
| UserRating       | g \_ wszWMDMUserRating  | **DWORD** que contém um valor que representa a classificação em estrela que o usuário especificou para o arquivo de mídia digital. | Windows Media Player 10 ou posterior. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Extensões de dispositivo para transferência de metadados acelerada**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




