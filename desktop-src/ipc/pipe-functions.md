---
description: A função a seguir é usada com pipes anônimos.
ms.assetid: 9e80783e-9641-4cbd-9c28-a8efe6b9efaa
title: Funções de pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0ef895fe8b987f19f025b6a21ef4c3a5dc3cb24db5458595c25708066e8a78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481600"
---
# <a name="pipe-functions"></a>Funções de pipe

A função a seguir é usada com pipes anônimos.



| Função                         | Descrição                |
|----------------------------------|----------------------------|
| [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) | Cria um pipe anônimo. |



 

As funções a seguir são usadas com pipes nomeados.



| Função                                                                 | Descrição                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea)                                   | Conecta-se a um pipe de tipo de mensagem, grava e lê do pipe e, em seguida, fecha o pipe.                                                                                                                                       |
| [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe)                             | Permite que um processo de servidor de pipe nomeado aguarde até que um processo de cliente se conecte a uma instância de um pipe nomeado.                                                                                                                         |
| [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)                               | Cria uma instância de um pipe nomeado e retorna um identificador para operações de pipe subsequentes. Um processo de cliente se conecta a um pipe nomeado usando a [**função CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) |
| [**DisconnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe)                       | Desconecta a extremidade do servidor de uma instância de pipe nomeada de um processo de cliente.                                                                                                                                                          |
| [**GetNamedPipeClientComputerName**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientcomputernamea) | Recupera o nome do computador cliente para o pipe nomeado especificado.                                                                                                                                                                    |
| [**GetNamedPipeClientProcessId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientprocessid)       | Recupera o identificador de processo do cliente para o pipe nomeado especificado.                                                                                                                                                               |
| [**GetNamedPipeClientSessionId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeclientsessionid)       | Recupera o identificador de sessão do cliente para o pipe nomeado especificado.                                                                                                                                                               |
| [**GetNamedPipeHandleState**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea)               | Recupera informações sobre um pipe nomeado especificado.                                                                                                                                                                                 |
| [**GetNamedPipeInfo**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo)                             | Recupera informações sobre o pipe nomeado especificado.                                                                                                                                                                               |
| [**GetNamedPipeServerProcessId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserverprocessid)       | Recupera o identificador de processo do servidor para o pipe nomeado especificado.                                                                                                                                                               |
| [**GetNamedPipeServerSessionId**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipeserversessionid)       | Recupera o identificador de sessão do servidor para o pipe nomeado especificado.                                                                                                                                                               |
| [**ImpersonateNamedPipeClient**](/windows/desktop/api/namedpipeapi/nf-namedpipeapi-impersonatenamedpipeclient)    | Representa um aplicativo cliente de pipe nomeado.                                                                                                                                                                                       |
| [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe)                                   | Copia dados de um pipe nomeado ou anônimo em um buffer sem removê-los do pipe.                                                                                                                                         |
| [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate)               | Define o modo de leitura e o modo de bloqueio do pipe nomeado especificado.                                                                                                                                                               |
| [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)                           | Combina as funções que escrevem uma mensagem em e leem uma mensagem do pipe nomeado especificado em uma única operação de rede.                                                                                                    |
| [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)                                   | Aguarda até que um intervalo de tempo-out desemita ou uma instância do pipe nomeado especificado está disponível para uma conexão.                                                                                                            |



 

 

 
