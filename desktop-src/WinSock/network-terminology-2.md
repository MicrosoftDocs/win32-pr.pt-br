---
description: As métricas são usadas para medir aspectos do desempenho de rede e protocolo.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: Terminologia de rede (Windows Soquetes 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d0c5fc67932b5c756ae52b9a7ffefef0f18c2728f2b2773de3741d0e5b7d41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794766"
---
# <a name="network-terminology-windows-sockets-2"></a>Terminologia de rede (Windows Soquetes 2)

As métricas são usadas para medir aspectos do desempenho de rede e protocolo. Os valores para essas métricas em vários cenários indicam o nível de desempenho de um aplicativo de rede. Esta seção define os termos e as métricas usados em todo o setor para medir o desempenho do aplicativo de rede. Esses termos são usados em todo o restante deste guia.

-   RTT (Tempo de ida e volta)

    Tempo, em milissegundos, para uma solicitação fazer uma viagem de um computador de origem para um computador de destino e voltar novamente. Valores inferiores indicam melhor desempenho. Os tempos de caminho de encaminhamento e retorno não são necessariamente iguais.

    Os valores de RTT são afetados pela infraestrutura de rede, distância entre nós, condições de rede e tamanho do pacote. O tamanho do pacote, o congestionamento e a compactação de conteúdo impactam o RTT quando medido em links lentos, como conexões discadas. Outros fatores afetam o RTT, incluindo correção de erro de encaminhamento e compactação de dados, que introduz buffers e filas que aumentam o RTT e, portanto, diminuem o desempenho.

-   Goodput

    Medida de dados úteis do aplicativo processados com êxito pelo receptor, em bits por segundo. O Goodput permite a medição da taxa de transferência efetiva ou útil e inclui apenas os dados do aplicativo; os headers de pacote, protocolo e mídia são considerados sobrecarga e não fazem parte da boa produtividade.

-   Sobrecarga de protocolo

    Bytes de não aplicação, incluindo enquadramento de protocolo e mídia, divididos pelo número total de bytes transmitidos. O valor é expresso como um percentual. Valores mais altos indicam um desempenho mais baixo.

    A sobrecarga é calculada para ambas as direções neste guia, mas pode ser calculada para cada direção separadamente.

-   Bandwidth-Delay produto

    Produto da largura de banda bits por segundo da rede e do RTT (em segundos). Esse valor equivale ao número de bits necessários para preencher a largura de banda de rede disponível. Quando o valor do produto de atraso de largura de banda é alto, a pilha TCP/IP deve lidar com grandes quantidades de dados não confirmados para manter o pipeline cheio. O produto de atraso de largura de banda é uma métrica de ponta a ponta fundamental para aplicativos de streaming.

 

 



