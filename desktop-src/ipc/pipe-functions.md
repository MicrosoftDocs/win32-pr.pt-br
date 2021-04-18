---
description: A função a seguir é usada com Pipes anônimos.
ms.assetid: 9e80783e-9641-4cbd-9c28-a8efe6b9efaa
title: Funções de pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2413157ca76af56b5344327e1d3a9e93f86253f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781310"
---
# <a name="pipe-functions"></a>Funções de pipe

A função a seguir é usada com Pipes anônimos.



| Função                         | Descrição                |
|----------------------------------|----------------------------|
| [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) | Cria um pipe anônimo. |



 

As funções a seguir são usadas com pipes nomeados.



| Função                                                                 | Descrição                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea)                                   | Conecta-se a um pipe do tipo mensagem, grava e lê a partir do pipe e fecha o pipe.                                                                                                                                       |
| [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)                             | Permite que um processo de servidor de pipe nomeado aguarde até que um processo de cliente se conecte a uma instância de um pipe nomeado.                                                                                                                         |
| [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)                               | Cria uma instância de um pipe nomeado e retorna um identificador para operações de pipe subsequentes. Um processo de cliente se conecta a um pipe nomeado usando a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) . |
| [**DisconnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe)                       | Desconecta a extremidade do servidor de uma instância de pipe nomeado de um processo de cliente.                                                                                                                                                          |
| [**GetNamedPipeClientComputerName**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientcomputernamea) | Recupera o nome do computador cliente para o pipe nomeado especificado.                                                                                                                                                                    |
| [**GetNamedPipeClientProcessId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientprocessid)       | Recupera o identificador do processo de cliente para o pipe nomeado especificado.                                                                                                                                                               |
| [**GetNamedPipeClientSessionId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientsessionid)       | Recupera o identificador de sessão de cliente para o pipe nomeado especificado.                                                                                                                                                               |
| [**GetNamedPipeHandleState**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea)               | Recupera informações sobre um pipe nomeado especificado.                                                                                                                                                                                 |
| [**GetNamedPipeInfo**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo)                             | Recupera informações sobre o pipe nomeado especificado.                                                                                                                                                                               |
| [**GetNamedPipeServerProcessId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserverprocessid)       | Recupera o identificador de processo do servidor para o pipe nomeado especificado.                                                                                                                                                               |
| [**GetNamedPipeServerSessionId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserversessionid)       | Recupera o identificador de sessão de servidor para o pipe nomeado especificado.                                                                                                                                                               |
| [**ImpersonateNamedPipeClient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient)    | Representa um aplicativo cliente de pipe nomeado.                                                                                                                                                                                       |
| [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe)                                   | Copia dados de um pipe nomeado ou anônimo para um buffer sem removê-lo do pipe.                                                                                                                                         |
| [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate)               | Define o modo de leitura e o modo de bloqueio do pipe nomeado especificado.                                                                                                                                                               |
| [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)                           | Combina as funções que gravam uma mensagem e lêem uma mensagem do pipe nomeado especificado em uma única operação de rede.                                                                                                    |
| [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)                                   | Aguarda até que um intervalo de tempo limite seja decorrido ou uma instância do pipe nomeado especificado esteja disponível para uma conexão.                                                                                                            |



 

 

 
