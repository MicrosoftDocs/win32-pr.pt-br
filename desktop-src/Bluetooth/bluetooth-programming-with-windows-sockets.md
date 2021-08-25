---
title: Bluetooth Programação com Windows soquetes
description: Esta seção descreve como usar funções e estruturas Windows Sockets para programar um Bluetooth aplicativo.
ms.assetid: 0f15cb84-1d7a-4b64-86e8-b1b23c956c64
keywords:
- Bluetooth, tarefas
- Windows Sockets
- programando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a20cebe459f17601c1c0cbb916be8844b1edbf3b36f974b47ce0d9b28d301d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004086"
---
# <a name="bluetooth-programming-with-windows-sockets"></a>Bluetooth Programação com Windows soquetes

Esta seção descreve como usar funções e estruturas Windows Sockets para programar um Bluetooth aplicativo. Informações de referência completas para os Windows da API de Soquetes podem ser encontradas [em Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2); esta seção fornece apenas Bluetooth informações específicas para cada elemento de programação Windows Sockets.

Você também pode baixar o [exemplo Bluetooth de conexão para](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) um exemplo completo.

Assim como em todas as Windows de aplicativos soquetes, a [**função WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) deve ser chamada para iniciar a funcionalidade Windows Sockets e habilitar Bluetooth.

Os tópicos a seguir fornecem diretrizes sobre o uso de funções e estruturas Windows Sockets com a API do Microsoft Bluetooth:



| Tópico                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Bluetooth e aceitar](bluetooth-and-accept.md)                                                 | Bluetooth usa a [**função accept**](/windows/desktop/api/winsock2/nf-winsock2-accept) para habilitar tentativas de conexão de entrada em um soquete.<br/>                                                                                                                                                                                                  |
| [Bluetooth e bind](bluetooth-and-bind.md)                                                     | Bluetooth usa a [**função bind**](/windows/desktop/api/winsock/nf-winsock-bind) para se vincular a um soquete.<br/>                                                                                                                                                                                                                                     |
| [Bluetooth e BLOB](bluetooth-and-blob.md)                                                     | Bluetooth usa a estrutura [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) para passar ou receber dados específicos de transporte para a estrutura [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) durante chamadas para as funções [**WSASetService**](bluetooth-and-wsasetservice.md) ou **WSALookupService.** \* <br/>             |
| [Bluetooth e conectar](bluetooth-and-connect.md)                                               | Bluetooth usa a [**função connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) para se conectar a um dispositivo Bluetooth de destino, usando um soquete Bluetooth anteriormente criado.<br/>                                                                                                                                                              |
| [Bluetooth e getaddrinfo](bluetooth-and-getaddrinfo.md)                                       | A [**função getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) fornece tradução do nome do host para o endereço para transporte baseado em IP.<br/>                                                                                                                                                                                   |
| [Bluetooth getpeername](bluetooth-and-getpeername.md)                                       | Usado para recuperar o Bluetooth do dispositivo Bluetooth par.<br/>                                                                                                                                                                                                                                            |
| [Bluetooth e getsockname](bluetooth-and-getsockname.md)                                       | Bluetooth usa a [**função getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname) para recuperar o endereço do dispositivo do servidor e o número da porta alocados a um soquete por meio de uma chamada anterior à [**função bind.**](/windows/desktop/api/winsock/nf-winsock-bind)<br/>                                                                                            |
| [Bluetooth e getsockopt](bluetooth-and-getsockopt.md)                                         | Bluetooth usa a [**função getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) para consultar vários parâmetros associados ao canal do servidor ou à conexão. <br/>                                                                                                                                                           |
| [Bluetooth e escutar, selecionar e fechar oocket](bluetooth-and-listen-select-and-closesocket.md) | Bluetooth usa as funções [**listen**](/windows/desktop/api/winsock2/nf-winsock2-listen), [**select**](/windows/desktop/api/winsock2/nf-winsock2-select)e [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) sem nenhuma modificação da programação padrão Windows Sockets.<br/>                                                                                                   |
| [Bluetooth operações de leitura ou gravação](bluetooth-and-read-or-write-operations.md)             | Detalha as operações de leitura e gravação do Winsock com suporte.<br/>                                                                                                                                                                                                                                                        |
| [Bluetooth e setsockopt](bluetooth-and-setsockopt.md)                                         | Bluetooth usa a [**função setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para definir vários parâmetros associados ao canal do servidor ou à conexão.<br/>                                                                                                                                                              |
| [Bluetooth e desligamento](bluetooth-and-shutdown.md)                                             | Bluetooth usa a função [**de desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) para se desconectar da rádio remota.<br/>                                                                                                                                                                                                             |
| [Bluetooth soquete](bluetooth-and-socket.md)                                                 | Bluetooth usa a função [**de soquete**](/windows/desktop/api/winsock2/nf-winsock2-socket) cria um soquete para conexões de entrada ou saída.<br/>                                                                                                                                                                                               |
| [Bluetooth e opções de soquete](bluetooth-and-socket-options.md)                                 | Detalha as opções de soquete com suporte da Microsoft Bluetooth.<br/>                                                                                                                                                                                                                                                    |
| [Bluetooth e WSAAddressToString](bluetooth-and-wsaaddresstostring.md)                         | Usado para converter um endereço Bluetooth dispositivo em uma cadeia de caracteres, que, por sua vez, é fornecida para a função [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) por meio da estrutura [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) ao recuperar informações de serviço do dispositivo.<br/>                                           |
| [Bluetooth e WSALookupServiceBegin](bluetooth-and-wsalookupservicebegin.md)                   | Bluetooth usa a [**função WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) para consultar dispositivos e descobrir serviços.<br/>                                                                                                                                                                         |
| [Bluetooth e WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)                     | Bluetooth usa a [**função WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) para corresponder às consultas especificadas em uma chamada anterior para [**WSALookupServiceBegin.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)<br/>                                                                                                           |
| [Bluetooth e WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)                       | Bluetooth usa a [**função WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) para encerrar uma consulta iniciada em uma chamada anterior para [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)e talvez estendida em chamadas subsequentes para [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).<br/> |
| [Bluetooth e WSAQUERYSET](bluetooth-and-wsaqueryset.md)                                       | A [**estrutura WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) é usada em operações, incluindo consulta de dispositivo, consulta de serviço e configuração do serviço.<br/>                                                                                                                                                                |
| [Bluetooth e WSASetService](bluetooth-and-wsasetservice.md)                                   | Bluetooth usa a [**função WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) para registrar ou remover uma instância de serviço no namespace Bluetooth (NS \_ BTH) do Registro.<br/>                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

