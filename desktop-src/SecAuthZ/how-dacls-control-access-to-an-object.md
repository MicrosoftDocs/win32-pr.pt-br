---
description: Quando um thread tenta acessar um objeto protegível, o sistema concede ou nega acesso.
ms.assetid: dc98b23e-ce42-4d4a-a285-c0b7b5e2a478
title: Como a AccessCheck funciona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 730cc8f63e7d69bf4cb38344f5eda60861d08a9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558850"
---
# <a name="how-accesscheck-works"></a>Como a AccessCheck funciona

Quando um thread tenta acessar um objeto protegível, o sistema concede ou nega acesso. Se o objeto não tiver uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ), o sistema concederá acesso; caso contrário, o sistema procura por ACEs ( [entradas de controle de acesso](access-control-entries.md) ) no DACL do objeto que se aplicam ao thread. Cada ACE na DACL do objeto especifica os direitos de acesso permitidos ou negados para um objeto de [confiança](trustees.md), que pode ser uma conta de usuário, uma conta de grupo ou uma [*sessão de logon*](/windows/desktop/SecGloss/l-gly).

## <a name="dacls"></a>DACLs

O sistema compara o confiável em cada ACE com os confiáveis identificados no [token de acesso](access-tokens.md)do thread. Um token de acesso contém SIDs ( [*identificadores de segurança*](/windows/desktop/SecGloss/s-gly) ) que identificam o usuário e as contas de grupo às quais o usuário pertence. Um token também contém um [*Sid de logon*](/windows/desktop/SecGloss/l-gly) que identifica a sessão de logon atual. Durante uma verificação de acesso, o sistema ignora os SIDs de grupo que não estão habilitados. Para obter mais informações sobre SIDs habilitados, desabilitados e somente negados, consulte [atributos de Sid em um token de acesso](sid-attributes-in-an-access-token.md).

Normalmente, o sistema usa o [*token de acesso primário*](/windows/desktop/SecGloss/p-gly) do thread que está solicitando o acesso. No entanto, se o thread estiver representando outro usuário, o sistema usará o [*token de representação*](/windows/desktop/SecGloss/i-gly)do thread.

O sistema examina cada ACE em sequência até que ocorra um dos seguintes eventos:

-   Uma ACE com acesso negado nega explicitamente qualquer um dos [direitos de acesso](access-rights-and-access-masks.md) solicitados a um dos os confiáveis listados no token de acesso do thread.
-   Uma ou mais ACEs permitidas pelo Access para os confiáveis listados no token de acesso do thread concedem explicitamente todos os direitos de acesso solicitados.
-   Todas as ACEs foram verificadas e ainda há pelo menos um direito de acesso solicitado que não tenha sido explicitamente permitido; nesse caso, o acesso é negado implicitamente.

A ilustração a seguir mostra como a DACL de um objeto pode permitir o acesso a um thread negando acesso a outro.

![DACL que concede direitos de acesso diferentes a threads diferentes](images/accctrl1.png)

Para o thread A, o sistema lê a ACE 1 e imediatamente nega o acesso porque a ACE de acesso negado se aplica ao usuário no token de acesso do thread. Nesse caso, o sistema não verifica as ACEs 2 e 3. Para o thread B, o ACE 1 não se aplica, portanto, o sistema prossegue para o ás 2, que permite acesso de gravação e ACE 3, que permite acesso de leitura e execução.

Como o sistema para de verificar as ACEs quando o acesso solicitado é explicitamente concedido ou negado, a ordem das ACEs em uma DACL é importante. Observe que, se a ordem de ACE fosse diferente no exemplo, o sistema pode ter concedido acesso ao thread A. Para objetos do sistema, o sistema operacional define uma [ordem preferida de ACEs em uma DACL](order-of-aces-in-a-dacl.md).

 

 
