---
title: Programação de Bluetooth com Windows Sockets
description: Esta seção descreve como usar as funções e estruturas do Windows Sockets para programar um aplicativo Bluetooth.
ms.assetid: 0f15cb84-1d7a-4b64-86e8-b1b23c956c64
keywords:
- Bluetooth, tarefas
- Windows Sockets
- programando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca797121696af8eb36549bf596ad51ee8189c3cd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105753633"
---
# <a name="bluetooth-programming-with-windows-sockets"></a>Programação de Bluetooth com Windows Sockets

Esta seção descreve como usar as funções e estruturas do Windows Sockets para programar um aplicativo Bluetooth. Informações de referência completas para os elementos da API do Windows Sockets podem ser encontradas no [Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2); Esta seção fornece apenas informações específicas de Bluetooth para cada elemento de programação do Windows Sockets.

Você também pode baixar o [exemplo de conexão Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) para obter um exemplo completo.

Assim como acontece com toda a programação de aplicativos do Windows Sockets, a função [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) deve ser chamada para iniciar a funcionalidade do Windows Sockets e habilitar o Bluetooth.

Os tópicos a seguir fornecem orientação sobre o uso de estruturas e funções do Windows Sockets com a API do Bluetooth da Microsoft:



| Tópico                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bluetooth e aceitar](bluetooth-and-accept.md)                                                 | O Bluetooth usa a função [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) para habilitar tentativas de conexão de entrada em um soquete.<br/>                                                                                                                                                                                                  |
| [Bluetooth e ligar](bluetooth-and-bind.md)                                                     | O Bluetooth usa a função de [**Associação**](/windows/desktop/api/winsock/nf-winsock-bind) para associar a um soquete.<br/>                                                                                                                                                                                                                                     |
| [Bluetooth e BLOB](bluetooth-and-blob.md)                                                     | O Bluetooth usa a estrutura de [**blob**](/windows/desktop/api/nspapi/ns-nspapi-blob) para passar ou receber dados específicos de transporte para a estrutura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante chamadas para as funções [**WSASetService**](bluetooth-and-wsasetservice.md) ou **WSALookupService** \* . <br/>             |
| [Bluetooth e conectar](bluetooth-and-connect.md)                                               | O Bluetooth usa a função [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) para se conectar a um dispositivo Bluetooth de destino, usando um soquete Bluetooth criado anteriormente.<br/>                                                                                                                                                              |
| [Bluetooth e getaddrinfo](bluetooth-and-getaddrinfo.md)                                       | A função [**Getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) fornece a tradução do nome do host para tratar de transportes baseados em IP.<br/>                                                                                                                                                                                   |
| [Bluetooth e getemparelhaname](bluetooth-and-getpeername.md)                                       | Usado para recuperar o endereço Bluetooth do dispositivo Bluetooth de mesmo nível.<br/>                                                                                                                                                                                                                                            |
| [Bluetooth e getsockname](bluetooth-and-getsockname.md)                                       | O Bluetooth usa a função [**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) para recuperar o endereço do dispositivo do servidor e o número da porta alocada a um soquete por meio de uma chamada anterior à função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) .<br/>                                                                                            |
| [Bluetooth e getsockopt](bluetooth-and-getsockopt.md)                                         | O Bluetooth usa a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para consultar vários parâmetros associados ao canal do servidor ou à conexão. <br/>                                                                                                                                                           |
| [Bluetooth e escutar, selecionar e fechamento](bluetooth-and-listen-select-and-closesocket.md) | O Bluetooth usa as funções [**escutar**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**selecionar**](/windows/desktop/api/winsock2/nf-winsock2-select)e [**fechamento**](/windows/desktop/api/winsock/nf-winsock-closesocket) sem qualquer modificação da programação padrão de soquetes do Windows.<br/>                                                                                                   |
| [Operações de leitura ou gravação de Bluetooth](bluetooth-and-read-or-write-operations.md)             | Detalha as operações de leitura e gravação do Winsock com suporte.<br/>                                                                                                                                                                                                                                                        |
| [Bluetooth e setsockopt](bluetooth-and-setsockopt.md)                                         | O Bluetooth usa a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para definir vários parâmetros associados ao canal do servidor ou à conexão.<br/>                                                                                                                                                              |
| [Bluetooth e desligar](bluetooth-and-shutdown.md)                                             | O Bluetooth usa a função de [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) para se desconectar do rádio remoto.<br/>                                                                                                                                                                                                             |
| [Bluetooth e soquete](bluetooth-and-socket.md)                                                 | O Bluetooth usa a função [**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket) cria um soquete para conexões de entrada ou saída.<br/>                                                                                                                                                                                               |
| [Opções de Bluetooth e soquete](bluetooth-and-socket-options.md)                                 | Detalha as opções de soquete com suporte do Bluetooth da Microsoft.<br/>                                                                                                                                                                                                                                                    |
| [Bluetooth e WSAAddressToString](bluetooth-and-wsaaddresstostring.md)                         | Usado para converter um endereço de dispositivo Bluetooth em uma cadeia de caracteres, que, por sua vez, é fornecido para a função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) por meio da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) ao recuperar informações de serviço do dispositivo.<br/>                                           |
| [Bluetooth e WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)                   | O Bluetooth usa a função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para consultar dispositivos e descobrir serviços.<br/>                                                                                                                                                                         |
| [Bluetooth e WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)                     | O Bluetooth usa a função [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) para fazer a correspondência de consultas especificadas em uma chamada anterior para [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).<br/>                                                                                                           |
| [Bluetooth e WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)                       | O Bluetooth usa a função [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) para encerrar uma consulta iniciada em uma chamada anterior para [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)e, talvez, estendida em chamadas subsequentes para [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).<br/> |
| [Bluetooth e WSAQUERYSET](bluetooth-and-wsaqueryset.md)                                       | A estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) é usada em operações, incluindo consulta de dispositivo, consulta de serviço e configuração do serviço.<br/>                                                                                                                                                                |
| [Bluetooth e WSASetService](bluetooth-and-wsasetservice.md)                                   | O Bluetooth usa a função [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para registrar ou remover uma instância de serviço no namespace do Bluetooth (ns \_ BTH) do registro.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

