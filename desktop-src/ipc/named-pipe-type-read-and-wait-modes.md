---
description: O servidor de pipe especifica o modo de tipo de pipe, o modo de leitura e o modo de espera no parâmetro dwPipeMode da função CreateNamedPipe. Os clientes de pipe podem especificar esses modos de pipe para seus alças de pipe usando a função CreateFile.
ms.assetid: 07cf9d06-6265-47f4-a9f1-c19c06cc5f9f
title: Tipos de pipe nomeados, modos de leitura e espera
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b8ba69ef0d795747070072511c84abf5a3950db3b9c03ec18973f4d29bbd51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014886"
---
# <a name="named-pipe-type-read-and-wait-modes"></a>Tipos de pipe nomeados, modos de leitura e espera

O servidor de pipe especifica o modo de tipo de pipe, o modo de leitura e o modo de espera no parâmetro *dwPipeMode* da [**função CreateNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) Os clientes de pipe podem especificar esses modos de pipe para seus alças de pipe usando a [**função CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)

## <a name="type-mode"></a>Modo de tipo

O modo de tipo de um pipe determina como os dados são gravados em um pipe nomeado. Os dados podem ser transmitidos por meio de um pipe nomeado como um fluxo de bytes ou como um fluxo de mensagens. O servidor de pipe especifica o tipo de pipe ao chamar [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) para criar uma instância de um pipe nomeado. Os modos de tipo devem ser os mesmos para todas as instâncias de um pipe.

Para criar um pipe de tipo de byte, especifique PIPE \_ TYPE \_ BYTE ou use o valor padrão. Os dados são gravados no pipe como um fluxo de bytes e o sistema não diferencia entre os bytes gravados em operações de gravação diferentes.

Para criar um pipe de tipo de mensagem, especifique PIPE \_ TYPE \_ MESSAGE. O sistema trata os bytes gravados em cada operação de gravação no pipe como uma unidade de mensagem. O sistema sempre executa operações de gravação em pipes de tipo de mensagem como se o modo de write-through estivesse habilitado.

## <a name="read-mode"></a>Modo de Leitura

O modo de leitura de um pipe determina como os dados são lidos de um pipe nomeado. O servidor de pipe especifica o modo de leitura inicial para um identificador de pipe ao [**chamar CreateNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) Os dados podem ser lidos no modo de leitura de byte ou no modo de leitura de mensagem. Um identificador para um pipe de tipo de byte pode estar apenas no modo de leitura de byte. Um identificador para um pipe de tipo de mensagem pode estar no modo de leitura de byte ou de leitura de mensagem. Para um pipe de tipo de mensagem, o modo de leitura pode ser diferente para identificador de servidor e cliente para a mesma instância de pipe.

Para criar a alça de pipe no modo de leitura de byte, especifique PIPE \_ READMODE \_ BYTE ou use o valor padrão. Os dados são lidos do pipe como um fluxo de bytes. Uma operação de leitura é concluída com êxito quando todos os bytes disponíveis no pipe são lidos ou quando o número especificado de bytes é lido.

Para criar a alça de pipe no modo de leitura de mensagem, especifique PIPE \_ READMODE \_ MESSAGE. Os dados são lidos do pipe como um fluxo de mensagens. Uma operação de leitura é concluída com êxito somente quando toda a mensagem é lida. Se o número especificado de bytes a ler for menor que o tamanho da próxima mensagem, a função lerá o máximo possível da mensagem antes de retornar zero (a [**função GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará ERROR \_ MORE \_ DATA). O restante da mensagem pode ser lido usando outra operação de leitura.

Para um cliente de pipe, uma alça de pipe retornada por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) está sempre no modo de leitura de byte inicialmente. Os clientes de pipe e os servidores de pipe podem usar a [**função SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para alterar o modo de leitura de um identificador de pipe. O alça de pipe deve ter o direito de \_ acesso FILE WRITE \_ ATTRIBUTES.

## <a name="wait-mode"></a>Modo de espera

O modo de espera de um identificador de pipe determina como as funções [**ReadFile,**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) lidam com operações demoradas. No modo de espera de bloqueio, as funções aguardam indefinidamente um processo na outra extremidade do pipe para concluir uma operação. No modo de espera sem bloqueio, as funções retornam imediatamente em situações que, de outra forma, exigiriam uma espera indefinido.

Uma [**operação ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) é afetada pelo modo de espera de uma alça de pipe quando o pipe está vazio. Com um alça de espera de bloqueio, a operação não é concluída com êxito até que os dados estão disponíveis em um thread que está sendo escrito na outra extremidade do pipe. Usando um handle nonblocking-wait, a função retorna zero imediatamente e a [**função GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna ERROR \_ NO \_ DATA.

Uma [**operação WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) é afetada pelo modo de espera de uma alça de pipe quando não há espaço suficiente no buffer do pipe. Com um alça de espera de bloqueio, a operação de gravação não poderá ser bem-sucedida até que espaço suficiente seja criado no buffer por uma leitura de thread da outra extremidade do pipe. Com um identificador de espera sem bloqueio, a operação de gravação retorna um valor diferente de zero imediatamente, sem gravar nenhum bytes (para um pipe de tipo de mensagem) ou depois de gravar quantos bytes o buffer contém (para um pipe de tipo byte).

Uma [**operação ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) é afetada pelo modo de espera de um identificador de pipe quando não há nenhum cliente conectado ou aguardando para se conectar à instância de pipe. Com um identificador de espera de bloqueio, a operação de conexão não terá êxito até que um cliente de pipe se conecte à instância de pipe chamando a [**função CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) Com um handle nonblocking-wait, a operação de conexão retorna zero imediatamente e a [**função GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna ERROR \_ PIPE \_ LISTENING.

Por padrão, todos os identificadores de pipe nomeados retornados pela [**função CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) ou [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) são criados com o modo de espera de bloqueio habilitado. Para criar o pipe no modo nonblocking-wait, o servidor de pipe especifica PIPE NOWAIT ao chamar \_ **CreateNamedPipe**.

Os clientes de pipe e os servidores de pipe podem alterar o modo de espera de um identificador de pipe especificando PIPE WAIT ou PIPE NOWAIT em uma chamada para \_ \_ a função [**SetNamedPipeHandleState.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate)

> [!Note]  
> O modo nonblocking-wait tem suporte para compatibilidade com o Microsoft LAN Manager versão 2.0. Esse modo não deve ser usado para obter E/S (entrada e saída) sobrecarradas com pipes nomeados. Em vez disso, a E/S sobrecarroada deve ser usada, pois permite que as operações demoradas sejam executados em segundo plano depois que a função é retornada. Para obter mais informações sobre E/S sobrecarronada, consulte Entrada e saída síncronas e [sobrecarronadas.](synchronous-and-overlapped-input-and-output.md)

 

 

 
