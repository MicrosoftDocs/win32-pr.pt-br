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
ms.openlocfilehash: 5014dc894c4a517bfdfac8478e520658a4987d4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005640"
---
# <a name="about-routing-table-manager-version-2"></a>Sobre o Gerenciador de tabela de roteamento versão 2

A documentação a seguir descreve a tecnologia de Gerenciador de tabela de roteamento versão 2 (RTMv2). A API do RTMv2 é um recurso do Windows 2000 e sistemas operacionais posteriores que você pode usar para gravar protocolos de roteamento que interagem com o Gerenciador de tabela de roteamento.

O Gerenciador de tabela de roteamento é o repositório central de informações de roteamento para todos os protocolos de roteamento que operam no RRAS (serviço de roteamento e acesso remoto).

O RTMv2 não está disponível para o Windows NT versão 4,0. Além disso, o RTMv2 não pode ser usado para protocolos de roteamento IPX que são executados no Windows NT 4,0 ou no Windows 2000. Se você estiver usando IPX ou gravando protocolos de roteamento para o Windows NT 4,0, consulte [sobre o Gerenciador de tabela de roteamento versão 1](about-routing-table-manager-version-1.md).

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

 

 




