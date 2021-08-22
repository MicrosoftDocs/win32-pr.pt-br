---
title: Funções de gancho fora do contexto
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 'Saiba mais sobre: funções de gancho fora de contexto'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e41e9a6bba1f705c3c5dc8781b2663be22086955f5dee45f07022504d0ccbf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133739"
---
# <a name="out-of-context-hook-functions"></a>Funções de gancho fora do contexto

A lista a seguir descreve os principais aspectos das funções de gancho fora do contexto:

-   As funções de gancho fora do contexto estão localizadas no espaço de endereço do cliente, seja no corpo do código ou em uma DLL.
-   Funções de gancho fora de contexto não são mapeadas para o espaço de endereço do servidor.
-   Quando um evento é disparado, os parâmetros da função Hook são empacotados entre limites de processo.
-   Funções de gancho fora do contexto são visivelmente mais lentas do que as funções de gancho no contexto devido ao marshaling.
-   O sistema enfileira as notificações de eventos para que elas cheguem de forma assíncrona (devido ao tempo necessário para realizar o marshaling).

Embora as notificações de eventos sejam assíncronas, a Microsoft Acessibilidade Ativa garante que a função de retorno de chamada receba todos os eventos na ordem em que são gerados.

O componente de usuário do sistema operacional aloca memória para eventos que são manipulados por funções de gancho fora do contexto. A memória é liberada quando as funções de gancho retornam. Se uma função de Hook não processar eventos com rapidez suficiente, os recursos do usuário serão reduzidos, eventualmente resultando em uma falha ou tempos de resposta extremamente lentos. Esses problemas podem ocorrer se:

-   Os eventos são acionados muito rapidamente.
-   O sistema está lento.
-   A função Hook processa eventos lentamente.
-   o cliente está em execução no Windows 9x.

 

 




