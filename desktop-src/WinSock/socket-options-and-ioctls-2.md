---
description: Algumas das opções de soquete do Windows Sockets 2 são resumidas na tabela a seguir.
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: Opções de soquete e IOCTLs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472d37bd8d2d97eead66d7c9d2319e57fc5dafde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814561"
---
# <a name="socket-options-and-ioctls"></a>Opções de soquete e IOCTLs

Algumas das opções de soquete do Windows Sockets 2 são resumidas na tabela a seguir. Informações mais detalhadas são fornecidas na seção 4 em [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) e/ou [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)). Há outras novas opções de soquete específicas de protocolo que podem ser encontradas no anexo Protocol-Specific. Uma lista completa de [**Opções de soquete**](socket-options.md) para Windows Sockets está disponível na referência do Winsock.

Para obter um resumo de alguns dos IOCTLs do Winsock, consulte [Resumo dos opcodes do soquete do IOCTL](summary-of-socket-ioctl-opcodes-2.md). Uma lista completa de [**IOCTLs do Winsock**](winsock-ioctls.md) está disponível na referência do Winsock.

## <a name="summary-of-common-socket-options"></a>Resumo das opções de soquetes comuns

Um provedor de serviços Winsock deve reconhecer todas essas opções e (para [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) retornar valores plausível para cada. O valor padrão para cada opção é mostrado na tabela a seguir.

Valor

Type

Significado

Padrão

Observação

<span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>\_ACCEPTCONN

BOOL

O soquete está ouvindo.

FALSE, a menos que um [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) tenha sido executado.

<span id="SO_BROADCAST"></span><span id="so_broadcast"></span>\_difusão

BOOL

O soquete está configurado para a transmissão e o recebimento de mensagens de difusão.

FALSE

<span id="SO_DEBUG"></span><span id="so_debug"></span>\_depuração

BOOL

A depuração está habilitada.

FALSE

Encontrei

<span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>\_DONTLINGER

BOOL

Se for true, a \_ opção for remanescente será desabilitada.

TRUE

<span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>\_DONTROUTE

BOOL

O roteamento está desabilitado. É bem-sucedida, mas é ignorado em \_ soquetes inet de AF; falha em \_ soquetes INET6 de AF com [WSAENOPROTOOPT](windows-sockets-error-codes-2.md). Sem suporte em Soquetes ATM (resulta em um erro).

FALSE

Encontrei

<span id="SO_ERROR"></span><span id="so_error"></span>\_erro

INT

Recupera o status de erro e limpe.

0

<span id="SO_GROUP_ID"></span><span id="so_group_id"></span>Portanto, a \_ ID do grupo \_

GROUP

Reservado.

NULO

Obter somente

<span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>Portanto \_ , \_ prioridade de grupo

INT

Reservado.

0

[**Portanto, \_ KeepAlive**](so-keepalive.md)

BOOL

As keepalives estão sendo enviadas. Sem suporte em Soquetes ATM (resulta em um erro).

FALSE

Encontrei

<span id="SO_LINGER"></span><span id="so_linger"></span>Então, \_ remanescente

Estrutura persistente

Retorna as opções atuais remanescentes.

l \_ Onoff é 0

<span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>Portanto \_ , \_ tamanho máximo da mensagem \_

INT

Tamanho máximo de saída de uma mensagem para tipos de soquete de mensagem. Não há nenhuma provisão para determinar o tamanho máximo da mensagem de entrada. Não tem significado para soquetes orientados a fluxo.

Dependente de implementação

Obter somente

<span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>\_OOBINLINE

BOOL

Os dados OOB estão sendo recebidos no fluxo de dados normal.

FALSE

<span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>Portanto \_ , \_ INFOW de protocolo

[ **\_ informações de WSAPROTOCOL** de estrutura](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)

Descrição das informações de protocolo para o protocolo que está associado a este Soquete.

Dependente de protocolo

Obter somente

<span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>\_RCVBUF

INT

O espaço total de buffer por soquete reservado para receives. Isso não está relacionado ao \_ tamanho máximo \_ \_ da mensagem e não corresponde necessariamente ao tamanho da janela de recepção TCP.

Dependente de implementação

Encontrei

<span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>\_REUSEADDR

BOOL

O endereço ao qual esse soquete está associado pode ser usado por outras pessoas. Não aplicável em Soquetes ATM.

FALSE

<span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>\_SNDBUF

INT

O espaço total de buffer por soquete reservado para envios. Isso não está relacionado ao \_ tamanho máximo \_ \_ da mensagem e não corresponde necessariamente ao tamanho de uma janela de envio TCP.

Dependente de implementação

Encontrei

<span id="SO_TYPE"></span><span id="so_type"></span>Portanto, \_ digite

INT

O tipo de soquete (por exemplo, fluxo de SOCK \_ ).

Conforme criado por meio do soquete.

<span id="PVD_CONFIG"></span><span id="pvd_config"></span>configuração do PVD \_

caractere de longe \*

Um objeto de estrutura de dados opaco que contém informações de configuração do provedor de serviços.

Dependente de implementação

<span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP \_ NOdelay

BOOL

Desabilita o algoritmo Nagle para união de envio.

Dependente de implementação

(i) um provedor de serviços pode ignorar silenciosamente essa opção em [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) e retornar um valor constante para [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), ou pode aceitar um valor para **WSPSetSockOpt** e retornar o valor correspondente em **WSPGetSockOpt** sem usar o valor de forma alguma.



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Opções de soquete**](socket-options.md)
</dt> <dt>

[**Opções de soquete de soquete de SOL \_**](sol-socket-socket-options.md)
</dt> <dt>

[**\_Opções de soquete TCP IPPROTO**](ipproto-tcp-socket-options.md)
</dt> <dt>

[**\_Opções de soquete UDP IPPROTO**](ipproto-udp-socket-options.md)
</dt> <dt>

[**Winsock IOCTLs**](winsock-ioctls.md)
</dt> </dl>

 

 
