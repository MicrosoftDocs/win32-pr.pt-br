---
title: Bluetooth e conectar
description: O Bluetooth usa a função Connect para se conectar a um dispositivo Bluetooth de destino, usando um soquete Bluetooth criado anteriormente.
ms.assetid: f9ab3934-7698-4f5e-8194-cca86685a4f8
keywords:
- Bluetooth de Bluetooth
- conectar Bluetooth
- Bluetooth e conectar Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b631aabbcd44d009ba30b9deb486e92a22feaec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454301"
---
# <a name="bluetooth-and-connect"></a>Bluetooth e conectar

O Bluetooth usa a função [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) para se conectar a um dispositivo Bluetooth de destino, usando um soquete Bluetooth criado anteriormente. O parâmetro *Name* da função **Connect** , que é uma estrutura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) , deve especificar um dispositivo Bluetooth de destino. Dois mecanismos são usados para identificar o dispositivo de destino:

-   A estrutura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) pode especificar diretamente o número da porta à qual uma conexão é solicitada. Esse mecanismo exige que o aplicativo execute suas próprias consultas SDP antes de tentar uma operação de [**conexão**](/windows/desktop/api/winsock2/nf-winsock2-connect) .
-   A estrutura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) pode especificar a ID de classe de serviço exclusiva do serviço ao qual deseja se conectar. Se o dispositivo par tiver mais de uma porta que corresponda à ID de classe de serviço, a chamada de função [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) se conectará ao primeiro serviço válido. Esse mecanismo pode ser usado sem consultas SDP anteriores.

Ao usar a estrutura [**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) com a função [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) , os seguintes requisitos se aplicam:

-   O membro **btAddr** deve ser um endereço de rádio remoto válido.
-   Para o membro Service **ClassID** , se o membro da porta for zero, o sistema tentará usar **o** ServiceId para resolver a porta remota correspondente ao serviço. A classe de serviço é um GUID de 128 bits normalizado, definido pela especificação de Bluetooth. Os GUIDs comuns são definidos pelo documento números de Bluetooth atribuídos. Como alternativa, um GUID exclusivo pode ser usado para um aplicativo específico de domínio.
-   O membro da porta deve ser uma porta remota válida ou zero **se o membro** do **ServicePortal** for especificado.

A tabela a seguir lista os códigos de resultado para Bluetooth e a função [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) .

| Erro/erro\#                    | Descrição                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| WSAEISCONN10056<br/>       | A função [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) chamada para soquete já conectado. |
| WSAEACCES10013<br/>        | Conectando a autenticação solicitada do aplicativo, mas a autenticação falhou.        |
| WSAENOBUFS10055<br/>       | Erro irrecuperável de memória insuficiente.                                                 |
| WSAEADDRINUSE10048<br/>    | O número de porta/canal solicitado está em uso.                                       |
| WSAETIMEDOUT10060<br/>     | O tempo limite de e/s foi atingido no nível de rádio Bluetooth ( \_ tempo limite da página).                    |
| WSAEDISCON10101<br/>       | O canal RFCOMM desconectado por um par remoto.                                    |
| WSAECONNRESET10054<br/>    | O multiplexador RFCOMM (sessão) desconectado por um par remoto.                      |
| WSAECONNABORTED10053<br/>  | O soquete foi desligado pelo aplicativo.                                                   |
| WSAENETUNREACH10051<br/>   | Erro diferente de tempo limite em nível de rádio L2CAP ou Bluetooth.                       |
| WSAEHOSTDOWN10064<br/>     | O RFCOMM recebeu a resposta DM.                                                   |
| WSAENETDOWN10050<br/>      | Erro de rede inesperado.                                                          |
| WSAESHUTDOWN10058<br/>     | O canal L2CAP desconectado por um par remoto.                                     |
| WSAEADDRNOTAVAIL10049<br/> | Porta/canal Bluetooth ou endereço de dispositivo inválido.                                |
| WSAEINVAL10022<br/>        | Plug and Play, evento de pilha de driver ou outro erro causou falha.                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> </dl>

 

