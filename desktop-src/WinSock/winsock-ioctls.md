---
description: Tópico de navegação para os IOCTLs de soquete do Windows Sockets (Winsock).
ms.assetid: 6a63c2c9-4e09-4a62-b39f-3ccb26287da8
title: Winsock IOCTLs (Winsock2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eadf4a0e2799d6123bf81069fe65ea16313af444
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550251"
---
# <a name="winsock-ioctls"></a>Winsock IOCTLs

Esta seção descreve os controles de entrada/saída de soquete do Winsock (IOCTLs) para várias edições de sistemas operacionais Windows. Use a função [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) ou [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) para emitir um Winsock IOCTL para controlar o modo de um soquete, o protocolo de transporte ou o subsistema de comunicações.

Alguns IOCTLs Winsock exigem mais explicações do que essa tabela pode transmitir; essas opções contêm links para tópicos adicionais.

É possível adotar um esquema de codificação que preserve os opcodes [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) definidos atualmente, fornecendo uma maneira conveniente de particionar o espaço do identificador de opcode em tanto quanto o parâmetro *dwIoControlCode* agora é uma entidade de 32 bits. O parâmetro *dwIoControlCode* foi criado para permitir a independência de protocolo e fornecedor ao adicionar novos códigos de controle, mantendo a compatibilidade com versões anteriores com os códigos de controle do Windows sockets 1,1 e UNIX. O parâmetro *dwIoControlCode* tem o seguinte formato.

| I  | O  | V  | T  | Família de fornecedor/endereço | Código                   |
|-|-|-|-|-|-|
| 3  | 3  | 2  | 2 2 | 2 2 2 2 2 2 2 1 1 1 1 | 1 1 1 1 1 1              |
| 1  | 0  | 9  | 8 7 | 6 5 4 3 2 1 0 9 8 7 6 | 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 |

> [!Note] 
> Os bits no parâmetro *dwIoControlCode* exibidos na tabela devem ser lidos verticalmente de cima para baixo por coluna. Assim, o bit mais à esquerda é 31 bit, o bit seguinte é 30 e o bit mais à direita é bit 0.

Vou definir se o buffer de entrada é válido para o código, assim como com **IOC_IN**.

O será definido se o buffer de saída for válido para o código, assim como ocorre com **IOC_OUT**. Os códigos de controle que usam os buffers de entrada e saída definem I e O.

V será definido se não houver parâmetros para o código, como com **IOC_VOID**.

T é uma quantidade de 2 bits que define o tipo do IOCTL. Os seguintes valores são definidos:

0 O IOCTL é um código IOCTL Unix padrão, assim como ocorre com **FIONREAD** e **FIONBIO.**

1 O IOCTL é um código IOCTL genérico do Windows Sockets 2. Novos códigos IOCTL definidos para Windows Sockets 2 terão T == 1.

2 O IOCTL se aplica somente a uma família de endereços específica.

3 O IOCTL aplica-se somente ao provedor de um fornecedor específico, assim como ocorre com **IOC_VENDOR**. Esse tipo permite que as empresas sejam atribuídas a um número de fornecedor que aparece no parâmetro **família Vendor/Address.** Em seguida, o fornecedor pode definir novas IOCTLs específicas para esse fornecedor sem precisar registrar o IOCTL em uma limpeza, fornecendo flexibilidade e privacidade ao fornecedor.

**Família de fornecedores/endereços** Uma quantidade de 11 bits que define o fornecedor que possui o código (se T == 3) ou que contém a família de endereços à qual o código se aplica (se T == 2). Se esse for um código unix IOCTL (T == 0), esse parâmetro terá o mesmo valor que o código no Unix. Se esse for um IOCTL genérico do Windows Sockets 2 (T == 1), esse parâmetro poderá ser usado como uma extensão do parâmetro de código para fornecer valores de código adicionais.

**Código** A quantidade de 16 bits que contém o código IOCTL específico para a operação.

## <a name="unix-ioctl-codes"></a>Códigos IOCTL do Unix

Há suporte para os seguintes códigos unix IOCTL (comandos).

### <a name="fionbio"></a>FIONBIO

Habilita ou desabilita o modo sem bloqueio no *soquete.* O *parâmetro lpvInBuffer* aponta para um QoS (unsigned **long),** que será diferente de zero se o modo sem bloqueio for habilitado e zero se ele for desabilitado. Quando um soquete é criado, ele opera no modo de bloqueio (ou seja, o modo sem bloqueio está desabilitado). Isso é consistente com os soquetes BSD.

A rotina [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) ou [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) define automaticamente um soquete para o modo sem bloqueio. Se **WSAAsyncSelect** ou **WSAEventSelect** tiver sido emitido em um soquete, qualquer tentativa de usar o [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) para definir o soquete de volta para o modo de bloqueio falhará com WSAEINVAL. Para definir o soquete de volta para o modo de bloqueio, um aplicativo deve primeiro desabilitar **WSAAsyncSelect** chamando **WSAAsyncSelect** com o parâmetro *Levent* igual a zero ou desabilitar **WSAEventSelect** chamando **WSAEventSelect** com o parâmetro *lNetworkEvents* igual a zero.

### <a name="fionread"></a>FIONREAD

Determine a quantidade de dados que podem ser lidos atomicamente do soquete *s*. O parâmetro *lpvOutBuffer* aponta para um **longo não assinado** no qual o [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) armazena o resultado.

Se o soquete passado no parâmetro *s* for orientado a fluxo (por exemplo, tipo Sock \_ Stream), **FIONREAD** retornará a quantidade total de dados que podem ser lidos em uma única operação de recebimento; normalmente, isso é o mesmo que a quantidade total de dados enfileirados no soquete (uma vez que um fluxo de dados é orientado por byte, isso não é garantido).

Se o soquete passado no parâmetro *s* for orientado a mensagens (por exemplo, digite Sock \_ DGRAM), **FIONREAD** retornará os relatórios o número total de bytes disponíveis para leitura, não o tamanho do primeiro datagrama (mensagem) na fila do soquete.

### <a name="siocatmark"></a>SIOCATMARK

Determine se todos os dados OOB foram lidos ou não. Isso se aplica somente a um soquete de estilo de fluxo (por exemplo, tipo SOCK \_ Stream) que foi configurado para a recepção embutida de qualquer dado OOB (portanto, \_ OOBINLINE). Se nenhum dado OOB estiver aguardando para ser lido, a operação retornará TRUE. Caso contrário, ele retorna **false** e a próxima operação Receive executada no soquete recuperará alguns ou todos os dados que antecedem a marca; o aplicativo deve usar a operação **SIOCATMARK** para determinar se um deles permanece. Se houver dados normais que antecedem os dados urgentes (fora de banda), eles serão recebidos na ordem. (Observe que as operações de [**recebimento**](/windows/desktop/api/winsock/nf-winsock-recv) nunca misturarão dados OOB e normais na mesma chamada.) *lpvOutBuffer* aponta para um bool no qual o [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) armazena o resultado.

## <a name="windows-sockets-2-commands"></a>Comandos do Windows Sockets 2

Há suporte para os seguintes comandos do Windows Sockets 2.

### <a name="sio_acquire_port_reservation-opcode-setting-i-t3"></a>SIO_ACQUIRE_PORT_RESERVATION (configuração de opcode: I, T = = 3)

Solicite uma reserva de tempo de execução para um bloco de portas TCP ou UDP. Para reservas de porta de tempo de execução, o pool de portas requer que as reservas sejam consumidas do processo em cujo soquete a reserva foi concedida. As reservas de porta de tempo de execução duram apenas desde o tempo de vida do soquete no qual o IOCTL de [**\_ reserva de \_ porta \_ de aquisição sio**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) foi chamado. Por outro lado, as reservas de porta persistentes criadas usando a função [**CreatePersistentTcpPortReservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) podem ser consumidas por qualquer processo com a capacidade de obter reservas persistentes.

Para obter informações mais detalhadas, consulte a referência de [**\_ reserva de \_ porta \_ sio Acquire**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) .

[**Sio \_ A \_ \_ reserva de porta de aquisição**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) tem suporte no Windows Vista e em versões posteriores do sistema operacional.

### <a name="sio_address_list_change-opcode-setting-v-t1"></a>\_Alteração da \_ lista de endereços sio \_ (configuração de opcode: V, T = = 1)

Para receber a notificação de alterações na lista de endereços de transporte locais da família de protocolos do soquete à qual o aplicativo pode se associar. Nenhuma informação de saída será fornecida após a conclusão deste IOCTL; a conclusão simplesmente indica que a lista de endereços locais disponíveis foi alterada e deve ser consultada novamente por meio da **consulta de lista de endereços do sio \_ \_ \_**.

Presume-se (embora não seja necessário) que o aplicativo usa e/s sobreposta para ser notificado da alteração pela conclusão da solicitação de **\_ alteração da \_ lista \_ de endereços sio** . Como alternativa, se o IOCTL de **alteração da \_ lista de endereços \_ \_ sio** for emitido em um soquete sem bloqueio e sem parâmetros sobrepostos (*lpOverlapped* /  *lpCompletionRoutine* forem definidos como **NULL**), ele será concluído imediatamente com o erro [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md). O aplicativo pode aguardar os eventos de alteração da lista de endereços por meio de uma chamada para [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) ou [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) com o \_ bit de \_ alteração da lista de endereços FD \_ definido no bitmask do evento de rede.

### <a name="sio_address_list_query-opcode-setting-o-t1"></a>\_ \_ \_ Consulta de lista de endereços do SiO (configuração de opcode: O, T = = 1)

Obtém uma lista de endereços de transporte locais da família de protocolos do soquete à qual o aplicativo pode ser associado. A lista de endereços varia de acordo com a família de endereços e alguns endereços são excluídos da lista.

> [!Note] 
> Em ambientes Windows plug-n-play, os endereços podem ser adicionados e removidos dinamicamente. Portanto, os aplicativos não podem contar com as informações retornadas pela **\_ consulta de \_ lista \_ de endereços sio** para serem persistentes. Os aplicativos podem se registrar para notificações de alteração de endereço por meio do IOCTL de **\_ alteração da \_ lista \_ de endereços sio** , que fornece notificação por meio do evento de alteração da lista de endereços e/s sobreposta ou FD \_ \_ \_ . A seguinte sequência de ações pode ser usada para garantir que o aplicativo sempre tenha informações da lista de endereços atual:

-  Problema **de \_ \_ \_ alteração da lista de endereços sio** do IOCTL
-  Problema **de \_ \_ \_ consulta da lista de endereços do sio** IOCTL
-  Sempre que o IOCTL de alteração da lista de endereços do sio notifica a aplicação da alteração da lista de endereços (por meio de e/s sobreposta ou sinalizando o evento de alteração da lista de **\_ \_ \_** \_ endereços FD \_ \_ ), toda a sequência de ações deve ser repetida.

Para obter informações mais detalhadas, consulte a referência de [**consulta da lista de endereços do sio \_ \_ \_**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) . **Sio \_ A \_ \_ consulta de lista de endereços** tem suporte no Windows 2000 e posterior.

### <a name="sio_apply_transport_setting-opcode-setting-i-t3"></a>SIO \_ aplicar \_ \_ configuração de transporte (configuração de opcode: I, T = = 3)

Aplica uma configuração de transporte a um soquete. A configuração de transporte sendo aplicada baseia-se [**na \_ \_ ID de configuração de transporte**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) passada no parâmetro *lpvInBuffer* .

A única configuração de transporte definida atualmente é para o recurso de **\_ capacidade de \_ notificação \_ em tempo real** em um soquete TCP.

Se a [**\_ \_ ID da configuração de transporte**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) passada tiver o membro **GUID** definido como **\_ \_ \_ recurso de notificação em tempo real**, essa será uma solicitação para aplicar configurações de notificação em tempo real para o soquete TCP usado com o [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) para receber notificações de rede em segundo plano em um aplicativo da Windows Store.

Para obter informações mais detalhadas, consulte a referência de [**\_ configuração de \_ transporte \_ sio Apply**](/previous-versions/windows/desktop/legacy/jj553481(v=vs.85)) . **Sio \_ A \_ \_ opção aplicar transporte** tem suporte no Windows 8, Windows Server 2012 e posterior.

### <a name="sio_associate_handle-opcode-setting-i-t1"></a>\_ \_ Identificador de associação de SiO (configuração de opcode: I, T = = 1)

Associe esse soquete com o identificador especificado de uma interface de assistente. O buffer de entrada contém o valor inteiro correspondente à constante de manifesto para a interface complementar (por exemplo, TH \_ NETDEV e th \_ TAPI.), seguido por um valor que é um identificador da interface complementar especificada, juntamente com quaisquer outras informações necessárias. Consulte a seção apropriada em [anexos do Winsock](winsock-annexes.md) para obter detalhes específicos de uma interface complementar específica. O tamanho total é refletido no comprimento do buffer de entrada. Nenhum buffer de saída é necessário. O código de erro [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) é indicado para provedores de serviço que não dão suporte a este IOCTL. O identificador associado por este IOCTL pode ser recuperado usando **o \_ \_ identificador de conversão sio**.

Uma interface complementar pode ser usada, por exemplo, se um provedor específico fornece (1) uma grande quantidade de controles adicionais sobre o comportamento de um soquete e (2) os controles são específicos do provedor o suficiente para que eles não mapeiem para funções existentes do Windows Socket ou aqueles que provavelmente serão definidos no futuro. É recomendável que o Component Object Model (COM) seja usado em vez desse IOCTL para descobrir e acompanhar outras interfaces que podem ter suporte por um soquete. Esse IOCTL está presente para compatibilidade (inversa) com sistemas em que o COM não está disponível ou não pode ser usado por algum outro motivo.

### <a name="sio_associate_port_reservation-opcode-setting-i-t3"></a>SIO \_ ASSOCIATE PORT RESERVATION \_ \_ (configuração de opcode: I, T==3)

Associe um soquete a uma reserva persistente ou de runtime para um bloco de portas TCP ou UDP identificadas pelo token de reserva de porta. O [**IOCTL SIO \_ ASSOCIATE \_ PORT \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) deve ser emitido antes que o soquete seja associado. Se e quando o soquete estiver vinculado, a porta atribuída a ele será selecionada na reserva de porta identificada pelo token determinado. Se nenhuma porta estiver disponível na reserva especificada, a chamada da função [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) falhará.

Para obter informações mais detalhadas, consulte a referência [**SIO \_ ASSOCIATE PORT \_ \_ RESERVATION.**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85))

[**SIO \_ HÁ \_ suporte para ASSOCIATE PORT \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) no Windows Vista e em versões posteriores do sistema operacional.

### <a name="sio_base_handle-opcode-setting-o-t1"></a>SIO \_ BASE \_ HANDLE (configuração de opcode: O, T==1)

Recupera o alça do provedor de serviços base para um determinado soquete. O valor retornado é um **SOCKET.**

Um provedor de serviços em camadas nunca interceptaria esse IOCTL, pois o valor de retorno deve ser o alça de soquete do provedor de serviços base.

Se o buffer de saída não for grande o suficiente para um identificador de soquete (o *cbOutBuffer* é menor que o tamanho de um **soquete**) ou o parâmetro *lpvOutBuffer* for um ponteiro **NULL** , o **\_ erro de soquete** será retornado como resultado desse IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [WSAEFAULT](windows-sockets-error-codes-2.md).

**Sio \_ O \_ identificador base** é definido no arquivo de cabeçalho *mswsock. h* e tem suporte no Windows Vista e posterior.

### <a name="sio_bsp_handle-opcode-setting-o-t1"></a>\_Identificador BSP sio \_ (configuração de opcode: O, T = = 1)

Recupera o identificador do provedor de serviços base para um soquete usado pela função [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) . O valor retornado é um **soquete**.

Esse IOCTL é usado por um provedor de serviços em camadas para garantir que o provedor intercepte a função [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) .

Se o buffer de saída não for grande o suficiente para um identificador de soquete (o *cbOutBuffer* é menor que o tamanho de um **soquete**) ou o parâmetro *lpvOutBuffer* for um ponteiro **NULL** , o **\_ erro de soquete** será retornado como resultado desse IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [WSAEFAULT](windows-sockets-error-codes-2.md).

**Sio \_ O \_ identificador BSP** é definido no arquivo de cabeçalho *mswsock. h* e tem suporte no Windows Vista e posterior.

### <a name="sio_bsp_handle_select-opcode-setting-o-t1"></a>SIO \_ \_ de identificador \_ de BSP (configuração de opcode: O, T = = 1)

Recupera o identificador do provedor de serviços base para um soquete usado pela função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) . O valor retornado é um **soquete**.

Esse IOCTL é usado por um provedor de serviços em camadas para garantir que o provedor intercepte a função [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) .

Se o buffer de saída não for grande o suficiente para um identificador de soquete (o *cbOutBuffer* é menor que o tamanho de um **soquete**) ou o parâmetro *lpvOutBuffer* for um ponteiro **NULL** , o **\_ erro de soquete** será retornado como resultado desse IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [WSAEFAULT](windows-sockets-error-codes-2.md).

**SIO \_ BSP \_ HANDLE \_ SELECT** é definido no arquivo de header *Mswsock.h* e tem suporte no Windows Vista e posterior.

### <a name="sio_bsp_handle_poll-opcode-setting-o-t1"></a>SIO \_ BSP \_ HANDLE POLL \_ (configuração de opcode: O, T==1)

Recupera o alça do provedor de serviços base para um soquete usado pela [**função WSAPoll.**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) O *parâmetro lpOverlapped* deve ser um **ponteiro NULL.** O valor retornado é um **SOCKET.**

Esse Ioctl é usado por um provedor de serviços em camadas para garantir que o provedor intercepte a [**função WSAPoll.**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)

Se o buffer de saída não for grande o suficiente para um alçamento de soquete (o *cbOutBuffer* for menor que o tamanho de um **SOCKET**), o parâmetro *lpvOutBuffer* será um ponteiro **NULL** ou o parâmetro *lpOverlapped* não for um ponteiro **NULL,** **SOCKET \_ ERROR** será retornado como resultado desse IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [WSAEFAULT](windows-sockets-error-codes-2.md).

**SIO \_ O BSP \_ HANDLE \_ POLL** é definido no arquivo de header *Mswsock.h* e tem suporte no Windows Vista e posterior.

### <a name="sio_chk_qos-opcode-setting-i-o-t3"></a>QOS do SIO \_ CHK \_ (configuração de opcode: I, O, T==3)

Recupera informações sobre características de tráfego de QoS. Durante a fase de transição no sistema de envio entre a configuração de fluxo e o recebimento de uma mensagem RESV (consulte Como o serviço [RSVP](/previous-versions/windows/desktop/qos/how-the-rsvp-service-invokes-tc) invoca o TC para obter mais informações sobre a fase de transição), o tráfego associado a um fluxo RSVP é formaado com base no tipo de serviço[(BEST EFFORT,](/previous-versions/windows/desktop/qos/best-effort) [CONTROLLED LOAD](/previous-versions/windows/desktop/qos/controlled-load)ou [GUARANTEED).](/previous-versions/windows/desktop/qos/guaranteed) Para obter mais informações, [consulte Usando O \_ \_ QOS do SIO CHK](/previous-versions/windows/desktop/qos/using-sio-chk-qos) na seção [Qualidade](/previous-versions/windows/desktop/qos/qos-start-page) de Serviço do SDK da Plataforma.

### <a name="sio_cpu_affinity-opcode-setting-i-t3"></a>SIO_CPU_AFFINITY (configuração de opcode: I, T==3)

Habilita o compartilhamento de porta e a paralelização de indicação de recebimento. Quando seu aplicativo usa essa opção de soquete para associar soquetes a processadores diferentes e, em seguida, associa os soquetes ao mesmo endereço, as indicações de recebimento serão distribuídas entre os soquetes com base no hash RSS (Receive Side Scaling). As configurações do RSS não mudam, portanto, qualquer fluxo determinado (ponto de extremidade local, par de ponto de extremidade remoto) sempre será indicado no mesmo processador. Como resultado, todos os pacotes que pertencem a um determinado fluxo serão indicados para o mesmo soquete. Esse IOCTL deve ser chamado antes da vinculação; caso contrário, WSAEINVAL será retornado. O buffer de entrada é um índice de processador (baseado em 0) do tipo USHORT. O IOCTL é incompatível com SO_REUSEADDR e SO_REUSE_MULTICASTPORT. Suporte apenas para soquetes UDP.

> [!NOTE]
> Se você estiver direcionando a versão 10.0.19041.0 (Windows 10, versão 2004) do SDK do Windows, use o valor em vez do nome `0x98000015` **SIO_CPU_AFFINITY**.

### <a name="sio_enable_circular_queueing-opcode-setting-v-t1"></a>SIO \_ ENABLE \_ CIRCULAR \_ QUEUEING (configuração de opcode: V, T==1)

Indica ao provedor de serviços orientado a mensagens subjacente que uma mensagem recém-chegada nunca deve ser descartado devido a um estouro de fila de buffer. Em vez disso, a mensagem mais antiga na fila deve ser eliminada para acomodar a mensagem recém-chegada. Nenhum buffer de entrada e saída é necessário. Observe que esse IOCTL só é válido para soquetes associados a protocolos não confiáveis orientados a mensagens. O [código de erro WSAENOPROTOOPT](windows-sockets-error-codes-2.md) é indicado para provedores de serviços que não são suportados por esse IOCTL.

### <a name="sio_find_route-opcode-setting-o-t1"></a>SIO \_ FIND \_ ROUTE (configuração de opcode: O, T==1)

Quando emitido, esse IOCTL solicita que a rota para o endereço remoto especificado como [**um sockaddr**](sockaddr-2.md) no buffer de entrada seja descoberta. Se o endereço já existir no cache local, sua entrada será invalidada. No caso do IPX da Novell, essa chamada inicia um GLT (GetLocalTarget) IPX, que consulta a rede para o endereço remoto determinado.

### <a name="sio_flush-opcode-setting-v-t1"></a>SIO \_ FLUSH (configuração de opcode: V, T==1)

Descarta o conteúdo atual da fila de envio associada a esse soquete. Nenhum buffer de entrada e saída é necessário. O [código de erro WSAENOPROTOOPT](windows-sockets-error-codes-2.md) é indicado para provedores de serviços que não são suportados por esse IOCTL.

### <a name="sio_get_broadcast_address-opcode-setting-o-t1"></a>SIO \_ GET BROADCAST ADDRESS \_ \_ (configuração de opcode: O, T==1)

Esse IOCTL preenche o buffer de saída com uma estrutura [sockaddr](sockaddr-2.md) que contém um endereço de difusão adequado para uso com [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) /  [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto). Esse IOCTL não tem suporte para soquetes IPv6 e retorna o código de erro [WSAENOPROTOOPT.](windows-sockets-error-codes-2.md)

### <a name="sio_get_extension_function_pointer-opcode-setting-o-i-t1"></a>SIO \_ GET EXTENSION FUNCTION POINTER \_ \_ \_ (configuração de opcode: O, I, T==1)

Recupere um ponteiro para a função de extensão especificada com suporte pelo provedor de serviços associado. O buffer de entrada contém um **GUID**(identificador global exclusivo) cujo valor identifica a função de extensão em questão. O ponteiro para a função desejada é retornado no buffer de saída. Os identificadores de função de extensão são estabelecidos por fornecedores do provedor de serviços e devem ser incluídos na documentação do fornecedor que descreve as funcionalidades e a semântica da função de extensão.

Os valores de GUID para funções de extensão com suporte pelo provedor de serviços TCP/IP do Windows são definidos no arquivo de header *Mswsock.h.* O valor possível para esses GUIDs é o seguinte:

| Termo                                                                                                                | Descrição                                                                               |
|-|-|
| <span id="WSAID_ACCEPTEX"></span><span id="wsaid_acceptex"></span>WSAID \_ ACCEPTEX<br/>                                     | A [**função de extensão AcceptEx.**](/windows/win32/api/mswsock/nf-mswsock-acceptex)<br/>                         |
| <span id="WSAID_CONNECTEX"></span><span id="wsaid_connectex"></span>WSAID \_ CONNECTEX<br/>                                  | A [**função de extensão ConnectEx.**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) <br/>                      |
| <span id="WSAID_DISCONNECTEX"></span><span id="wsaid_disconnectex"></span>WS \_ DISCONNECTEX<br/>                         | A [**função de extensão DisconnectEx.**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) <br/>                |
| <span id="WSAID_GETACCEPTEXSOCKADDRS"></span><span id="wsaid_getacceptexsockaddrs"></span>WSOCK \_ GETACCEPTEXSOCKADDRS<br/> | A [**função de extensão GetAcceptExSockaddrs.**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs)<br/> |
| <span id="WSAID_TRANSMITFILE"></span><span id="wsaid_transmitfile"></span>WSFILE \_ TRANSMITFILE<br/>                         | A [**função de extensão TransmitFile.**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)<br/>                 |
| <span id="WSAID_TRANSMITPACKETS"></span><span id="wsaid_transmitpackets"></span>\_TRANSMITPACKETS WSPACKETS<br/>                | A [**função de extensão TransmitPackets.**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) <br/>          |
| <span id="WSAID_WSARECVMSG"></span><span id="wsaid_wsarecvmsg"></span>WSAID \_ WSARECVMSG<br/>                               | A [**função LPFN_WSARECVMSG extensão (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)<br/>                     |
| <span id="WSAID_WSASENDMSG"></span><span id="wsaid_wsasendmsg"></span>WSEA \_ WSASENDMSG<br/>                               | A [**função de extensão WSASendMsg.**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) <br/>                      |

### <a name="sio_get_group_qos-opcode-setting-o-i-t1"></a>SIO \_ GET \_ GROUP \_ QOS (configuração de opcode: O, I, T==1)

Reservado para uso futuro com soquetes.

Recupere a [**estrutura QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) associada ao grupo de soquetes ao qual esse soquete pertence. O buffer de entrada é opcional. Alguns protocolos (por exemplo, RSVP) permitem que o buffer de entrada seja usado para qualificar uma qualidade de solicitação de serviço. A **estrutura QOS** será copiada para o buffer de saída. Se esse soquete não pertencer a um grupo de soquete apropriado, os membros **SendingFlowspec** e **ReceivingFlowspec** da estrutura **QOS** retornada serão definidos como **NULL.** O [código de erro WSAENOPROTOOPT](windows-sockets-error-codes-2.md) é indicado para provedores de serviços que não suportam a qualidade do serviço.

### <a name="sio_get_interface_list-opcode-setting-o-t0"></a>SIO \_ GET INTERFACE LIST \_ \_ (configuração de opcode: O, T==0)

Retorna uma lista de interfaces IP configuradas e seus parâmetros como uma matriz de estruturas [**INTERFACE \_ INFO.**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info)

> [!Note]  
> O suporte a esse comando é obrigatório para provedores de serviços TCP/IP compatíveis com Windows Sockets 2.

O *parâmetro lpvOutBuffer* aponta para o buffer no qual armazenar as informações sobre interfaces como uma matriz de estruturas [**INTERFACE \_ INFO**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) para endereços IP unicast nas interfaces. O *parâmetro cbOutBuffer* especifica o comprimento do buffer de saída. O número de interfaces retornadas (número de estruturas retornadas no buffer apontado pelo parâmetro *lpvOutBuffer)* pode ser determinado com base no comprimento real do buffer de saída retornado no parâmetro *lpcbBytesReturned.*

Se a [**função WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) for chamada com **SIO \_ GET INTERFACE \_ \_ LIST** e o membro de nível do parâmetro *do* soquete não for definido como **\_ IPPROTO,** **WSAEINVAL** será retornado. Uma chamada para a função **WSAIoctl** com **SIO \_ GET INTERFACE \_ \_ LIST** retornará **WSAEFAULT** se o parâmetro *cbOutBuffer* que especifica o comprimento do buffer de saída for muito pequeno e receber a lista de interfaces configuradas.

**SIO \_ HÁ \_ suporte para GET INTERFACE \_ LIST** no Windows Me/98 e Windows NT 4.0 com SP4 e posterior.

### <a name="sio_get_interface_list_ex-opcode-setting-o-t0"></a>SIO \_ GET INTERFACE LIST EX \_ \_ \_ (configuração de opcode: O, T==0)

Reservado para uso futuro com soquetes.

Retorna uma lista de interfaces IP configuradas e seus parâmetros como uma matriz de [**estruturas INTERFACE \_ INFO \_ EX.**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex)

O *parâmetro lpvOutBuffer* aponta para o buffer no qual armazenar as informações sobre interfaces como uma matriz de estruturas [**INTERFACE INFO \_ \_ EX**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) para endereços IP unicast na interface. O *parâmetro cbOutBuffer* especifica o comprimento do buffer de saída. O número de interfaces retornadas (número de estruturas retornadas em *lpvOutBuffer*) pode ser determinado com base no tamanho real do buffer de saída retornado no *parâmetro lpcbBytesReturned.*

**SIO \_ No \_ \_ momento, não \_** há suporte para GET INTERFACE LIST EX no Windows.

### <a name="sio_get_qos-opcode-setting-o-t1"></a>SIO \_ GET \_ QOS (configuração de opcode: O, T==1)

Reservado para uso futuro com soquetes. Recupere a [**estrutura QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) associada ao soquete. O buffer de entrada é opcional. Alguns protocolos (por exemplo, RSVP) permitem que o buffer de entrada seja usado para qualificar uma qualidade de solicitação de serviço. A **estrutura QOS** será copiada para o buffer de saída. O buffer de saída deve ser dimensionado o suficiente para poder conter a estrutura **completa do QOS.** O [código de erro WSAENOPROTOOPT](windows-sockets-error-codes-2.md) é indicado para provedores de serviços que não suportam a qualidade do serviço.

Um remetente não pode chamar **SIO \_ GET \_ QOS até** que o soquete esteja conectado.

Um receptor pode chamar **SIO \_ GET \_ QOS** assim que ele é vinculado.

### <a name="sio_get_tx_timestamp"></a>SIO_GET_TX_TIMESTAMP

Um IOCTL de soquete usado para obter os timestamps para pacotes transmitidos (TX). Válido somente para soquetes de datagrama.

O **SIO_GET_TX_TIMESTAMP** de controle remove um timestamp de transmissão da fila de data/hora de transmissão de um soquete. Habilita a recepção de timestamp primeiro usando [**o IOCTL SIO_TIMESTAMPING**](#sio_timestamping) soquete. Em seguida, recupere os timestamps tx por ID chamando a função [**WSAIoctl**](/windows/win32/api/winsock2/nf-winsock2-wsaioctl) (ou [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))) com os parâmetros a seguir.

Por **SIO_GET_TX_TIMESTAMP**, a entrada é uma ID de data/hora **UINT32** e a saída é um valor de data/hora **UINT64.** Em caso de êxito, o timestamp tx está disponível e é retornado. Se nenhum timestamp de transmissão estiver disponível, [**WSAGetLastError**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) retornará **WSAEBLOCKBLOCK**.

> [!NOTE]
> Não há suporte para osstamps de data/hora TX ao fazer um envio coalesced via **UDP_SEND_MSG_SIZE**.

Consulte também [Winsock timestamping](/windows/win32/winsock/winsock-timestamping).

### <a name="sio_ideal_send_backlog_change-opcode-setting-v-t0"></a>SIO \_ IDEAL \_ SEND \_ BACKLOG CHANGE \_ (configuração de opcode: V, T==0)

Notifica um aplicativo quando o valor ideal de ISB (backlog de envio) muda para a conexão subjacente.

Ao enviar dados por uma conexão TCP usando soquetes do Windows, é importante manter uma quantidade suficiente de dados pendentes (enviados, mas ainda não confirmados) em TCP para obter a taxa de transferência mais alta. O valor ideal para a quantidade de dados pendentes para obter a melhor produtividade para a conexão TCP é chamado de tamanho ideal de ISB (backlog de envio). O valor isb é uma função do produto de atraso de largura de banda da conexão TCP e da janela de recebimento anunciada do receptor (e, em parte, a quantidade de congestionamento na rede).

O valor isb por conexão está disponível na implementação do protocolo TCP no Windows Server 2008, windows Vista com SP1 e versões posteriores do sistema operacional. O IOCTL DE ALTERAÇÃO DA **\_ \_ \_ LISTA \_** DE PENDÊNCIAS IDEAL DO SIO pode ser usado por um aplicativo para receber notificação quando o valor isb é alterado dinamicamente para uma conexão.

Para obter informações mais detalhadas, consulte a referência [**SIO \_ IDEAL SEND \_ \_ BACKLOG \_ CHANGE.**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85))

[**SIO \_ HÁ suporte para a ALTERAÇÃO DE \_ \_ BACKLOG \_ DE**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85)) ENVIO IDEAL no Windows Server 2008, no Windows Vista com SP1 e em versões posteriores do sistema operacional.

### <a name="sio_ideal_send_backlog_query-opcode-setting-o-t0"></a>CONSULTA SIO \_ IDEAL \_ SEND \_ BACKLOG \_ (configuração de opcode: O, T==0)

Recupera o valor ideal de ISB (backlog de envio) para a conexão subjacente.

Ao enviar dados por uma conexão TCP usando soquetes do Windows, é importante manter uma quantidade suficiente de dados pendentes (enviados, mas ainda não confirmados) em TCP para obter a taxa de transferência mais alta. O valor ideal para a quantidade de dados pendentes para obter a melhor produtividade para a conexão TCP é chamado de tamanho ideal de ISB (backlog de envio). O valor isb é uma função do produto de atraso de largura de banda da conexão TCP e da janela de recebimento anunciada do receptor (e, em parte, a quantidade de congestionamento na rede).

O valor isb por conexão está disponível na implementação do protocolo TCP no Windows Server 2008 e posterior. O IOCTL DE CONSULTA **\_ DE \_ \_ BACKLOG \_** DO SIO IDEAL SEND pode ser usado por um aplicativo para consultar o valor isb de uma conexão.

Para obter informações mais detalhadas, consulte a referência de [**\_ CONSULTA DE \_ \_ BACKLOG \_ SEND DO SIO IDEAL.**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85))

[**Sio \_ A \_ \_ \_ consulta do registro posterior de envio ideal**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85)) tem suporte no Windows Server 2008, no Windows Vista com SP1 e em versões posteriores do sistema operacional.

### <a name="sio_keepalive_vals-opcode-setting-i-t3"></a>SIO \_ KeepAlive \_ Vals (configuração de opcode: I, T = = 3)

Habilita ou desabilita a configuração por conexão da opção TCP **Keep-Alive** que especifica o tempo limite e o intervalo de Keep-Alive TCP. Para obter mais informações sobre a opção keep-alive, consulte a seção 4.2.3.6 sobre os *requisitos para hosts da Internet — camadas de comunicação* especificadas no RFC 1122 disponíveis no [site da IETF](https://www.ietf.org/rfc/rfc1122.txt). (Este recurso só pode estar disponível em inglês.)

**Sio \_ KEEPALIVE \_ Vals** pode ser usado para habilitar ou desabilitar investigações Keep-Alive e definir o tempo limite e o intervalo de Keep-Alive. O tempo limite de Keep-Alive especifica o tempo limite, em milissegundos, sem atividade até que o primeiro pacote keep-alive seja enviado. O intervalo Keep-Alive especifica o intervalo, em milissegundos, entre quando os pacotes Keep Alive sucessivos são enviados, caso nenhuma confirmação seja recebida.

A opção de [**\_ KeepAlive**](so-keepalive.md) , que é uma das [Opções de \_ soquete de soquete de sol](sol-socket-socket-options.md), também pode ser usada para habilitar ou desabilitar o TCP Keep-Alive em uma conexão, bem como consultar o estado atual dessa opção. Para consultar se o TCP Keep-Alive está habilitado em um soquete, a função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) pode ser chamada com a opção de **\_ KeepAlive** . Para habilitar ou desabilitar o TCP Keep-Alive, a função [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pode ser chamada com a opção de [**\_ KeepAlive**](so-keepalive.md) . Se o TCP Keep-Alive estiver habilitado com o **\_ KeepAlive**, as configurações de TCP padrão serão usadas para tempo limite e intervalo de Keep-Alive, a menos que esses valores tenham sido alterados usando **sio \_ KeepAlive \_ Vals**.

Para obter informações mais detalhadas, consulte a referência do [**sio \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) . **Sio \_ O KEEPALIVE \_ Vals** tem suporte no Windows 2000 e posterior.

### <a name="sio_loopback_fast_path-opcode-setting-i-t3"></a>SIO \_ LOOPBACK \_ FAST PATH \_ (configuração de opcode: I, T==3)

Configura um soquete TCP para operações de menor latência e mais rápidas na interface de loopback. Esse IOCTL solicita que a pilha TCP/IP use um caminho rápido especial para operações de loopback nesse soquete. O IOCTL de CAMINHO RÁPIDO DO [**\_ \_ \_ LOOPBACK SIO**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) só pode ser usado com soquetes TCP. Esse IOCTL deve ser usado em ambos os lados da sessão de loopback. Há suporte para o caminho rápido de loopback TCP usando a interface de loopback IPv4 ou IPv6. Por padrão, **o SIO \_ LOOPBACK \_ FAST \_ PATH** está desabilitado.

Para obter informações mais detalhadas, consulte a referência [**SIO \_ LOOPBACK \_ FAST \_ PATH.**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) **SIO \_ HÁ suporte \_ para \_ LOOPBACK FAST PATH** Windows 8, Windows Server 2012 e posterior.

### <a name="sio_multipoint_loopback-opcode-setting-v-t1"></a>LOOPBACK \_ DO SIO MULTIPOINT \_ (configuração de opcode: V, T==1)

Controla se os dados enviados por um aplicativo no computador local (não necessariamente pelo mesmo soquete) em uma sessão multicast serão recebidos por um soquete ingressado no grupo de destino multicast na interface de loopback. Um valor true **faz com** que os dados multicast enviados por um aplicativo no computador local sejam entregues a um soquete de escuta na interface de loopback. Um valor false **impede** que os dados multicast enviados por um aplicativo no computador local seja entregue a um soquete de escuta na interface de loopback. Por padrão, **o SIO \_ MULTIPOINT \_ LOOPBACK** está habilitado.

### <a name="sio_multicast_scope-opcode-setting-i-t1"></a>ESCOPO DO MULTICAST SIO \_ \_ (configuração de opcode: I, T==1)

Especifica o escopo sobre o qual as transmissões multicast ocorrerão. O escopo é definido como o número de segmentos de rede roteados a serem cobertos. Um escopo de zero indicaria que a transmissão multicast não seria colocada na transmissão, mas poderia ser disseminada entre soquetes dentro do host local. Um valor de escopo de um (o padrão) indica que a transmissão será colocada na transmissão, mas não cruzará nenhum roteador. Valores de escopo mais altos determinam o número de roteadores que podem ser cruzados. Observe que isso corresponde ao parâmetro time-to-Live (TTL) no multicast de IP. Por padrão, o escopo é 1.

### <a name="sio_query_rss_processor_info-opcode-setting-o-t1"></a>SIO \_ consultar \_ \_ \_ informações do processador RSS (configuração de opcode: O, T = = 1)

Consulta a associação entre um soquete e um núcleo de processador RSS e um nó NUMA.

As [**\_ informações do \_ \_ processador \_ RSS da consulta sio**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) IOCTL retorna uma estrutura de [**\_ \_ afinidade de processador de soquete**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) que contém o [**\_ número do processador**](/windows/win32/api/winnt/ns-winnt-processor_number) e a ID do nó numa. A estrutura **de \_ número de processador** retornada contém um número de grupo e um número de processador relativo no grupo.

Para obter informações mais detalhadas, consulte a referência de [**\_ \_ \_ \_ informações do processador RSS de consulta sio**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) . **Sio \_ As \_ \_ \_ informações do processador RSS de consulta** têm suporte no Windows 8, Windows Server 2012 e posterior.

### <a name="sio_query_rss_scalability_info-opcode-setting-o-t3"></a>\_ \_ \_ Informações de escalabilidade de RSS da consulta sio \_ (configuração de opcode: O, T = = 3)

As consultas descarregam interfaces para o recurso de dimensionamento no lado do recebimento (RSS). A estrutura de argumentos retornada para as **\_ \_ \_ \_ informações de escalabilidade de RSS de consulta sio** é especificada na estrutura de **\_ \_ informações de escalabilidade de RSS** definida no arquivo de cabeçalho *Mstcpip. h* . Essa estrutura é definida da seguinte maneira:

```cpp
// Scalability info for the transport
typedef struct _RSS_SCALABILITY_INFO {
   BOOLEAN RssEnabled;
} RSS_SCALABILITY_INFO, *PRSS_SCALABILITY_INFO;
```

O valor retornado no membro **RssEnabled** indica se o RSS está habilitado em pelo menos uma interface.

Se o buffer de saída não for grande o suficiente para a estrutura de **\_ \_ informações de escalabilidade RSS** (o *cbOutBuffer* é menor que o tamanho de uma **\_ \_ informação de escalabilidade de RSS**) ou o parâmetro *lpvOutBuffer* é um ponteiro **nulo** , o **\_ erro de soquete** é retornado como resultado desse IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retorna [WSAEINVAL](windows-sockets-error-codes-2.md).

Em uma rede de alta velocidade em que várias CPUs residem em um único sistema, a capacidade da pilha de protocolos de rede de dimensionar bem em um sistema de várias CPU é inibida porque a arquitetura do NDIS 5.1 e versões anteriores limita o processamento de protocolo para uma única CPU. O RSS (dimensionamento do lado do recebimento) resolve esse problema permitindo que a carga de rede de um adaptador de rede seja balanceada em várias CPUs.

**SIO \_ AS INFORMAÇÕES \_ DE ESCALABILIDADE do RSS \_ \_ DE CONSULTA** são suportadas no Windows Vista e posterior.

### <a name="sio_query_transport_setting-opcode-setting-i-t3"></a>CONFIGURAÇÃO DE TRANSPORTE DE CONSULTA DO SIO \_ \_ \_ (configuração de opcode: I, T==3)

Consulta as configurações de transporte em um soquete. A configuração de transporte que está sendo consultada baseia-se na [**\_ \_ ID TRANSPORT SETTING**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) passada no *parâmetro lpvInBuffer.*

A única configuração de transporte atualmente definida é para a funcionalidade **\_ DE \_ NOTIFICAÇÃO \_ EM** TEMPO REAL em um soquete TCP.

Se a [**\_ \_ ID**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) DE CONFIGURAÇÃO DE TRANSPORTE tiver o membro **Guid** definido como CAPACIDADE DE NOTIFICAÇÃO EM TEMPO **REAL, \_ \_ \_** essa será uma solicitação para consultar as configurações de notificação em tempo real para o soquete TCP usado com [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) para receber notificações de rede em segundo plano em um aplicativo da Windows Store. Se a [**chamada WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) ou [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) for bem-sucedida, esse IOCTL retornará uma estrutura DE SAÍDA DE CONFIGURAÇÃO DE NOTIFICAÇÃO EM TEMPO REAL com o status atual. [**\_ \_ \_ \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-real_time_notification_setting_input)

Para obter informações mais detalhadas, consulte a referência DE CONFIGURAÇÃO DE TRANSPORTE DE [**\_ CONSULTA \_ \_ SIO.**](/previous-versions/windows/desktop/legacy/jj553483(v=vs.85)) **SIO \_ A CONFIGURAÇÃO \_ \_ DE TRANSPORTE DE** CONSULTA tem suporte Windows 8, Windows Server 2012 e posterior.

### <a name="sio_query_wfp_ale_endpoint_handle-opcode-setting-o-t3"></a>SIO \_ QUERY \_ WFP \_ ALE \_ ENDPOINT \_ HANDLE (configuração de opcode: O, T==3)

Consulta o alça do ponto de extremidade ALE (Imposição de Camada de Aplicativo).

A WFP (Plataforma de Filtragem do Windows) dá suporte à inspeção e modificação de tráfego de rede. No Windows Vista, a WFP se concentra em cenários em que a máquina host é o ponto de extremidade de comunicação. No Windows Server 2008, no entanto, há implementações de firewall do Edge que gostariam de aproveitar a plataforma WFP para inspecionar e fazer proxy do tráfego de passagem. O ISA (Internet Security and Acceleration) Server é um exemplo desse tipo de dispositivo de borda.

Há alguns cenários de firewall que podem exigir a capacidade de injetar um pacote de entrada no caminho de envio associado a um ponto de extremidade existente. Deve haver um mecanismo para descobrir o identificador de ponto de extremidade da camada de transporte associado ao ponto de extremidade de destino. O aplicativo que criou o ponto de extremidade possui esses pontos de extremidades da camada de transporte. Esse IOCTL é usado para fornecer um identificador de soquete ao mapeamento de identificador de ponto de extremidade de camada de transporte.

Se o buffer de saída não for grande o suficiente para o identificador do ponto de extremidade (o *cbOutBuffer* é menor que o tamanho de um **UINT64**) ou o parâmetro *lpvOutBuffer* for um ponteiro **NULL** , o **\_ erro de soquete** será retornado como resultado desse IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [WSAEINVAL](windows-sockets-error-codes-2.md).

**Sio \_ A consulta do \_ \_ identificador de ponto de \_ extremidade \_ Ale WFP** tem suporte no Windows Vista e posterior.

### <a name="sio_query_wfp_connection_redirect_context-opcode-setting-i-t3"></a>SIO \_ consultar \_ \_ \_ contexto de redirecionamento de conexão WFP \_ (configuração de opcode: I, T = = 3)

Consulta o contexto de redirecionamento para um registro de redirecionamento usado por um serviço de redirecionamento WFP (Windows Filtering Platform).

O [**\_ contexto de \_ \_ \_ redirecionamento \_ de conexão WFP de consulta sio**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) é usado para fornecer rastreamento de conexão com proxy em conexões de soquete redirecionadas. Esse recurso de WFP facilita o rastreamento de registros de redirecionamento do redirecionamento inicial de uma conexão com a conexão final com o destino.

Para obter informações mais detalhadas, consulte a referência de [**\_ \_ \_ \_ \_ contexto de redirecionamento de conexão WFP de consulta sio**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) . **SIO \_ HÁ suporte \_ para \_ \_ \_** O CONTEXTO DE REDIRECIONAMENTO DE CONEXÃO DO WFP Windows 8, Windows Server 2012 e posterior.

### <a name="sio_query_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ QUERY \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS (configuração de opcode: I, T==3)

Consulta o registro de redirecionamento para a conexão TCP/IP aceita para uso por um serviço de redirecionamento do WFP (Windows Filtering Platform).

O IOCTL DE REGISTROS DE REDIRECIONAMENTO DE CONEXÃO [**\_ \_ WFP \_ \_ \_**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) DE CONSULTA SIO é usado para fornecer o acompanhamento de conexão proxied em conexões de soquete redirecionadas. Esse recurso WFP facilita o acompanhamento de registros de redirecionamento do redirecionamento inicial de uma conexão com a conexão final com o destino.

Para obter informações mais detalhadas, consulte a referência DE REGISTROS DE REDIRECIONAMENTO DE [**\_ CONEXÃO \_ WFP \_ \_ \_ DA CONSULTA SIO.**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) **SIO \_ O QUERY \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS** tem suporte Windows 8, Windows Server 2012 e posterior.

### <a name="sio_rcvall-opcode-setting-i-t3"></a>SIO \_ RCCODE (configuração de opcode: I, T==3)

Permite que um soquete receba todos os pacotes IPv4 ou IPv6 passando por um adaptador de rede. O alça de soquete passado [**para a função WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) deve ser um dos seguintes:

-   Um soquete IPv4 criado com a família de endereços definida como AF INET, o tipo de soquete definido como SOCK RAW e o protocolo definido \_ \_ como IP IPPROTO. \_
-   Um soquete IPv6 criado com a família de endereços definida como AF INET6, o tipo de soquete definido como SOCK RAW e o protocolo definido como \_ \_ IPPROTO \_ IPV6.

O soquete também deve ser vinculado a uma interface IPv4 ou IPv6 local explícita, o que significa que você não pode se vincular a **INADDR \_ ANY** ou **in6addr \_ a qualquer**.

No Windows Server 2008 e anteriores, a configuração de IOCTL [**do SIO \_ RCTLE**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) não capturaria pacotes locais enviados de um interface de rede. Isso incluiu pacotes recebidos em outra interface e encaminhou o interface de rede especificado para o **IOCTL do SIO \_ RCTLE.**

No Windows 7 e no Windows Server 2008 R2, isso foi alterado para que os pacotes locais enviados de uma interface de rede também sejam capturados. Isso inclui os pacotes recebidos em outra interface e, em seguida, encaminhado o adaptador de rede associado ao soquete com [**sio \_ RCVALL**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) IOCTL.

Definir esse IOCTL requer privilégio de administrador no computador local.

Esse recurso é, às vezes, chamado de modo promíscuo.

Os valores possíveis para a opção **sio \_ RCVALL** IOCTL são especificados na enumeração **de \_ valor RCVALL** definida no arquivo de cabeçalho *Mstcpip. h* . Os valores possíveis para SIO \_ RCVALL são os seguintes:

| Termo                                                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-|-|
| <span id="RCVALL_OFF"></span><span id="rcvall_off"></span>RCVALL \_ desativado<br/>                                     | Desabilite essa opção para que um soquete não receba todos os pacotes IPv4 ou IPv6 na rede. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RCVALL_ON"></span><span id="rcvall_on"></span>RCVALL \_ em<br/>                                        | Habilite essa opção para que um soquete receba todos os pacotes IPv4 ou IPv6 na rede. Essa opção habilita o modo promíscuo na NIC (placa de interface de rede), se a NIC der suporte ao modo promíscuo. Em um segmento de LAN com um hub de rede, uma NIC que dá suporte ao modo promíscuo capturará todo o tráfego IPv4 ou IPv6 na LAN, incluindo o tráfego entre outros computadores no mesmo segmento de LAN. Todos os pacotes capturados (IPv4 ou IPv6, dependendo do soquete) serão entregues ao soquete bruto. <br/> Essa opção não capturará outros pacotes (ARP, IPX e pacotes NetBEUI, por exemplo) na interface.<br/> O Netmon usa o mesmo modo para a interface de rede, mas não usa essa opção para capturar o tráfego.<br/> |
| <span id="RCVALL_SOCKETLEVELONLY"></span><span id="rcvall_socketlevelonly"></span>RCVALL \_ SOCKETLEVELONLY<br/> | Este recurso não está implementado no momento; portanto, definir essa opção não tem nenhum efeito.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="RCVALL_IPLEVEL"></span><span id="rcvall_iplevel"></span>RCVALL \_ IPLEVEL<br/>                         | Habilite essa opção para que um soquete IPv4 ou IPv6 receba todos os pacotes no nível de IP na rede. Essa opção não habilita o modo promíscuo na placa de interface de rede. Essa opção afeta apenas o processamento de pacotes no nível de IP. A NIC ainda recebe apenas pacotes direcionados para seus endereços unicast e multicast configurados. No entanto, um soquete com essa opção habilitada receberá não apenas pacotes direcionados a endereços IP específicos, mas receberá todos os pacotes IPv4 ou IPv6 recebidos pela NIC.<br/> Essa opção não capturará outros pacotes (pacotes ARP, IPX e NetBEUI, por exemplo) recebidos na interface .<br/>                                                                                             |



 

Para obter informações mais detalhadas, consulte a [**referência do SIO \_ RC LTD.**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85))

**SIO \_ Há suporte** para RC LTDA no Windows 2000 e posterior.

### <a name="sio_rcvall_igmpmcast-opcode-setting-i-t3"></a>SIO \_ RCCODE \_ IGMPMCAST (configuração de opcode: I, T==3)

Permite que um soquete receba todo o tráfego IP multicast IGMP na rede, sem receber outro tráfego IP multicast. O identificador de soquete passado para a [**função WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) deve ser da família de endereços INET af, do tipo de soquete SOCK RAW e do \_ protocolo \_ \_ IGMP IPPROTO. O soquete também deve ser vinculado a uma interface local explícita, o que significa que você não pode se vincular a INADDR \_ ANY.

Depois que o soquete é vinculado e o conjunto IOCTL, as chamadas para as funções [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) ou [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) retornam datagramas IP multicast passando pela interface determinada. Observe que você deve fornecer um buffer suficientemente grande. Definir esse IOCTL requer o privilégio de Administrador no computador local.

**SIO \_ Há suporte para RC CHROME \_ IGMPMCAST** no Windows 2000 e posterior.

### <a name="sio_rcvall_mcast-opcode-setting-i-t3"></a>SIO \_ RCCODE \_ MCAST (configuração de opcode: I, T==3)

Permite que um soquete receba todo o tráfego IP multicast na rede (ou seja, todos os pacotes IP destinados a endereços IP no intervalo de 224.0.0.0 a 239.255.255.255). O identificador de soquete passado para a [**função WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) deve ser da família de endereços INET af, do tipo de soquete SOCK RAW e do \_ protocolo \_ UDP IPPROTO. \_ O soquete também deve se vincular a uma interface local explícita, o que significa que você não pode se vincular a INADDR \_ ANY. O soquete deve se vincular à porta zero.

Depois que o soquete é associado e o IOCTL definido, as chamadas para as funções [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) ou [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) retornam datagrams de IP de multicast que passam pela interface fornecida. Observe que você deve fornecer um buffer suficientemente grande. Definir esse IOCTL requer privilégio de administrador no computador local.

**Sio \_ O RCVALL \_ mcast** tem suporte no Windows 2000 e posterior.

### <a name="sio_release_port_reservation-opcode-setting-i-t3"></a>\_ \_ \_ Reserva de porta de liberação SiO (configuração de opcode: I, T = = 3)

Libera uma reserva de tempo de execução para um bloco de portas TCP ou UDP. A reserva de tempo de execução a ser lançada deve ter sido obtida do processo emissora usando o IOCTL de [**\_ reserva de \_ porta \_ de aquisição sio**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) .

Para obter informações mais detalhadas, consulte a referência de [**reserva de porta de liberação do sio \_ \_ \_**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) .

[**Sio \_ A \_ \_ reserva de porta de liberação**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) tem suporte no Windows Vista e em versões posteriores do sistema operacional.

### <a name="sio_routing_interface_change-opcode-setting-i-t1"></a>\_Alteração da \_ interface de roteamento sio \_ (configuração de opcode: I, T = = 1)

Para receber a notificação de uma alteração de interface de roteamento que deve ser usada para alcançar o endereço remoto no buffer de entrada (especificado como uma estrutura [**SOCKADDR**](sockaddr-2.md) ). Nenhuma informação de saída na nova interface de roteamento será fornecida após a conclusão deste IOCTL; a conclusão indica apenas que a interface de roteamento de um determinado destino foi alterada e deve ser consultada usando o IOCTL de **\_ consulta de \_ interface \_ de roteamento sio** .

Presume-se, embora não seja necessário, que o aplicativo use a e/s sobreposta para ser notificado da alteração da interface de roteamento por meio da conclusão da solicitação de **\_ alteração da \_ interface \_ de roteamento sio** . Como alternativa, se o IOCTL de ALTERAÇÃO da **\_ \_ INTERFACE \_** DE ROTEAMENTO do SIO for emitido em um soquete sem bloqueio com os parâmetros *lpOverlapped* e *lpCompletionRoutine* definidos como **NULL**), ele será concluído imediatamente retornando e [WSAEBLOCKBLOCK](windows-sockets-error-codes-2.md) como um erro e o aplicativo poderá aguardar o roteamento de eventos de alteração por meio da chamada para [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) ou [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) com o bit CHANGE da INTERFACE de ROTEAMENTO FD definido no \_ \_ bitmask de evento de \_ rede.

É reconhecido que as informações de roteamento permanecem estáveis na maioria dos casos, de modo que exigir que o aplicativo mantenha várias IOCTLs pendentes para obter notificações sobre todos os destinos nos quais está interessado, bem como fazer com que o provedor de serviços acompanhe essas solicitações de notificação usará uma quantidade significativa de recursos do sistema. Essa situação pode ser evitada estendendo o significado dos parâmetros de entrada e flexibilizar os requisitos do provedor de serviços da seguinte forma:

-   O aplicativo pode especificar um endereço curinga específico [](/windows/desktop/api/winsock/nf-winsock-bind) da família de protocolos (o mesmo usado na chamada de ligação ao solicitar a vinculação a qualquer endereço disponível) para solicitar notificações de quaisquer alterações de roteamento. Isso permite que o aplicativo mantenha apenas uma ALTERAÇÃO de **\_ \_ INTERFACE \_** DE ROTEAMENTO de SIO pendente para todos os soquetes e destinos que ele tem e, em seguida, use a CONSULTA **DE \_ \_ INTERFACE \_** de ROTEAMENTO SIO para obter as informações reais de roteamento.
-   Um provedor de serviços tem a opção de ignorar as informações especificadas pelo aplicativo no buffer de entrada da ALTERAÇÃO da INTERFACE DE ROTEAMENTO **SIO \_ \_ \_** (como se o aplicativo especificasse um endereço curinga) e concluir o evento CHANGE IOCTL ou signal FD ROUTING INTERFACE CHANGE no caso de qualquer alteração de informações de roteamento (não apenas a rota para o destino especificado no buffer de **\_ \_ \_** \_ \_ \_ entrada).

### <a name="sio_routing_interface_query-opcode-setting-i-o-t1"></a>\_Consulta da \_ interface de roteamento sio \_ (configuração de opcode: i, O, T = = 1)

Para obter o endereço da interface local (representada como estrutura [**SOCKADDR**](sockaddr-2.md) ) que deve ser usada para enviar para o endereço remoto especificado no buffer de entrada (como **SOCKADDR**). Os endereços de multicast remotos podem ser enviados no buffer de entrada para obter o endereço da interface preferencial para transmissão multicast. Em qualquer caso, o endereço de interface retornado pode ser usado pelo aplicativo em uma solicitação de BIND () subsequente.

Observe que as rotas estão sujeitas a alterações. Portanto, os aplicativos não podem contar com as informações retornadas pela **\_ consulta de \_ interface \_ de roteamento sio** para serem persistentes. Os aplicativos podem se registrar para rotear notificações de alteração por meio do IOCTL de **\_ alteração da \_ interface \_ de roteamento sio** , que fornece notificação por meio de e/s sobreposta ou um \_ evento de alteração da interface de roteamento FD \_ \_ . A seguinte sequência de ações pode ser usada para garantir que o aplicativo sempre tenha informações de interface de roteamento atuais para um determinado destino:

-   Emitir IOCTL de **\_ alteração da \_ interface \_ de roteamento sio**
-   Emitir **sio \_ de \_ \_ consulta de interface de roteamento** do IOCTL
-   Sempre que o IOCTL de **\_ alteração da \_ interface \_ de roteamento sio** notifica a aplicação da alteração de roteamento (por meio de e/s sobreposta ou sinalizando o \_ evento de \_ alteração da interface de roteamento FD \_ ), toda a sequência de ações deve ser repetida.

Se o buffer de saída não for grande o suficiente para conter o endereço de interface, o \_ erro de soquete será retornado como resultado desse IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [WSAEFAULT](windows-sockets-error-codes-2.md). O tamanho necessário do buffer de saída será retornado em *lpcbBytesReturned* nesse caso. Observe que o código de erro WSAEFAULT também será retornado se o parâmetro *lpvInBuffer*, *lpvOutBuffer* ou *lpcbBytesReturned* não estiver totalmente contido em uma parte válida do espaço de endereço de usuário.

Se o endereço de destino especificado no buffer de entrada não puder ser alcançado por meio de qualquer uma das interfaces disponíveis, SOCKET ERROR será retornado como resultado desse \_ IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [WSAENETUNREACH](windows-sockets-error-codes-2.md) ou até [mesmo WSAENETDOWN](windows-sockets-error-codes-2.md) se toda a conectividade de rede for perdida.

### <a name="sio_set_compatibility_mode-opcode-setting-i-t3"></a>SIO \_ SET \_ \_ COMPATIBILITY MODE (configuração de opcode: I, T==3)

Solicita como a pilha de rede deve lidar com determinados comportamentos para os quais a maneira padrão de lidar com o comportamento pode ser diferente entre as versões do Windows. A estrutura de argumentos para O MODO DE COMPATIBILIDADE DO SET SIO é especificada na estrutura MODO DE COMPATIBILIDADE do **WSA \_ \_** definida no arquivo de título *Mswsockdef.h.* **\_ \_ \_** Essa estrutura é definida da seguinte forma:

```cpp
/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

O valor especificado no membro **BehaviorId** indica o comportamento solicitado. O valor especificado no membro **TargetOsVersion** indica a versão do Windows que está sendo solicitada para o comportamento.

O **membro BehaviorId** pode ser um dos valores do tipo de enumeração **\_ \_ \_ ID** DE COMPORTAMENTO DE COMPATIBILIDADE do WSA definido no arquivo de título *Mswsockdef.h.* Os valores possíveis para **o membro BehaviorId** são os valores a seguir.

| Termo                                                                                                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-|-|
| <span id="WsaBehaviorAll"></span><span id="wsabehaviorall"></span><span id="WSABEHAVIORALL"></span>WsaBehaviorAll<br/>                                                     | Isso é equivalente a solicitar todos os possíveis comportamentos compatíveis definidos para a ID DE COMPORTAMENTO DE **\_ \_ \_ COMPATIBILIDADE do WSA**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="WsaBehaviorReceiveBuffering"></span><span id="wsabehaviorreceivebuffering"></span><span id="WSABEHAVIORRECEIVEBUFFERING"></span>WsaBehaviorReceiveBuffering<br/> | Quando o membro **TargetOsVersion** é definido como um valor para o Windows Vista ou posterior, as reduções para o tamanho do buffer de recebimento TCP nesse soquete usando a opção **\_ soquete SO RCVBUF** são permitidas mesmo depois que uma conexão TCP é estabelecida. <br/> Quando o membro **TargetOsVersion** é definido como um valor anterior ao Windows Vista, as reduções para o tamanho do buffer de recebimento TCP nesse soquete usando a opção **\_ soquete SO RCVBUF** não são permitidas após o estabelecimento da conexão. <br/>                                                                                                                                                                                  |
| <span id="WsaBehaviorAutoTuning"></span><span id="wsabehaviorautotuning"></span><span id="WSABEHAVIORAUTOTUNING"></span>WsaBehaviorAutoTuning<br/>                         | Quando o membro **TargetOsVersion** é definido como um valor para o Windows Vista ou posterior, o ajuste automático da janela de recebimento é habilitado e o fator de escala da janela TCP é reduzido para 2 a partir do valor padrão de 8.<br/> Quando **TargetOsVersion** é definido como um valor anterior ao Windows Vista, o ajuste automático da janela de recebimento está desabilitado. A opção de dimensionamento da janela TCP também está desabilitada e o tamanho máximo da janela de recepção é limitado a 65.535 bytes. A opção de dimensionamento da janela TCP não pode ser negociada na conexão mesmo que a opção de soquete **\_ RCVBUF** seja chamada nesse soquete especificando um valor maior que 65.535 bytes antes da conexão ser estabelecida.<br/> |



 

Para obter informações mais detalhadas, consulte a referência do [**\_ modo de \_ compatibilidade \_ sio Set**](/previous-versions/windows/desktop/legacy/cc136103(v=vs.85)) .

**Sio \_ O \_ \_ modo de compatibilidade definido** tem suporte no Windows Vista e posterior.

### <a name="sio_set_group_qos-opcode-setting-i-t1"></a>SIO \_ definir \_ \_ QoS do grupo (configuração de opcode: I, T = = 1)

Reservado.

### <a name="sio_set_priority_hint-opcode-setting-i-t3"></a>SIO_SET_PRIORITY_HINT (configuração de opcode: I, T = = 3)

Fornece uma dica para o protocolo de transporte subjacente para tratar o tráfego nesse soquete com uma prioridade específica. O *lpvInBuffer* deve apontar para uma variável do tipo **PRIORITY_HINT** com *cbInBuffer* definido como sizeof (PRIORITY_HINT). Os parâmetros *lpvOutBuffer* e *CbOutBuffer* devem ser **NULL** e 0, respectivamente. A implementação do Microsoft Windows TCP dá suporte a este IOCTL a partir do Windows 10, versão 1809 (10,0; Build 17763) e posterior da seguinte maneira: quando o valor de prioridade solicitado é definido como **IoPriorityHintVeryLow**, o TCP usa uma versão modificada do algoritmo LEDBAT (definido na RFC 6817) para controlar a taxa de tráfego de saída no soquete. O tráfego de entrada não é afetado por este IOCTL. LEDBAT é um algoritmo de recuperação, e seu objetivo é manter a latência baixa e evitar qualquer efeito adverso no tráfego de prioridade normal ao sair do caminho quando o tráfego de prioridade normal estiver presente.

Consulte também [RFC 6817](https://tools.ietf.org/html/rfc6817).

**SIO_SET_PRIORITY_HINT** há suporte no Windows 10, versão 1809 (10.0; Build 17763) e posterior.

### <a name="sio_set_qos-opcode-setting-i-t1"></a>SIO \_ SET \_ QOS (configuração de opcode: I, T==1)

Associe a [**estrutura QOS**](/windows/win32/api/winsock2/ns-winsock2-qos) especificada ao soquete. Nenhum buffer de saída é necessário, a **estrutura QOS** será obtida do buffer de entrada. O [código de erro WSAENOPROTOOPT](windows-sockets-error-codes-2.md) é indicado para provedores de serviços que não suportam a qualidade do serviço.

### <a name="sio_tcp_initial_rto-opcode-setting-i-t3"></a>SIO_TCP_INITIAL_RTO (configuração de opcode: I, T==3)

Controla as características de retransmissão iniciais (SYN/SYN+ACK) de um soquete TCP configurando parâmetros de RTO (tempo de retransmissão inicial). Os parâmetros de configuração são especificados em uma [**estrutura TCP \_ INITIAL \_ RTO \_ PARAMETERS.**](/windows/desktop/api/mswsock/ns-mswsock-transmit_file_buffers)

Para obter informações mais detalhadas, consulte a [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) referência. [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) há suporte no Windows 8, no Windows Server 2012 e posterior.

### <a name="sio_timestamping"></a>SIO_TIMESTAMPING

Um IOCTL de soquete usado para configurar a recepção de data/hora de transmissão/recebimento de soquete. Válido somente para soquetes de datagrama. O tipo de entrada **para SIO_TIMESTAMPING** é a [**estrutura TIMESTAMPING_CONFIG**](/windows/win32/api/mstcpip/ns-mstcpip-timestamping_config) dados.

Consulte também [Winsock timestamping](/windows/win32/winsock/winsock-timestamping).

### <a name="sio_translate_handle-opcode-setting-i-o-t1"></a>SIO \_ TRANSLATE \_ HANDLE (configuração de opcode: I, O, T==1)

Para obter um alça correspondente para *s* de soquete válido no contexto de uma interface de adendo (por exemplo, TH \_ NETDEV e TH \_ TAPI). Uma constante de manifesto que identifica a interface de adoção juntamente com quaisquer outros parâmetros necessários são especificados no buffer de entrada. O alça correspondente estará disponível no buffer de saída após a conclusão dessa função. Consulte a seção apropriada em [Anexos winsock para](winsock-annexes.md) obter detalhes específicos para uma interface de parceiro específica. O código de erro [WSAENOPROTOOPT](windows-sockets-error-codes-2.md) é indicado para provedores de serviço que não dão suporte a este ioctl para a interface complementar especificada. Esse IOCTL recupera o identificador associado usando **o \_ \_ identificador de conversão sio**.

É recomendável que o COM (Component Object Model) seja usado em vez deste IOCTL para descobrir e acompanhar outras interfaces que podem ter suporte em um soquete. Este IOCTL está presente para compatibilidade com versões anteriores com sistemas em que o COM não está disponível ou não pode ser usado por algum outro motivo.

### <a name="sio_udp_connreset-opcode-setting-i-t3"></a>SIO \_ UDP \_ CONNRESET (configuração de opcode: I, T = = 3)

**Windows XP:** Controla se \_ as mensagens INacessíveis da porta UDP são relatadas. Defina como **true** para habilitar o relatório. Defina como **false** para desabilitar os relatórios.

### <a name="sio_set_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ definir \_ \_ \_ registros de redirecionamento de conexão WFP \_ (configuração de opcode: I, T = = 3)

Define o registro de redirecionamento para o novo soquete TCP usado para se conectar ao destino final para uso por um serviço de redirecionamento WFP (Windows Filtering Platform).

O [**sio \_ set \_ WFP \_ Connection \_ Redirect \_ Records**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) IOCTL é usado como parte do rastreamento de conexão com proxy em conexões de soquete redirecionadas. Esse recurso de WFP facilita o rastreamento de registros de redirecionamento do redirecionamento inicial de uma conexão com a conexão final com o destino.

Para obter informações mais detalhadas, consulte a referência de [**\_ \_ \_ \_ \_ registros de redirecionamento de conexão WFP sio Set**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) . **Sio \_ A definição de \_ \_ \_ \_ registros de redirecionamento de conexão WFP** tem suporte no windows 8, Windows Server 2012 e posterior.

### <a name="sio_tcp_info-opcode-setting-i-o-t3"></a>\_ \_ Informações de TCP do SiO (configuração de opcode: i, O, T = = 3)

Recupera as estatísticas de TCP para um soquete. As estatísticas TCP são fornecidas em uma [**estrutura \_ \_ V0 de informações de TCP**](/windows/desktop/api/Mstcpip/ns-mstcpip-tcp_info_v0) .

Ao contrário da recuperação de estatísticas TCP com a função [**GetPerTcpConnectionEStats,**](/windows/win32/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) a recuperação de estatísticas TCP com esse código de controle não exige que o código do usuário carregue, armazene e filtre a tabela de conexão TCP e não exige privilégios elevados para usar.

Para obter mais informações, consulte [**SIO \_ TCP \_ INFO**](/previous-versions/windows/desktop/legacy/mt823415(v=vs.85)). **SIO \_ Há \_ suporte para TCP INFO** Windows 10, versão 1703, Windows Server 2016 e posterior.

## <a name="remarks"></a>Comentários

Os Ioctls winsock são definidos em vários arquivos de título diferentes. Eles incluem o arquivo de título *Winsock2.h,* *Mswsock.h* e *Mstcpip.h.*

No Microsoft Software Development Kit do Windows (SDK do Windows) (SDK) lançado para o Windows Vista e posterior, a organização dos arquivos de título foi alterada e vários Ioctls winsock também são definidos nos arquivos de título *Ws2def.h*, *Ws2ipdef.h* e *Mswsockdef.h.* O *arquivo de título Ws2def.h* é incluído automaticamente pelo arquivo de título *Winsock2.h.* O *arquivo de título Ws2ipdef.h* é incluído automaticamente pelo arquivo de título *Ws2tcpip.h.* O *arquivo de header Mswsockdef.h* é incluído automaticamente no arquivo de header *Mswsockdef.h.*

## <a name="requirements"></a>Requisitos

|Requisito|Valor|
|-|-|
| parâmetro<br/> | <dl> <dt>Winsock2.h; </dt> <dt>Mstcpip.h; </dt> <dt>Mswsock.h; </dt> <dt>Mswsockdef.h no Windows Vista, Windows Server 2008 e Windows 7 (inclua Mswsock.h); </dt> <dt>Ws2def.h no Windows Vista, Windows Server 2008 e Windows 7 (inclua Winsock2.h); </dt> <dt>Ws2ipdef.h no Windows Vista, Windows Server 2008 e Windows 7 (inclua Ws2tcpip.h)</dt> </dl> |
