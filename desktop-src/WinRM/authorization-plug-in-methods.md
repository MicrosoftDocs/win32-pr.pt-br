---
title: Métodos de plug-in de autorização
description: Todos os pontos de entrada de plug-in de autorização têm um mecanismo de retorno de chamada para relatar o êxito ou a falha da chamada. Alguns mecanismos de retorno de chamada são chamados várias vezes até que todos os resultados sejam relatados.
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9253267b87a30c5cc2781440b0ecd430f244e90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105790639"
---
# <a name="authorization-plug-in-methods"></a>Métodos de plug-in de autorização

Todos os pontos de entrada de plug-in de autorização têm um mecanismo de retorno de chamada para relatar o êxito ou a falha da chamada. Alguns mecanismos de retorno de chamada são chamados várias vezes até que todos os resultados sejam relatados.

A tabela a seguir fornece uma visão geral dos métodos de retorno de chamada de autorização.



| Método                                                                           | Descrição                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | Relata uma operação de usuário bem-sucedida ou com falha.                |
| [**WSManPluginAuthzQueryQuotaComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | Relata os detalhes de cota que são relevantes para o usuário especificado.      |
| [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | Relata uma autorização de conexão de usuário com êxito ou falha. |



 

 

 




