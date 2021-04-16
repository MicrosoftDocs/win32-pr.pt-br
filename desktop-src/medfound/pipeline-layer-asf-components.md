---
description: No modelo de pipeline do Media Foundations, uma fonte de mídia é conectada a uma transformação que é ainda mais conectada a um coletor de mídia.
ms.assetid: 55ab3a53-d9fd-438c-998c-8888f99958ce
title: Componentes ASF da camada de pipeline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b3b6eb2d00404d193e50cebf174210a1c25655e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105808214"
---
# <a name="pipeline-layer-asf-components"></a>Componentes ASF da camada de pipeline

No modelo de pipeline do Media Foundation, uma fonte de mídia é conectada a uma transformação que está mais conectada a um coletor de mídia. Os dados contidos na origem fluem pela transformação e gera amostras de mídia de saída no coletor para fins de reprodução ou codificação. Dependendo se o aplicativo deseja reproduzir o conteúdo ASF ou codificar em um arquivo ASF, o aplicativo deve criar o pipeline de forma diferente.

Os tópicos a seguir contêm informações sobre os componentes da camada de pipeline.

-   [Fonte de mídia ASF](asf-media-source.md)
-   [Codificadores de mídia do Windows](windows-media-encoders.md)
-   [Coletores de mídia ASF](asf-media-sinks.md)

Os três componentes principais de um pipeline ASF para reprodução são os seguintes:

-   A fonte de mídia ASF é fornecida por Media Foundation que representa um arquivo ASF.
-   Reamostragens de áudio, redimensionadores de imagem de vídeo, etc., (transformação)
-   Renderizador de áudio e vídeo (coletores)

Para obter informações sobre como criar um pipeline de reprodução, consulte [criando topologias de reprodução](creating-playback-topologies.md).

Os três componentes principais de um pipeline ASF para codificação são os seguintes:

-   Fonte de mídia que representa os dados em um formato que precisa ser convertido. Esse componente pode ser uma das fontes de mídia padrão fornecidas pelo Media Foundation ou uma fonte personalizada que expõe a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) .
-   Codificadores de mídia do Windows (transformação) que executam a conversão de formato.
-   Coletores de mídia ASF fornecidos por Media Foundation que gravam objetos ASF e amostras de mídia em um arquivo de saída especificado pelo aplicativo.

O pipeline é representado em uma topologia e cada objeto no pipeline é representado por um nó de topologia. Para reprodução e codificação, todas as operações de pipeline são tratadas pela sessão de mídia. Uma das responsabilidades da sessão de mídia é garantir que o pipeline tenha todos os componentes necessários para gerar a saída. Por exemplo, em um pipeline de codificação, se o formato de fonte de áudio for diferente do formato de destino, a sessão de mídia inserirá componentes de transformação adicionais, como o reamostrador que executa conversões de taxa de amostra apropriadas. O controle de fluxo de dados por meio do pipeline também é gerenciado pela sessão de mídia. Em um cenário de reprodução, iniciar a sessão de mídia a sessão de mídia envia amostras para SAR e EVR, que as renderiza no dispositivo de saída. Para codificação, iniciar a sessão de mídia inicia o processo de codificação. A sessão notifica de forma assíncrona o aplicativo quando a codificação é concluída.

O tópico a seguir contém instruções passo a passo sobre como usar os componentes da camada de pipeline para criar uma topologia de codificação. componentes para leitura e gravação de arquivos ASF.

-   [Tutorial: 1-transmitir codificação de mídia do Windows](tutorial--1-pass-windows-media-encoding.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



