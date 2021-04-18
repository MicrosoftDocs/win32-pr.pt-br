---
description: Grava uma versão atualizada do descritor de segurança que controla o acesso ao namespace do WMI ao qual você está conectado. O descritor de segurança é representado por uma instância de \_ \_ SecurityDescriptor.
ms.assetid: e92430fd-61b1-4986-88dc-b85f502f62e6
ms.tgt_platform: multiple
title: Método SetSecurityDescriptor da classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSecurityDescriptor
api_type:
- COM
api_location:
- All
ms.openlocfilehash: fcdc192801b839451cee256f57090780818d2046
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791549"
---
# <a name="setsecuritydescriptor-method-of-the-__systemsecurity-class"></a><span data-ttu-id="f5b91-104">Método SetSecurityDescriptor da \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="f5b91-104">SetSecurityDescriptor method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="f5b91-105">O método [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) grava uma versão atualizada do descritor de segurança que controla o acesso ao namespace do WMI ao qual você está conectado.</span><span class="sxs-lookup"><span data-stu-id="f5b91-105">The [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) method writes an updated version of the security descriptor that controls access to the WMI namespace to which you are connected.</span></span> <span data-ttu-id="f5b91-106">O descritor de segurança é representado por uma instância de [**\_ \_ SecurityDescriptor**](--securitydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="f5b91-106">The security descriptor is represented by an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span> <span data-ttu-id="f5b91-107">Para obter mais informações, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f5b91-107">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f5b91-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5b91-108">Syntax</span></span>


```mof
uint32 SetSecurityDescriptor(
  [in] __SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a><span data-ttu-id="f5b91-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f5b91-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5b91-110">*Descritor* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f5b91-110">*Descriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5b91-111">O descritor de segurança associado ao namespace WMI.</span><span class="sxs-lookup"><span data-stu-id="f5b91-111">The security descriptor associated with the WMI Namespace.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5b91-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f5b91-112">Return value</span></span>

<span data-ttu-id="f5b91-113">Retorna um dos valores listados na lista a seguir ou um valor diferente para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="f5b91-113">Returns one of the values listed in the following list, or a different value to indicate an error.</span></span> <span data-ttu-id="f5b91-114">Para obter mais informações, consulte [códigos de retorno do WMI](wmi-return-codes.md) ou [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="f5b91-114">For more information, see [WMI Return Codes](wmi-return-codes.md) or [**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="f5b91-115">**0**</span><span class="sxs-lookup"><span data-stu-id="f5b91-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="f5b91-116">Conclusão bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="f5b91-116">Successful completion.</span></span>

</dd> <dt>

<span data-ttu-id="f5b91-117">**2**</span><span class="sxs-lookup"><span data-stu-id="f5b91-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="f5b91-118">O usuário não tem acesso às informações solicitadas.</span><span class="sxs-lookup"><span data-stu-id="f5b91-118">The user does not have access to the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f5b91-119">**8**</span><span class="sxs-lookup"><span data-stu-id="f5b91-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="f5b91-120">Falha desconhecida.</span><span class="sxs-lookup"><span data-stu-id="f5b91-120">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f5b91-121">**9**</span><span class="sxs-lookup"><span data-stu-id="f5b91-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="f5b91-122">O usuário não tem privilégios adequados para executar o método.</span><span class="sxs-lookup"><span data-stu-id="f5b91-122">The user does not have adequate privileges to execute the method.</span></span>

</dd> <dt>

<span data-ttu-id="f5b91-123">**Abril**</span><span class="sxs-lookup"><span data-stu-id="f5b91-123">**21**</span></span>
</dt> <dd>

<span data-ttu-id="f5b91-124">Um parâmetro especificado na chamada do método não é válido.</span><span class="sxs-lookup"><span data-stu-id="f5b91-124">A parameter specified in the method call is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5b91-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5b91-125">Remarks</span></span>

<span data-ttu-id="f5b91-126">A instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) representa um tipo de dados de [**\_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) e contém uma DACL ( [*lista de controle de acesso discricionário*](/windows/desktop/SecGloss/d-gly) ) e uma SACL ( [*lista de controle de acesso*](/windows/desktop/SecGloss/a-gly) ) do sistema.</span><span class="sxs-lookup"><span data-stu-id="f5b91-126">The [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance represents a [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) data type and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL) and a [*System Access Control List*](/windows/desktop/SecGloss/a-gly) (SACL).</span></span> <span data-ttu-id="f5b91-127">Para obter mais informações, consulte [listas de controle de acesso](/windows/desktop/SecAuthZ/access-control-lists).</span><span class="sxs-lookup"><span data-stu-id="f5b91-127">For more information, see [Access Control Lists](/windows/desktop/SecAuthZ/access-control-lists).</span></span>

<span data-ttu-id="f5b91-128">Se **SeSecurityPrivilege** não for concedido ou habilitado ao obter um descritor de segurança, somente a DACL será retornada no descritor de segurança retornado.</span><span class="sxs-lookup"><span data-stu-id="f5b91-128">If the **SeSecurityPrivilege** is not granted or enabled when getting a security descriptor, then only the DACL is returned in the returned security descriptor.</span></span> <span data-ttu-id="f5b91-129">Para obter mais informações, consulte [**constantes de privilégio**](privilege-constants.md) e [executando operações privilegiadas](executing-privileged-operations.md).</span><span class="sxs-lookup"><span data-stu-id="f5b91-129">For more information, see [**Privilege Constants**](privilege-constants.md) and [Executing Privileged Operations](executing-privileged-operations.md).</span></span>

<span data-ttu-id="f5b91-130">Você pode atualizar a DACL e a SACL na instância [**\_ SecurityDescriptor do Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ao chamar esse método, mas também pode atualizar apenas a DACL ou apenas a SACL.</span><span class="sxs-lookup"><span data-stu-id="f5b91-130">You can update both the DACL and the SACL in the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) instance when calling this method, but you also can update only the DACL or only the SACL.</span></span>

<span data-ttu-id="f5b91-131">Os valores a seguir [**no \_ \_ controle do descritor de segurança**](/windows/desktop/SecAuthZ/security-descriptor-control) determinam se a DACL ou a SACL ou ambas são atualizadas.</span><span class="sxs-lookup"><span data-stu-id="f5b91-131">The following values in [**SECURITY\_DESCRIPTOR\_CONTROL**](/windows/desktop/SecAuthZ/security-descriptor-control) determine whether the DACL or the SACL or both are updated.</span></span>

-   <span data-ttu-id="f5b91-132">**\_DACL \_ presente**</span><span class="sxs-lookup"><span data-stu-id="f5b91-132">**SE\_DACL\_PRESENT**</span></span>

    <span data-ttu-id="f5b91-133">Indica que a DACL deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="f5b91-133">Indicates that the DACL should be updated.</span></span> <span data-ttu-id="f5b91-134">Se isso não for definido, o WMI preservará o valor original da DACL.</span><span class="sxs-lookup"><span data-stu-id="f5b91-134">If this is not set then WMI preserves the original value of the DACL.</span></span>

-   <span data-ttu-id="f5b91-135">**\_SACL \_ presente**</span><span class="sxs-lookup"><span data-stu-id="f5b91-135">**SE\_SACL\_PRESENT**</span></span>

    <span data-ttu-id="f5b91-136">Indica que a SACL deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="f5b91-136">Indicates that the SACL should be updated.</span></span> <span data-ttu-id="f5b91-137">Se isso não for definido, o WMI preservará o valor original da SACL.</span><span class="sxs-lookup"><span data-stu-id="f5b91-137">If this is not set then WMI preserves the original value of the SACL.</span></span> <span data-ttu-id="f5b91-138">Para atualizar a SACL, a conta deve ter o privilégio **SeSecurityPrivilege** habilitado.</span><span class="sxs-lookup"><span data-stu-id="f5b91-138">To update the SACL, the account must have the **SeSecurityPrivilege** privilege enabled.</span></span> <span data-ttu-id="f5b91-139">Para scripts, o nome do privilégio é **SeSecurityPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="f5b91-139">For scripting, the privilege name is **SeSecurityPrivilege**.</span></span> <span data-ttu-id="f5b91-140">Para obter mais informações, consulte [**constantes de privilégio**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f5b91-140">For more information, see [**Privilege Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="f5b91-141">Se o grupo de confiança e as propriedades de confiança do proprietário não forem **nulas**, eles serão atualizados.</span><span class="sxs-lookup"><span data-stu-id="f5b91-141">If the Group trustee and the Owner trustee properties are not **NULL**, then they are updated.</span></span> <span data-ttu-id="f5b91-142">Caso contrário, o WMI preservará os valores originais.</span><span class="sxs-lookup"><span data-stu-id="f5b91-142">Otherwise, WMI preserves the original values.</span></span> <span data-ttu-id="f5b91-143">Para obter mais informações, consulte [objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md).</span><span class="sxs-lookup"><span data-stu-id="f5b91-143">For more information, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md).</span></span>

<span data-ttu-id="f5b91-144">Quando uma nova SACL é **nula** em uma chamada desse método, a SACL do descritor de segurança no objeto protegível de destino permanece inalterada.</span><span class="sxs-lookup"><span data-stu-id="f5b91-144">When a new SACL is **NULL** in a call this method, then the security descriptor SACL on the target securable object is left unchanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5b91-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5b91-145">Requirements</span></span>



| <span data-ttu-id="f5b91-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5b91-146">Requirement</span></span> | <span data-ttu-id="f5b91-147">Valor</span><span class="sxs-lookup"><span data-stu-id="f5b91-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="f5b91-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5b91-148">Minimum supported client</span></span><br/> | <span data-ttu-id="f5b91-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5b91-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="f5b91-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5b91-150">Minimum supported server</span></span><br/> | <span data-ttu-id="f5b91-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5b91-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="f5b91-152">Namespace</span><span class="sxs-lookup"><span data-stu-id="f5b91-152">Namespace</span></span><br/>                | <span data-ttu-id="f5b91-153">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="f5b91-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="f5b91-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5b91-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5b91-155">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="f5b91-155">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="f5b91-156">Configurando descritores de segurança namepace</span><span class="sxs-lookup"><span data-stu-id="f5b91-156">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

