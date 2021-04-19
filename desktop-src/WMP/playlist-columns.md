---
title: LISTA de reprodução. colunas
description: O atributo Columns define as colunas que aparecem no elemento PLAYLIST.
ms.assetid: a805ee06-cf73-4eab-bcda-c374e55cd11a
keywords:
- PLAYLIST. Columns Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.columns
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc5f8ef5dc76428ca892d079b60692e6949a5ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764149"
---
# <a name="playlistcolumns"></a>LISTA de reprodução. colunas

O atributo **Columns** define as colunas que aparecem no elemento **playlist** .

``` syntax
        elementID.columns
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação no seguinte formato:

nome do banco de BD \_ = \_ nome amigável; nome do banco de BD \_ = \_ nome amigável;

\_Nome amigável é o valor mostrado no cabeçalho da coluna do elemento playlist e \_ nome do BD é um valor da tabela a seguir. Observe que um item de playlist pode ser um item de mídia da biblioteca ou de um CD, ou pode ser outra **playlist** que seja criada pelo usuário ou extraída de um CD. Algumas colunas são válidas somente com determinados itens da lista de reprodução, conforme indicado na coluna Descrição.



| Valor             | Descrição                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| Álbuns             | O nome do álbum. Usado somente com itens de mídia.                                                                      |
| Autor            | O nome do artista. Não usado com listas de reprodução criadas pelo usuário.                                                           |
| Autor            | O nome do artista.                                                                                                 |
| Bitrate           | A taxa de bits do conteúdo. Usado somente com itens de mídia da biblioteca.                                               |
| CDTrackEnabled    | Indica se a faixa do CD está habilitada. Usado somente com itens de mídia de CD.                                               |
| Verificado           | Reservado para uso futuro.                                                                                                |
| Direitos autorais         | Os direitos autorais da lista de reprodução. Não usado com playlists de CD ou itens de mídia.                                               |
| CreationDate      | A data e a hora em que a entrada na biblioteca foi criada. Usado somente com itens da biblioteca.                     |
| DigitallySecure   | Indica se o item está protegido com o Windows Media Rights Manager. Usado somente com itens de mídia da biblioteca. |
| Duration          | A duração do item de mídia.                                                                                         |
| FileType          | Reservado para uso futuro.                                                                                                |
| Gênero             | O gênero da lista de reprodução. Não usado com listas de reprodução de CDs.                                                            |
| Mediaattribute    | Reservado para uso futuro.                                                                                                |
| MediaType         | O tipo do item de mídia (áudio ou vídeo).                                                                            |
| Metadataização    | A origem dos metadados para esta faixa de CD (AMG, WindowsMedia.com e assim por diante). Usado somente com itens de mídia de CD.         |
| ModifiedBy        | Reservado para uso futuro.                                                                                                |
| Nome              | O nome da lista de reprodução.                                                                                               |
| OriginalIndex     | Se aplicável, o identificador de faixa do CD correspondente. Usado somente com itens de mídia de CD.                                    |
| PlayCount         | O número de vezes que o conteúdo foi reproduzido até o fim. Usado somente com itens de mídia da biblioteca.        |
| Playlistattribute | Reservado para uso futuro.                                                                                                |
| Classificação            | Reservado para uso futuro.                                                                                                |
| SourceURL         | O caminho ou a URL para o conteúdo. Usado somente com itens de mídia da biblioteca.                                            |
| Status            | O status de cópia de uma faixa de CD que está sendo copiada. Usado somente com itens de mídia de CD.                                           |
| Estilo             | Reservado para uso futuro.                                                                                                |
| SUMÁRIO               | Se aplicável, o identificador de Sumário do CD correspondente. Não usado com listas de reprodução criadas pelo usuário.                 |



 

## <a name="remarks"></a>Comentários

Se uma das colunas não existir na biblioteca, ela será deixada em branco.

Um máximo de 31 colunas pode ser especificado.

Se você especificar uma coluna duplicada, os dados na primeira coluna serão alinhados à esquerda, mas todas as outras colunas duplicadas serão alinhadas à direita. Por exemplo, se você tiver duas colunas Duration, os dados serão alinhados à esquerda no primeiro e alinhado à direita no segundo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. columnsVisible**](playlist-columnsvisible.md)
</dt> </dl>

 

 





