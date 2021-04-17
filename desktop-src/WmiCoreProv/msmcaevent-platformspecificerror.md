---
description: Indica um erro específico da plataforma MCA (arquitetura de verificação de máquina). Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: 409641d5-3451-4d26-88d1-bfd0e55db257
title: Classe MSMCAEvent_PlatformSpecificError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PlatformSpecificError
- MSMCAEvent_PlatformSpecificError.Active
- MSMCAEvent_PlatformSpecificError.AdditionalErrors
- MSMCAEvent_PlatformSpecificError.Cpu
- MSMCAEvent_PlatformSpecificError.ErrorSeverity
- MSMCAEvent_PlatformSpecificError.InstanceName
- MSMCAEvent_PlatformSpecificError.OEM_COMPONENT_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_BUS_SPECIFIC_DATA
- MSMCAEvent_PlatformSpecificError.PLATFORM_ERROR_STATUS
- MSMCAEvent_PlatformSpecificError.PLATFORM_REQUESTOR_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_RESPONDER_ID
- MSMCAEvent_PlatformSpecificError.PLATFORM_TARGET_ID
- MSMCAEvent_PlatformSpecificError.RawRecord
- MSMCAEvent_PlatformSpecificError.RecordId
- MSMCAEvent_PlatformSpecificError.Size
- MSMCAEvent_PlatformSpecificError.Type
- MSMCAEvent_PlatformSpecificError.VALIDATION_BITS
- MSMCAEvent_PlatformSpecificError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 51993c8c41206dac8f4c944d24fa59ae7b689f92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461107"
---
# <a name="msmcaevent_platformspecificerror-class"></a><span data-ttu-id="e4d19-104">\_Classe MSMCAEvent PlatformSpecificError</span><span class="sxs-lookup"><span data-stu-id="e4d19-104">MSMCAEvent\_PlatformSpecificError class</span></span>

<span data-ttu-id="e4d19-105">A classe **MSMCAEvent \_ PlatformSpecificError** indica um erro específico da plataforma MCA (arquitetura de verificação de máquina).</span><span class="sxs-lookup"><span data-stu-id="e4d19-105">The **MSMCAEvent\_PlatformSpecificError** class indicates a Machine Check Architecture (MCA) platform-specific error.</span></span> <span data-ttu-id="e4d19-106">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="e4d19-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="e4d19-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e4d19-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e4d19-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="e4d19-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4d19-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4d19-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PlatformSpecificError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   OEM_COMPONENT_ID;
  uint64  PLATFORM_BUS_SPECIFIC_DATA;
  uint64  PLATFORM_ERROR_STATUS;
  uint64  PLATFORM_REQUESTOR_ID;
  uint64  PLATFORM_RESPONDER_ID;
  uint64  PLATFORM_TARGET_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="e4d19-110">Membros</span><span class="sxs-lookup"><span data-stu-id="e4d19-110">Members</span></span>

<span data-ttu-id="e4d19-111">A classe **MSMCAEvent \_ PlatformSpecificError** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e4d19-111">The **MSMCAEvent\_PlatformSpecificError** class has these types of members:</span></span>

-   [<span data-ttu-id="e4d19-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e4d19-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4d19-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e4d19-113">Properties</span></span>

<span data-ttu-id="e4d19-114">A classe **MSMCAEvent \_ PlatformSpecificError** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e4d19-114">The **MSMCAEvent\_PlatformSpecificError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e4d19-115">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="e4d19-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="e4d19-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-118">**True**, se esta instância da classe estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="e4d19-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="e4d19-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4d19-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-122">Número de erros adicionais no registro.</span><span class="sxs-lookup"><span data-stu-id="e4d19-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-123">**CPUs**</span><span class="sxs-lookup"><span data-stu-id="e4d19-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4d19-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-126">CPU que relatou o erro.</span><span class="sxs-lookup"><span data-stu-id="e4d19-126">CPU that reported the error.</span></span> <span data-ttu-id="e4d19-127">Essa propriedade se aplica somente a um sistema multiprocessador no qual o primeiro processador recebe o número 0, o segundo processador recebe o número 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e4d19-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="e4d19-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-129">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="e4d19-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-131">Nível de severidade do erro relatado.</span><span class="sxs-lookup"><span data-stu-id="e4d19-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="e4d19-132">Valor</span><span class="sxs-lookup"><span data-stu-id="e4d19-132">Value</span></span>                                                                                                | <span data-ttu-id="e4d19-133">Significado</span><span class="sxs-lookup"><span data-stu-id="e4d19-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="e4d19-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d19-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="e4d19-135">Recuperado</span><span class="sxs-lookup"><span data-stu-id="e4d19-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="e4d19-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d19-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="e4d19-137">Fatais</span><span class="sxs-lookup"><span data-stu-id="e4d19-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="e4d19-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d19-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="e4d19-139">Corrigível</span><span class="sxs-lookup"><span data-stu-id="e4d19-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e4d19-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="e4d19-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e4d19-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-143">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e4d19-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-144">Identificador exclusivo desta instância da classe.</span><span class="sxs-lookup"><span data-stu-id="e4d19-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="e4d19-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4d19-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-148">Se for 0 (zero), esse evento não será registrado no log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="e4d19-148">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-149">**\_ID do componente OEM \_**</span><span class="sxs-lookup"><span data-stu-id="e4d19-149">**OEM\_COMPONENT\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-150">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="e4d19-150">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-152">Identificador exclusivo do componente que relata o erro.</span><span class="sxs-lookup"><span data-stu-id="e4d19-152">Unique identifier of the component that reports the error.</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-153">**\_ \_ dados específicos do barramento de plataforma \_**</span><span class="sxs-lookup"><span data-stu-id="e4d19-153">**PLATFORM\_BUS\_SPECIFIC\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-154">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4d19-154">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-156">Dados dependentes de barramento específicos do OEM.</span><span class="sxs-lookup"><span data-stu-id="e4d19-156">OEM-specific, bus-dependent data.</span></span>

<span data-ttu-id="e4d19-157">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4d19-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-158">**\_status de erro da plataforma \_**</span><span class="sxs-lookup"><span data-stu-id="e4d19-158">**PLATFORM\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-159">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4d19-159">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-161">Status de erro de plataforma genérica.</span><span class="sxs-lookup"><span data-stu-id="e4d19-161">Generic platform error status.</span></span>

<span data-ttu-id="e4d19-162">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4d19-162">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-163">**\_ID do solicitante de plataforma \_**</span><span class="sxs-lookup"><span data-stu-id="e4d19-163">**PLATFORM\_REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-164">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4d19-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-166">Identificador do solicitante no momento do evento.</span><span class="sxs-lookup"><span data-stu-id="e4d19-166">Requestor identifier at the time of the event.</span></span>

<span data-ttu-id="e4d19-167">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4d19-167">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-168">**\_ID do Respondente da plataforma \_**</span><span class="sxs-lookup"><span data-stu-id="e4d19-168">**PLATFORM\_RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-169">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4d19-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-171">Identificador do Respondente no momento do evento.</span><span class="sxs-lookup"><span data-stu-id="e4d19-171">Responder identifier at the time of the event.</span></span>

<span data-ttu-id="e4d19-172">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4d19-172">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-173">**\_ID de destino da plataforma \_**</span><span class="sxs-lookup"><span data-stu-id="e4d19-173">**PLATFORM\_TARGET\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-174">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4d19-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-176">Identificador de destino no momento do evento.</span><span class="sxs-lookup"><span data-stu-id="e4d19-176">Target identifier at the time of the event.</span></span>

<span data-ttu-id="e4d19-177">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4d19-177">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-178">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="e4d19-178">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-179">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="e4d19-179">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-180">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-181">Matriz de bytes que contém o registro de erro bruto conforme apresentado ao Windows pela camada de abstração do sistema (SAL).</span><span class="sxs-lookup"><span data-stu-id="e4d19-181">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="e4d19-182">O número de elementos na matriz é especificado pela propriedade **size** .</span><span class="sxs-lookup"><span data-stu-id="e4d19-182">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-183">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="e4d19-183">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-184">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4d19-184">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-186">Identificador de registro do registro de erro para este erro.</span><span class="sxs-lookup"><span data-stu-id="e4d19-186">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="e4d19-187">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4d19-187">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-188">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="e4d19-188">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-189">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4d19-189">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-191">Tamanho do registro de erro bruto.</span><span class="sxs-lookup"><span data-stu-id="e4d19-191">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-192">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="e4d19-192">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-193">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4d19-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-195">Tipo de mensagem de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="e4d19-195">Type of event log message.</span></span> <span data-ttu-id="e4d19-196">Essas mensagens correspondem aos códigos de mensagem de log de eventos usados para inserir mensagens de log de eventos pelo provedor de consumidor do log de eventos do Windows quando ele recebe um dos eventos.</span><span class="sxs-lookup"><span data-stu-id="e4d19-196">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="e4d19-197">**BITS de validação \_**</span><span class="sxs-lookup"><span data-stu-id="e4d19-197">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4d19-198">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="e4d19-198">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="e4d19-199">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e4d19-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e4d19-200">Bits de validação usados para indicar a validade dos campos subsequentes.</span><span class="sxs-lookup"><span data-stu-id="e4d19-200">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="e4d19-201">Valor</span><span class="sxs-lookup"><span data-stu-id="e4d19-201">Value</span></span>                                                                                                                                         | <span data-ttu-id="e4d19-202">Significado</span><span class="sxs-lookup"><span data-stu-id="e4d19-202">Meaning</span></span>                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="1_0x1"></span><span id="1_0X1"></span><dl> <span data-ttu-id="e4d19-203"><dt>**1 0x1**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d19-203"><dt>**1 0x1**</dt></span></span> </dl>          | <span data-ttu-id="e4d19-204">**Plataforma \_ do O \_ status do erro** é válido.</span><span class="sxs-lookup"><span data-stu-id="e4d19-204">**PLATFORM\_ERROR\_STATUS** is valid.</span></span><br/>            |
| <span id="2_0x2"></span><span id="2_0X2"></span><dl> <span data-ttu-id="e4d19-205"><dt>**2 0x2**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d19-205"><dt>**2 0x2**</dt></span></span> </dl>          | <span data-ttu-id="e4d19-206">**Plataforma \_ do A \_ \_ ID do solicitante de erro** é válida.</span><span class="sxs-lookup"><span data-stu-id="e4d19-206">**PLATFORM\_ERROR\_REQUESTOR\_ID** is valid.</span></span><br/>     |
| <span id="4_0x4"></span><span id="4_0X4"></span><dl> <span data-ttu-id="e4d19-207"><dt>**4 0x4**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d19-207"><dt>**4 0x4**</dt></span></span> </dl>          | <span data-ttu-id="e4d19-208">**Plataforma \_ do A \_ \_ ID do Respondente de erro** é válida.</span><span class="sxs-lookup"><span data-stu-id="e4d19-208">**PLATFORM\_ERROR\_RESPONDER\_ID** is valid.</span></span><br/>     |
| <span id="8_0x8"></span><span id="8_0X8"></span><dl> <span data-ttu-id="e4d19-209"><dt>**8 0x8**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d19-209"><dt>**8 0x8**</dt></span></span> </dl>          | <span data-ttu-id="e4d19-210">**Plataforma \_ do A \_ \_ ID de destino do erro** é válida.</span><span class="sxs-lookup"><span data-stu-id="e4d19-210">**PLATFORM\_ERROR\_TARGET\_ID** is valid.</span></span><br/>        |
| <span id="16_0x10"></span><span id="16_0X10"></span><dl> <span data-ttu-id="e4d19-211"><dt>**16 0x10**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d19-211"><dt>**16 0x10**</dt></span></span> </dl>    | <span data-ttu-id="e4d19-212">**Plataforma \_ do \_ \_ Dados específicos de erro** são válidos.</span><span class="sxs-lookup"><span data-stu-id="e4d19-212">**PLATFORM\_ERROR\_SPECIFIC\_DATA** is valid.</span></span><br/>    |
| <span id="32_0x20"></span><span id="32_0X20"></span><dl> <span data-ttu-id="e4d19-213"><dt>**32 0x20**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d19-213"><dt>**32 0x20**</dt></span></span> </dl>    | <span data-ttu-id="e4d19-214">**Plataforma \_ do ERRO \_ a \_ ID OEM** é válida.</span><span class="sxs-lookup"><span data-stu-id="e4d19-214">**PLATFORM\_ERROR\_OEM\_ID** is valid.</span></span><br/>           |
| <span id="64_0x40"></span><span id="64_0X40"></span><dl> <span data-ttu-id="e4d19-215"><dt>**64 0x40**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d19-215"><dt>**64 0x40**</dt></span></span> </dl>    | <span data-ttu-id="e4d19-216">**Plataforma \_ do ERRO \_ o \_ \_ struct de dados OEM** é válido.</span><span class="sxs-lookup"><span data-stu-id="e4d19-216">**PLATFORM\_ERROR\_OEM\_DATA\_STRUCT** is valid.</span></span><br/> |
| <span id="128_0x80"></span><span id="128_0X80"></span><dl> <span data-ttu-id="e4d19-217"><dt>**128 0x80**</dt></span><span class="sxs-lookup"><span data-stu-id="e4d19-217"><dt>**128 0x80**</dt></span></span> </dl> | <span data-ttu-id="e4d19-218">**Plataforma \_ do ERRO \_ o \_ \_ caminho do dispositivo OEM** é válido.</span><span class="sxs-lookup"><span data-stu-id="e4d19-218">**PLATFORM\_ERROR\_OEM\_DEVICE\_PATH** is valid.</span></span><br/> |



 

<span data-ttu-id="e4d19-219">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e4d19-219">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e4d19-220">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4d19-220">Remarks</span></span>

<span data-ttu-id="e4d19-221">A classe **MSMCAEvent \_ PlatformSpecificError** é derivada de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="e4d19-221">The **MSMCAEvent\_PlatformSpecificError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4d19-222">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4d19-222">Requirements</span></span>



| <span data-ttu-id="e4d19-223">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4d19-223">Requirement</span></span> | <span data-ttu-id="e4d19-224">Valor</span><span class="sxs-lookup"><span data-stu-id="e4d19-224">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4d19-225">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4d19-225">Minimum supported client</span></span><br/> | <span data-ttu-id="e4d19-226">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4d19-226">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="e4d19-227">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4d19-227">Minimum supported server</span></span><br/> | <span data-ttu-id="e4d19-228">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e4d19-228">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="e4d19-229">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4d19-229">Namespace</span></span><br/>                | <span data-ttu-id="e4d19-230">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="e4d19-230">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="e4d19-231">MOF</span><span class="sxs-lookup"><span data-stu-id="e4d19-231">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4d19-232"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4d19-232"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4d19-233">DLL</span><span class="sxs-lookup"><span data-stu-id="e4d19-233">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4d19-234"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4d19-234"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4d19-235">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4d19-235">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4d19-236">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="e4d19-236">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="e4d19-237">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="e4d19-237">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

