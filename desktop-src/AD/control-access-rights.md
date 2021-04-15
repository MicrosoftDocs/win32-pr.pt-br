---
title: Controlar direitos de acesso (AD DS)
description: Todos os objetos no Active Directory Domain Services dão suporte a um conjunto padrão de direitos de acesso definidos na enumeração de enumeração de direitos do ADS \_ \_ .
ms.assetid: 27ad74bd-ad87-422e-a4a2-02c0d51c4dd4
ms.tgt_platform: multiple
keywords:
- Controlar direitos de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 048c4aa685e0c569ef2ac762dcf17366a2394826
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453946"
---
# <a name="control-access-rights-ad-ds"></a>Controlar direitos de acesso (AD DS)

Todos os objetos no Active Directory Domain Services dão suporte a um conjunto padrão de direitos de acesso definidos na enumeração de [**\_ \_ enumeração de direitos do ADS**](/windows/win32/api/iads/ne-iads-ads_rights_enum) . Esses direitos de acesso podem ser usados nas ACEs (entradas de controle de acesso) do descritor de segurança de um objeto para controlar o acesso ao objeto; ou seja, para controlar quem pode executar operações padrão, como criar e excluir objetos filho, ou ler e gravar os atributos de objeto. No entanto, para algumas classes de objeto, pode ser desejável controlar o acesso de uma maneira não compatível com os direitos de acesso padrão. Para facilitar isso, Active Directory Domain Services permitir que o mecanismo de controle de acesso padrão seja estendido por meio do objeto **controlAccessRight** .

Os direitos de acesso de controle são usados de três maneiras:

-   Para direitos estendidos, que são operações especiais não cobertas pelo conjunto padrão de direitos de acesso. Por exemplo, a classe de usuário pode receber um direito "enviar como" que pode ser usado pelo Exchange, Outlook ou qualquer outro aplicativo de email, para determinar se um usuário específico pode ter outro usuário para enviar email em seu nome. Direitos estendidos são criados em objetos **controlAccessRight** definindo o atributo **validAccesses** como igual ao direito de acesso de **\_ \_ \_ \_ acesso de controle DS** (256) direito do ADS.
-   Para definir conjuntos de propriedades, para habilitar o controle de acesso a um subconjunto de atributos de um objeto, em vez de apenas aos atributos individuais. Usando os direitos de acesso padrão, uma única ACE pode conceder ou negar acesso a todos os atributos de um objeto ou a um único atributo. Os direitos de acesso de controle fornecem uma maneira para uma única ACE controlar o acesso a um conjunto de atributos. Por exemplo, a classe User dá suporte ao conjunto de propriedades **Personal-Information** que inclui atributos como endereço e número de telefone. Os direitos de conjunto de propriedades são criados em objetos **controlAccessRight** definindo o atributo **validAccesses** para conter os direitos de acesso **ACTR \_ DS \_ Read \_ prop** (16) e **ACTRL \_ DS \_ Write \_ prop** (32).
-   Para gravações validadas, para exigir que o sistema execute verificação de valor ou validação, além disso, que é exigido pelo esquema, antes de gravar um valor em um atributo em um objeto DS. Isso garante que o valor digitado para o atributo esteja de acordo com a semântica necessária, esteja dentro de um intervalo legal de valores ou que dê uma outra verificação especial que não seria executada para uma gravação simples de baixo nível no atributo. Uma gravação validada é associada a uma permissão especial que é distinta da permissão de "gravação <attribute> " que permite que qualquer valor seja gravado no atributo sem nenhuma verificação de valor realizada. A gravação validada é o único dos três direitos de acesso de controle que não podem ser criados como um novo direito de acesso de controle para um aplicativo. Isso ocorre porque o sistema existente não pode ser modificado de forma programática para impor a validação. Se um direito de acesso de controle tiver sido configurado no sistema como uma gravação validada, o atributo **validAccesses** nos objetos **controlAccessRight** conterá o direito de acesso de **ad \_ \_ \_ Self** (8).

    Há apenas três gravações validadas definidas no esquema de Active Directory do Windows 2000:

    -   Self-Membership permissão em um objeto de grupo, que permite que a conta do chamador, mas nenhuma outra conta seja adicionada ou removida da Associação de um grupo.
    -   A permissão Valid-DNS-Host-Name é validada em um objeto de computador, que permite que um atributo de nome de host DNS em conformidade com o nome do computador e o nome de domínio sejam definidos.
    -   Validou a permissão de SPN em um objeto de computador, que permite um atributo SPN que é compatível com o nome de host DNS do computador a ser definido.

Para sua conveniência, cada direito de acesso de controle é representado por um objeto **controlAccessRight** no contêiner Extended-Rights da partição de configuração, mesmo que os conjuntos de propriedades e as gravações validadas não sejam considerados direitos estendidos. Como o contêiner de configuração é replicado em toda a floresta, os direitos de controle são propagados em todos os domínios em uma floresta. Há vários direitos de acesso de controle predefinidos e, claro, os direitos de acesso personalizados também podem ser definidos.

Todos os direitos de acesso de controle podem ser exibidos como permissões no editor de ACL.

Para obter mais informações e um exemplo de código C++ e Visual Basic que define uma ACE para controlar o acesso de leitura/gravação a um conjunto de propriedades, consulte [código de exemplo para definir uma ACE em um objeto de diretório](example-code-for-setting-an-ace-on-a-directory-object.md).

Para obter mais informações sobre como usar direitos de acesso de controle para controlar o acesso a operações especiais, consulte:

-   [Criando um direito de acesso de controle](creating-a-control-access-right.md)
-   [Definindo uma ACE Right de acesso de controle na ACL de um objeto](setting-a-control-access-right-ace-in-an-objectampaposs-acl.md)
-   [Verificando um direito de acesso de controle na ACL de um objeto](checking-a-control-access-right-in-an-objectampaposs-acl.md)
-   [Lendo um conjunto direito de acesso de controle na ACL de um objeto](reading-a-control-access-right-set-in-an-objectampaposs-acl.md)

 

 