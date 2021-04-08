---
title: Classe MDM_SharedPC
description: A \_ classe MDM SharedPC é usada para definir configurações para uso compartilhado de computador.
ms.assetid: 90985c4d-601e-4827-aee0-13524a69f759
keywords:
- Classe MDM_SharedPC
- Classe MDM_SharedPC, descrita
topic_type:
- apiref
api_name:
- MDM_SharedPC
- MDM_SharedPC.InstanceID
- MDM_SharedPC.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7b515e4b794e2048ab26c8e1a32bfe7d3c4b50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008898"
---
# <a name="mdm_sharedpc-class"></a><span data-ttu-id="7ba35-105">\_Classe SharedPC do MDM</span><span class="sxs-lookup"><span data-stu-id="7ba35-105">MDM\_SharedPC class</span></span>

<span data-ttu-id="7ba35-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="7ba35-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7ba35-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="7ba35-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7ba35-108">A \_ classe MDM SharedPC é usada para definir configurações para uso compartilhado de computador.</span><span class="sxs-lookup"><span data-stu-id="7ba35-108">The MDM\_SharedPC class is used to configure settings for shared PC usage.</span></span>

<span data-ttu-id="7ba35-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7ba35-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba35-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ba35-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SharedPC
{
  string  InstanceID;
  string  ParentID;
  boolean EnableSharedPCMode;
  boolean SetEduPolicies;
  boolean SetPowerPolicies;
  sint32  MaintenanceStartTime;
  boolean SignInOnResume;
  sint32  SleepTimeout;
  boolean EnableAccountManager;
  sint32  AccountModel;
  sint32  DeletionPolicy;
  sint32  DiskLevelDeletion;
  sint32  DiskLevelCaching;
  boolean RestrictLocalStorage;
  string  KioskModeAUMID;
  string  KioskModeUserTileDisplayText;
  sint32  InactiveThreshold;
  sint32  MaxPageFileSizeMB;
};
```

## <a name="members"></a><span data-ttu-id="7ba35-111">Membros</span><span class="sxs-lookup"><span data-stu-id="7ba35-111">Members</span></span>

<span data-ttu-id="7ba35-112">A classe **MDM \_ SharedPC** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7ba35-112">The **MDM\_SharedPC** class has these types of members:</span></span>

-   [<span data-ttu-id="7ba35-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7ba35-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ba35-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7ba35-114">Properties</span></span>

<span data-ttu-id="7ba35-115">A classe **MDM \_ SharedPC** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7ba35-115">The **MDM\_SharedPC** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7ba35-116">AccountModel</span><span class="sxs-lookup"><span data-stu-id="7ba35-116">AccountModel</span></span>](/windows/client-management/mdm/sharedpc-csp#accountmodel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7ba35-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-119">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-119">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="7ba35-120">DeletionPolicy</span><span class="sxs-lookup"><span data-stu-id="7ba35-120">DeletionPolicy</span></span>](/windows/client-management/mdm/sharedpc-csp#deletionpolicy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-121">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7ba35-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-122">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-123">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-123">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="7ba35-124">DiskLevelCaching</span><span class="sxs-lookup"><span data-stu-id="7ba35-124">DiskLevelCaching</span></span>](/windows/client-management/mdm/sharedpc-csp#disklevelcaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-125">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7ba35-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-126">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-127">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-127">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="7ba35-128">DiskLevelDeletion</span><span class="sxs-lookup"><span data-stu-id="7ba35-128">DiskLevelDeletion</span></span>](/windows/client-management/mdm/sharedpc-csp#diskleveldeletion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-129">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7ba35-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-131">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-131">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="7ba35-132">EnableAccountManager</span><span class="sxs-lookup"><span data-stu-id="7ba35-132">EnableAccountManager</span></span>](/windows/client-management/mdm/sharedpc-csp#enableaccountmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-133">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7ba35-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-134">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-135">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-135">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="7ba35-136">EnableSharedPCMode</span><span class="sxs-lookup"><span data-stu-id="7ba35-136">EnableSharedPCMode</span></span>](/windows/client-management/mdm/sharedpc-csp#enablesharedpcmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-137">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7ba35-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-139">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-139">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="7ba35-140">InactiveThreshold</span><span class="sxs-lookup"><span data-stu-id="7ba35-140">InactiveThreshold</span></span>](/windows/client-management/mdm/sharedpc-csp#inactivethreshold)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-141">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7ba35-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-142">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-143">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-143">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

<span data-ttu-id="7ba35-144">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7ba35-144">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7ba35-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7ba35-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-147">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7ba35-147">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7ba35-148">KioskModeAUMID</span><span class="sxs-lookup"><span data-stu-id="7ba35-148">KioskModeAUMID</span></span>](/windows/client-management/mdm/sharedpc-csp#kioskmodeaumid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7ba35-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-151">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-151">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="7ba35-152">KioskModeUserTileDisplayText</span><span class="sxs-lookup"><span data-stu-id="7ba35-152">KioskModeUserTileDisplayText</span></span>](/windows/client-management/mdm/sharedpc-csp#kioskmodeusertiledisplaytext)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7ba35-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-154">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-155">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-155">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="7ba35-156">MaintenanceStartTime</span><span class="sxs-lookup"><span data-stu-id="7ba35-156">MaintenanceStartTime</span></span>](/windows/client-management/mdm/sharedpc-csp#maintenancestarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-157">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7ba35-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-158">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-159">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-159">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="7ba35-160">MaxPageFileSizeMB</span><span class="sxs-lookup"><span data-stu-id="7ba35-160">MaxPageFileSizeMB</span></span>](/windows/client-management/mdm/sharedpc-csp#maxpagefilesizemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-161">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7ba35-161">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-162">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-163">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-163">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

<span data-ttu-id="7ba35-164">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7ba35-164">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7ba35-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7ba35-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-167">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7ba35-167">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7ba35-168">RestrictLocalStorage</span><span class="sxs-lookup"><span data-stu-id="7ba35-168">RestrictLocalStorage</span></span>](/windows/client-management/mdm/sharedpc-csp#restrictlocalstorage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-169">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7ba35-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-170">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-171">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-171">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="7ba35-172">SetEduPolicies</span><span class="sxs-lookup"><span data-stu-id="7ba35-172">SetEduPolicies</span></span>](/windows/client-management/mdm/sharedpc-csp#setedupolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-173">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7ba35-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-174">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-175">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-175">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="7ba35-176">SetPowerPolicies</span><span class="sxs-lookup"><span data-stu-id="7ba35-176">SetPowerPolicies</span></span>](/windows/client-management/mdm/sharedpc-csp#setpowerpolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-177">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7ba35-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-178">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-179">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-179">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="7ba35-180">SignInOnResume</span><span class="sxs-lookup"><span data-stu-id="7ba35-180">SignInOnResume</span></span>](/windows/client-management/mdm/sharedpc-csp#signinonresume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-181">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7ba35-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-182">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-183">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-183">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="7ba35-184">SleepTimeout</span><span class="sxs-lookup"><span data-stu-id="7ba35-184">SleepTimeout</span></span>](/windows/client-management/mdm/sharedpc-csp#sleeptimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ba35-185">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7ba35-185">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7ba35-186">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="7ba35-186">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ba35-187">Para obter informações adicionais, consulte [CSP do SharedPC](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="7ba35-187">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ba35-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ba35-188">Requirements</span></span>



| <span data-ttu-id="7ba35-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ba35-189">Requirement</span></span> | <span data-ttu-id="7ba35-190">Valor</span><span class="sxs-lookup"><span data-stu-id="7ba35-190">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba35-191">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ba35-191">Minimum supported client</span></span><br/> | <span data-ttu-id="7ba35-192">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7ba35-192">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7ba35-193">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7ba35-193">Minimum supported server</span></span><br/> | <span data-ttu-id="7ba35-194">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7ba35-194">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="7ba35-195">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ba35-195">Namespace</span></span><br/>                | <span data-ttu-id="7ba35-196">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="7ba35-196">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="7ba35-197">MOF</span><span class="sxs-lookup"><span data-stu-id="7ba35-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ba35-198"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ba35-198"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ba35-199">DLL</span><span class="sxs-lookup"><span data-stu-id="7ba35-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ba35-200"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ba35-200"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

