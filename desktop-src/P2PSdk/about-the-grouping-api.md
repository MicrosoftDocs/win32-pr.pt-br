---
description: A API de agrupamento de pares combina a tecnologia da API do provedor de espaço de nome PNRP e a API de gráfico.
ms.assetid: 0a575efe-968c-48ab-a446-0d910ecb5708
title: Sobre a API de agrupamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e0c14e2731dd133afac32f2cd21905fa7e0c5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750784"
---
# <a name="about-the-grouping-api"></a>Sobre a API de agrupamento

A API de agrupamento de pares combina a tecnologia da API do [provedor de espaço de nome PNRP](pnrp-namespace-provider-api.md) e a [API de gráfico](graphing-api.md). O agrupamento adiciona as duas partes de tecnologia a seguir:

-   Uma camada de multiplexação que permite que vários aplicativos usem um grafo, uma porta e um banco de dados de registro.
-   Segurança que garante que somente os colegas convidados para um grupo possam ingressar e se conectar durante todo o tempo de vida de um grupo.

O agrupamento fornece uma abordagem fácil e acessível para a rede de mesmo nível por causa do fluxo de chamadas direto e mensagens seguras. Essa API utiliza o PNRP para a descoberta de grupo e um provedor de segurança baseado em PKI padrão em vez de exigir que um desenvolvedor implemente um. No entanto, se seu aplicativo exigir maior flexibilidade em termos de opções de segurança, considere usar a [API de gráfico](about-the-graphing-api.md).

A tabela a seguir identifica os tópicos nesta seção de API de agrupamento:

| Tópico                                                                | Descrição                                                                              |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Como trabalhar com grupos](how-to-work-with-groups.md)               | Descreve o fluxo de chamadas em um aplicativo de agrupamento de pares da inicialização para o desligamento.         |
| [Como funciona a segurança de grupo](how-group-security-works.md)             | Descreve como a associação de grupo de pares e as trocas de dados são protegidas.                      |
| [Convidando um par a um grupo](inviting-a-peer-to-a-group.md)         | Descreve o processo pelo qual os pares são convidados e adicionados a um grupo de pares.              |
| [Como se conectar a um grupo de pares](how-to-connect-to-a-peer-group.md) | Descreve como um par se conecta e interage com um grupo de pares.                        |
| [Gerenciando registros de grupo](managing-group-records.md)                 | Descreve os registros de grupo de pares e como gerenciá-los como um membro e como um administrador. |



 

> [!Note]  
> Os aplicativos que usam a API de agrupamento em um ambiente com um firewall exigem grupos de exceção que abrangem a porta específica do aplicativo, bem como a porta "3587-TCP" para a API de agrupamento e a porta "3540-UDP" para o PNRP. Esses grupos de exceções devem ser habilitados sempre que o aplicativo estiver em execução.

 

 

 



