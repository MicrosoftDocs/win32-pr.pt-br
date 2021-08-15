---
description: Estratégias para a comunicação com vários clientes de pipe e manutenção de várias instâncias de pipe.
ms.assetid: c764bde5-e053-4124-b859-1d2839ada918
title: Instâncias de pipe nomeado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 188ec90912132e5cdd972ac2b0a4ab3f4c1f97ebbb7bc35e20b75b04eebbfa15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481957"
---
# <a name="named-pipe-instances"></a>Instâncias de pipe nomeado

O servidor de pipe mais simples cria uma única instância de um pipe, conecta-se a um único cliente, se comunica com o cliente, desconecta do cliente, fecha o identificador de pipe e termina. No entanto, é mais comum que um servidor de pipe se comunique com vários clientes de pipe. Um servidor de pipe pode usar uma única instância de pipe para se conectar a vários clientes de pipe conectando-se ao e desconectando-se de cada cliente em sequência, mas o desempenho seria ruim. O servidor de pipe deve criar várias instâncias de pipe para lidar com eficiência com vários clientes simultaneamente.

Há três estratégias básicas para atender a várias instâncias de pipe.

-   Crie um thread separado para cada instância do pipe. Para obter um exemplo de um servidor de pipe multi-threaded, consulte [servidor de pipe multi-threaded](multithreaded-pipe-server.md).
-   Use operações sobrepostas especificando uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) nas funções [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) . Para obter um exemplo, consulte [servidor de pipe nomeado usando e/s sobreposta](named-pipe-server-using-overlapped-i-o.md).
-   Use operações sobrepostas usando as funções [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) , que especificam uma rotina de conclusão a ser executada quando a operação for concluída. Para obter um exemplo, consulte [servidor de pipe nomeado usando rotinas de conclusão](named-pipe-server-using-completion-routines.md).

O servidor de pipe multi-threaded é mais fácil de escrever, porque o thread de cada instância lida com comunicações para um único cliente de pipe. O sistema aloca o tempo do processador para cada thread, conforme necessário. Mas cada thread usa recursos do sistema, que é uma desvantagem para um servidor de pipe que lida com um grande número de clientes.

Com um servidor de thread único, é mais fácil coordenar operações que afetam vários clientes e é mais fácil proteger recursos compartilhados de acesso simultâneo por vários clientes. O desafio de um servidor de thread único é que ele requer a coordenação de operações sobrepostas para alocar o tempo do processador para lidar com as necessidades simultâneas dos clientes.

 

 
