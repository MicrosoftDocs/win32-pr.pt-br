---
description: Sobre a API transcódigo
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: Sobre a API transcódigo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca7a5c39ebb4527a615c4c488239a1da4b88283f66199d25f6613a8d1f9bd82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449766"
---
# <a name="about-the-transcode-api"></a>Sobre a API transcódigo

O diagrama a seguir mostra como a API de transcódigo está relacionada ao restante do pipeline Media Foundation codificação.

![um diagrama que mostra a API de transcodificar.](images/encoding08.png)

O pipeline de codificação contém os seguintes objetos de processamento de dados:

-   Fonte de mídia
-   Decodificador
-   Ressampler de áudio ou ressemplor de vídeo
-   Codificador
-   Sink de mídia

O resizer de vídeo só será necessário se o tamanho do vídeo de saída for diferente da origem. O resampler de áudio só será necessário se o áudio precisar ser resamplado antes da codificação. O par de decodificador/codificador é necessário para transcodificação, mas não para remuxing.

A topologia de *codificação* é o conjunto de objetos de pipeline (origem, decodificador, resizer, resampler, codificador e sink de mídia), além dos pontos de conexão entre eles. Para obter mais informações sobre topologias, consulte [Topologias](topologies.md).

Componentes diferentes são responsáveis por criar os vários objetos de pipeline:

-   O aplicativo normalmente usa o Resolvedor [de Origem](source-resolver.md) para criar a fonte de mídia.
-   A [Sessão de](media-session.md) Mídia carrega e configura o decodificador, o ressizer de vídeo e o resampledor de áudio. Internamente, ele usa o carregador de topologia para fazer isso (consulte [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).
-   A API de transcodificar carrega e configura o codificador e o sink de mídia.

Aplicativos avançados podem configurar o codificador e o sink de mídia diretamente, em vez de usar a API de transcodificar.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API de transcodificar](transcode-api.md)
</dt> <dt>

[Usando a API transcódigo](fast-transcode-objects.md)
</dt> </dl>

 

 



