---
title: Método addaccount da classe Win32_TSPermissionsSetting (Faxcomex. h)
description: O método addaccount se prepara para adicionar uma conta ao terminal com o conjunto de permissões especificado. Você pode adicionar usuários, grupos ou computadores.
ms.assetid: da4d8f5b-7aa2-4b55-bf0f-b3e98b70a06b
ms.tgt_platform: multiple
keywords:
- Método addaccount Serviços de Área de Trabalho Remota
- Método addaccount Serviços de Área de Trabalho Remota, classe Win32_TSPermissionsSetting
- Classe Win32_TSPermissionsSetting Serviços de Área de Trabalho Remota, método addaccount
topic_type:
- apiref
api_name:
- Win32_TSPermissionsSetting.AddAccount
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de89c34bd7aab20fbfbcbdedfd9d2f91bba866bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455473"
---
# <a name="addaccount-method-of-the-win32_tspermissionssetting-class"></a><span data-ttu-id="f0dd1-107">Método addaccount da classe Win32 \_ TSPermissionsSetting</span><span class="sxs-lookup"><span data-stu-id="f0dd1-107">AddAccount method of the Win32\_TSPermissionsSetting class</span></span>

<span data-ttu-id="f0dd1-108">O método **addaccount** se prepara para adicionar uma conta ao terminal com o conjunto de permissões especificado.</span><span class="sxs-lookup"><span data-stu-id="f0dd1-108">The **AddAccount** method prepares to add an account to the terminal with the specified permission set.</span></span> <span data-ttu-id="f0dd1-109">Você pode adicionar usuários, grupos ou computadores.</span><span class="sxs-lookup"><span data-stu-id="f0dd1-109">You can add users, groups, or computers.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0dd1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0dd1-110">Syntax</span></span>


```mof
uint32 AddAccount(
  [in] string AccountName,
  [in] uint32 PermissionPreSet
);
```



## <a name="parameters"></a><span data-ttu-id="f0dd1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0dd1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0dd1-112">*AccountName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0dd1-112">*AccountName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0dd1-113">O nome da conta a ser adicionada ao terminal.</span><span class="sxs-lookup"><span data-stu-id="f0dd1-113">The name of the account to add to the terminal.</span></span>

</dd> <dt>

<span data-ttu-id="f0dd1-114">*PermissionPreSet* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0dd1-114">*PermissionPreSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0dd1-115">O conjunto de permissões a ser associado à conta especificada.</span><span class="sxs-lookup"><span data-stu-id="f0dd1-115">The set of permissions to associate with the specified account.</span></span> <span data-ttu-id="f0dd1-116">Esse parâmetro pode ser qualquer um ou todos os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="f0dd1-116">This parameter can be any or all of the following values.</span></span> <span data-ttu-id="f0dd1-117">Para obter mais informações, consulte [serviços de área de trabalho remota permissões](terminal-services-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="f0dd1-117">For more information, see [Remote Desktop Services Permissions](terminal-services-permissions.md).</span></span>

<dt>

<span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>

<span data-ttu-id="f0dd1-118"><span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION \_ \_Acesso de convidado** (0)</span><span class="sxs-lookup"><span data-stu-id="f0dd1-118"><span id="WINSTATION_GUEST_ACCESS"></span><span id="winstation_guest_access"></span>**WINSTATION\_GUEST\_ACCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="f0dd1-119">A conta tem permissão de logon.</span><span class="sxs-lookup"><span data-stu-id="f0dd1-119">The account has Logon permission.</span></span>

</dd> <dt>

<span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>

<span data-ttu-id="f0dd1-120"><span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION \_ \_Acesso do usuário** (1)</span><span class="sxs-lookup"><span data-stu-id="f0dd1-120"><span id="WINSTATION_USER_ACCESS"></span><span id="winstation_user_access"></span>**WINSTATION\_USER\_ACCESS** (1)</span></span>


</dt> <dd>

<span data-ttu-id="f0dd1-121">A conta tem as seguintes permissões: logon, informações de consulta, enviar mensagem e conectar.</span><span class="sxs-lookup"><span data-stu-id="f0dd1-121">The account has the following permissions: Logon, Query Information, Send Message, and Connect.</span></span>

</dd> <dt>

<span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>

<span data-ttu-id="f0dd1-122"><span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION \_ Todos os \_ acessos** (2)</span><span class="sxs-lookup"><span data-stu-id="f0dd1-122"><span id="WINSTATION_ALL_ACCESS"></span><span id="winstation_all_access"></span>**WINSTATION\_ALL\_ACCESS** (2)</span></span>


</dt> <dd>

<span data-ttu-id="f0dd1-123">A conta tem todas as permissões de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="f0dd1-123">The account has all Remote Desktop Services Permissions.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0dd1-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0dd1-124">Return value</span></span>

<span data-ttu-id="f0dd1-125">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="f0dd1-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f0dd1-126">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="f0dd1-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0dd1-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0dd1-127">Remarks</span></span>

<span data-ttu-id="f0dd1-128">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="f0dd1-128">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f0dd1-129">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f0dd1-129">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f0dd1-130">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="f0dd1-130">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f0dd1-131">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f0dd1-131">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0dd1-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0dd1-132">Requirements</span></span>



| <span data-ttu-id="f0dd1-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0dd1-133">Requirement</span></span> | <span data-ttu-id="f0dd1-134">Valor</span><span class="sxs-lookup"><span data-stu-id="f0dd1-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0dd1-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0dd1-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f0dd1-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0dd1-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f0dd1-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f0dd1-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f0dd1-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0dd1-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f0dd1-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="f0dd1-139">Namespace</span></span><br/>                | <span data-ttu-id="f0dd1-140">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="f0dd1-140">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f0dd1-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0dd1-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0dd1-142"><dt>Faxcomex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0dd1-142"><dt>Faxcomex.h</dt></span></span> </dl>   |
| <span data-ttu-id="f0dd1-143">MOF</span><span class="sxs-lookup"><span data-stu-id="f0dd1-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0dd1-144"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0dd1-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0dd1-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f0dd1-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0dd1-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0dd1-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0dd1-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0dd1-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0dd1-148">**\_TSPermissionsSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="f0dd1-148">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> </dl>

 

