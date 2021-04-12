---
title: Escolhendo as funções
description: Escolhendo as funções
ms.assetid: ded3c578-5087-4e4f-bf21-2149cf72719d
keywords:
- Capas móveis do Windows Media Player, funções para áudio
- capas, funções de áudio
- Criando capas, funções para áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a139dc21a7d10847a7920955988ec2b02fced0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364353"
---
# <a name="choosing-the-functions"></a>Escolhendo as funções

A finalidade dessa capa é fornecer a funcionalidade básica para a reprodução de áudio. As seguintes funções serão usadas:



| Função                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PlayPause ou PlayPauseStop\* | Iniciar o item de mídia é de importância principal. Se você estiver criando uma capa para o Windows Media Player 10 Mobile ou posterior, use PlayPauseStop. Se você estiver trabalhando com uma versão anterior do Windows Media Player Mobile, deverá usar PlayPause. Ambas as funções oferecem a funcionalidade adicional de pausar, mas somente PlayPauseStop permite que você interrompa uma transmissão ao vivo quando a funcionalidade de pausa não está disponível. |
| Stop                         | Você desejará adicionar parar para parar de executar o item. Se você estiver criando uma capa para o Windows Media Player 10 Mobile ou posterior, a função PlayPauseStop já fornecerá essa funcionalidade.                                                                                                                                                                                                                                          |
| Avançar                         | Se você tiver uma lista de reprodução, será conveniente poder escolher o próximo item. Você precisa disso para a navegação básica de mídia digital.                                                                                                                                                                                                                                                                                                       |
| Prev                         | Embora você possa usar avançar para percorrer a lista de reprodução até chegar ao início, adicionar anterior tornará mais fácil para o usuário voltar e para frente ao navegar na lista de reprodução.                                                                                                                                                                                                                                   |
| VolumeUp ou VolumeDown\*     | Você deverá fornecer ao usuário a capacidade de ativar ou desativar o volume.                                                                                                                                                                                                                                                                                                                                                    |



 

\*Disponível para Windows Media Player 10 Mobile ou posterior.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Guia de aparência**](skin-guide.md)
</dt> </dl>

 

 




