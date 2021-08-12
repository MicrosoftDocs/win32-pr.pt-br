---
description: Sempre deve ser levado em consideração as diferenças entre a ordenação de bytes usada para armazenar inteiros pela arquitetura do host e a ordem de bytes usada na conexão por protocolos de transporte individuais.
ms.assetid: 54c84cdb-50a1-4f5e-a18f-0477d90c74d2
title: ordenação da regra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 554b9f00b67fcd602daee0ed33443e228e4e3976f334506d949e3af79fef7e8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118560176"
---
# <a name="byte-ordering"></a>ordenação da regra

Sempre deve ser levado em consideração as diferenças entre a ordenação de bytes usada para armazenar inteiros pela arquitetura do host e a ordem de bytes usada na conexão por protocolos de transporte individuais. qualquer referência a um endereço ou número de porta passado para ou de uma rotina de soquetes de Windows deve estar na ordem de rede (big-endian) para o protocolo que está sendo utilizado. No caso do IP, isso inclui o endereço IP e os parâmetros de porta de uma estrutura [**SOCKADDR**](sockaddr-2.md) (mas não o parâmetro *\_ da família Sin* ).

vários sistemas de UNIX operam em CPUs que representam inteiros em ordem de bytes de rede (big-endian). Portanto, a necessidade de converter inteiros de ordem de bytes de host para ordem de bytes de rede pode ser ignorada sem causar problemas, mesmo que isso não seja recomendado para portabilidade.

Por outro lado, a ordem de bytes usada para representar inteiros pela maioria das CPUs Intel® é little-endian. Portanto, se torna obrigatório que os inteiros sejam convertidos de ordem de byte de host para ordem de bytes de rede antes de serem usados em estruturas e funções de soquetes Winsock.

Considere um aplicativo que normalmente entra em contato com um servidor na porta TCP correspondente ao serviço de tempo, mas fornece um mecanismo para que o usuário especifique uma porta alternativa. O número da porta retornado por [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) já está na ordem de rede, que é o formato necessário para construir um endereço para que nenhuma conversão seja necessária. No entanto, se o usuário optar por usar uma porta diferente, inserida como um inteiro, o aplicativo deverá convertê-la do host para a ordem de rede TCP/IP (usando a função [**htons**](/windows/desktop/api/winsock/nf-winsock-htons) ou [**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons) ) antes de usá-la para construir um endereço. Por outro lado, se o aplicativo fosse exibir o número da porta dentro de um endereço (retornado por [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) , por exemplo), o número da porta deve ser convertido da ordem da rede para o host (usando a função [**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs) ou [**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs) ) antes que possa ser exibido.

Como as ordens de byte da Intel e da Internet são diferentes, as conversões descritas no anterior são inevitáveis. Os gravadores de aplicativo são cuidadosos de que devem usar as funções de conversão padrão fornecidas como parte do Winsock em vez de escrever seu próprio código de conversão, já que as implementações futuras do Winsock provavelmente serão executadas em sistemas para os quais a ordem de host é idêntica à ordem de bytes de rede. Somente os aplicativos que usam as funções de conversão padrão entre a ordem de bytes do host e da rede provavelmente serão portáteis.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**getemparelhaname**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)
</dt> <dt>

[**htonl**](/windows/desktop/api/winsock/nf-winsock-htonl)
</dt> <dt>

[**htons**](/windows/desktop/api/winsock/nf-winsock-htons)
</dt> <dt>

[**ntohl**](/windows/desktop/api/winsock/nf-winsock-ntohl)
</dt> <dt>

[**ntohs**](/windows/desktop/api/winsock/nf-winsock-ntohs)
</dt> <dt>

[Portando aplicativos de soquete para Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[**SOCKADDR**](sockaddr-2.md)
</dt> <dt>

[Considerações sobre programação do Winsock](winsock-programming-considerations.md)
</dt> <dt>

[**WSAHtonl**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtonl)
</dt> <dt>

[**WSAHtons**](/windows/desktop/api/Winsock2/nf-winsock2-wsahtons)
</dt> <dt>

[**WSANtohl**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohl)
</dt> <dt>

[**WSANtohs**](/windows/desktop/api/Winsock2/nf-winsock2-wsantohs)
</dt> </dl>

 

 



