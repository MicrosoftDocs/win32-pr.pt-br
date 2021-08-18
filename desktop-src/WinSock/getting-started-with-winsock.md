---
description: veja a seguir um guia passo a passo para a introdução à programação de soquetes de Windows.
ms.assetid: 905cd5bc-44af-4d3f-841a-9e9a2700a785
title: Introdução com o Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcce956d7dcb142e4a51ac3a461868dfa055acc9a2d1624b6a6dff5132f86ea7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132149"
---
# <a name="getting-started-with-winsock"></a>Introdução com o Winsock

veja a seguir um guia passo a passo para a introdução à programação de soquetes de Windows. Ele foi projetado para fornecer uma compreensão das funções e estruturas de dados básicas do Winsock e de como elas funcionam juntas.

O aplicativo cliente e servidor usado para ilustração é um cliente e servidor muito básicos. exemplos de código mais avançados estão incluídos nos exemplos incluídos no Microsoft Windows Software Development Kit (SDK).

As primeiras etapas são as mesmas para aplicativos de cliente e de servidor.

-   [Sobre servidores e clientes](about-clients-and-servers.md)
-   [Criando um aplicativo Winsock básico](creating-a-basic-winsock-application.md)
-   [Inicializando o Winsock](initializing-winsock.md)

As seções a seguir descrevem as etapas restantes para criar um aplicativo cliente Winsock.

-   [Criando um soquete para o cliente](creating-a-socket-for-the-client.md)
-   [Conectando a um soquete](connecting-to-a-socket.md)
-   [Enviando e recebendo dados no cliente](sending-and-receiving-data-on-the-client.md)
-   [Desconectando o cliente](disconnecting-the-client.md)

As seções a seguir descrevem as etapas restantes para criar um aplicativo de servidor Winsock.

-   [Criando um soquete para o servidor](creating-a-socket-for-the-server.md)
-   [Ligando um soquete](binding-a-socket.md)
-   [Ouvindo em um soquete](listening-on-a-socket.md)
-   [Aceitando uma conexão](accepting-a-connection.md)
-   [Recebendo e enviando dados no servidor](receiving-and-sending-data-on-the-server.md)
-   [Desconectando o servidor](disconnecting-the-server.md)

O código-fonte completo para esses exemplos básicos.

-   [Executando o cliente Winsock e o exemplo de código do servidor](finished-server-and-client-code.md)
-   [Código completo do cliente Winsock](complete-client-code.md)
-   [Código completo do servidor Winsock](complete-server-code.md)

## <a name="advanced-winsock-samples"></a>Exemplos de Winsock avançados

vários exemplos de cliente e servidor Winsock mais avançados estão incluídos no SDK do Windows. por padrão, o código-fonte de exemplo do Winsock é instalado no seguinte diretório pelo SDK do Windows para Windows 7:

*C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ NetDs \\ winsock*

em versões anteriores do SDK do Windows, o número de versão no caminho acima seria alterado. por exemplo, o código-fonte de exemplo do Winsock é instalado no seguinte diretório padrão pelo SDK do Windows para Windows Vista

*C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 6.0 \\ amostras \\ NetDs \\ winsock*

Os exemplos mais avançados listados abaixo na ordem de mais alto para o menor desempenho são encontrados nos seguintes diretórios:

-   IOCP

    Esse diretório contém três programas de exemplo que usam portas de conclusão de e/s. Os programas incluem um servidor Winsock (iocpserver) que usa a função [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) , um servidor Winsock (iocpserverex) que usa a função [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) e um cliente Winsock multithread simples (iocpclient) usado para testar qualquer um desses servidores. Os programas de servidor dão suporte a vários clientes que se conectam via TCP/IP e enviam buffers de dados de tamanho arbitrário que o servidor, em seguida, retorna ao cliente. Para sua conveniência, um simples programa cliente, o iocpclient, foi desenvolvido para se conectar e enviar dados continuamente ao servidor para ressaltar o uso de vários threads. Os servidores Winsock que usam portas de conclusão de e/s fornecem a maior capacidade de desempenho.

-   post

    Esse diretório contém um programa de servidor de exemplo que usa e/s sobreposta. O programa de exemplo usa a função [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) e a e/s sobreposta para lidar com várias solicitações de conexão assíncronas de clientes com eficiência. O servidor usa a função **AcceptEx** para multiplexar diferentes conexões de cliente em um aplicativo Win32 de thread único. O uso de e/s sobreposta permite maior escalabilidade.

-   WSAPoll

    Esse diretório contém um programa de exemplo básico que demonstra o uso da função [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) . O programa de cliente e servidor combinado não está bloqueando e usam a função **WSAPoll** para determinar quando é possível enviar ou receber sem bloqueio. Este exemplo é mais para ilustração e não é um servidor de alto desempenho.

-   simple

    Esse diretório contém três programas de exemplo básicos que demonstram o uso de vários threads por um servidor. Os programas incluem um servidor TCP/UDP simples (simples), um servidor somente TCP ( \_ IOCTL simples) que usa a função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) em um aplicativo de console do Win32 para dar suporte a várias solicitações de cliente e um SIMPLEC (programa TCP/UDP) de cliente para testar os servidores. Os servidores demonstram o uso de vários threads para lidar com várias solicitações de cliente. Esse método tem problemas de escalabilidade, uma vez que um thread separado é criado para cada solicitação do cliente.

-   accept

    Esse diretório contém um servidor de exemplo básico e um programa cliente. O servidor demonstra o uso de uma aceitação sem bloqueio usando a função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) ou a aceitação assíncrona usando a função [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) . Este exemplo é mais para ilustração e não é um servidor de alto desempenho.

 

 
