---
description: O usuário pode iniciar um serviço com o utilitário do painel de controle de serviços. O usuário pode especificar argumentos para o serviço no campo Iniciar parâmetros. Um programa de controle de serviço pode iniciar um serviço e especificar seus argumentos com a função StartService.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Iniciando serviços sob demanda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3762721eaeaea32d42da729f57c0753b18fb951cb57ad091aa697c144df0de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888462"
---
# <a name="starting-services-on-demand"></a>Iniciando serviços sob demanda

O usuário pode iniciar um serviço com o utilitário do painel de controle de serviços. O usuário pode especificar argumentos para o serviço no campo **Iniciar parâmetros** . Um programa de controle de serviço pode iniciar um serviço e especificar seus argumentos com a função [**StartService**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea) .

Quando o serviço é iniciado, o SCM executa as seguintes etapas:

-   Recupere as informações de conta armazenadas no banco de dados.
-   Faça logon na conta de serviço.
-   Carregue o perfil do usuário.
-   Crie o serviço no estado suspenso.
-   Atribua o token de logon ao processo.
-   Permitir que o processo seja executado.

 

 



