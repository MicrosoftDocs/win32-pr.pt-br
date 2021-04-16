---
title: Delegando unidades organizacionais
description: A empresa Fabrikam contrata dois administradores, Mike e Paul, para gerenciar as unidades organizacionais leste e oeste, respectivamente.
ms.assetid: ecf71ae6-9b6f-4e3c-878a-2c6fd193da33
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9928884c8be19f9668d6f81ed9462f6fb757286f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105754052"
---
# <a name="delegating-organizational-units"></a><span data-ttu-id="b755e-103">Delegando unidades organizacionais</span><span class="sxs-lookup"><span data-stu-id="b755e-103">Delegating Organizational Units</span></span>

<span data-ttu-id="b755e-104">A empresa Fabrikam contrata dois administradores, Mike e Paul, para gerenciar as unidades organizacionais leste e oeste, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b755e-104">The Fabrikam company hires two administrators, Mike and Paul, to manage the East and West organizational units, respectively.</span></span> <span data-ttu-id="b755e-105">Joe Delega suas responsabilidades administrativas a elas para que possam criar e excluir usuários em suas respectivas unidades organizacionais.</span><span class="sxs-lookup"><span data-stu-id="b755e-105">Joe delegates his administrative responsibilities to them so that they can create and delete users in their respective organizational units.</span></span>

<span data-ttu-id="b755e-106">Antes de saber como configurar essas unidades organizacionais em Mike e Paul, você deve entender como configurar o acesso a objetos no Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b755e-106">Before seeing how to set up these organizational units under Mike and Paul, you must understand how to set up access to objects in Active Directory.</span></span> <span data-ttu-id="b755e-107">Cada objeto no Active Directory tem um descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="b755e-107">Each object in Active Directory has a security descriptor.</span></span> <span data-ttu-id="b755e-108">Com o descritor de segurança, você pode modificar permissões no objeto, propagar permissões, habilitar a auditoria e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b755e-108">With the security descriptor, you can modify permissions on the object, propagate permissions, enable auditing, and so on.</span></span> <span data-ttu-id="b755e-109">O descritor de segurança em si tem duas ACLs (listas de controle de acesso): uma DACL (ACL condicional) e uma SACL (ACL do sistema).</span><span class="sxs-lookup"><span data-stu-id="b755e-109">The security descriptor itself has two access control lists (ACLs): a discretionary ACL (DACL) and a system ACL (SACL).</span></span> <span data-ttu-id="b755e-110">Cada ACL pode conter ACEs (entradas de controle de acesso).</span><span class="sxs-lookup"><span data-stu-id="b755e-110">Each ACL can contain access control entries (ACEs).</span></span> <span data-ttu-id="b755e-111">Com uma ACE, você pode definir o acesso permitido ou negado em um objeto.</span><span class="sxs-lookup"><span data-stu-id="b755e-111">With an ACE, you can set allowed or denied access on an object.</span></span> <span data-ttu-id="b755e-112">Além disso, você pode especificar ações específicas para permitir ou negar.</span><span class="sxs-lookup"><span data-stu-id="b755e-112">In addition, you can specify specific actions to allow or deny.</span></span> <span data-ttu-id="b755e-113">Exemplos de ações incluem criar filho, excluir filho, ler Propriedade e gravar propriedade.</span><span class="sxs-lookup"><span data-stu-id="b755e-113">Examples of actions include Create Child, Delete Child, Read Property, and Write Property.</span></span> <span data-ttu-id="b755e-114">Esses direitos são especificados com [**AccessMask**](iadsaccesscontrolentry-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="b755e-114">These rights are specified with the [**AccessMask**](iadsaccesscontrolentry-property-methods.md).</span></span>

<span data-ttu-id="b755e-115">Em seguida, você pode especificar as classes ou os atributos aos quais essa ACE está associada.</span><span class="sxs-lookup"><span data-stu-id="b755e-115">Next, you may specify the classes or attributes to which this ACE is associated.</span></span> <span data-ttu-id="b755e-116">No exemplo da Fabrikam a seguir, Joe escolhe a classe User para que cada administrador possa adicionar usuários ao sistema.</span><span class="sxs-lookup"><span data-stu-id="b755e-116">In the Fabrikam example that follows, Joe picks the user class so that each administrator can add users to the system.</span></span> <span data-ttu-id="b755e-117">Em seguida, você deve responder à pergunta: "quem será o beneficiário desta ACE?"</span><span class="sxs-lookup"><span data-stu-id="b755e-117">Next, you must answer the question: "Who will be the beneficiary of this ACE?"</span></span> <span data-ttu-id="b755e-118">Joe vai especificar Mike.</span><span class="sxs-lookup"><span data-stu-id="b755e-118">Joe will specify Mike.</span></span>

<span data-ttu-id="b755e-119">Por fim, você pode definir o comportamento de herança da ACE — por exemplo, as ACEs podem ser especificadas para propagar a hierarquia.</span><span class="sxs-lookup"><span data-stu-id="b755e-119">Finally, you can set the ACE inheritance behavior—for example, ACEs can be specified to propagate down the hierarchy.</span></span> <span data-ttu-id="b755e-120">Em resumo, o exemplo anterior fará com que Mike seja capaz de criar e excluir objetos de usuário na unidade organizacional vendas leste.</span><span class="sxs-lookup"><span data-stu-id="b755e-120">In summary, the previous example will result in Mike being able to create and delete user objects under the East Sales organizational unit.</span></span>

<span data-ttu-id="b755e-121">Joe usa o exemplo de código a seguir para configurar as ACEs e ACLs na unidade organizacional leste.</span><span class="sxs-lookup"><span data-stu-id="b755e-121">Joe uses the following code example to set up the ACEs and ACLs on the East organizational unit.</span></span>


```VB
Set ou = GetObject("LDAP://OU=East, OU=Sales, DC=Fabrikam,DC=COM")
Set sec = ou.Get("ntSecurityDescriptor")
Set acl = sec.DiscretionaryAcl

Set ace = CreateObject("AccessControlEntry") 
' You can also use Set ace = new ADsAccessControlEntry.

' Grant access to the object.
ace.AceType = ADS_ACETYPE_ACCESS_ALLOWED_OBJECT 

' Create and delete child objects.
ace.AccessMask = ADS_RIGHT_DS_CREATE_CHILD Or ADS_RIGHT_DS_DELETE_CHILD 
' Create the user object with the user schema IDGUID.
ace.ObjectType = "{BF967ABA-0DE6-11D0-A285-00AA003049E2}" 
' Propagate the ACE down.  
ace.AceFlags = ADS_ACEFLAG_INHERIT_ACE
' Provide an option that notifies that the objectType is filled.
ace.Flags = ADS_FLAG_OBJECT_TYPE_PRESENT 
' Show the beneficiary of this ACE.
ace.Trustee = "FABRIKAM\Mike" 
acl.AddAce ace

sec.DiscretionaryAcl = acl
ou.Put "ntSecurityDescriptor", Array(sec)
' Use SetInfo to commit the data to Active Directory.
ou.SetInfo 

' Release the objects.
Set ace = Nothing
Set acl  = Nothing
Set sec = Nothing
```



<span data-ttu-id="b755e-122">A figura a seguir mostra o Active Directory menu **criar novo modo de exibição** após a execução do código.</span><span class="sxs-lookup"><span data-stu-id="b755e-122">The following figure shows the Active Directory **Create New View** menu after the code runs.</span></span> <span data-ttu-id="b755e-123">Quando Joe, o administrador, faz logon, ele vê várias classes que ele pode criar.</span><span class="sxs-lookup"><span data-stu-id="b755e-123">When Joe, the administrator, logs on, he sees several classes that he can create.</span></span> <span data-ttu-id="b755e-124">No entanto, quando Mike fizer logon, ele só poderá criar objetos de usuário.</span><span class="sxs-lookup"><span data-stu-id="b755e-124">However, when Mike logs on, he is able only to create user objects.</span></span>

![menu de opção Criar novo modo de exibição](images/adadsi5.png)

<span data-ttu-id="b755e-126">Para obter mais informações, consulte [modelo de segurança ADSI](adsi-security-model.md).</span><span class="sxs-lookup"><span data-stu-id="b755e-126">For more information, see [ADSI Security Model](adsi-security-model.md).</span></span>

 

 




