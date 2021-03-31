---
title: Configurando fluxos de vídeo para busca de desempenho
description: Configurando fluxos de vídeo para busca de desempenho
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- fluxos, configurando fluxos de vídeo
- codecs, configurando fluxos de vídeo
- fluxos de vídeo, configurando
- fluxos de vídeo, desempenho
- desempenho, fluxos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4fc68e0b3a91cf135d29dc7123d5af88db84c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640130"
---
# <a name="configuring-video-streams-for-seeking-performance"></a>Configurando fluxos de vídeo para busca de desempenho

Alguns aplicativos de reprodução executam muitas buscas em fluxos individuais. A busca é uma área em que o desempenho pode variar muito dependendo das configurações do fluxo. Se você souber que seu conteúdo precisa ser otimizado para busca rápida, você pode personalizar sua configuração de fluxo para melhorar o desempenho.

O maior fator que afeta a velocidade das operações de busca em vídeo é o espaçamento dos quadros-chave. Como cada quadro entre os quadros-chave precisa ser reconstruído com base nos quadros que vier antes dele, quadros-chave amplamente espaçados resultam em tempos de busca mais longos. Por exemplo, se um fluxo de vídeo com 30 quadros por segundo tiver um espaçamento máximo de quadro de chave de 10 segundos, haverá quadros potencialmente 300 entre quadros-chave. Se você buscar até o último [*quadro Delta*](wmformat-glossary.md), 299 quadros precisarão ser reconstruídos para que o quadro seja descompactado. Se cada reconstrução de quadro levou 0,01 segundo, a busca levaria quase 3 segundos. Se você quiser aumentar a eficiência de busca, reduzir o espaçamento de quadro-chave pode ajudar. No entanto, se você definir os quadros-chave muito próximos juntos, poderá perder a qualidade.

Você pode definir o espaçamento máximo de quadro de chave chamando [**IWMVideoMediaProps:: SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing). Os valores recomendados, com base na taxa de bits do fluxo, são listados na tabela a seguir. Esses valores fornecem um bom equilíbrio entre desempenho e qualidade de busca. O SDK não impõe nenhum limite no tempo entre os quadros-chave. Em geral, as vezes mais de 30 segundos podem afetar negativamente os tempos de busca quando o conteúdo é transmitido em uma rede e quando é reproduzido localmente.



| Taxa de bits             | Máximo sugerido de espaçamento de quadro de chave |
|----------------------|-------------------------------------|
| 22 kbps a 300 kbps  | 8 segundos                           |
| 300 kbps a 600 kbps | 6 segundos                           |
| 600 kbps a 2 Mbps   | 4 segundos                           |
| 2 Mbps e superior    | 3 Segundos                           |



 

Para obter mais informações sobre como obter o melhor desempenho ao buscar arquivos de vídeo, consulte [obtendo o melhor desempenho de busca de vídeo](getting-the-best-video-seeking-performance.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurando fluxos**](configuring-streams.md)
</dt> </dl>

 

 




