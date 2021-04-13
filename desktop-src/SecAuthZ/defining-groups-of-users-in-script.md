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
ms.openlocfilehash: 4f0b652530167c71fbea7bc23d27434ae458f9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297436"
---
# <a name="defining-groups-of-users-in-script"></a>Definindo grupos de usuários no script

No Gerenciador de autorização, um objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa um grupo de usuários. As funções podem ser atribuídas a esse grupo de usuários coletivamente. Um objeto **IAzApplicationGroup** também pode incluir outros objetos **IAzApplicationGroup** como membros. Para obter mais informações sobre grupos de aplicativos, consulte [usuários e grupos](users-and-groups.md).

Um grupo pode ser definido por listas explícitas de membros e não membros ou por uma consulta LDAP ( [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) ). Os exemplos a seguir mostram como criar cada tipo de grupo de aplicativos:

-   [Criando um grupo básico](#creating-a-basic-group)
-   [Criando um grupo de consulta LDAP](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a>Criando um grupo básico

Um grupo de aplicativos básico é definido pelos membros incluídos nas propriedades [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) e [**nonmembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) do objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) que representa o grupo. Os usuários e grupos listados na propriedade **Members** são incluídos no grupo de aplicativos, e os usuários e grupos listados na propriedade **nonmembers** são excluídos do grupo de aplicativos. Estar listado na propriedade **nonmembers** está sendo listado na propriedade **Members** .

O exemplo a seguir mostra como criar um grupo de aplicativos básico e adicionar todos os usuários locais como membros desse grupo. O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C.


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



## <a name="creating-an-ldap-query-group"></a>Criando um grupo de consulta LDAP

Um grupo de consulta LDAP tem uma associação definida pela consulta contida no valor de sua propriedade [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) .

O exemplo a seguir mostra como criar um grupo de aplicativos de consulta LDAP e adicionar todos os usuários como membros desse grupo. O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C.


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



 

 
