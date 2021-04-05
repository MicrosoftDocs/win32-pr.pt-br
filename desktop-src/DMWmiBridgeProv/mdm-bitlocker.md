---
title: Classe MDM_BitLocker
description: A \_ classe MDM BitLocker é usada pela empresa para gerenciar a criptografia de computadores e dispositivos.
ms.assetid: e8bea6dc-8d3d-46d2-b2e3-9a4c547a639f
keywords:
- Classe MDM_BitLocker
- Classe MDM_BitLocker, descrita
topic_type:
- apiref
api_name:
- MDM_BitLocker
- MDM_BitLocker.InstanceID
- MDM_BitLocker.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94db491333cada64b6287dc87ec233b420bf0f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086375"
---
# <a name="mdm_bitlocker-class"></a><span data-ttu-id="1da9e-105">\_Classe BitLocker do MDM</span><span class="sxs-lookup"><span data-stu-id="1da9e-105">MDM\_BitLocker class</span></span>

<span data-ttu-id="1da9e-106">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="1da9e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1da9e-107">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="1da9e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1da9e-108">A \_ classe MDM BitLocker é usada pela empresa para gerenciar a criptografia de computadores e dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1da9e-108">The MDM\_BitLocker class is used by the enterprise to manage encryption of PCs and devices.</span></span>

<span data-ttu-id="1da9e-109">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1da9e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1da9e-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1da9e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_BitLocker
{
  string InstanceID;
  string ParentID;
  sint32 RequireStorageCardEncryption;
  sint32 RequireDeviceEncryption;
  string EncryptionMethodByDriveType;
  string SystemDrivesRequireStartupAuthentication;
  string SystemDrivesMinimumPINLength;
  string SystemDrivesRecoveryMessage;
  string SystemDrivesRecoveryOptions;
  string FixedDrivesRecoveryOptions;
  string FixedDrivesRequireEncryption;
  string RemovableDrivesRequireEncryption;
  sint32 AllowWarningForOtherDiskEncryption;
};
```

## <a name="members"></a><span data-ttu-id="1da9e-111">Membros</span><span class="sxs-lookup"><span data-stu-id="1da9e-111">Members</span></span>

<span data-ttu-id="1da9e-112">A classe **MDM \_ BitLocker** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1da9e-112">The **MDM\_BitLocker** class has these types of members:</span></span>

-   [<span data-ttu-id="1da9e-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1da9e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1da9e-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1da9e-114">Properties</span></span>

<span data-ttu-id="1da9e-115">A classe **MDM \_ BitLocker** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1da9e-115">The **MDM\_BitLocker** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1da9e-116">AllowWarningForOtherDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="1da9e-116">AllowWarningForOtherDiskEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#allowwarningforotherdiskencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da9e-117">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1da9e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-118">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1da9e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1da9e-119">EncryptionMethodByDriveType</span><span class="sxs-lookup"><span data-stu-id="1da9e-119">EncryptionMethodByDriveType</span></span>](/windows/client-management/mdm/bitlocker-csp#encryptionmethodbydrivetype)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da9e-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1da9e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-121">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1da9e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1da9e-122">FixedDrivesRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="1da9e-122">FixedDrivesRecoveryOptions</span></span>](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da9e-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1da9e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1da9e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1da9e-125">FixedDrivesRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="1da9e-125">FixedDrivesRequireEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrequireencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da9e-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1da9e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1da9e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1da9e-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1da9e-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da9e-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1da9e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1da9e-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-131">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1da9e-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1da9e-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1da9e-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da9e-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1da9e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1da9e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-135">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1da9e-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1da9e-136">RemovableDrivesRequireEncryption</span><span class="sxs-lookup"><span data-stu-id="1da9e-136">RemovableDrivesRequireEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#removabledrivesrequireencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da9e-137">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1da9e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-138">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1da9e-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1da9e-139">RequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="1da9e-139">RequireDeviceEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#requiredeviceencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da9e-140">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1da9e-140">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-141">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1da9e-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1da9e-142">RequireStorageCardEncryption</span><span class="sxs-lookup"><span data-stu-id="1da9e-142">RequireStorageCardEncryption</span></span>](/windows/client-management/mdm/bitlocker-csp#requirestoragecardencryption)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da9e-143">Tipo de dados: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1da9e-143">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-144">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1da9e-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1da9e-145">SystemDrivesMinimumPINLength</span><span class="sxs-lookup"><span data-stu-id="1da9e-145">SystemDrivesMinimumPINLength</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesminimumpinlength)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da9e-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1da9e-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-147">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1da9e-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1da9e-148">SystemDrivesRecoveryMessage</span><span class="sxs-lookup"><span data-stu-id="1da9e-148">SystemDrivesRecoveryMessage</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoverymessage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da9e-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1da9e-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-150">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1da9e-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1da9e-151">SystemDrivesRecoveryOptions</span><span class="sxs-lookup"><span data-stu-id="1da9e-151">SystemDrivesRecoveryOptions</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da9e-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1da9e-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-153">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1da9e-153">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1da9e-154">SystemDrivesRequireStartupAuthentication</span><span class="sxs-lookup"><span data-stu-id="1da9e-154">SystemDrivesRequireStartupAuthentication</span></span>](/windows/client-management/mdm/bitlocker-csp#systemdrivesrequirestartupauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1da9e-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1da9e-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1da9e-156">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1da9e-156">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1da9e-157">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1da9e-157">Requirements</span></span>



| <span data-ttu-id="1da9e-158">Requisito</span><span class="sxs-lookup"><span data-stu-id="1da9e-158">Requirement</span></span> | <span data-ttu-id="1da9e-159">Valor</span><span class="sxs-lookup"><span data-stu-id="1da9e-159">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1da9e-160">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1da9e-160">Minimum supported client</span></span><br/> | <span data-ttu-id="1da9e-161">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1da9e-161">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1da9e-162">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1da9e-162">Minimum supported server</span></span><br/> | <span data-ttu-id="1da9e-163">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1da9e-163">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="1da9e-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="1da9e-164">Namespace</span></span><br/>                | <span data-ttu-id="1da9e-165">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="1da9e-165">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="1da9e-166">MOF</span><span class="sxs-lookup"><span data-stu-id="1da9e-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1da9e-167"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1da9e-167"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="1da9e-168">DLL</span><span class="sxs-lookup"><span data-stu-id="1da9e-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1da9e-169"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1da9e-169"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

