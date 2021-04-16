---
title: Sobre Serviços de Área de Trabalho Remota
description: O Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) fornece uma funcionalidade semelhante a um ambiente baseado em terminal, host centralizado ou mainframe, no qual vários terminais se conectam a um computador host.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4644170cfca3b4bacdd6db647e35549d56844e9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761335"
---
# <a name="about-remote-desktop-services"></a>Sobre Serviços de Área de Trabalho Remota

O Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) fornece uma funcionalidade semelhante a um ambiente baseado em terminal, host centralizado ou mainframe, no qual vários terminais se conectam a um computador host. Cada terminal fornece um canal para entrada e saída entre um usuário e o computador host. Um usuário pode fazer logon em um terminal e, em seguida, executar aplicativos no computador host, acessar arquivos, bancos de dados, recursos de rede e assim por diante. Cada sessão de terminal é independente, com o sistema operacional do host que gerencia conflitos entre vários usuários que contendem recursos compartilhados.

A principal diferença entre Serviços de Área de Trabalho Remota e o ambiente de mainframe tradicional é que os terminais inconsistentes em um ambiente de mainframe fornecem apenas entrada e saída baseadas em caractere. Um cliente de Conexão de Área de Trabalho Remota (RDC) ou emulador fornece uma interface gráfica completa do usuário, incluindo uma área de trabalho do sistema operacional Windows e suporte para uma variedade de dispositivos de entrada, como um teclado e um mouse.

No ambiente de Serviços de Área de Trabalho Remota, um aplicativo é executado inteiramente no servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) (anteriormente conhecido como servidor de terminal). O cliente RDC não executa nenhum processamento local de software de aplicativo. O servidor transmite a interface gráfica do usuário para o cliente. O cliente transmite a entrada do usuário de volta para o servidor.

Para obter mais informações, consulte os tópicos a seguir.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Modificar o padrão de redirecionamento de dispositivo](modify-device-redirection-default-.md)
</dt> <dd>

Como Área de Trabalho Remota servidores de gateway tentam impor políticas de redirecionamento de dispositivo seguro antes de passar a conexão do cliente para um servidor Host da Sessão da Área de Trabalho Remota, talvez seja necessário desabilitar esse padrão em alguns casos.

</dd> <dt>

[Protocolo RDP](remote-desktop-protocol.md)
</dt> <dd>

O protocolo de Área de Trabalho Remota da Microsoft (RDP) fornece recursos de exibição e entrada remotos em conexões de rede para aplicativos baseados no Windows em execução em um servidor.

</dd> <dt>

[API de Serviços de Área de Trabalho Remota](terminal-services-api.md)
</dt> <dd>

A API Serviços de Área de Trabalho Remota é principalmente útil para aplicativos cliente/servidor e aplicativos para administração de Serviços de Área de Trabalho Remota.

</dd> <dt>

[Serviços de Área de Trabalho Remota aplicativos de gerenciamento](terminal-services-management-applications.md)
</dt> <dd>

Descreve os aplicativos de gerenciamento aos quais Serviços de Área de Trabalho Remota dá suporte.

</dd> <dt>

[Diretrizes de programação de Serviços de Área de Trabalho Remota](terminal-services-programming-guidelines.md)
</dt> <dd>

Tópicos que fornecem diretrizes para o desenvolvimento de aplicativos em um ambiente Serviços de Área de Trabalho Remota.

</dd> <dt>

[Sessões de Área de Trabalho Remota](terminal-services-sessions.md)
</dt> <dd>

Como cada logon em um cliente de Conexão de Área de Trabalho Remota (RDC) recebe uma ID de sessão separada, a experiência do usuário é semelhante a ser conectada a vários computadores ao mesmo tempo; por exemplo, um computador do escritório e um computador doméstico.

</dd> <dt>

[Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection.md)
</dt> <dd>

Descreve como instalar um Conexão Web de Área de Trabalho Remota.

</dd> <dt>

[Recursos em um servidor Host da Sessão da Área de Trabalho Remota](resources-on-a-terminal-server.md)
</dt> <dd>

Vários usuários podem fazer logon simultaneamente em um único servidor de Host da Sessão RD, compartilhando os recursos de hardware e software do servidor.

</dd> <dt>

[O que há de novo no Serviços de Área de Trabalho Remota](what-s-new-in-terminal-services.md)
</dt> <dd>

Tópicos que descrevem as alterações em cada versão da API de Serviços de Área de Trabalho Remota.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conectar-se a outro computador usando Conexão de Área de Trabalho Remota](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




