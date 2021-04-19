---
description: Propriedades de exemplo de MPEG
ms.assetid: 339aab84-e5ad-4071-8b67-2b04cb17e450
title: Propriedades de exemplo de MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c20df4b9285a77d00bd98bc6f21558f0d6b3c60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105810933"
---
# <a name="mpeg-sample-properties"></a>Propriedades de exemplo de MPEG

Exemplos de MPEG têm as seguintes características.

**Carimbos de Data/Hora**

Nem todas as amostras têm horários de início e parada. O tempo de parada de exemplo para dados de pacote e carga não é útil; Normalmente, ela é definida como a hora de início mais uma. Os exemplos de dados de pacote ou de carga MPEG terão um horário de início e de parada definido se o pacote da camada do sistema do qual eles são gerados tiver um PTS válido.

Para obter mais informações sobre carimbos de data/hora, consulte a seção 2.4.1 de ISO1-11172: "o cabeçalho do pacote pode conter decodificação e/ou carimbos de data/hora (DTS e PTS) que se referem à primeira unidade de acesso no pacote."

Para \_ tipos principais de fluxo MPEG, a hora de início é a posição de byte do primeiro byte, classificada em 1 byte por segundo. A hora de parada é a posição de byte do último byte. Portanto, os exemplos consecutivos devem ter a hora de parada do primeiro pacote igual à hora de início do próximo pacote. Para dados de CD de vídeo, a origem da mídia deve corresponder ao formato de um arquivo de vídeo-CD exposto por CDFS com a parte padrão do RIFF no início.

Para os tipos de conteúdo e pacote de vídeo MPEG, o carimbo de data/hora é o tempo de apresentação para o primeiro quadro de vídeo cujo código de início de imagem começa no exemplo.

Para tipos de carga e pacote de áudio MPEG, o carimbo de data/hora é o tempo de apresentação para o primeiro quadro de áudio cujo código de sincronização começa no exemplo.

Supõe-se que os dados de pacote e carga sem carimbos de data/hora possam ser registrados com êxito pelos filtros de manipulação.

**Descontinuidades**

Se houver uma interrupção no fluxo (por exemplo, uma lacuna nos dados em tempo real ou um erro nos dados ou após uma busca), a propriedade de descontinuidade será definida no exemplo de mídia seguinte. Isso também permite uma descontinuidade de carimbo de data/hora.

**Notificações de fim de fluxo**

Quando o decodificador recebe essa notificação, ele deve processar dados armazenados em buffer. Todos os novos dados devem começar com a propriedade de descontinuidade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Suporte a MPEG-2 no DirectShow](mpeg-2-support-in-directshow.md)
</dt> </dl>

 

 



