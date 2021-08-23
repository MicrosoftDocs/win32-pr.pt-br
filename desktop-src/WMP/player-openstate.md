---
title: Player.openState
description: A propriedade openState recupera um valor que indica o estado da fonte de conteúdo.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Player.openState Windows Media Player
topic_type:
- apiref
api_name:
- Player.openState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7c0b88d3cab5d5bae4efb1e9a2a5032709943d82484b073302bf0b45a6f5b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995976"
---
# <a name="playeropenstate"></a>Player.openState

A **propriedade openState** recupera um valor que indica o estado da fonte de conteúdo.

## <a name="syntax"></a>Syntax

*player* . **openState**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um Número somente **leitura** (**long**). A constante de enumeração de estilo C pode ser derivada prefixando o valor de estado com "wmpos". Por exemplo, a constante para o estado PlaylistOpening **é wmposPlaylistOpening.**



| Valor | Estado                   | Descrição                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Indefinido               | Windows Media Player está em um estado indefinido.                                                                                                         |
| 1     | PlaylistChanging        | A nova playlist está prestes a ser carregada.                                                                                                                    |
| 2     | PlaylistLocando        | Windows Media Player está tentando localizar a playlist. A playlist pode ser local (biblioteca ou metarquivo com uma extensão de nome de arquivo .asx) ou remota. |
| 3     | PlaylistConnecting      | Conectando-se à playlist.                                                                                                                            |
| 4     | PlaylistLoading         | A playlist foi encontrada e agora está sendo recuperada.                                                                                                    |
| 5     | PlaylistOpening         | A playlist foi recuperada e agora está sendo analisado e carregado.                                                                                        |
| 6     | PlaylistOpenNoMedia     | A playlist está aberta.                                                                                                                                      |
| 7     | PlaylistChanged         | Uma nova playlist foi atribuída a **currentPlaylist.**                                                                                               |
| 8     | MediaChanging           | Um novo item de mídia está prestes a ser carregado.                                                                                                                |
| 9     | Localização de mídia           | Windows Media Player está localizando o item de mídia. O arquivo pode ser local ou remoto.                                                                      |
| 10    | MediaConnecting         | Conectando-se ao servidor que contém o item de mídia.                                                                                                    |
| 11    | MediaLoading            | O item de mídia foi localizado e agora está sendo recuperado.                                                                                                |
| 12    | MediaOpening            | O item de mídia foi recuperado e agora está sendo aberto.                                                                                                 |
| 13    | MediaOpen               | O item de mídia agora está aberto.                                                                                                                                |
| 14    | BeginCodecAcquisition   | Iniciando a aquisição de codec.                                                                                                                            |
| 15    | EndCodecAcquisition     | A aquisição do Codec foi concluída.                                                                                                                         |
| 16    | BeginLicenseAcquisition | Adquirir uma licença para reproduzir conteúdo protegido por DRM.                                                                                                     |
| 17    | EndLicenseAcquisition   | A licença para reproduzir conteúdo protegido por DRM foi adquirida.                                                                                               |
| 18    | BeginIndividualization  | Inicie a individualização do DRM.                                                                                                                           |
| 19    | EndIndividualization    | A individualização do DRM foi concluída.                                                                                                              |
| 20    | MediaWaiting            | Aguardando o item de mídia.                                                                                                                                |
| 21    | OpeningUnknownURL       | Abrir uma URL com um tipo desconhecido.                                                                                                                    |



 

## <a name="remarks"></a>Comentários

Windows Media Player não há garantia de que ocorram em nenhuma ordem específica. Além disso, nem todos os estados ocorrem necessariamente durante uma sequência de eventos. Você não deve escrever código que depende da ordem de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Player**](player-object.md)
</dt> <dt>

[**Evento Player.OpenStateChange**](player-player-openstatechange.md)
</dt> </dl>

 

 





