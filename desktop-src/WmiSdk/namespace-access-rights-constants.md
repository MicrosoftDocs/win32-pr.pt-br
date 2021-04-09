---
description: 'O WMI tem constantes de segurança usadas para verificação de acesso de namespace por \_ \_ SystemSecurity:: GetCallerAccessRights.'
ms.assetid: 2e905078-d510-4417-8acb-a6ff535d9d0b
ms.tgt_platform: multiple
title: Constantes de direitos de acesso de namespace (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEM_ENABLE
- WBEM_METHOD_EXECUTE
- WBEM_FULL_WRITE_REP
- WBEM_PARTIAL_WRITE_REP
- WBEM_WRITE_PROVIDER
- WBEM_REMOTE_ACCESS
api_type:
- HeaderDef
api_location:
- Wbemcli.h
ms.openlocfilehash: 469e036b7cd385fa2ac2bae23e0da081288b536b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010346"
---
# <a name="namespace-access-rights-constants"></a><span data-ttu-id="a9dc9-103">Constantes de direitos de acesso de namespace</span><span class="sxs-lookup"><span data-stu-id="a9dc9-103">Namespace Access Rights Constants</span></span>

<span data-ttu-id="a9dc9-104">O WMI tem constantes de segurança usadas para verificação de acesso de namespace por [**\_ \_ SystemSecurity:: GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md).</span><span class="sxs-lookup"><span data-stu-id="a9dc9-104">WMI has security constants used for namespace access checking by [**\_\_SystemSecurity::GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md).</span></span> <span data-ttu-id="a9dc9-105">Para obter informações de segurança sobre listas de controle de acesso (ACLs, DACLs ou SACLs), consulte [listas de controle de acesso (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) e [**direitos de acesso padrão**](/windows/desktop/SecAuthZ/standard-access-rights).</span><span class="sxs-lookup"><span data-stu-id="a9dc9-105">For security information about access control lists (ACLs, DACLs, or SACLs), see [Access Control Lists (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) and [**Standard Access Rights**](/windows/desktop/SecAuthZ/standard-access-rights).</span></span> <span data-ttu-id="a9dc9-106">Essas constantes são definidas na enumeração **\_ \_ flags de segurança do WBEM** .</span><span class="sxs-lookup"><span data-stu-id="a9dc9-106">These constants are defined in the **WBEM\_SECURITY\_FLAGS** enumeration.</span></span>

<dl> <dt>

<span data-ttu-id="a9dc9-107"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**habilitar o WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="a9dc9-107"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM\_ENABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dc9-108">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="a9dc9-108">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="a9dc9-109">Habilita a conta e concede ao usuário permissões de leitura.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-109">Enables the account and grants the user read permissions.</span></span> <span data-ttu-id="a9dc9-110">Esse é um direito de acesso padrão para todos os usuários e corresponde à permissão habilitar conta na guia Segurança do [*controle WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="a9dc9-110">This is a default access right for all users and corresponds to the Enable Account permission on the Security tab of the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="a9dc9-111">Para obter mais informações, consulte [definindo a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="a9dc9-111">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a9dc9-112"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**\_execução do método WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="a9dc9-112"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM\_METHOD\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dc9-113">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="a9dc9-113">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="a9dc9-114">Permite a execução de métodos.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-114">Allows the execution of methods.</span></span> <span data-ttu-id="a9dc9-115">Os provedores podem executar verificações de acesso adicionais.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-115">Providers can perform additional access checks.</span></span> <span data-ttu-id="a9dc9-116">Esse é um direito de acesso padrão para todos os usuários e corresponde à permissão execute Methods na guia Security do controle WMI.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-116">This is a default access right for all users and corresponds to the Execute Methods permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a9dc9-117"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**\_representante de \_ gravação \_ completa do WBEM**</span><span class="sxs-lookup"><span data-stu-id="a9dc9-117"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM\_FULL\_WRITE\_REP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dc9-118">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="a9dc9-118">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="a9dc9-119">Permite que uma conta de usuário grave em classes no repositório do WMI, bem como em instâncias.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-119">Allows a user account to write to classes in the WMI repository as well as instances.</span></span> <span data-ttu-id="a9dc9-120">Um usuário não pode gravar em classes do sistema.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-120">A user cannot write to system classes.</span></span> <span data-ttu-id="a9dc9-121">Somente os membros do grupo Administradores têm essa permissão.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-121">Only members of the Administrators group have this permission.</span></span> <span data-ttu-id="a9dc9-122">**WBEM \_ O \_ \_ representante de gravação completa** corresponde à permissão de gravação completa na guia Segurança do controle WMI.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-122">**WBEM\_FULL\_WRITE\_REP** corresponds to the Full Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a9dc9-123"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**\_representante de \_ gravação \_ parcial do WBEM**</span><span class="sxs-lookup"><span data-stu-id="a9dc9-123"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM\_PARTIAL\_WRITE\_REP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dc9-124">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="a9dc9-124">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="a9dc9-125">Permite que você grave dados somente em instâncias, não em classes.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-125">Allows you to write data to instances only, not classes.</span></span> <span data-ttu-id="a9dc9-126">Um usuário não pode gravar classes no [*repositório do WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="a9dc9-126">A user cannot write classes to the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="a9dc9-127">Somente os membros do grupo Administradores têm esse direito.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-127">Only members of the Administrators group have this right.</span></span> <span data-ttu-id="a9dc9-128">**WBEM \_ O \_ \_ representante de gravação parcial** corresponde à permissão de gravação parcial na guia Segurança do controle WMI.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-128">**WBEM\_PARTIAL\_WRITE\_REP** corresponds to the Partial Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a9dc9-129"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**\_provedor de gravação WBEM \_**</span><span class="sxs-lookup"><span data-stu-id="a9dc9-129"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM\_WRITE\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dc9-130">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="a9dc9-130">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="a9dc9-131">Permite gravar classes e instâncias em provedores.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-131">Allows writing classes and instances to providers.</span></span> <span data-ttu-id="a9dc9-132">Observe que os provedores podem realizar verificações de acesso adicionais ao representar um usuário.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-132">Note that providers can do additional access checks when impersonating a user.</span></span> <span data-ttu-id="a9dc9-133">Esse é um direito de acesso padrão para todos os usuários e corresponde à permissão de gravação do provedor na guia Segurança do controle WMI.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-133">This is a default access right for all users and corresponds to the Provider Write permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a9dc9-134"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**\_acesso remoto \_ WBEM**</span><span class="sxs-lookup"><span data-stu-id="a9dc9-134"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM\_REMOTE\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9dc9-135">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="a9dc9-135">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="a9dc9-136">Permite que uma conta de usuário execute remotamente qualquer operação permitida pelas permissões descritas acima.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-136">Allows a user account to remotely perform any operations allowed by the permissions described above.</span></span> <span data-ttu-id="a9dc9-137">Somente os membros do grupo Administradores têm esse direito.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-137">Only members of the Administrators group have this right.</span></span> <span data-ttu-id="a9dc9-138">**WBEM \_ O \_ acesso remoto** corresponde à permissão habilitar remota na guia Segurança do controle WMI.</span><span class="sxs-lookup"><span data-stu-id="a9dc9-138">**WBEM\_REMOTE\_ACCESS** corresponds to the Remote Enable permission on the Security tab of the WMI Control.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a9dc9-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9dc9-139">Requirements</span></span>



| <span data-ttu-id="a9dc9-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9dc9-140">Requirement</span></span> | <span data-ttu-id="a9dc9-141">Valor</span><span class="sxs-lookup"><span data-stu-id="a9dc9-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a9dc9-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9dc9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a9dc9-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9dc9-143">Windows Vista</span></span><br/>                                                             |
| <span data-ttu-id="a9dc9-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9dc9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a9dc9-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9dc9-145">Windows Server 2008</span></span><br/>                                                       |
| <span data-ttu-id="a9dc9-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9dc9-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9dc9-147"><dt>Wbemcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9dc9-147"><dt>Wbemcli.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9dc9-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9dc9-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9dc9-149">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="a9dc9-149">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="a9dc9-150">Protegendo namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="a9dc9-150">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="a9dc9-151">Acesso a namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="a9dc9-151">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="a9dc9-152">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="a9dc9-152">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> <dt>

[<span data-ttu-id="a9dc9-153">Alterando a segurança de acesso em objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="a9dc9-153">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

