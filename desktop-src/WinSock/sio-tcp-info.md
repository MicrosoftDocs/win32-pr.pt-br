---
description: O código de controle recupera as estatísticas do protocolo TCP para um soquete especificado.
ms.assetid: AB5F25B6-D2D2-42D7-8189-06CAC4842C66
title: SIO_TCP_INFO de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 60b4c04fc4629e67fcd9dc07a4590b4a1b4c735e84000b1272e27681b4436f0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244846"
---
# <a name="sio_tcp_info-control-code"></a>SIO_TCP_INFO de controle

## <a name="description"></a>Descrição

O **código de controle \_ SIO TCP \_ INFO** recupera as estatísticas do protocolo TCP para um soquete especificado.

Para executar essa operação, chame a [**função WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) **ou WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
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

### <a name="dwiocontrolcode"></a>Dwiocontrolcode

O código de controle para a operação.
Use **SIO \_ TCP \_ INFO** para esta operação.

### <a name="lpvinbuffer"></a>Lpvinbuffer

Um ponteiro para o buffer de entrada.
Esse parâmetro contém um ponteiro para **um DWORD** que especifica a versão do código de controle **\_ SIO TCP \_ INFO** que você está usando. Especifique 0 para [usar TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0). Especifique 1 para [usar TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1), que fornece mais campos.

### <a name="cbinbuffer"></a>Cbinbuffer

O tamanho, em bytes, do buffer de entrada.
Esse parâmetro deve ser o tamanho do tipo **de dados DWORD.**

### <a name="lpvoutbuffer"></a>Lpvoutbuffer

Um ponteiro para o buffer de saída.
Na saída bem-sucedida, esse parâmetro contém um ponteiro para [**uma estrutura TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) que contém as estatísticas TCP para o soquete especificado.

### <a name="cboutbuffer"></a>cbOutBuffer

O tamanho, em bytes, do buffer de saída.
Esse parâmetro deve ter pelo menos o tamanho da estrutura [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) dados.

### <a name="lpcbbytesreturned"></a>Lpcbbytesreturned

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.

Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* aponta para um **valor DWORD** de zero.

Se *lpOverlapped* for **NULL,** o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.

Se o *parâmetro lpOverlapped* não for **NULL** para soquetes sobrepondo, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada posteriormente.
O **valor DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado pode ser zero, pois o tamanho dos dados armazenados não pode ser determinado até que a operação sobrecarregada seja concluída.
O status de conclusão final pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.

### <a name="lpvoverlapped"></a>lpvOverlapped

Um ponteiro para uma [**estrutura WSAOVERLAPPED.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

Se o *soquete s* tiver sido criado sem o atributo sobrecodado, *o parâmetro lpOverlapped* será ignorado.

Se *s* foi aberto com o atributo sobre mapeado e o parâmetro *lpOverlapped* não é **NULL,** a operação é executada como uma operação sobressalo (assíncrona).
Nesse caso, *o parâmetro lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.

Para operações sobreporadas, a [**função WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente e o método de conclusão apropriado é sinalizado quando a operação é concluída.
Caso contrário, a função não retornará até que a operação seja concluída ou ocorra um erro.

### <a name="lpcompletionroutine"></a>Lpcompletionroutine

Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobre mapeados).

### <a name="lpthreadid"></a>lpThreadId

Um ponteiro para uma [**estrutura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usada pelo provedor em uma chamada subsequente para [**WPUQueueApc.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)
O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até depois que a [**função WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) retornar.

**Observação**  Esse parâmetro se aplica somente à **função WSPIoctl.**

### <a name="lperrno"></a>Lperrno

Um ponteiro para o código de erro.

**Observação**  Esse parâmetro se aplica somente à **função WSPIoctl.**

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com êxito, a [**função WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) **ou WSPIoctl** retornará zero.

Se a operação falhar ou estiver pendente, a [**função WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **SOCKET \_ ERROR**.
Para obter informações de erro estendidas, [**chame WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Código do erro | Significado |
|------------|---------|
| **WSAEMSGSIZE** | O ponteiro para o buffer de entrada **era NULL** ou o tamanho especificado do buffer de entrada não estava correto. |
| **Wsaeinval** | Foi fornecido um argumento inválido. Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado. |

## <a name="remarks"></a>Comentários

Ao contrário da recuperação de estatísticas TCP com a função [**GetPerTcpConnectionEStats,**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) a recuperação de estatísticas TCP com esse código de controle não exige que o código do usuário carregue, armazene e filtre a tabela de conexão TCP e não exige privilégios elevados para usar.

## <a name="see-also"></a>Confira também

[Soquete](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0)

[**GetPerTcpConnectionEStats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats)

[**Wsagetlasterror**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**Wsagetoverlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**Wsaioctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlapped**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
