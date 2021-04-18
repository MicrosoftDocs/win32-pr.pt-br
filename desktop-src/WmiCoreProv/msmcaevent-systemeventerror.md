---
description: Indica que ocorreu um evento de sistema de interface de gerenciamento de plataforma inteligente (IPMI). O erro é gravado no SEL (log de eventos do sistema) do SMBIOS. Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: 1964f850-ac55-4639-9205-2eb0996dbaae
title: Classe MSMCAEvent_SystemEventError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SystemEventError
- MSMCAEvent_SystemEventError.Active
- MSMCAEvent_SystemEventError.AdditionalErrors
- MSMCAEvent_SystemEventError.Cpu
- MSMCAEvent_SystemEventError.ErrorSeverity
- MSMCAEvent_SystemEventError.InstanceName
- MSMCAEvent_SystemEventError.RawRecord
- MSMCAEvent_SystemEventError.RecordId
- MSMCAEvent_SystemEventError.SEL_DATA1
- MSMCAEvent_SystemEventError.SEL_DATA2
- MSMCAEvent_SystemEventError.SEL_DATA3
- MSMCAEvent_SystemEventError.SEL_EVENT_DIR_TYPE
- MSMCAEvent_SystemEventError.SEL_EVM_REV
- MSMCAEvent_SystemEventError.SEL_GENERATOR_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_ID
- MSMCAEvent_SystemEventError.SEL_RECORD_TYPE
- MSMCAEvent_SystemEventError.SEL_SENSOR_NUM
- MSMCAEvent_SystemEventError.SEL_SENSOR_TYPE
- MSMCAEvent_SystemEventError.SEL_TIME_STAMP
- MSMCAEvent_SystemEventError.Size
- MSMCAEvent_SystemEventError.Type
- MSMCAEvent_SystemEventError.VALIDATION_BITS
- MSMCAEvent_SystemEventError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f20f95fb5e1b1bf07b0f70c25d54122642b13569
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749719"
---
# <a name="msmcaevent_systemeventerror-class"></a><span data-ttu-id="16d14-105">\_Classe MSMCAEvent SystemEventError</span><span class="sxs-lookup"><span data-stu-id="16d14-105">MSMCAEvent\_SystemEventError class</span></span>

<span data-ttu-id="16d14-106">A classe **MSMCAEvent \_ SystemEventError** indica que ocorreu um evento de sistema de interface de gerenciamento de plataforma inteligente (IPMI).</span><span class="sxs-lookup"><span data-stu-id="16d14-106">The **MSMCAEvent\_SystemEventError** class indicates that an Intelligent Platform Management Interface (IPMI) system event has occurred.</span></span> <span data-ttu-id="16d14-107">O erro é gravado no SEL (log de eventos do sistema) do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="16d14-107">The error is written to the SMBIOS System Event Log (SEL).</span></span> <span data-ttu-id="16d14-108">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="16d14-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="16d14-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="16d14-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="16d14-110">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="16d14-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="16d14-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="16d14-111">Syntax</span></span>

``` syntax
class MSMCAEvent_SystemEventError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint8   SEL_DATA1;
  uint8   SEL_DATA2;
  uint8   SEL_DATA3;
  uint8   SEL_EVENT_DIR_TYPE;
  uint8   SEL_EVM_REV;
  uint16  SEL_GENERATOR_ID;
  uint16  SEL_RECORD_ID;
  uint8   SEL_RECORD_TYPE;
  uint8   SEL_SENSOR_NUM;
  uint8   SEL_SENSOR_TYPE;
  uint64  SEL_TIME_STAMP;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="16d14-112">Membros</span><span class="sxs-lookup"><span data-stu-id="16d14-112">Members</span></span>

<span data-ttu-id="16d14-113">A classe **MSMCAEvent \_ SystemEventError** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="16d14-113">The **MSMCAEvent\_SystemEventError** class has these types of members:</span></span>

-   [<span data-ttu-id="16d14-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="16d14-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="16d14-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="16d14-115">Properties</span></span>

<span data-ttu-id="16d14-116">A classe **MSMCAEvent \_ SystemEventError** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="16d14-116">The **MSMCAEvent\_SystemEventError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="16d14-117">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="16d14-117">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-118">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="16d14-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-120">**True**, se esta instância da classe estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="16d14-120">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-121">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="16d14-121">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-122">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16d14-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-124">Número de erros adicionais no registro.</span><span class="sxs-lookup"><span data-stu-id="16d14-124">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-125">**CPUs**</span><span class="sxs-lookup"><span data-stu-id="16d14-125">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-126">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16d14-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-128">CPU que relatou o erro.</span><span class="sxs-lookup"><span data-stu-id="16d14-128">CPU that reported the error.</span></span> <span data-ttu-id="16d14-129">Essa propriedade se aplica somente a um sistema multiprocessador no qual o primeiro processador recebe o número 0, o segundo processador recebe o número 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="16d14-129">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-130">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="16d14-130">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-131">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="16d14-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-133">Nível de severidade do erro relatado.</span><span class="sxs-lookup"><span data-stu-id="16d14-133">Severity level of the error reported.</span></span>



| <span data-ttu-id="16d14-134">Valor</span><span class="sxs-lookup"><span data-stu-id="16d14-134">Value</span></span>                                                                                                | <span data-ttu-id="16d14-135">Significado</span><span class="sxs-lookup"><span data-stu-id="16d14-135">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="16d14-136"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-136"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="16d14-137">Recuperado</span><span class="sxs-lookup"><span data-stu-id="16d14-137">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="16d14-138"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-138"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="16d14-139">Fatais</span><span class="sxs-lookup"><span data-stu-id="16d14-139">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="16d14-140"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-140"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="16d14-141">Corrigível</span><span class="sxs-lookup"><span data-stu-id="16d14-141">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="16d14-142">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="16d14-142">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="16d14-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="16d14-145">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="16d14-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="16d14-146">Identificador exclusivo desta instância da classe.</span><span class="sxs-lookup"><span data-stu-id="16d14-146">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-147">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="16d14-147">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-148">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16d14-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-150">Se for 0 (zero), esse evento não será registrado no log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="16d14-150">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-151">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="16d14-151">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-152">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="16d14-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="16d14-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-154">Matriz de bytes que contém o registro de erro bruto.</span><span class="sxs-lookup"><span data-stu-id="16d14-154">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="16d14-155">O número de elementos na matriz que a propriedade **size** especifica.</span><span class="sxs-lookup"><span data-stu-id="16d14-155">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-156">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="16d14-156">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-157">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="16d14-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-159">Identificador de registro do registro de erro para este erro.</span><span class="sxs-lookup"><span data-stu-id="16d14-159">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="16d14-160">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="16d14-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="16d14-161">**Data1 de SEL \_**</span><span class="sxs-lookup"><span data-stu-id="16d14-161">**SEL\_DATA1**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-162">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="16d14-162">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-164">Campo de dados de evento 1.</span><span class="sxs-lookup"><span data-stu-id="16d14-164">Event data field 1.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-165">**Data2 do SEL \_**</span><span class="sxs-lookup"><span data-stu-id="16d14-165">**SEL\_DATA2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-166">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="16d14-166">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-168">Campo de dados de evento 2.</span><span class="sxs-lookup"><span data-stu-id="16d14-168">Event data field 2.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-169">**SEL \_ DATA3**</span><span class="sxs-lookup"><span data-stu-id="16d14-169">**SEL\_DATA3**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-170">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="16d14-170">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-172">Campo de dados de evento 3.</span><span class="sxs-lookup"><span data-stu-id="16d14-172">Event data field 3.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-173">**tipo de dir. de \_ evento Sel \_ \_**</span><span class="sxs-lookup"><span data-stu-id="16d14-173">**SEL\_EVENT\_DIR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-174">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="16d14-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-176">Tipo de diretório de evento.</span><span class="sxs-lookup"><span data-stu-id="16d14-176">Event directory type.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-177">**SEL \_ EVM \_ Rev**</span><span class="sxs-lookup"><span data-stu-id="16d14-177">**SEL\_EVM\_REV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-178">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="16d14-178">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-180">Versão de formato da mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="16d14-180">Format version of the error message.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-181">**\_ID do gerador de Sel \_**</span><span class="sxs-lookup"><span data-stu-id="16d14-181">**SEL\_GENERATOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-182">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16d14-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-184">Identificador de software, se o evento foi gerado pelo software.</span><span class="sxs-lookup"><span data-stu-id="16d14-184">Software identifier, if the event was software-generated.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-185">**\_ID do registro de Sel \_**</span><span class="sxs-lookup"><span data-stu-id="16d14-185">**SEL\_RECORD\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-186">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="16d14-186">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-188">Identificador de registro usado para acesso ao registro de eventos do sistema (SEL) do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="16d14-188">Record identifier used for SMBIOS system event log (SEL) access.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-189">**\_tipo de registro de Sel \_**</span><span class="sxs-lookup"><span data-stu-id="16d14-189">**SEL\_RECORD\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-190">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="16d14-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-192">Tipo de registro.</span><span class="sxs-lookup"><span data-stu-id="16d14-192">Record type.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-193">**\_número do sensor Sel \_**</span><span class="sxs-lookup"><span data-stu-id="16d14-193">**SEL\_SENSOR\_NUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-194">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="16d14-194">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-195">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-195">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-196">Número do sensor que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="16d14-196">Sensor number that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-197">**\_tipo de sensor Sel \_**</span><span class="sxs-lookup"><span data-stu-id="16d14-197">**SEL\_SENSOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-198">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="16d14-198">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-200">O código do tipo de sensor do sensor que gerou o evento.</span><span class="sxs-lookup"><span data-stu-id="16d14-200">Sensor type code of the sensor that generated the event.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-201">**carimbo de data/hora do SEL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="16d14-201">**SEL\_TIME\_STAMP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-202">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="16d14-202">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-204">Carimbo de data/hora do log de eventos.</span><span class="sxs-lookup"><span data-stu-id="16d14-204">Timestamp of the event log.</span></span>

<span data-ttu-id="16d14-205">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="16d14-205">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="16d14-206">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="16d14-206">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-207">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16d14-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-208">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-209">Tamanho do registro de erro bruto.</span><span class="sxs-lookup"><span data-stu-id="16d14-209">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-210">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="16d14-210">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-211">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16d14-211">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-213">Tipo de mensagem de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="16d14-213">Type of event log message.</span></span> <span data-ttu-id="16d14-214">Essas mensagens correspondem aos códigos de mensagem de log de eventos usados para inserir mensagens de log de eventos pelo provedor de consumidor do log de eventos do Windows quando ele recebe um dos eventos.</span><span class="sxs-lookup"><span data-stu-id="16d14-214">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="16d14-215">**BITS de validação \_**</span><span class="sxs-lookup"><span data-stu-id="16d14-215">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16d14-216">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="16d14-216">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="16d14-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="16d14-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="16d14-218">Bits de validação usados para indicar a validade dos campos subsequentes.</span><span class="sxs-lookup"><span data-stu-id="16d14-218">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="16d14-219">Valor</span><span class="sxs-lookup"><span data-stu-id="16d14-219">Value</span></span>                                                                                                                                            | <span data-ttu-id="16d14-220">Significado</span><span class="sxs-lookup"><span data-stu-id="16d14-220">Meaning</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <span data-ttu-id="16d14-221"><dt>**1 0x1**</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-221"><dt>**1 0x1**</dt></span></span> </dl>             | <span data-ttu-id="16d14-222">**Sel \_ A \_ ID do registro** é válida.</span><span class="sxs-lookup"><span data-stu-id="16d14-222">**SEL\_RECORD\_ID** is valid.</span></span><br/>    |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <span data-ttu-id="16d14-223"><dt>**2 0x2**</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-223"><dt>**2 0x2**</dt></span></span> </dl>             | <span data-ttu-id="16d14-224">**Sel \_ O \_ tipo de registro** é válido.</span><span class="sxs-lookup"><span data-stu-id="16d14-224">**SEL\_RECORD\_TYPE** is valid.</span></span><br/>  |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <span data-ttu-id="16d14-225"><dt>**4 0x4**</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-225"><dt>**4 0x4**</dt></span></span> </dl>             | <span data-ttu-id="16d14-226">**Sel \_ A \_ ID do gerador** é válida.</span><span class="sxs-lookup"><span data-stu-id="16d14-226">**SEL\_GENERATOR\_ID** is valid.</span></span><br/> |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <span data-ttu-id="16d14-227"><dt>**8 0x8**</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-227"><dt>**8 0x8**</dt></span></span> </dl>             | <span data-ttu-id="16d14-228">**Sel \_ EVM \_ Rev** é válido.</span><span class="sxs-lookup"><span data-stu-id="16d14-228">**SEL\_EVM\_REV** is valid.</span></span><br/>      |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <span data-ttu-id="16d14-229"><dt>**16 0x10**</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-229"><dt>**16 0x10**</dt></span></span> </dl>       | <span data-ttu-id="16d14-230">**Sel \_ O \_ tipo de sensor** é válido.</span><span class="sxs-lookup"><span data-stu-id="16d14-230">**SEL\_SENSOR\_TYPE** is valid.</span></span><br/>  |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <span data-ttu-id="16d14-231"><dt>**32 0x20**</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-231"><dt>**32 0x20**</dt></span></span> </dl>       | <span data-ttu-id="16d14-232">**Sel \_ O \_ número do sensor** é válido.</span><span class="sxs-lookup"><span data-stu-id="16d14-232">**SEL\_SENSOR\_NUM** is valid.</span></span><br/>   |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <span data-ttu-id="16d14-233"><dt>**64 0x40**</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-233"><dt>**64 0x40**</dt></span></span> </dl>       | <span data-ttu-id="16d14-234">**Sel \_ O \_ diretório do evento** é válido.</span><span class="sxs-lookup"><span data-stu-id="16d14-234">**SEL\_EVENT\_DIR** is valid.</span></span><br/>    |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <span data-ttu-id="16d14-235"><dt>**128 0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-235"><dt>**128 0x80**</dt></span></span> </dl>    | <span data-ttu-id="16d14-236">**Sel \_ O evento \_ dados1** é válido.</span><span class="sxs-lookup"><span data-stu-id="16d14-236">**SEL\_EVENT\_DATA1** is valid.</span></span><br/>  |
| <span id="256_0x100"></span><span id="256_0X100"></span><dl> <span data-ttu-id="16d14-237"><dt>**256 0x100**</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-237"><dt>**256 0x100**</dt></span></span> </dl> | <span data-ttu-id="16d14-238">**Sel \_ O \_ data2 do evento** é válido.</span><span class="sxs-lookup"><span data-stu-id="16d14-238">**SEL\_EVENT\_DATA2** is valid.</span></span><br/>  |
| <span id="512_0x200"></span><span id="512_0X200"></span><dl> <span data-ttu-id="16d14-239"><dt>**512 0x200**</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-239"><dt>**512 0x200**</dt></span></span> </dl> | <span data-ttu-id="16d14-240">**Sel \_ O \_ DATA3 do evento** é válido.</span><span class="sxs-lookup"><span data-stu-id="16d14-240">**SEL\_EVENT\_DATA3** is valid.</span></span><br/>  |



 

<span data-ttu-id="16d14-241">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="16d14-241">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16d14-242">Comentários</span><span class="sxs-lookup"><span data-stu-id="16d14-242">Remarks</span></span>

<span data-ttu-id="16d14-243">A classe **MSMCAEvent \_ SystemEventError** é derivada de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="16d14-243">The **MSMCAEvent\_SystemEventError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16d14-244">Requisitos</span><span class="sxs-lookup"><span data-stu-id="16d14-244">Requirements</span></span>



| <span data-ttu-id="16d14-245">Requisito</span><span class="sxs-lookup"><span data-stu-id="16d14-245">Requirement</span></span> | <span data-ttu-id="16d14-246">Valor</span><span class="sxs-lookup"><span data-stu-id="16d14-246">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="16d14-247">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16d14-247">Minimum supported client</span></span><br/> | <span data-ttu-id="16d14-248">Windows XP</span><span class="sxs-lookup"><span data-stu-id="16d14-248">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="16d14-249">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="16d14-249">Minimum supported server</span></span><br/> | <span data-ttu-id="16d14-250">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="16d14-250">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="16d14-251">Namespace</span><span class="sxs-lookup"><span data-stu-id="16d14-251">Namespace</span></span><br/>                | <span data-ttu-id="16d14-252">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="16d14-252">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="16d14-253">MOF</span><span class="sxs-lookup"><span data-stu-id="16d14-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16d14-254"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-254"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="16d14-255">DLL</span><span class="sxs-lookup"><span data-stu-id="16d14-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16d14-256"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16d14-256"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16d14-257">Confira também</span><span class="sxs-lookup"><span data-stu-id="16d14-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16d14-258">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="16d14-258">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="16d14-259">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="16d14-259">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

