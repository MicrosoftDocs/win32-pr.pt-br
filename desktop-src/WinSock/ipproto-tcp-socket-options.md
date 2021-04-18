---
description: A tabela a seguir descreve \_ as opções de soquete TCP IPPROTO que se aplicam aos soquetes criados para as famílias de endereços IPv4 e IPv6 (AF \_ inet e AF \_ INET6) com o parâmetro Protocol para a função socket especificada como TCP (IPPROTO \_ TCP).
ms.assetid: 2a10498d-0a0b-4a2d-941e-9aa45a1a4428
title: Opções de soquete IPPROTO_TCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d261a639c10faa8c8ef52ba1ae88a0fbc52a16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813607"
---
# <a name="ipproto_tcp-socket-options"></a>\_Opções de soquete TCP IPPROTO

A tabela a seguir descreve as opções de soquete **\_ TCP IPPROTO** que se aplicam aos soquetes criados para as famílias de endereços IPv4 e IPv6 (AF \_ inet e AF \_ INET6) com o parâmetro *Protocol* para a função [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) especificada como TCP (IPPROTO \_ TCP). Consulte as páginas de referência de função [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) e [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) para obter mais informações sobre como obter e definir opções de soquete.

Para enumerar protocolos e descobrir Propriedades com suporte para cada protocolo instalado, use a função [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

## <a name="options"></a>Opções

<table>
<colgroup>
<col/>
<col/>
<col/>
<col/>
<col/>
</colgroup>
<thead>
<tr class="header">
<th>Opção</th>
<th>Obter</th>
<th>Definir</th>
<th>Tipo de optval</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr>
<td>TCP_BSDURGENT</td>
<td>sim</td>
<td>sim</td>
<td>DWORD (booliano)</td>
<td>Se <strong>for true</strong>, o provedor de serviços implementará o estilo BSD (Berkeley Software Distribution) (padrão) para manipulação de dados emitidos. Essa opção é o inverso da opção TCP_EXPEDITED_1122. Essa opção só pode ser definida na conexão uma vez. Depois que essa opção é definida em, essa opção não pode ser desativada. Essa opção não precisa ser implementada pelos provedores de serviços. A opção é habilitada (definida como <strong>true</strong>) por padrão.</td>
</tr>
<tr>
<td>TCP_EXPEDITED_1122</td>
<td>sim</td>
<td>sim</td>
<td>DWORD (booliano)</td>
<td>Se <strong>for true</strong>, o provedor de serviços implementará os dados emitidos conforme especificado em RFC-1222. Caso contrário, o estilo de distribuição de software Berkeley (BSD) (padrão) será usado. Essa opção só pode ser definida na conexão uma vez. Depois que essa opção é definida em, essa opção não pode ser desativada. Essa opção não precisa ser implementada pelos provedores de serviços.</td>
</tr>
<tr>
<td>TCP_FAIL_CONNECT_ON_ICMP_ERROR</td>
<td>sim</td>
<td>sim</td>
<td>DWORD (booliano)</td>
<td>Se <strong>for true</strong>, uma chamada à API Connect retornará após a recepção de um erro de ICMP com o valor WSAEHOSTUNREACH. O endereço de origem do erro estará disponível por meio da opção de soquete TCP_ICMP_ERROR_INFO. Se <strong>for false</strong>, o soquete se comporta normalmente. O padrão é desabilitado (definido como <strong>false</strong>). Para a segurança de tipo, você deve usar as funções <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror">WSAGetFailConnectOnIcmpError</a> e <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror">WSASetFailConnectOnIcmpError</a> em vez de usar a opção socket diretamente.</td>
</tr>
<tr>
<td>TCP_ICMP_ERROR_INFO</td>
<td>sim</td>
<td>não</td>
<td><a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a></td>
<td>Recupera as informações de um erro ICMP recebido pelo soquete TCP durante uma chamada de conexão com falha. Válido somente em um soquete TCP em que TCP_FAIL_CONNECT_ON_ICMP_ERROR foi habilitado anteriormente e <strong>Connect</strong> retornou WSAEHOSTUNREACH. A consulta é sem bloqueio. Se consultado com êxito e o valor de optlen retornado for 0, nenhum erro de ICMP será recebido desde a última chamada de conexão. Se um erro ICMP foi recebido, suas informações estarão disponíveis até que o <strong>Connect</strong> seja chamado novamente. As informações são retornadas como uma estrutura de <a href="/windows/win32/api/ws2ipdef/ns-ws2ipdef-icmp_error_info">ICMP_ERROR_INFO</a> . Para a segurança de tipo, você deve usar a função <a href="/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo">WSAGetIcmpErrorInfo</a> em vez de usar a opção socket diretamente.</td>
</tr>
<tr>
<td>TCP_KEEPCNT</td>
<td>sim</td>
<td>sim</td>
<td>DWORD</td>
<td>Obtém ou define o número de investigações de Keep Alive de TCP que serão enviadas antes que a conexão seja encerrada. É ilegal definir TCP_KEEPCNT como um valor maior que 255.</td>
</tr>
<tr>
<td>TCP_MAXRT</td>
<td>sim</td>
<td>sim</td>
<td>DWORD</td>
<td>Se esse valor for não negativo, ele representará o tempo limite de conexão desejado em segundos. Se for-1, ele representa uma solicitação para desabilitar o tempo limite de conexão (ou seja, a conexão será retransmitida para sempre). Se o tempo limite da conexão for desabilitado, o tempo limite de retransmissão aumentará exponencialmente para cada retransmissão até seu valor máximo de 60sec e, em seguida, permanecerá lá.</td>
</tr>
<tr>
<td>TCP_NODELAY</td>
<td>sim</td>
<td>sim</td>
<td>DWORD (booliano)</td>
<td>Habilita ou desabilita o algoritmo Nagle para Soquetes TCP. Essa opção é desabilitada (definida como FALSE) por padrão.</td>
</tr>
<tr>
<td>TCP_TIMESTAMPS</td>
<td>sim</td>
<td>sim</td>
<td>DWORD (booliano)</td>
<td>Habilita ou desabilita carimbos de data/hora RFC 1323. Observe que há também uma configuração global para carimbos de data/hora (o padrão é off), &quot; carimbos &quot; de data/hora em (set/get)-nettcpsetting. Definir essa opção de soquete substitui essa definição de configuração global.</td>
</tr>
<tr>
<td>TCP_FASTOPEN</td>
<td>sim</td>
<td>sim</td>
<td>DWORD (booliano)</td>
<td>Habilita ou desabilita o <a href="https://tools.ietf.org/html/rfc7413">RFC 7413</a> TCP Fast Open, que permite que você comece a enviar dados durante a fase de handshake de três vias de abrir uma conexão. Observe que para fazer uso de aberturas rápidas, você deve usar <a href="/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex"><strong>ConnectEx</strong></a> para fazer a conexão inicial e especificar os dados no parâmetro <em>lpSendBuffer</em> da função a ser transferido durante o processo de handshake. Alguns dos dados no <em>lpSendBuffer</em> serão transferidos com o protocolo Open Fast.</td>
</tr>
<tr>
<td>TCP_KEEPIDLE</td>
<td>sim</td>
<td>sim</td>
<td>DWORD</td>
<td>Obtém ou define o número de segundos que uma conexão TCP permanecerá ociosa antes que as investigações de KeepAlive sejam enviadas para o remoto.
<blockquote>
[!Note]<br />
Essa opção está disponível a partir do Windows 10, versão 1709.
</blockquote>
<br/></td>
</tr>
<tr>
<td>TCP_KEEPINTVL</td>
<td>sim</td>
<td>sim</td>
<td>DWORD</td>
<td>Obtém ou define o número de segundos que uma conexão TCP aguardará por uma resposta de KeepAlive antes de enviar outra investigação de KeepAlive.
<blockquote>
[!Note]<br />
Essa opção está disponível a partir do Windows 10, versão 1709.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>

## <a name="windows-support-for-ipproto_tcp-options"></a>Suporte do Windows para \_ Opções TCP IPPROTO

| Opção | Windows 10 | Windows 7 | Windows Server 2008 | Windows Vista |
|-|-|-|-|-|
| \_BSDURGENT TCP | x | x | x | x |
| TCP \_ expedida \_ 1122 | x | x | x | x |
| \_KEEPCNT TCP | A partir do Windows 10, versão 1703 | | | |
| \_MAXRT TCP | x | x | x | x |
| TCP \_ NOdelay | x | x | x | x |
| \_carimbos de data/hora TCP | x | x | x | x |
| \_FASTOPEN TCP | A partir do Windows 10, versão 1607 | | | |

<br/>

 | Opção | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/me |
|-|-|-|-|-|-|
| \_BSDURGENT TCP | x | x | x | x | |
| TCP \_ expedida \_ 1122 | x | x | x | | |
| \_KEEPCNT TCP | | | | | |
| \_MAXRT TCP | | | | | |
| TCP \_ NOdelay | x | x | x | x | |
| \_carimbos de data/hora TCP | | | | | |
| \_FASTOPEN TCP | | | | | |

## <a name="remarks"></a>Comentários

No SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior, a organização dos arquivos de cabeçalho mudou e **IPPROTO \_** nível de TCP é definido no arquivo de cabeçalho *Ws2def. h* , que é incluído automaticamente no arquivo de cabeçalho *Winsock2. h* . As opções de soquete **\_ TCP IPPROTO** , com exceção de **TCP \_ BSDURGENT**, são definidas no arquivo de cabeçalho *Ws2ipdef. h* , que é incluído automaticamente no arquivo de cabeçalho *Ws2tcpip. h* . A opção **TCP \_ BSDURGENT** para motivos históricos é definida no arquivo de cabeçalho *mswsock. h* . Os arquivos de cabeçalho *Ws2def. h* e *Ws2ipdef. h* nunca devem ser usados diretamente.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-|-|
| parâmetro | <dl> <dt>Ws2def. h (incluir Winsock2. h); </dt> <dt>Winsock2. h no Windows Server 2003, Windows XP e windows 2000</dt> </dl> |
