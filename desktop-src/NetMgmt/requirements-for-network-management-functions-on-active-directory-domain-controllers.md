---
title: Requisitos para funções de gerenciamento de rede Domínio do Active Directory controladores
description: Se você chamar uma das funções de gerenciamento de rede listadas neste tópico em um controlador de domínio que executa o Active Directory, o acesso a um objeto de proteção será permitido ou negado com base na ACL (lista de controle de acesso) do objeto.
ms.assetid: 4dfb3180-3ca5-4e22-b7a1-4e6b132431fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67326708e2b3c83d1e41ace30c2813ccd2449193530fd4affca450d8a0538961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983255"
---
# <a name="requirements-for-network-management-functions-on-active-directory-domain-controllers"></a>Requisitos para funções de gerenciamento de rede Domínio do Active Directory controladores

Se você chamar uma das funções de gerenciamento de rede listadas neste tópico em um controlador de domínio que executa o Active Directory, o acesso [a](/windows/desktop/SecAuthZ/securable-objects) um objeto de proteção será permitido ou negado com base na ACL [(lista](/windows/desktop/SecAuthZ/access-control-lists) de controle de acesso) do objeto. (AS ACLs são especificadas no diretório.)

Diferentes requisitos de acesso se aplicam a consultas de informações e atualizações de informações.

## <a name="queries"></a>Consultas

Para consultas, a ACL padrão permite que todos os usuários autenticados e membros do grupo " Acesso compatível com[Windows 2000](/windows/desktop/SecAuthZ/allowing-anonymous-access)" para ler e enumerar informações. As funções listadas a seguir são afetadas:

-   [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (somente os níveis 1 e 2)
-   [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (somente os níveis 2 e 502)
-   [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

O acesso anônimo a informações de grupo requer que o usuário Anônimo seja adicionado explicitamente ao grupo "Acesso compatível com Windows 2000". Isso porque os tokens anônimos não incluem o SID de Grupo de Todos.

**Windows 2000:** Por padrão, o grupo "Acesso Windows 2000" inclui Todos como membro. Isso habilita o acesso anônimo (Logon Anônimo) às informações se o sistema permitir acesso anônimo. Os administradores podem remover Todos do grupo "Acesso Windows 2000 Compatível" a qualquer momento. A remoção de Todos do grupo restringe o acesso de informações somente a usuários autenticados. Para obter mais informações sobre acesso anônimo, consulte [Identificadores de segurança](/windows/desktop/SecAuthZ/security-identifiers) e [SIDs conhecidos.](/windows/desktop/SecAuthZ/well-known-sids)

Você pode substituir o padrão do sistema definindo a seguinte chave no Registro como o valor 1:

**HKEY \_ Controle LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ \\ Lsa** \\ **EveryoneIncludesAnonymous** = 1

Consulte [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) e [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum) para obter informações adicionais sobre o acesso anônimo a informações de grupo ao chamar essas duas funções.

## <a name="updates"></a>Atualizações

Para atualizações, a ACL padrão permite que apenas administradores de domínio e operadores de conta escrevam informações. Uma exceção é que os usuários podem alterar sua própria senha e definir o campo de comentário \* \_ usri \_ usr. Outra exceção é que os Operadores de Conta não podem modificar contas de administração. As funções listadas a seguir são afetadas:

-   [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd), [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser), [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel), [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser), [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo), [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers)
-   [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd), [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers), [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel), [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers), [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo), [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers)
-   [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)
-   [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups), [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)

Normalmente, os chamadores devem ter acesso de gravação a todo o objeto para chamadas para [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo), [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) e [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo) para ter êxito. Para um controle de acesso mais fino, você deve considerar o uso da ADSI. Para obter mais informações sobre ADSI, consulte [Interfaces de serviço do Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).

Para obter mais informações sobre como controlar o acesso a objetos de segurança, consulte [Controle](/windows/desktop/SecAuthZ/access-control)de acesso, [privilégios](/windows/desktop/SecAuthZ/privileges)e objetos [de segurança](/windows/desktop/SecAuthZ/securable-objects). Para obter mais informações sobre como chamar funções que exigem privilégios de administrador, consulte [Executando com privilégios especiais](/windows/desktop/SecBP/running-with-special-privileges).

 

 