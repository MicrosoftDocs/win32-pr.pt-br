---
title: Controle de direitos de acesso (AD DS)
description: Todos os objetos Active Directory Domain Services suporte a um conjunto padrão de direitos de acesso definidos na enumeração ADS \_ RIGHTS \_ ENUM.
ms.assetid: 27ad74bd-ad87-422e-a4a2-02c0d51c4dd4
ms.tgt_platform: multiple
keywords:
- Controlar direitos de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c975ac20cac683e754f1b703bd272356c9b8df8f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881619"
---
# <a name="control-access-rights-ad-ds"></a>Controle de direitos de acesso (AD DS)

Todos os objetos Active Directory Domain Services dar suporte a um conjunto padrão de direitos de acesso definidos na [**enumeração ADS \_ RIGHTS \_ ENUM.**](/windows/win32/api/iads/ne-iads-ads_rights_enum) Esses direitos de acesso podem ser usados nas ACEs (Entradas de Controle de Acesso) do descritor de segurança de um objeto para controlar o acesso ao objeto; ou seja, para controlar quem pode executar operações padrão, como criar e excluir objetos filho ou ler e escrever os atributos de objeto. No entanto, para algumas classes de objeto, pode ser desejável controlar o acesso de uma maneira sem suporte pelos direitos de acesso padrão. Para facilitar isso, Active Directory Domain Services o mecanismo de controle de acesso padrão seja estendido por meio do **objeto controlAccessRight.**

Os direitos de acesso de controle são usados de três maneiras:

-   Para direitos estendidos, que são operações especiais não cobertas pelo conjunto padrão de direitos de acesso. Por exemplo, a classe de usuário pode ter um direito "Enviar como" que pode ser usado por Exchange, Outlook ou qualquer outro aplicativo de email, para determinar se um usuário específico pode ter outro usuário para enviar emails em seu nome. Os direitos estendidos são criados **em objetos controlAccessRight** definindo o atributo **validAccesses** como igual ao direito de acesso **ADS RIGHT \_ \_ DS CONTROL \_ \_ ACCESS** (256).
-   Para definir conjuntos de propriedades, para habilitar o controle do acesso a um subconjunto dos atributos de um objeto, em vez de apenas aos atributos individuais. Usando os direitos de acesso padrão, uma única ACE pode conceder ou negar acesso a todos os atributos de um objeto ou a um único atributo. Os direitos de acesso de controle fornecem uma maneira para uma única ACE controlar o acesso a um conjunto de atributos. Por exemplo, a classe de usuário dá suporte ao **conjunto de** propriedades Informações Pessoais que inclui atributos como endereço de rua e número de telefone. Os direitos do conjunto de propriedades são criados em objetos **controlAccessRight** definindo o atributo **validAccesses** para conter os direitos de acesso **ACTR \_ DS \_ READ \_ PROP** (16) e **ACTRL \_ DS \_ WRITE \_ PROP** (32).
-   Para gravações validadas, para exigir que o sistema execute a verificação de valor, ou validação, além do que é exigido pelo esquema, antes de escrever um valor em um atributo em um objeto DS. Isso garante que o valor inserido para o atributo esteja em conformidade com a semântica necessária, está dentro de um intervalo legal de valores ou passa por alguma outra verificação especial que não seria executada para uma gravação simples de baixo nível no atributo. Uma gravação validada está associada a uma permissão especial que é diferente da permissão "Atributo de gravação" que permitiria que qualquer valor fosse gravado no atributo sem verificação de &lt; &gt; valor executada. A gravação validada é o único dos três direitos de acesso de controle que não podem ser criados como um novo direito de acesso de controle para um aplicativo. Isso ocorre porque o sistema existente não pode ser modificado programaticamente para impor a validação. Se um direito de acesso de controle tiver sido definido no sistema como uma gravação validada, o atributo **validAccesses** nos objetos **controlAccessRight** conterá o direito de acesso **ADS RIGHT \_ \_ DS \_ SELF** (8).

    Há apenas três gravações validadas definidas no Windows 2000 do Active Directory:

    -   Self-Membership permissão em um objeto Group, que permite que a conta do chamador, mas nenhuma outra conta, seja adicionada ou removida da associação de um grupo.
    -   Permissão Validated-DNS-Host-Name em um objeto Computer, que permite que um atributo de nome de host DNS compatível com o nome do computador e o nome de domínio seja definido.
    -   Permissão Validated-SPN em um objeto Computer, que permite que um atributo SPN compatível com o nome do host DNS do computador seja definido.

Para sua conveniência, cada direito de acesso de controle é representado por um objeto **controlAccessRight** no contêiner Extended-Rights da partição De configuração, embora conjuntos de propriedades e gravações validadas não sejam considerados direitos estendidos. Como o contêiner de Configuração é replicado em toda a floresta, os direitos de controle são propagados em todos os domínios em uma floresta. Há vários direitos de acesso de controle predefinidos e, é claro, direitos de acesso personalizados também podem ser definidos.

Todos os direitos de acesso de controle podem ser exibidos como permissões no Editor de ACL.

Para obter mais informações e um exemplo de código C++ e Visual Basic que define uma ACE para controlar o acesso de leitura/gravação a um conjunto de propriedades, consulte Código de exemplo para definir uma ACE em um [objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).

Para obter mais informações sobre como usar direitos de acesso de controle para controlar o acesso a operações especiais, consulte:

-   [Criando um direito de acesso de controle](creating-a-control-access-right.md)
-   [Definindo um ACE direito de acesso de controle na ACL de um objeto](setting-a-control-access-right-ace-in-an-objectampaposs-acl.md)
-   [Verificando um direito de acesso de controle na ACL de um objeto](checking-a-control-access-right-in-an-objectampaposs-acl.md)
-   [Lendo um conjunto de direitos de acesso de controle na ACL de um objeto](reading-a-control-access-right-set-in-an-objectampaposs-acl.md)

 

 
