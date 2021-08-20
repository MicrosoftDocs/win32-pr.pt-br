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
ms.openlocfilehash: 2dcccda2af46e60e4bb0733d17e35e1a50d1fe923e9775fa6b10d2c06e3a972a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865356"
---
# <a name="about-the-metadata"></a>Sobre os metadados

o Windows Media Player 10 ou posterior tenta sincronizar os atributos de metadados a seguir.



| Atributo do Player | Constante global WMDM  | Descrição                                                                                                 | Versão necessária                  |
|------------------|-----------------------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| AlbumArtist      | g \_ wszWMDMAlbumArtist | **Cadeia de caracteres** terminada em nulo que contém o nome do artista principal para o álbum.                         | Windows Media Player 11 ou posterior. |
| Álbum            | g \_ wszWMDMAlbumTitle  | **Cadeia de caracteres** terminada em nulo que contém o título do álbum no qual o conteúdo foi originalmente lançado.  | Windows Media Player 11 ou posterior. |
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

 

 




