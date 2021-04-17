---
description: Tanto os aplicativos C++ quanto os scripts em execução com uma conta de administrador completo podem alterar um descritor de segurança de namespace.
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: Definindo descritores de segurança de namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877b1dfc0ae1a9467b1beb7d169bfa31fdf7395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762433"
---
# <a name="setting-namespace-security-descriptors"></a><span data-ttu-id="ed4e5-103">Definindo descritores de segurança de namespace</span><span class="sxs-lookup"><span data-stu-id="ed4e5-103">Setting Namespace Security Descriptors</span></span>

<span data-ttu-id="ed4e5-104">Tanto os aplicativos C++ quanto os scripts em execução com uma conta de administrador completo podem alterar um descritor de segurança de namespace.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-104">Both C++ applications and scripts running under a full administrator account can change a namespace security descriptor.</span></span>

## <a name="namespace-security-descriptors"></a><span data-ttu-id="ed4e5-105">Descritores de segurança de namespace</span><span class="sxs-lookup"><span data-stu-id="ed4e5-105">Namespace Security Descriptors</span></span>

<span data-ttu-id="ed4e5-106">Cada namespace WMI tem um [*descritor de segurança*](/windows/desktop/SecGloss/s-gly), que permite que cada namespace tenha configurações de segurança exclusivas que determinam quem tem acesso aos dados e métodos do namespace.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-106">Each WMI namespace has a [*security descriptor*](/windows/desktop/SecGloss/s-gly), which allows each namespace to have unique security settings that determine who has access to the namespace data and methods.</span></span> <span data-ttu-id="ed4e5-107">Para obter mais informações sobre a segurança de acesso do WMI, consulte [acesso a objetos protegíveis do WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ed4e5-107">For more information about WMI access security, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span> <span data-ttu-id="ed4e5-108">O [acesso aos namespaces do WMI](access-to-wmi-namespaces.md) descreve as configurações de segurança padrão para namespaces do WMI e auditoria de segurança no WMI.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-108">[Access to WMI Namespaces](access-to-wmi-namespaces.md) describes the default security settings for WMI namespaces and security auditing in WMI.</span></span>

<span data-ttu-id="ed4e5-109">Você pode definir permissões de conta para cada namespace WMI no repositório WMI (CIM) das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="ed4e5-109">You can set account permissions for each WMI namespace in the WMI (CIM) repository in the following ways:</span></span>

-   <span data-ttu-id="ed4e5-110">Quando o namespace é criado no arquivo MOF.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-110">When the namespace is created in the MOF file.</span></span> <span data-ttu-id="ed4e5-111">Para obter mais informações, consulte [definindo a segurança do namespace quando o namespace é criado](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="ed4e5-111">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>
-   <span data-ttu-id="ed4e5-112">Manualmente, usando o controle WMI.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-112">Manually, using the WMI Control.</span></span> <span data-ttu-id="ed4e5-113">Para obter mais informações, consulte [definindo a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="ed4e5-113">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>
-   <span data-ttu-id="ed4e5-114">Programaticamente, chamando os métodos da classe [**\_ \_ SystemSecurity**](--systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="ed4e5-114">Programmatically, by calling the methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class.</span></span>

<span data-ttu-id="ed4e5-115">Os métodos a seguir do objeto [**\_ \_ SystemSecurity**](--systemsecurity.md) associado a cada namespace permitem que você leia ou altere a segurança em um namespace.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-115">The following methods of the [**\_\_SystemSecurity**](--systemsecurity.md) object associated with each namespace allow you to read or change security on a namespace.</span></span>

<dl> <dt>

<span data-ttu-id="ed4e5-116"><span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)</span><span class="sxs-lookup"><span data-stu-id="ed4e5-116"><span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)</span></span>
</dt> <dd>

<span data-ttu-id="ed4e5-117">Define o parâmetro de *direitos* como um bitmap com cada bit correspondente a um direito de acesso.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-117">Sets the *rights* parameter as a bitmap with each bit corresponding to an access right.</span></span>

</dd> <dt>

<span data-ttu-id="ed4e5-118"><span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)</span><span class="sxs-lookup"><span data-stu-id="ed4e5-118"><span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)</span></span>
</dt> <dd>

<span data-ttu-id="ed4e5-119">Obtém o descritor de segurança para o namespace ao qual o usuário está conectado.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-119">Gets the security descriptor for the namespace to which the user is connected.</span></span> <span data-ttu-id="ed4e5-120">Esse método retorna um descritor de segurança em formato de matriz de bytes binários.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-120">This method returns a security descriptor in binary byte array format.</span></span> <span data-ttu-id="ed4e5-121">Se você estiver escrevendo um script, use o método [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) .</span><span class="sxs-lookup"><span data-stu-id="ed4e5-121">If you are writing a script, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="ed4e5-122"><span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)</span><span class="sxs-lookup"><span data-stu-id="ed4e5-122"><span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)</span></span>
</dt> <dd>

<span data-ttu-id="ed4e5-123">Define o descritor de segurança (SD) para o namespace ao qual um usuário está conectado.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-123">Sets the security descriptor (SD) for the namespace to which a user is connected.</span></span> <span data-ttu-id="ed4e5-124">Esse método requer um descritor de segurança em formato de matriz de bytes binários.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-124">This method requires a security descriptor in binary byte array format.</span></span> <span data-ttu-id="ed4e5-125">Se você estiver escrevendo um script, use o método [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) .</span><span class="sxs-lookup"><span data-stu-id="ed4e5-125">If you are writing a script, use the [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="ed4e5-126"><span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)</span><span class="sxs-lookup"><span data-stu-id="ed4e5-126"><span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)</span></span>
</dt> <dd>

<span data-ttu-id="ed4e5-127">Obtém o descritor de segurança que controla o acesso ao namespace WMI associado à instância de [**\_ \_ SystemSecurity**](--systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="ed4e5-127">Gets the security descriptor that controls access to the WMI namespace associated with the instance of [**\_\_SystemSecurity**](--systemsecurity.md).</span></span> <span data-ttu-id="ed4e5-128">O descritor de segurança é retornado como uma instância de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="ed4e5-128">The security descriptor is returned as an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed4e5-129"><span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)</span><span class="sxs-lookup"><span data-stu-id="ed4e5-129"><span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)</span></span>
</dt> <dd>

<span data-ttu-id="ed4e5-130">Grava uma versão atualizada do descritor de segurança que controla o acesso à impressora.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-130">Writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="ed4e5-131">O descritor de segurança é representado por uma instância de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="ed4e5-131">The security descriptor is represented by an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span>

</dd> <dt>

<span data-ttu-id="ed4e5-132"><span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)</span><span class="sxs-lookup"><span data-stu-id="ed4e5-132"><span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)</span></span>
</dt> <dd>

<span data-ttu-id="ed4e5-133">Obtém os direitos de acesso remoto para uma lista de usuários individuais em computadores que executam versões obsoletas do Windows, em que o controle de acesso por meio de descritores de segurança do Windows não está disponível.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-133">Gets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

</dd> <dt>

<span data-ttu-id="ed4e5-134"><span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)</span><span class="sxs-lookup"><span data-stu-id="ed4e5-134"><span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)</span></span>
</dt> <dd>

<span data-ttu-id="ed4e5-135">Define os direitos de acesso remoto para uma lista de usuários individuais em computadores que executam versões obsoletas do Windows, em que o controle de acesso por meio de descritores de segurança do Windows não está disponível.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-135">Sets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

</dd> </dl>

<span data-ttu-id="ed4e5-136">Se você estiver escrevendo scripts, use o [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) e o [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md).</span><span class="sxs-lookup"><span data-stu-id="ed4e5-136">If you are writing scripts, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) and [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md).</span></span> <span data-ttu-id="ed4e5-137">Você pode usar os métodos da classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) para alterar os descritores de segurança.</span><span class="sxs-lookup"><span data-stu-id="ed4e5-137">You can use the methods of the [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class to alter the security descriptors.</span></span>

<span data-ttu-id="ed4e5-138">Se você estiver programando em C++, poderá manipular o descritor de segurança binário usando o [SDDL (Security Descriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)e os métodos de conversão [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) e [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span><span class="sxs-lookup"><span data-stu-id="ed4e5-138">If you are programming in C++, you can manipulate the binary security descriptor using [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="ed4e5-139">Lembre-se de que, a partir do Windows Vista, o UAC ( [controle de conta de usuário](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) ) afeta o acesso aos dados do WMI e o que pode ser configurado com o [*controle WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="ed4e5-139">Be aware that, starting with Windows Vista, [User Account Control](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (UAC) affects access to WMI data and what can be configured with the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="ed4e5-140">Para obter mais informações, consulte [controle de conta de usuário e WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="ed4e5-140">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed4e5-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed4e5-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed4e5-142">Protegendo namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="ed4e5-142">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="ed4e5-143">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="ed4e5-143">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="ed4e5-144">Acesso a namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="ed4e5-144">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="ed4e5-145">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="ed4e5-145">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
