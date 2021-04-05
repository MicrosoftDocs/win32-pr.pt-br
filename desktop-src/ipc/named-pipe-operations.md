---
description: As operações de pipe, incluindo clientes e servidores de pipe, podem chamar uma das várias funções — além de CallNamedPipe – para ler e gravar em um pipe nomeado.
ms.assetid: ae06455e-33bc-433d-be8f-aeb8eeb99b1d
title: Operações de pipe nomeado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 703189a129fc44b956ab65c2f70bbf88bfd22700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089866"
---
# <a name="named-pipe-operations"></a>Operações de pipe nomeado

Na primeira vez que o servidor de pipe chama a função [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) , ele usa o parâmetro *nMaxInstances* para especificar o número máximo de instâncias do pipe que podem existir simultaneamente. O servidor pode chamar **CreateNamedPipe** repetidamente para criar instâncias adicionais do pipe, desde que ele não exceda o número máximo de instâncias. Se a função for realizada com sucesso, cada chamada retornará um identificador para a extremidade do servidor de uma instância de pipe nomeado.

Assim que o servidor de pipe cria uma instância de pipe, um cliente de pipe pode se conectar a ela chamando a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) . Se uma instância de pipe estiver disponível, **CreateFile** retornará um identificador para a extremidade do cliente da instância do pipe. Se nenhuma instância do pipe estiver disponível, um cliente de pipe poderá usar a função [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) para aguardar até que um pipe fique disponível.

Um servidor de pipe pode determinar quando um cliente de pipe está conectado a uma instância de pipe chamando a função [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) . Se o identificador de pipe estiver no modo de espera de bloqueio, **ConnectNamedPipe** não retornará até que um cliente esteja conectado.

Clientes e servidores de pipe podem chamar uma das várias funções — além de [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) — para ler e gravar em um pipe nomeado. O comportamento dessas funções depende do tipo de pipe e dos modos em vigor para o identificador de pipe especificado, da seguinte maneira:

-   As funções [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) e [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) podem ser usadas com pipes de tipo byte ou de mensagem.
-   As funções [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) podem ser usadas com pipes de tipo de byte ou de mensagem se o identificador de pipe foi aberto para operações sobrepostas.
-   A função [**PeekNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) pode ser usada para ler sem remover o conteúdo de um pipe de tipo de byte ou um pipe de tipo de mensagem. **PeekNamedPipe** também pode retornar informações adicionais sobre a instância de pipe.
-   A função [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) pode ser usada com pipes duplex do tipo de mensagem se o identificador de pipe para o processo de chamada estiver definido como modo de leitura de mensagem. A função grava uma mensagem de solicitação e lê uma mensagem de resposta em uma única operação, aprimorando o desempenho da rede.

O servidor de pipe não deve executar uma operação de leitura de bloqueio até que o cliente do pipe seja iniciado. Caso contrário, pode ocorrer uma condição de corrida. Isso normalmente ocorre quando o código de inicialização, como o da biblioteca de tempo de execução do C, precisa bloquear e examinar identificadores herdados.

Quando um cliente e um servidor terminarem de usar uma instância de pipe, o servidor deverá primeiro chamar a função [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) para garantir que todos os bytes ou mensagens gravados no pipe sejam lidos pelo cliente. **FlushFileBuffers** não retorna até que o cliente Leia todos os dados do pipe. Em seguida, o servidor chama a função [**DisconnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe) para fechar a conexão com o cliente do pipe. Essa função torna o identificador do cliente inválido, se ele ainda não tiver sido fechado. Todos os dados não lidos no pipe são descartados. Depois que o cliente é desconectado, o servidor chama a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) para fechar seu identificador para a instância de pipe. Como alternativa, o servidor pode usar [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) para permitir que um novo cliente se conecte a essa instância do pipe.

Um processo pode recuperar informações sobre um pipe nomeado chamando a função [**GetNamedPipeInfo**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo) , que retorna o tipo do pipe, o tamanho dos buffers de entrada e saída e o número máximo de instâncias de pipe que podem ser criadas. A função [**GetNamedPipeHandleState**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea) relata os modos de leitura e de espera de um identificador de pipe, o número atual de instâncias de pipe e informações adicionais para pipes que se comunicam através de uma rede. A função [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) define o modo de leitura e os modos de espera de um identificador de pipe. Para clientes de pipe que se comunicam com um servidor remoto, a função também controla o número máximo de bytes a serem coletados ou o tempo máximo de espera antes de transmitir uma mensagem (supondo que o identificador do cliente não foi aberto com o modo write-through habilitado).

 

 
