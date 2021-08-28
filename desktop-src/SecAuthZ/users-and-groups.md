---
description: Explica a definição de usuários e grupos na API do Gerenciador de Autorização.
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: Usuários e Grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7d6ae84dba833ddd06eb81944cecb9aa401c0f8f1971c3164317cefae14fbe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906816"
---
# <a name="users-and-groups"></a>Usuários e Grupos

No Gerenciador de Autorização, os destinatários da política de autorização são representados pelos seguintes grupos:

-   Windows Usuários e grupos

    Esses grupos incluem usuários, computadores e grupos integrados para entidades de segurança.

-   Grupos de consultas LDAP

    A associação nesses grupos é calculada dinamicamente conforme necessário nas consultas LDAP (Lightweight Directory Access Protocol). Um grupo de consultas LDAP é um tipo de grupo de aplicativos.

-   Grupos de Aplicativos Básicos

    Esses grupos consistem em grupos de consulta LDAP, Windows usuários e grupos e outros grupos de aplicativos básicos.

## <a name="windows-users-and-groups"></a>Windows Usuários e grupos

Eles são os mesmos que os usuários e grupos usados em todo o Windows operacional.

## <a name="ldap-query-groups"></a>Grupos de consultas LDAP

No Gerenciador de Autorização, você pode usar consultas LDAP para corresponder os atributos do usuário com aqueles do objeto do usuário no Active Directory.

Por exemplo, a consulta a seguir localiza todos, exceto Paulo.


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



A consulta a seguir localiza todos os membros do alias alguém em www.fabrikam.com.


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a>Grupos de Aplicativos Básicos

Na API do Gerenciador de Autorização, um grupo de aplicativos é representado por [**um objeto IAzApplicationGroup.**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) Um grupo de aplicativos básico é um tipo de grupo de aplicativos.

Para definir a associação básica do grupo de aplicativos, defina quem é membro e defina quem não é membro. Ambas as etapas são executadas da mesma maneira. Especifique zero ou mais Windows usuários e grupos, grupos de aplicativos básicos definidos anteriormente ou grupos de consulta LDAP. A associação do grupo de aplicativos básico é calculada removendo todos os não membros do grupo. O Gerenciador de Autorização faz isso automaticamente em tempo de operação.

A não membidade em um grupo de aplicativos básico tem precedência sobre a associação.

Definições de associação circular não são permitidas; eles resultam na seguinte mensagem de erro: "Não é possível adicionar GroupName. O seguinte problema ocorreu: um loop foi detectado."

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo grupos de usuários no C++](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 



