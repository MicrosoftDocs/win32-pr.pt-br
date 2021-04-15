---
description: Representa um evento de erro de CPU. Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: 4ee4aa51-a965-4569-b53c-0ba21bf42752
title: Classe MSMCAEvent_CPUError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_CPUError
- MSMCAEvent_CPUError.Active
- MSMCAEvent_CPUError.AdditionalErrors
- MSMCAEvent_CPUError.Cpu
- MSMCAEvent_CPUError.ErrorSeverity
- MSMCAEvent_CPUError.InstanceName
- MSMCAEvent_CPUError.Level
- MSMCAEvent_CPUError.RawRecord
- MSMCAEvent_CPUError.RecordId
- MSMCAEvent_CPUError.Size
- MSMCAEvent_CPUError.Type
- MSMCAEvent_CPUError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: dff990b46d730a1e8b54ef99a24a686745e3dacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501674"
---
# <a name="msmcaevent_cpuerror-class"></a><span data-ttu-id="aad9a-104">\_Classe MSMCAEvent CPUError</span><span class="sxs-lookup"><span data-stu-id="aad9a-104">MSMCAEvent\_CPUError class</span></span>

<span data-ttu-id="aad9a-105">A classe **MSMCAEvent \_ CPUError** representa um evento de erro de CPU.</span><span class="sxs-lookup"><span data-stu-id="aad9a-105">The **MSMCAEvent\_CPUError** class represents a CPU error event.</span></span> <span data-ttu-id="aad9a-106">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="aad9a-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="aad9a-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="aad9a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="aad9a-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="aad9a-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aad9a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aad9a-109">Syntax</span></span>

``` syntax
class MSMCAEvent_CPUError : WmiEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint32  Level;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="aad9a-110">Membros</span><span class="sxs-lookup"><span data-stu-id="aad9a-110">Members</span></span>

<span data-ttu-id="aad9a-111">A classe **MSMCAEvent \_ CPUError** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="aad9a-111">The **MSMCAEvent\_CPUError** class has these types of members:</span></span>

-   [<span data-ttu-id="aad9a-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aad9a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aad9a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aad9a-113">Properties</span></span>

<span data-ttu-id="aad9a-114">A classe **MSMCAEvent \_ CPUError** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="aad9a-114">The **MSMCAEvent\_CPUError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aad9a-115">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="aad9a-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad9a-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="aad9a-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aad9a-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aad9a-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aad9a-118">**True**, se esta instância da classe estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="aad9a-118">**TRUE**, if this instance of the class is active; otherwise **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="aad9a-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="aad9a-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad9a-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aad9a-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad9a-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aad9a-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aad9a-122">Número de erros adicionais no registro MCA.</span><span class="sxs-lookup"><span data-stu-id="aad9a-122">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="aad9a-123">**CPUs**</span><span class="sxs-lookup"><span data-stu-id="aad9a-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad9a-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aad9a-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad9a-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aad9a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aad9a-126">CPU que relatou o erro.</span><span class="sxs-lookup"><span data-stu-id="aad9a-126">CPU that reported the error.</span></span> <span data-ttu-id="aad9a-127">Essa propriedade se aplica somente a um sistema multiprocessador no qual o primeiro processador recebe o número 0, o segundo processador recebe o número 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="aad9a-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="aad9a-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="aad9a-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad9a-129">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="aad9a-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="aad9a-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aad9a-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aad9a-131">Nível de severidade do erro relatado.</span><span class="sxs-lookup"><span data-stu-id="aad9a-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="aad9a-132">Valor</span><span class="sxs-lookup"><span data-stu-id="aad9a-132">Value</span></span>                                                                                                | <span data-ttu-id="aad9a-133">Significado</span><span class="sxs-lookup"><span data-stu-id="aad9a-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="aad9a-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="aad9a-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="aad9a-135">Recuperado</span><span class="sxs-lookup"><span data-stu-id="aad9a-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="aad9a-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="aad9a-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="aad9a-137">Fatais</span><span class="sxs-lookup"><span data-stu-id="aad9a-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="aad9a-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="aad9a-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="aad9a-139">Corrigível</span><span class="sxs-lookup"><span data-stu-id="aad9a-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="aad9a-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="aad9a-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad9a-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="aad9a-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="aad9a-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aad9a-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad9a-143">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="aad9a-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="aad9a-144">Identificador exclusivo para esta instância da classe.</span><span class="sxs-lookup"><span data-stu-id="aad9a-144">Unique identifier for this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="aad9a-145">**Level**</span><span class="sxs-lookup"><span data-stu-id="aad9a-145">**Level**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad9a-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aad9a-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad9a-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aad9a-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aad9a-148">Qualificadores: **WmiMissingData** (-1)</span><span class="sxs-lookup"><span data-stu-id="aad9a-148">Qualifiers: **WmiMissingData** (-1)</span></span>
</dt> </dl>

<span data-ttu-id="aad9a-149">Nível de cache, TLB (buffer de conversão) ou estrutura de micro-arquitetura em que o erro ocorreu.</span><span class="sxs-lookup"><span data-stu-id="aad9a-149">Level of cache, translation buffer (TLB), or micro-architectural structure where the error occurred.</span></span> <span data-ttu-id="aad9a-150">Um valor de 0 (zero) indica o primeiro nível.</span><span class="sxs-lookup"><span data-stu-id="aad9a-150">A value of 0 (zero) indicates the first level.</span></span>

</dd> <dt>

<span data-ttu-id="aad9a-151">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="aad9a-151">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad9a-152">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aad9a-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad9a-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aad9a-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aad9a-154">Se for zero, esse evento não será registrado no log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="aad9a-154">If zero then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="aad9a-155">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="aad9a-155">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad9a-156">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="aad9a-156">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="aad9a-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aad9a-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aad9a-158">Matriz de bytes que contém o registro de erro bruto.</span><span class="sxs-lookup"><span data-stu-id="aad9a-158">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="aad9a-159">O número de elementos na matriz que a propriedade **size** especifica.</span><span class="sxs-lookup"><span data-stu-id="aad9a-159">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="aad9a-160">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="aad9a-160">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad9a-161">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="aad9a-161">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="aad9a-162">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aad9a-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aad9a-163">Identificador de registro do registro de erro para este erro.</span><span class="sxs-lookup"><span data-stu-id="aad9a-163">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="aad9a-164">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="aad9a-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="aad9a-165">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="aad9a-165">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad9a-166">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aad9a-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad9a-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aad9a-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aad9a-168">Tamanho do registro de erro bruto em bytes.</span><span class="sxs-lookup"><span data-stu-id="aad9a-168">Size of the raw error record in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="aad9a-169">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="aad9a-169">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aad9a-170">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="aad9a-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="aad9a-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aad9a-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aad9a-172">Tipo de mensagem de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="aad9a-172">Type of event log message.</span></span> <span data-ttu-id="aad9a-173">Essas mensagens correspondem aos códigos de mensagem de log de eventos usados para inserir mensagens de log de eventos pelo provedor de consumidor do log de eventos do Windows quando ele recebe um dos eventos.</span><span class="sxs-lookup"><span data-stu-id="aad9a-173">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aad9a-174">Comentários</span><span class="sxs-lookup"><span data-stu-id="aad9a-174">Remarks</span></span>

<span data-ttu-id="aad9a-175">A classe **MSMCAEvent \_ CPUError** é derivada de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="aad9a-175">The **MSMCAEvent\_CPUError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aad9a-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aad9a-176">Requirements</span></span>



| <span data-ttu-id="aad9a-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="aad9a-177">Requirement</span></span> | <span data-ttu-id="aad9a-178">Valor</span><span class="sxs-lookup"><span data-stu-id="aad9a-178">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aad9a-179">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aad9a-179">Minimum supported client</span></span><br/> | <span data-ttu-id="aad9a-180">Windows XP</span><span class="sxs-lookup"><span data-stu-id="aad9a-180">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="aad9a-181">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aad9a-181">Minimum supported server</span></span><br/> | <span data-ttu-id="aad9a-182">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aad9a-182">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="aad9a-183">Namespace</span><span class="sxs-lookup"><span data-stu-id="aad9a-183">Namespace</span></span><br/>                | <span data-ttu-id="aad9a-184">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="aad9a-184">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="aad9a-185">MOF</span><span class="sxs-lookup"><span data-stu-id="aad9a-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aad9a-186"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aad9a-186"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="aad9a-187">DLL</span><span class="sxs-lookup"><span data-stu-id="aad9a-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aad9a-188"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aad9a-188"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aad9a-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="aad9a-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aad9a-190">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="aad9a-190">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="aad9a-191">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="aad9a-191">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

