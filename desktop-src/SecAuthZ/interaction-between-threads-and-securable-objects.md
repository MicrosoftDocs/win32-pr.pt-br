---
description: Em uma verificação de acesso, o sistema compara as informações de segurança no token de acesso de threads com relação às informações de segurança no descritor de segurança de objetos.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Interação entre threads e objetos protegíveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3e2b18f707ece4d651eeca1c6897bb67aad334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829734"
---
# <a name="interaction-between-threads-and-securable-objects"></a>Interação entre threads e objetos protegíveis

Quando um thread tenta usar um [objeto protegível](securable-objects.md), o sistema executa uma verificação de acesso antes de permitir que o thread prossiga. Em uma verificação de acesso, o sistema compara as informações de segurança no [*token de acesso*](/windows/desktop/SecGloss/a-gly) do thread com as informações de segurança no [*descritor de segurança*](/windows/desktop/SecGloss/s-gly)do objeto.

-   O token de acesso contém SIDs ( [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) ) que identificam o usuário associado ao thread.
-   O descritor de segurança identifica o proprietário do objeto e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ). A DACL contém ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ), cada uma delas especificando os direitos de acesso permitidos ou negados a um usuário ou grupo específico.

O sistema verifica a DACL do objeto, procurando ACEs que se aplicam aos SIDs de usuário e grupo do token de acesso do thread. O sistema verifica cada ACE até que o acesso seja concedido ou negado ou até que não haja mais ACEs a serem verificadas. Concebível, uma ACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) pode ter várias ACEs que se aplicam aos SIDs do token. E, se isso ocorrer, os direitos de acesso concedidos por cada ACE se acumulam. Por exemplo, se uma ACE conceder acesso de leitura a um grupo e outra ACE conceder acesso de gravação a um usuário que seja membro do grupo, o usuário poderá ter acesso de leitura e gravação ao objeto.

A ilustração a seguir mostra a relação entre esses blocos de informações de segurança:

![relações entre processos, Aces e DACLs](images/cssec-02.png)

 

 
