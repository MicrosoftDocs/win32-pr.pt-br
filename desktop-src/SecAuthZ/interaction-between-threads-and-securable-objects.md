---
description: Em uma verificação de acesso, o sistema compara as informações de segurança no token de acesso de threads com as informações de segurança no descritor de segurança de objetos.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Interação entre threads e objetos securáveis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b27ab85aa461892d0e6fdf6bdbd9adc8aa7b78a3d9bf1b3896d53ad8e2e236de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670807"
---
# <a name="interaction-between-threads-and-securable-objects"></a>Interação entre threads e objetos securáveis

Quando um thread tenta usar um objeto [securável](securable-objects.md), o sistema executa uma verificação de acesso antes de permitir que o thread continue. Em uma verificação de acesso, o sistema compara as informações de segurança no token de acesso do [*thread*](/windows/desktop/SecGloss/a-gly) com as informações de segurança no [*descritor de segurança do objeto*](/windows/desktop/SecGloss/s-gly).

-   O token de acesso [*contém SIDs (identificadores*](/windows/desktop/SecGloss/s-gly) de segurança) que identificam o usuário associado ao thread.
-   O descritor de segurança identifica o proprietário do objeto e contém uma DACL (lista de controle [*de*](/windows/desktop/SecGloss/d-gly) acesso discricionário). A DACL contém [*ACEs*](/windows/desktop/SecGloss/a-gly) (entradas de controle de acesso), cada uma das quais especifica os direitos de acesso permitidos ou negados a um usuário ou grupo específico.

O sistema verifica a DACL do objeto, procurando ACEs que se aplicam aos SIDs de usuário e grupo do token de acesso do thread. O sistema verifica cada ACE até que o acesso seja concedido ou negado ou até que não haja mais ACEs a verificar. De forma concebível, [*uma*](/windows/desktop/SecGloss/a-gly) ACL (lista de controle de acesso) pode ter várias ACEs que se aplicam aos SIDs do token. E, se isso ocorrer, os direitos de acesso concedidos por cada ACE se acumulam. Por exemplo, se uma ACE conceder acesso de leitura a um grupo e outra ACE conceder acesso de gravação a um usuário que seja membro do grupo, o usuário poderá ter acesso de leitura e gravação ao objeto.

A ilustração a seguir mostra a relação entre esses blocos de informações de segurança:

![relações entre processos, acess e dacls](images/cssec-02.png)

 

 
