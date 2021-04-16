---
description: Sobre a API de transcodificação
ms.assetid: 54733364-f10c-4c1d-9800-75e283ba4be4
title: Sobre a API de transcodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d2d49a33a97bbb538888173db78705061583ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571069"
---
# <a name="about-the-transcode-api"></a>Sobre a API de transcodificação

O diagrama a seguir mostra como a API de transcodificação está relacionada ao restante do pipeline de codificação de Media Foundation.

![um diagrama que mostra a API de transcodificação.](images/encoding08.png)

O pipeline de codificação contém os seguintes objetos de processamento de dados:

-   Origem da mídia
-   Decodificador
-   Redimensionador de vídeo ou reamostrador de áudio
-   Codificador
-   Coletor de mídia

O redimensionador de vídeo será necessário somente se o tamanho do vídeo de saída diferir da origem. O reamostrador de áudio será necessário somente se o áudio precisar ser reamostrado antes da codificação. O par de decodificador/codificador é necessário para transcodificação, mas não para remuxing.

A *topologia* de codificação é o conjunto de objetos de pipeline (origem, decodificador, redimensionador, reamostrador, codificador e coletor de mídia), além dos pontos de conexão entre eles. Para obter mais informações sobre topologias, consulte [topologias](topologies.md).

Componentes diferentes são responsáveis por criar os vários objetos de pipeline:

-   O aplicativo normalmente usa o [resolvedor de origem](source-resolver.md) para criar a origem da mídia.
-   A [sessão de mídia](media-session.md) carrega e configura o decodificador, o redimensionador de vídeo e o reamostrador de áudio. Internamente, ele usa o carregador de topologia para fazer isso (consulte [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader)).
-   A API de transcodificação carrega e configura o codificador e o coletor de mídia.

Os aplicativos avançados podem configurar o codificador e o coletor de mídia diretamente, em vez de usar a API de transcodificação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API de transcodificação](transcode-api.md)
</dt> <dt>

[Usando a API de transcodificação](fast-transcode-objects.md)
</dt> </dl>

 

 



