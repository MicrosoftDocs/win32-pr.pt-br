---
title: Serviços de Área de Trabalho Remota (Serviços de Área de Trabalho Remota)
description: Área de Trabalho Remota da Microsoft Serviços é um software de acesso de computador remoto que dá suporte ao acesso à área de trabalho remota. Serviços de Área de Trabalho Remota conecta vários clientes a um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota home page
- Serviços de terminal consulte Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525f62433c10c8c4f750a8ae1abbfa9496f2f096139c182a677c9dbf69ce4a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999896"
---
# <a name="remote-desktop-services-remote-desktop-services"></a>Serviços de Área de Trabalho Remota (Serviços de Área de Trabalho Remota)

## <a name="purpose"></a>Finalidade

Windows Server 2012 r2, Windows Server 2012, Windows server 2008 R2 ou Windows server 2008 com Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de Terminal) permitem que um servidor hospede várias sessões de cliente simultâneas. Área de Trabalho Remota usa a tecnologia Serviços de Área de Trabalho Remota para permitir que uma única sessão seja executada remotamente. Um usuário pode se conectar a um servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) (anteriormente conhecido como servidor de terminal) usando o software cliente do Conexão de Área de Trabalho Remota (RDC). A Conexão Web de Área de Trabalho Remota estende Serviços de Área de Trabalho Remota tecnologia à Web.

> [!Note]  
> Este tópico destina-se a desenvolvedores de software. Se você estiver procurando informações do usuário para Área de Trabalho Remota conexões, consulte [conexão de área de trabalho remota: perguntas](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8)frequentes.

 

## <a name="where-applicable"></a>Quando aplicável

Um cliente Conexão de Área de Trabalho Remota (RDC) pode existir em uma variedade de formulários. dispositivos de hardware de cliente fino que executam um sistema operacional incorporado baseado em Windows podem executar o software cliente do RDC para se conectar a um servidor Host da Sessão RD. computadores com Windows, Macintosh ou UNIX podem executar o software cliente do RDC para se conectar a um servidor Host da Sessão RD para exibir aplicativos baseados em Windows. essa combinação de clientes RDC fornece acesso a aplicativos baseados em Windows de praticamente qualquer sistema operacional.

## <a name="developer-audience"></a>Público de desenvolvedores

os desenvolvedores que usam Serviços de Área de Trabalho Remota devem estar familiarizados com as linguagens de programação C e C++ e o ambiente de programação baseado em Windows. É necessário ter familiaridade com a arquitetura de cliente/servidor. O Conexão Web de Área de Trabalho Remota inclui interfaces programáveis para criar e implantar canais virtuais programáveis em Serviços de Área de Trabalho Remota aplicativos Web.

## <a name="run-time-requirements"></a>Requisitos de tempo de execução

os aplicativos que usam Serviços de Área de Trabalho Remota exigem Windows Server 2012 r2, Windows 8.1, Windows Server 2012, Windows 8, Windows server 2008 R2, Windows 7, Windows Server 2008 ou Windows Vista. Para usar Conexão Web de Área de Trabalho Remota funcionalidade, o aplicativo cliente Serviços de Área de Trabalho Remota requer o Internet Explorer e uma conexão com o World Wide Web. Para obter informações sobre os requisitos de tempo de execução para um determinado elemento de programação, consulte a seção requisitos da página de referência para esse elemento.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[controle de ActiveX de Área de Trabalho Remota](remote-desktop-activex-control.md)
</dt> <dd>

descreve como usar o controle de ActiveX de Área de Trabalho Remota.

</dd> <dt>

[API do provedor de protocolo RDP](custom-remote-desktop-protocols.md)
</dt> <dd>

Você usa a API do provedor de protocolo RDP para criar um protocolo para fornecer comunicação entre o serviço de Serviços de Área de Trabalho Remota e vários clientes.

</dd> <dt>

[Canais virtuais Serviços de Área de Trabalho Remota](terminal-services-virtual-channels.md)
</dt> <dd>

Os *canais virtuais* são extensões de software que podem ser usadas para adicionar aprimoramentos funcionais a um aplicativo serviços de área de trabalho remota.

</dd> <dt>

[RemoteFX API de redirecionamento de mídia](remotefx-api.md)
</dt> <dd>

a API de redirecionamento de mídia RemoteFX é usada em uma sessão de Área de Trabalho Remota para identificar áreas do servidor que estão exibindo conteúdo de alteração rápida, como vídeo. Esse conteúdo pode então ser codificado em vídeo e enviado ao cliente em formato codificado.

</dd> <dt>

[API de cliente do agente de Conexão de Área de Trabalho Remota](connection-broker-client-api.md)
</dt> <dd>

Descreve como usar a API de cliente do agente do Conexão de Área de Trabalho Remota.

</dd> <dt>

[Referência de API do agente de tarefa de área de trabalho pessoal](task-agent-api-reference.md)
</dt> <dd>

A API do agente de tarefa de área de trabalho pessoal é usada para lidar com atualizações agendadas em uma área de trabalho virtual pessoal.

</dd> <dt>

[Sobre Serviços de Área de Trabalho Remota](about-terminal-services.md)
</dt> <dd>

O Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) fornece uma funcionalidade semelhante a um ambiente baseado em terminal, host centralizado ou mainframe, no qual vários terminais se conectam a um computador host.

</dd> <dt>

[Provedor de serviços de gerenciamento de Área de Trabalho Remota](rdms-api-reference.md)
</dt> <dd>

O provedor de serviços de gerenciamento de Área de Trabalho Remota (RDMS) gerencia ambientes de VDI (Virtual Desktop Infrastructure).

</dd> <dt>

[Referência de Serviços de Área de Trabalho Remota](terminal-services-reference.md)
</dt> <dd>

Documentação dos métodos de propriedade que você pode usar para examinar e configurar Serviços de Área de Trabalho Remota Propriedades de usuário. Serviços de Área de Trabalho Remota funções, estruturas e Conexão Web de Área de Trabalho Remota interfaces programáveis por script também são documentadas.

</dd> <dt>

[Teclas de atalho Serviços de Área de Trabalho Remota](terminal-services-shortcut-keys.md)
</dt> <dd>

Uma lista de teclas de atalho Serviços de Área de Trabalho Remota.

</dd> <dt>

[Provedor WMI de Serviços de Área de Trabalho Remota](terminal-services-wmi-provider.md)
</dt> <dd>

O provedor WMI de Serviços de Área de Trabalho Remota fornece acesso programático às informações e configurações que são expostas pelo snap-in do MMC (console de gerenciamento Microsoft) Serviços de Área de Trabalho Remota de configuração/conexões.

</dd> <dt>

[Usando Serviços de Área de Trabalho Remota](using-terminal-services.md)
</dt> <dd>

Como programar no ambiente de Serviços de Área de Trabalho Remota e como estender a tecnologia Serviços de Área de Trabalho Remota (anteriormente conhecida como serviços de terminal) para a Web usando Conexão Web de Área de Trabalho Remota.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Os serviços de terminal agora estão Serviços de Área de Trabalho Remota](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




