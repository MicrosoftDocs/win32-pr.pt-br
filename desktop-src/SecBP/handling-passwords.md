---
description: Atualmente, as credenciais de nome de usuário e senha são as credenciais mais comuns usadas para autenticação.
ms.assetid: 1d810f71-9bf5-4c5c-a573-c35081f604cf
title: Manipulando senhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99aaf133d23390a6f4efce97940c5116fddf91b45776dfd6847b2712b15b74ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035466"
---
# <a name="handling-passwords"></a>Manipulando senhas

Atualmente, as credenciais de nome de usuário e senha são as credenciais mais comuns usadas para autenticação. Embora outros tipos de credenciais, como certificados e biometria, estão começando a se deparar com o mundo dos sistemas e da rede, eles geralmente são apoiados por senhas. E, mesmo quando os certificados são usados, suas chaves de criptografia devem ser protegidas. Portanto, os nomes de usuário e senhas continuarão a ser usados para credenciais bem no futuro próximo.

Considerando que as senhas e as chaves de criptografia estarão por algum tempo, é importante que os sistemas de software as usem de maneira segura. Se um sistema de rede ou computador permanecer seguro, as senhas deverão ser protegidas contra invasores. Isso pode, a princípio, parecer trivial. No entanto, o sistema após o sistema e a rede após a rede foram comprometidos porque um invasor conseguiu detectar as senhas dos usuários. Os problemas variam de usuários compartilhando suas senhas com alguém, até software que pode ser penetrado por um invasor.

É impossível armazenar informações secretas em software de maneira completamente segura. E como o armazenamento de senhas e chaves de criptografia em um sistema de software nunca pode ser completamente seguro, é recomendável que elas não sejam armazenadas em um sistema de software.

No entanto, quando as senhas devem ser armazenadas em um sistema de software, que geralmente é o caso, há precauções que podem ser tomadas. A principal precaução é tornar o mais difícil possível para um invasor descobrir uma senha. Assim como bloquear as portas da casa, se alguém estiver determinado a entrar, é quase impossível impedi-lo de fazer isso. Mas, esperamos que você tenha elevado o nível de dificuldade o suficiente para que o invasor em vez de encontrar mais facilidade.

Há muitas maneiras de dificultar o trabalho de um invasor de descobrir senhas. No entanto, a extensão do que pode realmente ser feito é geralmente uma troca com a qual os usuários da rede ou do sistema estão dispostos a residi-lo. Por exemplo, leve em conta o caso em que o "logom único" não é usado e o usuário é solicitado a usar uma senha sempre que um aplicativo é iniciado. Na maioria dos casos, isso criaria uma carga significativa para os usuários, e eles provavelmente teriam uma reclamações. Não apenas isso, mas a falta de um único login é ineficiente e prejudicaria a produtividade dos usuários. Portanto, na prática, uma senha geralmente não é coletada de um usuário, exceto no momento do logoff.

Considerando que as senhas geralmente devem ser armazenadas no sistema de software, torna-se importante garantir que as senhas sejam mantidas o mais segura possível e que a conveniência para os usuários seja mantida. Para obter mais informações, consulte estes tópicos:

-   [Avaliação de Ameaças de Senha](password-threat-assessment.md)
-   [Técnicas de mitigação de ameaças](threat-mitigation-techniques.md)

> [!Note]  
> Quando terminar de usar senhas em aplicativos, limpe as informações confidenciais da memória chamando a [**função SecureZeroMemory.**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85))

 

 

 
