---
description: Propriedades de exemplo do MPEG
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: Propriedades de exemplo do MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c78872b41c579f6af594280b064bfbefc65ef13e8b9d4abf8c21ba9b19613bcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075786"
---
# <a name="mpeg-sample-properties"></a>Propriedades de exemplo do MPEG

Os exemplos de MPEG têm as seguintes características.

**Carimbos de Data/Hora**

Nem todos os exemplos têm horários de início e de parada. O tempo de parada de exemplo para dados de pacote e de carga não é útil; geralmente é definido como a hora de início mais um. Os exemplos de dados de pacote ou de carga MPEG terão um tempo de início e de parada definido se o pacote da camada do sistema de que eles são gerados tiver um PTS válido.

Para obter mais informações sobre carimbos de data/hora, consulte a seção 2.4.1 de ISO1-11172: "O título do pacote pode conter carimbos de data/hora de decodificação e/ou de apresentação (DTS e PTS) que se referem à primeira unidade de acesso no pacote."

Para tipos principais de Fluxo MPEG, a hora de início é a posição de byte do primeiro byte, classificada em \_ 1 byte por segundo. A hora de parada é a posição de byte do último byte. Portanto, exemplos consecutivos devem ter a hora de parada do primeiro pacote igual à hora de início do próximo pacote. Para CD de vídeo dados, a origem do meio deve corresponder ao formato de um arquivo de CD de vídeo exposto pelo CDFS com a parte STANDARD DOIS no início.

Para tipos de carga e pacote de vídeo MPEG, o carimbo de data/hora é a hora de apresentação do primeiro quadro de vídeo cujo código de início de imagem começa no exemplo.

Para tipos de conteúdo e pacote de áudio MPEG, o carimbo de data/hora é a hora de apresentação do primeiro quadro de áudio cujo código de sincronização começa no exemplo.

Supõe-se que os dados de pacote e conteúdo sem carimbos de data/hora possam ser previamente previamente pré-coletados pelos filtros de manipulação.

**Descontinuidades**

Se houver uma interrupção no fluxo (por exemplo, uma lacuna nos dados em tempo real ou um erro nos dados ou após uma busca), a propriedade de descontinuidade será definida no próximo exemplo de mídia. Isso também permite uma descontinuidade de carimbo de data/hora.

**Notificações de fim de fluxo**

Quando o decodificador recebe essa notificação, ele deve processar todos os dados armazenados em buffer. Todos os novos dados devem começar com a propriedade de descontinuidade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a MPEG-2 no DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



