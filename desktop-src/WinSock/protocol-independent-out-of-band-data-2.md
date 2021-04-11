---
description: A abstração de soquete de fluxo inclui a noção de dados de fora de banda (OOB).
ms.assetid: 1a517885-2688-421f-9389-2d329e5c3d56
title: Protocol-Independent dados fora de banda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a929f4273d9cc9f268a296b711649406622ca9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296343"
---
# <a name="protocol-independent-out-of-band-data"></a>Protocol-Independent dados fora de banda

A abstração de soquete de fluxo inclui a noção de dados de fora de banda (OOB). Muitos protocolos permitem que partes de dados de entrada sejam marcadas como especiais de alguma forma, e esses blocos de dados especiais podem ser entregues ao usuário fora da sequência normal. Os exemplos incluem dados acelerados em X. 25 e outros protocolos OSI e dados urgentes no uso do TCP do BSD UNIX. A seção a seguir descreve a manipulação de dados OOB de maneira independente de protocolo. Uma discussão sobre os dados OOB implementados usando dados TCP urgentes segue a explicação independente de protocolo. Em cada discussão, o uso de [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) também implica em [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)e [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom), e as referências a [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) também se aplicam a [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect).

## <a name="protocol-independent-oob-data"></a>Dados OOB independentes de protocolo

Os dados OOB são um canal de transmissão logicamente independente associado a cada par de soquetes de fluxo conectados. Os dados OOB podem ser entregues ao usuário independentemente dos dados normais. A abstração define que os recursos de dados OOB devem dar suporte à entrega confiável de pelo menos um bloco de dados OOB de cada vez. Esse bloco de dados pode conter pelo menos um byte de dados e pelo menos um bloco de dados OOB pode estar com entrega pendente para o usuário a qualquer momento. Para protocolos de comunicação que dão suporte à sinalização em banda (como TCP, em que os dados urgentes são entregues em sequência com os dados normais), o sistema normalmente extrai os dados OOB do fluxo de dados normal e os armazena separadamente (deixando uma lacuna no fluxo de dados normal). Isso permite que os usuários escolham entre receber os dados OOB em ordem e recebê-los fora de sequência sem precisar armazenar em buffer todos os dados intermediários. É possível inspecionar dados de fora de banda (OOB).

Um usuário pode determinar se algum dado OOB está aguardando para ser lido usando a função [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) ou [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) com o IOCTL **SIOCATMARK** . Para protocolos em que o conceito da posição do bloco de dados OOB dentro do fluxo de dados normal é significativo, como o TCP, um provedor de serviços do Windows Sockets mantém um marcador conceitual que indica a posição do último byte de dados OOB dentro do fluxo de dados normal. Isso não é necessário para a implementação das funções **ioctlsocket** ou **WSAIoctl** que dão suporte a **SIOCATMARK**. A presença ou a ausência de dados OOB é necessária.

Para protocolos em que o conceito da posição do bloco de dados OOB dentro do fluxo de dados normal é significativo, um aplicativo pode processar dados fora de banda embutidos, como parte do fluxo de dados normal. Isso é feito definindo a opção socket de modo que \_ OOBINLINE com a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) . Para outros protocolos em que os blocos de dados OOB são verdadeiramente independentes do fluxo de dados normal, tentar definir \_ OOBINLINE resulta em um erro. Um aplicativo pode usar a função [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) ou [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) com o **SIOCATMARK** IOCTL para determinar se há algum dado OOB Não lido antes da marca. Por exemplo, ele pode usar essas informações para sincronizar novamente com seu par, garantindo que todos os dados até a marca no fluxo de dados sejam descartados quando apropriado.

Com \_ o OOBINLINE desabilitado (a configuração padrão):

-   O Windows Sockets notifica um aplicativo sobre um \_ evento de OOB do FD, se o aplicativo estiver registrado para notificação com [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect), exatamente da mesma forma que a leitura de FD \_ é usada para notificar a presença de dados normais. Ou seja, FD \_ OOB é Postado quando dados OOB chegam sem dados OOB anteriormente na fila. O OOB do FD \_ também é Postado quando os dados são lidos usando o sinalizador de OOB da msg \_ enquanto alguns dados OOB permanecem na fila depois que a operação de leitura é retornada. \_As mensagens de leitura do FD não são postadas para dados OOB.
-   O Windows Sockets retorna de [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) com o conjunto de soquetes *exceptfds* apropriado se os dados OOB estiverem na fila no soquete.
-   O aplicativo pode chamar [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) com MSG \_ OOB para ler o bloco de dados urgentes a qualquer momento. O bloco de dados OOB salta a fila.
-   O aplicativo pode chamar [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) sem \_ o OOB de MSG para ler o fluxo de dados normal. O bloco de dados OOB Não aparece no fluxo de dados com dados normais. Se os dados OOB permanecerem após qualquer chamada para **recv**, o Windows Sockets notificará o aplicativo com FD \_ OOB ou com *exceptfds* ao usar [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select).
-   Para protocolos em que os dados OOB têm uma posição dentro do fluxo de dados normal, uma única operação de [**recebimento**](/windows/desktop/api/winsock/nf-winsock-recv) não abrange essa posição. Um **recv** retorna os dados normais antes da marca e um segundo **recv** é necessário para começar a ler os dados após a marca.

Com o \_ OOBINLINE habilitado:

-   \_As mensagens OOB do FD não são postadas para dados OOB. Os dados OOB são tratados como normais para fins das funções [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) e [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) e são indicados pela definição do soquete no *readfds* ou pela envio de uma \_ mensagem de leitura FD, respectivamente.
-   O aplicativo não pode chamar [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) com o \_ sinalizador de mensagem OOB definido para ler o bloco de dados OOB. O código de erro WSAEINVAL é retornado.
-   O aplicativo pode chamar [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) sem o conjunto de sinalizadores de OOB de MSG \_ . Todos os dados OOB são entregues em sua ordem correta dentro do fluxo de dados normal. Os dados OOB nunca são misturados com dados normais. Deve haver três solicitações de leitura para passar os dados OOB. O primeiro retorna os dados normais antes do bloco de dados OOB, o segundo retorna os dados OOB, o terceiro retorna os dados normais que seguem os dados OOB. Em outras palavras, os limites de bloco de dados OOB são preservados.

A rotina [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) é particularmente adequada para lidar com a notificação da presença de dados fora de banda quando \_ OOBINLINE está desativado.

## <a name="oob-data-in-tcp"></a>Dados OOB no TCP

> [!IMPORTANT]
> A seguinte discussão sobre dados fora de banda (OOB), implementados usando dados urgentes TCP, segue o modelo usado na distribuição de software Berkeley. Os usuários e os implementadores devem estar cientes de que:

 

-   Há, no momento, duas interpretações conflitantes do [RFC 793](https://www.ietf.org/rfc/rfc793.txt) (onde o conceito é introduzido).
-   A implementação de dados OOB na Berkeley Software Distribution (BSD) não está de acordo com os requisitos de host especificados no [RFC 1122](https://www.ietf.org/rfc/rfc1122.txt).

    Especificamente, o ponteiro urgente TCP no BSD aponta para o byte após o byte de dados urgente e um ponteiro urgente TCP compatível com RFC aponta para o byte de dados urgente. Como resultado, se um aplicativo enviar dados urgentes de uma implementação compatível com BSD para uma implementação compatível com o RFC 1122, o receptor lerá o byte de dados urgente incorreto (ele lê o byte localizado após o byte correto no fluxo de dados como o byte de dados urgente).

    Para minimizar problemas de interoperabilidade, os gravadores de aplicativos são aconselhados a não usar dados OOB, a menos que isso seja necessário para interoperar com um serviço existente. Os fornecedores do Windows Sockets são incentivados a documentar a semântica OOB (BSD ou RFC 1122) que seus produtos implementam.

A chegada de um segmento TCP com o sinalizador de URG (para urgente) indica a existência de um único byte de dados OOB dentro do fluxo de dados TCP. O bloco de dados OOB tem um tamanho de byte. O ponteiro urgente é um deslocamento positivo do número de sequência atual no cabeçalho TCP que indica o local do bloco de dados OOB (de forma ambígua, conforme observado no anterior). Portanto, ele pode apontar para dados que ainda não foram recebidos.

Se o \_ OOBINLINE estiver desabilitado (o padrão) quando o segmento TCP que contém o byte apontado pelo ponteiro urgente chegar, o bloco de dados OOB (um byte) será removido do fluxo de dados e armazenado em buffer. Se um segmento TCP subsequente chegar com o sinalizador urgente definido (e um novo ponteiro urgente), o byte OOB atualmente na fila poderá ser perdido quando for substituído pelo novo bloco de dados OOB (como ocorre na distribuição de software da Berkeley). No entanto, ele nunca é substituído no fluxo de dados.

Com \_ o OOBINLINE habilitado, os dados urgentes permanecem no fluxo de dados. Como resultado, o bloco de dados OOB nunca é perdido quando um novo segmento TCP chega contendo dados urgentes. A marca de dados OOB existente é atualizada para a nova posição.

> [!Note]  
> Quando a \_ opção de soquete OOBINLINE é definida, o IOCTL SIOCATMARK sempre retorna **true** e os dados OOB são retornados ao usuário como dados normais.

 

 

 



