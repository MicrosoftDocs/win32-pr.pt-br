---
title: Usando Serviços de Área de Trabalho Remota
description: Como programar no ambiente de Serviços de Área de Trabalho Remota e como estender a tecnologia Serviços de Área de Trabalho Remota (anteriormente conhecida como serviços de terminal) para a Web usando Conexão Web de Área de Trabalho Remota.
ms.assetid: 17a8055c-3fde-4ba0-9ed9-af0ebe0a36b9
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, usando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7d0af90aef8eed3c8b9dc397f86cb6940a79e8e399af201ff854cbfaba3ff3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868766"
---
# <a name="using-remote-desktop-services"></a>Usando Serviços de Área de Trabalho Remota

As seções a seguir descrevem como programar no ambiente de Serviços de Área de Trabalho Remota e como estender a tecnologia Serviços de Área de Trabalho Remota (anteriormente conhecida como serviços de terminal) para a Web usando Conexão Web de Área de Trabalho Remota. se você estiver procurando informações do usuário para Área de Trabalho Remota conexões, consulte [Conexão para outro computador usando Conexão de Área de Trabalho Remota](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7).

> [!Note]  
> Este tópico destina-se a desenvolvedores de software.

 

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[Detectando se a função de Serviços de Área de Trabalho Remota está instalada](detecting-whether-terminal-services-is-installed.md)
</dt> <dd>

exemplo de código C# que mostra um método que retorna **True** se a função de servidor Serviços de Área de Trabalho Remota estiver instalada e em execução ou **false** caso contrário, começando com Windows server 2008.

</dd> <dt>

[Extensão do agente de sessão dos serviços de terminal](extending-ts-session-broker.md)
</dt> <dd>

Você pode estender o agente de Sessão TS usando a interface com do [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) .

</dd> <dt>

[Implementando um enumerador de ponto de extremidade de áudio personalizado](implementing-an-audio-endpoint-enumerator.md)
</dt> <dd>

a partir do Windows Server 2008 R2, você pode implementar um enumerador personalizado de ponto de extremidade de áudio remoto como parte de um provedor de protocolo de Área de Trabalho Remota.

</dd> <dt>

[Monikers de sessão](session-monikers.md)
</dt> <dd>

O COM distribuído (DCOM) permite a ativação de objeto por sessão usando um moniker de sessão fornecido pelo sistema.

</dd> <dt>

[Usando a extensão ADSI para Serviços de Área de Trabalho Remota configuração de usuário](using-the-adsi-extension-for-terminal-services-user-configuration.md)
</dt> <dd>

A administração de propriedades de usuário específicas de Serviços de Área de Trabalho Remota é possível usando os métodos implementados pela extensão ADSI (Active Directory Service Interfaces), que é empacotada com a biblioteca de vínculo dinâmico Tsuserex.dll.

</dd> <dt>

[Usando a API de Serviços de Área de Trabalho Remota](using-the-terminal-services-api.md)
</dt> <dd>

Descreve como você pode usar a API Serviços de Área de Trabalho Remota para permitir que os aplicativos executem tarefas em um ambiente Serviços de Área de Trabalho Remota.

</dd> <dt>

[Usando a API de virtualização Área de Trabalho Remota](using-the-remote-desktop-virtualization-api.md)
</dt> <dd>

Os desenvolvedores podem usar essa API para personalizar a lógica que o Conexão de Área de Trabalho Remota Broker (agente de conexão de área de trabalho remota) usa para determinar o melhor destino para uma conexão de cliente de entrada.

</dd> <dt>

[Interface WSDL para soluções de VDI personalizadas](wsdl-interface-for-custom-vdi-solutions.md)
</dt> <dd>

Os desenvolvedores podem criar serviços Web personalizados que gerenciam soluções de VDI (Virtual Desktop Infrastructure).

</dd> </dl>

Para obter mais informações, consulte [diretrizes de programação de serviços de área de trabalho remota](terminal-services-programming-guidelines.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Os serviços de terminal agora estão Serviços de Área de Trabalho Remota](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Detectando o ambiente de Serviços de Área de Trabalho Remota](detecting-the-terminal-services-environment.md)
</dt> </dl>

 

 




