---
title: Sobre o Gerenciador de tabela de roteamento versão 2
description: A documentação a seguir descreve a tecnologia de Gerenciador de tabela de roteamento versão 2 (RTMv2).
ms.assetid: 9f84863e-45ed-49d1-8df4-3b59b1b5f3c9
keywords:
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de tabela de roteamento versão 2
- Serviço de roteamento e acesso remoto RRAS, Gerenciador de tabela de roteamento versão 2, descrito
- Gerenciador de tabela de roteamento versão 2 RRAS
- Gerenciador de tabela de roteamento versão 2 RRAS, descrito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87228222f31daf7f951064d05c92d950a3fff0d570fcac3536887b50193b16b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792103"
---
# <a name="about-routing-table-manager-version-2"></a>Sobre o Gerenciador de tabela de roteamento versão 2

A documentação a seguir descreve a tecnologia de Gerenciador de tabela de roteamento versão 2 (RTMv2). a API do RTMv2 é um recurso do Windows 2000 e sistemas operacionais posteriores que você pode usar para gravar protocolos de roteamento que interagem com o gerenciador de tabela de roteamento.

O Gerenciador de tabela de roteamento é o repositório central de informações de roteamento para todos os protocolos de roteamento que operam no RRAS (serviço de roteamento e acesso remoto).

RTMv2 não está disponível para a versão Windows NT 4,0. além disso, RTMv2 não pode ser usado para protocolos de roteamento IPX que são executados em Windows NT 4,0 ou Windows 2000. se você estiver usando IPX ou gravando protocolos de roteamento para Windows NT 4,0, consulte [sobre o gerenciador de tabela de roteamento versão 1](about-routing-table-manager-version-1.md).

Esta visão geral descreve os seguintes tópicos:

-   [Componentes da arquitetura do Gerenciador de tabela de roteamento](components-of-the-routing-table-manager-architecture.md)
-   [Registrando com o Gerenciador de tabela de roteamento](registering-with-the-routing-table-manager.md)
-   [Enumerando entidades registradas](enumerating-registered-entities.md)
-   [Usando métodos](using-methods.md)
-   [Usando ponteiros opacos](using-opaque-pointers.md)
-   [Marcando rotas para o estado de Hold-Down](marking-routes-for-the-hold-down-state.md)
-   [Adicionando rotas](adding-routes.md)
-   [Recuperando informações de rota](retrieving-route-information.md)
-   [Atualizando rotas](updating-routes.md)
-   [Recebendo notificação de alterações](receiving-notification-of-changes.md)
-   [Trabalhando com próximos saltos](working-with-next-hops.md)
-   [Enumerando entradas da tabela de roteamento](enumerating-routing-table-entries.md)
-   [Localizando informações específicas na tabela de roteamento](finding-specific-information-in-the-routing-table.md)
-   [Manutenção de listas de Client-Specific](maintaining-client-specific-lists.md)
-   [Gerenciando identificadores](managing-handles.md)

 

 




