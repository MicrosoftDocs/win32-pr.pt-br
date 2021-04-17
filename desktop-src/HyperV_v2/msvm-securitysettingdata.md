---
description: Representa o estado configurado das configurações de segurança para.
ms.assetid: c57ab966-591e-4dd9-87be-0d2b81611d5d
title: Classe Msvm_SecuritySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecuritySettingData
- Msvm_SecuritySettingData.TpmEnabled
- Msvm_SecuritySettingData.KsdEnabled
- Msvm_SecuritySettingData.ShieldingRequested
- Msvm_SecuritySettingData.DataProtectionRequested
- Msvm_SecuritySettingData.EncryptStateAndVmMigrationTraffic
- Msvm_SecuritySettingData.VirtualizationBasedSecurityOptOut
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7125e06ad4ce33e70a8cf84b24933e7390e7a74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761708"
---
# <a name="msvm_securitysettingdata-class"></a><span data-ttu-id="9a019-103">\_Classe Msvm SecuritySettingData</span><span class="sxs-lookup"><span data-stu-id="9a019-103">Msvm\_SecuritySettingData class</span></span>

<span data-ttu-id="9a019-104">Representa o estado configurado das configurações de segurança para uma máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="9a019-104">Represents the configured state of the security settings for a virtual machine.</span></span>

<span data-ttu-id="9a019-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9a019-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a019-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a019-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecuritySettingData : CIM_SettingData
{
  boolean TpmEnabled;
  boolean KsdEnabled;
  boolean ShieldingRequested;
  boolean DataProtectionRequested;
  boolean EncryptStateAndVmMigrationTraffic;
  boolean VirtualizationBasedSecurityOptOut;
};
```

## <a name="members"></a><span data-ttu-id="9a019-107">Membros</span><span class="sxs-lookup"><span data-stu-id="9a019-107">Members</span></span>

<span data-ttu-id="9a019-108">A classe **Msvm \_ SecuritySettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9a019-108">The **Msvm\_SecuritySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="9a019-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9a019-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9a019-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9a019-110">Properties</span></span>

<span data-ttu-id="9a019-111">A classe **Msvm \_ SecuritySettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9a019-111">The **Msvm\_SecuritySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9a019-112">**DataProtectionRequested**</span><span class="sxs-lookup"><span data-stu-id="9a019-112">**DataProtectionRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a019-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9a019-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a019-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a019-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a019-115">Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9a019-115">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9a019-116">**true** para solicitar a proteção de dados para uma VM; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="9a019-116">**true** to request data protection for a VM; otherwise, **false**.</span></span> <span data-ttu-id="9a019-117">O valor padrão é **false.**</span><span class="sxs-lookup"><span data-stu-id="9a019-117">The default value is **false.**</span></span>

</dd> <dt>

<span data-ttu-id="9a019-118">**EncryptStateAndVmMigrationTraffic**</span><span class="sxs-lookup"><span data-stu-id="9a019-118">**EncryptStateAndVmMigrationTraffic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a019-119">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9a019-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a019-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a019-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a019-121">Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9a019-121">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9a019-122">**true** para ter o estado e a migração do tráfego de uma VM criptografada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="9a019-122">**true** to have the state and migration traffic of a VM encrypted; otherwise, **false**.</span></span> <span data-ttu-id="9a019-123">O valor padrão para uma VM recém-criada é **false**.</span><span class="sxs-lookup"><span data-stu-id="9a019-123">The default value for a newly-created VM is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="9a019-124">**KsdEnabled**</span><span class="sxs-lookup"><span data-stu-id="9a019-124">**KsdEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a019-125">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9a019-125">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a019-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a019-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a019-127">Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9a019-127">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9a019-128">**true** para habilitar um dispositivo de armazenamento de chave (KSD) para esta máquina virtual; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="9a019-128">**true** to enable a key storage device (KSD) for this virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="9a019-129">Uma VM recém-criada tem um Disable KSD.</span><span class="sxs-lookup"><span data-stu-id="9a019-129">A newly-created VM has a disable KSD.</span></span>

</dd> <dt>

<span data-ttu-id="9a019-130">**ShieldingRequested**</span><span class="sxs-lookup"><span data-stu-id="9a019-130">**ShieldingRequested**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a019-131">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9a019-131">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a019-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a019-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a019-133">Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9a019-133">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9a019-134">**true** para solicitar blindagem para uma VM; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="9a019-134">**true** to request shielding for a VM; otherwise, **false**.</span></span> <span data-ttu-id="9a019-135">Uma VM recém-criada tem um estado de blindagem inicial solicitado de **false**.</span><span class="sxs-lookup"><span data-stu-id="9a019-135">A newly-created VM has an initial shielding requested state of **false**.</span></span>

</dd> <dt>

<span data-ttu-id="9a019-136">**TpmEnabled**</span><span class="sxs-lookup"><span data-stu-id="9a019-136">**TpmEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a019-137">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9a019-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a019-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a019-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a019-139">Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9a019-139">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9a019-140">**true** para habilitar um TPM (Nodule Platform) confiável para esta máquina virtual; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="9a019-140">**true** to enable a trusted platform nodule (TPM) for this virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="9a019-141">Uma VM criada recentemente tem um desabilitar TPM.</span><span class="sxs-lookup"><span data-stu-id="9a019-141">A newly-created VM has a disable TPM.</span></span>

</dd> <dt>

<span data-ttu-id="9a019-142">**VirtualizationBasedSecurityOptOut**</span><span class="sxs-lookup"><span data-stu-id="9a019-142">**VirtualizationBasedSecurityOptOut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9a019-143">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9a019-143">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9a019-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9a019-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9a019-145">Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9a019-145">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9a019-146">**true** para não oferecer uma segurança baseada em virtualização de VM; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="9a019-146">**true** to not offer a VM virtualization-based security; otherwise, **false**.</span></span> <span data-ttu-id="9a019-147">A configuração padrão para o estado de aceitação de uma VM recém-criada é **false**.</span><span class="sxs-lookup"><span data-stu-id="9a019-147">The default setting for a newly-crated VM's opt-out state is **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a019-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a019-148">Requirements</span></span>



| <span data-ttu-id="9a019-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a019-149">Requirement</span></span> | <span data-ttu-id="9a019-150">Valor</span><span class="sxs-lookup"><span data-stu-id="9a019-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a019-151">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a019-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9a019-152">\[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]</span><span class="sxs-lookup"><span data-stu-id="9a019-152">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="9a019-153">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9a019-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9a019-154">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9a019-154">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="9a019-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="9a019-155">Namespace</span></span><br/>                | <span data-ttu-id="9a019-156">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="9a019-156">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="9a019-157">MOF</span><span class="sxs-lookup"><span data-stu-id="9a019-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9a019-158"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9a019-158"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9a019-159">DLL</span><span class="sxs-lookup"><span data-stu-id="9a019-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a019-160"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9a019-160"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9a019-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a019-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a019-162">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="9a019-162">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

