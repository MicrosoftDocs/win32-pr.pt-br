---
title: Diretrizes de aplicativo cliente/servidor
description: Aplicativos cliente/servidor não devem assumir que uma única conexão de computador é equivalente a uma única sessão de usuário.
ms.assetid: 69822ef1-eca8-4302-b014-8e5894d52109
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0c1a71256f3ab469bfeb1c08b2d096b56ac1b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105761943"
---
# <a name="clientserver-application-guidelines"></a>Diretrizes de aplicativo cliente/servidor

Aplicativos cliente/servidor não devem assumir que uma única conexão de computador é equivalente a uma única sessão de usuário. Esse é um caso especial do problema discutido em [endereços IP e nomes de computador](ip-addresses-and-computer-names.md).

Para identificar exclusivamente uma conexão de cliente/servidor, cada módulo de cliente deve usar um nome ou identificador exclusivo. Os aplicativos podem usar objetos nomeados ou pipes, soquetes ou outros métodos de IPC. Para obter mais informações, consulte [namespaces de objeto kernel](kernel-object-namespaces.md).

Para ser compatível Serviços de Área de Trabalho Remota, o módulo de servidor em um aplicativo cliente/servidor deve ser capaz de lidar com vários clientes que se conectam a partir do mesmo computador. Para fazer isso, o módulo de servidor deve aceitar conexões de cliente por meio de uma interface global bem definida, como RPC ou pipes nomeados. O servidor e o cliente devem negociar um canal de comunicação diferente para cada sessão de usuário. O cliente deve estabelecer uma conexão com o servidor usando protocolos que dão suporte facilmente a esse tipo de operação, como TCP/IP, em que uma conexão de soquete diferente pode ser usada para cada aplicativo cliente.

O módulo de cliente pode chamar a função [**ProcessIdToSessionId**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-processidtosessionid) para recuperar o identificador de sua sessão de serviços de área de trabalho remota. Em seguida, o cliente usa alguma forma de comunicação entre processos para passar seu identificador de sessão para o módulo de servidor. Os módulos cliente e servidor podem usar o identificador de sessão para configurar um canal de comunicação privada. Por exemplo, o módulo de servidor pode usar um identificador de sessão para acessar objetos no namespace da sessão para objetos kernel.

Além disso, o módulo de servidor pode usar o identificador de sessão em uma chamada [**WTSQuerySessionInformation**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsquerysessioninformationa) para recuperar informações adicionais sobre o cliente. O módulo de servidor também pode usar o identificador de sessão em uma chamada [**WTSSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) para exibir uma mensagem no terminal do cliente. O módulo de servidor também pode criar dois eventos para monitorar a conexão do cliente e a desconexão de uma sessão. No entanto, ele deve ser registrado no servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) para fazer isso. Para obter mais informações, consulte [monitorando conexões de sessão e desconexões](monitoring-session-connections-and-disconnections.md).

Prompts para entrada do usuário são uma fonte potencial de problemas para aplicativos cliente/servidor. Por exemplo, se um serviço chamar a função [**MessageBox**](/windows/desktop/api/winuser/nf-winuser-messagebox) , a caixa de mensagem será exibida na área de trabalho do servidor de host da Sessão RD, não na área de trabalho cliente. Para exibir uma mensagem em uma área de trabalho cliente, o serviço pode chamar a função [**WtsSendMessage**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtssendmessagea) . Como alternativa, o serviço pode solicitar entrada do módulo do cliente e o módulo do cliente pode exibir a interface do usuário e enviar a entrada resultante de volta para o serviço.

Os processos gerados de várias sessões podem enviar dados e receber dados uns dos outros por meio do uso de blocos de memória compartilhada. Para obter mais informações, consulte [criando memória compartilhada nomeada](/windows/desktop/Memory/creating-named-shared-memory). A memória compartilhada não pode ser usada sob as seguintes condições:

-   Os processos que usam o bloco de memória compartilhada foram gerados por várias sessões.
-   As sessões compartilham a mesma credencial de autenticação de usuário.

 

 