---
title: Como os descritores de segurança são definidos em novos objetos de diretório
description: Ao criar um novo objeto no Active Directory Domain Services, você pode criar explicitamente um descritor de segurança e, em seguida, definir esse descritor de segurança como a propriedade nTSecurityDescriptor do objeto.
ms.assetid: 07c367f8-cb5a-49ef-8e13-d31673c2ceee
ms.tgt_platform: multiple
keywords:
- o AD de objetos, como descritores de segurança são definidos em novos objetos de diretório
- descritores de segurança AD, como definir em novos objetos de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7858d08944e93165b4a1a63ef7d845ee646dc648
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104453920"
---
# <a name="how-security-descriptors-are-set-on-new-directory-objects"></a>Como os descritores de segurança são definidos em novos objetos de diretório

Ao criar um novo objeto no Active Directory Domain Services, você pode criar explicitamente um descritor de segurança e, em seguida, definir esse descritor de segurança como a propriedade **nTSecurityDescriptor** do objeto. Para obter mais informações, consulte [criando um descritor de segurança para um novo objeto de diretório](creating-a-security-descriptor-for-a-new-directory-object.md).

Active Directory Domain Services use as regras a seguir para definir a DACL no descritor de segurança do novo objeto:

-   Se você especificar explicitamente um descritor de segurança ao criar o objeto, o sistema mesclará quaisquer ACEs herdáveis do objeto pai para a DACL especificada, a menos que o bit de controle da **\_ DACL \_ protegida** seja definido nos bits de controles do descritor de segurança.
-   Se você não especificar um descritor de segurança, o sistema criará a DACL do objeto mesclando quaisquer ACEs herdáveis do objeto pai para a DACL padrão do objeto **classSchema** para a classe do objeto.
-   Se o esquema não tiver uma DACL padrão, a DACL do objeto será a DACL padrão do token primário ou de representação do criador.
-   Se não houver nenhuma DACL especificada, herdada ou padrão, o sistema criará o objeto sem nenhuma DACL, o que permitirá que todos tenham acesso completo ao objeto.

O sistema usa um algoritmo semelhante para criar uma SACL para um objeto de serviço de diretório.

O proprietário e o grupo primário no descritor de segurança do novo objeto são definidos para os valores especificados na propriedade **nTSecurityDescriptor** quando você cria o objeto. Se você não definir esses valores, Active Directory Domain Services use as regras listadas na tabela a seguir para defini-los.



| Regra          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Proprietário         | O proprietário em um descritor de segurança padrão é definido como o SID do proprietário padrão do token primário ou de representação do processo de criação. Para a maioria dos usuários, o SID padrão do proprietário é o mesmo que o SID que identifica a conta do usuário. Lembre-se de que, para os usuários que são membros do grupo de administradores internos, o sistema define automaticamente o SID de proprietário padrão no token de acesso para o grupo de administradores; Portanto, os objetos criados por um membro do grupo Administradores normalmente são de Propriedade do grupo Administradores. Para obter ou definir o proprietário padrão em um token de acesso, chame a função [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) ou [**SetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation) com a estrutura de [**\_ proprietário do token**](/windows/desktop/api/winnt/ns-winnt-token_owner) . |
| Grupo primário | O grupo primário em um descritor de segurança padrão é definido como o grupo primário padrão do token principal ou de representação do criador. Lembre-se de que o grupo primário não é usado no contexto de Active Directory Domain Services.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

Para obter mais informações sobre herança de ACE, consulte [herança e delegação de administração](inheritance-and-delegation-of-administration.md).

Para obter mais informações sobre os descritores de segurança padrão no esquema do, consulte [descriptor de segurança padrão](default-security-descriptor.md).

Para obter mais informações sobre objetos **classSchema** , consulte [Active Directory esquema](active-directory-schema.md).

 

 