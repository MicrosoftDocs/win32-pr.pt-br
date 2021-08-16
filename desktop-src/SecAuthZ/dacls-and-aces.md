---
description: Se um Windows objeto não tiver uma DACL (lista de controle de acesso discricionário), o sistema permitirá a todos acesso completo a ele.
ms.assetid: be9633fb-14ef-42d2-9269-84287b35b653
title: DACLs e ACEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07bf87c2bd5f64b7178eca9d9fedd695a8b618430bf505f74be297780e48f774
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782171"
---
# <a name="dacls-and-aces"></a>DACLs e ACEs

Se um Windows objeto não tiver uma DACL [*(lista*](/windows/desktop/SecGloss/d-gly) de controle de acesso discricionário), o sistema permitirá a todos acesso completo a ele. Se um objeto tiver uma DACL, o sistema permitirá apenas o acesso que é explicitamente permitido pelas ACEs [*(entradas*](/windows/desktop/SecGloss/a-gly) de controle de acesso) na DACL. Se não houver ACEs na DACL, o sistema não permitirá o acesso a ninguém. Da mesma forma, se uma DACL tiver ACEs que permitam o acesso a um conjunto limitado de usuários ou grupos, o sistema negará implicitamente o acesso a todos os administradores não incluídos nas ACEs.

Na maioria dos casos, você pode controlar o acesso a um objeto usando ACEs permitidas para acesso; você não precisa negar explicitamente o acesso a um objeto . A exceção é quando uma ACE permite o acesso a um grupo e você deseja negar o acesso a um membro do grupo. Para fazer isso, coloque uma ACE de acesso negado para o usuário na DACL antes da ACE com acesso permitido para o grupo. Observe que [a ordem das ACEs](order-of-aces-in-a-dacl.md) é importante porque o sistema lê as ACEs em sequência até que o acesso seja concedido ou negado. A ACE de acesso negado do usuário deve aparecer primeiro; caso contrário, quando o sistema ler o acesso do grupo permitido ace, ele concederá acesso ao usuário restrito.

A ilustração a seguir mostra uma DACL que nega acesso a um usuário e concede acesso a dois grupos. Os membros do Grupo A têm direitos de acesso de Leitura, Gravação e Execução acumulando os direitos permitidos para o Grupo A e os direitos permitidos para Todos. A exceção é Andrew, que tem o acesso negado pela ACE negada ao acesso, apesar de ser membro do Grupo Todos.

![dacl que concede direitos de acesso diferentes com base na associação de grupo](images/accctrl1.png)

 

 
