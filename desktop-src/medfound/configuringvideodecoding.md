---
description: Configurando a decodificação de vídeo
ms.assetid: 897b8e2d-9827-428d-91ae-632038c4c8c0
title: Configurando a decodificação de vídeo (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7c49d42b47b4b6745731287e2b0bf0ee2d21c1eb503ed561274a5fb4cc8b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035334"
---
# <a name="configuring-video-decoding-microsoft-media-foundation"></a>Configurando a decodificação de vídeo (Microsoft Media Foundation)

A decodificação é essencialmente o oposto da codificação em termos de configuração. O decodificador dá suporte a poucas propriedades e nenhuma delas é necessária. De definir o tipo de entrada para o tipo usado para a saída do decodificador (incluindo os dados particulares do codec). Em seguida, de definir a saída para o formato descompactado desejado, de definir a estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) para refletir o tamanho adequado do quadro e iniciar o processamento de exemplos.

Você deve fornecer ao decodificador um tipo de mídia que inclua os dados particulares do codec posicionados imediatamente após a [**estrutura VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) O decodificador não pode decodificar o conteúdo sem esses dados. A validação de formato executada pelo decodificador não valida os dados privados. Se os dados particulares do codec estão ausentes ou incorretos, o decodificador responde como se o fluxo de bits estivesse corrompido. Para obter mais informações, consulte [Using Video Codec Private Data](usingvideocodecprivatedata.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando dados privados do Codec de Vídeo](usingvideocodecprivatedata.md)
</dt> <dt>

[Trabalhando com vídeo](workingwithvideo.md)
</dt> </dl>

 

 
