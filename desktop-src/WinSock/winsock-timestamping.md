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
# <a name="winsock-timestamping"></a><span data-ttu-id="9b470-104">Data/hora do Winsock</span><span class="sxs-lookup"><span data-stu-id="9b470-104">Winsock timestamping</span></span>

## <a name="introduction"></a><span data-ttu-id="9b470-105">Introdução</span><span class="sxs-lookup"><span data-stu-id="9b470-105">Introduction</span></span>

<span data-ttu-id="9b470-106">Os timestamps de pacote são um recurso crucial para muitos aplicativos de sincronização de &mdash; relógio, por exemplo, o Protocolo de Tempo de Precisão.</span><span class="sxs-lookup"><span data-stu-id="9b470-106">Packet timestamps are a crucial feature to many clock synchronization applications&mdash;for example, Precision Time Protocol.</span></span> <span data-ttu-id="9b470-107">Quanto mais próxima a geração de timestamp estiver quando um pacote for recebido/enviado pelo hardware do adaptador de rede, mais preciso o aplicativo de sincronização poderá ser.</span><span class="sxs-lookup"><span data-stu-id="9b470-107">The closer the timestamp generation is to when a packet is received/sent by the network adapter hardware, the more accurate the synchronization application can be.</span></span>

<span data-ttu-id="9b470-108">Portanto, as APIs de data/hora descritas neste tópico fornecem ao seu aplicativo um mecanismo para relatar os timestamps gerados bem abaixo da camada do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b470-108">So the timestamping APIs described in this topic provide your application with a mechanism to report timestamps that are generated well below the application layer.</span></span> <span data-ttu-id="9b470-109">Especificamente, um timestamp de software na interface entre o miniporte e o NDIS e um timestamp de hardware no hardware NIC.</span><span class="sxs-lookup"><span data-stu-id="9b470-109">Specifically, a software timestamp at the interface between the miniport and NDIS, and a hardware timestamp in the NIC hardware.</span></span> <span data-ttu-id="9b470-110">A API de data/hora pode melhorar muito a precisão da sincronização do relógio.</span><span class="sxs-lookup"><span data-stu-id="9b470-110">The timestamping API can greatly improve clock synchronization accuracy.</span></span> <span data-ttu-id="9b470-111">Atualmente, o suporte está no escopo de soquetes UDP (User Datagram Protocol).</span><span class="sxs-lookup"><span data-stu-id="9b470-111">Currently, support is scoped to User Datagram Protocol (UDP) sockets.</span></span>

## <a name="receive-timestamps"></a><span data-ttu-id="9b470-112">Receber os tempos de data/hora</span><span class="sxs-lookup"><span data-stu-id="9b470-112">Receive timestamps</span></span>

<span data-ttu-id="9b470-113">Você configura a recepção de data/hora de recebimento [**por meio do SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span><span class="sxs-lookup"><span data-stu-id="9b470-113">You configure receive timestamp reception through the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span></span> <span data-ttu-id="9b470-114">Use esse IOCTL para habilitar a recepção do timestamp de recebimento.</span><span class="sxs-lookup"><span data-stu-id="9b470-114">Use that IOCTL to enable receive timestamp reception.</span></span> <span data-ttu-id="9b470-115">Quando você recebe um datagrama usando a função [**LPFN_WSARECVMSG (WSARecvMsg),**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) seu timestamp (se disponível) está contido na mensagem **SO_TIMESTAMP** controle.</span><span class="sxs-lookup"><span data-stu-id="9b470-115">When you receive a datagram using the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function, its timestamp (if available) is contained in the **SO_TIMESTAMP** control message.</span></span>

<span data-ttu-id="9b470-116">**SO_TIMESTAMP** (0x300A) é definido em `mstcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="9b470-116">**SO_TIMESTAMP** (0x300A) is defined in `mstcpip.h`.</span></span> <span data-ttu-id="9b470-117">Os dados da mensagem de controle são retornados como **um UINT64.**</span><span class="sxs-lookup"><span data-stu-id="9b470-117">The control message data is returned as a **UINT64**.</span></span>

## <a name="transmit-timestamps"></a><span data-ttu-id="9b470-118">Transmitir os timestamps</span><span class="sxs-lookup"><span data-stu-id="9b470-118">Transmit timestamps</span></span>

<span data-ttu-id="9b470-119">A recepção do timestamp de transmissão também é configurada por meio [**do SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span><span class="sxs-lookup"><span data-stu-id="9b470-119">Transmit timestamp reception is also configured through the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) IOCTL.</span></span> <span data-ttu-id="9b470-120">Use esse IOCTL para habilitar a recepção do timestamp de transmissão e especifique o número de data/hora de transmissão que o sistema vai buffer.</span><span class="sxs-lookup"><span data-stu-id="9b470-120">Use that IOCTL to enable transmit timestamp reception, and specify the number of transmit timestamps that the system will buffer.</span></span> <span data-ttu-id="9b470-121">À medida que osstamps de hora de transmissão são gerados, eles são adicionados ao buffer.</span><span class="sxs-lookup"><span data-stu-id="9b470-121">As transmit timestamps are generated, they are added to the buffer.</span></span> <span data-ttu-id="9b470-122">Se o buffer estiver cheio, novos carimbos de data/hora de transmissão serão descartados.</span><span class="sxs-lookup"><span data-stu-id="9b470-122">If the buffer is full, new transmit timestamps are discarded.</span></span>

<span data-ttu-id="9b470-123">Ao enviar um datagrama, associe o datagrama a uma mensagem de controle de **SO_TIMESTAMP_ID** .</span><span class="sxs-lookup"><span data-stu-id="9b470-123">When sending a datagram, associate the datagram with an **SO_TIMESTAMP_ID** control message.</span></span> <span data-ttu-id="9b470-124">Deve conter um identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="9b470-124">This should contain a unique identifier.</span></span> <span data-ttu-id="9b470-125">Envie o datagrama, junto com sua mensagem de controle de **SO_TIMESTAMP_ID** , usando [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg).</span><span class="sxs-lookup"><span data-stu-id="9b470-125">Send the datagram, along with its **SO_TIMESTAMP_ID** control message, using [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg).</span></span> <span data-ttu-id="9b470-126">Os carimbos de data/hora de transmissão podem não estar imediatamente disponíveis após o retorno de **WSASendMsg** .</span><span class="sxs-lookup"><span data-stu-id="9b470-126">Transmit timestamps might not be immediately available after **WSASendMsg** returns.</span></span> <span data-ttu-id="9b470-127">À medida que os carimbos de data/hora de transmissão ficam disponíveis, eles são colocados em um buffer por soquete.</span><span class="sxs-lookup"><span data-stu-id="9b470-127">As transmit timestamps become available, they are placed into a per-socket buffer.</span></span> <span data-ttu-id="9b470-128">Use o [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL para sondar o carimbo de data/hora por sua ID.</span><span class="sxs-lookup"><span data-stu-id="9b470-128">Use the [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) IOCTL to poll for the timestamp by its ID.</span></span> <span data-ttu-id="9b470-129">Se o carimbo de data/hora estiver disponível, ele será removido do buffer e retornado.</span><span class="sxs-lookup"><span data-stu-id="9b470-129">If the timestamp is available, then it is removed from the buffer and returned.</span></span> <span data-ttu-id="9b470-130">Se o carimbo de data/hora não estiver disponível, [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) retornará **WSAEWOULDBLOCK**.</span><span class="sxs-lookup"><span data-stu-id="9b470-130">If the timestamp is not available, then [WSAGetLastError](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) returns **WSAEWOULDBLOCK**.</span></span> <span data-ttu-id="9b470-131">Se um carimbo de data/hora de transmissão for gerado enquanto o buffer estiver cheio, o novo carimbo de data/hora será Descartado.</span><span class="sxs-lookup"><span data-stu-id="9b470-131">If a transmit timestamp is generated while the buffer is full, the new timestamp is discarded.</span></span>

<span data-ttu-id="9b470-132">**SO_TIMESTAMP_ID** (0x300B) é definido em `mstcpip.h` .</span><span class="sxs-lookup"><span data-stu-id="9b470-132">**SO_TIMESTAMP_ID** (0x300B) is defined in `mstcpip.h`.</span></span> <span data-ttu-id="9b470-133">Você deve fornecer os dados da mensagem de controle como um **UINT32**.</span><span class="sxs-lookup"><span data-stu-id="9b470-133">You should supply the control message data as a **UINT32**.</span></span>

<span data-ttu-id="9b470-134">Os carimbos de data/hora são representados como um valor de contador de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9b470-134">Timestamps are represented as a 64-bit counter value.</span></span> <span data-ttu-id="9b470-135">A frequência do contador depende da origem do carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="9b470-135">The frequency of the counter depends on the source of the timestamp.</span></span> <span data-ttu-id="9b470-136">Para carimbos de data/hora de software, o contador é um valor de [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (Qpc) e você pode determinar sua frequência por meio de [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).</span><span class="sxs-lookup"><span data-stu-id="9b470-136">For software timestamps, the counter is a [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter) (QPC) value, and you can determine its frequency via [**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency).</span></span> <span data-ttu-id="9b470-137">Para carimbos de data/hora de hardware NIC, a frequência do contador depende do hardware da NIC e você pode determinar isso com informações adicionais fornecidas pelo [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp).</span><span class="sxs-lookup"><span data-stu-id="9b470-137">For NIC hardware timestamps, the counter frequency is dependent on the NIC hardware, and you can determine it with additional information given by [**CaptureInterfaceHardwareCrossTimestamp**](/windows/win32/api/iphlpapi/nf-iphlpapi-captureinterfacehardwarecrosstimestamp).</span></span> <span data-ttu-id="9b470-138">Para determinar a fonte de carimbos de data/hora, use as funções [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) e [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) .</span><span class="sxs-lookup"><span data-stu-id="9b470-138">To determine the source of timestamps, use the [**GetInterfaceActiveTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfaceactivetimestampcapabilities) and [**GetInterfaceSupportedTimestampCapabilities**](/windows/win32/api/iphlpapi/nf-iphlpapi-getinterfacesupportedtimestampcapabilities) functions.</span></span>

<span data-ttu-id="9b470-139">Além da configuração em nível de soquete usando a opção de soquete [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) para habilitar a recepção de carimbo de data/hora para um soquete, a configuração de nível de sistema também é necessária.</span><span class="sxs-lookup"><span data-stu-id="9b470-139">In addition to socket-level configuration using the [**SIO_TIMESTAMPING**](/windows/win32/winsock/winsock-ioctls#sio_timestamping) socket option to enable timestamp reception for a socket, system-level configuration is also needed.</span></span>

## <a name="estimating-latency-of-socket-send-path"></a><span data-ttu-id="9b470-140">Estimando a latência do caminho de envio do soquete</span><span class="sxs-lookup"><span data-stu-id="9b470-140">Estimating latency of socket send path</span></span>

<span data-ttu-id="9b470-141">Nesta seção, usaremos os carimbos de hora de transmissão para estimar a latência do caminho de envio do soquete.</span><span class="sxs-lookup"><span data-stu-id="9b470-141">In this section, we'll use transmit timestamps to estimate the latency of the socket send path.</span></span> <span data-ttu-id="9b470-142">Se você tiver um aplicativo existente que consome os tempos de E/S no nível do aplicativo em que o timestamp precisa ser o mais próximo possível do ponto real de transmissão, este exemplo fornece uma descrição quantitativa de quanto as APIs de data/hora winsock podem melhorar a precisão &mdash; &mdash; do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9b470-142">If you have an existing application that consumes application-level IO timestamps&mdash;where the timestamp needs to be as close as possible to the actual point of transmission&mdash;then this sample provides a quantitative description as to how much the Winsock timestamping APIs can improve the accuracy of your application.</span></span>

<span data-ttu-id="9b470-143">O exemplo presume que há apenas uma NIC (placa de adaptador de rede) no sistema e que *interfaceLuid* é o LUID desse adaptador.</span><span class="sxs-lookup"><span data-stu-id="9b470-143">The example assumes that there's only one network interface card (NIC) in the system, and that *interfaceLuid* is the LUID of that adapter.</span></span>

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

## <a name="estimating-latency-of-socket-receive-path"></a><span data-ttu-id="9b470-144">Estimando a latência do caminho de recebimento do soquete</span><span class="sxs-lookup"><span data-stu-id="9b470-144">Estimating latency of socket receive path</span></span>

<span data-ttu-id="9b470-145">Aqui está um exemplo semelhante para o caminho de recebimento.</span><span class="sxs-lookup"><span data-stu-id="9b470-145">Here's a similar sample for the receive path.</span></span> <span data-ttu-id="9b470-146">O exemplo presume que há apenas uma NIC (placa de adaptador de rede) no sistema e que *interfaceLuid* é o LUID desse adaptador.</span><span class="sxs-lookup"><span data-stu-id="9b470-146">The example assumes that there's only one network interface card (NIC) in the system, and that *interfaceLuid* is the LUID of that adapter.</span></span>

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

## <a name="a-limitation"></a><span data-ttu-id="9b470-147">Uma limitação</span><span class="sxs-lookup"><span data-stu-id="9b470-147">A limitation</span></span>

<span data-ttu-id="9b470-148">Uma limitação das APIs de data/hora do Winsock é que chamar SIO_GET_TX_TIMESTAMP [**é**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) sempre uma operação sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="9b470-148">One limitation of the Winsock timestamping APIs is that calling [**SIO_GET_TX_TIMESTAMP**](/windows/win32/winsock/winsock-ioctls#sio_get_tx_timestamp) is always a non-blocking operation.</span></span> <span data-ttu-id="9b470-149">Mesmo chamar o IOCTL de forma OVERLAPPED resulta em um retorno imediato de **WSAEBLOCKBLOCK** se não houver nenhum timestamp de transmissão disponível no momento.</span><span class="sxs-lookup"><span data-stu-id="9b470-149">Even calling the IOCTL in an OVERLAPPED fashion results in an immediate return of **WSAEWOULDBLOCK** if there are currently no available transmit timestamps.</span></span> <span data-ttu-id="9b470-150">Como os timestamps de transmissão podem não estar imediatamente disponíveis após o [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) retornar, seu aplicativo deve sondar o IOCTL até que o timestamp seja disponibilizado.</span><span class="sxs-lookup"><span data-stu-id="9b470-150">Since transmit timestamps might not be immediately available after [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) returns, your application must poll the IOCTL until the timestamp is available.</span></span> <span data-ttu-id="9b470-151">Um timestamp de transmissão tem a garantia de estar disponível após uma chamada **WSASendMsg** bem-sucedida, considerando que o buffer de timestamp de transmissão não está cheio.</span><span class="sxs-lookup"><span data-stu-id="9b470-151">A transmit timestamp is guaranteed to be available after a successful **WSASendMsg** call given that the transmit timestamp buffer is not full.</span></span>
