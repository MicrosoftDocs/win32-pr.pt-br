---
title: Propriedades do usuário personalizado do WinNT
description: O provedor WinNT disponibiliza as seguintes propriedades personalizadas para a classe User. Eles podem ser acessados por meio dos métodos IADs. Get e IADs. put. Para obter mais informações, consulte a \_ estrutura User info \_ 3.
ms.assetid: 3b122424-ff24-4de7-bdaf-693fb4529b09
ms.tgt_platform: multiple
keywords:
- ADSI das propriedades do usuário personalizado do WinNT
- ADSI do provedor WinNT, objeto de usuário, propriedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95230de6f7bb5bd848d7a8a047c0ec1966e5a67e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103917680"
---
# <a name="winnt-custom-user-properties"></a><span data-ttu-id="6b95b-107">Propriedades do usuário personalizado do WinNT</span><span class="sxs-lookup"><span data-stu-id="6b95b-107">WinNT Custom User Properties</span></span>

<span data-ttu-id="6b95b-108">O provedor WinNT disponibiliza as seguintes propriedades personalizadas para a classe User.</span><span class="sxs-lookup"><span data-stu-id="6b95b-108">The WinNT provider makes available the following custom properties for the User class.</span></span> <span data-ttu-id="6b95b-109">Eles podem ser acessados por meio dos métodos [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) .</span><span class="sxs-lookup"><span data-stu-id="6b95b-109">They may be accessed through the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) methods.</span></span> <span data-ttu-id="6b95b-110">Para obter mais informações, consulte a estrutura [**user \_ info \_ 3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) .</span><span class="sxs-lookup"><span data-stu-id="6b95b-110">For more information, see the [**USER\_INFO\_3**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_3) structure.</span></span>



| <span data-ttu-id="6b95b-111">Propriedade</span><span class="sxs-lookup"><span data-stu-id="6b95b-111">Property</span></span>            | <span data-ttu-id="6b95b-112">Type</span><span class="sxs-lookup"><span data-stu-id="6b95b-112">Type</span></span>         | <span data-ttu-id="6b95b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="6b95b-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                   |
|---------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b95b-114">**HomeDirDrive**</span><span class="sxs-lookup"><span data-stu-id="6b95b-114">**HomeDirDrive**</span></span>    | <span data-ttu-id="6b95b-115">String</span><span class="sxs-lookup"><span data-stu-id="6b95b-115">String</span></span>       | <span data-ttu-id="6b95b-116">Unidade do diretório base do usuário.</span><span class="sxs-lookup"><span data-stu-id="6b95b-116">Home Directory Drive of the user.</span></span> <span data-ttu-id="6b95b-117">Esse é um ponteiro para uma cadeia de caracteres Unicode que especifica o caminho do diretório base.</span><span class="sxs-lookup"><span data-stu-id="6b95b-117">This is a pointer to a Unicode string that specifies the path of the home directory.</span></span> <span data-ttu-id="6b95b-118">A cadeia de caracteres pode ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="6b95b-118">The string can be **null**.</span></span> <span data-ttu-id="6b95b-119">Consulte o exemplo neste tópico.</span><span class="sxs-lookup"><span data-stu-id="6b95b-119">See example in this topic.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="6b95b-120">**ObjectSID**</span><span class="sxs-lookup"><span data-stu-id="6b95b-120">**ObjectSID**</span></span>       | <span data-ttu-id="6b95b-121">Cadeia de caracteres de octeto</span><span class="sxs-lookup"><span data-stu-id="6b95b-121">Octet String</span></span> | <span data-ttu-id="6b95b-122">SID de objeto do usuário.</span><span class="sxs-lookup"><span data-stu-id="6b95b-122">Object SID of the user.</span></span> <span data-ttu-id="6b95b-123">Para obter um exemplo de como recuperar o SID do objeto usando o provedor WinNT, consulte [SID do objeto (provedor winnt)](object-sid.md)</span><span class="sxs-lookup"><span data-stu-id="6b95b-123">For an example of how to retrieve the Object SID using the WinNT Provider, see [Object SID (WinNT Provider)](object-sid.md)</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="6b95b-124">**Parâmetros**</span><span class="sxs-lookup"><span data-stu-id="6b95b-124">**Parameters**</span></span>      | <span data-ttu-id="6b95b-125">String</span><span class="sxs-lookup"><span data-stu-id="6b95b-125">String</span></span>       | <span data-ttu-id="6b95b-126">Parâmetros do usuário.</span><span class="sxs-lookup"><span data-stu-id="6b95b-126">Parameters of the user.</span></span> <span data-ttu-id="6b95b-127">Aponta para uma cadeia de caracteres Unicode que é reservada para uso por aplicativos.</span><span class="sxs-lookup"><span data-stu-id="6b95b-127">Points to a Unicode string that is set aside for use by applications.</span></span> <span data-ttu-id="6b95b-128">Essa cadeia de caracteres pode ser uma cadeia de caracteres nula ou pode ter qualquer número de caracteres antes do caractere nulo de terminação.</span><span class="sxs-lookup"><span data-stu-id="6b95b-128">This string can be a null string, or it can have any number of characters before the terminating null character.</span></span> <span data-ttu-id="6b95b-129">Os produtos da Microsoft usam esse membro para armazenar dados de configuração do usuário.</span><span class="sxs-lookup"><span data-stu-id="6b95b-129">Microsoft products use this member to store user configuration data.</span></span> <span data-ttu-id="6b95b-130">Essa propriedade só pode ser modificada por um aplicativo durante a instalação.</span><span class="sxs-lookup"><span data-stu-id="6b95b-130">This property can only be modified by an application during installation.</span></span> |
| <span data-ttu-id="6b95b-131">**Senha**</span><span class="sxs-lookup"><span data-stu-id="6b95b-131">**PasswordAge**</span></span>     | <span data-ttu-id="6b95b-132">Hora</span><span class="sxs-lookup"><span data-stu-id="6b95b-132">Time</span></span>         | <span data-ttu-id="6b95b-133">Duração de tempo da senha em uso.</span><span class="sxs-lookup"><span data-stu-id="6b95b-133">Time duration of the password in use.</span></span> <span data-ttu-id="6b95b-134">Essa propriedade indica o número de segundos decorridos desde que a senha foi alterada pela última vez.</span><span class="sxs-lookup"><span data-stu-id="6b95b-134">This property indicates the number of seconds that have elapsed since the password was last changed.</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="6b95b-135">**PasswordExpired**</span><span class="sxs-lookup"><span data-stu-id="6b95b-135">**PasswordExpired**</span></span> | <span data-ttu-id="6b95b-136">Inteiro</span><span class="sxs-lookup"><span data-stu-id="6b95b-136">Integer</span></span>      | <span data-ttu-id="6b95b-137">Informa quando a senha expirou.</span><span class="sxs-lookup"><span data-stu-id="6b95b-137">Tells when the password was expired.</span></span> <span data-ttu-id="6b95b-138">Quando você usa Get, ele retornará zero será a senha não expirou ou será diferente de zero se tiver expirado.</span><span class="sxs-lookup"><span data-stu-id="6b95b-138">When you use Get, it will return zero is the password has not expired, or nonzero if it has expired.</span></span> <span data-ttu-id="6b95b-139">Consulte o exemplo neste tópico.</span><span class="sxs-lookup"><span data-stu-id="6b95b-139">See example in this topic.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="6b95b-140">**PrimaryGroupID**</span><span class="sxs-lookup"><span data-stu-id="6b95b-140">**PrimaryGroupID**</span></span>  | <span data-ttu-id="6b95b-141">Inteiro</span><span class="sxs-lookup"><span data-stu-id="6b95b-141">Integer</span></span>      | <span data-ttu-id="6b95b-142">ID do grupo primário do usuário, por exemplo, ID do grupo de usuários de domínio.</span><span class="sxs-lookup"><span data-stu-id="6b95b-142">User's primary group ID, for example, domain user group ID.</span></span> <span data-ttu-id="6b95b-143">Consulte o exemplo neste tópico.</span><span class="sxs-lookup"><span data-stu-id="6b95b-143">See example in this topic.</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="6b95b-144">**Sinalizadors de**</span><span class="sxs-lookup"><span data-stu-id="6b95b-144">**UserFlags**</span></span>       | <span data-ttu-id="6b95b-145">Inteiro</span><span class="sxs-lookup"><span data-stu-id="6b95b-145">Integer</span></span>      | <span data-ttu-id="6b95b-146">Sinalizador de usuário definido [**na \_ \_ \_ enumeração de sinalizador de usuário do ADS**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum).</span><span class="sxs-lookup"><span data-stu-id="6b95b-146">User Flag defined in [**ADS\_USER\_FLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum).</span></span> <span data-ttu-id="6b95b-147">Para obter um exemplo de como usar UserFlags, consulte a [senha nunca expira (provedor de winnt)](winnt-password-never-expires.md)</span><span class="sxs-lookup"><span data-stu-id="6b95b-147">For an example of how to use UserFlags, see [Password Never Expires (WinNT Provider)](winnt-password-never-expires.md)</span></span>                                                                                                                                                             |



 

<span data-ttu-id="6b95b-148">Este exemplo mostra como definir o diretório da unidade inicial de um usuário.</span><span class="sxs-lookup"><span data-stu-id="6b95b-148">This example shows how to set a user's Home Drive Directory.</span></span>


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
usr.HomeDirectory = "UserHomeDirHere"
usr.HomeDirDrive = "HomeDirDriveHere"
usr.SetInfo
```



<span data-ttu-id="6b95b-149">Este exemplo mostra como usar PasswordExpired para forçar um usuário a alterar a senha no próximo logon.</span><span class="sxs-lookup"><span data-stu-id="6b95b-149">This example shows how to use PasswordExpired to force a user to change the password at the next logon.</span></span>


```VB
Dim usr As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user")
usr.Put "PasswordExpired", CLng(1)
usr.SetInfo 

'--- Clear this flag so that the user does not have to change the password at next logon.

usr.Put "PasswordExpired", CLng(0)
usr.SetInfo
```



<span data-ttu-id="6b95b-150">Este exemplo mostra como obter o grupo primário do usuário.</span><span class="sxs-lookup"><span data-stu-id="6b95b-150">This example shows how to get the user's primary group.</span></span>


```VB
Dim usr As Object
Dim grpPrimaryID As Object

Set usr = GetObject("WinNT://Fabrikam/jsmith,user") 
grpPrimaryID = usr.Get("PrimaryGroupID")
```



 

 