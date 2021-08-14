---
description: Um objeto IAzApplicationGroup representa um grupo de usuários. As funções podem ser atribuídas a esse grupo de usuários coletivamente. Um objeto IAzApplicationGroup também pode incluir outros objetos IAzApplicationGroup como membros.
ms.assetid: 8b445419-7316-4034-b742-a05845af1862
title: Definindo grupos de usuários no script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6198d31a53dbd7d30100a8df56536cf0336c9c1e7ca5b78ad4e9e73e40da13cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118913982"
---
# <a name="defining-groups-of-users-in-script"></a>Definindo grupos de usuários no script

No Gerenciador de Autorização, [**um objeto IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa um grupo de usuários. As funções podem ser atribuídas a esse grupo de usuários coletivamente. Um **objeto IAzApplicationGroup** também pode incluir outros **objetos IAzApplicationGroup** como membros. Para obter mais informações sobre grupos de aplicativos, consulte [Usuários e grupos](users-and-groups.md).

Um grupo pode ser definido por listas explícitas de membros e não membros ou por uma consulta LDAP [*(Lightweight Directory Access Protocol).*](/windows/desktop/SecGloss/l-gly) Os exemplos a seguir mostram como criar cada tipo de grupo de aplicativos:

-   [Criando um grupo básico](#creating-a-basic-group)
-   [Criando um grupo de consultas LDAP](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a>Criando um grupo básico

Um grupo de aplicativos básico é definido pelos membros incluídos nas propriedades [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) e [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) do objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) que representa o grupo. Usuários e grupos listados na propriedade **Membros** são incluídos no grupo de aplicativos e usuários e grupos listados na propriedade **NonMembers** são excluídos do grupo de aplicativos. Estar listado na **propriedade NonMembers** é o que está sendo listado na **propriedade** Members.

O exemplo a seguir mostra como criar um grupo de aplicativos básico e adicionar todos os usuários locais como membros desse grupo. O exemplo supõe que haja um armazenamento de políticas XML existente chamado MyStore.xml no diretório raiz da unidade C.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("Trusted Users")

'  Add a well-known SID for all local users to the group.
appGroup.AddMember("S-1-1-0")

'  Save the application group to the store.
appGroup.Submit
```



## <a name="creating-an-ldap-query-group"></a>Criando um grupo de consultas LDAP

Um grupo de consultas LDAP tem uma associação definida pela consulta contida no valor de sua [**propriedade LdapQuery.**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery)

O exemplo a seguir mostra como criar um grupo de aplicativos de consulta LDAP e adicionar todos os usuários como membros desse grupo. O exemplo supõe que haja um armazenamento de políticas XML existente chamado MyStore.xml no diretório raiz da unidade C.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create an application group object.
Dim appGroup
Set appGroup = expenseApp.CreateApplicationGroup("LDAP Trusted Users")

'  Set the Type property of the group to two
'  (AZ_GROUPTYPE_LDAP_QUERY).
appGroup.Type = 2

'  Add LDAP query for all users.
appGroup.LdapQuery = ("&(objectCategory=person)(objectClass=user)")

'  Save the application group to the store.
appGroup.Submit

```



 

 
