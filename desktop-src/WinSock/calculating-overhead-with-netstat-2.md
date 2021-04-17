---
description: Calculando a sobrecarga com netstat
ms.assetid: d96a8fba-8d76-443f-be49-81a8ad7050fa
title: Calculando a sobrecarga com netstat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7843c3cd445bee66e25a9f191ae4b78093faea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784517"
---
# <a name="calculating-overhead-with-netstat"></a>Calculando a sobrecarga com netstat

O cálculo da sobrecarga com o netstat deve ser executado em uma rede silenciosa para evitar que outros tráfegos de rede distorcem os dados, como difusão ou tráfego multicast.

**Para calcular a sobrecarga de rede de um aplicativo usando netstat**

1.  Recupere as estatísticas de interface atuais usando netstat.
2.  Execute o aplicativo.
3.  Obtenha as estatísticas de interface novamente usando netstat.
4.  Calcule o número de bytes recebidos entre as duas medidas netstat.

## <a name="example"></a>Exemplo

O exemplo a seguir demonstra essas etapas, usando TTCP para enviar 10 bytes de dados, um byte por vez.

Primeiro, uma sobrecarga teórica para o aplicativo é calculada. Para esse teste, todos os pacotes são 60 bytes (o mínimo de Ethernet). Essa transferência requer três pacotes para configurar a conexão, 10 pacotes de dados, 10 pacotes de confirmação (a confirmação de atraso é disparada quase todas as vezes) e quatro pacotes para fechar a conexão normalmente.

Isso equivale a 27 pacotes de 60 bytes cada, ou 1620 bytes (3 + 4 + 10 + 10) \* 60 = 1620). Como apenas 10 bytes de dados são transferidos, a sobrecarga é de 1610 bytes, que tem mais de 99% de sobrecarga de protocolo.

### <a name="commands"></a>Comandos

**netstat-e**

``` syntax
Interface Statistics
                     Received     Sent
Bytes                392291400    444684566
Unicast packets      487627       570086
Non-unicast packets  1159163      11300
Discards             0            0
Errors               0            0
Unknown protocols    52812
```

**Ttcp-t-H0-D-L1-N10-P9 172.31.71.99**

``` syntax
ttcp-t: 10 bytes in 2168 real milliseconds = 0 KB/sec
ttcp-t: 10 I/O calls, msec/call = 216, calls/sec = 4, bytes/call = 1
```

**netstat-e**

``` syntax
Interface Statistics
                      Received     Sent
Bytes                 39229207     444685382
Unicast packets       487641       570100
Non-unicast packets   1159164      11301
Discards              0            0
Errors                0            0
Unknown protocols     52812
```

### <a name="calculations"></a>Cálculos

**Enviado:** 816 bytes

**Recebido:** 674 bytes

**Total de bytes:** 1490

**Bytes de usuário:** 10

**Sobrecarga:** 1480/1490 = 99,3%

* * Goodput: * * = 5 bytes/segundo (ou 40 bits/s)

> [!Note]  
> Os bytes reais transferidos não correspondem aos valores teóricos porque os bytes de preenchimento não estão sendo contabilizados nos valores netstat.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comportamento do aplicativo](application-behavior-2.md)
</dt> <dt>

[Aplicativos de alto desempenho do Windows Sockets](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



