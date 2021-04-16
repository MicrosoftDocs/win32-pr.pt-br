---
description: Nesta versão do aplicativo, um envio de bloco compactado dos dados é usado. Essa alteração resulta em uma melhoria significativa no desempenho.
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 'Revisão três: envio de bloco compactado'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657579406ed31fce08239c518a6910f525219fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765176"
---
# <a name="revision-three-compressed-block-send"></a>Revisão três: envio de bloco compactado

Nesta versão do aplicativo, um envio de bloco compactado dos dados é usado. Essa alteração resulta em uma melhoria significativa no desempenho.


```C++
BYTE tmp[3*ROWS*COLS];
FIELD Old = Map;
ComputeNext( Map );
n=Compact(Map,Old,tmp);
bind( s, ... );
connect( s, ... );
send( s, tmp, 3*n );
//can't do recv(s,tmp,n)
for(int i=0; i < n; )
    recv( s, tmp+i, n-i );
closesocket( s );
```



## <a name="changes-in-this-version"></a>Alterações nesta versão

Esta versão reflete as seguintes alterações:

-   As atualizações de célula não são mais serializadas.
-   Como um bloco Send é usado, o aplicativo não é mais informativo.
-   A compactação de dados é usada, resultando em um aplicativo menos Fat.

Ainda há um problema com esta versão do aplicativo; o risco de deadlock existe porque um grande envio é usado sem recebimentos. O servidor envia um byte para cada 3 bytes recebidos. Isso poderá causar um deadlock se o tamanho do buffer de recebimento for menor que 1000 bytes para este aplicativo de exemplo.

## <a name="key-performance-metrics"></a>Principais métricas de desempenho

As métricas de desempenho a seguir são expressas em RTT (tempo de ida e volta), Goodput e sobrecarga de protocolo. Consulte o tópico [terminologia de rede](network-terminology-2.md) para obter uma explicação desses termos.

Esta versão reflete as seguintes métricas de desempenho:

-   Hora da célula —. 002 \* RTT
-   Goodput – 2 kilobytes/RTT
-   Sobrecarga de protocolo – 14%

Da sobrecarga de 14%, 6% é dos cabeçalhos de Ethernet e os outros 8% são da inicialização da conexão e da subdivisão.

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

[Revisão 2: redesignação para menos conexões](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[Aprimoramentos futuros](future-improvements-2.md)
</dt> </dl>

 

 



