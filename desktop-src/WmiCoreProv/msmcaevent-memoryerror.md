---
description: Representa um evento de erro de memória da arquitetura de verificação de máquina (MCA). Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: 0db1d526-e2c3-4e48-90c8-cbcd9121040e
title: Classe MSMCAEvent_MemoryError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_MemoryError
- MSMCAEvent_MemoryError.Active
- MSMCAEvent_MemoryError.AdditionalErrors
- MSMCAEvent_MemoryError.BUS_SPECIFIC_DATA
- MSMCAEvent_MemoryError.Cpu
- MSMCAEvent_MemoryError.ErrorSeverity
- MSMCAEvent_MemoryError.InstanceName
- MSMCAEvent_MemoryError.MEM_BANK
- MSMCAEvent_MemoryError.MEM_BIT_POSITION
- MSMCAEvent_MemoryError.MEM_CARD
- MSMCAEvent_MemoryError.MEM_COLUMN
- MSMCAEvent_MemoryError.MEM_ERROR_STATUS
- MSMCAEvent_MemoryError.MEM_MODULE
- MSMCAEvent_MemoryError.MEM_NODE
- MSMCAEvent_MemoryError.MEM_PHYSICAL_ADDR
- MSMCAEvent_MemoryError.MEM_PHYSICAL_MASK
- MSMCAEvent_MemoryError.MEM_ROW
- MSMCAEvent_MemoryError.RawRecord
- MSMCAEvent_MemoryError.RecordId
- MSMCAEvent_MemoryError.REQUESTOR_ID
- MSMCAEvent_MemoryError.RESPONDER_ID
- MSMCAEvent_MemoryError.Size
- MSMCAEvent_MemoryError.TARGET_ID
- MSMCAEvent_MemoryError.Type
- MSMCAEvent_MemoryError.VALIDATION_BITS
- MSMCAEvent_MemoryError.MEM_DEVICE
- MSMCAEvent_MemoryError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 8dce82b8fa7a87676c34a9c6f26f43e4db10e227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813442"
---
# <a name="msmcaevent_memoryerror-class"></a><span data-ttu-id="f1d63-104">\_Classe MSMCAEvent MemoryError</span><span class="sxs-lookup"><span data-stu-id="f1d63-104">MSMCAEvent\_MemoryError class</span></span>

<span data-ttu-id="f1d63-105">A classe **MSMCAEvent \_ MemoryError** representa um evento de erro de memória de arquitetura de verificação de máquina (MCA).</span><span class="sxs-lookup"><span data-stu-id="f1d63-105">The **MSMCAEvent\_MemoryError** class represents a Machine Check Architecture (MCA) memory error event.</span></span> <span data-ttu-id="f1d63-106">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="f1d63-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="f1d63-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f1d63-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f1d63-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="f1d63-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1d63-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1d63-109">Syntax</span></span>

``` syntax
class MSMCAEvent_MemoryError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint64  BUS_SPECIFIC_DATA;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint16  MEM_BANK;
  uint16  MEM_BIT_POSITION;
  uint16  MEM_CARD;
  uint16  MEM_COLUMN;
  uint64  MEM_ERROR_STATUS;
  uint16  MEM_MODULE;
  uint16  MEM_NODE;
  uint64  MEM_PHYSICAL_ADDR;
  uint64  MEM_PHYSICAL_MASK;
  uint16  MEM_ROW;
  uint8   RawRecord[];
  uint64  RecordId;
  uint64  REQUESTOR_ID;
  uint64  RESPONDER_ID;
  uint32  Size;
  uint64  TARGET_ID;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint16  MEM_DEVICE;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="f1d63-110">Membros</span><span class="sxs-lookup"><span data-stu-id="f1d63-110">Members</span></span>

<span data-ttu-id="f1d63-111">A classe **MSMCAEvent \_ MemoryError** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f1d63-111">The **MSMCAEvent\_MemoryError** class has these types of members:</span></span>

-   [<span data-ttu-id="f1d63-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1d63-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f1d63-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1d63-113">Properties</span></span>

<span data-ttu-id="f1d63-114">A classe **MSMCAEvent \_ MemoryError** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1d63-114">The **MSMCAEvent\_MemoryError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f1d63-115">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="f1d63-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="f1d63-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-118">**True**, se esta instância da classe estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="f1d63-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="f1d63-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1d63-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-122">Número de erros adicionais no registro MCA.</span><span class="sxs-lookup"><span data-stu-id="f1d63-122">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-123">**\_dados específicos do barramento \_**</span><span class="sxs-lookup"><span data-stu-id="f1d63-123">**BUS\_SPECIFIC\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-124">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1d63-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-126">Dados dependentes de barramento específicos do OEM.</span><span class="sxs-lookup"><span data-stu-id="f1d63-126">OEM-specific, bus-dependent data.</span></span>

<span data-ttu-id="f1d63-127">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1d63-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-128">**CPUs**</span><span class="sxs-lookup"><span data-stu-id="f1d63-128">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-129">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1d63-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-131">CPU que relatou o erro.</span><span class="sxs-lookup"><span data-stu-id="f1d63-131">CPU that reported the error.</span></span> <span data-ttu-id="f1d63-132">Essa propriedade se aplica somente a um sistema multiprocessador no qual o primeiro processador recebe o número 0, o segundo processador recebe o número 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="f1d63-132">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-133">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="f1d63-133">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-134">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="f1d63-134">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-136">Nível de severidade do erro relatado.</span><span class="sxs-lookup"><span data-stu-id="f1d63-136">Severity level of the error reported.</span></span>



| <span data-ttu-id="f1d63-137">Valor</span><span class="sxs-lookup"><span data-stu-id="f1d63-137">Value</span></span>                                                                                                | <span data-ttu-id="f1d63-138">Significado</span><span class="sxs-lookup"><span data-stu-id="f1d63-138">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="f1d63-139"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-139"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="f1d63-140">Recuperado</span><span class="sxs-lookup"><span data-stu-id="f1d63-140">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="f1d63-141"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-141"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="f1d63-142">Fatais</span><span class="sxs-lookup"><span data-stu-id="f1d63-142">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="f1d63-143"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-143"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="f1d63-144">Corrigível</span><span class="sxs-lookup"><span data-stu-id="f1d63-144">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="f1d63-145">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="f1d63-145">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f1d63-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-148">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f1d63-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-149">Identificador exclusivo desta instância da classe.</span><span class="sxs-lookup"><span data-stu-id="f1d63-149">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-150">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="f1d63-150">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-151">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1d63-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-153">Se for zero, esse evento não será registrado no log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="f1d63-153">If zero then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-154">**banco de memória \_**</span><span class="sxs-lookup"><span data-stu-id="f1d63-154">**MEM\_BANK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-155">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1d63-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-157">O módulo ou número de classificação do local de erro de memória.</span><span class="sxs-lookup"><span data-stu-id="f1d63-157">The Module or RANK number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-158">**\_posição do bit mem \_**</span><span class="sxs-lookup"><span data-stu-id="f1d63-158">**MEM\_BIT\_POSITION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-159">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1d63-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-161">Posição do bit na palavra de memória que contém o erro.</span><span class="sxs-lookup"><span data-stu-id="f1d63-161">Bit position in the memory word that contains the error.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-162">**\_placa mem**</span><span class="sxs-lookup"><span data-stu-id="f1d63-162">**MEM\_CARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-163">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1d63-163">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-165">Número do cartão do local do erro de memória.</span><span class="sxs-lookup"><span data-stu-id="f1d63-165">Card number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-166">**\_coluna mem**</span><span class="sxs-lookup"><span data-stu-id="f1d63-166">**MEM\_COLUMN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1d63-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-169">Número da coluna do local de erro de memória.</span><span class="sxs-lookup"><span data-stu-id="f1d63-169">Column number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-170">**\_dispositivo mem**</span><span class="sxs-lookup"><span data-stu-id="f1d63-170">**MEM\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-171">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1d63-171">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-172">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-173">Número do dispositivo do local de erro de memória.</span><span class="sxs-lookup"><span data-stu-id="f1d63-173">Device number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-174">**\_status de erro de mem \_**</span><span class="sxs-lookup"><span data-stu-id="f1d63-174">**MEM\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-175">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1d63-175">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-177">Status de erro de memória.</span><span class="sxs-lookup"><span data-stu-id="f1d63-177">Memory error status.</span></span>

<span data-ttu-id="f1d63-178">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1d63-178">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-179">**\_módulo mem**</span><span class="sxs-lookup"><span data-stu-id="f1d63-179">**MEM\_MODULE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-180">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1d63-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-182">Número de módulo ou de classificação do local de erro de memória.</span><span class="sxs-lookup"><span data-stu-id="f1d63-182">Module or rank number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-183">**nó do MEM \_**</span><span class="sxs-lookup"><span data-stu-id="f1d63-183">**MEM\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-184">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1d63-184">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-185">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-186">Nó que contém o erro de memória.</span><span class="sxs-lookup"><span data-stu-id="f1d63-186">Node that contains the memory error.</span></span> <span data-ttu-id="f1d63-187">Essa propriedade só se aplica a um sistema com vários nós.</span><span class="sxs-lookup"><span data-stu-id="f1d63-187">This property applies only in a multi-node system.</span></span> <span data-ttu-id="f1d63-188">Essa propriedade é específica do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="f1d63-188">This property is vendor-specific.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-189">**\_endereço físico de mem \_**</span><span class="sxs-lookup"><span data-stu-id="f1d63-189">**MEM\_PHYSICAL\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-190">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1d63-190">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-192">Endereço físico do erro de memória.</span><span class="sxs-lookup"><span data-stu-id="f1d63-192">Physical address of the memory error.</span></span>

<span data-ttu-id="f1d63-193">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1d63-193">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-194">**\_máscara física de mem \_**</span><span class="sxs-lookup"><span data-stu-id="f1d63-194">**MEM\_PHYSICAL\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-195">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1d63-195">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-196">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-197">Bits de endereço válidos no endereço físico de 64 bits do erro de memória.</span><span class="sxs-lookup"><span data-stu-id="f1d63-197">Valid address bits in the 64-bit physical address of the memory error.</span></span>

> [!Note]  
> <span data-ttu-id="f1d63-198">A máscara física especifica a granularidade do endereço físico.</span><span class="sxs-lookup"><span data-stu-id="f1d63-198">The physical mask specifies the granularity of the physical address.</span></span> <span data-ttu-id="f1d63-199">O endereço físico do erro de memória depende dos fatores de implementação de hardware.</span><span class="sxs-lookup"><span data-stu-id="f1d63-199">The physical address of the memory error is dependent on hardware implementation factors.</span></span>

 

<span data-ttu-id="f1d63-200">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1d63-200">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-201">**linha de MEM \_**</span><span class="sxs-lookup"><span data-stu-id="f1d63-201">**MEM\_ROW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-202">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f1d63-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-204">Número da linha do local do erro de memória.</span><span class="sxs-lookup"><span data-stu-id="f1d63-204">Row number of the memory error location.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-205">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="f1d63-205">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-206">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="f1d63-206">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-207">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-207">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-208">Matriz de bytes que contém o registro de erro bruto conforme apresentado ao Windows pela camada de abstração do sistema (SAL).</span><span class="sxs-lookup"><span data-stu-id="f1d63-208">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="f1d63-209">O número de elementos na matriz é especificado pela propriedade **size** .</span><span class="sxs-lookup"><span data-stu-id="f1d63-209">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-210">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="f1d63-210">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-211">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1d63-211">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-212">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-213">Identificador de registro do registro de erro para este erro.</span><span class="sxs-lookup"><span data-stu-id="f1d63-213">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="f1d63-214">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1d63-214">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-215">**ID do SOLICITAnte \_**</span><span class="sxs-lookup"><span data-stu-id="f1d63-215">**REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-216">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1d63-216">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-218">Endereço de hardware do dispositivo ou componente que inicia a transação.</span><span class="sxs-lookup"><span data-stu-id="f1d63-218">Hardware address of the device or component that initiates the transaction.</span></span>

<span data-ttu-id="f1d63-219">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1d63-219">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-220">**ID do RESPONDEnte \_**</span><span class="sxs-lookup"><span data-stu-id="f1d63-220">**RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-221">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1d63-221">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-223">Endereço de hardware do Respondente para a transação.</span><span class="sxs-lookup"><span data-stu-id="f1d63-223">Hardware address of the responder to the transaction.</span></span>

<span data-ttu-id="f1d63-224">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1d63-224">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-225">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="f1d63-225">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-226">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1d63-226">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-227">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-227">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-228">Tamanho do registro de erro bruto em bytes.</span><span class="sxs-lookup"><span data-stu-id="f1d63-228">Size of the raw error record in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-229">**ID de destino \_**</span><span class="sxs-lookup"><span data-stu-id="f1d63-229">**TARGET\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-230">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1d63-230">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-231">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-231">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-232">Endereço de hardware do destino pretendido da transação.</span><span class="sxs-lookup"><span data-stu-id="f1d63-232">Hardware address of the intended target of the transaction.</span></span>

<span data-ttu-id="f1d63-233">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1d63-233">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-234">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f1d63-234">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-235">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f1d63-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-237">Tipo de mensagem de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="f1d63-237">Type of event log message.</span></span> <span data-ttu-id="f1d63-238">Essas mensagens correspondem aos códigos de mensagem de log de eventos usados para inserir mensagens de log de eventos pelo provedor de consumidor do log de eventos do Windows quando ele recebe um dos eventos.</span><span class="sxs-lookup"><span data-stu-id="f1d63-238">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="f1d63-239">**BITS de validação \_**</span><span class="sxs-lookup"><span data-stu-id="f1d63-239">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f1d63-240">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f1d63-240">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f1d63-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1d63-241">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f1d63-242">Bits de validação usados para indicar a validade dos campos subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f1d63-242">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="f1d63-243">Valores</span><span class="sxs-lookup"><span data-stu-id="f1d63-243">Values</span></span>                                                                                     | <span data-ttu-id="f1d63-244">Significado</span><span class="sxs-lookup"><span data-stu-id="f1d63-244">Meaning</span></span>                                                 |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="f1d63-245"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-245"><dt>1 (0x1)</dt></span></span> </dl>         | <span data-ttu-id="f1d63-246">O \_ status de erro de mem \_ é válido.</span><span class="sxs-lookup"><span data-stu-id="f1d63-246">MEM\_ERROR\_STATUS is valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="f1d63-247"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-247"><dt>2 (0x2)</dt></span></span> </dl>         | <span data-ttu-id="f1d63-248">O \_ endereço físico de mem \_ é válido.</span><span class="sxs-lookup"><span data-stu-id="f1d63-248">MEM\_PHYSICAL\_ADDR is valid.</span></span><br/>                |
| <dl> <span data-ttu-id="f1d63-249"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-249"><dt>4 (0x4)</dt></span></span> </dl>         | <span data-ttu-id="f1d63-250">A \_ máscara de endereço de mem \_ é válida.</span><span class="sxs-lookup"><span data-stu-id="f1d63-250">MEM\_ADDR\_MASK is valid.</span></span><br/>                    |
| <dl> <span data-ttu-id="f1d63-251"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-251"><dt>8 (0x8)</dt></span></span> </dl>         | <span data-ttu-id="f1d63-252">O \_ nó mem é válido.</span><span class="sxs-lookup"><span data-stu-id="f1d63-252">MEM\_NODE is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="f1d63-253"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-253"><dt>16 (0x10)</dt></span></span> </dl>       | <span data-ttu-id="f1d63-254">O \_ cartão mem é válido.</span><span class="sxs-lookup"><span data-stu-id="f1d63-254">MEM\_CARD is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="f1d63-255"><dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-255"><dt>32 (0x20)</dt></span></span> </dl>       | <span data-ttu-id="f1d63-256">O \_ módulo mem é válido.</span><span class="sxs-lookup"><span data-stu-id="f1d63-256">MEM\_MODULE is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="f1d63-257"><dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-257"><dt>64 (0x40)</dt></span></span> </dl>       | <span data-ttu-id="f1d63-258">O \_ banco mem é válido.</span><span class="sxs-lookup"><span data-stu-id="f1d63-258">MEM\_BANK is valid.</span></span><br/>                          |
| <dl> <span data-ttu-id="f1d63-259"><dt>128 (0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-259"><dt>128 (0x80)</dt></span></span> </dl>      | <span data-ttu-id="f1d63-260">O \_ dispositivo mem é válido.</span><span class="sxs-lookup"><span data-stu-id="f1d63-260">MEM\_DEVICE is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="f1d63-261"><dt>256 (0x100)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-261"><dt>256 (0x100)</dt></span></span> </dl>     | <span data-ttu-id="f1d63-262">A \_ linha de mem é válida.</span><span class="sxs-lookup"><span data-stu-id="f1d63-262">MEM\_ROW is valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="f1d63-263"><dt>512 (0x200)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-263"><dt>512 (0x200)</dt></span></span> </dl>     | <span data-ttu-id="f1d63-264">A \_ coluna mem é válida.</span><span class="sxs-lookup"><span data-stu-id="f1d63-264">MEM\_COLUMN is valid.</span></span><br/>                        |
| <dl> <span data-ttu-id="f1d63-265"><dt>1024 (0x400)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-265"><dt>1024 (0x400)</dt></span></span> </dl>    | <span data-ttu-id="f1d63-266">A \_ posição do bit mem \_ é válida.</span><span class="sxs-lookup"><span data-stu-id="f1d63-266">MEM\_BIT\_POSITION is valid.</span></span><br/>                 |
| <dl> <span data-ttu-id="f1d63-267"><dt>2048 (0x800)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-267"><dt>2048 (0x800)</dt></span></span> </dl>    | <span data-ttu-id="f1d63-268">A \_ ID do solicitante da plataforma mem \_ \_ é válida.</span><span class="sxs-lookup"><span data-stu-id="f1d63-268">MEM\_PLATFORM\_REQUESTOR\_ID is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="f1d63-269"><dt>4096 (0x1000)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-269"><dt>4096 (0x1000)</dt></span></span> </dl>   | <span data-ttu-id="f1d63-270">A \_ ID do Respondente da plataforma mem \_ \_ é válida.</span><span class="sxs-lookup"><span data-stu-id="f1d63-270">MEM\_PLATFORM\_RESPONDER\_ID is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="f1d63-271"><dt>8192 (0x2000)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-271"><dt>8192 (0x2000)</dt></span></span> </dl>   | <span data-ttu-id="f1d63-272">O \_ destino da plataforma mem \_ é válido.</span><span class="sxs-lookup"><span data-stu-id="f1d63-272">MEM\_PLATFORM\_TARGET is valid.</span></span><br/>              |
| <dl> <span data-ttu-id="f1d63-273"><dt>16384 (0x4000)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-273"><dt>16384 (0x4000)</dt></span></span> </dl>  | <span data-ttu-id="f1d63-274">\_ \_ Os dados específicos do barramento da plataforma mem \_ \_ são válidos.</span><span class="sxs-lookup"><span data-stu-id="f1d63-274">MEM\_PLATFORM\_BUS\_SPECIFIC\_DATA is valid.</span></span><br/> |
| <dl> <span data-ttu-id="f1d63-275"><dt>32768 (0x8000)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-275"><dt>32768 (0x8000)</dt></span></span> </dl>  | <span data-ttu-id="f1d63-276">A \_ ID OEM da plataforma mem \_ \_ é válida.</span><span class="sxs-lookup"><span data-stu-id="f1d63-276">MEM\_PLATFORM\_OEM\_ID is valid.</span></span><br/>             |
| <dl> <span data-ttu-id="f1d63-277"><dt>65536 (0x10000)</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-277"><dt>65536 (0x10000)</dt></span></span> </dl> | <span data-ttu-id="f1d63-278">A \_ estrutura de dados OEM da plataforma mem \_ \_ \_ é válida.</span><span class="sxs-lookup"><span data-stu-id="f1d63-278">MEM\_PLATFORM\_OEM\_DATA\_STRUCT is valid.</span></span><br/>   |



 

<span data-ttu-id="f1d63-279">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f1d63-279">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1d63-280">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1d63-280">Remarks</span></span>

<span data-ttu-id="f1d63-281">A classe **MSMCAEvent \_ MemoryError** é derivada de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="f1d63-281">The **MSMCAEvent\_MemoryError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1d63-282">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1d63-282">Requirements</span></span>



| <span data-ttu-id="f1d63-283">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1d63-283">Requirement</span></span> | <span data-ttu-id="f1d63-284">Valor</span><span class="sxs-lookup"><span data-stu-id="f1d63-284">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1d63-285">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1d63-285">Minimum supported client</span></span><br/> | <span data-ttu-id="f1d63-286">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f1d63-286">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="f1d63-287">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1d63-287">Minimum supported server</span></span><br/> | <span data-ttu-id="f1d63-288">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f1d63-288">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="f1d63-289">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1d63-289">Namespace</span></span><br/>                | <span data-ttu-id="f1d63-290">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="f1d63-290">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="f1d63-291">MOF</span><span class="sxs-lookup"><span data-stu-id="f1d63-291">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f1d63-292"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-292"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="f1d63-293">DLL</span><span class="sxs-lookup"><span data-stu-id="f1d63-293">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1d63-294"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1d63-294"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1d63-295">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1d63-295">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1d63-296">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="f1d63-296">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="f1d63-297">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="f1d63-297">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

