---
description: Indica um erro de componente de PCI de arquitetura de verificação de máquina (MCA). Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: 2b241333-2ea5-42cb-bdd3-27a10df51f3e
title: Classe MSMCAEvent_PCIComponentError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIComponentError
- MSMCAEvent_PCIComponentError.Active
- MSMCAEvent_PCIComponentError.AdditionalErrors
- MSMCAEvent_PCIComponentError.Cpu
- MSMCAEvent_PCIComponentError.ErrorSeverity
- MSMCAEvent_PCIComponentError.InstanceName
- MSMCAEvent_PCIComponentError.PCI_COMP_ERROR_STATUS
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_BusNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeBaseClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeInterface
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_ClassCodeSubClass
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceId
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_DeviceNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_FunctionNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_SegmentNumber
- MSMCAEvent_PCIComponentError.PCI_COMP_INFO_VendorId
- MSMCAEvent_PCIComponentError.RawRecord
- MSMCAEvent_PCIComponentError.RecordId
- MSMCAEvent_PCIComponentError.Size
- MSMCAEvent_PCIComponentError.Type
- MSMCAEvent_PCIComponentError.VALIDATION_BITS
- MSMCAEvent_PCIComponentError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cbcf3ee13e822fd59cdcdd30538d5e369d798aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765194"
---
# <a name="msmcaevent_pcicomponenterror-class"></a><span data-ttu-id="066e3-104">\_Classe MSMCAEvent PCIComponentError</span><span class="sxs-lookup"><span data-stu-id="066e3-104">MSMCAEvent\_PCIComponentError class</span></span>

<span data-ttu-id="066e3-105">A classe **MSMCAEvent \_ PCIComponentError** indica um erro de componente de PCI MCA (arquitetura de verificação de máquina).</span><span class="sxs-lookup"><span data-stu-id="066e3-105">The **MSMCAEvent\_PCIComponentError** class indicates an Machine Check Architecture (MCA) PCI component error.</span></span> <span data-ttu-id="066e3-106">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="066e3-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="066e3-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="066e3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="066e3-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="066e3-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="066e3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="066e3-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PCIComponentError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_COMP_ERROR_STATUS;
  uint8   PCI_COMP_INFO_BusNumber;
  uint8   PCI_COMP_INFO_ClassCodeBaseClass;
  uint8   PCI_COMP_INFO_ClassCodeInterface;
  uint8   PCI_COMP_INFO_ClassCodeSubClass;
  uint16  PCI_COMP_INFO_DeviceId;
  uint8   PCI_COMP_INFO_DeviceNumber;
  uint8   PCI_COMP_INFO_FunctionNumber;
  uint8   PCI_COMP_INFO_SegmentNumber;
  uint16  PCI_COMP_INFO_VendorId;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="066e3-110">Membros</span><span class="sxs-lookup"><span data-stu-id="066e3-110">Members</span></span>

<span data-ttu-id="066e3-111">A classe **MSMCAEvent \_ PCIComponentError** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="066e3-111">The **MSMCAEvent\_PCIComponentError** class has these types of members:</span></span>

-   [<span data-ttu-id="066e3-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="066e3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="066e3-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="066e3-113">Properties</span></span>

<span data-ttu-id="066e3-114">A classe **MSMCAEvent \_ PCIComponentError** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="066e3-114">The **MSMCAEvent\_PCIComponentError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="066e3-115">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="066e3-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="066e3-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-118">**True**, se esta instância da classe estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="066e3-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="066e3-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="066e3-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-122">Número de erros adicionais no registro.</span><span class="sxs-lookup"><span data-stu-id="066e3-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-123">**CPUs**</span><span class="sxs-lookup"><span data-stu-id="066e3-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="066e3-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-126">CPU que relatou o erro.</span><span class="sxs-lookup"><span data-stu-id="066e3-126">CPU that reported the error.</span></span> <span data-ttu-id="066e3-127">Essa propriedade se aplica somente a um sistema multiprocessador no qual o primeiro processador recebe o número 0, o segundo processador recebe o número 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="066e3-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="066e3-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-129">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="066e3-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-131">Nível de severidade do erro relatado.</span><span class="sxs-lookup"><span data-stu-id="066e3-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="066e3-132">Valor</span><span class="sxs-lookup"><span data-stu-id="066e3-132">Value</span></span>                                                                                                | <span data-ttu-id="066e3-133">Significado</span><span class="sxs-lookup"><span data-stu-id="066e3-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="066e3-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="066e3-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="066e3-135">Recuperado</span><span class="sxs-lookup"><span data-stu-id="066e3-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="066e3-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="066e3-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="066e3-137">Fatais</span><span class="sxs-lookup"><span data-stu-id="066e3-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="066e3-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="066e3-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="066e3-139">Corrigível</span><span class="sxs-lookup"><span data-stu-id="066e3-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="066e3-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="066e3-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="066e3-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="066e3-143">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="066e3-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="066e3-144">Identificador exclusivo desta instância da classe.</span><span class="sxs-lookup"><span data-stu-id="066e3-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="066e3-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="066e3-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-148">Se for 0 (zero), esse evento não será registrado no log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="066e3-148">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-149">**\_status de \_ erro de comp de PCI \_**</span><span class="sxs-lookup"><span data-stu-id="066e3-149">**PCI\_COMP\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-150">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="066e3-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-152">Código de erro interno.</span><span class="sxs-lookup"><span data-stu-id="066e3-152">Internal error code.</span></span>

<span data-ttu-id="066e3-153">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="066e3-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="066e3-154">**Informações de comp de PCI \_ \_ \_ BusNumber**</span><span class="sxs-lookup"><span data-stu-id="066e3-154">**PCI\_COMP\_INFO\_BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-155">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="066e3-155">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-157">Número de barramento do componente PCI.</span><span class="sxs-lookup"><span data-stu-id="066e3-157">Bus number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-158">**Informações de comp de PCI \_ \_ \_ ClassCodeBaseClass**</span><span class="sxs-lookup"><span data-stu-id="066e3-158">**PCI\_COMP\_INFO\_ClassCodeBaseClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-159">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="066e3-159">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-161">Código de classe da classe base do componente PCI.</span><span class="sxs-lookup"><span data-stu-id="066e3-161">Class code of the base class of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-162">**Informações de comp de PCI \_ \_ \_ ClassCodeInterface**</span><span class="sxs-lookup"><span data-stu-id="066e3-162">**PCI\_COMP\_INFO\_ClassCodeInterface**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-163">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="066e3-163">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-165">Interface de código de classe do componente PCI.</span><span class="sxs-lookup"><span data-stu-id="066e3-165">Class code interface of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-166">**Informações de comp de PCI \_ \_ \_ ClassCodeSubClass**</span><span class="sxs-lookup"><span data-stu-id="066e3-166">**PCI\_COMP\_INFO\_ClassCodeSubClass**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-167">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="066e3-167">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-169">Subclasse de código de classe do componente PCI.</span><span class="sxs-lookup"><span data-stu-id="066e3-169">Class code subclass of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-170">**\_Dispositivo de \_ informações de comp de PCI \_**</span><span class="sxs-lookup"><span data-stu-id="066e3-170">**PCI\_COMP\_INFO\_DeviceId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-171">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="066e3-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-173">Identificador de dispositivo do componente PCI.</span><span class="sxs-lookup"><span data-stu-id="066e3-173">Device identifier of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-174">**Informações de comp de PCI \_ \_ \_ DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="066e3-174">**PCI\_COMP\_INFO\_DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-175">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="066e3-175">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-177">Número do dispositivo do componente PCI.</span><span class="sxs-lookup"><span data-stu-id="066e3-177">Device number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-178">**Informações de comp de PCI \_ \_ \_ FunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="066e3-178">**PCI\_COMP\_INFO\_FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-179">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="066e3-179">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-181">Número da função do componente PCI.</span><span class="sxs-lookup"><span data-stu-id="066e3-181">Function number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-182">**Informações de comp de PCI \_ \_ \_ SegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="066e3-182">**PCI\_COMP\_INFO\_SegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-183">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="066e3-183">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-185">Número de segmento do componente PCI.</span><span class="sxs-lookup"><span data-stu-id="066e3-185">Segment number of the PCI component.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-186">**Informações de comp de PCI do \_ \_ \_ fornecedor**</span><span class="sxs-lookup"><span data-stu-id="066e3-186">**PCI\_COMP\_INFO\_VendorId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-187">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="066e3-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-188">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-189">Identificador de fornecedor do componente PCI.</span><span class="sxs-lookup"><span data-stu-id="066e3-189">Vendor identifier of the PCI Component.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-190">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="066e3-190">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-191">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="066e3-191">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="066e3-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-193">Matriz de bytes que contém o registro de erro bruto.</span><span class="sxs-lookup"><span data-stu-id="066e3-193">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="066e3-194">O número de elementos na matriz que a propriedade **size** especifica.</span><span class="sxs-lookup"><span data-stu-id="066e3-194">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-195">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="066e3-195">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-196">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="066e3-196">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-198">Identificador de registro do registro de erro para este erro.</span><span class="sxs-lookup"><span data-stu-id="066e3-198">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="066e3-199">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="066e3-199">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="066e3-200">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="066e3-200">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-201">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="066e3-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-203">Tamanho do registro de erro bruto.</span><span class="sxs-lookup"><span data-stu-id="066e3-203">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-204">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="066e3-204">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-205">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="066e3-205">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-207">Tipo de mensagem de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="066e3-207">Type of event log message.</span></span> <span data-ttu-id="066e3-208">Essas mensagens correspondem aos códigos de mensagem de log de eventos usados para inserir mensagens de log de eventos pelo provedor de consumidor do log de eventos do Windows quando ele recebe um dos eventos.</span><span class="sxs-lookup"><span data-stu-id="066e3-208">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="066e3-209">**BITS de validação \_**</span><span class="sxs-lookup"><span data-stu-id="066e3-209">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="066e3-210">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="066e3-210">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="066e3-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="066e3-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="066e3-212">Bits de validação usados para indicar a validade dos campos subsequentes.</span><span class="sxs-lookup"><span data-stu-id="066e3-212">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="066e3-213">Valores</span><span class="sxs-lookup"><span data-stu-id="066e3-213">Values</span></span>                                                                               | <span data-ttu-id="066e3-214">Significado</span><span class="sxs-lookup"><span data-stu-id="066e3-214">Meaning</span></span>                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="066e3-215"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="066e3-215"><dt>1 (0x1)</dt></span></span> </dl>   | <span data-ttu-id="066e3-216">O \_ status de erro de comp de PCI \_ \_ é válido.</span><span class="sxs-lookup"><span data-stu-id="066e3-216">PCI\_COMP\_ERROR\_STATUS is valid.</span></span><br/>    |
| <dl> <span data-ttu-id="066e3-217"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="066e3-217"><dt>2 (0x2)</dt></span></span> </dl>   | <span data-ttu-id="066e3-218">As \_ informações de comp de PCI \_ são válidas.</span><span class="sxs-lookup"><span data-stu-id="066e3-218">PCI\_COMP\_INFO is valid.</span></span><br/>             |
| <dl> <span data-ttu-id="066e3-219"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="066e3-219"><dt>4 (0x4)</dt></span></span> </dl>   | <span data-ttu-id="066e3-220">O \_ número de memória do PCI comp \_ \_ é válido.</span><span class="sxs-lookup"><span data-stu-id="066e3-220">PCI\_COMP\_MEM\_NUM is valid.</span></span><br/>         |
| <dl> <span data-ttu-id="066e3-221"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="066e3-221"><dt>8 (0x8)</dt></span></span> </dl>   | <span data-ttu-id="066e3-222">O \_ número de e/s de comp de PCI \_ \_ é válido.</span><span class="sxs-lookup"><span data-stu-id="066e3-222">PCI\_COMP\_IO\_NUM is valid.</span></span><br/>          |
| <dl> <span data-ttu-id="066e3-223"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="066e3-223"><dt>16 (0x10)</dt></span></span> </dl> | <span data-ttu-id="066e3-224">O \_ par de dados regs de PCI comp \_ \_ \_ é válido.</span><span class="sxs-lookup"><span data-stu-id="066e3-224">PCI\_COMP\_REGS\_DATA\_PAIR is valid.</span></span><br/> |



 

<span data-ttu-id="066e3-225">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="066e3-225">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="066e3-226">Comentários</span><span class="sxs-lookup"><span data-stu-id="066e3-226">Remarks</span></span>

<span data-ttu-id="066e3-227">A classe **MSMCAEvent \_ PCIComponentError** é derivada de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="066e3-227">The **MSMCAEvent\_PCIComponentError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="066e3-228">Requisitos</span><span class="sxs-lookup"><span data-stu-id="066e3-228">Requirements</span></span>



| <span data-ttu-id="066e3-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="066e3-229">Requirement</span></span> | <span data-ttu-id="066e3-230">Valor</span><span class="sxs-lookup"><span data-stu-id="066e3-230">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="066e3-231">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="066e3-231">Minimum supported client</span></span><br/> | <span data-ttu-id="066e3-232">Windows XP</span><span class="sxs-lookup"><span data-stu-id="066e3-232">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="066e3-233">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="066e3-233">Minimum supported server</span></span><br/> | <span data-ttu-id="066e3-234">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="066e3-234">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="066e3-235">Namespace</span><span class="sxs-lookup"><span data-stu-id="066e3-235">Namespace</span></span><br/>                | <span data-ttu-id="066e3-236">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="066e3-236">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="066e3-237">MOF</span><span class="sxs-lookup"><span data-stu-id="066e3-237">MOF</span></span><br/>                      | <dl> <span data-ttu-id="066e3-238"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="066e3-238"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="066e3-239">DLL</span><span class="sxs-lookup"><span data-stu-id="066e3-239">DLL</span></span><br/>                      | <dl> <span data-ttu-id="066e3-240"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="066e3-240"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="066e3-241">Confira também</span><span class="sxs-lookup"><span data-stu-id="066e3-241">See also</span></span>

<dl> <dt>

[<span data-ttu-id="066e3-242">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="066e3-242">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="066e3-243">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="066e3-243">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

