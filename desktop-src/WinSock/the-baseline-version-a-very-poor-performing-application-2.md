---
description: A versão de linha de base de um aplicativo com baixo desempenho no Windows Sockets (Winsock).
ms.assetid: 923884c4-f1bd-4f72-983e-6158f368e0dd
title: 'A versão de linha de base: um aplicativo com muito mau desempenho'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c094be5fd5cf6e3b9eaeb07c7ff38880e651dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781255"
---
# <a name="the-baseline-version-a-very-poor-performing-application"></a>A versão de linha de base: um aplicativo com muito mau desempenho

O exemplo de código inicial e de baixa execução usado para calcular as atualizações é o seguinte:

> [!Note]  
> Para simplificar, não há nenhum tratamento de erros nos exemplos a seguir. Qualquer aplicativo de produção sempre verifica valores de retorno.

 

> [!WARNING]
> Os primeiros exemplos do aplicativo fornecem um desempenho intencionalmente insatisfatório, a fim de ilustrar as melhorias de desempenho possíveis com alterações no código. Não use esses exemplos de código em seu aplicativo; Eles são apenas para fins ilustrativos.

 


```C++
#include <windows.h>

BOOL Map[ROWS][COLS];

void LifeUpdate()
{
    ComputeNext( Map );
    for( int i = 0 ; i < ROWS ; ++i )     //serialized
        for( int j = 0 ; j < COLS ; ++j )
            Set( i, j, Map[i][j] );    //chatty
}

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    setsockopt( s, SO_SNDBUF, &Zero, sizeof(int) );
    bind( s, ... );
    connect( s, ... );
    send( s, &row, 1 );
    send( s, &col, 1 );
    send( s, &bAlive, 1 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



Nesse estado, o aplicativo tem o pior desempenho de rede possível. Os problemas com esta versão do aplicativo de exemplo incluem:

-   O aplicativo é informativo. Cada transação é muito pequena — as células não precisam ser atualizadas uma a uma.
-   As transações são estritamente serializadas, embora as células possam ser atualizadas simultaneamente.
-   O buffer de envio é definido como zero e o aplicativo incorre em um atraso de 200 milissegundos para cada envio — três vezes por célula.
-   O aplicativo é muito conectado, conectando uma vez para cada célula. Os aplicativos são limitados no número de conexões por segundo para um determinado destino devido ao estado de espera de tempo, mas isso não é um problema aqui, uma vez que cada transação leva mais de 600 milissegundos.
-   O aplicativo é FAT; muitas transações não têm efeito sobre o estado do servidor, pois muitas células não são alteradas de Update para Update.
-   O aplicativo exibe streaming ruim; pequenos envios consomem muita CPU e RAM.
-   O aplicativo assume uma representação little-endian para seus envios. Essa é uma suposição natural para a plataforma atual do Windows, mas pode ser perigosa para código de vida longa.

## <a name="key-performance-metrics"></a>Principais métricas de desempenho

As métricas de desempenho a seguir são expressas em RTT (tempo de ida e volta), Goodput e sobrecarga de protocolo. Consulte o tópico [terminologia de rede](network-terminology-2.md) para obter uma explicação desses termos.

-   A hora da célula, o tempo de rede para uma atualização de célula única, requer 4 \* RTT + 600 milissegundos para interações de Nagle e de ACK atrasada.
-   Goodput é menor que 6 bytes.
-   A sobrecarga de protocolo é 99,6%.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Melhorando um aplicativo lento](improving-a-slow-application-2.md)
</dt> <dt>

[Terminologia de rede](network-terminology-2.md)
</dt> <dt>

[Revisão 1: limpando o óbvio](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revisão 2: redesignação para menos conexões](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Revisão 3: envio de bloco compactado](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Aprimoramentos futuros](future-improvements-2.md)
</dt> </dl>

 

 



