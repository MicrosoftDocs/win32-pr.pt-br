---
description: Algumas funções exigem privilégios especiais para serem executadas corretamente.
ms.assetid: b25db548-d5ab-4276-9b50-36d030909384
title: Executando com privilégios especiais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be662d187ef27c7afc12b031f2d8de225d34c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762910"
---
# <a name="running-with-special-privileges"></a>Executando com privilégios especiais

Algumas funções exigem [privilégios](/windows/desktop/SecAuthZ/privileges) especiais para serem executadas corretamente. Em alguns casos, a função só pode ser executada por determinados usuários ou por membros de determinados grupos. O requisito mais comum é que o usuário seja um administrador local. Outras funções exigem que a conta do usuário tenha privilégios específicos habilitados.

Para reduzir a possibilidade de código não autorizado ser capaz de obter controle, o sistema deve ser executado com o privilégio mínimo necessário. Os aplicativos que precisam chamar funções que exigem privilégios especiais podem deixar o sistema aberto para atacar por hackers. Esses aplicativos devem ser projetados para serem executados por curto período de tempo e devem informar o usuário das implicações de segurança envolvidas.

Para obter informações sobre como executar o como usuários diferentes e como habilitar privilégios em seu aplicativo, consulte os seguintes tópicos:<dl>

[Executando com privilégios de administrador](running-with-administrator-privileges.md)  
[Solicitando credenciais ao usuário](asking-the-user-for-credentials.md)  
[Alterando privilégios em um token](changing-privileges-in-a-token.md)  
[Atribuindo privilégios a uma conta](assigning-privileges-to-an-account.md)  
</dl>

 

 
