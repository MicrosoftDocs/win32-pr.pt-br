---
title: Configurando o vídeo Fluxos para buscar o desempenho
description: Configurando o vídeo Fluxos para buscar o desempenho
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- fluxos, configurando fluxos de vídeo
- codecs, configurando fluxos de vídeo
- fluxos de vídeo, configurando
- fluxos de vídeo, desempenho
- desempenho, fluxos de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b7a21e6352d03375b680702a16190b4af9eef24ca7ba9d592adb79ab5794b5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840156"
---
# <a name="configuring-video-streams-for-seeking-performance"></a>Configurando o vídeo Fluxos para buscar o desempenho

Alguns aplicativos de reprodução executam muita busca em fluxos individuais. A busca é uma área em que o desempenho pode variar muito dependendo das configurações do fluxo. Se você sabe que seu conteúdo precisa ser otimizado para busca rápida, você pode adaptar sua configuração de fluxo para melhorar o desempenho.

O maior fator que afeta a velocidade de busca de operações em vídeo é o espaçamento dos quadros-chave. Como cada quadro entre quadros-chave precisa ser reconstruído com base nos quadros que vêm antes dele, quadros-chave amplamente espamados resultam em tempos de busca mais longos. Por exemplo, se um fluxo de vídeo com 30 quadros por segundo tiver um espaçamento máximo de quadro-chave de 10 segundos, haverá potencialmente 300 quadros entre quadros-chave. Se você buscar até o último [*quadro delta,*](wmformat-glossary.md)299 quadros deverão ser reconstruídos para que o quadro seja descompactado. Se cada reconstrução de quadro levou 0,01 segundo, a busca levará quase 3 segundos. Se você quiser aumentar a eficiência da busca, reduzir o espaçamento de quadro-chave pode ajudar. No entanto, se você definir os quadros-chave muito próximos, poderá perder a qualidade.

Você pode definir o espaçamento máximo do quadro-chave chamando [**IWMVideoMediaProps::SetMaxKeyFrameSpacing.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing) Os valores recomendados, com base na taxa de bits do fluxo, são listados na tabela a seguir. Esses valores fornecem um bom equilíbrio de busca de desempenho e qualidade. O SDK não impõe nenhum limite de tempo entre quadros-chave. Em geral, tempos maiores que 30 segundos podem afetar negativamente os tempos de busca quando o conteúdo é transmitido por uma rede e quando ele é tocado localmente.



| Taxa de bits             | Espaçamento máximo de quadro-chave sugerido |
|----------------------|-------------------------------------|
| 22 Kbps a 300 Kbps  | 8 segundos                           |
| 300 Kbps a 600 Kbps | 6 segundos                           |
| 600 Kbps a 2 Mbps   | 4 segundos                           |
| 2 Mbps e superior    | 3 Segundos                           |



 

Para obter mais informações sobre como obter o melhor desempenho ao buscar arquivos de vídeo, consulte [Obter o melhor desempenho de busca de vídeo.](getting-the-best-video-seeking-performance.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configurando Fluxos**](configuring-streams.md)
</dt> </dl>

 

 




