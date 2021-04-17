---
description: O usuário pode iniciar um serviço com o utilitário do painel de controle de serviços. O usuário pode especificar argumentos para o serviço no campo Iniciar parâmetros. Um programa de controle de serviço pode iniciar um serviço e especificar seus argumentos com a função StartService.
ms.assetid: 72f51b38-d62c-4400-a38d-b9a0e90e9db4
title: Iniciando serviços sob demanda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c70be74e6cf54468f244ca798ae7ca48da3512
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751070"
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

 

 



