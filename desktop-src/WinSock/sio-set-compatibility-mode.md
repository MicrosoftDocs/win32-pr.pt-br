---
description: Solicita como a pilha de rede deve lidar com determinados comportamentos para os quais a maneira padrão de manipular o comportamento pode ser diferente nas versões do Windows.
ms.assetid: 9574e21f-5ac4-4210-8031-2f3b07416813
title: SIO_SET_COMPATIBILITY_MODE código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 58972595adb71a30728cb4817a80814cd987a6de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105802153"
---
# <a name="sio_set_compatibility_mode-control-code"></a>SIO_SET_COMPATIBILITY_MODE código de controle

## <a name="description"></a>Descrição

O código de controle do **\_ \_ \_ modo de compatibilidade Set sio** solicita como a pilha de rede deve lidar com determinados comportamentos para os quais a maneira padrão de manipular o comportamento pode ser diferente nas versões do Windows.

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_SET_COMPATIBILITY_MODE, // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to WSA_COMPATIBILITY_MODE struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_SET_COMPATIBILITY_MODE, // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to WSA_COMPATIBILITY_MODE struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a>Parâmetros

### <a name="s"></a>s

Um descritor que identifica um soquete.

### <a name="dwiocontrolcode"></a>dwIoControlCode

O código de controle para a operação.
Use **o \_ \_ \_ modo de compatibilidade definir sio** para esta operação.

### <a name="lpvinbuffer"></a>lpvInBuffer

Um ponteiro para o buffer de entrada.
Esse parâmetro deve apontar para uma estrutura de **\_ \_ modo de compatibilidade de WSA** .

### <a name="cbinbuffer"></a>cbInBuffer

O tamanho, em bytes, do buffer de entrada.
Esse parâmetro deve ser igual ou maior que o tamanho da estrutura **do \_ \_ modo de compatibilidade de WSA** apontada pelo parâmetro *lpvInBuffer* .

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Um ponteiro para o buffer de saída.
Este parâmetro não é usado para esta operação.

### <a name="cboutbuffer"></a>cbOutBuffer

O tamanho, em bytes, do buffer de saída.
Esse parâmetro deve ser definido como zero.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.
Esse parâmetro retornado aponta para um valor **DWORD** de zero para esta operação, pois não há nenhuma saída.

### <a name="lpvoverlapped"></a>lpvOverlapped

Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .

Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.

Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).
Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.

Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.
Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).

### <a name="lpthreadid"></a>lpThreadId

Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).
O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.

**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .

### <a name="lperrno"></a>lpErrno

Um ponteiro para o código de erro.

**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.

Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.
Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Código do erro | Significado |
|------------|---------|
| **\_e/s de WSA \_ pendente** | Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior. |
| **operação de WSA \_ \_ anulada** | Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush** IOCTL. |
| **WSAEFAULT** | O parâmetro *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço do usuário. |
| **WSAEINPROGRESS** | A função é invocada quando um retorno de chamada está em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida. |
| **WSAEINVAL** | O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado. Esse erro será retornado se o parâmetro *cbInBuffer* for menor do que o sizeof da estrutura do **\_ \_ modo de compatibilidade do WSA** .
| **WSAENETDOWN** | Falha no subsistema de rede. |
| **WSAENOPROTOOPT** | Não há suporte para a opção de soquete no protocolo especificado. |
| **WSAENOTCONN** | O Soquete s não está conectado. |
| **WSAENOTSOCK** | O descritor *s* não é um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para o comando IOCTL especificado. Esse erro será retornado se o **sio \_ definir \_ o \_ modo de compatibilidade** do IOCTL não for suportado pelo provedor de transporte. Esse erro também é retornado quando uma tentativa de usar o **\_ modo de \_ compatibilidade \_ set de sio** é feita em um soquete de datagrama. |

## <a name="remarks"></a>Comentários

o **sio \_ definir \_ o \_ modo de compatibilidade** do IOCTL solicita como a pilha de rede deve lidar com determinados comportamentos para os quais a maneira padrão de manipular o comportamento pode ser diferente nas versões do Windows.
A estrutura do argumento de entrada para o modo de compatibilidade do conjunto de sio é especificada na estrutura do **modo de \_ compatibilidade \_ do WSA** definida no arquivo de cabeçalho *Mswsockdef. h* . **\_ \_ \_**
Um ponteiro para a estrutura do **\_ \_ modo de compatibilidade de WSA** é passado no parâmetro *cbInBuffer* .
Essa estrutura é definida da seguinte maneira:

```cpp
// Need to #include <mswsock.h>

/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

O valor especificado no membro **BehaviorID** indica o comportamento solicitado.
O valor especificado no membro **TargetOsVersion** indica a versão do Windows que está sendo solicitada para o comportamento.

O membro **BehaviorID** pode ser um dos valores do tipo de enumeração de ID do comportamento de compatibilidade do WSA definido no arquivo de cabeçalho *Mswsockdef. h* . **\_ \_ \_**
Os valores possíveis para o membro **BehaviorID** são os seguintes:

| Termo | Descrição |
|------|-------------|
| WsaBehaviorAll | Isso é equivalente a solicitar todos os comportamentos compatíveis possíveis definidos para a **\_ ID de \_ comportamento \_ de compatibilidade de WSA**. |
| WsaBehaviorReceiveBuffering | Quando o membro **TargetOsVersion** é definido como um valor para o Windows Vista ou posterior, as reduções para o tamanho do buffer de recebimento TCP nesse soquete usando a opção de soquete **\_ RCVBUF,** são permitidas mesmo após uma conexão TCP ter sido estabelecimento. Quando o membro **TargetOsVersion** é definido como um valor anterior ao Windows Vista, as reduções no tamanho do buffer de recebimento TCP nesse soquete usando a opção de soquete **\_ RCVBUF** não são permitidas após o estabelecimento da conexão. |
| WsaBehaviorAutoTuning | Quando o membro **TargetOsVersion** é definido como um valor para o Windows Vista ou posterior, o ajuste automático da janela de recebimento é habilitado e o fator de escala da janela TCP é reduzido para 2 a partir do valor padrão de 8. Quando **TargetOsVersion** é definido como um valor anterior ao Windows Vista, o ajuste automático da janela de recebimento está desabilitado. A opção de dimensionamento da janela TCP também está desabilitada e o tamanho máximo da janela de recepção é limitado a 65.535 bytes. A opção de dimensionamento da janela TCP não pode ser negociada na conexão mesmo que a opção de soquete **\_ RCVBUF** seja chamada nesse soquete especificando um valor maior que 65.535 bytes antes da conexão ser estabelecida. |

O membro **TargetOsVersion** pode ser uma das constantes da versão NTDDI definidas no arquivo de cabeçalho *Sdkddkver. h* .
Alguns dos valores possíveis para o membro **TargetOsVersion** são os seguintes:

| Termo | Descrição |
|------|-------------|
| NTDDI \_ Longhorn | O comportamento de destino é o padrão para o Windows Vista. |
| NTDDI \_ WS03 | O comportamento de destino é o padrão para o Windows Server 2003. |
| NTDDI \_ WinXP | O comportamento de destino é o padrão para o Windows XP. |
| NTDDI \_ Win2k | O comportamento de destino é o padrão para o Windows 2000. |

O impacto principal do membro **TargetOsVersion** é se esse membro está definido como um valor igual ou maior que o **NTDDI \_ Longhorn**.

O desempenho do TCP depende não apenas da própria taxa de transferência, mas sim do produto da taxa de transferência e do tempo de atraso da viagem de ida e volta.
Esse produto de atraso de largura de banda mede a quantidade de dados que "preencherão o pipe".
Esse produto de atraso de largura de banda é o espaço em buffer necessário no remetente e no destinatário para obter a taxa de transferência máxima na conexão TCP no caminho.
Esse espaço de buffer representa a quantidade de dados não confirmados que o TCP deve manipular para manter o pipeline cheio.
Problemas de desempenho de TCP surgem quando o produto de atraso de largura de banda é grande.
Um caminho de rede operando nessas condições geralmente é chamado de "pipe longo, de Fat".
Os exemplos incluem links de satélite de pacotes de alta capacidade, links sem fio de alta velocidade e links de fibra óptica terrestres por longas distâncias.

O cabeçalho TCP usa um campo de dados de 16 bits (o campo de janela no cabeçalho do pacote TCP) para relatar o tamanho da janela de recebimento para o remetente.
Portanto, a maior janela que pode ser usada é de 65.535 bytes.
Para evitar essa limitação, uma opção de extensão TCP, escala de janela TCP, foi adicionada para TCP de alto desempenho para permitir o Windows com mais de 65.535 bytes.
A opção de dimensionamento de janela TCP (WSopt) é definida no RFC 1323 disponível no [site da IETF](https://www.ietf.org/rfc/rfc1122.txt).
A extensão WSopt expande a definição da janela TCP para 32 bits usando um fator de escala logarítmica de um byte para estender o campo de janela de 16 bits no cabeçalho TCP.
A extensão WSopt define um fator de escala implícito (2 a alguma potência), que é usado para multiplicar o valor de tamanho da janela encontrado em um cabeçalho TCP para obter o tamanho de janela verdadeiro.
Portanto, um fator de dimensionamento de janela de 8 resultaria em um tamanho de janela verdadeiro igual ao valor no campo janela no cabeçalho TCP multiplicado por 2 ^ 8 ou 256.
Portanto, se o campo de janela no cabeçalho TCP tiver sido definido com o valor máximo de 65.535 bytes e o fator de escala WSopt fosse negociado com um valor de 8, o tamanho de janela verdadeiro seria de 16.776.960 bytes.

O verdadeiro tamanho da janela de recepção e, portanto, o fator de escala é determinado pelo espaço máximo de buffer de recebimento.
Esse espaço máximo de buffer é a quantidade de dados que um receptor TCP permite que um remetente TCP envie antes de ter que esperar por uma confirmação.
Depois que a conexão é estabelecida, o tamanho da janela de recebimento é anunciado em cada segmento TCP (o campo janela no cabeçalho TCP).
Anunciar a quantidade máxima de dados que o remetente pode enviar é um mecanismo de controle de fluxo do lado do destinatário que impede que o remetente envie dados que o receptor não pode armazenar.
Um host de envio só pode enviar a quantidade máxima de dados anunciados pelo receptor antes de aguardar uma confirmação e uma atualização de tamanho de janela de recebimento.

No Windows Server 2003 e no Windows XP, o espaço máximo de buffer de recebimento que representa o tamanho da janela de recebimento para a pilha TCP/IP tem um valor padrão baseado na velocidade do link da interface de envio.
O valor real é ajustado automaticamente para até mesmo incrementos do MSS (tamanho máximo de segmento) negociado durante o estabelecimento de conexão TCP.
Portanto, para um link de 10 Mbit/s, o tamanho padrão da janela de recepção normalmente seria definido como 16K bytes, enquanto em um link de 100 MBit/s o tamanho da janela de recebimento padrão seria definido como 65.535 bytes.

No Windows Server 2003 e no Windows XP, o tamanho máximo real da janela de recepção para a pilha TCP/IP pode ser configurado manualmente usando os seguintes valores de registro em uma interface específica ou para todo o sistema:

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\TCPWindowSize`

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Interface\TCPWindowSize`

O valor do registro para **TcpWindowSize** pode ser definido como um máximo de 65.535 bytes quando não estiver usando a extensão WSopt ou um máximo de 1.073.741.823 bytes quando a extensão WSopt for usada (há suporte para um fator de escala máximo de 4).
Sem o dimensionamento da janela, um aplicativo só pode obter uma taxa de transferência de aproximadamente 5 megabits por segundo (Mbps) em um caminho com um RTT (tempo de ida e volta) de 100 milissegundo, independentemente da largura de banda do caminho.
Essa taxa de transferência pode ser dimensionada para mais de um gigabit por segundo (Gbps) com dimensionamento de janela, o que permite que o TCP negocie o fator de dimensionamento para o tamanho da janela durante o estabelecimento da conexão.

No Windows Server 2003 e no Windows XP, a extensão WSopt pode ser habilitada definindo o seguinte valor de registro.

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Tcp1323Opts`

O valor do registro **TCP1323Opts** é um **DWORD** codificado de modo que quando o bit 0 é definido, a extensão TCP WSopt está habilitada.
Quando o bit 1 é definido, a opção de carimbo de data/hora TCP (TSopt) definida no RFC 1323 é habilitada.
Portanto, um valor de 1 ou 3 habilitará a extensão WSopt.

No Windows Server 2003 e no Windows XP, o padrão é que os valores de registro TCPWindowSize e Tcp1323Opts não sejam criados.
Portanto, o padrão é que a extensão WSopt está desabilitada e o tamanho da janela de recepção TCP é definido pelo sistema para o valor máximo de até 65.535 bytes com base na velocidade do link.
Quando o dimensionamento de janela é habilitado no Windows Server 2003 e no Windows XP definindo o valor do registro Tcp1323Opts, o dimensionamento da janela em uma conexão TCP ainda é usado apenas quando o remetente e o receptor incluem uma opção de escala de janela TCP no segmento sincronizar (SYN) enviado entre si para negociar um fator de escala de janela.
Quando o dimensionamento da janela é usado em uma conexão, o campo janela no cabeçalho TCP é definido como 65.535 bytes e o fator de escala da janela é usado para ajustar o tamanho da janela de recepção em cima pelo fator de escala da janela negociado quando a conexão é estabelecida.

Um aplicativo pode especificar o tamanho da janela de recepção TCP para uma conexão usando a opção de soquete **\_ RCVBUF** .
O tamanho da janela de recepção TCP para um soquete pode ser aumentado a qualquer momento usando o **\_ RCVBUF**, mas só pode ser reduzido antes de estabelecer uma conexão.
Para usar o dimensionamento de janela, um aplicativo deve especificar um tamanho de janela maior que 65.535 bytes ao usar a opção de soquete **\_ RCVBUF** antes que a conexão seja estabelecida.

Geralmente, é difícil determinar o valor ideal para o tamanho da janela de recepção TCP.
Para preencher a capacidade da rede entre o remetente e o destinatário, o tamanho da janela de recebimento deve ser definido como o produto de atraso da largura de banda da conexão, que é a largura de banda multiplicada pelo tempo de viagem de ida e volta.
Mesmo que um aplicativo possa determinar corretamente o produto de atraso da largura de banda, ainda não é conhecido com a rapidez com que o aplicativo de recebimento recuperará dados do buffer de dados de entrada (a taxa de recuperação do aplicativo).
Apesar do suporte para o dimensionamento de janela de TCP, o tamanho máximo da janela de recepção no Windows Server 2003 e no Windows XP ainda pode limitar a taxa de transferência, pois é um tamanho máximo fixo para todas as conexões TCP (a menos que especificado por aplicativo usando **\_ RCVBUF**), o que pode melhorar a taxa de transferência para algumas conexões e diminuir a taxa de transferência para outras.
Além disso, o tamanho máximo fixo da janela de recepção para uma conexão TCP não varia de acordo com as condições de rede em alteração.

Para resolver o problema de determinar corretamente o valor do tamanho máximo da janela de recepção para uma conexão TCP com base nas condições atuais da rede, a pilha de TCP/IP no Windows Vista dá suporte a um recurso de ajuste automático da janela de recebimento.
Quando esse recurso é habilitado, o ajuste automático da janela de recebimento determina continuamente o tamanho da janela de recepção verdadeiro ideal medindo o produto de atraso da largura de banda e a taxa de recuperação do aplicativo e ajusta o tamanho máximo real da janela de recepção com base na alteração das condições de rede.
O ajuste automático da janela de recebimento habilita a extensão TCP WSopt por padrão, permitindo até 16.776.960 bytes para o tamanho real da janela.
À medida que os dados fluem pela conexão, a pilha TCP/IP monitora a conexão, mede o produto de atraso de largura de banda atual para a conexão e a taxa de recebimento do aplicativo e ajusta o tamanho real da janela de recepção para otimizar a taxa de transferência.
A pilha TCP/IP altera o valor do campo Window no cabeçalho TCP com base nas condições de rede, pois o fator de escala WSopt é fixo quando a conexão é estabelecida pela primeira vez.

A pilha de TCP/IP no Windows Vista não usa mais os valores de registro **TcpWindowSize** .
Com uma melhor taxa de transferência entre os pares de TCP, a utilização da largura de banda de rede aumenta durante a transferência de dados.
Se todos os aplicativos forem otimizados para receber dados TCP, a utilização geral da rede poderá aumentar substancialmente, tornando o uso da QoS (qualidade de serviço) mais importante em redes que estão operando na capacidade ou perto dela.

O comportamento padrão no Windows Vista para buffer de recebimento quando **o \_ \_ \_ modo de compatibilidade Set sio** não é especificado usando **WsaBehaviorReceiveBuffering** é que nenhuma reduções de tamanho de janela de recebimento usando a opção de soquete **\_ RCVBUF** é permitida depois que uma conexão é estabelecida.

O comportamento padrão no Windows Vista para ajuste automático quando o **\_ modo de \_ compatibilidade \_ set sio** não é especificado usando **WsaBehaviorAutoTuning** é que a pilha fará o ajuste automático da janela de recepção usando um fator de escala de janela de 8.
Observe que, se um aplicativo definir um tamanho de janela de recebimento válido com a opção de soquete **\_ RCVBUF** , a pilha usará o tamanho especificado e a janela de recebimento automático será desabilitada.
O ajuste automática do Windows também pode ser desabilitado completamente usando o comando a seguir `netsh interface tcp set global autotuninglevel=disabled` . nesse caso, especificar **WsaBehaviorAutoTuning** não terá nenhum efeito.
A janela receber ajuste automática também pode ser desabilitada com base na política de grupo definida no Windows Server 2008.

A opção **WsaBehaviorAutoTuning** é necessária no Windows Vista para alguns dispositivos de gateway de Internet e firewalls que não dão suporte correto a fluxos de dados para conexões TCP que usam a extensão WSopt e um fator de escala do Windows.
No Windows Vista, um receptor, por padrão, negocia um fator de dimensionamento de janela de 8 para um tamanho de janela verdadeiro máximo de 16.776.960 bytes.
Quando os dados começam a fluir em um link rápido, o Windows inicialmente começa com um tamanho de janela true de 64 KB definindo o campo Window do cabeçalho TCP como 256 e definindo o fator de escala da janela como 8 nas opções TCP (256 * 2 ^ 8 = 64 KB).
Alguns dispositivos e firewalls de gateway de Internet ignoram o fator de escala da janela e apenas examinam o campo de janela anunciado no cabeçalho TCP especificado como 256 e removem os pacotes de entrada para a conexão que contém mais de 256 bytes de dados TCP.
Para dar suporte ao dimensionamento da janela de recepção TCP, um dispositivo ou firewall de gateway deve monitorar o handshake TCP e acompanhar o fator de escala da janela negociada como parte dos dados de conexão TCP.
Além disso, alguns aplicativos e implementações de pilha TCP em outras plataformas ignoram a extensão TCP WSopt e o fator de dimensionamento de janela.
Portanto, o host remoto que envia os dados pode enviar dados na taxa anunciada no campo janela do cabeçalho TCP (256 bytes).
Isso pode resultar na recebimento de dados muito lentos pelo receptor.

Definir o membro **BehaviorID** como **WsaBehaviorAutoTuning** e o **TargetOsVersion** para o Windows Vista reduz o fator de escala da janela para 2, de modo que o campo janela no cabeçalho TCP é inicialmente definido como 16.384 bytes e o fator de escala da janela é definido como 2 para um tamanho de recebimento de janela real inicial de 64K bytes.
O recurso de ajuste automático da janela pode aumentar o tamanho de recebimento da janela true até 262.140 bytes, definindo o campo Window no cabeçalho TCP para 65.535 bytes.
Um aplicativo deve definir o **\_ modo de \_ compatibilidade \_ do sio Set** para o IOCTL assim que um soquete é criado, pois essa opção não faz sentido ou se aplica depois que um SYN é enviado.
Definir essa opção tem o mesmo impacto que o seguinte comando: `netsh interface tcp set global autotuninglevel=highlyrestricted`

Observe que o arquivo de cabeçalho *Mswsockdef. h* é incluído automaticamente em *mswsock. h* ou *Netiodef. h* e não deve ser usado diretamente.

## <a name="see-also"></a>Confira também

[**SSA**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
