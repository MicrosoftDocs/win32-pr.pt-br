---
description: O seguinte descreve o incidente de operações para desligar uma conexão de soquete estabelecida.
ms.assetid: 052e04a4-5290-4dca-af7a-cd590ebfbe15
title: Desligamento de conexão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babbd26716c255c83a8ecc17305d9e59676645739a6f90d18ac72b5bcda49241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898416"
---
# <a name="connection-shutdown"></a>Desligamento de conexão

O seguinte descreve o incidente de operações para desligar uma conexão de soquete estabelecida.

## <a name="initiating-shutdown-sequence"></a>Iniciando sequência de desligamento

Uma conexão de soquete pode ser retirada de várias maneiras. [**WSPShutdown**](/previous-versions/windows/desktop/legacy/ms742294(v=vs.85)) (com *o* igual a SD \_ Send ou SD \_ both) e [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) pode ser usado para iniciar um desligamento de conexão normal. O [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) pode ser usado para iniciar um desligamento normal ou de anulação, dependendo das opções remanescentes invocadas pelo fechamento de um soquete. Consulte abaixo para obter mais informações sobre desligamentos normais e anuláveis e opções remanescentes.

## <a name="indicating-remote-shutdown"></a>Indicando o desligamento remoto

Provedores de serviço indicam a desmontagem de conexão que é iniciada pela parte remota por meio do \_ evento FD Close Network. O desligamento normal também é indicado por meio de [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) quando o número de bytes lidos é 0 para protocolos de fluxo de bytes ou por meio de um código de erro de retorno de WSAEDISCON para protocolos orientados a mensagens. Em qualquer caso, um código de erro **WSPRecv** de retorno de WSAECONNRESET indica um desligamento anulado.

## <a name="exchanging-user-data-at-shutdown-time"></a>Trocando dados do usuário no momento do desligamento

No momento da desmontagem da conexão, também é possível (para protocolos que dão suporte a isso) para trocar dados de usuário entre os pontos de extremidade. O final que inicia a desmontagem pode chamar [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) para indicar que não é mais possível enviar mais dados e fazer com que a sequência de subdivisão de conexão seja iniciada. Para determinados protocolos, parte dessa sequência de desmontagem é a entrega de dados desconectados do iniciador de desmontagem. Depois de receber o aviso de que a extremidade remota iniciou a sequência de desmontagem (normalmente por meio da \_ indicação de fechamento FD), a função [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) pode ser chamada para receber os dados de desconexão (se houver).

Para ilustrar como os dados de desconexão podem ser usados, considere o cenário a seguir. A metade do cliente de um aplicativo cliente/servidor é responsável por encerrar uma conexão de soquete. Coincidente com o encerramento que ele fornece (por meio de dados de desconexão) o número total de transações processadas com o servidor. O servidor, por sua vez, responde com o total geral cumulativo de transações processadas com todos os clientes. A sequência de chamadas e indicações pode ocorrer conforme mostrado na tabela a seguir.

| Lado do cliente                                                                                                               | Lado do Servidor                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| (1) invoca [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) para concluir a sessão e fornecer o total da transação.            |                                                                                                                                         |
|                                                                                                                           | (2) obtém FD \_ Close ou [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) com um valor de retorno de zero ou WSAEDISCON indicando que o desligamento normal está em andamento. |
|                                                                                                                           | (3) invoca [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) para obter o total da transação do cliente.                                         |
|                                                                                                                           | (4) computa o total geral cumulativo de todas as transações.                                                                                |
|                                                                                                                           | (5) invoca [**WSPSendDisconnect**](/previous-versions/windows/desktop/legacy/ms742290(v=vs.85)) para transmitir total geral.                                                   |
| (6) recebe a \_ indicação de fechamento FD.                                                                                        | (5 ') invoca [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                 |
| (7) invoca [**WSPRecvDisconnect**](/previous-versions/windows/desktop/legacy/ms742285(v=vs.85)) para receber e armazenar o total geral cumulativo de transações. |                                                                                                                                         |
|                                                                                                                           | (8) invoca [ **WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85))                                                                                  |



 

A etapa (5 ') deve seguir a etapa (5), mas não tem relação de tempo com as etapas (6), (7) ou (8).

 

 
