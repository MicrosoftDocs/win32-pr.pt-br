---
title: Configurando e alterando senhas de usuário com o provedor LDAP
description: Para definir uma senha de usuário, use o método IADsUser. SetPassword.
ms.assetid: da3d9861-dd04-406c-9356-db1e4ff0eebc
ms.tgt_platform: multiple
keywords:
- ADSI do provedor LDAP, objeto de usuário, definindo senhas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5488146de271ac1108a904cd85163fad9d7dd205
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104294496"
---
# <a name="setting-and-changing-user-passwords-with-the-ldap-provider"></a>Configurando e alterando senhas de usuário com o provedor LDAP

Para definir uma senha de usuário, use o método [**IADsUser. SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) .

O provedor LDAP para Active Directory usa um dos três processos para definir a senha (diretórios LDAP de terceiros, como iPlanet não use esse processo de autenticação de senha). O método pode variar de acordo com a configuração de rede. Os métodos set password ocorrem na seguinte ordem:

-   Primeiro, o provedor LDAP tenta usar LDAP em uma conexão SSL de 128 bits. Para que o LDAP SSL opere com êxito, o servidor LDAP deve ter o certificado de autenticação de servidor apropriado instalado e os clientes que executam o código ADSI devem confiar na autoridade que emitiu esses certificados. Tanto o servidor quanto o cliente devem oferecer suporte à criptografia de 128 bits.
-   Em segundo lugar, se a conexão SSL não for bem-sucedida, o provedor LDAP tentará usar o Kerberos. No Windows 2000, o Kerberos pode não dar suporte à autenticação entre florestas. Aprimoramentos posteriores ao Kerberos dão suporte à autenticação entre florestas.
-   Terceiro, se o Kerberos não for bem-sucedido, o provedor LDAP tentará uma chamada à API [**NetUserSetInfo**](/windows/desktop/api/lmaccess/nf-lmaccess-netusersetinfo) . Em versões anteriores, a ADSI chamou **NetUserSetInfo** no contexto de segurança no qual o thread estava em execução, e não o contexto de segurança especificado na chamada para [**IADsOpenDSObject. OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) ou [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject). Em versões posteriores, isso foi alterado de forma que o provedor ADSI LDAP representaria o usuário especificado na chamada **OpenDSObject** ao chamar **NetUserSetInfo**.

Para alterar uma senha de usuário, use o método [**IADsUser. ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) . Como [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword), esse método pode usar vários processos para alterar a senha. Os métodos de alteração de senha ocorrem na seguinte ordem:

-   Primeiro, o provedor LDAP tenta usar LDAP em uma conexão SSL de 128 bits.
-   Em segundo lugar, se a conexão 128-SSL não for bem-sucedida, o provedor LDAP tentará uma chamada à API [**NetUserChangePassword**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserchangepassword) . Como [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword), em versões anteriores, o provedor de LDAP ADSI representa as credenciais de usuário passadas usando o método [**IADsOpenDSObject. OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) ou a função [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) .

 

 