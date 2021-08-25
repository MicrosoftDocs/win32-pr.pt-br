---
description: A abstração de soquete de fluxo inclui a noção de dados OOB (fora de banda).
ms.assetid: 1a517885-2688-421f-9389-2d329e5c3d56
title: Protocol-Independent dados fora de banda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1918ba1525462f4352d76c989d7fb5d92beeb59766f92cdccbdda66a5b82744d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860826"
---
# <a name="protocol-independent-out-of-band-data"></a>Protocol-Independent dados fora de banda

A abstração de soquete de fluxo inclui a noção de dados OOB (fora de banda). Muitos protocolos permitem que partes de dados de entrada sejam marcadas como especiais de alguma forma, e esses blocos de dados especiais podem ser entregues ao usuário fora da sequência normal. Exemplos incluem dados acelerados no X.25 e outros protocolos OSI e dados urgentes no BSD UNIX uso do TCP. A seção a seguir descreve o tratamento de dados OOB de maneira independente de protocolo. Uma discussão sobre os dados OOB implementados usando dados urgentes TCP segue a explicação independente do protocolo. Em cada discussão, o uso de [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) também implica [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)e [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom)e as referências a [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) também se aplicam a [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect).

## <a name="protocol-independent-oob-data"></a>Dados OOB independentes de protocolo

Os dados OOB são um canal de transmissão logicamente independente associado a cada par de soquetes de fluxo conectados. Os dados OOB podem ser entregues ao usuário independentemente dos dados normais. A abstração define que os recursos de dados OOB devem dar suporte à entrega confiável de pelo menos um bloco de dados OOB por vez. Esse bloco de dados pode conter pelo menos um byte de dados e pelo menos um bloco de dados OOB pode estar aguardando a entrega ao usuário a qualquer momento. Para protocolos de comunicação que suportam a sinalização em banda (como TCP, em que os dados urgentes são entregues em sequência com os dados normais), o sistema normalmente extrai os dados OOB do fluxo de dados normal e os armazena separadamente (deixando uma lacuna no fluxo de dados normal). Isso permite que os usuários escolham entre receber os dados OOB em ordem e recebê-los fora de sequência sem a necessidade de buffer de todos os dados intermediários. É possível espiar dados fora de banda (OOB).

Um usuário pode determinar se os dados OOB estão aguardando para serem lidos usando a função [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) ou [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) com o **IOCTL SIOCATMARK.** Para protocolos em que o conceito da posição do bloco de dados OOB dentro do fluxo de dados normal é significativo, como TCP, um provedor de serviços soquetes do Windows mantém um marcador conceitual que indica a posição do último byte de dados OOB dentro do fluxo de dados normal. Isso não é necessário para a implementação das funções **ioctlsocket** ou **WSAIoctl** que suportam **SIOCATMARK.** A presença ou ausência de dados OOB é necessária.

Para protocolos em que o conceito da posição do bloco de dados OOB dentro do fluxo de dados normal é significativo, um aplicativo pode processar dados fora de banda em linha, como parte do fluxo de dados normal. Isso é feito definindo a opção soquete SO \_ OOBINLINE com a [**função setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt) Para outros protocolos em que os blocos de dados OOB são realmente independentes do fluxo de dados normal, tentar definir SO \_ OOBINLINE resulta em um erro. Um aplicativo pode usar a função [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) ou [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) com o IOCTL **SIOCATMARK** para determinar se há dados OOB não lidos que precedem a marca. Por exemplo, ele pode usar essas informações para ressincronizar com seu par, garantindo que todos os dados até a marca no fluxo de dados sejam descartados quando apropriado.

Com SO \_ OOBINLINE desabilitado (a configuração padrão):

-   Windows Os soquetes notificam um aplicativo de um evento OOB FD, se o aplicativo registrado para notificação com \_ [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect), exatamente da mesma maneira que o FD READ é usado para notificar a presença de \_ dados normais. Ou seja, o FD OOB é postado quando os dados OOB chegam sem dados OOB anteriormente \_ na fila. O FD OOB também é postado quando os dados são lidos usando o sinalizador OOB do MSG, enquanto alguns dados OOB permanecem na fila depois que a operação de \_ \_ leitura é retornada. As mensagens \_ FD READ não são postadas para dados OOB.
-   Windows Os soquetes [**retornam de select**](/windows/desktop/api/Winsock2/nf-winsock2-select) com o *soquete exceptfds* apropriado definido se os dados OOB estão na fila no soquete.
-   O aplicativo pode chamar [**recv com**](/windows/desktop/api/winsock/nf-winsock-recv) MSG OOB para ler o bloco de dados \_ urgente a qualquer momento. O bloco de dados OOB salta para a fila.
-   O aplicativo pode chamar [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) sem OOB do MSG \_ para ler o fluxo de dados normal. O bloco de dados OOB não aparece no fluxo de dados com dados normais. Se os dados OOB permanecerem após qualquer chamada para **recv,** Windows Sockets notifica o aplicativo com FD OOB ou com \_ *exceptfds* ao usar [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select).
-   Para protocolos em que os dados OOB têm uma posição dentro do fluxo de dados normal, uma única operação [**de recv**](/windows/desktop/api/winsock/nf-winsock-recv) não abrange essa posição. Um **recv** retorna os dados normais antes da marca e um segundo **recv** é necessário para começar a ler os dados após a marca.

Com SO \_ OOBINLINE habilitado:

-   As mensagens \_ FD OOB não são postadas para dados OOB. Os dados OOB são tratados como normais para a finalidade das funções [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) e [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) e indicados definindo o soquete em *readfds* ou enviando uma mensagem FD \_ READ, respectivamente.
-   O aplicativo não pode [**chamar recv com**](/windows/desktop/api/winsock/nf-winsock-recv) o sinalizador OOB do MSG \_ definido para ler o bloco de dados OOB. O código de erro WSAEINVAL é retornado.
-   O aplicativo pode chamar [**recv sem**](/windows/desktop/api/winsock/nf-winsock-recv) o sinalizador OOB do MSG \_ definido. Todos os dados OOB são entregues em sua ordem correta dentro do fluxo de dados normal. Os dados OOB nunca são mistos com dados normais. Deve haver três solicitações de leitura para passar dos dados OOB. O primeiro retorna os dados normais antes do bloco de dados OOB, o segundo retorna os dados OOB, o terceiro retorna os dados normais após os dados OOB. Em outras palavras, os limites do bloco de dados OOB são preservados.

A [**rotina WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) é particularmente adequada para lidar com a notificação da presença de dados fora de banda quando SO \_ OOBINLINE está desligado.

## <a name="oob-data-in-tcp"></a>Dados OOB em TCP

> [!IMPORTANT]
> A discussão a seguir sobre dados fora de banda (OOB), implementada usando dados urgentes de TCP, segue o modelo usado na distribuição de software de Berkeley. Os usuários e implementadores devem estar cientes de que:

 

-   No momento, há duas interpretações conflitantes do [RFC 793](https://www.ietf.org/rfc/rfc793.txt) (em que o conceito é introduzido).
-   A implementação de dados OOB na BSD (Distribuição de Software Berkeley) não está em conformidade com os Requisitos de Host especificados na [RFC 1122](https://www.ietf.org/rfc/rfc1122.txt).

    Especificamente, o ponteiro urgente TCP no BSD aponta para o byte após o byte de dados urgente e um ponteiro urgente TCP compatível com RFC aponta para o byte de dados urgente. Como resultado, se um aplicativo envia dados urgentes de uma implementação compatível com BSD para uma implementação compatível com o RFC 1122, o receptor lê o byte de dados urgentes errado (ele lê o byte localizado após o byte correto no fluxo de dados como o byte de dados urgente).

    Para minimizar problemas de interoperabilidade, os autores de aplicativos são aconselhados a não usar dados OOB, a menos que isso seja necessário para interoperar com um serviço existente. Windows Os fornecedores de soquetes são incentivados a documentar a semântica OOB (BSD ou RFC 1122) que seu produto implementa.

A chegada de um segmento TCP com o sinalizador LTD (para urgente) definido indica a existência de um único byte de dados OOB dentro do fluxo de dados TCP. O bloco de dados OOB tem um byte de tamanho. O ponteiro urgente é um deslocamento positivo do número de sequência atual no header TCP que indica o local do bloco de dados OOB (de forma ambígua, conforme indicado no anterior). Portanto, ele pode apontar para dados que ainda não foram recebidos.

Se SO OOBINLINE estiver desabilitado (o padrão) quando o segmento TCP que contém o byte apontado pelo ponteiro urgente chegar, o bloco de dados \_ OOB (um byte) será removido do fluxo de dados e armazenado em buffer. Se um segmento TCP subsequente chegar com o sinalizador urgente definido (e um novo ponteiro urgente), o byte OOB atualmente na fila poderá ser perdido à medida que ele for substituído pelo novo bloco de dados OOB (como ocorre na Distribuição de Software De Berkeley). No entanto, ele nunca é substituído no fluxo de dados.

Com SO \_ OOBINLINE habilitado, os dados urgentes permanecem no fluxo de dados. Como resultado, o bloco de dados OOB nunca é perdido quando um novo segmento TCP chega contendo dados urgentes. A marca de dados OOB existente é atualizada para a nova posição.

> [!Note]  
> Quando a opção \_ soquete SO OOBINLINE é definida, o IOCTL SIOCATMARK sempre retorna **TRUE** e os dados OOB são retornados ao usuário como dados normais.

 

 

 



