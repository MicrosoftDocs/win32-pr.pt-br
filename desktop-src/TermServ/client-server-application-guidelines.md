---
title: Diretrizes de aplicativo cliente/servidor
description: Aplicativos cliente/servidor não devem assumir que uma única conexão de computador é equivalente a uma única sessão de usuário.
ms.assetid: 69822ef1-eca8-4302-b014-8e5894d52109
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d27f5bd024e2311307f39e4f86584747b59b874576e5cd5aa28e735b2945d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001614"
---
# <a name="clientserver-application-guidelines"></a>Diretrizes de aplicativo cliente/servidor

Aplicativos cliente/servidor não devem assumir que uma única conexão de computador é equivalente a uma única sessão de usuário. Esse é um caso especial do problema discutido em Endereços [IP e Nomes de Computador.](ip-addresses-and-computer-names.md)

Para identificar exclusivamente uma conexão de cliente/servidor, cada módulo cliente deve usar um nome ou identificador exclusivo. Os aplicativos podem usar objetos nomeados, pipes, soquetes ou outros métodos IPC. Para obter mais informações, consulte [Namespaces de objeto kernel](kernel-object-namespaces.md).

Para ser Serviços de Área de Trabalho Remota, o módulo de servidor em um aplicativo cliente/servidor deve ser capaz de lidar com vários clientes que se conectam do mesmo computador. Para fazer isso, o módulo de servidor deve aceitar conexões de cliente por meio de uma interface global bem definida, como RPC ou pipes nomeados. O servidor e o cliente devem negociar um canal de comunicação diferente para cada sessão do usuário. O cliente deve estabelecer uma conexão com o servidor usando protocolos que facilmente suportam esse tipo de operação, como TCP/IP, em que uma conexão de soquete diferente pode ser usada para cada aplicativo cliente.

O módulo cliente pode chamar a [**função ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) para recuperar o identificador de sua Serviços de Área de Trabalho Remota sessão. Em seguida, o cliente usa alguma forma de comunicação entre processos para passar seu identificador de sessão para o módulo do servidor. Os módulos de cliente e servidor podem usar o identificador de sessão para configurar um canal de comunicação privado. Por exemplo, o módulo de servidor pode usar um identificador de sessão para acessar objetos no namespace da sessão para objetos kernel.

Além disso, o módulo do servidor pode usar o identificador de sessão em [**uma chamada WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) para recuperar informações adicionais sobre o cliente. O módulo do servidor também pode usar o identificador de sessão em [**uma chamada WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) para exibir uma mensagem no terminal do cliente. O módulo de servidor também pode criar dois eventos para monitorar a conexão do cliente com e a desconexão de uma sessão. No entanto, ele deve ser registrado no Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) para fazer isso. Para obter mais informações, consulte [Monitoramento de conexões de sessão e desconexões](monitoring-session-connections-and-disconnections.md).

Os prompts de entrada do usuário são uma possível fonte de problemas para aplicativos cliente/servidor. Por exemplo, se um serviço chamar a função [**MessageBox,**](/windows/desktop/api/winuser/nf-winuser-messagebox) a caixa de mensagem será exibida na área de trabalho do servidor Host da Sessão RD, não na área de trabalho do cliente. Para exibir uma mensagem em uma área de trabalho cliente, o serviço pode chamar a [**função WtsSendMessage.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) Como alternativa, o serviço pode solicitar a entrada do módulo cliente e o módulo cliente pode exibir a interface do usuário e enviar a entrada resultante de volta para o serviço.

Processos gerados de várias sessões podem enviar dados e receber dados uns dos outros por meio do uso de blocos de memória compartilhados. Para obter mais informações, consulte [Criando memória compartilhada nomeada.](/windows/desktop/Memory/creating-named-shared-memory) A memória compartilhada não pode ser usada sob as seguintes condições:

-   Os processos que usam o bloco de memória compartilhada foram gerados por várias sessões.
-   As sessões compartilham a mesma credencial de autenticação de usuário.

 

 