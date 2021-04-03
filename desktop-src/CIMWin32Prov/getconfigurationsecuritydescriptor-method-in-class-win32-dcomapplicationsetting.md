---
description: Obtém o descritor de segurança que controla quem tem permissão para configurar um aplicativo DCOM.
ms.assetid: 2858a7a0-1e5b-47aa-9967-0f578c3c22c1
ms.tgt_platform: multiple
title: Método GetConfigurationSecurityDescriptor da classe Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting.GetConfigurationSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 320af05b352641c812c51353c2e7bda0da046bb8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646307"
---
# <a name="getconfigurationsecuritydescriptor-method-of-the-win32_dcomapplicationsetting-class"></a><span data-ttu-id="d8110-103">Método GetConfigurationSecurityDescriptor da classe Win32 \_ DCOMApplicationSetting</span><span class="sxs-lookup"><span data-stu-id="d8110-103">GetConfigurationSecurityDescriptor method of the Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="d8110-104">O método WMI **GetConfigurationSecurityDescriptor** Obtém o descritor de segurança que controla quem tem permissão para configurar um aplicativo DCOM.</span><span class="sxs-lookup"><span data-stu-id="d8110-104">The **GetConfigurationSecurityDescriptor** WMI method gets the security descriptor that controls who is allowed to configure a DCOM application.</span></span> <span data-ttu-id="d8110-105">O descritor de segurança é uma instância da classe [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="d8110-105">The security descriptor is a instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span> <span data-ttu-id="d8110-106">A conta que executa o script ou o aplicativo que chama esse método deve ter os privilégios **SeSecurityPrivilege** e **SeRestorePrivilege** .</span><span class="sxs-lookup"><span data-stu-id="d8110-106">The account running the script or application that calls this method must have the **SeSecurityPrivilege** and **SeRestorePrivilege** privileges.</span></span> <span data-ttu-id="d8110-107">Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span><span class="sxs-lookup"><span data-stu-id="d8110-107">For more information, see [Changing Access Security on Securable Objects](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="d8110-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8110-108">Syntax</span></span>


```mof
uint32 GetConfigurationSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="d8110-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8110-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8110-110">*Descritor* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d8110-110">*Descriptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8110-111">O descritor de segurança a ser definido para o aplicativo DCOM.</span><span class="sxs-lookup"><span data-stu-id="d8110-111">The security descriptor to set for the DCOM application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8110-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8110-112">Return value</span></span>

<span data-ttu-id="d8110-113">Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="d8110-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="d8110-114">Para obter mais informações, consulte [códigos de retorno do WMI](/windows/desktop/WmiSdk/wmi-return-codes) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="d8110-114">For more information, see [WMI Return Codes](/windows/desktop/WmiSdk/wmi-return-codes) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="d8110-115">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="d8110-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="d8110-116">0</span><span class="sxs-lookup"><span data-stu-id="d8110-116">0</span></span>

<span data-ttu-id="d8110-117">Conclusão bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="d8110-117">Successful completion</span></span>

</dd> <dt>

<span data-ttu-id="d8110-118">**2**</span><span class="sxs-lookup"><span data-stu-id="d8110-118">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d8110-119">O usuário não tem acesso às informações solicitadas</span><span class="sxs-lookup"><span data-stu-id="d8110-119">The user does not have access to the requested information</span></span>

</dd> <dt>

<span data-ttu-id="d8110-120">**8**</span><span class="sxs-lookup"><span data-stu-id="d8110-120">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d8110-121">Falha desconhecida</span><span class="sxs-lookup"><span data-stu-id="d8110-121">Unknown failure</span></span>

</dd> <dt>

<span data-ttu-id="d8110-122">**9**</span><span class="sxs-lookup"><span data-stu-id="d8110-122">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d8110-123">O usuário não tem privilégios adequados para executar o método</span><span class="sxs-lookup"><span data-stu-id="d8110-123">The user does not have adequate privileges to execute the method</span></span>

</dd> <dt>

<span data-ttu-id="d8110-124">**Abril**</span><span class="sxs-lookup"><span data-stu-id="d8110-124">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d8110-125">Um parâmetro especificado na chamada do método é inválido</span><span class="sxs-lookup"><span data-stu-id="d8110-125">A parameter specified in the method call is invalid</span></span>

</dd> <dt>

<span data-ttu-id="d8110-126">**Outras**</span><span class="sxs-lookup"><span data-stu-id="d8110-126">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d8110-127">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="d8110-127">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8110-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8110-128">Remarks</span></span>

<span data-ttu-id="d8110-129">A instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados de [**\_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) e uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/s-gly) ) do sistema.</span><span class="sxs-lookup"><span data-stu-id="d8110-129">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="d8110-130">Para obter mais informações, consulte [listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="d8110-130">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="d8110-131">Se **SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado.</span><span class="sxs-lookup"><span data-stu-id="d8110-131">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="d8110-132">Para obter mais informações, consulte [**constantes de privilégio**](/windows/desktop/WmiSdk/privilege-constants) e [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).</span><span class="sxs-lookup"><span data-stu-id="d8110-132">For more information, see [**Privilege Constants**](/windows/desktop/WmiSdk/privilege-constants) and [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="requirements"></a><span data-ttu-id="d8110-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8110-133">Requirements</span></span>



| <span data-ttu-id="d8110-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8110-134">Requirement</span></span> | <span data-ttu-id="d8110-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d8110-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8110-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8110-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d8110-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8110-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d8110-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d8110-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d8110-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8110-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d8110-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="d8110-140">Namespace</span></span><br/>                | <span data-ttu-id="d8110-141">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d8110-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d8110-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d8110-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d8110-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d8110-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d8110-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d8110-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8110-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8110-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8110-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8110-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8110-147">**\_DCOMApplicationSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="d8110-147">**Win32\_DCOMApplicationSetting**</span></span>](win32-dcomapplicationsetting.md)
</dt> <dt>

[<span data-ttu-id="d8110-148">**Constantes de privilégio**</span><span class="sxs-lookup"><span data-stu-id="d8110-148">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="d8110-149">Objetos do descritor de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="d8110-149">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="d8110-150">Alterando a segurança de acesso em objetos protegíveis</span><span class="sxs-lookup"><span data-stu-id="d8110-150">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

