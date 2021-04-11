---
description: Grava uma versão atualizada do descritor de segurança que controla o acesso à impressora.
ms.assetid: 6a709043-473e-4b24-8b52-6c68b670ebcf
ms.tgt_platform: multiple
title: Método SetSecurityDescriptor da classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.SetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1572919d0ac0b5c18a6fc5084636c52b9b3ea1c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164175"
---
# <a name="setsecuritydescriptor-method-of-the-win32_printer-class"></a><span data-ttu-id="7a5f6-103">Método SetSecurityDescriptor da classe de \_ impressora Win32</span><span class="sxs-lookup"><span data-stu-id="7a5f6-103">SetSecurityDescriptor method of the Win32\_Printer class</span></span>

<span data-ttu-id="7a5f6-104">O método **SetSecurityDescriptor** grava uma versão atualizada do descritor de segurança que controla o acesso à impressora.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-104">The **SetSecurityDescriptor** method writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="7a5f6-105">O descritor de segurança é uma instância da classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="7a5f6-105">The security descriptor is an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="7a5f6-106">Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="7a5f6-106">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

<span data-ttu-id="7a5f6-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="7a5f6-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="7a5f6-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="7a5f6-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a5f6-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7a5f6-109">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="7a5f6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7a5f6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a5f6-111">*Descritor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7a5f6-111">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a5f6-112">O descritor de segurança associado à impressora.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-112">The security descriptor that is associated with the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a5f6-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7a5f6-113">Return value</span></span>

<span data-ttu-id="7a5f6-114">Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-114">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="7a5f6-115">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="7a5f6-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="7a5f6-116">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="7a5f6-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="7a5f6-117">**0**</span><span class="sxs-lookup"><span data-stu-id="7a5f6-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="7a5f6-118">Conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-118">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="7a5f6-119">**2**</span><span class="sxs-lookup"><span data-stu-id="7a5f6-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="7a5f6-120">O usuário não tem acesso às informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-120">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="7a5f6-121">**8**</span><span class="sxs-lookup"><span data-stu-id="7a5f6-121">**8**</span></span>
</dt> <dd>

<span data-ttu-id="7a5f6-122">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-122">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="7a5f6-123">**9**</span><span class="sxs-lookup"><span data-stu-id="7a5f6-123">**9**</span></span>
</dt> <dd>

<span data-ttu-id="7a5f6-124">O usuário não tem privilégios adequados para executar o método.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-124">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="7a5f6-125">**Abril**</span><span class="sxs-lookup"><span data-stu-id="7a5f6-125">**21**</span></span>
</dt> <dd>

<span data-ttu-id="7a5f6-126">Um parâmetro especificado na chamada do método não é válido.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-126">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a5f6-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="7a5f6-127">Remarks</span></span>

<span data-ttu-id="7a5f6-128">A instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados de [**\_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) e uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-128">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="7a5f6-129">Para obter mais informações, consulte [listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="7a5f6-129">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="7a5f6-130">Se **SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-130">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="7a5f6-131">Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants) e [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="7a5f6-131">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

<span data-ttu-id="7a5f6-132">Você pode atualizar a DACL e a SACL na instância [**\_ SecurityDescriptor do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ao chamar esse método, mas também pode atualizar apenas a DACL ou apenas a SACL.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-132">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you can also update only the DACL or only the SACL.</span></span>

<span data-ttu-id="7a5f6-133">Os valores a seguir [**no \_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) determinam se a DACL, a SACL ou ambas são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-133">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL, the SACL, or both are updated.</span></span>

-   <span data-ttu-id="7a5f6-134">**\_DACL \_ presente**</span><span class="sxs-lookup"><span data-stu-id="7a5f6-134">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="7a5f6-135">Indica que a DACL deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-135">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="7a5f6-136">Se isso não for definido, o WMI preservará o valor original da DACL.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-136">If this is not set then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="7a5f6-137">**\_SACL \_ presente**</span><span class="sxs-lookup"><span data-stu-id="7a5f6-137">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="7a5f6-138">Indica que a SACL deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-138">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="7a5f6-139">Se isso não for definido, o WMI preservará o valor original da SACL.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-139">If this is not set, then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="7a5f6-140">Para atualizar a SACL, a conta deve ter o privilégio **SeSecurityPrivilege** habilitado.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-140">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="7a5f6-141">Para scripts, o nome do privilégio é **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-141">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="7a5f6-142">Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants).</span><span class="sxs-lookup"><span data-stu-id="7a5f6-142">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants).</span></span>

<span data-ttu-id="7a5f6-143">Se o grupo de confiança e as propriedades de confiança do proprietário não forem **nulas**, eles serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-143">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="7a5f6-144">Caso contrário, o WMI preservará os valores originais.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-144">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="7a5f6-145">Para obter mais informações, consulte [objetos do descritor de segurança do WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span><span class="sxs-lookup"><span data-stu-id="7a5f6-145">For more information, see [WMI Security Descriptor Objects](/windows/desktop/WmiSdk/wmi-security-descriptor-objects).</span></span>

<span data-ttu-id="7a5f6-146">Quando uma nova SACL é **nula** em uma chamada para esse método, a SACL do descritor de segurança no objeto protegível de destino permanece inalterada.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-146">When a new SACL is **NULL** in a call to this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="examples"></a><span data-ttu-id="7a5f6-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7a5f6-147">Examples</span></span>

<span data-ttu-id="7a5f6-148">O exemplo do PowerShell [Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) substitui as permissões (ACL) de uma impressora para outra.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-148">The [Copy-ACLToPrinter](https://Gallery.TechNet.Microsoft.Com/Copy-ACLToPrinter-2d66ce19) PowerShell sample Replace the permissions (ACL) from one printer to another.</span></span>

<span data-ttu-id="7a5f6-149">O exemplo de código do PowerShell a seguir descreve como definir o descritor de segurança para uma impressora.</span><span class="sxs-lookup"><span data-stu-id="7a5f6-149">The following PowerShell code sample describes how to set the security descriptor for a printer.</span></span>


```PowerShell
# Specify the user or group
$user = "everyone"

# create instances of necessary classes
$SD = ([WMIClass] "Win32_SecurityDescriptor").CreateInstance()
$ace = ([WMIClass] "Win32_Ace").CreateInstance()
$Trustee = ([WMIClass] "Win32_Trustee").CreateInstance()

# Translate a name of user or group to SID
$SID = (new-object security.principal.ntaccount $user).translate([security.principal.securityidentifier])

# Get binary form from SID and byte Array
[byte[]] $SIDArray = ,0 * $SID.BinaryLength
$SID.GetBinaryForm($SIDArray,0)

# Fill Trustee object parameters
$Trustee.Name = $user
$Trustee.SID = $SIDArray

# Set AccessMask which can contain following values:
# Takeownership - 524288
# ReadPermissions - 131072
# ChangePermissions - 262144
# ManageDocuments - 983088
# ManagePrinters - 983052
# Print + ReadPermissions - 131080
$ace.AccessMask = 983052

# Set AceType. Can be 0 (Allow), or 1 (Deny), or 2 (System Audit)
$ace.AceType = 0
$ace.AceFlags = 0  

# Write Win32_Trustee object to Win32_Ace Trustee property
$ace.Trustee = $Trustee

# Write Win32_Ace and Win32_Trustee objects to SecurityDescriptor object
$SD.DACL = $ace

# Set SE_DACL_PRESENT control flag
$SD.ControlFlags = 0x0004

# Get printer object. For example 'CutePDF Writer' printer object
$Printer = gwmi win32_printer -filter "name = 'CutePDF Writer'"

# Enable SeSecurityPrivilege privilegies
$Printer.psbase.Scope.Options.EnablePrivileges = $true

# Invoke SetSecurityDescriptor method and write new ACE to specified
# printer ACL.
$Printer.SetSecurityDescriptor($SD)
```



## <a name="requirements"></a><span data-ttu-id="7a5f6-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a5f6-150">Requirements</span></span>



| <span data-ttu-id="7a5f6-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a5f6-151">Requirement</span></span> | <span data-ttu-id="7a5f6-152">Valor</span><span class="sxs-lookup"><span data-stu-id="7a5f6-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5f6-153">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a5f6-153">Minimum supported client</span></span><br/> | <span data-ttu-id="7a5f6-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a5f6-154">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="7a5f6-155">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7a5f6-155">Minimum supported server</span></span><br/> | <span data-ttu-id="7a5f6-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a5f6-156">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="7a5f6-157">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a5f6-157">Namespace</span></span><br/>                | <span data-ttu-id="7a5f6-158">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7a5f6-158">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="7a5f6-159">MOF</span><span class="sxs-lookup"><span data-stu-id="7a5f6-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a5f6-160"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="7a5f6-160"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a5f6-161">DLL</span><span class="sxs-lookup"><span data-stu-id="7a5f6-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a5f6-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a5f6-162"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="7a5f6-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="7a5f6-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a5f6-164">**\_Impressora Win32**</span><span class="sxs-lookup"><span data-stu-id="7a5f6-164">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="7a5f6-165">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="7a5f6-165">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="7a5f6-166">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="7a5f6-166">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="7a5f6-167">Alterando a segurança de acesso em objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="7a5f6-167">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

