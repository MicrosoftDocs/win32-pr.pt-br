---
description: Representa o estado configurado do dispositivo TPM.
ms.assetid: 948ccb47-3626-48f1-b18f-ef1d05978b21
title: Classe Msvm_TPMSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TPMSettingData
- Msvm_TPMSettingData.Shielded
- Msvm_TPMSettingData.DataProtected
- Msvm_TPMSettingData.EnabledState
- Msvm_TPMSettingData.KeyProtector
- Msvm_TPMSettingData.LastKnownGoodKeyProtector
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8a14f50f01212129ed34cc7e45ee28facbdb991f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502194"
---
# <a name="msvm_tpmsettingdata-class"></a><span data-ttu-id="b82ce-103">\_Classe Msvm TPMSettingData</span><span class="sxs-lookup"><span data-stu-id="b82ce-103">Msvm\_TPMSettingData class</span></span>

<span data-ttu-id="b82ce-104">Representa o estado configurado do dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="b82ce-104">Represents the configured state of the TPM device.</span></span>

<span data-ttu-id="b82ce-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b82ce-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b82ce-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b82ce-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TPMSettingData : CIM_ResourceAllocationSettingData
{
  boolean Shielded = FALSE;
  boolean DataProtected = FALSE;
  uint16  EnabledState = 3;
  uint8   KeyProtector[];
  uint8   LastKnownGoodKeyProtector[];
};
```

## <a name="members"></a><span data-ttu-id="b82ce-107">Membros</span><span class="sxs-lookup"><span data-stu-id="b82ce-107">Members</span></span>

<span data-ttu-id="b82ce-108">A classe **Msvm \_ TPMSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b82ce-108">The **Msvm\_TPMSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b82ce-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b82ce-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b82ce-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b82ce-110">Properties</span></span>

<span data-ttu-id="b82ce-111">A classe **Msvm \_ TPMSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b82ce-111">The **Msvm\_TPMSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b82ce-112">**Protegido por dataprotegida**</span><span class="sxs-lookup"><span data-stu-id="b82ce-112">**DataProtected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b82ce-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b82ce-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b82ce-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b82ce-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b82ce-115">Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b82ce-115">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b82ce-116">**true** para definir uma política para proteger os dados de uma VM; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="b82ce-116">**true** to set a policy to protect a VM's data; otherwise, **false**.</span></span> <span data-ttu-id="b82ce-117">Um TPM recém-criado está desabilitado, portanto, o estado inicial da proteção de dados é **false**.</span><span class="sxs-lookup"><span data-stu-id="b82ce-117">A newly created TPM is disabled, so the initial data protection state is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="b82ce-118">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="b82ce-118">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b82ce-119">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b82ce-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b82ce-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b82ce-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b82ce-121">Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b82ce-121">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b82ce-122">Os Estados habilitado e desabilitado de um elemento.</span><span class="sxs-lookup"><span data-stu-id="b82ce-122">The enabled and disabled states of an element.</span></span> <span data-ttu-id="b82ce-123">O valor padrão é **desabilitado**.</span><span class="sxs-lookup"><span data-stu-id="b82ce-123">The default value is **Disabled**.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="b82ce-124">**Habilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="b82ce-124">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="b82ce-125">**Desabilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="b82ce-125">**Disabled** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b82ce-126">**Keyprotector**</span><span class="sxs-lookup"><span data-stu-id="b82ce-126">**KeyProtector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b82ce-127">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="b82ce-127">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b82ce-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b82ce-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b82ce-129">Qualificadores: [**obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers), **octetstring**</span><span class="sxs-lookup"><span data-stu-id="b82ce-129">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span></span>
</dt> </dl>

<span data-ttu-id="b82ce-130">O protetor de chave do cliente do serviço guardião de host.</span><span class="sxs-lookup"><span data-stu-id="b82ce-130">The key protector from Host Guardian Service client.</span></span>

</dd> <dt>

<span data-ttu-id="b82ce-131">**LastKnownGoodKeyProtector**</span><span class="sxs-lookup"><span data-stu-id="b82ce-131">**LastKnownGoodKeyProtector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b82ce-132">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="b82ce-132">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="b82ce-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b82ce-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b82ce-134">Qualificadores: [**obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers), **octetstring**</span><span class="sxs-lookup"><span data-stu-id="b82ce-134">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), **OctetString**</span></span>
</dt> </dl>

<span data-ttu-id="b82ce-135">O último protetor de chave válido criptografou com êxito o estado do dispositivo TPM na última inicialização da VM.</span><span class="sxs-lookup"><span data-stu-id="b82ce-135">The last known good key protector successfully encrypted TPM device state in the last VM boot.</span></span>

<span data-ttu-id="b82ce-136">Essa propriedade é somente leitura para o cliente WMI e só pode ser modificada pelo dispositivo TPM de VM.</span><span class="sxs-lookup"><span data-stu-id="b82ce-136">This property is read-only for the WMI client, and can only be modified by the VM TPM device.</span></span>

</dd> <dt>

<span data-ttu-id="b82ce-137">**Blindado**</span><span class="sxs-lookup"><span data-stu-id="b82ce-137">**Shielded**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b82ce-138">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b82ce-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b82ce-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b82ce-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b82ce-140">Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b82ce-140">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b82ce-141">**true** para definir uma política que protege uma máquina virtual; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="b82ce-141">**true** to define a policy that shields a virtual machine; otherwise, **false**.</span></span> <span data-ttu-id="b82ce-142">Um TPM recém-criado está desabilitado, portanto, o estado de blindagem inicial é **false**.</span><span class="sxs-lookup"><span data-stu-id="b82ce-142">A newly created TPM is disabled, so the initial shielding state is **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b82ce-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b82ce-143">Requirements</span></span>



| <span data-ttu-id="b82ce-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="b82ce-144">Requirement</span></span> | <span data-ttu-id="b82ce-145">Valor</span><span class="sxs-lookup"><span data-stu-id="b82ce-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b82ce-146">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b82ce-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b82ce-147">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="b82ce-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="b82ce-148">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b82ce-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b82ce-149">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b82ce-149">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b82ce-150">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b82ce-150">End of client support</span></span><br/>    | <span data-ttu-id="b82ce-151">Windows 10</span><span class="sxs-lookup"><span data-stu-id="b82ce-151">Windows 10</span></span><br/>                                                                                   |
| <span data-ttu-id="b82ce-152">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b82ce-152">End of server support</span></span><br/>    | <span data-ttu-id="b82ce-153">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="b82ce-153">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="b82ce-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="b82ce-154">Namespace</span></span><br/>                | <span data-ttu-id="b82ce-155">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b82ce-155">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b82ce-156">MOF</span><span class="sxs-lookup"><span data-stu-id="b82ce-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b82ce-157"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b82ce-157"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b82ce-158">DLL</span><span class="sxs-lookup"><span data-stu-id="b82ce-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b82ce-159"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b82ce-159"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b82ce-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="b82ce-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b82ce-161">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="b82ce-161">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

