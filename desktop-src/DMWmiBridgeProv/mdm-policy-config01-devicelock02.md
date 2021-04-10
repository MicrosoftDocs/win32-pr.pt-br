---
title: Classe MDM_Policy_Config01_DeviceLock02
description: A \_ classe MDM Policy \_ Config01 \_ DeviceLock02 representa as políticas de bloqueio de dispositivo disponíveis.
ms.assetid: 222081ec-c38f-481d-ae38-941fd1317197
keywords:
- Classe MDM_Policy_Config01_DeviceLock02
- Classe MDM_Policy_Config01_DeviceLock02, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_DeviceLock02
- MDM_Policy_Config01_DeviceLock02.InstanceID
- MDM_Policy_Config01_DeviceLock02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c5926912d276fbe04f75c161196c47d0f0dd384
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086238"
---
# <a name="mdm_policy_config01_devicelock02-class"></a><span data-ttu-id="8a24a-105">\_Classe MDM \_ Config01 \_ DeviceLock02</span><span class="sxs-lookup"><span data-stu-id="8a24a-105">MDM\_Policy\_Config01\_DeviceLock02 class</span></span>

<span data-ttu-id="8a24a-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="8a24a-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="8a24a-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="8a24a-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="8a24a-108">A classe **MDM \_ Policy \_ Config01 \_ DeviceLock02** representa as políticas de bloqueio de dispositivo disponíveis.</span><span class="sxs-lookup"><span data-stu-id="8a24a-108">The **MDM\_Policy\_Config01\_DeviceLock02** class represents the device lock policies available.</span></span>

<span data-ttu-id="8a24a-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8a24a-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a24a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8a24a-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_DeviceLock02
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

## <a name="members"></a><span data-ttu-id="8a24a-111">Membros</span><span class="sxs-lookup"><span data-stu-id="8a24a-111">Members</span></span>

<span data-ttu-id="8a24a-112">A **classe \_ \_ Config01 \_ DeviceLock02 da política MDM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8a24a-112">The **MDM\_Policy\_Config01\_DeviceLock02** class has these types of members:</span></span>

-   [<span data-ttu-id="8a24a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8a24a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8a24a-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8a24a-114">Properties</span></span>

<span data-ttu-id="8a24a-115">A **classe \_ \_ Config01 \_ DeviceLock02 da política MDM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8a24a-115">The **MDM\_Policy\_Config01\_DeviceLock02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8a24a-116">AllowScreenTimeoutWhileLockedUserConfig</span><span class="sxs-lookup"><span data-stu-id="8a24a-116">AllowScreenTimeoutWhileLockedUserConfig</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8a24a-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8a24a-119">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="8a24a-119">AllowSimpleDevicePassword</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-allowsimpledevicepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-120">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8a24a-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8a24a-122">AlphanumericDevicePasswordRequired</span><span class="sxs-lookup"><span data-stu-id="8a24a-122">AlphanumericDevicePasswordRequired</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-alphanumericdevicepasswordrequired)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-123">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8a24a-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8a24a-125">DevicePasswordEnabled</span><span class="sxs-lookup"><span data-stu-id="8a24a-125">DevicePasswordEnabled</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordenabled)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-126">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8a24a-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="8a24a-128">DevicePasswordEnabled não deve ser definido como Enabled (0) quando WMI é usado para definir as políticas de DeviceLock do EAS, uma vez que ele está habilitado por padrão no CSP de política para compatibilidade de volta com o Windows 8. x.</span><span class="sxs-lookup"><span data-stu-id="8a24a-128">DevicePasswordEnabled should not be set to Enabled (0) when WMI is used to set the EAS DeviceLock policies given that it is Enabled by default in Policy CSP for back compat with Windows 8.x.</span></span> <span data-ttu-id="8a24a-129">Se DevicePasswordEnabled for definido como Enabled (0), o CSP da política retornará um erro informando que DevicePasswordEnabled já existe.</span><span class="sxs-lookup"><span data-stu-id="8a24a-129">If DevicePasswordEnabled is set to Enabled(0) then Policy CSP will return an error stating that DevicePasswordEnabled already exists.</span></span> <span data-ttu-id="8a24a-130">O Windows 8. x não oferecia suporte à política DevicePassword.</span><span class="sxs-lookup"><span data-stu-id="8a24a-130">Windows 8.x did not support DevicePassword policy.</span></span> <span data-ttu-id="8a24a-131">Ao desabilitar DevicePasswordEnabled (1), essa deve ser a única política definida do grupo DeviceLock de políticas abaixo.</span><span class="sxs-lookup"><span data-stu-id="8a24a-131">When disabling DevicePasswordEnabled  (1) then this should be the only policy set from the DeviceLock group of policies below.</span></span> <span data-ttu-id="8a24a-132">As políticas são listadas abaixo: >-DevicePasswordEnabled é a política pai do seguinte:</span><span class="sxs-lookup"><span data-stu-id="8a24a-132">The policies are listed below: > - DevicePasswordEnabled is the parent policy of the following:</span></span>

-   <span data-ttu-id="8a24a-133">DevicePasswordEnabled é a política pai do seguinte:</span><span class="sxs-lookup"><span data-stu-id="8a24a-133">DevicePasswordEnabled is the parent policy of the following:</span></span>
    -   <span data-ttu-id="8a24a-134">AllowSimpleDevicePassword</span><span class="sxs-lookup"><span data-stu-id="8a24a-134">AllowSimpleDevicePassword</span></span>
    -   <span data-ttu-id="8a24a-135">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="8a24a-135">MinDevicePasswordLength</span></span>
    -   <span data-ttu-id="8a24a-136">AlphanumericDevicePasswordRequired é a política pai de:</span><span class="sxs-lookup"><span data-stu-id="8a24a-136">AlphanumericDevicePasswordRequired is the parent policy of:</span></span>
        -   <span data-ttu-id="8a24a-137">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="8a24a-137">MinDevicePasswordComplexCharacters</span></span> 
    -   <span data-ttu-id="8a24a-138">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="8a24a-138">MaxDevicePasswordFailedAttempts</span></span>
    -   <span data-ttu-id="8a24a-139">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="8a24a-139">MaxInactivityTimeDeviceLock</span></span>

</dd> <dt>

[<span data-ttu-id="8a24a-140">DevicePasswordExpiration</span><span class="sxs-lookup"><span data-stu-id="8a24a-140">DevicePasswordExpiration</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordexpiration)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8a24a-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8a24a-143">DevicePasswordHistory</span><span class="sxs-lookup"><span data-stu-id="8a24a-143">DevicePasswordHistory</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-devicepasswordhistory)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-144">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8a24a-144">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-145">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8a24a-146">EnforceLockScreenAndLogonImage</span><span class="sxs-lookup"><span data-stu-id="8a24a-146">EnforceLockScreenAndLogonImage</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-enforcelockscreenandlogonimage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a24a-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-148">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8a24a-149">EnforceLockScreenProvider</span><span class="sxs-lookup"><span data-stu-id="8a24a-149">EnforceLockScreenProvider</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a24a-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-151">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-151">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8a24a-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="8a24a-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a24a-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a24a-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-155">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8a24a-155">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8a24a-156">Identifica o nome do nó pai.</span><span class="sxs-lookup"><span data-stu-id="8a24a-156">Identifies the name of the parent node.</span></span> <span data-ttu-id="8a24a-157">Para essa classe, a cadeia de caracteres é "DeviceLock".</span><span class="sxs-lookup"><span data-stu-id="8a24a-157">For this class, the string is "DeviceLock".</span></span>

</dd> <dt>

[<span data-ttu-id="8a24a-158">MaxDevicePasswordFailedAttempts</span><span class="sxs-lookup"><span data-stu-id="8a24a-158">MaxDevicePasswordFailedAttempts</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxdevicepasswordfailedattempts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-159">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8a24a-159">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-160">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-160">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8a24a-161">MaxInactivityTimeDeviceLock</span><span class="sxs-lookup"><span data-stu-id="8a24a-161">MaxInactivityTimeDeviceLock</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-maxinactivitytimedevicelock)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-162">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8a24a-162">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-163">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-163">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8a24a-164">MinDevicePasswordComplexCharacters</span><span class="sxs-lookup"><span data-stu-id="8a24a-164">MinDevicePasswordComplexCharacters</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordcomplexcharacters)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-165">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8a24a-165">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-166">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-166">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8a24a-167">MinDevicePasswordLength</span><span class="sxs-lookup"><span data-stu-id="8a24a-167">MinDevicePasswordLength</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-mindevicepasswordlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-168">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8a24a-168">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-169">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-169">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="8a24a-170">MinimumPasswordAge</span><span class="sxs-lookup"><span data-stu-id="8a24a-170">MinimumPasswordAge</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-minimumpasswordage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-171">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8a24a-171">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-172">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-172">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8a24a-173">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="8a24a-173">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a24a-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8a24a-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-176">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="8a24a-176">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="8a24a-177">Descreve o caminho completo para o nó pai.</span><span class="sxs-lookup"><span data-stu-id="8a24a-177">Describes the full path to the parent node.</span></span> <span data-ttu-id="8a24a-178">Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/Policy/Config"</span><span class="sxs-lookup"><span data-stu-id="8a24a-178">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="8a24a-179">PreventLockScreenSlideShow</span><span class="sxs-lookup"><span data-stu-id="8a24a-179">PreventLockScreenSlideShow</span></span>](/windows/client-management/mdm/policy-csp-devicelock#devicelock-preventlockscreenslideshow)
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8a24a-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-181">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-181">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="8a24a-182">ScreenTimeoutWhileLocked</span><span class="sxs-lookup"><span data-stu-id="8a24a-182">ScreenTimeoutWhileLocked</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8a24a-183">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="8a24a-183">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="8a24a-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8a24a-184">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8a24a-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a24a-185">Requirements</span></span>



| <span data-ttu-id="8a24a-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a24a-186">Requirement</span></span> | <span data-ttu-id="8a24a-187">Valor</span><span class="sxs-lookup"><span data-stu-id="8a24a-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a24a-188">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a24a-188">Minimum supported client</span></span><br/> | <span data-ttu-id="8a24a-189">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="8a24a-189">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8a24a-190">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8a24a-190">Minimum supported server</span></span><br/> | <span data-ttu-id="8a24a-191">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="8a24a-191">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="8a24a-192">Namespace</span><span class="sxs-lookup"><span data-stu-id="8a24a-192">Namespace</span></span><br/>                | <span data-ttu-id="8a24a-193">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="8a24a-193">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="8a24a-194">MOF</span><span class="sxs-lookup"><span data-stu-id="8a24a-194">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8a24a-195"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8a24a-195"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8a24a-196">DLL</span><span class="sxs-lookup"><span data-stu-id="8a24a-196">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a24a-197"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a24a-197"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a24a-198">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a24a-198">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a24a-199">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="8a24a-199">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

