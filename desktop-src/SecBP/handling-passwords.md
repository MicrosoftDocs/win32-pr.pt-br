---
description: Atualmente, as credenciais de nome de usuário e senha são as credenciais mais comuns usadas para autenticação.
ms.assetid: 1d810f71-9bf5-4c5c-a573-c35081f604cf
title: Manipulando senhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d3a5ab2bc034500159adb25dab02b47eb43bcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105750769"
---
# <a name="handling-passwords"></a>Manipulando senhas

Atualmente, as credenciais de nome de usuário e senha são as credenciais mais comuns usadas para autenticação. Embora outros tipos de credenciais, como certificados e Biometria, estejam começando a encontrar seu caminho no mundo dos sistemas e da rede, muitas vezes eles são submetidos a backup por senhas. E, mesmo onde os certificados são usados, suas chaves de criptografia devem ser protegidas. Assim, os nomes de usuário e as senhas continuarão sendo usados para as credenciais bem no futuro próximo.

Considerando que senhas e chaves de criptografia serão delimitadas, é importante que os sistemas de software as usem de maneira segura. Se um sistema de rede ou computador for permanecer seguro, as senhas deverão ser protegidas contra intrusos. Isso pode, a princípio, parecer trivial. No entanto, o sistema após o sistema e a rede após a rede foi comprometido porque um invasor conseguiu detectar as senhas dos usuários. Os problemas variam de usuários que compartilham suas senhas com alguém, para software que pode ser invadido por um invasor.

É impossível armazenar informações secretas no software de uma maneira totalmente segura. E, como o armazenamento de senhas e chaves de criptografia em um sistema de software nunca pode ser totalmente seguro, é recomendável que elas não sejam armazenadas em um sistema de software.

No entanto, quando as senhas devem ser armazenadas em um sistema de software, que geralmente é o caso, há precauções que podem ser tomadas. A precaução principal é torná-lo o mais difícil possível para um invasor descobrir uma senha. Assim como o bloqueio de suas portas de casa, se alguém for considerado interrompido, será quase impossível impedi-lo de fazer isso. Mas, espero, você terá aumentado o nível de dificuldade de que o invasor seria, em vez disso, acharia mais fácil.

Há várias maneiras de tornar mais difícil o trabalho do invasor de descobrir senhas. No entanto, a extensão do que realmente pode ser feito é, em geral, uma compensação com o que os usuários da rede ou do sistema estão dispostos a viver. Por exemplo, considere o caso em que "logon único" não é usado e o usuário é solicitado a fornecer uma senha toda vez que um aplicativo é iniciado. Na maioria dos casos, isso criaria uma sobrecarga significativa nos usuários e, provavelmente, reclamaria. Não só isso, mas a falta de um logon único é ineficiente e degrada a produtividade dos usuários. Portanto, quase falando, uma senha geralmente não é coletada de um usuário, exceto no momento do logon.

Considerando que as senhas normalmente devem ser armazenadas no sistema de software, é importante garantir que as senhas sejam mantidas o mais seguras possível e que a conveniência para os usuários seja mantida. Para mais informações, consulte os seguintes tópicos:

-   [Avaliação de ameaças de senha](password-threat-assessment.md)
-   [Técnicas de mitigação de ameaças](threat-mitigation-techniques.md)

> [!Note]  
> Quando você terminar de usar senhas em aplicativos, desmarque as informações confidenciais da memória chamando a função [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) .

 

 

 
