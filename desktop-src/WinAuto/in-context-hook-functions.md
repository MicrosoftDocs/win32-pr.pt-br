---
title: Funções de In-Context Hook
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 'Saiba mais sobre: funções de In-Context Hook'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cbeb6340642d63700901d9306aea5dca20b26ce46790d900e26e42875571379
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118565557"
---
# <a name="in-context-hook-functions"></a>Funções de In-Context Hook

A lista a seguir descreve os principais aspectos das funções de gancho no contexto:

-   As funções de ganchos no contexto devem estar localizadas em uma DLL (biblioteca de vínculo dinâmico) que o sistema mapeia para o espaço de endereço do servidor.
-   As funções de gancho no contexto compartilham o espaço de endereço com o servidor.
-   Quando o servidor dispara um evento, o sistema chama uma função de gancho sem realizar marshaling (empacotamento e envio de parâmetros de interface entre limites de processo).
-   As funções de gancho no contexto tendem a ser muito rápidas e recebem notificações de eventos de forma síncrona porque não há marshaling.
-   Alguns eventos podem ser fornecidos fora do processo, mesmo que você solicite que eles sejam entregues em processo (usando o \_ sinalizador de INCONTEXTO WINEVENT). você pode ver essa situação com problemas de interoperabilidade de aplicativos de 64 bits e 32 bits e com Windows eventos de console.

 

 




