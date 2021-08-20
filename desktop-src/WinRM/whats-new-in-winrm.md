---
title: Novidades no WinRM 2.0
description: Novos recursos estão disponíveis no Windows Remote Management versão 2.0. (WinRM 2.0).
ms.assetid: 402c179a-6dd7-4d75-9318-bb8194b5527d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d322b0b86600cd783bd787427b53df334f3d499a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480582"
---
# <a name="whats-new-in-winrm-20"></a>Novidades no WinRM 2.0

Novos recursos estão disponíveis no Windows Remote Management versão 2.0. (WinRM 2.0)

O WinRM 2.0 está incluído no Windows Server 2008 R2 e Windows 7.

Você também pode baixar o WinRM 2.0 para o Windows Server 2008 com Service Pack 2 (SP2) e Windows Vista com Service Pack 2 (SP2). Para obter informações sobre como baixar o WinRM 2.0, consulte [KB968929](https://support.microsoft.com/kb/968929).

A tabela a seguir lista a documentação do WinRM 2.0.




| Tópico | Descrição | 
|-------|-------------|
| <a href="client-shell-api.md">API do shell do cliente WinRM</a><br /> | A API (interface de programação de aplicativos) do WinRM Client Shell fornece funcionalidade para criar e gerenciar shells e operações de shell, comandos e fluxos de dados em computadores remotos. <br /> | 
| <a href="winrm-plugin-api.md">API de plug-in do WinRM</a><br /> | A API de Plug-in do WinRM fornece funcionalidade que permite que um usuário escreva plug-ins implementando determinadas APIs para <a href="windows-remote-management-glossary.md"><em>URIs</em></a> e operações de recursos com suporte.<br /> | 
| <a href="winrm-application-hosting.md">Infraestrutura para gerenciar serviços hospedados</a><br /> | O WinRM 2.0 apresenta uma estrutura de hospedagem. Há suporte para dois modelos de hospedagem. Uma delas é baseada no IIS (Serviço de Informações da Internet) e a outra é baseada em serviço WinRM. <br /> Para obter mais informações sobre a configuração do host, consulte os seguintes tópicos:<br /><ul><li><a href="iis-host-plug-in-configuration.md">Configuração de plug-in de host do IIS</a></li><li><a href="wsman-service-plug-in-configuration.md">Configuração de plug-in do serviço WinRM</a></li></ul> | 
| <a href="dmtf-association-traversal.md">Descoberta de perfil DMTF por meio de passagem de associação</a><br /> | A travessia de associação permite que um usuário recupere instâncias de classes de Associação usando um mecanismo de filtragem padrão.<br /> | 
| <a href="remote-shell-infrastructure-improvements.md">Melhorias na infraestrutura do Shell Remoto</a><br /> | Este tópico inclui informações sobre as melhorias de infraestrutura remota para WinRM. <br /> | 
| <a href="multi-hop-support.md">Suporte a vários saltos</a><br /> | A funcionalidade foi adicionada ao WinRM 2.0 que dá suporte à delegação de credenciais de usuário em vários computadores remotos. <br /> O <a href="authentication-constants.md"><strong>tópico Constantes de</strong></a> Autenticação foi atualizado para adicionar a seguinte constante: <strong>WSManFlagUseCredSsp</strong>.<br /> A API C++ a seguir foi adicionada para fornecer suporte a vários saltos: <a href="/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex3"><strong>IWSManEx3.</strong></a><br /> A API de script a seguir foi adicionada para fornecer suporte a vários saltos: <a href="wsman-sessionflagusecredssp.md"><strong>WSMan.SessionFlagUseCredSsp</strong></a>.<br /> | 
| <a href="quotas.md">Gerenciamento de cotas para shells remotos</a><br /> | Este tópico inclui informações sobre a configuração de cota para gerenciamento de shell remoto.<br /> | 
| <a href="winrm-powershell-commandlets.md">Referência gerenciada para WS-Management comandos do PowerShell</a><br /> | Os usuários do WinRM 2.0 podem usar Windows PowerShell cmdlets para gerenciamento do sistema.<br /> | 




 

 

 





