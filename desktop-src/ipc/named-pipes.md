---
description: Um pipe nomeado é um pipe nomeado, unidirecional ou bidirecional para comunicação entre o servidor de pipe e um ou mais clientes de pipe.
ms.assetid: 7a4c11ac-14c0-4a93-b72e-02fb8852cc15
title: Pipes nomeados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0675244e09b7c202b4fa6b67f6268392b1b260f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921869"
---
# <a name="named-pipes"></a>Pipes nomeados

Um *pipe nomeado* é um pipe nomeado, unidirecional ou bidirecional para comunicação entre o servidor de pipe e um ou mais clientes de pipe. Todas as instâncias de um pipe nomeado compartilham o mesmo nome de pipe, mas cada instância tem seus próprios buffers e identificadores e fornece um canal separado para comunicação de cliente/servidor. O uso de instâncias permite que vários clientes de pipe usem o mesmo pipe nomeado simultaneamente.

Qualquer processo pode acessar pipes nomeados, sujeito a verificações de segurança, tornando os pipes nomeados uma forma fácil de comunicação entre processos relacionados ou não relacionados.

Qualquer processo pode atuar como um servidor e um cliente, tornando possível a comunicação ponto a ponto. Conforme usado aqui, o servidor de pipe de termo se refere a um processo que cria um pipe nomeado e o cliente de pipe de termo refere-se a um processo que se conecta a uma instância de um pipe nomeado. A função do lado do servidor para instanciar um pipe nomeado é [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea). A função do lado do servidor para aceitar uma conexão é [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe). Um processo de cliente se conecta a um pipe nomeado usando a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) .

Pipes nomeados podem ser usados para fornecer comunicação entre processos no mesmo computador ou entre processos em computadores diferentes em uma rede. Se o serviço do servidor estiver em execução, todos os pipes nomeados poderão ser acessados remotamente. Se você pretende usar apenas um pipe nomeado localmente, negue o acesso à rede de Autoridade NT \\ ou alterne para o RPC local.

Para mais informações, consulte os seguintes tópicos:

-   [Nomes de pipe](pipe-names.md)
-   [Modos abertos do pipe nomeado](named-pipe-open-modes.md)
-   [Modos de tipo de pipe nomeado, leitura e espera](named-pipe-type-read-and-wait-modes.md)
-   [Instâncias de pipe nomeado](named-pipe-instances.md)
-   [Operações de pipe nomeado](named-pipe-operations.md)
-   [Entrada e saída síncronas e sobrepostas](synchronous-and-overlapped-input-and-output.md)
-   [Segurança de pipe nomeado e direitos de acesso](named-pipe-security-and-access-rights.md)
-   [Representando um cliente de pipe nomeado](impersonating-a-named-pipe-client.md)
-   [Usando pipes](using-pipes.md)

 

 
