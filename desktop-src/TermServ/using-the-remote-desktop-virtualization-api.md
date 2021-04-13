---
title: Usando a API de virtualização Área de Trabalho Remota
description: Os desenvolvedores podem usar essa API para personalizar a lógica que o agente de conexão de área de trabalho remota usa para determinar o melhor destino para uma conexão de cliente de entrada.
ms.assetid: b25eb87e-dac4-49ce-890e-b39c7e9e3408
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota, usando a API de virtualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda9ebfc014a2c8ec20d299bbb8be9183b25ce89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366132"
---
# <a name="using-the-remote-desktop-virtualization-api"></a>Usando a API de virtualização Área de Trabalho Remota

O serviço de função do diretório de sessão dos serviços de terminal (diretório de Sessão TS) permite que os servidores de terminal armazenem informações de usuário e de sessão em um banco de dados chamado de diretório de sessões. Quando um usuário se conecta a um servidor de terminal em um farm, o diretório de Sessão TS determina se o usuário já tem uma sessão em execução em um servidor de terminal e, nesse caso, redireciona o usuário para esse servidor de terminal.

No Windows Server 2008, o serviço de função do diretório de sessões TS foi expandido e renomeado como agente de sessão de serviços de terminal (provedor de Sessão TS). Além de manter um diretório de sessões existentes, o agente de Sessão TS também pode fazer o agente de conexões de entrada. Quando o agente de Sessão TS recebe uma conexão de entrada de um usuário, ele verifica seu banco de dados para determinar se o usuário tem uma sessão existente em um servidor de terminal. Nesse caso, o agente de Sessão TS redireciona a conexão para o mesmo servidor de terminal. Caso contrário, o agente de Sessão TS determina qual servidor de terminal tem as menores conexões e redireciona a conexão para esse servidor.

A partir do Windows Server 2008, a Microsoft também lançou uma API (interface de programação de aplicativo) pública para monitorar e interagir com sessões em servidores de terminal. Essa API é descrita em [referência de plug-in do conexão de área de trabalho remota Broker](/windows/desktop/TermServ/terminal-services-virtualization-api-reference). Usando essa API, os desenvolvedores podem criar plug-ins de política personalizados que substituem a lógica de redirecionamento padrão do agente de Sessão TS. Os plug-ins personalizados podem redirecionar sessões para servidores de terminal, bem como máquinas virtuais, áreas de trabalho virtuais, servidores de folha e áreas de trabalho físicas.

No Windows Server 2008 R2, a arquitetura do agente do Conexão de Área de Trabalho Remota (agente de conexão RD) (anteriormente conhecido como agente de Sessão TS) foi expandida para dar suporte a conexões com máquinas virtuais. A nova arquitetura dá suporte ao gerenciamento de sessões para máquinas virtuais por meio da API de virtualização Área de Trabalho Remota. Os desenvolvedores podem usar essa API para personalizar a lógica que o agente de conexão de área de trabalho remota usa para determinar o melhor destino para uma conexão de cliente de entrada.

A API de virtualização Área de Trabalho Remota oferece vários benefícios para os desenvolvedores:

-   As interfaces para trabalhar com servidores de terminal físicos são semelhantes às do trabalho com máquinas virtuais.
-   Os desenvolvedores podem substituir toda ou parte da lógica de redirecionamento padrão. Os desenvolvedores podem criar o código que acompanha o produto e não precisam escrever tudo do zero.
-   Nenhum agente de gerenciamento adicional é necessário no servidor de gerenciamento ou na sessão.
-   Plug-ins do agente de Sessão TS desenvolvidos para uso com o Windows Server 2008 ainda têm suporte.
-   A API também permite que os desenvolvedores criem interfaces do usuário para administração de servidores Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) (anteriormente conhecidos como "servidores de terminal") e máquinas virtuais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de API de virtualização Área de Trabalho Remota](terminal-services-virtualization-api-reference.md)
</dt> <dt>

[Referência de plug-in do Conexão de Área de Trabalho Remota Broker](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)
</dt> </dl>

 

 