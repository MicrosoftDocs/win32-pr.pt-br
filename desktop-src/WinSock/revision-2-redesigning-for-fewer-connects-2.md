---
description: Nesta revisão, o aplicativo de exemplo é reprojetado para eliminar conexões desnecessárias.
ms.assetid: 0db6ded4-0a59-454e-824e-8cd7f0dc9fec
title: 'Revisão dois: redesignação para menos conexões'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d5a8c8648f43f9ddac93c9d17f667b4b97011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091310"
---
# <a name="revision-two-redesigning-for-fewer-connects"></a>Revisão dois: redesignação para menos conexões

Nesta revisão, o aplicativo de exemplo é reprojetado para eliminar conexões desnecessárias.

> [!WARNING]
> Esses exemplos do aplicativo também fornecem um desempenho intencionalmente insatisfatório, a fim de ilustrar as melhorias de desempenho possíveis com alterações no código. Não use este exemplo de código em seu aplicativo; Ele é apenas para fins ilustrativos.

 


```C++
ComputeNext( Map );
bind( s, ... );
connect( s, ... );
for(int i=0 ; i < ROWS ; ++i)
  for(int j=0 ; j < COLS ; ++j)
  {
    BYTE tmp[3];
    tmp[0] = i;
    tmp[1] = j;
    tmp[2] = Map[i][j];
    send( s, tmp, 3 );
    recv( s, &byRet, 1 );
  }
closesocket( s );
```



## <a name="remaining-problems"></a>Problemas restantes

As alterações na revisão dois remodelaram o aplicativo para fazer apenas uma conexão por atualização. O aplicativo ainda inclui os seguintes problemas de desempenho:

-   O aplicativo ainda é serializado e informativo.
-   O aplicativo ainda tem um design de Fat; Há muitos envios que não exigem nenhuma operação neste design.
-   Os envios ainda são apenas 3 bytes, o que é um streaming ruim.

## <a name="key-performance-metrics"></a>Principais métricas de desempenho

As métricas de desempenho a seguir são expressas em RTT (tempo de ida e volta), Goodput e sobrecarga de protocolo. Consulte o tópico [terminologia de rede](network-terminology-2.md) para obter uma explicação desses termos.

Esta versão reflete as seguintes métricas de desempenho:

-   Tempo da célula — 1 \* RTT
-   Goodput – 4 bytes/RTT
-   Sobrecarga de protocolo — 96,8%

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Melhorando um aplicativo lento](improving-a-slow-application-2.md)
</dt> <dt>

[Terminologia de rede](network-terminology-2.md)
</dt> <dt>

[A versão de linha de base: um aplicativo com muito mau desempenho](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[Revisão 1: limpando o óbvio](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[Revisão 3: envio de bloco compactado](revision-3-compressed-block-send-2.md)
</dt> <dt>

[Aprimoramentos futuros](future-improvements-2.md)
</dt> </dl>

 

 



