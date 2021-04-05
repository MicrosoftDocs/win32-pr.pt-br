---
description: Atualiza o descritor de segurança de acesso do aplicativo DCOM com um novo descritor de segurança que é definido por uma instância de uma \_ classe Win32 SecurityDescriptor.
ms.assetid: 71b708ba-5eb7-400e-bee2-37ca93966c3f
ms.tgt_platform: multiple
title: Método SetAccessSecurityDescriptor da classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.SetAccessSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53c0975475c5f20682ee77125b66ed703fbb4b9f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826663"
---
# <a name="setaccesssecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="251e9-103">Método SetAccessSecurityDescriptor da classe Win32 \_ DCOMApplicationSetting</span><span class="sxs-lookup"><span data-stu-id="251e9-103">SetAccessSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="251e9-104">O método **SetAccessSecurityDescriptor** atualiza o descritor de segurança de acesso do aplicativo DCOM com um novo descritor de segurança que é definido por uma instância de uma classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="251e9-104">The **SetAccessSecurityDescriptor** method updates the access security descriptor of the DCOM application with a new security descriptor that is defined by an instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="251e9-105">Este descritor de segurança controla quem tem permissão para acessar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="251e9-105">This security descriptor controls who is allowed to access the application.</span></span> <span data-ttu-id="251e9-106">A conta que executa o script ou o aplicativo que chama esse método deve ter os privilégios **SeSecurityPrivilege** e **SeRestorePrivilege** .</span><span class="sxs-lookup"><span data-stu-id="251e9-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privileges.</span></span> <span data-ttu-id="251e9-107">Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="251e9-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="251e9-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="251e9-108">Syntax</span></span>


```mof
uint32 SetAccessSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="251e9-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="251e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="251e9-110">*Descritor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="251e9-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="251e9-111">O descritor de segurança a ser definido para o aplicativo DCOM.</span><span class="sxs-lookup"><span data-stu-id="251e9-111">The security descriptor to set for the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="251e9-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="251e9-112">Return value</span></span>

<span data-ttu-id="251e9-113">Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="251e9-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="251e9-114">Para obter mais informações, consulte [códigos de retorno do WMI](/windows/desktop/WmiSdk/wmi-return-codes) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="251e9-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="251e9-115">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="251e9-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="251e9-116">0</span><span class="sxs-lookup"><span data-stu-id="251e9-116">0</span></span>

<span data-ttu-id="251e9-117">Conclusão bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="251e9-117">Successful completion</span></span>

</dd> <dt>

<span data-ttu-id="251e9-118">**2**</span><span class="sxs-lookup"><span data-stu-id="251e9-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="251e9-119">O usuário não tem acesso às informações solicitadas</span><span class="sxs-lookup"><span data-stu-id="251e9-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="251e9-120">**8**</span><span class="sxs-lookup"><span data-stu-id="251e9-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="251e9-121">Falha desconhecida</span><span class="sxs-lookup"><span data-stu-id="251e9-121">Unknown failure</span></span>

</dd> <dt>

<span data-ttu-id="251e9-122">**9**</span><span class="sxs-lookup"><span data-stu-id="251e9-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="251e9-123">O usuário não tem privilégios adequados para executar o método</span><span class="sxs-lookup"><span data-stu-id="251e9-123">The user does not have adequate privileges to execute the method</span></span>

</dd> <dt>

<span data-ttu-id="251e9-124">**Abril**</span><span class="sxs-lookup"><span data-stu-id="251e9-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="251e9-125">Um parâmetro especificado na chamada do método é inválido</span><span class="sxs-lookup"><span data-stu-id="251e9-125">A parameter specified in the method call is invalid</span></span>

</dd> <dt>

<span data-ttu-id="251e9-126">**Outras**</span><span class="sxs-lookup"><span data-stu-id="251e9-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="251e9-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="251e9-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="251e9-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="251e9-128">Remarks</span></span>

<span data-ttu-id="251e9-129">A instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados de [**\_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) e uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema.</span><span class="sxs-lookup"><span data-stu-id="251e9-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="251e9-130">Para obter mais informações, consulte [listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="251e9-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="251e9-131">Se **SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado.</span><span class="sxs-lookup"><span data-stu-id="251e9-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="251e9-132">Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants) e [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="251e9-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="251e9-133">Você pode atualizar a DACL e a SACL na instância [**\_ SecurityDescriptor do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ao chamar esse método, mas também pode atualizar apenas a DACL ou apenas a SACL.</span><span class="sxs-lookup"><span data-stu-id="251e9-133">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="251e9-134">Os valores a seguir no [**\_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) determinam se a DACL, a SACL ou ambas são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="251e9-134">The following values in the [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="251e9-135">**\_DACL \_ presente**</span><span class="sxs-lookup"><span data-stu-id="251e9-135">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="251e9-136">Indica que a DACL deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="251e9-136">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="251e9-137">Se isso não for definido, o WMI preservará o valor original da DACL.</span><span class="sxs-lookup"><span data-stu-id="251e9-137">If this is not set, then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="251e9-138">**\_SACL \_ presente**</span><span class="sxs-lookup"><span data-stu-id="251e9-138">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="251e9-139">Indica que a SACL deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="251e9-139">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="251e9-140">Se isso não for definido, o WMI preservará o valor original da SACL.</span><span class="sxs-lookup"><span data-stu-id="251e9-140">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="251e9-141">Para atualizar a SACL, a conta deve ter o privilégio **SeSecurityPrivilege** habilitado.</span><span class="sxs-lookup"><span data-stu-id="251e9-141">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="251e9-142">Para scripts, o nome do privilégio é **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="251e9-142">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="251e9-143">Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="251e9-143">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="251e9-144">Se o grupo de confiança e as propriedades de confiança do proprietário não forem **nulas**, eles serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="251e9-144">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="251e9-145">Caso contrário, o WMI preservará os valores originais.</span><span class="sxs-lookup"><span data-stu-id="251e9-145">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="251e9-146">Para obter mais informações, consulte [objetos do descritor de segurança do WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="251e9-146">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="251e9-147">Quando uma nova SACL é **nula** em uma chamada para esse método, a SACL do descritor de segurança no objeto protegível de destino permanece inalterada.</span><span class="sxs-lookup"><span data-stu-id="251e9-147">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="251e9-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="251e9-148">Requirements</span></span>



| <span data-ttu-id="251e9-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="251e9-149">Requirement</span></span> | <span data-ttu-id="251e9-150">Valor</span><span class="sxs-lookup"><span data-stu-id="251e9-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="251e9-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="251e9-151">Minimum supported client</span></span><br/> | <span data-ttu-id="251e9-152">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="251e9-152">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="251e9-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="251e9-153">Minimum supported server</span></span><br/> | <span data-ttu-id="251e9-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="251e9-154">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="251e9-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="251e9-155">Namespace</span></span><br/>                | <span data-ttu-id="251e9-156">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="251e9-156">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="251e9-157">MOF</span><span class="sxs-lookup"><span data-stu-id="251e9-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="251e9-158"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="251e9-158"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="251e9-159">DLL</span><span class="sxs-lookup"><span data-stu-id="251e9-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="251e9-160"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="251e9-160"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="251e9-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="251e9-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="251e9-162">**\_DCOMApplicationSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="251e9-162">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="251e9-163">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="251e9-163">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="251e9-164">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="251e9-164">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="251e9-165">Alterando a segurança de acesso em objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="251e9-165">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

