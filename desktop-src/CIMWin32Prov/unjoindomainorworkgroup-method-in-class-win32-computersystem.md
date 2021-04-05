---
description: Remove um sistema de computador de um domínio ou grupo de trabalho.
ms.assetid: 79ee177e-81e2-441b-b39a-2fb53a0145bf
ms.tgt_platform: multiple
title: Método UnjoinDomainOrWorkgroup da classe Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.UnjoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c6942c5367b6deb02accd9d06927a4d923fa8f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826630"
---
# <a name="unjoindomainorworkgroup-method-of-the-win32_computersystem-class"></a><span data-ttu-id="33c11-103">Método UnjoinDomainOrWorkgroup da classe Win32 \_ ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="33c11-103">UnjoinDomainOrWorkgroup method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="33c11-104">O método **UnjoinDomainOrWorkgroup** remove um sistema de computador de um domínio ou grupo de trabalho.</span><span class="sxs-lookup"><span data-stu-id="33c11-104">The **UnjoinDomainOrWorkgroup** method removes a computer system from a domain or workgroup.</span></span>

<span data-ttu-id="33c11-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="33c11-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="33c11-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="33c11-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="33c11-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33c11-107">Syntax</span></span>


```mof
uint32 UnjoinDomainOrWorkgroup(
  [in] string Password,
  [in] string UserName,
  [in] uint32 FUnjoinOptions = 
);
```



## <a name="parameters"></a><span data-ttu-id="33c11-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33c11-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33c11-109">*Senha* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="33c11-109">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c11-110">Se o parâmetro *username* especificar um nome de conta, o parâmetro *password* deverá apontar para a senha a ser usada na conexão com o controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="33c11-110">If the *UserName* parameter specifies an account name, the *Password* parameter must point to the password to use when connecting to the domain controller.</span></span> <span data-ttu-id="33c11-111">Caso contrário, esse parâmetro deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="33c11-111">Otherwise, this parameter must be **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="33c11-112">A *senha* deve usar um nível de autenticação alto, não menor que a privacidade do PCT de **\_ \_ \_ nível \_ \_ de autenticação RPC C**, ao se conectar a winmgmt ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) no ponteiro de [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="33c11-112">*Password* must use a high authentication level, not less than **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, when connecting to Winmgmt or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) pointer.</span></span> <span data-ttu-id="33c11-113">Se for local para winmgmt, isso não é uma preocupação.</span><span class="sxs-lookup"><span data-stu-id="33c11-113">If local to Winmgmt, this is not a concern.</span></span>

 

</dd> <dt>

<span data-ttu-id="33c11-114">*Nome de usuário* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33c11-114">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c11-115">Ponteiro para uma cadeia de caracteres constante terminada em nulo que especifica o nome da conta a ser usada ao conectar-se ao controlador de domínio.</span><span class="sxs-lookup"><span data-stu-id="33c11-115">Pointer to a constant null-terminated character string that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="33c11-116">É necessário especificar uma conta de domínio e de usuário, por exemplo, "domínio \\ usuário" ou " user@domain ".</span><span class="sxs-lookup"><span data-stu-id="33c11-116">Must specify a domain and user account, for example, "domain\\user" or "user@domain".</span></span> <span data-ttu-id="33c11-117">Se esse parâmetro for **NULL**, o contexto do chamador será usado.</span><span class="sxs-lookup"><span data-stu-id="33c11-117">If this parameter is **NULL**, the caller context is used.</span></span>

> [!Note]  
> <span data-ttu-id="33c11-118">O *nome de usuário* deve usar um nível de autenticação alto, não menor que a privacidade do PCT de **\_ \_ \_ nível \_ \_ de autenticação RPC C**, ao se conectar a winmgmt ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) no ponteiro de [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="33c11-118">*UserName* must use a high authentication level, not less than **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, when connecting to Winmgmt or [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) on the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) pointer.</span></span> <span data-ttu-id="33c11-119">Se for local para winmgmt, isso não é uma preocupação.</span><span class="sxs-lookup"><span data-stu-id="33c11-119">If local to Winmgmt, this is not a concern.</span></span>

 

</dd> <dt>

<span data-ttu-id="33c11-120">*FUnjoinOptions* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="33c11-120">*FUnjoinOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33c11-121">Conjunto de sinalizadores de bits que definem as opções de desjunção.</span><span class="sxs-lookup"><span data-stu-id="33c11-121">Set of bit flags defining the unjoin options.</span></span>

<dt>



 <span data-ttu-id="33c11-122"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="33c11-122">(0)</span></span>


</dt> <dd>

<span data-ttu-id="33c11-123">Padrão.</span><span class="sxs-lookup"><span data-stu-id="33c11-123">Default.</span></span> <span data-ttu-id="33c11-124">Não há opções.</span><span class="sxs-lookup"><span data-stu-id="33c11-124">No options.</span></span>

</dd> <dt>

<span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>

<span data-ttu-id="33c11-125"><span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>INSTALAÇÃO do NET **\_ \_Exclusão de acct** (4)</span><span class="sxs-lookup"><span data-stu-id="33c11-125"><span id="NETSETUP_ACCT_DELETE"></span><span id="netsetup_acct_delete"></span>**NETSETUP\_ACCT\_DELETE** (4)</span></span>


</dt> <dd>

<span data-ttu-id="33c11-126">Desabilite a conta de Active Directory após a operação de desassociação, mas não exclua a conta.</span><span class="sxs-lookup"><span data-stu-id="33c11-126">Disable the Active Directory account after the unjoin operation, but do not delete the account.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33c11-127">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33c11-127">Return value</span></span>

<span data-ttu-id="33c11-128">O método **UnjoinDomainOrWorkgroup** retorna 0 (zero) em caso de êxito ou quando não há opções envolvidas.</span><span class="sxs-lookup"><span data-stu-id="33c11-128">The **UnjoinDomainOrWorkgroup** method returns 0 (zero) on success or when no options are involved.</span></span> <span data-ttu-id="33c11-129">Qualquer outro valor indica um erro.</span><span class="sxs-lookup"><span data-stu-id="33c11-129">Any other value indicates an error.</span></span> <span data-ttu-id="33c11-130">Para códigos de erro, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="33c11-130">For error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="33c11-131">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="33c11-131">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="33c11-132">**Êxito** (0)</span><span class="sxs-lookup"><span data-stu-id="33c11-132">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="33c11-133">**Outro** (1 4294967295)</span><span class="sxs-lookup"><span data-stu-id="33c11-133">**Other** (1 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="33c11-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="33c11-134">Remarks</span></span>

<span data-ttu-id="33c11-135">Depois de chamar esse método, reinicie o computador afetado para aplicar as alterações.</span><span class="sxs-lookup"><span data-stu-id="33c11-135">After calling this method, restart the affected computer to apply the changes.</span></span>

## <a name="examples"></a><span data-ttu-id="33c11-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="33c11-136">Examples</span></span>

<span data-ttu-id="33c11-137">[A desassociação de um computador de um domínio](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) A amostra do VBScript desune o computador local do seu domínio atual e desabilita a conta do computador.</span><span class="sxs-lookup"><span data-stu-id="33c11-137">[The Unjoin a Computer from a Domain](https://Gallery.TechNet.Microsoft.Com/c2025ace-cb51-4136-9de9-db8871f79f62) VBScript sample unjoins the local computer from its current domain and disables the computer account.</span></span>

<span data-ttu-id="33c11-138">O exemplo [desassociar um computador de um domínio usando script vbs](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) não une um computador especificado de um domínio.</span><span class="sxs-lookup"><span data-stu-id="33c11-138">The [Unjoin a Computer from a Domain using VBS script](https://Gallery.TechNet.Microsoft.Com/Unjoin-a-Computer-from-a-825249e1) sample unjoins a specified computer from a domain.</span></span> <span data-ttu-id="33c11-139">.</span><span class="sxs-lookup"><span data-stu-id="33c11-139">.</span></span>

## <a name="requirements"></a><span data-ttu-id="33c11-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33c11-140">Requirements</span></span>



| <span data-ttu-id="33c11-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="33c11-141">Requirement</span></span> | <span data-ttu-id="33c11-142">Valor</span><span class="sxs-lookup"><span data-stu-id="33c11-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="33c11-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33c11-143">Minimum supported client</span></span><br/> | <span data-ttu-id="33c11-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="33c11-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="33c11-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33c11-145">Minimum supported server</span></span><br/> | <span data-ttu-id="33c11-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="33c11-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="33c11-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="33c11-147">Namespace</span></span><br/>                | <span data-ttu-id="33c11-148">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="33c11-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="33c11-149">MOF</span><span class="sxs-lookup"><span data-stu-id="33c11-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33c11-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33c11-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="33c11-151">DLL</span><span class="sxs-lookup"><span data-stu-id="33c11-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33c11-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33c11-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33c11-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="33c11-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33c11-154">**\_Sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="33c11-154">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="33c11-155">**Método JoinDomainOrWorkgroup**</span><span class="sxs-lookup"><span data-stu-id="33c11-155">**JoinDomainOrWorkgroup method**</span></span>](joindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

