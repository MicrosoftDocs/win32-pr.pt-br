---
description: Explica a definição de usuários e grupos na API do Gerenciador de autorização.
ms.assetid: 783be0b2-7894-4780-900d-98918f824a04
title: Usuários e Grupos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c40ee9234fa8d6259282855011cfc3fc008d6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749962"
---
# <a name="users-and-groups"></a>Usuários e Grupos

No Gerenciador de autorização, os destinatários da política de autorização são representados pelos seguintes grupos:

-   Usuários e grupos do Windows

    Esses grupos incluem usuários, computadores e grupos internos para entidades de segurança.

-   Grupos de consulta LDAP

    A associação nesses grupos é calculada dinamicamente conforme necessário nas consultas do protocolo LDAP. Um grupo de consulta LDAP é um tipo de grupo de aplicativos.

-   Grupos de aplicativos básicos

    Esses grupos consistem em grupos de consulta LDAP, usuários e grupos do Windows e outros grupos de aplicativos básicos.

## <a name="windows-users-and-groups"></a>Usuários e grupos do Windows

Esses são os mesmos usuários e grupos usados em todo o sistema operacional Windows.

## <a name="ldap-query-groups"></a>Grupos de consulta LDAP

No Gerenciador de autorização, você pode usar consultas LDAP para corresponder os atributos do usuário com aqueles do objeto do usuário em Active Directory.

Por exemplo, a consulta a seguir localiza todos, exceto Andy.


```C++
(&(objectCategory=person)(objectClass=user)(!cn=andy))
```



A consulta a seguir localiza todos os membros do alias de alguém em www.fabrikam.com.


```C++
(memberOf=CN=someone,OU=litwareinc,DC=Fabrikam,DC=com)
```



## <a name="basic-application-groups"></a>Grupos de aplicativos básicos

Na API do Gerenciador de autorização, um grupo de aplicativos é representado por um objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) . Um grupo de aplicativos básico é um tipo de grupo de aplicativos.

Para definir a associação básica do grupo de aplicativos, defina quem é um membro e defina quem não é um membro. Essas duas etapas são executadas da mesma maneira. Especifique zero ou mais usuários e grupos do Windows, grupos de aplicativos básicos definidos anteriormente ou grupos de consulta LDAP. A associação do grupo de aplicativos básico é calculada removendo quaisquer não membros do grupo. O Gerenciador de autorização faz isso automaticamente em tempo de execução.

A não-membro em um grupo de aplicativos básico tem precedência sobre a associação.

Definições de associação circular não são permitidas; Eles resultam na seguinte mensagem de erro: "não é possível adicionar GroupName. Ocorreu o seguinte problema: um loop foi detectado. "

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Definindo grupos de usuários em C++](defining-groups-of-users-in-c--.md)
</dt> </dl>

 

 



