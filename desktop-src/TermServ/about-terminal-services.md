---
title: Sobre Serviços de Área de Trabalho Remota
description: Serviços de Área de Trabalho Remota (anteriormente conhecido como Serviços de Terminal) fornece funcionalidade semelhante a um ambiente baseado em terminal, host centralizado ou mainframe, no qual vários terminais se conectam a um computador host.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota , sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680ccae3d8944c92d64da526831142d662ac5dc38157c741cf8f5426768fc745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681456"
---
# <a name="about-remote-desktop-services"></a>Sobre Serviços de Área de Trabalho Remota

Serviços de Área de Trabalho Remota (anteriormente conhecido como Serviços de Terminal) fornece funcionalidade semelhante a um ambiente baseado em terminal, host centralizado ou mainframe, no qual vários terminais se conectam a um computador host. Cada terminal fornece um canal para entrada e saída entre um usuário e o computador host. Um usuário pode fazer logoff em um terminal e, em seguida, executar aplicativos no computador host, acessando arquivos, bancos de dados, recursos de rede e assim por diante. Cada sessão de terminal é independente, com o sistema operacional host gerenciando conflitos entre vários usuários que estão contenção de recursos compartilhados.

A principal diferença entre Serviços de Área de Trabalho Remota e o ambiente de mainframe tradicional é que os terminais insuportários em um ambiente de mainframe fornecem apenas entrada e saída baseadas em caracteres. Um cliente ou emulador RDC (Conexão de Área de Trabalho Remota) fornece uma interface gráfica do usuário completa, incluindo uma área de trabalho do sistema operacional do Windows e suporte para uma variedade de dispositivos de entrada, como um teclado e mouse.

No ambiente Serviços de Área de Trabalho Remota, um aplicativo é executado inteiramente no servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) (anteriormente conhecido como servidor terminal). O cliente RDC não executa nenhum processamento local do software de aplicativo. O servidor transmite a interface gráfica do usuário para o cliente. O cliente transmite a entrada do usuário de volta para o servidor.

Para obter mais informações, consulte estes tópicos.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Modificar o padrão de redirecionamento de dispositivo](modify-device-redirection-default-.md)
</dt> <dd>

Como Área de Trabalho Remota gateway de gateway tentam impor políticas de redirecionamento de dispositivo seguras antes de passar a conexão do cliente para um servidor Host da Sessão da Área de Trabalho Remota, talvez seja necessário desabilitar esse padrão em alguns casos.

</dd> <dt>

[Protocolo RDP](remote-desktop-protocol.md)
</dt> <dd>

O protocolo Área de Trabalho Remota da Microsoft (RDP) fornece recursos remotos de exibição e entrada em conexões de rede para Windows aplicativos baseados em execução em um servidor.

</dd> <dt>

[API do Serviços de Área de Trabalho Remota](terminal-services-api.md)
</dt> <dd>

A API Serviços de Área de Trabalho Remota é útil principalmente para aplicativos e aplicativos de cliente/servidor para Serviços de Área de Trabalho Remota administração.

</dd> <dt>

[Serviços de Área de Trabalho Remota de gerenciamento](terminal-services-management-applications.md)
</dt> <dd>

Descreve os aplicativos de gerenciamento aos Serviços de Área de Trabalho Remota compatíveis.

</dd> <dt>

[Serviços de Área de Trabalho Remota diretrizes de programação](terminal-services-programming-guidelines.md)
</dt> <dd>

Tópicos que fornecem diretrizes para o desenvolvimento de aplicativos em Serviços de Área de Trabalho Remota ambiente.

</dd> <dt>

[Área de Trabalho Remota sessões](terminal-services-sessions.md)
</dt> <dd>

Como cada logon para um cliente RDC (Conexão de Área de Trabalho Remota) recebe uma ID de sessão separada, a experiência do usuário é semelhante a estar conectado a vários computadores ao mesmo tempo; por exemplo, um computador office e um computador home.

</dd> <dt>

[Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection.md)
</dt> <dd>

Descreve como instalar um Conexão Web de Área de Trabalho Remota.

</dd> <dt>

[Recursos em um Host da Sessão da Área de Trabalho Remota Server](resources-on-a-terminal-server.md)
</dt> <dd>

Vários usuários podem fazer logoff simultaneamente em um único Host da Sessão RD, compartilhando os recursos de hardware e software do servidor.

</dd> <dt>

[Novidades no Serviços de Área de Trabalho Remota](what-s-new-in-terminal-services.md)
</dt> <dd>

Tópicos que descrevem as alterações em cada versão da API Serviços de Área de Trabalho Remota.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conexão outro computador usando Conexão de Área de Trabalho Remota](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




