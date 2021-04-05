---
description: O servidor de pipe especifica o modo de tipo de pipe, modo de leitura e modo de espera no parâmetro dwPipeMode da função CreateNamedPipe. Os clientes de pipe podem especificar esses modos de pipe para seus identificadores de pipe usando a função CreateFile.
ms.assetid: 07cf9d06-6265-47f4-a9f1-c19c06cc5f9f
title: Modos de tipo de pipe nomeado, leitura e espera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b116e5ca9357a65a6d63549b96065843b046d479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826790"
---
# <a name="named-pipe-type-read-and-wait-modes"></a>Modos de tipo de pipe nomeado, leitura e espera

O servidor de pipe especifica o modo de tipo de pipe, modo de leitura e modo de espera no parâmetro *dwPipeMode* da função [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) . Os clientes de pipe podem especificar esses modos de pipe para seus identificadores de pipe usando a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

## <a name="type-mode"></a>Modo de tipo

O modo de tipo de um pipe determina como os dados são gravados em um pipe nomeado. Os dados podem ser transmitidos por meio de um pipe nomeado como um fluxo de bytes ou como um fluxo de mensagens. O servidor de pipe especifica o tipo de pipe ao chamar [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) para criar uma instância de um pipe nomeado. Os modos de tipo devem ser os mesmos para todas as instâncias de um pipe.

Para criar um pipe de tipo de byte, especifique \_ \_ o tipo de pipe byte ou use o valor padrão. Os dados são gravados no pipe como um fluxo de bytes, e o sistema não diferencia os bytes gravados em operações de gravação diferentes.

Para criar um pipe de tipo de mensagem, especifique a mensagem de tipo de PIPE \_ \_ . O sistema trata os bytes gravados em cada operação de gravação no pipe como uma unidade de mensagem. O sistema sempre executa operações de gravação em pipes do tipo de mensagem como se o modo de write-through estivesse habilitado.

## <a name="read-mode"></a>Modo de leitura

O modo de leitura de um pipe determina como os dados são lidos de um pipe nomeado. O servidor de pipe especifica o modo de leitura inicial para um identificador de pipe ao chamar [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea). Os dados podem ser lidos no modo de leitura de bytes ou no modo de leitura de mensagem. Um identificador para um pipe de tipo de byte só pode estar no modo de leitura de bytes. Um identificador para um pipe de tipo de mensagem pode estar no modo de leitura de byte ou de leitura de mensagem. Para um pipe de tipo de mensagem, o modo de leitura pode ser diferente para identificadores de servidor e cliente para a mesma instância de pipe.

Para criar o identificador de pipe no modo de leitura de byte, especifique \_ o pipe ReadMode \_ byte ou use o valor padrão. Os dados são lidos do pipe como um fluxo de bytes. Uma operação de leitura foi concluída com êxito quando todos os bytes disponíveis no pipe são lidos ou quando o número especificado de bytes é lido.

Para criar o identificador de pipe no modo de leitura de mensagem, especifique a mensagem de leitura de PIPE \_ \_ . Os dados são lidos do pipe como um fluxo de mensagens. Uma operação de leitura foi concluída com êxito somente quando a mensagem inteira é lida. Se o número especificado de bytes a serem lidos for menor que o tamanho da próxima mensagem, a função lerá o máximo possível da mensagem antes de retornar zero (a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna um erro \_ mais \_ dados). O restante da mensagem pode ser lido usando outra operação de leitura.

Para um cliente de pipe, um identificador de pipe retornado por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) sempre está no modo de leitura de bytes inicialmente. Os clientes de pipe e os servidores de pipe podem usar a função [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para alterar o modo de leitura de um identificador de pipe. O identificador de pipe deve ter o \_ direito de acesso de atributos de gravação de arquivo \_ .

## <a name="wait-mode"></a>Modo de espera

O modo de espera de um identificador de pipe determina como as funções [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) lidam com operações demoradas. No modo de espera de bloqueio, as funções aguardam indefinidamente um processo na outra extremidade do pipe para concluir uma operação. No modo de espera de não bloqueio, as funções retornam imediatamente em situações que, de outra forma, exigiriam uma espera indefinida.

Uma operação [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) é afetada pelo modo de espera de um identificador de pipe quando o pipe está vazio. Com um identificador de espera de bloqueio, a operação não é concluída com êxito até que os dados estejam disponíveis de um thread que esteja gravando na outra extremidade do pipe. Usando um identificador de espera de não bloqueio, a função retorna zero imediatamente e a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna um erro \_ sem \_ dados.

Uma operação [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) é afetada pelo modo de espera de um identificador de pipe quando não há espaço suficiente no buffer do pipe. Com um identificador de espera de bloqueio, a operação de gravação não pode ter sucesso até que espaço suficiente seja criado no buffer por uma leitura de thread a partir da outra extremidade do pipe. Com um identificador de espera de não bloqueio, a operação de gravação retorna um valor diferente de zero imediatamente, sem gravar nenhum byte (para um pipe de tipo de mensagem) ou depois de gravar quantos bytes o buffer mantém (para um pipe de tipo de byte).

Uma operação [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) é afetada pelo modo de espera de um identificador de pipe quando não há nenhum cliente conectado ou esperando para se conectar à instância do pipe. Com um identificador de espera de bloqueio, a operação de conexão não tem sucesso até que um cliente de pipe se conecte à instância de pipe chamando a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) . Com um identificador de espera de não bloqueio, a operação de conexão retorna zero imediatamente e a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna o \_ pipe de erro \_ escutando.

Por padrão, todos os identificadores de pipe nomeado retornados pela função [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) ou [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) são criados com o modo de espera de bloqueio habilitado. Para criar o pipe no modo de espera de não bloqueio, o servidor de pipe especifica o PIPE \_ nowait ao chamar **CreateNamedPipe**.

Os clientes de pipe e os servidores de pipe podem alterar o modo de espera de um identificador de pipe especificando a espera de PIPE \_ ou o pipe \_ nowait em uma chamada para a função [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) .

> [!Note]  
> O modo de espera de não bloqueio tem suporte para compatibilidade com o Microsoft LAN Manager versão 2,0. Esse modo não deve ser usado para obter entrada e saída sobrepostas (e/s) com pipes nomeados. A e/s sobreposta deve ser usada, pois permite que operações demoradas sejam executadas em segundo plano depois que a função retorna. Para obter mais informações sobre e/s sobreposta, consulte [entrada e saída síncrona e sobreposta](synchronous-and-overlapped-input-and-output.md).

 

 

 
