---
title: Contextos de segurança e Active Directory Domain Services
description: Quando um aplicativo é associado a um controlador de Domínio do Active Directory (DC), ele faz isso no contexto de segurança de uma entidade de segurança, que pode ser um usuário ou uma entidade, como um computador ou um serviço do sistema.
ms.assetid: 7ad0acbe-f81b-46d6-be87-3526b0bfbd1b
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, contextos de segurança
- contextos de segurança Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c337cb05f8158dbb90f231652c42fb10a486aef4
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007290"
---
# <a name="security-contexts-and-active-directory-domain-services"></a>Contextos de segurança e Active Directory Domain Services

Quando um aplicativo é associado a um controlador de Domínio do Active Directory (DC), ele faz isso no contexto de segurança de uma entidade de segurança, que pode ser um usuário ou uma entidade, como um computador ou um serviço do sistema. O contexto de segurança é a conta de usuário que o sistema usa para impor a segurança quando um thread tenta acessar um objeto protegível. Esses dados incluem o SID (identificador de segurança do usuário), as associações de grupo e os privilégios.

Um usuário estabelece um contexto de segurança apresentando credenciais para autenticação. Se as credenciais forem autenticadas, o sistema produzirá um token de acesso que identifica as associações de grupo e os privilégios associados à conta de usuário. O sistema verifica seu token de acesso quando você tenta acessar um objeto de diretório. Ele compara os dados em seu token de acesso às contas e aos grupos com acesso concedido ou negado pelo descritor de segurança do objeto.

Use os métodos a seguir para controlar o contexto de segurança com o qual você se associa a um Active Directory DC:

-   Associe usando a opção de **\_ \_ autenticação segura do ADS** com a função [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) ou o método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject) e especifique explicitamente um nome de usuário e senha. O sistema autentica essas credenciais e gera um token de acesso que ele usa para a verificação de acesso durante essa associação. Para obter mais informações, consulte [Autenticação](authentication.md).
-   Associe usando a opção de **\_ \_ autenticação segura do ADS** , mas sem especificar credenciais. Se você não estiver representando um usuário, o sistema usará o contexto de segurança primário do seu aplicativo, ou seja, o contexto de segurança do usuário que iniciou seu aplicativo. No caso de um serviço do sistema, esse é o contexto de segurança da conta de serviço ou da conta LocalSystem.
-   Representar um usuário e, em seguida, associar-se à **\_ \_ autenticação segura do ADS**, mas sem especificar credenciais. Nesse caso, o sistema usa o contexto de segurança do cliente que é representado. Para obter mais informações, consulte [representação do cliente](/windows/desktop/SecAuthZ/client-impersonation).
-   Associar usando [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) ou [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/iads/nf-iads-iadsopendsobject-opendsobject) com a opção **ADS \_ sem \_ autenticação** . Esse método é associado sem autenticação e resulta em "todos" como contexto de segurança. Somente o provedor LDAP dá suporte a essa opção.

Se possível, associe sem especificar credenciais. Ou seja, use o contexto de segurança do usuário conectado ou o cliente representado. Isso permite que você evite as credenciais de cache. Se você precisar usar credenciais de usuário alternativas, solicite as credenciais, associe-as a elas, mas não as armazene em cache. Para usar o mesmo contexto de segurança em várias operações de ligação, você pode especificar o nome de usuário e a senha para a primeira operação de ligação e, em seguida, especificar apenas o nome de usuário para fazer as associações subsequentes. Para obter mais informações sobre como usar essa técnica, consulte [autenticação](authentication.md).

Alguns contextos de segurança são mais poderosos do que outros. Por exemplo, a conta LocalSystem em um controlador de domínio tem acesso completo ao Active Directory Domain Services, enquanto que um usuário típico tem acesso limitado a alguns dos objetos no diretório. Em geral, seu aplicativo não deve ser executado em um contexto de segurança avançado, como LocalSystem, quando um contexto de segurança menos potente é suficiente para executar as operações. Isso significa que talvez você queira dividir seu aplicativo em componentes separados, cada um deles executado em um contexto de segurança apropriado para as operações a serem executadas. Por exemplo, a instalação do aplicativo pode ser dividida da seguinte maneira:

-   Execute alterações de esquema e extensões no contexto de um usuário que seja membro do grupo de administradores de esquema.
-   Execute alterações no contêiner de configuração no contexto de um usuário que seja membro do grupo de administradores de empresa.
-   Execute alterações no contêiner de domínio no contexto de um usuário que seja membro do grupo Administradores de domínio.

 

 