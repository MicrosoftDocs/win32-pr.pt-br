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
# <a name="defining-groups-of-users-in-script"></a><span data-ttu-id="1f53b-105">Definindo grupos de usuários no script</span><span class="sxs-lookup"><span data-stu-id="1f53b-105">Defining Groups of Users in Script</span></span>

<span data-ttu-id="1f53b-106">No Gerenciador de autorização, um objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) representa um grupo de usuários.</span><span class="sxs-lookup"><span data-stu-id="1f53b-106">In Authorization Manager, an [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object represents a group of users.</span></span> <span data-ttu-id="1f53b-107">As funções podem ser atribuídas a esse grupo de usuários coletivamente.</span><span class="sxs-lookup"><span data-stu-id="1f53b-107">Roles can then be assigned to this group of users collectively.</span></span> <span data-ttu-id="1f53b-108">Um objeto **IAzApplicationGroup** também pode incluir outros objetos **IAzApplicationGroup** como membros.</span><span class="sxs-lookup"><span data-stu-id="1f53b-108">An **IAzApplicationGroup** object can also include other **IAzApplicationGroup** objects as members.</span></span> <span data-ttu-id="1f53b-109">Para obter mais informações sobre grupos de aplicativos, consulte [usuários e grupos](users-and-groups.md).</span><span class="sxs-lookup"><span data-stu-id="1f53b-109">For more information about application groups, see [Users and Groups](users-and-groups.md).</span></span>

<span data-ttu-id="1f53b-110">Um grupo pode ser definido por listas explícitas de membros e não membros ou por uma consulta LDAP ( [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) ).</span><span class="sxs-lookup"><span data-stu-id="1f53b-110">A group can be defined either by explicit lists of members and nonmembers or by a [*Lightweight Directory Access Protocol*](/windows/desktop/SecGloss/l-gly) (LDAP) query.</span></span> <span data-ttu-id="1f53b-111">Os exemplos a seguir mostram como criar cada tipo de grupo de aplicativos:</span><span class="sxs-lookup"><span data-stu-id="1f53b-111">The following examples show how to create each type of application group:</span></span>

-   [<span data-ttu-id="1f53b-112">Criando um grupo básico</span><span class="sxs-lookup"><span data-stu-id="1f53b-112">Creating a Basic Group</span></span>](#creating-a-basic-group)
-   [<span data-ttu-id="1f53b-113">Criando um grupo de consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="1f53b-113">Creating an LDAP Query Group</span></span>](#creating-an-ldap-query-group)

## <a name="creating-a-basic-group"></a><span data-ttu-id="1f53b-114">Criando um grupo básico</span><span class="sxs-lookup"><span data-stu-id="1f53b-114">Creating a Basic Group</span></span>

<span data-ttu-id="1f53b-115">Um grupo de aplicativos básico é definido pelos membros incluídos nas propriedades [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) e [**nonmembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) do objeto [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) que representa o grupo.</span><span class="sxs-lookup"><span data-stu-id="1f53b-115">A basic application group is defined by the members included in the [**Members**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_members) and [**NonMembers**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_nonmembers) properties of the [**IAzApplicationGroup**](/windows/desktop/api/Azroles/nn-azroles-iazapplicationgroup) object that represents the group.</span></span> <span data-ttu-id="1f53b-116">Os usuários e grupos listados na propriedade **Members** são incluídos no grupo de aplicativos, e os usuários e grupos listados na propriedade **nonmembers** são excluídos do grupo de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1f53b-116">Users and groups listed in the **Members** property are included in the application group, and users and groups listed in the **NonMembers** property are excluded from the application group.</span></span> <span data-ttu-id="1f53b-117">Estar listado na propriedade **nonmembers** está sendo listado na propriedade **Members** .</span><span class="sxs-lookup"><span data-stu-id="1f53b-117">Being listed in the **NonMembers** property supersedes being listed in the **Members** property.</span></span>

<span data-ttu-id="1f53b-118">O exemplo a seguir mostra como criar um grupo de aplicativos básico e adicionar todos os usuários locais como membros desse grupo.</span><span class="sxs-lookup"><span data-stu-id="1f53b-118">The following example shows how to create a basic application group and add all local users as members of that group.</span></span> <span data-ttu-id="1f53b-119">O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C.</span><span class="sxs-lookup"><span data-stu-id="1f53b-119">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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



## <a name="creating-an-ldap-query-group"></a><span data-ttu-id="1f53b-120">Criando um grupo de consulta LDAP</span><span class="sxs-lookup"><span data-stu-id="1f53b-120">Creating an LDAP Query Group</span></span>

<span data-ttu-id="1f53b-121">Um grupo de consulta LDAP tem uma associação definida pela consulta contida no valor de sua propriedade [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) .</span><span class="sxs-lookup"><span data-stu-id="1f53b-121">An LDAP query group has a membership defined by the query contained in the value of its [**LdapQuery**](/windows/desktop/api/Azroles/nf-azroles-iazapplicationgroup-get_ldapquery) property.</span></span>

<span data-ttu-id="1f53b-122">O exemplo a seguir mostra como criar um grupo de aplicativos de consulta LDAP e adicionar todos os usuários como membros desse grupo.</span><span class="sxs-lookup"><span data-stu-id="1f53b-122">The following example shows how to create an LDAP query application group and add all users as members of that group.</span></span> <span data-ttu-id="1f53b-123">O exemplo supõe que haja um repositório de política XML existente chamado MyStore.xml no diretório raiz da unidade C.</span><span class="sxs-lookup"><span data-stu-id="1f53b-123">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


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



 

 
