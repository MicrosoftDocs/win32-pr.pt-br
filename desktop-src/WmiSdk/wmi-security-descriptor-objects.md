---
description: O WMI tem objetos e métodos que permitem ler e manipular descritores de segurança para determinar quem tem acesso a objetos protegíveis.
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: Objetos do descritor de segurança do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104551353"
---
# <a name="wmi-security-descriptor-objects"></a><span data-ttu-id="8c9fa-103">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="8c9fa-103">WMI Security Descriptor Objects</span></span>

<span data-ttu-id="8c9fa-104">O WMI tem objetos e métodos que permitem ler e manipular descritores de segurança para determinar quem tem acesso a objetos protegíveis.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-104">WMI has objects and methods that allow you to read and manipulate security descriptors to determine who has access to securable objects.</span></span>

-   [<span data-ttu-id="8c9fa-105">A função de descritores de segurança</span><span class="sxs-lookup"><span data-stu-id="8c9fa-105">The Role of Security Descriptors</span></span>](#the-role-of-security-descriptors)
-   [<span data-ttu-id="8c9fa-106">Controle de acesso e objetos de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="8c9fa-106">Access Control and WMI Security Objects</span></span>](#access-control-and-wmi-security-objects)
-   [<span data-ttu-id="8c9fa-107">\_Objeto SecurityDescriptor do Win32</span><span class="sxs-lookup"><span data-stu-id="8c9fa-107">Win32\_SecurityDescriptor Object</span></span>](/windows)
-   [<span data-ttu-id="8c9fa-108">DACL e SACL</span><span class="sxs-lookup"><span data-stu-id="8c9fa-108">DACL and SACL</span></span>](#dacl-and-sacl)
-   [<span data-ttu-id="8c9fa-109">Win32 \_ Ace, confiança do Win32 \_ , \_ SID do Win32</span><span class="sxs-lookup"><span data-stu-id="8c9fa-109">Win32\_ACE, Win32\_Trustee, Win32\_SID</span></span>](/windows)
-   [<span data-ttu-id="8c9fa-110">Exemplo: verificando quem tem acesso às impressoras</span><span class="sxs-lookup"><span data-stu-id="8c9fa-110">Example: Checking Who has Access to Printers</span></span>](#example-checking-who-has-access-to-printers)
-   [<span data-ttu-id="8c9fa-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c9fa-111">Related topics</span></span>](#related-topics)

## <a name="the-role-of-security-descriptors"></a><span data-ttu-id="8c9fa-112">A função de descritores de segurança</span><span class="sxs-lookup"><span data-stu-id="8c9fa-112">The Role of Security Descriptors</span></span>

<span data-ttu-id="8c9fa-113">Os descritores de segurança definem os atributos de segurança de objetos protegíveis, como arquivos, chaves do registro, namespaces do WMI, impressoras, serviços ou compartilhamentos.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-113">Security descriptors define the security attributes of securable objects such as files, registry keys, WMI namespaces, printers, services, or shares.</span></span> <span data-ttu-id="8c9fa-114">Um descritor de segurança contém informações sobre o proprietário e o grupo primário de um objeto.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-114">A security descriptor contains information about the owner and primary group of an object.</span></span> <span data-ttu-id="8c9fa-115">Um provedor pode comparar o descritor de segurança de recurso com a identidade de um usuário solicitante e determinar se o usuário tem o direito de acessar o recurso que um usuário está solicitando.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-115">A provider can compare the resource security descriptor to the identity of a requesting user, and determine whether or not the user has the right to access the resource that a user is requesting.</span></span> <span data-ttu-id="8c9fa-116">Para obter mais informações, consulte [acesso a objetos protegíveis do WMI](access-to-wmi-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8c9fa-116">For more information, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>

<span data-ttu-id="8c9fa-117">Alguns métodos [**WMI, como o obtido**](--systemsecurity-getsd.md), retornam um descritor de segurança no formato de matriz de bytes binários.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-117">Some WMI methods, such as [**GetSD**](--systemsecurity-getsd.md), return a security descriptor in the binary byte array format.</span></span> <span data-ttu-id="8c9fa-118">A partir do Windows Vista, use os métodos da classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) para converter um descritor de segurança binário em uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), que pode ser manipulada com mais facilidade.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-118">Starting with Windows Vista, use the methods of the [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class to convert a binary security descriptor to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), which can be manipulated more easily.</span></span> <span data-ttu-id="8c9fa-119">Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8c9fa-119">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="access-control-and-wmi-security-objects"></a><span data-ttu-id="8c9fa-120">Controle de acesso e objetos de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="8c9fa-120">Access Control and WMI Security Objects</span></span>

<span data-ttu-id="8c9fa-121">A seguir está uma lista de objetos de segurança do WMI:</span><span class="sxs-lookup"><span data-stu-id="8c9fa-121">The following is a list of WMI security objects:</span></span>

-   [<span data-ttu-id="8c9fa-122">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="8c9fa-122">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [<span data-ttu-id="8c9fa-123">**Ace do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="8c9fa-123">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [<span data-ttu-id="8c9fa-124">**Confiança do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="8c9fa-124">**Win32\_Trustee**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [<span data-ttu-id="8c9fa-125">**Sid do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="8c9fa-125">**Win32\_SID**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

<span data-ttu-id="8c9fa-126">O diagrama a seguir mostra as relações entre os objetos de segurança do WMI.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-126">The following diagram shows the relationships among WMI security objects.</span></span>

![relações entre os objetos de segurança do WMI](images/security-descriptor.png)

<span data-ttu-id="8c9fa-128">Para obter mais informações sobre a função de segurança de acesso, consulte [práticas recomendadas de segurança](/windows/desktop/SecBP/best-practices-for-the-security-apis), [mantendo a segurança do WMI](maintaining-wmi-security.md)e o controle de [acesso](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="8c9fa-128">For more information about the role of access security, see [Security Best Practices](/windows/desktop/SecBP/best-practices-for-the-security-apis), [Maintaining WMI Security](maintaining-wmi-security.md), and [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

## <a name="win32_securitydescriptor-object"></a><span data-ttu-id="8c9fa-129">\_Objeto SecurityDescriptor do Win32</span><span class="sxs-lookup"><span data-stu-id="8c9fa-129">Win32\_SecurityDescriptor Object</span></span>

<span data-ttu-id="8c9fa-130">A tabela a seguir lista as propriedades da classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="8c9fa-130">The following table lists the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class properties.</span></span>



| <span data-ttu-id="8c9fa-131">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8c9fa-131">Property</span></span>         | <span data-ttu-id="8c9fa-132">Descrição</span><span class="sxs-lookup"><span data-stu-id="8c9fa-132">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c9fa-133">**ControlFlags**</span><span class="sxs-lookup"><span data-stu-id="8c9fa-133">**ControlFlags**</span></span> | <span data-ttu-id="8c9fa-134">Conjunto de bits de controle que qualifica o significado de um SD ou de seus membros individuais.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-134">Set of control bits that qualify the meaning of an SD or its individual members.</span></span> <span data-ttu-id="8c9fa-135">Para obter mais informações sobre como definir os valores de bit **ControlFlags** , consulte [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="8c9fa-135">For more information about setting the **ControlFlags** bit values, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span><br/>                                                                                                                                                                      |
| <span data-ttu-id="8c9fa-136">**DACL**</span><span class="sxs-lookup"><span data-stu-id="8c9fa-136">**DACL**</span></span>         | <span data-ttu-id="8c9fa-137">[Lista de controle de acesso discricional (ACL)](/windows/desktop/SecAuthZ/access-control-lists) de usuários e grupos e seus direitos de acesso a um objeto protegido.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-137">[Discretionary Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) of users and groups, and their access rights to a secured object.</span></span> <span data-ttu-id="8c9fa-138">Essa propriedade contém uma matriz de instâncias do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) que representam [entradas de controle de acesso](/windows/desktop/SecAuthZ/access-control-entries).</span><span class="sxs-lookup"><span data-stu-id="8c9fa-138">This property contains an array of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instances that represent [Access Control Entries](/windows/desktop/SecAuthZ/access-control-entries).</span></span> <span data-ttu-id="8c9fa-139">Para obter mais informações, consulte [criando uma DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span><span class="sxs-lookup"><span data-stu-id="8c9fa-139">For more information, see [Creating a DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span></span><br/> |
| <span data-ttu-id="8c9fa-140">**Grupo**</span><span class="sxs-lookup"><span data-stu-id="8c9fa-140">**Group**</span></span>        | <span data-ttu-id="8c9fa-141">Grupo ao qual este objeto protegido pertence.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-141">Group to which this secured object belongs.</span></span> <span data-ttu-id="8c9fa-142">Essa propriedade contém uma instância de [**\_ confiança do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que contém o nome, o domínio e o Sid (identificador de segurança) do grupo ao qual o proprietário pertence.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-142">This property contains an instance of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) that contains the name, domain, and security identifier (SID) of the group to which the owner belongs.</span></span><br/>                                                                                                                                                             |
| <span data-ttu-id="8c9fa-143">**Proprietário**</span><span class="sxs-lookup"><span data-stu-id="8c9fa-143">**Owner**</span></span>        | <span data-ttu-id="8c9fa-144">Proprietário deste objeto protegido.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-144">Owner of this secured object.</span></span> <span data-ttu-id="8c9fa-145">Essa propriedade contém uma instância de [ \_ confiança do Win32](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que contém o nome, o domínio e o Sid (identificador de segurança) do proprietário.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-145">This property contains an instance of [Win32\_Trustee](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) that contains the name, domain, and security identifier (SID) of the owner.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="8c9fa-146">**Right**</span><span class="sxs-lookup"><span data-stu-id="8c9fa-146">**SACL**</span></span>         | <span data-ttu-id="8c9fa-147">A [ACL (lista de controle de acesso) do sistema](/windows/desktop/SecAuthZ/access-control-lists) contém uma matriz de instâncias do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) que representam o tipo de tentativas de acesso que geram registros de auditoria para usuários ou grupos.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-147">[System Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) contains an array of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instances that represent the type of access attempts that generate audit records for users or groups.</span></span> <span data-ttu-id="8c9fa-148">Para obter mais informações, consulte [SACL para um novo objeto](/windows/desktop/SecAuthZ/sacl-for-a-new-object).</span><span class="sxs-lookup"><span data-stu-id="8c9fa-148">For more information, see [SACL for a New Object](/windows/desktop/SecAuthZ/sacl-for-a-new-object).</span></span><br/>                                                                        |



 

## <a name="dacl-and-sacl"></a><span data-ttu-id="8c9fa-149">DACL e SACL</span><span class="sxs-lookup"><span data-stu-id="8c9fa-149">DACL and SACL</span></span>

<span data-ttu-id="8c9fa-150">As matrizes de objetos do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) na DACL (lista de controle de acesso discricionário) e na lista de controle de acesso do sistema {SACL) criam um vínculo entre um usuário ou grupo e seus direitos de acesso.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-150">The arrays of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) objects in the discretionary access control list (DACL) and system access control list {SACL) create a link between a user or group and their access rights.</span></span>

<span data-ttu-id="8c9fa-151">Quando uma propriedade DACL não contém uma ACE (entrada de controle de acesso), os direitos de acesso não são concedidos e o acesso ao objeto é negado.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-151">When a DACL property does not contain an access control entry (ACE), access rights are not granted and access to the object is denied.</span></span>

> [!Note]  
> <span data-ttu-id="8c9fa-152">Uma DACL **nula** dá acesso completo a todos, o que é um risco de segurança sério.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-152">A **NULL** DACL gives full access to everyone, which is a serious security risk.</span></span> <span data-ttu-id="8c9fa-153">Para obter mais informações, consulte [criando uma DACL](/windows/desktop/SecBP/creating-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="8c9fa-153">For more information, see [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

 

## <a name="win32_ace-win32_trustee-win32_sid"></a><span data-ttu-id="8c9fa-154">Win32 \_ Ace, confiança do Win32 \_ , \_ SID do Win32</span><span class="sxs-lookup"><span data-stu-id="8c9fa-154">Win32\_ACE, Win32\_Trustee, Win32\_SID</span></span>

<span data-ttu-id="8c9fa-155">Um objeto do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) contém uma instância da classe de [**\_ confiança do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) que identifica um usuário ou grupo e uma propriedade **AccessMask** que é um bitmask, que especifica as ações que um usuário ou grupo pode executar.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-155">A [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) object contains an instance of the [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) class that identifies a user or group, and an **AccessMask** property that is a bitmask, which specifies the actions that a user or group can take.</span></span> <span data-ttu-id="8c9fa-156">Por exemplo, um usuário ou grupo pode receber o direito de ler um arquivo, mas não gravar no arquivo.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-156">For example, a user or group might be granted the right to read a file but not write to the file.</span></span> <span data-ttu-id="8c9fa-157">Um objeto do **Win32 \_ Ace** também contém uma ACE que indica se é ou não um acesso de permissão ou negação.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-157">A **Win32\_ACE** object also contains an ACE that indicates whether or not it is an allow or a deny access.</span></span>

> [!Note]  
> <span data-ttu-id="8c9fa-158">A ordem de [**\_ Ace do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) em uma DACL é importante porque permitir e negar entrada de controle de acesso (ACE) são permitidos em uma DACL.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-158">The [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) order in a DACL is important because both allow and deny access control entry (ACE) are permitted in a DACL.</span></span> <span data-ttu-id="8c9fa-159">Para obter mais informações, consulte [ordem das ACEs em uma DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span><span class="sxs-lookup"><span data-stu-id="8c9fa-159">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

<span data-ttu-id="8c9fa-160">Cada conta de usuário ou grupo representado por [**um \_ confiável do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) tem um SID (identificador de segurança) que identifica exclusivamente uma conta e especifica os privilégios de acesso da conta.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-160">Each user account or group represented by a [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) has a security identifier (SID) that uniquely identifies an account, and specifies the access privileges of the account.</span></span> <span data-ttu-id="8c9fa-161">A maneira como você especifica os dados do SID depende do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-161">How you specify the SID data depends on the operating system.</span></span> <span data-ttu-id="8c9fa-162">Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8c9fa-162">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="8c9fa-163">O diagrama a seguir mostra o conteúdo de uma instância do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) .</span><span class="sxs-lookup"><span data-stu-id="8c9fa-163">The following diagram shows the contents of one [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instance.</span></span>

![conteúdo de uma instância do Win32 \- Ace](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a><span data-ttu-id="8c9fa-165">Exemplo: verificando quem tem acesso às impressoras</span><span class="sxs-lookup"><span data-stu-id="8c9fa-165">Example: Checking Who has Access to Printers</span></span>

<span data-ttu-id="8c9fa-166">O exemplo de código VBScript a seguir mostra como usar o descritor de segurança da impressora.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-166">The following VBScript code example shows how to use the printer security descriptor.</span></span> <span data-ttu-id="8c9fa-167">O script chama o método [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) na classe [**de \_ impressora do Win32**](/windows/desktop/CIMWin32Prov/win32-printer) para obter o descritor e determina se há uma DACL (lista de controle de acesso discricionário) presente no descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-167">The script calls the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) method in the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class to obtain the descriptor then determines if there is a Discretionary Access Control List (DACL) present in the security descriptor.</span></span> <span data-ttu-id="8c9fa-168">Se houver uma DACL, o script obterá a lista de entradas de controle de acesso (ACE) da DACL.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-168">If there is a DACL, then the script obtains the list of Access Control Entries (ACE) from the DACL.</span></span> <span data-ttu-id="8c9fa-169">Cada ACE é representado por uma instância do [**Win32 \_ Ace**](/previous-versions/windows/desktop/secrcw32prov/win32-ace).</span><span class="sxs-lookup"><span data-stu-id="8c9fa-169">Each ACE is represented by an instance of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace).</span></span> <span data-ttu-id="8c9fa-170">O script verifica cada ACE para obter o nome do usuário e determinar se o usuário tem acesso à impressora.</span><span class="sxs-lookup"><span data-stu-id="8c9fa-170">The script checks every ACE to get the name of the user and determine whether the user has access to the printer.</span></span> <span data-ttu-id="8c9fa-171">O usuário é representado por uma instância do [**Win32 \_ Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) inserido na instância do **Win32 \_ Ace** .</span><span class="sxs-lookup"><span data-stu-id="8c9fa-171">The user is represented in by an instance of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) embedded in the **Win32\_ACE** instance.</span></span>


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        colACEs = objSD.DACL
    For Each objACE in colACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="related-topics"></a><span data-ttu-id="8c9fa-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8c9fa-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c9fa-173">Alterando a segurança de acesso em objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="8c9fa-173">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> <dt>

[<span data-ttu-id="8c9fa-174">Classe auxiliar do descritor de segurança</span><span class="sxs-lookup"><span data-stu-id="8c9fa-174">Security Descriptor Helper Class</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[<span data-ttu-id="8c9fa-175">Práticas recomendadas de segurança</span><span class="sxs-lookup"><span data-stu-id="8c9fa-175">Security Best Practices</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[<span data-ttu-id="8c9fa-176">Mantendo a segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="8c9fa-176">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="8c9fa-177">Controle de acesso</span><span class="sxs-lookup"><span data-stu-id="8c9fa-177">Access Control</span></span>](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[<span data-ttu-id="8c9fa-178">Acesso a namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="8c9fa-178">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

