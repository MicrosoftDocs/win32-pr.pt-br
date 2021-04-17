---
description: Indica um erro de arquitetura de verificação de máquina (MCA) inválido. Um erro de MCA inválido identifica um formato de erro que não está de acordo com as especificações do Windows. Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: 476ea558-2e0e-480f-b4ba-8d73fdef3308
title: Classe MSMCAEvent_InvalidError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_InvalidError
- MSMCAEvent_InvalidError.Active
- MSMCAEvent_InvalidError.AdditionalErrors
- MSMCAEvent_InvalidError.Cpu
- MSMCAEvent_InvalidError.ErrorSeverity
- MSMCAEvent_InvalidError.InstanceName
- MSMCAEvent_InvalidError.RawRecord
- MSMCAEvent_InvalidError.RecordId
- MSMCAEvent_InvalidError.Size
- MSMCAEvent_InvalidError.Type
- MSMCAEvent_InvalidError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: abd12cfa7280a1b2f6a718b47b17d4ddf121cc25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763984"
---
# <a name="msmcaevent_invaliderror-class"></a><span data-ttu-id="62631-105">\_Classe MSMCAEvent InvalidError</span><span class="sxs-lookup"><span data-stu-id="62631-105">MSMCAEvent\_InvalidError class</span></span>

<span data-ttu-id="62631-106">A classe **MSMCAEvent \_ InvalidError** indica um erro de arquitetura de verificação de máquina (MCA) inválido.</span><span class="sxs-lookup"><span data-stu-id="62631-106">The **MSMCAEvent\_InvalidError** class indicates a Machine Check Architecture (MCA) invalid error.</span></span> <span data-ttu-id="62631-107">Um erro de MCA inválido identifica um formato de erro que não está de acordo com as especificações do Windows.</span><span class="sxs-lookup"><span data-stu-id="62631-107">An invalid MCA error identifies an error format that does not conform to Windows specifications.</span></span> <span data-ttu-id="62631-108">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="62631-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="62631-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="62631-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="62631-110">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="62631-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="62631-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62631-111">Syntax</span></span>

``` syntax
class MSMCAEvent_InvalidError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="62631-112">Membros</span><span class="sxs-lookup"><span data-stu-id="62631-112">Members</span></span>

<span data-ttu-id="62631-113">A classe **MSMCAEvent \_ InvalidError** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="62631-113">The **MSMCAEvent\_InvalidError** class has these types of members:</span></span>

-   [<span data-ttu-id="62631-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="62631-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62631-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="62631-115">Properties</span></span>

<span data-ttu-id="62631-116">A classe **MSMCAEvent \_ InvalidError** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="62631-116">The **MSMCAEvent\_InvalidError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62631-117">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="62631-117">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62631-118">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="62631-118">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="62631-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62631-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62631-120">**True**, se esta instância da classe estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="62631-120">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="62631-121">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="62631-121">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62631-122">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62631-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62631-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62631-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62631-124">Número de erros adicionais no registro MCA.</span><span class="sxs-lookup"><span data-stu-id="62631-124">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="62631-125">**CPUs**</span><span class="sxs-lookup"><span data-stu-id="62631-125">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62631-126">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62631-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62631-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62631-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62631-128">CPU que relatou o erro.</span><span class="sxs-lookup"><span data-stu-id="62631-128">CPU that reported the error.</span></span> <span data-ttu-id="62631-129">Essa propriedade se aplica somente a um sistema multiprocessador no qual o primeiro processador recebe o número 0, o segundo processador recebe o número 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="62631-129">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="62631-130">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="62631-130">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62631-131">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="62631-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="62631-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62631-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62631-133">Nível de severidade do erro relatado.</span><span class="sxs-lookup"><span data-stu-id="62631-133">Severity level of the error reported.</span></span>



| <span data-ttu-id="62631-134">Valor</span><span class="sxs-lookup"><span data-stu-id="62631-134">Value</span></span>                                                                                                | <span data-ttu-id="62631-135">Significado</span><span class="sxs-lookup"><span data-stu-id="62631-135">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="62631-136"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="62631-136"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="62631-137">Recuperado</span><span class="sxs-lookup"><span data-stu-id="62631-137">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="62631-138"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="62631-138"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="62631-139">Fatais</span><span class="sxs-lookup"><span data-stu-id="62631-139">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="62631-140"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="62631-140"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="62631-141">Corrigível</span><span class="sxs-lookup"><span data-stu-id="62631-141">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="62631-142">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="62631-142">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62631-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="62631-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="62631-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62631-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="62631-145">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="62631-145">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="62631-146">Identificador exclusivo desta instância da classe.</span><span class="sxs-lookup"><span data-stu-id="62631-146">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="62631-147">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="62631-147">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62631-148">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62631-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62631-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62631-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62631-150">Se for 0 (zero), esse evento não será registrado no log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="62631-150">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="62631-151">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="62631-151">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62631-152">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="62631-152">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="62631-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62631-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62631-154">Matriz de bytes que contém o registro de erro bruto conforme apresentado ao Windows pela camada de abstração do sistema (SAL).</span><span class="sxs-lookup"><span data-stu-id="62631-154">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="62631-155">O número de elementos na matriz é especificado pela propriedade **size** .</span><span class="sxs-lookup"><span data-stu-id="62631-155">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="62631-156">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="62631-156">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62631-157">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="62631-157">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="62631-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62631-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62631-159">Identificador de registro do registro de erro para este erro.</span><span class="sxs-lookup"><span data-stu-id="62631-159">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="62631-160">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="62631-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="62631-161">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="62631-161">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62631-162">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62631-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62631-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62631-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62631-164">Tamanho do registro de erro bruto.</span><span class="sxs-lookup"><span data-stu-id="62631-164">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="62631-165">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="62631-165">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62631-166">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="62631-166">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="62631-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="62631-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62631-168">Tipo de mensagem de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="62631-168">Type of event log message.</span></span> <span data-ttu-id="62631-169">Essas mensagens correspondem aos códigos de mensagem de log de eventos usados para inserir mensagens de log de eventos pelo provedor de consumidor do log de eventos do Windows quando ele recebe um dos eventos.</span><span class="sxs-lookup"><span data-stu-id="62631-169">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62631-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="62631-170">Remarks</span></span>

<span data-ttu-id="62631-171">A classe **MSMCAEvent \_ InvalidError** é derivada de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="62631-171">The **MSMCAEvent\_InvalidError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62631-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62631-172">Requirements</span></span>



| <span data-ttu-id="62631-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="62631-173">Requirement</span></span> | <span data-ttu-id="62631-174">Valor</span><span class="sxs-lookup"><span data-stu-id="62631-174">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62631-175">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62631-175">Minimum supported client</span></span><br/> | <span data-ttu-id="62631-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="62631-176">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="62631-177">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62631-177">Minimum supported server</span></span><br/> | <span data-ttu-id="62631-178">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="62631-178">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="62631-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="62631-179">Namespace</span></span><br/>                | <span data-ttu-id="62631-180">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="62631-180">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="62631-181">MOF</span><span class="sxs-lookup"><span data-stu-id="62631-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62631-182"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62631-182"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="62631-183">DLL</span><span class="sxs-lookup"><span data-stu-id="62631-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62631-184"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62631-184"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62631-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="62631-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62631-186">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="62631-186">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="62631-187">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="62631-187">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

