---
title: Requisitos para funções de gerenciamento de rede em controladores de Domínio do Active Directory
description: Se você chamar uma das funções de gerenciamento de rede listadas neste tópico em um controlador de domínio que executa Active Directory, o acesso a um objeto protegível será permitido ou negado com base na ACL (lista de controle de acesso) do objeto.
ms.assetid: 4dfb3180-3ca5-4e22-b7a1-4e6b132431fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c6b646290ef6352a529a37243a6ea30c8b0d39
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823824"
---
# <a name="requirements-for-network-management-functions-on-active-directory-domain-controllers"></a>Requisitos para funções de gerenciamento de rede em controladores de Domínio do Active Directory

Se você chamar uma das funções de gerenciamento de rede listadas neste tópico em um controlador de domínio que executa Active Directory, o acesso a um [objeto protegível](/windows/desktop/SecAuthZ/securable-objects) será permitido ou negado com base na ACL ( [lista de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists) ) do objeto. (As ACLs são especificadas no diretório.)

Requisitos de acesso diferentes se aplicam a consultas de informações e atualizações de informações.

## <a name="queries"></a>Consultas

Para consultas, a ACL padrão permite que todos os usuários autenticados e membros do grupo "[acesso compatível com o Windows 2000](/windows/desktop/SecAuthZ/allowing-anonymous-access)" leiam e enumerem informações. As funções listadas a seguir são afetadas:

-   [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (somente níveis 1 e 2)
-   [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (somente níveis 2 e 502)
-   [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

O acesso anônimo a informações de grupo exige que o usuário anônimo seja explicitamente adicionado ao grupo "acesso compatível com o Windows 2000". Isso ocorre porque os tokens anônimos não incluem o SID do grupo Everyone.

**Windows 2000:** Por padrão, o grupo "acesso compatível com o Windows 2000" inclui todos como um membro. Isso habilita o acesso anônimo (logon anônimo) a informações se o sistema permitir acesso anônimo. Os administradores podem remover todos do grupo "acesso compatível com o Windows 2000" a qualquer momento. Remover todos do grupo restringe o acesso às informações somente a usuários autenticados. Para obter mais informações sobre o acesso anônimo, consulte [identificadores de segurança](/windows/desktop/SecAuthZ/security-identifiers) e [SIDs conhecidos](/windows/desktop/SecAuthZ/well-known-sids).

Você pode substituir o padrão do sistema definindo a seguinte chave no registro para o valor 1:

**HKEY \_ \_Sistema de máquina local \\ \\ CurrentControlSet \\ controle \\ LSA** \\ **EveryoneIncludesAnonymous** = 1

Consulte [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) e [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum) para obter informações adicionais sobre o acesso anônimo a informações de grupo ao chamar essas duas funções.

## <a name="updates"></a>Atualizações

Para atualizações, a ACL padrão permite que somente administradores de domínio e operadores de conta gravem informações. Uma exceção é que os usuários podem alterar sua própria senha e definir o \* \_ campo de comentário usri usr \_ . Outra exceção é que os operadores de contas não podem modificar contas de administração. As funções listadas a seguir são afetadas:

-   [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd), [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser), [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel), [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser), [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo), [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers)
-   [**NetLocalGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupadd), [**NetLocalGroupAddMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupaddmembers), [**NetLocalGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdel), [**NetLocalGroupDelMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupdelmembers), [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo), [**NetLocalGroupSetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetmembers)
-   [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)
-   [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd), [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword), [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel), [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups), [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)

Normalmente, os chamadores devem ter acesso de gravação ao objeto inteiro para que as chamadas para [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset), [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo), [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) e [**NetLocalGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupsetinfo) tenham sucesso. Para obter um controle de acesso mais preciso, você deve considerar o uso de ADSI. Para obter mais informações sobre ADSI, consulte [Active Directory interfaces de serviço](/windows/desktop/ADSI/active-directory-service-interfaces-adsi).

Para obter mais informações sobre como controlar o acesso a objetos protegíveis, consulte [controle de acesso](/windows/desktop/SecAuthZ/access-control), [privilégios](/windows/desktop/SecAuthZ/privileges)e [objetos protegíveis](/windows/desktop/SecAuthZ/securable-objects). Para obter mais informações sobre como chamar funções que exigem privilégios de administrador, consulte [executando com privilégios especiais](/windows/desktop/SecBP/running-with-special-privileges).

 

 