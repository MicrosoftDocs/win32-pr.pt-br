---
title: Bluetooth e conectar
description: Bluetooth usa a função connect para se conectar a um dispositivo Bluetooth de destino, usando um soquete Bluetooth anteriormente criado.
ms.assetid: f9ab3934-7698-4f5e-8194-cca86685a4f8
keywords:
- Bluetooth Bluetooth
- conectar Bluetooth
- Bluetooth e conectar-se Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d38e00456b3174c49676e081a0fa6188da13fd54f8e07940edcf703e7f5b680d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119588456"
---
# <a name="bluetooth-and-connect"></a>Bluetooth e conectar

Bluetooth usa a [**função connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) para se conectar a um dispositivo Bluetooth de destino, usando um soquete Bluetooth anteriormente criado. O *parâmetro* name da **função connect,** que é uma estrutura [**\_ BTH SOCKADDR,**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) deve especificar um dispositivo Bluetooth destino. Dois mecanismos são usados para identificar o dispositivo de destino:

-   A [**estrutura \_ BTH SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) pode especificar diretamente o número da porta à qual uma conexão é solicitada. Esse mecanismo exige que o aplicativo execute suas próprias consultas SDP antes de tentar uma [**operação de**](/windows/desktop/api/winsock2/nf-winsock2-connect) conexão.
-   A [**estrutura \_ BTH SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) pode especificar a ID de classe de serviço exclusiva do serviço ao qual deseja se conectar. Se o dispositivo par tiver mais de uma porta que [](/windows/desktop/api/winsock2/nf-winsock2-connect) corresponde à ID da classe de serviço, a chamada de função de conexão se conectará ao primeiro serviço válido. Esse mecanismo pode ser usado sem consultas SDP anteriores.

Ao usar a [**estrutura \_ BTH SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) com a [**função connect,**](/windows/desktop/api/winsock2/nf-winsock2-connect) os seguintes requisitos se aplicam:

-   O **membro btAddr** deve ser um endereço de rádio remoto válido.
-   Para o **membro serviceClassId,** se o membro da porta for zero, o sistema tentará usar **serviceClassId** para resolver a porta remota correspondente ao serviço. A classe de serviço é um GUID normalizado de 128 bits, definido pela especificação Bluetooth dados. GUIDs comuns são definidos pelo documento Bluetooth números atribuídos. Como alternativa, um GUID exclusivo pode ser usado para um aplicativo específico do domínio.
-   O **membro** da porta deve ser uma porta remota válida ou zero se **o membro serviceClassId** for especificado.

A tabela a seguir lista os códigos de resultado para Bluetooth e a [**função connect.**](/windows/desktop/api/winsock2/nf-winsock2-connect)

| Erro/erro\#                    | Descrição                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| WSAEISCONN10056<br/>       | A [**função connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) chamada para soquete já conectado. |
| WSAEACCES10013<br/>        | A conexão do aplicativo solicitou autenticação, mas a autenticação falhou.        |
| WSAENOBUFS10055<br/>       | Erro de falta de memória irrecuperável.                                                 |
| WSAEADDRINUSE10048<br/>    | O número da porta/canal solicitado está em uso.                                       |
| WSAETIMEDOUT10060<br/>     | O tempo de E/S foi desa Bluetooth nível de rádio (PAGE \_ TIMEOUT).                    |
| WSAEDISCON10101<br/>       | O canal RFCOMM desconectado por par remoto.                                    |
| WSAECONNRESET10054<br/>    | O multiplexador RFCOMM (sessão) desconectado por par remoto.                      |
| WSAECONNABORTED10053<br/>  | Soquete desligado por aplicativo.                                                   |
| WSAENETUNREACH10051<br/>   | Erro diferente do tempo-final no L2CAP ou Bluetooth nível de rádio.                       |
| WSAEHOSTDOWN10064<br/>     | O RFCOMM recebeu a resposta DM.                                                   |
| WSAENETDOWN10050<br/>      | Erro de rede inesperado.                                                          |
| WSAESHUTDOWN10058<br/>     | O canal L2CAP desconectado por par remoto.                                     |
| WSAEADDRNOTAVAIL10049<br/> | Bluetooth porta/canal ou endereço do dispositivo não válido.                                |
| WSAEINVAL10022<br/>        | Plug and Play, evento de pilha de driver ou outro erro causou falha.                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Conectar**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> </dl>

 

