---
title: O banco de dados do serviço de nome RPC
description: Um serviço de nome é um serviço que mapeia nomes para objetos e geralmente mantém os pares (nome, objeto) em um banco de dados.
ms.assetid: 9ced2307-cf30-45d5-bcd2-c1e4aae8c63b
keywords:
- Chamada de procedimento remoto RPC, descrito, nome do banco de dados de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19ae37473bcf28ddf995ab0a657f300ce13aa83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453641"
---
# <a name="the-rpc-name-service-database"></a>O banco de dados do serviço de nome RPC

Um serviço de nome é um serviço que mapeia nomes para objetos e geralmente mantém os pares (nome, objeto) em um banco de dados. Em geral, o nome é um nome lógico que é fácil para os usuários se lembrar e usar. Por exemplo, um serviço de nome permite que um usuário use o nome lógico "laserprinter". O serviço de nome mapeia esse nome para o nome específico da rede usado pelo servidor de impressão.

Para usar uma explicação simplificada, o serviço de nome RPC mapeia um nome para um identificador de associação e mantém os mapeamentos (nome, identificador de associação) no banco de dados do serviço de nome RPC. O serviço de nome RPC permite que os aplicativos cliente usem um nome lógico em vez de uma sequência de protocolo e endereço de rede específicos. O uso do nome lógico torna mais fácil para os administradores de rede instalar e configurar seu aplicativo distribuído.

Uma entrada de banco de dados de serviço de nome RPC tem um dos seguintes atributos: **servidor**, **grupo** ou **perfil**. Na implementação da Microsoft, as entradas podem ter apenas um atributo, portanto, essas entradas também são conhecidas como entradas de servidor, entradas de grupo e entradas de perfil.

A entrada do servidor consiste em UUIDs de interface, UUIDs de objeto (necessários quando o servidor implementa pontos de várias entradas), endereço de rede, sequência de protocolo e quaisquer informações de ponto de extremidade associadas a pontos de extremidades conhecidos. Quando um ponto de extremidade dinâmico é usado, as informações do ponto de extremidade são mantidas no banco de dados do mapa de ponto de extremidade em vez do banco de dados do serviço de nome e o ponto de extremidade é resolvido como qualquer outro ponto de extremidade As entradas de servidor são gerenciadas por funções que começam com o prefixo "RpcNsBinding".

A entrada de grupo pode conter entradas de servidor ou outras entradas de grupo. As entradas de grupo são gerenciadas por funções que começam com o prefixo "RpcNsGroup".

A entrada de perfil pode conter entradas de perfil, grupo ou servidor. As entradas de perfil são gerenciadas pelas funções que começam com o prefixo "RpcNsProfile".

Esta seção apresenta uma visão geral do banco de dados do serviço de nome nos seguintes tópicos:

-   [Diretrizes de aplicativo de serviço de nome](name-service-application-guidelines.md)
-   [Uma visão geral da entrada de serviço de nome](an-overview-of-the-name-service-entry.md)
-   [Critérios para entradas de serviço de nome](criteria-for-name-service-entries.md)
-   [Limpeza da entrada do serviço de nome](name-service-entry-cleanup.md)
-   [O que acontece durante uma consulta](what-happens-during-a-query.md)
-   [Usando o Microsoft Locator](using-microsoft-locator.md)
-   [Usando o CDS (serviço de diretório de células)](using-the-cell-directory-service-cds-.md)
-   [Sintaxe do nome](name-syntax.md)

 

 




