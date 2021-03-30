---
description: Métricas são usadas para medir aspectos de desempenho de rede e protocolo.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: Terminologia de rede (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04e84621cdaec2638762d54f67e5aca7e3d55ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647129"
---
# <a name="network-terminology-windows-sockets-2"></a>Terminologia de rede (Windows Sockets 2)

Métricas são usadas para medir aspectos de desempenho de rede e protocolo. Os valores para essas métricas em vários cenários indicam o nível de desempenho de um aplicativo de rede. Esta seção define os termos e as métricas usadas em todo o setor para medir o desempenho do aplicativo de rede. Esses termos são usados em todo o restante deste guia.

-   RTT (tempo de ida e volta)

    Tempo, em milissegundos, para uma solicitação para fazer uma viagem de um computador de origem para um computador de destino e de volta. Valores mais baixos indicam melhor desempenho. Os tempos do caminho de avanço e de retorno não são necessariamente iguais.

    Os valores de RTT são afetados pela infraestrutura de rede, distância entre nós, condições de rede e tamanho do pacote. O tamanho do pacote, o congestionamento e a carga compactação impactam o RTT quando medido em links lentos, como conexões dial-up. Outros fatores afetam o RTT, incluindo a correção de erros e a compactação de dados de encaminhamento, que introduzem buffers e filas que aumentam o RTT e, portanto, diminuem o desempenho.

-   Goodput

    Medida de dados de aplicativo úteis processados com êxito pelo destinatário, em bits por segundo. O Goodput permite a medição da produtividade efetiva ou útil e inclui apenas os dados do aplicativo; os cabeçalhos de pacote, protocolo e mídia são considerados sobrecarga e não fazem parte do goodput.

-   Sobrecarga de protocolo

    Bytes não aplicativos, incluindo o enquadramento de protocolo e mídia, dividido pelo número total de bytes transmitidos. O valor é expresso como uma porcentagem. Valores mais altos indicam um desempenho mais baixo.

    A sobrecarga é calculada para ambas as direções neste guia, mas pode ser calculada para cada direção separadamente.

-   Bandwidth-Delay produto

    Produto da largura de banda de bits por segundo da rede e o RTT (em segundos). Esse valor equivale ao número de bits que leva para preencher a largura de banda de rede disponível. Quando o valor do produto de atraso de largura de banda é alto, a pilha TCP/IP deve lidar com grandes quantidades de dados não confirmados para manter o pipeline cheio. O produto de atraso de largura de banda é uma métrica de ponta a ponta de aplicativos de streaming.

 

 



