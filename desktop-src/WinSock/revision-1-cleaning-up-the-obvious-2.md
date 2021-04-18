---
description: Nesta versão do programa de exemplo, foram feitas algumas alterações óbvias que adotarão o desempenho inicial para melhorar a performance.
ms.assetid: ef9d594c-31fe-44c0-b707-47c01e2c5bf0
title: 'Revisão um: limpando o óbvio'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631bea7395000531cce542b41ace3b3aab9afff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764225"
---
# <a name="revision-one-cleaning-up-the-obvious"></a>Revisão um: limpando o óbvio

Nesta versão do programa de exemplo, foram feitas algumas alterações óbvias que adotarão o desempenho inicial para melhorar a performance. Esta versão do código está longe de ser ajustada pelo desempenho, mas é uma boa etapa incremental que permite examinar os efeitos de abordagens incrementalmente melhores.

> [!WARNING]
> Este exemplo do aplicativo fornece desempenho intencionalmente insatisfatório, a fim de ilustrar as melhorias de desempenho possíveis com alterações no código. Não use este exemplo de código em seu aplicativo; Ele é apenas para fins ilustrativos.

 


```C++
#include <windows.h>

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    BYTE tmp[3];
    tmp[0] = (BYTE)row;
    tmp[1] = (BYTE)col;
    tmp[2] = (BYTE)bAlive;
    bind( s, ... );
    connect( s, ... );
    send( s, &tmp, 3 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



## <a name="changes-in-this-version"></a>Alterações nesta versão

Esta versão reflete as seguintes alterações:

-   SNDBUF removido = 0. Os atrasos de 200 milissegundos devido a envios não armazenados em buffer e a confirmações atrasadas são removidos.
-   Removido o comportamento enviar-enviar-receber. Essa alteração elimina atrasos de 200 milissegundos devido a Nagle e interações de ACK atrasadas.
-   Suposição little-endian removida. Os bytes agora estão em ordem.

## <a name="remaining-problems"></a>Problemas restantes

Nesta versão, os seguintes problemas permanecem:

-   O aplicativo ainda é muito conectado. Como os mais de 600 milissegundos são removidos, o aplicativo agora atinge a taxa sustentada de 12 conexões por segundo. Muitas conexões simultâneas agora se tornam um problema.
-   O aplicativo ainda é FAT; as células inalteradas ainda são propagadas para o servidor.
-   O aplicativo ainda exibe streaming ruim; envios de 3 bytes ainda são pequenos envios.
-   O aplicativo agora envia 2 bytes/RTT, que é igual a 4 KB/s em Ethernet conectada diretamente. Isso não é rápido, mas o tempo de espera provavelmente causará problemas primeiro.
-   A sobrecarga está abaixo de 99,3%, que ainda não é uma boa porcentagem de sobrecarga.

## <a name="key-performance-metrics"></a>Principais métricas de desempenho

As principais métricas de desempenho a seguir são expressas em RTT (tempo de ida e volta), Goodput e sobrecarga de protocolo. Consulte o tópico [terminologia de rede](network-terminology-2.md) para obter uma explicação desses termos.

Esta versão reflete as seguintes métricas de desempenho:

-   Tempo da célula — 2 × RTT
-   Goodput – 2 bytes/RTT
-   Sobrecarga de protocolo — 99.3%

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Melhorando um aplicativo lento](improving-a-slow-application-2.md)
</dt> <dt>

[Terminologia de rede](network-terminology-2.md)
</dt> <dt>

[A versão de linha de base: um aplicativo com muito mau desempenho](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revisão 2: redesignação para menos conexões](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revisão 3: envio de bloco compactado](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Aprimoramentos futuros](future-improvements-2.md)
</dt> </dl>

 

 



