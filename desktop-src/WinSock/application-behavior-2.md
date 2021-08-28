---
description: Outro aspecto do desenvolvimento de aplicativos a ser considerado é a diferença no comportamento entre operações locais ou intracomputer e o comportamento quando as operações ocorrem entre dois computadores em rede.
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: Comportamento do aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb09441eda4f0d909652ac38a9ca0596a1b4bce456f58c0e1eae1a7af7dc53b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121456"
---
# <a name="application-behavior"></a>Comportamento do aplicativo

Outro aspecto do desenvolvimento de aplicativos a ser considerado é a diferença no comportamento entre operações locais ou intracomputer e o comportamento quando as operações ocorrem entre dois computadores em rede. Há comportamentos de aplicativo que podem funcionar de forma aceitável em um computador local, mas quando executados em uma rede, causam degradação significativa de desempenho e consumo de recursos. os comportamentos de aplicativo a seguir devem ser evitados ao desenvolver aplicativos Windows sockets.

## <a name="behaviors-to-avoid"></a>Comportamentos a serem evitados

-   Aplicativos informais.

    Alguns aplicativos executam muitas transações pequenas. Quando combinado com a sobrecarga de rede associada a cada uma dessas transações, o efeito é multiplicado. Em rede, as transações pequenas podem consumir tantos recursos quanto grandes transações. Uma abordagem melhor é combinar muitas transações pequenas em uma única transação grande.

-   Transações serializadas.

    A serialização desnecessária de transações pode resultar em baixo desempenho e afetar a escalabilidade. Por exemplo, 1000 transações serializadas levam pelo menos 1000 \* RTT para serem concluídas. Uma abordagem melhor é executar transações não relacionadas em paralelo. Quando aplicativos serializados são combinados com aplicativos informais, a capacidade de resposta pode ser seriamente dificultada.

    > [!Note]  
    > A desserialização correta de um aplicativo pode ser difícil. Se a alteração de uma prova de serializado para paralelo for muito difícil, considere combinar várias transações em menos transações grandes.

     

-   Transações de Fat.

    Os aplicativos que enviam bytes desnecessários na rede são considerados aplicativos Fat. Os aplicativos que enviam bytes desnecessários na rede aumentam a sobrecarga de rede e o desempenho é dificultado. Essa situação geralmente vem de estruturas de dados ineficientes ou streaming de dados ineficiente. Para corrigir isso, Otimize as estruturas de dados ou considere o uso da compactação.

As seções a seguir abordam aspectos do desenvolvimento de aplicativos a serem considerados.

-   [Problemas específicos de TCP/IP](tcp-ip-specific-issues-2.md)
-   [Reconhecendo aplicativos lentos](recognizing-slow-applications-2.md)
-   [Calculando a sobrecarga com netstat](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[aplicativos de alto desempenho Windows sockets](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



