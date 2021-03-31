---
title: Classe MDM_Policy_Result01_DeviceLock02
description: A \_ classe MDM Policy \_ Result01 \_ DeviceLock02 representa as políticas de bloqueio de dispositivo disponíveis.
ms.assetid: 9aac25a8-8502-468f-9478-1ac4ccccaf0b
keywords:
- Classe MDM_Policy_Result01_DeviceLock02
- Classe MDM_Policy_Result01_DeviceLock02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_DeviceLock02
- MDM_Policy_Result01_DeviceLock02.InstanceID
- MDM_Policy_Result01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa93236b99add5cb49e0b54aa10eab9e959ab01a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824439"
---
# <a name="mdm_policy_result01_devicelock02-class"></a><span data-ttu-id="bfc18-105">\_Classe MDM \_ Result01 \_ DeviceLock02</span><span class="sxs-lookup"><span data-stu-id="bfc18-105">MDM\_Policy\_Result01\_DeviceLock02 class</span></span>

<span data-ttu-id="bfc18-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="bfc18-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bfc18-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="bfc18-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bfc18-108">A classe **MDM \_ Policy \_ Result01 \_ DeviceLock02** representa as políticas de bloqueio de dispositivo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="bfc18-108">The **MDM\_Policy\_Result01\_DeviceLock02** class represents the device lock policies available.</span></span>

<span data-ttu-id="bfc18-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bfc18-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfc18-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfc18-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_DeviceLock02
{
  string InstanceID;
  string ParentID;
  sint32 AllowScreenTimeoutWhileLockedUserConfig;
  sint32 AllowSimpleDevicePassword;
  sint32 AlphanumericDevicePasswordRequired;
  sint32 DevicePasswordEnabled;
  sint32 DevicePasswordExpiration;
  sint32 DevicePasswordHistory;
  string EnforceLockScreenAndLogonImage;
  string EnforceLockScreenProvider;
  sint32 MinimumPasswordAge;
  sint32 MaxDevicePasswordFailedAttempts;
  sint32 MaxInactivityTimeDeviceLock;
  sint32 MinDevicePasswordComplexCharacters;
  sint32 MinDevicePasswordLength;
  sint32 ScreenTimeoutWhileLocked;
  string PreventLockScreenSlideShow;
};
```

## <a name="members"></a><span data-ttu-id="bfc18-111">Membros</span><span class="sxs-lookup"><span data-stu-id="bfc18-111">Members</span></span>

<span data-ttu-id="bfc18-112">A **classe \_ \_ Result01 \_ DeviceLock02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bfc18-112">The **MDM\_Policy\_Result01\_DeviceLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="bfc18-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bfc18-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bfc18-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bfc18-114">Properties</span></span>

<span data-ttu-id="bfc18-115">A **classe \_ \_ Result01 \_ DeviceLock02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bfc18-115">The **MDM\_Policy\_Result01\_DeviceLock02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bfc18-116">AllowScreenTimeoutWhileLockedUserConfig</span><span class="sxs-lookup"><span data-stu-id="bfc18-116">AllowScreenTimeoutWhileLockedUserConfig</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bfc18-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bfc18-119">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="bfc18-119">AllowSimpleDevicePassword</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bfc18-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bfc18-122">AlphanumericDevicePasswordRequired</span><span class="sxs-lookup"><span data-stu-id="bfc18-122">AlphanumericDevicePasswordRequired</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bfc18-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bfc18-125">DevicePasswordEnabled</span><span class="sxs-lookup"><span data-stu-id="bfc18-125">DevicePasswordEnabled</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bfc18-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bfc18-128">DevicePasswordExpiration</span><span class="sxs-lookup"><span data-stu-id="bfc18-128">DevicePasswordExpiration</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bfc18-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bfc18-131">DevicePasswordHistory</span><span class="sxs-lookup"><span data-stu-id="bfc18-131">DevicePasswordHistory</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-132">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bfc18-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-133">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bfc18-134">EnforceLockScreenAndLogonImage</span><span class="sxs-lookup"><span data-stu-id="bfc18-134">EnforceLockScreenAndLogonImage</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bfc18-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bfc18-137">EnforceLockScreenProvider</span><span class="sxs-lookup"><span data-stu-id="bfc18-137">EnforceLockScreenProvider</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bfc18-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-139">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bfc18-140">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bfc18-140">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bfc18-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bfc18-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-143">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bfc18-143">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bfc18-144">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="bfc18-144">Identifies the name of the parent node.</span></span> <span data-ttu-id="bfc18-145">Para essa classe, a cadeia de caracteres é "DeviceLock".</span><span class="sxs-lookup"><span data-stu-id="bfc18-145">For this class, the string is "DeviceLock".</span></span>

</dd> <dt>

[<span data-ttu-id="bfc18-146">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="bfc18-146">MaxDevicePasswordFailedAttempts</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-147">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bfc18-147">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bfc18-149">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="bfc18-149">MaxInactivityTimeDeviceLock</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-150">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bfc18-150">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bfc18-152">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="bfc18-152">MinDevicePasswordComplexCharacters</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-153">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bfc18-153">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-154">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bfc18-155">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="bfc18-155">MinDevicePasswordLength</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-156">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bfc18-156">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-157">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-157">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="bfc18-158">MinimumPasswordAge</span><span class="sxs-lookup"><span data-stu-id="bfc18-158">MinimumPasswordAge</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-159">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bfc18-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bfc18-161">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="bfc18-161">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bfc18-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bfc18-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-164">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="bfc18-164">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="bfc18-165">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="bfc18-165">Describes the full path to the parent node.</span></span> <span data-ttu-id="bfc18-166">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Result"</span><span class="sxs-lookup"><span data-stu-id="bfc18-166">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="bfc18-167">PreventLockScreenSlideShow</span><span class="sxs-lookup"><span data-stu-id="bfc18-167">PreventLockScreenSlideShow</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bfc18-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="bfc18-170">ScreenTimeoutWhileLocked</span><span class="sxs-lookup"><span data-stu-id="bfc18-170">ScreenTimeoutWhileLocked</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfc18-171">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="bfc18-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="bfc18-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="bfc18-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bfc18-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfc18-173">Requirements</span></span>



| <span data-ttu-id="bfc18-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfc18-174">Requirement</span></span> | <span data-ttu-id="bfc18-175">Valor</span><span class="sxs-lookup"><span data-stu-id="bfc18-175">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc18-176">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfc18-176">Minimum supported client</span></span><br/> | <span data-ttu-id="bfc18-177">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="bfc18-177">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bfc18-178">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bfc18-178">Minimum supported server</span></span><br/> | <span data-ttu-id="bfc18-179">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="bfc18-179">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bfc18-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="bfc18-180">Namespace</span></span><br/>                | <span data-ttu-id="bfc18-181">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="bfc18-181">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="bfc18-182">MOF</span><span class="sxs-lookup"><span data-stu-id="bfc18-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfc18-183"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfc18-183"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfc18-184">DLL</span><span class="sxs-lookup"><span data-stu-id="bfc18-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfc18-185"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfc18-185"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfc18-186">Consulte também</span><span class="sxs-lookup"><span data-stu-id="bfc18-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfc18-187">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="bfc18-187">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

