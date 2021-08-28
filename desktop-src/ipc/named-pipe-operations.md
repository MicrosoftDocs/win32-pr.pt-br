---
description: As operações de pipe, incluindo clientes de pipe e servidores, podem chamar uma das várias funções , além de CallNamedPipe, para ler e gravar em um pipe nomeado.
ms.assetid: ae06455e-33bc-433d-be8f-aeb8eeb99b1d
title: Operações de pipe nomeadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21bc389071a2861754b5d71659ec3cb836204c631a75de67565933f28e8632c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602146"
---
# <a name="named-pipe-operations"></a>Operações de pipe nomeadas

Na primeira vez que o servidor de pipe chama a função [**CreateNamedPipe,**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) ele usa o parâmetro *nMaxInstances* para especificar o número máximo de instâncias do pipe que podem existir simultaneamente. O servidor pode chamar **CreateNamedPipe** repetidamente para criar instâncias adicionais do pipe, desde que ele não exceda o número máximo de instâncias. Se a função for bem-sucedida, cada chamada retornará um identificador para a extremidade do servidor de uma instância de pipe nomeada.

Assim que o servidor de pipe cria uma instância de pipe, um cliente de pipe pode se conectar a ela chamando a [**função CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) Se uma instância de pipe estiver disponível, **CreateFile** retornará um alçado para a extremidade do cliente da instância de pipe. Se nenhuma instância do pipe estiver disponível, um cliente de pipe poderá usar a função [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) para aguardar até que um pipe fique disponível.

Um servidor de pipe pode determinar quando um cliente de pipe está conectado a uma instância de pipe chamando a [**função ConnectNamedPipe.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) Se o identificador de pipe estiver no modo de espera de bloqueio, **ConnectNamedPipe** não retornará até que um cliente esteja conectado.

Os clientes e servidores de pipe podem chamar uma das várias funções , além de [**CallNamedPipe,**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) para ler e gravar em um pipe nomeado. O comportamento dessas funções depende do tipo de pipe e dos modos em vigor para o identificador de pipe especificado, da seguinte forma:

-   As [**funções ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**e WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) podem ser usadas com pipes de tipo de byte ou de tipo de mensagem.
-   As [**funções ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) poderão ser usadas com pipes de tipo de byte ou de tipo de mensagem se o identificador de pipe tiver sido aberto para operações sobrecarradas.
-   A [**função PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) pode ser usada para ler sem remover o conteúdo de um pipe de tipo de byte ou um pipe de tipo de mensagem. **PeekNamedPipe** também pode retornar informações adicionais sobre a instância de pipe.
-   A [**função TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) poderá ser usada com pipes duplex de tipo de mensagem se o identificador de pipe para o processo de chamada estiver definido como modo de leitura de mensagem. A função grava uma mensagem de solicitação e lê uma mensagem de resposta em uma única operação, aprimorando o desempenho da rede.

O servidor de pipe não deve executar uma operação de leitura de bloqueio até que o cliente de pipe seja iniciado. Caso contrário, uma condição de corrida pode ocorrer. Isso normalmente ocorre quando o código de inicialização, como o da biblioteca em tempo de executar C, precisa bloquear e examinar os alças herdados.

Quando um cliente e um servidor terminam de usar uma instância de pipe, o servidor deve primeiro chamar a função [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) para garantir que todos os bytes ou mensagens gravados no pipe sejam lidos pelo cliente. **FlushFileBuffers** não retorna até que o cliente tenha lido todos os dados do pipe. Em seguida, o servidor chama [**a função DisconnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe) para fechar a conexão com o cliente de pipe. Essa função torna o handle do cliente inválido, se ele ainda não tiver sido fechado. Todos os dados não lidos no pipe são descartados. Depois que o cliente é desconectado, o servidor chama a [**função CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para fechar seu handle para a instância de pipe. Como alternativa, o servidor pode usar [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) para habilitar um novo cliente a se conectar a essa instância do pipe.

Um processo pode recuperar informações sobre um pipe nomeado chamando a função [**GetNamedPipeInfo,**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo) que retorna o tipo do pipe, o tamanho dos buffers de entrada e saída e o número máximo de instâncias de pipe que podem ser criadas. A [**função GetNamedPipeHandleState**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea) relata os modos de leitura e espera de um identificador de pipe, o número atual de instâncias de pipe e informações adicionais para pipes que se comunicam por uma rede. A [**função SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) define os modos de leitura e espera de um identificador de pipe. Para clientes de pipe que se comunicam com um servidor remoto, a função também controla o número máximo de bytes a coletar ou o tempo máximo de espera antes de transmitir uma mensagem (supondo que o handle do cliente não tenha sido aberto com o modo de gravação habilitado).

 

 
