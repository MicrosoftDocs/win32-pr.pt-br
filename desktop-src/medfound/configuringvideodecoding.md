---
description: Configurando decodificação de vídeo
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Configurando a decodificação de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f386e3dbb39d6296756f2fe8eec1b94c5533bff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782388"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a>Configurando a decodificação de vídeo (Microsoft Media Foundation)

A decodificação é essencialmente o oposto da codificação em termos de configuração. O decodificador dá suporte a poucas propriedades, e nenhuma delas é necessária. Defina o tipo de entrada para o tipo usado para a saída do decodificador (incluindo os dados privados do codec). Em seguida, defina a saída para o formato descompactado desejado, defina a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para refletir o tamanho do quadro apropriado e comece a processar exemplos.

Você deve fornecer o decodificador com um tipo de mídia que inclua os dados privados do codec posicionados imediatamente após a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) . O decodificador não pode decodificar o conteúdo sem esses dados. A validação de formato executada pelo decodificador não valida os dados privados. Se os dados privados do codec estiverem ausentes ou incorretos, o decodificador responderá como se o fluxo de bits estiver corrompido. Para obter mais informações, consulte [usando dados privados do codec de vídeo](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando dados privados do codec de vídeo](usingvideocodecprivatedata.md)
</dt> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 
