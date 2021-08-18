---
title: Escolhendo as funções
description: Escolhendo as funções
ms.assetid: ded3c578-5087-4e4f-bf21-2149cf72719d
keywords:
- Windows Media Player Capas móveis, funções para áudio
- skins, funções para áudio
- criando capas, funções para áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222a7a6b26b225b0c40e461833f731c477c84338c458f88074fd747c33a1e70e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119828"
---
# <a name="choosing-the-functions"></a>Escolhendo as funções

A finalidade dessa capa é fornecer funcionalidade básica para reprodução de áudio. As seguintes funções serão usadas:



| Função                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PlayPause ou PlayPauseStop\* | Iniciar o item de mídia é de grande importância. Se você estiver criando uma capa para o Windows Media Player 10 Mobile ou posterior, use PlayPauseStop. Se você estiver trabalhando com uma versão anterior do Windows Media Player Mobile, deverá usar o PlayPause. Ambas as funções dão a você a funcionalidade adicionada de pausa, mas somente PlayPauseStop permite que você pare uma difusão ao vivo quando a funcionalidade de pausa não estiver disponível. |
| Stop                         | Você deseja adicionar Parar para interromper a reprodução do item. Se você estiver criando uma capa para Windows Media Player 10 Mobile ou posterior, a função PlayPauseStop já fornece essa funcionalidade.                                                                                                                                                                                                                                          |
| Avançar                         | Se você tiver uma playlist, poderá escolher o próximo item. Você precisa disso para a navegação básica da mídia digital.                                                                                                                                                                                                                                                                                                       |
| Prev                         | Embora você possa usar Avançar para navegar pela playlist até chegar ao início, adicionar Prev facilitará o retrocesso do usuário e o encaminhamento ao navegar pela playlist.                                                                                                                                                                                                                                   |
| VolumeUp ou VolumeDown\*     | Você deseja fornecer ao usuário a capacidade de ativar ou desativar o volume.                                                                                                                                                                                                                                                                                                                                                    |



 

\*Disponível para o Windows Media Player 10 Mobile ou posterior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de capa**](skin-guide.md)
</dt> </dl>

 

 




