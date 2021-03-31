---
description: O cache local de dados é uma técnica usada para acelerar o acesso à rede para arquivos de dados. Ele envolve o armazenamento em cache de dados em clientes em vez de servidores, quando possível.
ms.assetid: a7eb24b3-7e23-4798-8584-30a171fa4f04
title: Cache local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8132bc51831db752422de1e3071ee3ef0b33a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836997"
---
# <a name="local-caching"></a>Cache local

O *cache local* de dados é uma técnica usada para acelerar o acesso à rede para arquivos de dados. Ele envolve o armazenamento em cache de dados em clientes em vez de servidores, quando possível.

O efeito do cache local é que ele permite que várias operações de gravação na mesma região de um arquivo sejam combinadas em uma operação de gravação na rede. O cache local reduz o tráfego de rede porque os dados são gravados uma vez. Esse cache melhora o tempo de resposta aparente dos aplicativos, pois os aplicativos não aguardam que os dados sejam enviados pela rede para o servidor.

O cache local de dados a serem lidos pode parecer acelerar as coisas por meio da leitura antecipada. Um exemplo simples é um aplicativo que acessa dados sequencialmente, como o pré-processador de um compilador. Nesses casos, a camada de rede do sistema operacional lê dados pela rede antes que o aplicativo solicite os dados. O ideal é que a rede entregue os dados antes que o aplicativo o solicite do sistema de arquivos, resultando em uma resposta quase instantânea. Na prática, isso raramente acontece, mas geralmente a leitura antecipada acelera os aplicativos, prevendo a próxima solicitação.

O cache local também pode ajudar a reduzir o tráfego de rede, lendo uma parte de um arquivo na rede uma vez e mantendo-o no cache local. Operações de leitura subsequentes nessa parte pelo aplicativo lido do cache local.

Um tipo de aplicativo que pode se beneficiar do cache local são arquivos em lotes. Processadores de comando leia e execute um arquivo em lotes uma linha por vez. Para cada linha, o processador de comando abre o arquivo, pesquisa o início da linha, lê o máximo de acordo com a necessidade, fecha o arquivo e executa a linha. Cada linha resulta em muito tráfego de rede. O tráfego de rede pode ser consideravelmente reduzido ao armazenar em cache todo o arquivo em lotes em um cliente.

O cache local também ajuda com outro problema associado a redes, especialmente redes que executam o trabalho em modems e outros pipes finos: tempo de resposta lento. Os usuários não desejam aguardar enquanto os dados são recuperados pela rede, modificados e gravados novamente. Com a leitura antecipada e gravação em cache, geralmente parece que essas funções funcionam muito mais rápido do que realmente.

Um risco de cache local é que os dados gravados têm apenas a mesma integridade que o cliente, desde que os dados sejam armazenados em cache no cliente. Em geral, os dados armazenados em cache localmente devem ser liberados para o servidor assim que possível. Com sistemas operacionais modernos e suporte a hardware, como fontes de alimentação ininterrupta, o risco de perder dados armazenados em cache localmente é reduzido. Mas o risco ainda existe, e você deve considerar a compensação entre a integridade dos dados e a velocidade de resposta aparente e a compensação entre a integridade dos dados e o tráfego de rede reduzido.

 

 



