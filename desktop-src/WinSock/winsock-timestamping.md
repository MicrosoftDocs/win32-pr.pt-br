---
title: Data/hora do Winsock
description: Os timestamps de pacote são um recurso crucial para muitos aplicativos de sincronização de &mdash; relógio, por exemplo, o Protocolo de Tempo de Precisão. Quanto mais próxima a geração de timestamp estiver quando um pacote for recebido/enviado pelo hardware do adaptador de rede, mais preciso o aplicativo de sincronização poderá ser.
ms.topic: article
ms.date: 10/22/2020
ms.openlocfilehash: eae0dce8c2c16bc187ef5522f323e7f36d7fc0b4
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559926"
---
# <a name="winsock-timestamping"></a>Data/hora do Winsock

## <a name="introduction"></a>Introdução

Os timestamps de pacote são um recurso crucial para muitos aplicativos de sincronização de &mdash; relógio, por exemplo, o Protocolo de Tempo de Precisão. Quanto mais próxima a geração de timestamp estiver quando um pacote for recebido/enviado pelo hardware do adaptador de rede, mais preciso o aplicativo de sincronização poderá ser.

Portanto, as APIs de data/hora descritas neste tópico fornecem ao seu aplicativo um mecanismo para relatar os timestamps gerados bem abaixo da camada do aplicativo. Especificamente, um timestamp de software na interface entre o miniporte e o NDIS e um timestamp de hardware no hardware NIC. A API de data/hora pode melhorar muito a precisão da sincronização do relógio. Atualmente, o suporte está no escopo de soquetes UDP (User Datagram Protocol).

## <a name="receive-timestamps"></a>Receber os tempos de data/hora

Você configura a recepção de data/hora de recebimento [**por meio do SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL. Use esse IOCTL para habilitar a recepção do timestamp de recebimento. Quando você recebe um datagrama usando a função [**LPFN_WSARECVMSG (WSARecvMsg),**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) seu timestamp (se disponível) está contido na mensagem **SO_TIMESTAMP** controle.

**SO_TIMESTAMP** (0x300A) é definido em `mstcpip.h` . Os dados da mensagem de controle são retornados como **um UINT64.**

## <a name="transmit-timestamps"></a>Transmitir os timestamps

A recepção do timestamp de transmissão também é configurada por meio [**do SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL. Use esse IOCTL para habilitar a recepção do timestamp de transmissão e especifique o número de data/hora de transmissão que o sistema vai buffer. À medida que osstamps de hora de transmissão são gerados, eles são adicionados ao buffer. Se o buffer estiver cheio, novos carimbos de data/hora de transmissão serão descartados.

Ao enviar um datagrama, associe o datagrama a uma mensagem de controle de **SO_TIMESTAMP_ID** . Deve conter um identificador exclusivo. Envie o datagrama, junto com sua mensagem de controle de **SO_TIMESTAMP_ID** , usando [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg). Os carimbos de data/hora de transmissão podem não estar imediatamente disponíveis após o retorno de **WSASendMsg** . À medida que os carimbos de data/hora de transmissão ficam disponíveis, eles são colocados em um buffer por soquete. Use o [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL para sondar o carimbo de data/hora por sua ID. Se o carimbo de data/hora estiver disponível, ele será removido do buffer e retornado. Se o carimbo de data/hora não estiver disponível, [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) retornará **WSAEWOULDBLOCK**. Se um carimbo de data/hora de transmissão for gerado enquanto o buffer estiver cheio, o novo carimbo de data/hora será Descartado.

**SO_TIMESTAMP_ID** (0x300B) é definido em `mstcpip.h` . Você deve fornecer os dados da mensagem de controle como um **UINT32**.

Os carimbos de data/hora são representados como um valor de contador de 64 bits. A frequência do contador depende da origem do carimbo de data/hora. Para carimbos de data/hora de software, o contador é um valor de [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (Qpc) e você pode determinar sua frequência por meio de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency). Para carimbos de data/hora de hardware NIC, a frequência do contador depende do hardware da NIC e você pode determinar isso com informações adicionais fornecidas pelo [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp). Para determinar a fonte de carimbos de data/hora, use as funções [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) e [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) .

Além da configuração em nível de soquete usando a opção de soquete [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) para habilitar a recepção de carimbo de data/hora para um soquete, a configuração de nível de sistema também é necessária.

## <a name="estimating-latency-of-socket-send-path"></a>Estimando a latência do caminho de envio do soquete

Nesta seção, usaremos os carimbos de hora de transmissão para estimar a latência do caminho de envio do soquete. Se você tiver um aplicativo existente que consome os tempos de E/S no nível do aplicativo em que o timestamp precisa ser o mais próximo possível do ponto real de transmissão, este exemplo fornece uma descrição quantitativa de quanto as APIs de data/hora winsock podem melhorar a precisão &mdash; &mdash; do seu aplicativo.

O exemplo presume que há apenas uma NIC (placa de adaptador de rede) no sistema e que *interfaceLuid* é o LUID desse adaptador.

```c
void QueryHardwareClockFrequency(LARGE_INTEGER* clockFrequency)
{
    // Returns the hardware clock frequency. This can be calculated by
    // collecting crosstimestamps via CaptureInterfaceHardwareCrossTimestamp
    // and forming a linear regression model.
}

void estimate_send_latency(SOCKET sock,
    PSOCKADDR_STORAGE addr,
    NET_LUID* interfaceLuid,
    BOOLEAN hardwareTimestampSource)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT32))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    ULONG64 appLevelTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)addr;
    wsaMsg.namelen = (INT)INET_SOCKADDR_LENGTH(addr->ss_family);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure tx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.flags |= TIMESTAMPING_FLAG_TX;
    config.txTimestampsBuffered = 1;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    // Assign a tx timestamp ID to this datagram.
    UINT32 txTimestampId = 123;
    PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    cmsg->cmsg_len = WSA_CMSG_LEN(sizeof(UINT32));
    cmsg->cmsg_level = SOL_SOCKET;
    cmsg->cmsg_type = SO_TIMESTAMP_ID;
    *(PUINT32)WSA_CMSG_DATA(cmsg) = txTimestampId;

    // Capture app-layer timestamp prior to send call.
    if (hardwareTimestampSource) {
        INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp = { 0 };
        crossTimestamp.Version = INTERFACE_HARDWARE_CROSSTIMESTAMP_VERSION_1;
        error = CaptureInterfaceHardwareCrossTimestamp(interfaceLuid, &crossTimestamp);
        if (error != NO_ERROR) {
            printf("CaptureInterfaceHardwareCrossTimestamp failed %d\n", error);
            return;
        }
        appLevelTimestamp = crossTimestamp.HardwareClockTimestamp;
    }
    else { // software source
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;
    }

    error =
        sendmsg(
            sock,
            &wsaMsg,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("sendmsg failed %d\n", WSAGetLastError());
        return;
    }

    printf("sent packet\n");

    // Poll for the socket tx timestamp value. The timestamp may not be available
    // immediately.
    UINT64 socketTimestamp;
    ULONG maxTimestampPollAttempts = 6;
    ULONG txTstampRetrieveIntervalMs = 1;
    BOOLEAN retrievedTimestamp = FALSE;
    for (ULONG i = 0; i < maxTimestampPollAttempts; i++) {
        error =
            WSAIoctl(
                sock,
                SIO_GET_TX_TIMESTAMP,
                &txTimestampId,
                sizeof(txTimestampId),
                &socketTimestamp,
                sizeof(socketTimestamp),
                &numBytes,
                NULL,
                NULL);
        if (error != SOCKET_ERROR) {
            ASSERT(numBytes == sizeof(timestamp));
            ASSERT(timestamp != 0);
            retrievedTimestamp = TRUE;
            break;
        }

        error = WSAGetLastError();
        if (error != WSAEWOULDBLOCK) {
            printf(“WSAIoctl failed % d\n”, error);
            break;
        }

        Sleep(txTstampRetrieveIntervalMs);
        txTstampRetrieveIntervalMs *= 2;
    }

    if (retrievedTimestamp) {
        LARGE_INTEGER clockFrequency;
        ULONG64 elapsedMicroseconds;

        if (hardwareTimestampSource) {
            QueryHardwareClockFrequency(&clockFrequency);
        }
        else { // software source
            QueryPerformanceFrequency(&clockFrequency);
        }

        // Compute socket send path latency.
        elapsedMicroseconds = socketTimestamp - appLevelTimestamp;
        elapsedMicroseconds *= 1000000;
        elapsedMicroseconds /= clockFrequency.QuadPart;
        printf("socket send path latency estimation: %lld microseconds\n",
            elapsedMicroseconds);
    }
    else {
        printf("failed to retrieve TX timestamp\n");
    }
}
```

## <a name="estimating-latency-of-socket-receive-path"></a>Estimando a latência do caminho de recebimento do soquete

Aqui está um exemplo semelhante para o caminho de recebimento. O exemplo presume que há apenas uma NIC (placa de adaptador de rede) no sistema e que *interfaceLuid* é o LUID desse adaptador.

```c
void QueryHardwareClockFrequency(LARGE_INTEGER* clockFrequency)
{
    // Returns the hardware clock frequency. This can be calculated by
    // collecting crosstimestamps via CaptureInterfaceHardwareCrossTimestamp
    // and forming a linear regression model.
}

void estimate_receive_latency(SOCKET sock,
    NET_LUID* interfaceLuid,
    BOOLEAN hardwareTimestampSource)
{
    DWORD numBytes;
    INT error;
    CHAR data[512];
    CHAR control[WSA_CMSG_SPACE(sizeof(UINT64))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    UINT64 socketTimestamp = 0;
    ULONG64 appLevelTimestamp;

    dataBuf.buf = data;
    dataBuf.len = sizeof(data);
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = NULL;
    wsaMsg.namelen = 0;
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    // Configure rx timestamp reception.
    TIMESTAMPING_CONFIG config = { 0 };
    config.flags |= TIMESTAMPING_FLAG_RX;
    error =
        WSAIoctl(
            sock,
            SIO_TIMESTAMPING,
            &config,
            sizeof(config),
            NULL,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("WSAIoctl failed %d\n", WSAGetLastError());
        return;
    }

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return;
    }

    // Capture app-layer timestamp upon message reception.
    if (hardwareTimestampSource) {
        INTERFACE_HARDWARE_CROSSTIMESTAMP crossTimestamp = { 0 };
        crossTimestamp.Version = INTERFACE_HARDWARE_CROSSTIMESTAMP_VERSION_1;
        error = CaptureInterfaceHardwareCrossTimestamp(interfaceLuid, &crossTimestamp);
        if (error != NO_ERROR) {
            printf("CaptureInterfaceHardwareCrossTimestamp failed %d\n", error);
            return;
        }
        appLevelTimestamp = crossTimestamp.HardwareClockTimestamp;
    }
    else { // software source
        LARGE_INTEGER t1;
        QueryPerformanceCounter(&t1);
        appLevelTimestamp = t1.QuadPart;
    }

    printf("received packet\n");

    // Look for socket rx timestamp returned via control message.
    BOOLEAN retrievedTimestamp = FALSE;
    PCMSGHDR cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    while (cmsg != NULL) {
        if (cmsg->cmsg_level == SOL_SOCKET && cmsg->cmsg_type == SO_TIMESTAMP) {
            socketTimestamp = *(PUINT64)WSA_CMSG_DATA(cmsg);
            retrievedTimestamp = TRUE;
            break;
        }
        cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
    }

    if (retrievedTimestamp) {
        // Compute socket receive path latency.
        LARGE_INTEGER clockFrequency;
        ULONG64 elapsedMicroseconds;

        if (hardwareTimestampSource) {
            QueryHardwareClockFrequency(&clockFrequency);
        }
        else { // software source
            QueryPerformanceFrequency(&clockFrequency);
        }

        // Compute socket send path latency.
        elapsedMicroseconds = appLevelTimestamp - socketTimestamp;
        elapsedMicroseconds *= 1000000;
        elapsedMicroseconds /= clockFrequency.QuadPart;
        printf("RX latency estimation: %lld microseconds\n",
            elapsedMicroseconds);
    }
    else {
        printf("failed to retrieve RX timestamp\n");
    }
}
```

## <a name="a-limitation"></a>Uma limitação

Uma limitação das APIs de data/hora do Winsock é que chamar SIO_GET_TX_TIMESTAMP [**é**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) sempre uma operação sem bloqueio. Mesmo chamar o IOCTL de forma OVERLAPPED resulta em um retorno imediato de **WSAEBLOCKBLOCK** se não houver nenhum timestamp de transmissão disponível no momento. Como os timestamps de transmissão podem não estar imediatamente disponíveis após o [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) retornar, seu aplicativo deve sondar o IOCTL até que o timestamp seja disponibilizado. Um timestamp de transmissão tem a garantia de estar disponível após uma chamada **WSASendMsg** bem-sucedida, considerando que o buffer de timestamp de transmissão não está cheio.
