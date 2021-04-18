---
description: Define o parâmetro de direitos como um bitmap com cada bit correspondente a um direito de acesso.
ms.assetid: f28391a8-2b34-4234-bf1a-4688726b0b4b
ms.tgt_platform: multiple
title: Método GetCallerAccessRights da classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.GetCallerAccessRights
api_type:
- COM
api_location:
- All
ms.openlocfilehash: c86ea3044411e33026ed6328fcfc227e615648b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796178"
---
# <a name="getcalleraccessrights-method-of-the-__systemsecurity-class"></a><span data-ttu-id="3a579-103">Método GetCallerAccessRights da \_ \_ classe SystemSecurity</span><span class="sxs-lookup"><span data-stu-id="3a579-103">GetCallerAccessRights method of the \_\_SystemSecurity class</span></span>

<span data-ttu-id="3a579-104">O método **\_ \_ SystemSecurity:: GetCallerAccessRights** define o parâmetro *Rights* como um bitmap com cada bit correspondente a um direito de acesso.</span><span class="sxs-lookup"><span data-stu-id="3a579-104">The **\_\_SystemSecurity::GetCallerAccessRights** method sets the *rights* parameter as a bitmap with each bit corresponding to an access right.</span></span> <span data-ttu-id="3a579-105">Qualquer cliente pode chamá-lo para determinar quais direitos o cliente tem.</span><span class="sxs-lookup"><span data-stu-id="3a579-105">Any client can call this to determine which rights the client has.</span></span> <span data-ttu-id="3a579-106">Esse método é útil para clientes que habilitam ou desabilitam recursos.</span><span class="sxs-lookup"><span data-stu-id="3a579-106">This method is useful for clients that enable or disable features.</span></span> <span data-ttu-id="3a579-107">Por exemplo, um aplicativo de GUI pode desabilitar um botão se o usuário conectado no momento não tiver direitos de execução de método.</span><span class="sxs-lookup"><span data-stu-id="3a579-107">For example, a GUI application might disable a button if the currently logged-on user does not have method execution rights.</span></span>

<span data-ttu-id="3a579-108">Qualquer cliente habilitado tem o direito de chamar **GetCallerAccessRights**, mesmo que esse cliente não tenha direitos de execução de método geral.</span><span class="sxs-lookup"><span data-stu-id="3a579-108">Any enabled client has the right to call **GetCallerAccessRights**, even if that client does not have general method execution rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a579-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3a579-109">Syntax</span></span>


```mof
HRESULT GetCallerAccessRights(
  [out] sint32 rights
);
```



## <a name="parameters"></a><span data-ttu-id="3a579-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3a579-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a579-111">*direitos* \[ do fora\]</span><span class="sxs-lookup"><span data-stu-id="3a579-111">*rights* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a579-112">Direitos de acesso do cliente.</span><span class="sxs-lookup"><span data-stu-id="3a579-112">Access rights of the client.</span></span> <span data-ttu-id="3a579-113">Para obter mais informações, consulte [**\_ \_ SystemSecurity**](--systemsecurity.md) and [WMI Security Constants](wmi-security-constants.md).</span><span class="sxs-lookup"><span data-stu-id="3a579-113">For more information, see [**\_\_SystemSecurity**](--systemsecurity.md) and [WMI Security Constants](wmi-security-constants.md).</span></span>

<dt>

<span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>

<span data-ttu-id="3a579-114"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM \_ ENABLE** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="3a579-114"><span id="WBEM_ENABLE"></span><span id="wbem_enable"></span>**WBEM\_ENABLE** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="3a579-115">Habilita a conta e concede ao usuário permissões de leitura.</span><span class="sxs-lookup"><span data-stu-id="3a579-115">Enables the account and grants the user read permissions.</span></span> <span data-ttu-id="3a579-116">Esse é o direito de acesso padrão para todos os usuários.</span><span class="sxs-lookup"><span data-stu-id="3a579-116">This is the default access right for all users.</span></span>

</dd> <dt>

<span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>

<span data-ttu-id="3a579-117"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM \_ MÉTODO \_ Execute** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="3a579-117"><span id="WBEM_METHOD_EXECUTE"></span><span id="wbem_method_execute"></span>**WBEM\_METHOD\_EXECUTE** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="3a579-118">Permite a execução de métodos.</span><span class="sxs-lookup"><span data-stu-id="3a579-118">Allows the execution of methods.</span></span>

> [!Note]  
> <span data-ttu-id="3a579-119">Os provedores podem executar verificações de acesso adicionais.</span><span class="sxs-lookup"><span data-stu-id="3a579-119">Providers may perform additional access checks.</span></span>

 

</dd> <dt>

<span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>

<span data-ttu-id="3a579-120"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM \_ \_ \_ Rep. de gravação completa** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="3a579-120"><span id="WBEM_FULL_WRITE_REP"></span><span id="wbem_full_write_rep"></span>**WBEM\_FULL\_WRITE\_REP** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="3a579-121">Permite que o chamador, o contexto de segurança ou o usuário grave em classes e instâncias, exceto nas classes do sistema.</span><span class="sxs-lookup"><span data-stu-id="3a579-121">Allows the caller, security context, or user to write to classes and instances except for system classes.</span></span>

</dd> <dt>

<span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>

<span data-ttu-id="3a579-122"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM \_ \_ \_ Representante de gravação parcial** (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="3a579-122"><span id="WBEM_PARTIAL_WRITE_REP"></span><span id="wbem_partial_write_rep"></span>**WBEM\_PARTIAL\_WRITE\_REP** (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="3a579-123">Permite que o chamador, o contexto de segurança ou o usuário grave instâncias de provedor, mas não classes estáticas ou instâncias estáticas para o repositório.</span><span class="sxs-lookup"><span data-stu-id="3a579-123">Allows the caller, security context, or user to write provider instances but not static classes or static instances to the repository.</span></span>

</dd> <dt>

<span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>

<span data-ttu-id="3a579-124"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM \_ \_Provedor de gravação** (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="3a579-124"><span id="WBEM_WRITE_PROVIDER"></span><span id="wbem_write_provider"></span>**WBEM\_WRITE\_PROVIDER** (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="3a579-125">Permite que o chamador, o contexto de segurança ou o usuário grave classes e instâncias em provedores.</span><span class="sxs-lookup"><span data-stu-id="3a579-125">Allows the caller, security context, or user to write classes and instances to providers.</span></span>

> [!Note]  
> <span data-ttu-id="3a579-126">A representação de provedores pode fazer verificações de acesso adicionais.</span><span class="sxs-lookup"><span data-stu-id="3a579-126">Impersonating providers may do additional access checks.</span></span>

 

</dd> <dt>

<span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>

<span data-ttu-id="3a579-127"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM \_ \_Acesso remoto** (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="3a579-127"><span id="WBEM_REMOTE_ACCESS"></span><span id="wbem_remote_access"></span>**WBEM\_REMOTE\_ACCESS** (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="3a579-128">Permite que uma conta de usuário execute remotamente qualquer operação permitida pelas permissões definidas por outros bits.</span><span class="sxs-lookup"><span data-stu-id="3a579-128">Allows a user account to remotely perform any operations allowed by the permissions set by other bits.</span></span>

</dd> <dt>

<span id="READ_CONTROL"></span><span id="read_control"></span>

<span data-ttu-id="3a579-129"><span id="READ_CONTROL"></span><span id="read_control"></span>**Ler \_ CONTROLE** (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="3a579-129"><span id="READ_CONTROL"></span><span id="read_control"></span>**READ\_CONTROL** (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="3a579-130">Permite o acesso de leitura aos descritores de segurança.</span><span class="sxs-lookup"><span data-stu-id="3a579-130">Allows read access to the security descriptors.</span></span>

</dd> <dt>

<span id="WRITE_DAC"></span><span id="write_dac"></span>

<span data-ttu-id="3a579-131"><span id="WRITE_DAC"></span><span id="write_dac"></span>**Gravar \_ DAC** (262144 (0x40000))</span><span class="sxs-lookup"><span data-stu-id="3a579-131"><span id="WRITE_DAC"></span><span id="write_dac"></span>**WRITE\_DAC** (262144 (0x40000))</span></span>


</dt> <dd>

<span data-ttu-id="3a579-132">Permite acesso de gravação para listas de controle de acesso discricional (DACL).</span><span class="sxs-lookup"><span data-stu-id="3a579-132">Allows write access to discretionary access control lists (DACL).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a579-133">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3a579-133">Return value</span></span>

<span data-ttu-id="3a579-134">Esse método retorna um **HRESULT** que indica o status da chamada do método.</span><span class="sxs-lookup"><span data-stu-id="3a579-134">This method returns an **HRESULT** that indicates the status of the method call.</span></span> <span data-ttu-id="3a579-135">A lista a seguir lista os valores de retorno que são de significância a [**Set9XUserList**](--systemsecurity-set9xuserlist.md).</span><span class="sxs-lookup"><span data-stu-id="3a579-135">The following list lists the return values that are of significance to [**Set9XUserList**](--systemsecurity-set9xuserlist.md).</span></span> <span data-ttu-id="3a579-136">Para aplicativos de script e Visual Basic, o resultado pode ser obtido de [Parameters. ReturnValue](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3a579-136">For scripting and Visual Basic applications, the result can be obtained from [OutParameters.ReturnValue](parsing-outparameters-objects.md).</span></span> <span data-ttu-id="3a579-137">Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3a579-137">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<dl> <dt>

<span data-ttu-id="3a579-138">**\_método WBEM \_ E \_ desabilitado**</span><span class="sxs-lookup"><span data-stu-id="3a579-138">**WBEM\_E\_METHOD\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="3a579-139">Não há suporte para esse método em versões do Windows com suporte.</span><span class="sxs-lookup"><span data-stu-id="3a579-139">This method is not supported on supported versions of Windows.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a579-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a579-140">Requirements</span></span>



| <span data-ttu-id="3a579-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a579-141">Requirement</span></span> | <span data-ttu-id="3a579-142">Valor</span><span class="sxs-lookup"><span data-stu-id="3a579-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3a579-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a579-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3a579-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a579-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3a579-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3a579-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3a579-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a579-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="3a579-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a579-147">Namespace</span></span><br/>                | <span data-ttu-id="3a579-148">Todos os namespaces do WMI</span><span class="sxs-lookup"><span data-stu-id="3a579-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="3a579-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a579-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a579-150">Classes do sistema WMI</span><span class="sxs-lookup"><span data-stu-id="3a579-150">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="3a579-151">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="3a579-151">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> <dt>

[<span data-ttu-id="3a579-152">**\_\_SystemSecurity:: Obtém-se**</span><span class="sxs-lookup"><span data-stu-id="3a579-152">**\_\_SystemSecurity::GetSD**</span></span>](--systemsecurity-getsd.md)
</dt> <dt>

[<span data-ttu-id="3a579-153">**\_\_SystemSecurity:: definido**</span><span class="sxs-lookup"><span data-stu-id="3a579-153">**\_\_SystemSecurity::SetSD**</span></span>](--systemsecurity-setsd.md)
</dt> <dt>

[<span data-ttu-id="3a579-154">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="3a579-154">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="3a579-155">**Ace do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="3a579-155">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[<span data-ttu-id="3a579-156">**\_SecurityDescriptor Win32**</span><span class="sxs-lookup"><span data-stu-id="3a579-156">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[<span data-ttu-id="3a579-157">Protegendo namespaces WMI</span><span class="sxs-lookup"><span data-stu-id="3a579-157">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

<span data-ttu-id="3a579-158">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="3a579-158">WMI Security Constants</span></span>
</dt> </dl>

 

