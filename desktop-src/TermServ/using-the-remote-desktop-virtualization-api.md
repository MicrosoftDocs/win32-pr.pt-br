---
title: Usando a API Área de Trabalho Remota virtualização
description: Os desenvolvedores podem usar essa API para personalizar a lógica que o Agente de Conexão RD usa para determinar o melhor destino para uma conexão de cliente de entrada.
ms.assetid: b25eb87e-dac4-49ce-890e-b39c7e9e3408
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota Serviços de Área de Trabalho Remota , usando a API de virtualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7075c3a0cfcabc2df0dcb8438b7de5a748eb2b0340e26bf3d1e51afdb182f81e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119423626"
---
# <a name="using-the-remote-desktop-virtualization-api"></a>Usando a API Área de Trabalho Remota virtualização

O serviço de função Diretório de Sessão dos Serviços de Terminal (Diretório de Sessão do TS) permite que os servidores de terminal armazenem informações de usuário e sessão em um banco de dados chamado diretório de sessão. Quando um usuário se conecta a um servidor de terminal em um farm, o Diretório de Sessão do TS determina se o usuário já tem uma sessão em execução em um servidor de terminal e, se for o caso, redireciona o usuário para esse servidor terminal.

No Windows Server 2008, o serviço de função do Diretório de Sessão do TS foi expandido e renomeado como Agente de Sessão dos Serviços de Terminal (Agente de Sessão do TS). Além de manter um diretório de sessões existentes, o Agente de Sessão do TS também pode intermediar conexões de entrada. Quando o Agente de Sessão do TS recebe uma conexão de entrada de um usuário, ele verifica seu banco de dados para determinar se o usuário tem uma sessão existente em um servidor de terminal. Nesse caso, o Agente de Sessão do TS redireciona a conexão para o mesmo servidor terminal. Caso não tenha, o Agente de Sessão do TS determina qual servidor terminal tem o menor conexões e redireciona a conexão para esse servidor.

A partir do Windows Server 2008, a Microsoft também lançou uma API (interface de programação de aplicativo) pública para monitorar e interagir com sessões em servidores terminais. Essa API é descrita em [referência Conexão de Área de Trabalho Remota plug-in do Broker.](/windows/desktop/TermServ/terminal-services-virtualization-api-reference) Usando essa API, os desenvolvedores podem criar plug-ins de política personalizados que substituem a lógica de redirecionamento padrão do Agente de Sessão do TS. Os plug-ins personalizados podem redirecionar sessões para servidores de terminal, bem como máquinas virtuais, áreas de trabalho virtuais, servidores de folha e áreas de trabalho físicas.

No Windows Server 2008 R2, a arquitetura do Conexão de Área de Trabalho Remota Broker (Agente de Conexão RD) (anteriormente conhecido como Agente de Sessão TS) foi expandida para dar suporte a conexões com máquinas virtuais. A nova arquitetura dá suporte ao gerenciamento de sessão para máquinas virtuais por meio da API Área de Trabalho Remota Virtualização. Os desenvolvedores podem usar essa API para personalizar a lógica que o Agente de Conexão RD usa para determinar o melhor destino para uma conexão de cliente de entrada.

Área de Trabalho Remota API de Virtualização oferece vários benefícios aos desenvolvedores:

-   As interfaces para trabalhar com servidores de terminal físico são semelhantes às que trabalham com máquinas virtuais.
-   Os desenvolvedores podem substituir toda ou parte da lógica de redirecionamento padrão. Os desenvolvedores podem se basear no código que acompanha o produto e não precisa escrever tudo do zero.
-   Nenhum agente de gerenciamento adicional é necessário no servidor de gerenciamento ou na sessão.
-   Ainda há suporte para plug-ins do Agente de Sessão TS desenvolvidos para uso com Windows Server 2008.
-   A API também permite que os desenvolvedores criem interfaces do usuário para administração de servidores Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) (anteriormente conhecidos como "servidores terminais") e máquinas virtuais.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência Área de Trabalho Remota API de Virtualização do Área de Trabalho Remota](terminal-services-virtualization-api-reference.md)
</dt> <dt>

[Conexão de Área de Trabalho Remota plug-in do Broker do Conexão de Área de Trabalho Remota](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)
</dt> </dl>

 

 