---
description: Requisitos para decodificadores
ms.assetid: 149aea20-0d37-4b1c-a098-8446c4088ce1
title: Requisitos para decodificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a84d02926b4ce36cea9e4221589d52690edb8e256b2f0f4863fa19fff5dc033
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697026"
---
# <a name="requirements-for-decoders"></a>Requisitos para decodificadores

Os decodificadores que fornecem amostras para o VMR devem observar as seguintes regras:

-   Deve haver um quadro de subimagem entregue ao VMR para cada quadro de vídeo. Os dois quadros devem ter os mesmos carimbos de data/hora.
-   Se a subimagem não tiver sido alterada, use o \_ sinalizador am gbf \_ NOTASYNCPOINT no método [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) para forçar o alocador a retornar um buffer que contém o último quadro entregue ao VMR. Basta colocar um novo carimbo de data/hora no exemplo e entregá-lo ao VMR novamente. Se a fama da subimagem estiver em branco, você ainda deverá entregá-la. O VMR detectará o quadro vazio e não o mesclará com o vídeo. Esse teste é executado pelo chip VGA e não afeta o desempenho da reprodução.
-   Todos os exemplos, exceto para transmissões ao vivo, devem ter carimbos de hora de início e parada válidos anexados. (O DVD não é um fluxo ao vivo.)
-   Os carimbos de data/hora de exemplo de mídia devem ser contíguos
-   O decodificador deve se identificar como compatível com o VMR para uso por construtores de grafo.
-   O fluxo de subimagem agora deve conter valores Alfa inseridos por pixel. O tipo de superfície ARGB4444 é ideal para subimagems.
-   Não assuma que o stride da subimagem seja igual à largura da superfície. Isso nem sempre acontece com o VMR.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a aceleração de vídeo do DirectX](about-directx-video-acceleration.md)
</dt> </dl>

 

 



