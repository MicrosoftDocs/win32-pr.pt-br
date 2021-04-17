---
description: Determinadas técnicas de programação são executadas em problemas de desempenho que estão vinculados à implementação do TCP/IP.
ms.assetid: 2a63e85e-06fd-4b6f-8351-9866099b9d54
title: Problemas específicos de TCP/IP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9a7334471d3e419830eb054399ff1dcb721cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798514"
---
# <a name="tcpip-specific-issues"></a>Problemas específicos de TCP/IP

Determinadas técnicas de programação são executadas em problemas de desempenho que estão vinculados à implementação do TCP/IP. Esses problemas de desempenho não sugerem que o TCP/IP é ineficiente ou um afunilamento de desempenho; em vez disso, esses problemas são vistos quando as operações de TCP/IP não são compreendidas.

Os problemas a seguir identificam cenários comuns nos quais a combinação de operação TCP/IP e opções de desenvolvimento de aplicativos de rede resultam em baixo desempenho.

-   Aplicativos com conexão pesada.

    Alguns aplicativos instanciam uma nova conexão TCP para cada transação. O estabelecimento da conexão TCP leva tempo, contribui para RTTs extras e está sujeito a um início lento. Além disso, as conexões fechadas estão sujeitas à espera de tempo, o que consome recursos do sistema.

    Aplicativos com conexão pesada são comuns em grande parte porque são fáceis de criar; o teste e o tratamento de erros são muito simples. Detectar falhas em uma conexão persistente pode levar a um código e esforço consideráveis e, portanto, às vezes não é concluído.

    Remediar essa situação reutilizando a conexão TCP. Isso pode causar a serialização sobre a conexão TCP, a menos que as transações sejam multiplexada em várias conexões. Se essa abordagem for adotada, o número de conexões deverá ser limitado a dois, e o enquadramento de camada de aplicativo e o tratamento de erros avançado serão necessários.

-   Buffers de envio de comprimento zero e envios de bloqueio.

    Desativar o armazenamento em buffer usando a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para definir o buffer de envio (portanto, \_ SNDBUF) como zero é semelhante a desativar o cache de disco. Ao definir o buffer de envio como zero e emitir o bloqueio envia, um aplicativo tem uma chance de 50% de atingir uma confirmação de atraso de 200 milissegundos.

    Não desative o buffer de envio, a menos que você tenha considerado o impacto em todos os ambientes de rede. Uma exceção: streaming de dados usando e/s sobreposta deve definir o buffer de envio como zero.

-   Modelo de programação enviar-enviar-receber.

    Estruturar um aplicativo para executar Send-Send-receives aumenta suas chances de encontrar o algoritmo Nagle, o que causa um atraso de RTT + 200 ms. O algoritmo Nagle poderá ser encontrado se o último envio for menor que o tamanho máximo de segmento TCP (MSS, o máximo de dados em um único datagrama). O MSS pode ser um valor muito grande (64K em IPv4 e ainda maior no IPv6), portanto, não conte em um MSS pequeno, normalmente. Uma opção melhor é combinar os dois envios em um único envio usando a função [**WSASend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) ou **memcpy** .

-   Grande número de conexões simultâneas.

    As conexões simultâneas não devem exceder duas, exceto em aplicativos de finalidade especial. Exceder duas conexões simultâneas resulta em recursos desperdiçados. Uma boa regra é ter até quatro conexões de curta duração ou duas conexões persistentes por destino.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comportamento do aplicativo](application-behavior-2.md)
</dt> <dt>

[Aplicativos de alto desempenho do Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[Algoritmo Nagle](https://msdn.microsoft.com/library/ms817942.aspx)
</dt> </dl>

 

 



