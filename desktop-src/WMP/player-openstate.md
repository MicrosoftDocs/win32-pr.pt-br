---
title: Player. openState
description: A propriedade OpenState recupera um valor que indica o estado da fonte de conteúdo.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Player. OpenState do Windows Media Player
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
ms.openlocfilehash: b87ad682a0c9ea6420ec291cbe66a7f81c9062e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791518"
---
# <a name="playeropenstate"></a>Player. openState

A propriedade **OpenState** recupera um valor que indica o estado da fonte de conteúdo.

## <a name="syntax"></a>Syntax

*Player* . **OpenState**

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**longo**). A constante de enumeração de estilo C pode ser derivada pela prefixação do valor de estado com "wmpos". Por exemplo, a constante para o estado PlaylistOpening é **wmposPlaylistOpening**.



| Valor | Estado                   | Descrição                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Indefinido               | O Windows Media Player está em um estado indefinido.                                                                                                         |
| 1     | PlaylistChanging        | A nova Playlist está prestes a ser carregada.                                                                                                                    |
| 2     | PlaylistLocating        | O Windows Media Player está tentando localizar a lista de reprodução. A lista de reprodução pode ser local (biblioteca ou metarquivo com uma extensão de nome de arquivo. asx) ou remoto. |
| 3     | PlaylistConnecting      | Conectando-se à lista de reprodução.                                                                                                                            |
| 4     | PlaylistLoading         | A playlist foi encontrada e agora está sendo recuperada.                                                                                                    |
| 5     | PlaylistOpening         | A playlist foi recuperada e agora está sendo analisada e carregada.                                                                                        |
| 6     | PlaylistOpenNoMedia     | A playlist está aberta.                                                                                                                                      |
| 7     | Playlistchanged         | Uma nova lista de reprodução foi atribuída a **currentPlaylist**.                                                                                               |
| 8     | MediaChanging           | Um novo item de mídia está prestes a ser carregado.                                                                                                                |
| 9     | MediaLocating           | O Windows Media Player está localizando o item de mídia. O arquivo pode ser local ou remoto.                                                                      |
| 10    | MediaConnecting         | Conectando-se ao servidor que contém o item de mídia.                                                                                                    |
| 11    | MediaLoading            | O item de mídia está localizado e agora está sendo recuperado.                                                                                                |
| 12    | MediaOpening            | O item de mídia foi recuperado e agora está sendo aberto.                                                                                                 |
| 13    | MediaOpen               | O item de mídia está aberto agora.                                                                                                                                |
| 14    | BeginCodecAcquisition   | Iniciando a aquisição do codec.                                                                                                                            |
| 15    | EndCodecAcquisition     | A aquisição do codec foi concluída.                                                                                                                         |
| 16    | BeginLicenseAcquisition | Aquisição de uma licença para reproduzir conteúdo protegido por DRM.                                                                                                     |
| 17    | EndLicenseAcquisition   | A licença para reproduzir conteúdo protegido por DRM foi adquirida.                                                                                               |
| 18    | BeginIndividualization  | Inicie a individualização DRM.                                                                                                                           |
| 19    | Endindividualização    | A individualização de DRM foi concluída.                                                                                                              |
| 20    | MediaWaiting            | Aguardando item de mídia.                                                                                                                                |
| 21    | OpeningUnknownURL       | Abrindo uma URL com um tipo desconhecido.                                                                                                                    |



 

## <a name="remarks"></a>Comentários

Não há garantia de que os Estados do Windows Media Player ocorram em uma ordem específica. Além disso, nem todo estado ocorre necessariamente durante uma sequência de eventos. Você não deve escrever código que dependa da ordem de estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de jogador**](player-object.md)
</dt> <dt>

[**Evento Player. OpenStateChange**](player-player-openstatechange.md)
</dt> </dl>

 

 





