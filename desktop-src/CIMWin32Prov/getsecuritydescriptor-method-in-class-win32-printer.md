---
description: Retorna o descritor de segurança que controla o acesso à impressora.
ms.assetid: c12ca35c-07b3-41ad-98c4-48ee584059d1
ms.tgt_platform: multiple
title: Método GetSecurityDescriptor da classe Win32_Printer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Printer.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c74d79430d15fa136c6edeb2a6e77e79e76b02ca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753981"
---
# <a name="getsecuritydescriptor-method-of-the-win32_printer-class"></a><span data-ttu-id="707db-103">Método GetSecurityDescriptor da classe de \_ impressora Win32</span><span class="sxs-lookup"><span data-stu-id="707db-103">GetSecurityDescriptor method of the Win32\_Printer class</span></span>

<span data-ttu-id="707db-104">O método **GetSecurityDescriptor** retorna o descritor de segurança que controla o acesso à impressora.</span><span class="sxs-lookup"><span data-stu-id="707db-104">The **GetSecurityDescriptor** method returns the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="707db-105">O descritor é retornado como uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="707db-105">The descriptor is returned as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="707db-106">Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="707db-106">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

<span data-ttu-id="707db-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="707db-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="707db-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="707db-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="707db-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="707db-109">Syntax</span></span>


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="707db-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="707db-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="707db-111">*Descritor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="707db-111">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="707db-112">O descritor de segurança associado à impressora.</span><span class="sxs-lookup"><span data-stu-id="707db-112">The security descriptor associated with the printer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="707db-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="707db-113">Return value</span></span>

<span data-ttu-id="707db-114">Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="707db-114">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="707db-115">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="707db-115">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="707db-116">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="707db-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="707db-117">**0**</span><span class="sxs-lookup"><span data-stu-id="707db-117">**0**</span></span>
</dt> <dd>

<span data-ttu-id="707db-118">Conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="707db-118">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="707db-119">**2**</span><span class="sxs-lookup"><span data-stu-id="707db-119">**2**</span></span>
</dt> <dd>

<span data-ttu-id="707db-120">O usuário não tem acesso às informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="707db-120">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="707db-121">**8**</span><span class="sxs-lookup"><span data-stu-id="707db-121">**8**</span></span>
</dt> <dd>

<span data-ttu-id="707db-122">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="707db-122">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="707db-123">**9**</span><span class="sxs-lookup"><span data-stu-id="707db-123">**9**</span></span>
</dt> <dd>

<span data-ttu-id="707db-124">O usuário não tem privilégios adequados para executar o método.</span><span class="sxs-lookup"><span data-stu-id="707db-124">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="707db-125">**Abril**</span><span class="sxs-lookup"><span data-stu-id="707db-125">**21**</span></span>
</dt> <dd>

<span data-ttu-id="707db-126">Um parâmetro especificado na chamada do método não é válido.</span><span class="sxs-lookup"><span data-stu-id="707db-126">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="707db-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="707db-127">Remarks</span></span>

<span data-ttu-id="707db-128">A instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados de [**\_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) e uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema.</span><span class="sxs-lookup"><span data-stu-id="707db-128">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="707db-129">Para obter mais informações, consulte [listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="707db-129">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="707db-130">Se **SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado.</span><span class="sxs-lookup"><span data-stu-id="707db-130">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="707db-131">Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants) e [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="707db-131">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="707db-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="707db-132">Examples</span></span>

<span data-ttu-id="707db-133">O exemplo de código VBScript a seguir lista as impressoras anexadas ao computador local e Obtém o descritor de segurança para cada impressora.</span><span class="sxs-lookup"><span data-stu-id="707db-133">The following VBScript code example lists the printers attached to the local computer and gets the security descriptor for each printer.</span></span> <span data-ttu-id="707db-134">Em seguida, as [*entradas de controle de acesso*](/windows/desktop/SecGloss/a-gly) (ACE) na lista de controle de [*acesso discricional*](/windows/desktop/SecGloss/d-gly) (DACL) são extraídas para determinar quais usuários têm acesso à impressora.</span><span class="sxs-lookup"><span data-stu-id="707db-134">Then the [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACE) in the [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) are extracted to determine which users have access to the printer.</span></span>


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set objWMIService = GetObject("winmgmts:")
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
        arrACEs = objSD.DACL
    For Each objACE in arrACEs
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



## <a name="requirements"></a><span data-ttu-id="707db-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="707db-135">Requirements</span></span>



| <span data-ttu-id="707db-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="707db-136">Requirement</span></span> | <span data-ttu-id="707db-137">Valor</span><span class="sxs-lookup"><span data-stu-id="707db-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="707db-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="707db-138">Minimum supported client</span></span><br/> | <span data-ttu-id="707db-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="707db-139">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="707db-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="707db-140">Minimum supported server</span></span><br/> | <span data-ttu-id="707db-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="707db-141">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="707db-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="707db-142">Namespace</span></span><br/>                | <span data-ttu-id="707db-143">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="707db-143">Root\\CIMV2</span></span><br/>                                                                        |
| <span data-ttu-id="707db-144">MOF</span><span class="sxs-lookup"><span data-stu-id="707db-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="707db-145"><dt>\_Impressora. mof do Win32</dt></span><span class="sxs-lookup"><span data-stu-id="707db-145"><dt>Win32\_Printer.mof</dt></span></span> </dl> |
| <span data-ttu-id="707db-146">DLL</span><span class="sxs-lookup"><span data-stu-id="707db-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="707db-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="707db-147"><dt>CIMWin32.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="707db-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="707db-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="707db-149">**\_Impressora Win32**</span><span class="sxs-lookup"><span data-stu-id="707db-149">**Win32\_Printer**</span></span>](win32-printer.md)
</dt> <dt>

[<span data-ttu-id="707db-150">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="707db-150">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="707db-151">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="707db-151">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="707db-152">Alterando a segurança de acesso em objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="707db-152">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

