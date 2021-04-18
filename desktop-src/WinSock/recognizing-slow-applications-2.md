---
description: Este guia identifica um aplicativo lento como um aplicativo do Microsoft Windows com desempenho prejudicado.
ms.assetid: cacf55d8-ab64-47a4-a55b-59a3c4e3877b
title: Reconhecendo aplicativos lentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07be9484a3b08951b8b64989757459531ff72906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814143"
---
# <a name="recognizing-slow-applications"></a>Reconhecendo aplicativos lentos

Este guia identifica um aplicativo *lento* como um aplicativo do Microsoft Windows com desempenho prejudicado. Um aplicativo lento exibe um ou mais dos seguintes sintomas:

-   A utilização da CPU e da rede é baixa.

    O computador parece estar aguardando algo. Geralmente, o aplicativo está aguardando a rede.

-   A desativação do algoritmo Nagle por meio da \_ opção de soquete TCP NoDelay aumenta o desempenho.

    Isso indica outros problemas e não deve ser considerado uma solução. A desativação do algoritmo Nagle aumenta a sobrecarga do protocolo. Não use esse método como uma correção para os aplicativos desfeitos – apenas como uma indicação de que o aplicativo precisa de outro trabalho para corrigir problemas de desempenho.

-   O aplicativo exibe uma sobrecarga alta.

    Para calcular a sobrecarga dos aplicativos, determine a quantidade de dados que você pretende transferir em cada direção. Em seguida, use netstat e Add (para Ethernet) 60 bytes para cada pacote e 500 bytes para cada conexão. A melhor sobrecarga que pode ser esperada para streaming pela Ethernet é de aproximadamente 6%. Para uma conexão de modem, a melhor sobrecarga é de aproximadamente 2%, devido ao fato de que um link PPP usa a compactação de cabeçalho. Consulte [calculando a sobrecarga com o netstat](calculating-overhead-with-netstat-2.md) para obter mais informações.

-   A resposta do aplicativo fica mais lenta quando a conexão tem um RTT grande.

    Supondo que o aplicativo não esteja se aproximando da largura de banda do link, um RTT grande deve ter pouco ou nenhum efeito. Uma lentidão drástica com um grande RTT é um sinal claro de processamento serializado e muitas transações pequenas.

Cada aplicativo deve ser testado em um ambiente com um grande RTT. Isso revela a maioria dos aplicativos que sofrem com opções de desenvolvimento deficientes. Esse teste pode ser executado em vários ambientes, incluindo uma rede LAN sem fio, um simulador de atraso de link ou uma rede de satélite.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comportamento do aplicativo](application-behavior-2.md)
</dt> <dt>

[Aplicativos de alto desempenho do Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Algoritmo Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



