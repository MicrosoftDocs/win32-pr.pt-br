---
title: Atributos de objeto de usuário
description: Um objeto de usuário tem vários atributos. Esta seção documenta os principais atributos usados pelo Windows, ferramentas administrativas e o WAB (catálogo de endereços do Windows). Ele não descreve todos os atributos; muitos atributos não são usados para o objeto de usuário.
ms.assetid: c173c5d1-2680-4b9c-961d-251fba6e2c7c
ms.tgt_platform: multiple
keywords:
- AD de atributos de objeto de usuário
- Usuários AD, atributos de objeto de usuário
- Objetos AD, User, Attributes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9c90d8d5f28c41971f5f6910cfb8bef1fafd6f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917097"
---
# <a name="user-object-attributes"></a><span data-ttu-id="cbac5-108">Atributos de objeto de usuário</span><span class="sxs-lookup"><span data-stu-id="cbac5-108">User Object Attributes</span></span>

<span data-ttu-id="cbac5-109">Um objeto de usuário tem vários atributos.</span><span class="sxs-lookup"><span data-stu-id="cbac5-109">A user object has multiple attributes.</span></span> <span data-ttu-id="cbac5-110">Esta seção documenta os principais atributos usados pelo Windows, ferramentas administrativas e o WAB (catálogo de endereços do Windows).</span><span class="sxs-lookup"><span data-stu-id="cbac5-110">This section documents key attributes used by Windows, administrative tools, and the Windows Address Book (WAB).</span></span> <span data-ttu-id="cbac5-111">Ele não descreve todos os atributos; muitos atributos não são usados para o objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="cbac5-111">It does not describe all attributes; many attributes are not used for the user object.</span></span>

<span data-ttu-id="cbac5-112">Alguns atributos são armazenados no diretório, como [**CN**](/windows/desktop/ADSchema/a-cn), [**NTSECURITYDESCRIPTOR**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid)e assim por diante, e replicados para todos os controladores de domínio em um domínio.</span><span class="sxs-lookup"><span data-stu-id="cbac5-112">Some attributes are stored in the directory, such as [**cn**](/windows/desktop/ADSchema/a-cn), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), and so on, and replicated to all domain controllers within a domain.</span></span> <span data-ttu-id="cbac5-113">Um subconjunto desses atributos também é replicado para o catálogo global.</span><span class="sxs-lookup"><span data-stu-id="cbac5-113">A subset of these attributes is also replicated to the global catalog.</span></span>

<span data-ttu-id="cbac5-114">Os atributos não replicados são armazenados em cada controlador de domínio, mas não são replicados em outro lugar, como [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**LastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="cbac5-114">Non-replicated attributes are stored on each domain controller, but are not replicated elsewhere, such as [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount), [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon), [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff), and so on.</span></span> <span data-ttu-id="cbac5-115">Os atributos não replicados são atributos que pertencem a um controlador de domínio específico.</span><span class="sxs-lookup"><span data-stu-id="cbac5-115">The non-replicated attributes are attributes that pertain to a particular domain controller.</span></span> <span data-ttu-id="cbac5-116">Por exemplo, **LastLogon** é a última data e hora em que o logon de rede do usuário foi validado pelo controlador de domínio específico que está retornando a propriedade.</span><span class="sxs-lookup"><span data-stu-id="cbac5-116">For example, **lastLogon** is the last date and time that the user network logon was validated by the particular domain controller that is returning the property.</span></span>

<span data-ttu-id="cbac5-117">Um objeto de usuário também tem atributos construídos que não são armazenados no diretório, mas são calculados pelo controlador de domínio, como [**canônicaname**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedattributes**](/windows/desktop/ADSchema/a-allowedattributes)e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="cbac5-117">A user object also has constructed attributes that are not stored in the directory, but are calculated by the domain controller, such as [**canonicalName**](/windows/desktop/ADSchema/a-canonicalname), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**allowedAttributes**](/windows/desktop/ADSchema/a-allowedattributes), and so on.</span></span>

<span data-ttu-id="cbac5-118">Os atributos para objetos de usuário são classificados como:</span><span class="sxs-lookup"><span data-stu-id="cbac5-118">Attributes for user objects are classified as:</span></span>

<dl> <dt>

<span data-ttu-id="cbac5-119"><span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Atributos de objeto base</span><span class="sxs-lookup"><span data-stu-id="cbac5-119"><span id="Base_Object_Attributes"></span><span id="base_object_attributes"></span><span id="BASE_OBJECT_ATTRIBUTES"></span>Base Object Attributes</span></span>
</dt> <dd>

<span data-ttu-id="cbac5-120">Essa categoria inclui atributos necessários para todos os objetos de diretório, como [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor)e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="cbac5-120">This category includes attributes required for all directory objects, such as [**objectClass**](/windows/desktop/ADSchema/a-objectclass), [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor), and so on.</span></span>

</dd> <dt>

<span data-ttu-id="cbac5-121"><span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Atributos de nomenclatura</span><span class="sxs-lookup"><span data-stu-id="cbac5-121"><span id="Naming_Attributes"></span><span id="naming_attributes"></span><span id="NAMING_ATTRIBUTES"></span>Naming Attributes</span></span>
</dt> <dd>

<span data-ttu-id="cbac5-122">Essa categoria inclui atributos usados para fazer referência ou identificar o objeto, como [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSid**](/windows/desktop/ADSchema/a-objectsid)e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="cbac5-122">This category includes attributes used to refer to or identify the object, such as [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSID**](/windows/desktop/ADSchema/a-objectsid), and so on.</span></span> <span data-ttu-id="cbac5-123">Para obter mais informações sobre atributos de nomenclatura para objetos de usuário, consulte [atributos de nomenclatura de usuário](naming-properties.md).</span><span class="sxs-lookup"><span data-stu-id="cbac5-123">For more information about naming attributes for user objects, see [User Naming Attributes](naming-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbac5-124"><span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Atributos de segurança</span><span class="sxs-lookup"><span data-stu-id="cbac5-124"><span id="Security_Attributes"></span><span id="security_attributes"></span><span id="SECURITY_ATTRIBUTES"></span>Security Attributes</span></span>
</dt> <dd>

<span data-ttu-id="cbac5-125">Essa categoria inclui atributos para logon e controle de acesso.</span><span class="sxs-lookup"><span data-stu-id="cbac5-125">This category includes attributes for logon and access control.</span></span> <span data-ttu-id="cbac5-126">Para obter mais informações sobre atributos de segurança para objetos de usuário, consulte [atributos de segurança do usuário](security-properties.md).</span><span class="sxs-lookup"><span data-stu-id="cbac5-126">For more information about security attributes for user objects, see [User Security Attributes](security-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbac5-127"><span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Atributos do catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="cbac5-127"><span id="Address_Book_Attributes"></span><span id="address_book_attributes"></span><span id="ADDRESS_BOOK_ATTRIBUTES"></span>Address Book Attributes</span></span>
</dt> <dd>

<span data-ttu-id="cbac5-128">Essa categoria inclui atributos para email e dados de usuário.</span><span class="sxs-lookup"><span data-stu-id="cbac5-128">This category includes attributes for email and user data.</span></span> <span data-ttu-id="cbac5-129">Para obter mais informações sobre atributos de catálogo de endereços para objetos de usuário, consulte [atributos de catálogo de endereços de usuário](address-book-properties.md).</span><span class="sxs-lookup"><span data-stu-id="cbac5-129">For more information about address book attributes for user objects, see [User Address Book Attributes](address-book-properties.md).</span></span>

</dd> <dt>

<span data-ttu-id="cbac5-130"><span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Atributos específicos do aplicativo</span><span class="sxs-lookup"><span data-stu-id="cbac5-130"><span id="Application_Specific_Attributes"></span><span id="application_specific_attributes"></span><span id="APPLICATION_SPECIFIC_ATTRIBUTES"></span>Application Specific Attributes</span></span>
</dt> <dd>

<span data-ttu-id="cbac5-131">Essa categoria inclui dados de configuração específicos do usuário para aplicativos específicos.</span><span class="sxs-lookup"><span data-stu-id="cbac5-131">This category includes user-specific configuration data for specific applications.</span></span>

</dd> </dl>

<span data-ttu-id="cbac5-132">Para obter mais informações sobre como ler e modificar atributos para um objeto de usuário, consulte [lendo e gravando atributos de objetos no Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="cbac5-132">For more information about reading and modifying attributes for a user object, see [Reading and Writing Attributes of Objects in Active Directory Domain Services](reading-and-writing-attributes-of-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="cbac5-133">Para obter mais informações sobre a classe User, incluindo uma lista completa dos atributos [**mayContain**](/windows/desktop/ADSchema/a-maycontain) e [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) da classe, consulte [**User**](/windows/desktop/ADSchema/c-user).</span><span class="sxs-lookup"><span data-stu-id="cbac5-133">For more information about the User class, including a complete list of the [**mayContain**](/windows/desktop/ADSchema/a-maycontain) and [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) attributes of the class, see [**User**](/windows/desktop/ADSchema/c-user).</span></span>

## <a name="setting-passwords"></a><span data-ttu-id="cbac5-134">Definindo senhas</span><span class="sxs-lookup"><span data-stu-id="cbac5-134">Setting Passwords</span></span>

<span data-ttu-id="cbac5-135">A senha para um usuário não pode ser modificada diretamente porque isso envolveria o envio de uma senha não criptografada pela rede.</span><span class="sxs-lookup"><span data-stu-id="cbac5-135">The password for a user cannot be modified directly because this would involve sending an unencrypted password over the network.</span></span> <span data-ttu-id="cbac5-136">Para definir a senha para um usuário, é necessário usar o método [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) ou [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) .</span><span class="sxs-lookup"><span data-stu-id="cbac5-136">To set the password for a user, it is necessary to use the [**IADsUser.ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) or [**IADsUser.SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) method.</span></span> <span data-ttu-id="cbac5-137">O método **IADsUser. ChangePassword** é usado quando o aplicativo está permitindo que o usuário altere sua própria senha.</span><span class="sxs-lookup"><span data-stu-id="cbac5-137">The **IADsUser.ChangePassword** method is used when the application is allowing the user to change their own password.</span></span> <span data-ttu-id="cbac5-138">O método **IADsUser. SetPassword** é usado quando o aplicativo permite que um administrador redefina uma senha.</span><span class="sxs-lookup"><span data-stu-id="cbac5-138">The **IADsUser.SetPassword** method is used when the application enables an administrator to reset a password.</span></span>

 

 