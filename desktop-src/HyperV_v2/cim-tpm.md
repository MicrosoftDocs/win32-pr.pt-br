---
description: Descreve um dispositivo Trusted Platform Module (TPM).
ms.assetid: c923106f-126e-4e7e-822a-2fb715bbbc26
title: Classe CIM_TPM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TPM
- CIM_TPM.TPMSpecMajorVersion
- CIM_TPM.TPMSpecMinorVersion
- CIM_TPM.TPMManafucturerMajorRevision
- CIM_TPM.TPMManufacturerMinorRevision
- CIM_TPM.TPMManufacturerInfo
- CIM_TPM.TPMManufacturerId
- CIM_TPM.TPMState
- CIM_TPM.TransitioningToTPMState
- CIM_TPM.AvailableRequestedTPMStates
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f2d35d42e864a247ca042ec81813ff7d1ac5c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010834"
---
# <a name="cim_tpm-class"></a><span data-ttu-id="0a4f6-103">\_Classe TPM CIM</span><span class="sxs-lookup"><span data-stu-id="0a4f6-103">CIM\_TPM class</span></span>

<span data-ttu-id="0a4f6-104">Descreve um dispositivo Trusted Platform Module (TPM).</span><span class="sxs-lookup"><span data-stu-id="0a4f6-104">Describes a Trusted Platform Module (TPM) device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a4f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0a4f6-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.21.0"), UMLPackagePath("CIM::Device::TPM"), AMENDMENT]
class CIM_TPM : CIM_LogicalDevice
{
  uint32 TPMSpecMajorVersion;
  uint32 TPMSpecMinorVersion;
  uint32 TPMManafucturerMajorRevision;
  uint32 TPMManufacturerMinorRevision;
  string TPMManufacturerInfo;
  uint32 TPMManufacturerId;
  uint16 TPMState;
  uint16 TransitioningToTPMState = 12;
  uint16 AvailableRequestedTPMStates[];
};
```

## <a name="members"></a><span data-ttu-id="0a4f6-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0a4f6-106">Members</span></span>

<span data-ttu-id="0a4f6-107">A classe **CIM \_ TPM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0a4f6-107">The **CIM\_TPM** class has these types of members:</span></span>

-   [<span data-ttu-id="0a4f6-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="0a4f6-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="0a4f6-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0a4f6-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0a4f6-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="0a4f6-110">Methods</span></span>

<span data-ttu-id="0a4f6-111">A classe **CIM \_ TPM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-111">The **CIM\_TPM** class has these methods.</span></span>



| <span data-ttu-id="0a4f6-112">Método</span><span class="sxs-lookup"><span data-stu-id="0a4f6-112">Method</span></span>                                                         | <span data-ttu-id="0a4f6-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a4f6-113">Description</span></span>                                                                                                             |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0a4f6-114">**ChangeOwnerAuth**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-114">**ChangeOwnerAuth**</span></span>](cim-tpm-changeownerauth.md)             | <span data-ttu-id="0a4f6-115">Altera a credencial de autorização do proprietário de um dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-115">Changes the owner authorization credential of a TPM device.</span></span><br/>                                                  |
| [<span data-ttu-id="0a4f6-116">**RequestTPMStateChange**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-116">**RequestTPMStateChange**</span></span>](cim-tpm-requesttpmstatechange.md) | <span data-ttu-id="0a4f6-117">Solicita que o estado do TPM seja alterado para o valor especificado no parâmetro **RequestedTPMState** .</span><span class="sxs-lookup"><span data-stu-id="0a4f6-117">Requests that the state of the TPM be changed to the value specified in the **RequestedTPMState** parameter.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="0a4f6-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0a4f6-118">Properties</span></span>

<span data-ttu-id="0a4f6-119">A classe **CIM \_ TPM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-119">The **CIM\_TPM** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0a4f6-120">**AvailableRequestedTPMStates**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-120">**AvailableRequestedTPMStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a4f6-121">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0a4f6-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-123">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ TPM CIM**.**RequestTPMStateChange**, CIM \_ TPMCapabilities. RequestedTPMStatesSupported ")</span><span class="sxs-lookup"><span data-stu-id="0a4f6-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**, CIM\_TPMCapabilities.RequestedTPMStatesSupported")</span></span>
</dt> </dl>

<span data-ttu-id="0a4f6-124">Os valores possíveis para o parâmetro *RequestedTPMState* do método [**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md) .</span><span class="sxs-lookup"><span data-stu-id="0a4f6-124">The possible values for the *RequestedTPMState* parameter of the [**RequestTPMStateChange**](cim-tpm-requesttpmstatechange.md) method.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0a4f6-125">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-125">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="0a4f6-126">**S1 habilitado – ativo-de propriedade** (2)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-126">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="0a4f6-127">**S2 desabilitado-ativo-proprietário** (3)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-127">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="0a4f6-128">**S3 habilitado-inativo-de propriedade** (4)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-128">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="0a4f6-129">**S4 desabilitado-inativo-de propriedade** (5)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-129">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="0a4f6-130">**S5 habilitado-ativo-sem proprietário** (6)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-130">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="0a4f6-131">**S6 desabilitado – ativo-sem proprietário** (7)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-131">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="0a4f6-132">**S7 habilitado – inativo – sem proprietário** (8)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-132">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="0a4f6-133">**S8 desabilitado-inativo – sem proprietário** (9)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-133">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0a4f6-134">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-134">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0a4f6-135">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-135">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0a4f6-136">**TPMManafucturerMajorRevision**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-136">**TPMManafucturerMajorRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a4f6-137">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0a4f6-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-139">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| parte 2 v1dot2 \| seção 5,3 \| versão \| revMajor ")</span><span class="sxs-lookup"><span data-stu-id="0a4f6-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|revMajor")</span></span>
</dt> </dl>

<span data-ttu-id="0a4f6-140">A revisão principal do fabricante do TPM.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-140">The manufacturer major revision of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="0a4f6-141">**TPMManufacturerId**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-141">**TPMManufacturerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a4f6-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0a4f6-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-144">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| Part 2 v1dot2 \| seção 21,6 \| TPM \_ Cap \_ informações de versão \_ \| tpmVendorID ")</span><span class="sxs-lookup"><span data-stu-id="0a4f6-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 21.6\|TPM\_CAP\_VERSION\_INFO\|tpmVendorID")</span></span>
</dt> </dl>

<span data-ttu-id="0a4f6-145">A ID do fabricante do TPM.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-145">The TPM manufacturer ID.</span></span>

</dd> <dt>

<span data-ttu-id="0a4f6-146">**TPMManufacturerInfo**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-146">**TPMManufacturerInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a4f6-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0a4f6-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-149">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| Part 2 v 1.2. TCG \| seção 21,6 \| TPM \_ Cap \_ version \_ info \| vendorSpecific ")</span><span class="sxs-lookup"><span data-stu-id="0a4f6-149">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1.2.TCG\|Section 21.6\|TPM\_CAP\_VERSION\_INFO\|vendorSpecific")</span></span>
</dt> </dl>

<span data-ttu-id="0a4f6-150">As informações adicionais definidas pelo fabricante do TPM.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-150">The additional information defined by the TPM manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="0a4f6-151">**TPMManufacturerMinorRevision**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-151">**TPMManufacturerMinorRevision**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a4f6-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0a4f6-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-154">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| parte 2 v1dot2 \| seção 5,3 \| versão \| revMinor ")</span><span class="sxs-lookup"><span data-stu-id="0a4f6-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|revMinor")</span></span>
</dt> </dl>

<span data-ttu-id="0a4f6-155">A revisão mínima do fabricante do TPM.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-155">The manufacturer minor revision of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="0a4f6-156">**TPMSpecMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-156">**TPMSpecMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a4f6-157">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0a4f6-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-159">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| Part 2 v1dot2 \| seção 5,3 \| versão \| principal "," TSS. O TCG \| nível 1 v 1.2 \| seção 2.3.2.18 ")</span><span class="sxs-lookup"><span data-stu-id="0a4f6-159">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|major", "TSS.TCG\|Level 1 v1.2\|Section 2.3.2.18")</span></span>
</dt> </dl>

<span data-ttu-id="0a4f6-160">A versão principal do TPM.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-160">The major version of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="0a4f6-161">**TPMSpecMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-161">**TPMSpecMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a4f6-162">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0a4f6-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-164">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| parte 2 v1dot2 \| seção 5,3 \| versão \| secundária "," TSS. O TCG \| nível 1 v 1.2 \| seção 2.3.2.18 ")</span><span class="sxs-lookup"><span data-stu-id="0a4f6-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 2 v1dot2\|Section 5.3\|version\|minor", "TSS.TCG\|Level 1 v1.2\|Section 2.3.2.18")</span></span>
</dt> </dl>

<span data-ttu-id="0a4f6-165">A versão secundária do TPM.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-165">The minor version of the TPM.</span></span>

</dd> <dt>

<span data-ttu-id="0a4f6-166">**TPMState**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-166">**TPMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a4f6-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0a4f6-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-169">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM. TCG \| parte 1 v1dot2 \| seção 9,4 "," TPM. TCG \| parte 2 v1dot2 \| seção 7,1 \| \_ sinalizadores permanentes do TPM \_ "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ TPM do CIM**.**RequestTPMStateChange**","**\_ TPM CIM**.**TransitioningToTPMState**")</span><span class="sxs-lookup"><span data-stu-id="0a4f6-169">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("TPM.TCG\|Part 1 v1dot2\|Section 9.4", "TPM.TCG\|Part 2 v1dot2\|Section 7.1\|TPM\_PERMANENT\_FLAGS"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**", "**CIM\_TPM**.**TransitioningToTPMState**")</span></span>
</dt> </dl>

<span data-ttu-id="0a4f6-170">O estado operacional do TPM.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-170">The operational state of the TPM.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0a4f6-171">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-171">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="0a4f6-172">**S1 habilitado – ativo-de propriedade** (2)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-172">**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="0a4f6-173">**S2 desabilitado-ativo-proprietário** (3)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-173">**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="0a4f6-174">**S3 habilitado-inativo-de propriedade** (4)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-174">**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="0a4f6-175">**S4 desabilitado-inativo-de propriedade** (5)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-175">**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="0a4f6-176">**S5 habilitado-ativo-sem proprietário** (6)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-176">**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="0a4f6-177">**S6 desabilitado – ativo-sem proprietário** (7)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-177">**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="0a4f6-178">**S7 habilitado – inativo – sem proprietário** (8)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-178">**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="0a4f6-179">**S8 desabilitado-inativo – sem proprietário** (9)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-179">**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0a4f6-180">**Não aplicável** (10)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-180">**Not Applicable** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0a4f6-181">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-181">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0a4f6-182">**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-182">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="0a4f6-183">**TransitioningToTPMState**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-183">**TransitioningToTPMState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0a4f6-184">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0a4f6-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0a4f6-186">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ TPM CIM**.**RequestTPMStateChange**","**\_ TPM CIM**.**TPMState**")</span><span class="sxs-lookup"><span data-stu-id="0a4f6-186">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_TPM**.**RequestTPMStateChange**", "**CIM\_TPM**.**TPMState**")</span></span>
</dt> </dl>

<span data-ttu-id="0a4f6-187">O estado de destino para o qual o TPM está em transição.</span><span class="sxs-lookup"><span data-stu-id="0a4f6-187">The target state to which the TPM is transitioning.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0a4f6-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="0a4f6-189"><span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**S1 habilitado – ativo-de propriedade** (2)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-189"><span id="S1_Enabled-Active-Owned"></span><span id="s1_enabled-active-owned"></span><span id="S1_ENABLED-ACTIVE-OWNED"></span>**S1 Enabled-Active-Owned** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>

<span data-ttu-id="0a4f6-190"><span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 desabilitado-ativo-proprietário** (3)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-190"><span id="S2_Disabled-Active-Owned"></span><span id="s2_disabled-active-owned"></span><span id="S2_DISABLED-ACTIVE-OWNED"></span>**S2 Disabled-Active-Owned** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="0a4f6-191"><span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**S3 habilitado-inativo-de propriedade** (4)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-191"><span id="S3_Enabled-Inactive-Owned"></span><span id="s3_enabled-inactive-owned"></span><span id="S3_ENABLED-INACTIVE-OWNED"></span>**S3 Enabled-Inactive-Owned** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>

<span data-ttu-id="0a4f6-192"><span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**S4 desabilitado-inativo-de propriedade** (5)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-192"><span id="S4_Disabled-Inactive-Owned"></span><span id="s4_disabled-inactive-owned"></span><span id="S4_DISABLED-INACTIVE-OWNED"></span>**S4 Disabled-Inactive-Owned** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="0a4f6-193"><span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**S5 habilitado-ativo-sem proprietário** (6)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-193"><span id="S5_Enabled-Active-Unowned"></span><span id="s5_enabled-active-unowned"></span><span id="S5_ENABLED-ACTIVE-UNOWNED"></span>**S5 Enabled-Active-Unowned** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>

<span data-ttu-id="0a4f6-194"><span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 desabilitado – ativo-sem proprietário** (7)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-194"><span id="S6_Disabled-Active-Unowned"></span><span id="s6_disabled-active-unowned"></span><span id="S6_DISABLED-ACTIVE-UNOWNED"></span>**S6 Disabled-Active-Unowned** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="0a4f6-195"><span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 habilitado – inativo – sem proprietário** (8)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-195"><span id="S7_Enabled-Inactive-Unowned"></span><span id="s7_enabled-inactive-unowned"></span><span id="S7_ENABLED-INACTIVE-UNOWNED"></span>**S7 Enabled-Inactive-Unowned** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>

<span data-ttu-id="0a4f6-196"><span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 desabilitado-inativo – sem proprietário** (9)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-196"><span id="S8_Disabled-Inactive-Unowned"></span><span id="s8_disabled-inactive-unowned"></span><span id="S8_DISABLED-INACTIVE-UNOWNED"></span>**S8 Disabled-Inactive-Unowned** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="0a4f6-197"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (10)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-197"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="0a4f6-198"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**Nenhuma alteração** (11)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-198"><span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>**No Change** (11)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0a4f6-199">12</span><span class="sxs-lookup"><span data-stu-id="0a4f6-199">(12)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="0a4f6-200"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-200"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="0a4f6-201"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="0a4f6-201"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


<span data-ttu-id="0a4f6-202"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0a4f6-202"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0a4f6-203">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a4f6-203">Requirements</span></span>



| <span data-ttu-id="0a4f6-204">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a4f6-204">Requirement</span></span> | <span data-ttu-id="0a4f6-205">Valor</span><span class="sxs-lookup"><span data-stu-id="0a4f6-205">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a4f6-206">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a4f6-206">Minimum supported client</span></span><br/> | <span data-ttu-id="0a4f6-207">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0a4f6-207">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0a4f6-208">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0a4f6-208">Minimum supported server</span></span><br/> | <span data-ttu-id="0a4f6-209">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0a4f6-209">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0a4f6-210">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a4f6-210">Namespace</span></span><br/>                | <span data-ttu-id="0a4f6-211">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0a4f6-211">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0a4f6-212">MOF</span><span class="sxs-lookup"><span data-stu-id="0a4f6-212">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0a4f6-213"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0a4f6-213"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0a4f6-214">DLL</span><span class="sxs-lookup"><span data-stu-id="0a4f6-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a4f6-215"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0a4f6-215"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0a4f6-216">Confira também</span><span class="sxs-lookup"><span data-stu-id="0a4f6-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a4f6-217">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="0a4f6-217">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

