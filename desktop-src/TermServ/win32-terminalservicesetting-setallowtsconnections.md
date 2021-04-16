---
title: Método SetAllowTSConnections da classe Win32_TerminalServiceSetting
description: O método SetAllowTSConnections permite ou nega novas conexões de área de trabalho remota. Esse método modificará a propriedade AllowTSConnections da classe de forma adequada.
ms.assetid: 6cbaea62-ced0-4788-99fb-5b36816b80a1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetAllowTSConnections
- Método SetAllowTSConnections Serviços de Área de Trabalho Remota, classe Win32_TerminalServiceSetting
- Classe Win32_TerminalServiceSetting Serviços de Área de Trabalho Remota, método SetAllowTSConnections
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetAllowTSConnections
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e800f1a47567f16d916563d4d1e62c767016329a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455852"
---
# <a name="setallowtsconnections-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="64230-107">Método SetAllowTSConnections da classe Win32 \_ TerminalServiceSetting</span><span class="sxs-lookup"><span data-stu-id="64230-107">SetAllowTSConnections method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="64230-108">O método **SetAllowTSConnections** permite ou nega novas conexões de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="64230-108">The **SetAllowTSConnections** method allows or denies new remote desktop connections.</span></span> <span data-ttu-id="64230-109">Esse método modificará a propriedade **AllowTSConnections** da classe de forma adequada.</span><span class="sxs-lookup"><span data-stu-id="64230-109">This method will modify the **AllowTSConnections** property for the class accordingly.</span></span>

## <a name="syntax"></a><span data-ttu-id="64230-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="64230-110">Syntax</span></span>


```mof
uint32 SetAllowTSConnections(
  [in] uint32 AllowTSConnections,
  [in] uint32 ModifyFirewallException
);
```



## <a name="parameters"></a><span data-ttu-id="64230-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="64230-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64230-112">*AllowTSConnections* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="64230-112">*AllowTSConnections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64230-113">Especifica se são permitidas novas conexões de área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="64230-113">Specifies whether new remote desktop connections are allowed.</span></span> <span data-ttu-id="64230-114">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="64230-114">This must be one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="64230-115"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="64230-115"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="64230-116">Não são permitidas novas conexões.</span><span class="sxs-lookup"><span data-stu-id="64230-116">New connections are not allowed.</span></span> <span data-ttu-id="64230-117">Se o parâmetro *ModifyFirewallException* for 1, a exceção de firewall área de trabalho remota será desabilitada.</span><span class="sxs-lookup"><span data-stu-id="64230-117">If the *ModifyFirewallException* parameter is 1, then the Remote Desktop firewall exception is disabled.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="64230-118"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="64230-118"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="64230-119">Novas conexões são permitidas.</span><span class="sxs-lookup"><span data-stu-id="64230-119">New connections are allowed.</span></span> <span data-ttu-id="64230-120">Se o parâmetro *ModifyFirewallException* for 1, a exceção de firewall área de trabalho remota será habilitada.</span><span class="sxs-lookup"><span data-stu-id="64230-120">If the *ModifyFirewallException* parameter is 1, then the Remote Desktop firewall exception is enabled.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="64230-121">*ModifyFirewallException* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="64230-121">*ModifyFirewallException* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64230-122">Especifica se a configuração de exceção do firewall para Área de Trabalho Remota será modificada para o estado especificado pelo parâmetro *AllowTSConnections* .</span><span class="sxs-lookup"><span data-stu-id="64230-122">Specifies if the firewall exception setting for Remote Desktop will be modified to the state specified by the *AllowTSConnections* parameter.</span></span> <span data-ttu-id="64230-123">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="64230-123">This must be one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="64230-124"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="64230-124"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="64230-125">Não modifique a configuração de exceção do firewall.</span><span class="sxs-lookup"><span data-stu-id="64230-125">Do not modify the firewall exception setting.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="64230-126"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="64230-126"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="64230-127">Modifique a configuração de exceção do firewall.</span><span class="sxs-lookup"><span data-stu-id="64230-127">Modify the firewall exception setting.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64230-128">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="64230-128">Return value</span></span>

<span data-ttu-id="64230-129">Retorna êxito em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="64230-129">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="64230-130">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="64230-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="64230-131">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="64230-131">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="64230-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="64230-132">Remarks</span></span>

<span data-ttu-id="64230-133">Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="64230-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="64230-134">Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="64230-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="64230-135">Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor.</span><span class="sxs-lookup"><span data-stu-id="64230-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="64230-136">Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="64230-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="64230-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="64230-137">Requirements</span></span>



| <span data-ttu-id="64230-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="64230-138">Requirement</span></span> | <span data-ttu-id="64230-139">Valor</span><span class="sxs-lookup"><span data-stu-id="64230-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64230-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64230-140">Minimum supported client</span></span><br/> | <span data-ttu-id="64230-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64230-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64230-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="64230-142">Minimum supported server</span></span><br/> | <span data-ttu-id="64230-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64230-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64230-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="64230-144">Namespace</span></span><br/>                | <span data-ttu-id="64230-145">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="64230-145">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="64230-146">MOF</span><span class="sxs-lookup"><span data-stu-id="64230-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64230-147"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="64230-147"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="64230-148">DLL</span><span class="sxs-lookup"><span data-stu-id="64230-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64230-149"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64230-149"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64230-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="64230-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64230-151">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="64230-151">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

