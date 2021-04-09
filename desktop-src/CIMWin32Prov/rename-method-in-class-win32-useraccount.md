---
description: Renomeia um nome de conta de usuário.
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Método Rename da classe Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d495804fb68bc74eda269c2dd7921540f05f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089478"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a><span data-ttu-id="abcdf-103">Método Rename da \_ classe USERACCOUNT do Win32</span><span class="sxs-lookup"><span data-stu-id="abcdf-103">Rename method of the Win32\_UserAccount class</span></span>

<span data-ttu-id="abcdf-104">O método **renomear** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) renomeia um nome de conta de usuário.</span><span class="sxs-lookup"><span data-stu-id="abcdf-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames a user account name.</span></span>

<span data-ttu-id="abcdf-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="abcdf-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="abcdf-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="abcdf-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="abcdf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="abcdf-107">Syntax</span></span>


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a><span data-ttu-id="abcdf-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="abcdf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abcdf-109">*Nome* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="abcdf-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abcdf-110">Nome da nova conta.</span><span class="sxs-lookup"><span data-stu-id="abcdf-110">New account name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abcdf-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="abcdf-111">Return value</span></span>

<span data-ttu-id="abcdf-112">Retorna um dos valores listados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="abcdf-112">Returns one of the values listed in the following list.</span></span> <span data-ttu-id="abcdf-113">Para obter códigos de erro adicionais, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants) ou [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="abcdf-113">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="abcdf-114">Para obter valores gerais de **HRESULT** , consulte [códigos de erro do sistema](/windows/desktop/Debug/system-error-codes).</span><span class="sxs-lookup"><span data-stu-id="abcdf-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="abcdf-115">**Êxito**</span><span class="sxs-lookup"><span data-stu-id="abcdf-115">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="abcdf-116">0</span><span class="sxs-lookup"><span data-stu-id="abcdf-116">0</span></span>

<span data-ttu-id="abcdf-117">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="abcdf-117">Success.</span></span>

</dd> <dt>

<span data-ttu-id="abcdf-118">**Instância não encontrada**</span><span class="sxs-lookup"><span data-stu-id="abcdf-118">**Instance not found**</span></span>
</dt> <dd>

<span data-ttu-id="abcdf-119">1</span><span class="sxs-lookup"><span data-stu-id="abcdf-119">1</span></span>

<span data-ttu-id="abcdf-120">Instância não encontrada.</span><span class="sxs-lookup"><span data-stu-id="abcdf-120">Instance not found.</span></span>

</dd> <dt>

<span data-ttu-id="abcdf-121">**Instância necessária**</span><span class="sxs-lookup"><span data-stu-id="abcdf-121">**Instance required**</span></span>
</dt> <dd>

<span data-ttu-id="abcdf-122">2</span><span class="sxs-lookup"><span data-stu-id="abcdf-122">2</span></span>

<span data-ttu-id="abcdf-123">Instância necessária.</span><span class="sxs-lookup"><span data-stu-id="abcdf-123">Instance required.</span></span>

</dd> <dt>

<span data-ttu-id="abcdf-124">**Parâmetro inválido**</span><span class="sxs-lookup"><span data-stu-id="abcdf-124">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="abcdf-125">3</span><span class="sxs-lookup"><span data-stu-id="abcdf-125">3</span></span>

<span data-ttu-id="abcdf-126">Parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="abcdf-126">Invalid parameter.</span></span>

</dd> <dt>

<span data-ttu-id="abcdf-127">**Usuário não encontrado**</span><span class="sxs-lookup"><span data-stu-id="abcdf-127">**User not found**</span></span>
</dt> <dd>

<span data-ttu-id="abcdf-128">4</span><span class="sxs-lookup"><span data-stu-id="abcdf-128">4</span></span>

<span data-ttu-id="abcdf-129">Usuário não encontrado.</span><span class="sxs-lookup"><span data-stu-id="abcdf-129">User not found.</span></span>

</dd> <dt>

<span data-ttu-id="abcdf-130">**Domínio não encontrado**</span><span class="sxs-lookup"><span data-stu-id="abcdf-130">**Domain not found**</span></span>
</dt> <dd>

<span data-ttu-id="abcdf-131">5</span><span class="sxs-lookup"><span data-stu-id="abcdf-131">5</span></span>

<span data-ttu-id="abcdf-132">Domínio não encontrado.</span><span class="sxs-lookup"><span data-stu-id="abcdf-132">Domain not found.</span></span>

</dd> <dt>

<span data-ttu-id="abcdf-133">**A operação é permitida somente no controlador de domínio primário do domínio**</span><span class="sxs-lookup"><span data-stu-id="abcdf-133">**Operation is allowed only on the primary domain controller of the domain**</span></span>
</dt> <dd>

<span data-ttu-id="abcdf-134">6</span><span class="sxs-lookup"><span data-stu-id="abcdf-134">6</span></span>

<span data-ttu-id="abcdf-135">A operação é permitida somente no controlador de domínio primário do domínio.</span><span class="sxs-lookup"><span data-stu-id="abcdf-135">Operation is allowed only on the primary domain controller of the domain.</span></span>

</dd> <dt>

<span data-ttu-id="abcdf-136">**A operação não é permitida na última conta administrativa.**</span><span class="sxs-lookup"><span data-stu-id="abcdf-136">**Operation is not allowed on the last administrative account.**</span></span>
</dt> <dd>

<span data-ttu-id="abcdf-137">7</span><span class="sxs-lookup"><span data-stu-id="abcdf-137">7</span></span>

</dd> <dt>

<span data-ttu-id="abcdf-138">**A operação não é permitida em grupos especiais especificados; usuário, administrador, local ou convidado.**</span><span class="sxs-lookup"><span data-stu-id="abcdf-138">**Operation is not allowed on specified special groups; user, admin, local or guest.**</span></span>
</dt> <dd>

<span data-ttu-id="abcdf-139">8</span><span class="sxs-lookup"><span data-stu-id="abcdf-139">8</span></span>

<span data-ttu-id="abcdf-140">A operação não é permitida em grupos especiais especificados: usuário, administrador, local ou convidado.</span><span class="sxs-lookup"><span data-stu-id="abcdf-140">Operation is not allowed on specified special groups: user, admin, local, or guest.</span></span>

</dd> <dt>

<span data-ttu-id="abcdf-141">**Outro erro de API**</span><span class="sxs-lookup"><span data-stu-id="abcdf-141">**Other API error**</span></span>
</dt> <dd>

<span data-ttu-id="abcdf-142">9</span><span class="sxs-lookup"><span data-stu-id="abcdf-142">9</span></span>

<span data-ttu-id="abcdf-143">Outro erro de API.</span><span class="sxs-lookup"><span data-stu-id="abcdf-143">Other API error.</span></span>

</dd> <dt>

<span data-ttu-id="abcdf-144">**Erro interno**</span><span class="sxs-lookup"><span data-stu-id="abcdf-144">**Internal error**</span></span>
</dt> <dd>

<span data-ttu-id="abcdf-145">10</span><span class="sxs-lookup"><span data-stu-id="abcdf-145">10</span></span>

<span data-ttu-id="abcdf-146">Erro interno.</span><span class="sxs-lookup"><span data-stu-id="abcdf-146">Internal error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abcdf-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="abcdf-147">Remarks</span></span>

<span data-ttu-id="abcdf-148">Essa funcionalidade é implementada como um método para fornecer um contexto separado para o novo nome que é distinguivel do valor da propriedade de chave para o nome que está associado à instância a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="abcdf-148">This functionality is implemented as a method to provide a separate context for the new name that is distinguishable from the key property value for Name that is associated with the instance to be modified.</span></span>

## <a name="requirements"></a><span data-ttu-id="abcdf-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abcdf-149">Requirements</span></span>



| <span data-ttu-id="abcdf-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="abcdf-150">Requirement</span></span> | <span data-ttu-id="abcdf-151">Valor</span><span class="sxs-lookup"><span data-stu-id="abcdf-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abcdf-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abcdf-152">Minimum supported client</span></span><br/> | <span data-ttu-id="abcdf-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="abcdf-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="abcdf-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="abcdf-154">Minimum supported server</span></span><br/> | <span data-ttu-id="abcdf-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abcdf-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="abcdf-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="abcdf-156">Namespace</span></span><br/>                | <span data-ttu-id="abcdf-157">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="abcdf-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="abcdf-158">MOF</span><span class="sxs-lookup"><span data-stu-id="abcdf-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abcdf-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="abcdf-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="abcdf-160">DLL</span><span class="sxs-lookup"><span data-stu-id="abcdf-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abcdf-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abcdf-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abcdf-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="abcdf-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abcdf-163">**Conta userwin32 \_**</span><span class="sxs-lookup"><span data-stu-id="abcdf-163">**Win32\_UserAccount**</span></span>](win32-useraccount.md)
</dt> <dt>

<span data-ttu-id="abcdf-164">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="abcdf-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

