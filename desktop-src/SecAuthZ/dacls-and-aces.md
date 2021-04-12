---
description: Se um objeto do Windows não tiver uma DACL (lista de controle de acesso discricionário), o sistema permitirá que todos tenham acesso completo a ele.
ms.assetid: be9633fb-14ef-42d2-9269-84287b35b653
title: DACLs e ACEs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28bf351fd59f634a7c7bf960aedac1c76659ad3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171683"
---
# <a name="dacls-and-aces"></a>DACLs e ACEs

Se um objeto do Windows não tiver uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ), o sistema permitirá que todos tenham acesso completo a ele. Se um objeto tiver uma DACL, o sistema permitirá apenas o acesso explicitamente permitido pelas ACEs ( [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) na DACL. Se não houver ACEs na DACL, o sistema não permitirá o acesso a ninguém. Da mesma forma, se uma DACL tiver ACEs que permitem o acesso a um conjunto limitado de usuários ou grupos, o sistema negará implicitamente o acesso a todos os confiáveis não incluídos nas ACEs.

Na maioria dos casos, você pode controlar o acesso a um objeto usando ACEs permitidas pelo Access; Você não precisa negar explicitamente o acesso a um objeto. A exceção é quando uma ACE permite o acesso a um grupo e você deseja negar o acesso a um membro do grupo. Para fazer isso, coloque uma ACE de acesso negado para o usuário na DACL à frente da ACE permitida pelo acesso para o grupo. Observe que a [ordem das ACEs](order-of-aces-in-a-dacl.md) é importante porque o sistema lê as ACEs em sequência até que o acesso seja concedido ou negado. A ACE de acesso negado do usuário deve aparecer primeiro; caso contrário, quando o sistema ler a ACE de acesso permitido do grupo, ele concederá acesso ao usuário restrito.

A ilustração a seguir mostra uma DACL que nega o acesso a um usuário e concede acesso a dois grupos. Os membros do grupo A obtêm direitos de acesso de leitura, gravação e execução, acumulando os direitos permitidos ao grupo A e direitos permitidos a todos. A exceção é Andrew, que tem o acesso negado pela ACE de acesso negado, apesar de ser um membro do grupo Everyone.

![DACL que concede diferentes direitos de acesso com base na associação de grupo](images/accctrl1.png)

 

 
