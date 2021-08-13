---
title: Configurando e alterando senhas de usuário com o provedor LDAP
description: Para definir uma senha de usuário, use o método IADsUser.SetPassword.
ms.assetid: da3d9861-dd04-406c-9356-db1e4ff0eebc
ms.tgt_platform: multiple
keywords:
- ADSI do provedor LDAP, objeto de usuário, Definindo senhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbbd0439a011575fbc9278dbe506d46db2210ce03d807ea74097499cb764b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690521"
---
# <a name="setting-and-changing-user-passwords-with-the-ldap-provider"></a>Configurando e alterando senhas de usuário com o provedor LDAP

Para definir uma senha de usuário, use o [**método IADsUser.SetPassword.**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword)

O provedor LDAP para Active Directory usa um dos três processos para definir a senha (diretórios LDAP de terceiros, como iPlanet, não usam esse processo de autenticação de senha). O método pode variar de acordo com a configuração de rede. Os métodos set password ocorrem na seguinte ordem:

-   Primeiro, o provedor LDAP tenta usar lDAP em uma conexão SSL de 128 bits. Para que o SSL LDAP opere com êxito, o servidor LDAP deve ter o certificado de autenticação de servidor apropriado instalado e os clientes que executam o código ADSI devem confiar na autoridade que emitiu esses certificados. O servidor e o cliente devem dar suporte à criptografia de 128 bits.
-   Em segundo lugar, se a conexão SSL não for bem-sucedida, o provedor LDAP tentará usar Kerberos. No Windows 2000, o Kerberos pode não dar suporte à autenticação entre florestas. Aprimoramentos posteriores no Kerberos são suportados pela autenticação entre florestas.
-   Em terceiro lugar, se Kerberos não for bem-sucedido, o provedor LDAP tentará uma chamada à API [**NetUserSetInfo.**](/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo) Em versões anteriores, o ADSI chamado **NetUserSetInfo** no contexto de segurança no qual o thread estava em execução e não o contexto de segurança especificado na chamada para [**IADsOpenDSObject.OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) [**ou ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject). Em versões posteriores, isso foi alterado para que o provedor ADSI LDAP representasse o usuário especificado na chamada **OpenDSObject** quando chama **NetUserSetInfo**.

Para alterar uma senha de usuário, use o [**método IADsUser.ChangePassword.**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) Como [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword), esse método pode usar vários processos para alterar a senha. Os métodos de alteração de senha ocorrem na seguinte ordem:

-   Primeiro, o provedor LDAP tenta usar lDAP em uma conexão SSL de 128 bits.
-   Em segundo lugar, se a conexão 128-SSL não for bem-sucedida, o provedor LDAP tentará uma chamada à API [**NetUserChangePassword.**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserchangepassword) Como [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword), em versões anteriores, o provedor ADSI LDAP representa as credenciais do usuário passadas usando o método [**IADsOpenDSObject.OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) ou [**a função ADsOpenObject.**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)

 

 