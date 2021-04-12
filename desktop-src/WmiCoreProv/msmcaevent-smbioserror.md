---
description: Indica um erro de BIOS do sistema de arquitetura de verificação de máquina (MCA). Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: b451ca45-6208-4445-b9f1-b4e3174837a4
title: Classe MSMCAEvent_SMBIOSError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SMBIOSError
- MSMCAEvent_SMBIOSError.Active
- MSMCAEvent_SMBIOSError.AdditionalErrors
- MSMCAEvent_SMBIOSError.Cpu
- MSMCAEvent_SMBIOSError.ErrorSeverity
- MSMCAEvent_SMBIOSError.InstanceName
- MSMCAEvent_SMBIOSError.RawRecord
- MSMCAEvent_SMBIOSError.RecordId
- MSMCAEvent_SMBIOSError.Size
- MSMCAEvent_SMBIOSError.SMBIOS_EVENT_TYPE
- MSMCAEvent_SMBIOSError.Type
- MSMCAEvent_SMBIOSError.VALIDATION_BITS
- MSMCAEvent_SMBIOSError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 709d480e8865c5d5bde2a9f5e8de45f138e66548
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171099"
---
# <a name="msmcaevent_smbioserror-class"></a><span data-ttu-id="a73f8-104">\_Classe MSMCAEvent SMBIOSError</span><span class="sxs-lookup"><span data-stu-id="a73f8-104">MSMCAEvent\_SMBIOSError class</span></span>

<span data-ttu-id="a73f8-105">A classe **MSMCAEvent \_ SMBIOSError** indica um erro de BIOS do sistema de arquitetura de verificação de máquina (MCA).</span><span class="sxs-lookup"><span data-stu-id="a73f8-105">The **MSMCAEvent\_SMBIOSError** class indicates a Machine Check Architecture (MCA) system BIOS error.</span></span> <span data-ttu-id="a73f8-106">Essa classe está disponível somente em sistemas Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a73f8-106">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="a73f8-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a73f8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="a73f8-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="a73f8-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73f8-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a73f8-109">Syntax</span></span>

``` syntax
class MSMCAEvent_SMBIOSError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint8   SMBIOS_EVENT_TYPE;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="a73f8-110">Membros</span><span class="sxs-lookup"><span data-stu-id="a73f8-110">Members</span></span>

<span data-ttu-id="a73f8-111">A classe **MSMCAEvent \_ SMBIOSError** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a73f8-111">The **MSMCAEvent\_SMBIOSError** class has these types of members:</span></span>

-   [<span data-ttu-id="a73f8-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a73f8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a73f8-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a73f8-113">Properties</span></span>

<span data-ttu-id="a73f8-114">A classe **MSMCAEvent \_ SMBIOSError** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a73f8-114">The **MSMCAEvent\_SMBIOSError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a73f8-115">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="a73f8-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73f8-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a73f8-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a73f8-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a73f8-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a73f8-118">**True**, se esta instância da classe estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="a73f8-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a73f8-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="a73f8-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73f8-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a73f8-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a73f8-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a73f8-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a73f8-122">Número de erros adicionais no registro.</span><span class="sxs-lookup"><span data-stu-id="a73f8-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="a73f8-123">**CPUs**</span><span class="sxs-lookup"><span data-stu-id="a73f8-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73f8-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a73f8-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a73f8-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a73f8-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a73f8-126">CPU que relatou o erro.</span><span class="sxs-lookup"><span data-stu-id="a73f8-126">CPU that reported the error.</span></span> <span data-ttu-id="a73f8-127">Essa propriedade se aplica somente a um sistema multiprocessador no qual o primeiro processador recebe o número 0, o segundo processador recebe o número 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a73f8-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="a73f8-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="a73f8-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73f8-129">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="a73f8-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a73f8-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a73f8-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a73f8-131">Nível de severidade do erro relatado.</span><span class="sxs-lookup"><span data-stu-id="a73f8-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="a73f8-132">Valor</span><span class="sxs-lookup"><span data-stu-id="a73f8-132">Value</span></span>                                                                                                | <span data-ttu-id="a73f8-133">Significado</span><span class="sxs-lookup"><span data-stu-id="a73f8-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="a73f8-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="a73f8-135">Recuperado</span><span class="sxs-lookup"><span data-stu-id="a73f8-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="a73f8-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="a73f8-137">Fatais</span><span class="sxs-lookup"><span data-stu-id="a73f8-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="a73f8-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="a73f8-139">Corrigível</span><span class="sxs-lookup"><span data-stu-id="a73f8-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a73f8-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="a73f8-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73f8-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a73f8-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a73f8-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a73f8-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a73f8-143">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a73f8-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a73f8-144">Identificador exclusivo desta instância da classe.</span><span class="sxs-lookup"><span data-stu-id="a73f8-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="a73f8-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="a73f8-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73f8-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a73f8-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a73f8-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a73f8-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a73f8-148">Se for 0 (zero), esse evento não será registrado no log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="a73f8-148">If 0 (zero), then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="a73f8-149">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="a73f8-149">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73f8-150">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="a73f8-150">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a73f8-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a73f8-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a73f8-152">Matriz de bytes que contém o registro de erro bruto.</span><span class="sxs-lookup"><span data-stu-id="a73f8-152">Array of bytes that contains the raw error record.</span></span> <span data-ttu-id="a73f8-153">O número de elementos na matriz que a propriedade **size** especifica.</span><span class="sxs-lookup"><span data-stu-id="a73f8-153">The number of elements in the array that the **Size** property specifies.</span></span>

</dd> <dt>

<span data-ttu-id="a73f8-154">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="a73f8-154">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73f8-155">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a73f8-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a73f8-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a73f8-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a73f8-157">Identificador de registro do registro de erro para este erro.</span><span class="sxs-lookup"><span data-stu-id="a73f8-157">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="a73f8-158">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a73f8-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a73f8-159">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="a73f8-159">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73f8-160">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a73f8-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a73f8-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a73f8-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a73f8-162">Tamanho do registro de erro bruto.</span><span class="sxs-lookup"><span data-stu-id="a73f8-162">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="a73f8-163">**\_tipo de evento SMBIOS \_**</span><span class="sxs-lookup"><span data-stu-id="a73f8-163">**SMBIOS\_EVENT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73f8-164">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="a73f8-164">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="a73f8-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a73f8-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a73f8-166">Tipo de evento.</span><span class="sxs-lookup"><span data-stu-id="a73f8-166">Event type.</span></span>



| <span data-ttu-id="a73f8-167">Valor</span><span class="sxs-lookup"><span data-stu-id="a73f8-167">Value</span></span>                                                                                                  | <span data-ttu-id="a73f8-168">Significado</span><span class="sxs-lookup"><span data-stu-id="a73f8-168">Meaning</span></span>                                                                                                                     |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="a73f8-169"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-169"><dt>**0**</dt></span></span> </dl>   | <span data-ttu-id="a73f8-170">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a73f8-170">Reserved.</span></span><br/>                                                                                                        |
| <span id="1"></span><dl> <span data-ttu-id="a73f8-171"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-171"><dt>**1**</dt></span></span> </dl>   | <span data-ttu-id="a73f8-172">Erro de memória ECC de bit único.</span><span class="sxs-lookup"><span data-stu-id="a73f8-172">Single bit ECC memory error.</span></span><br/>                                                                                     |
| <span id="2"></span><dl> <span data-ttu-id="a73f8-173"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-173"><dt>**2**</dt></span></span> </dl>   | <span data-ttu-id="a73f8-174">Erro de memória ECC de vários bits.</span><span class="sxs-lookup"><span data-stu-id="a73f8-174">Multiple bit ECC memory error.</span></span><br/>                                                                                   |
| <span id="3"></span><dl> <span data-ttu-id="a73f8-175"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-175"><dt>**3**</dt></span></span> </dl>   | <span data-ttu-id="a73f8-176">Erro de memória de paridade.</span><span class="sxs-lookup"><span data-stu-id="a73f8-176">Parity Memory error.</span></span><br/>                                                                                             |
| <span id="4"></span><dl> <span data-ttu-id="a73f8-177"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-177"><dt>**4**</dt></span></span> </dl>   | <span data-ttu-id="a73f8-178">Tempo limite do barramento.</span><span class="sxs-lookup"><span data-stu-id="a73f8-178">Bus time out.</span></span><br/>                                                                                                    |
| <span id="5"></span><dl> <span data-ttu-id="a73f8-179"><dt>**05**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-179"><dt>**5**</dt></span></span> </dl>   | <span data-ttu-id="a73f8-180">Verificação de canal de e/s.</span><span class="sxs-lookup"><span data-stu-id="a73f8-180">I/O Channel Check.</span></span><br/>                                                                                               |
| <span id="6"></span><dl> <span data-ttu-id="a73f8-181"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-181"><dt>**6**</dt></span></span> </dl>   | <span data-ttu-id="a73f8-182">NMI de software.</span><span class="sxs-lookup"><span data-stu-id="a73f8-182">Software NMI.</span></span><br/>                                                                                                    |
| <span id="7"></span><dl> <span data-ttu-id="a73f8-183"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-183"><dt>**7**</dt></span></span> </dl>   | <span data-ttu-id="a73f8-184">Redimensionamento da memória de post.</span><span class="sxs-lookup"><span data-stu-id="a73f8-184">Post Memory Resize.</span></span><br/>                                                                                              |
| <span id="8"></span><dl> <span data-ttu-id="a73f8-185"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-185"><dt>**8**</dt></span></span> </dl>   | <span data-ttu-id="a73f8-186">Erro de POSTAgem.</span><span class="sxs-lookup"><span data-stu-id="a73f8-186">POST Error.</span></span><br/>                                                                                                      |
| <span id="9"></span><dl> <span data-ttu-id="a73f8-187"><dt>**9**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-187"><dt>**9**</dt></span></span> </dl>   | <span data-ttu-id="a73f8-188">Erro de paridade de PCI.</span><span class="sxs-lookup"><span data-stu-id="a73f8-188">PCI Parity Error.</span></span><br/>                                                                                                |
| <span id="10"></span><dl> <span data-ttu-id="a73f8-189"><dt>**10**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-189"><dt>**10**</dt></span></span> </dl> | <span data-ttu-id="a73f8-190">Erro do sistema PCI.</span><span class="sxs-lookup"><span data-stu-id="a73f8-190">PCI System Error.</span></span><br/>                                                                                                |
| <span id="11"></span><dl> <span data-ttu-id="a73f8-191"><dt>**11**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-191"><dt>**11**</dt></span></span> </dl> | <span data-ttu-id="a73f8-192">Falha de CPU.</span><span class="sxs-lookup"><span data-stu-id="a73f8-192">CPU Failure.</span></span><br/>                                                                                                     |
| <span id="12"></span><dl> <span data-ttu-id="a73f8-193"><dt>**12**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-193"><dt>**12**</dt></span></span> </dl> | <span data-ttu-id="a73f8-194">Tempo limite do temporizador de failsafe de EISA.</span><span class="sxs-lookup"><span data-stu-id="a73f8-194">EISA Failsafe Timer time out.</span></span><br/>                                                                                    |
| <span id="13"></span><dl> <span data-ttu-id="a73f8-195"><dt>**13**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-195"><dt>**13**</dt></span></span> </dl> | <span data-ttu-id="a73f8-196">Log de memória corrigível desabilitado.</span><span class="sxs-lookup"><span data-stu-id="a73f8-196">Correctable memory log disabled.</span></span><br/>                                                                                 |
| <span id="14"></span><dl> <span data-ttu-id="a73f8-197"><dt>**140**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-197"><dt>**14**</dt></span></span> </dl> | <span data-ttu-id="a73f8-198">Registro em log desabilitado para um tipo de evento específico.</span><span class="sxs-lookup"><span data-stu-id="a73f8-198">Logging disabled for a specific event type.</span></span> <span data-ttu-id="a73f8-199">Muitos erros do mesmo tipo recebidos em um curto período de tempo.</span><span class="sxs-lookup"><span data-stu-id="a73f8-199">Too many errors of the same type received in a short amount of time.</span></span><br/> |
| <span id="15"></span><dl> <span data-ttu-id="a73f8-200"><dt>**15**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-200"><dt>**15**</dt></span></span> </dl> | <span data-ttu-id="a73f8-201">Reservado.</span><span class="sxs-lookup"><span data-stu-id="a73f8-201">Reserved.</span></span><br/>                                                                                                        |
| <span id="16"></span><dl> <span data-ttu-id="a73f8-202"><dt>**16**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-202"><dt>**16**</dt></span></span> </dl> | <span data-ttu-id="a73f8-203">Limite do sistema excedido (por exemplo, tensão ou limite de temperatura excedido).</span><span class="sxs-lookup"><span data-stu-id="a73f8-203">System limit exceeded (for example, voltage or temperature threshold exceeded).</span></span><br/>                                  |
| <span id="17"></span><dl> <span data-ttu-id="a73f8-204"><dt>**16**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-204"><dt>**17**</dt></span></span> </dl> | <span data-ttu-id="a73f8-205">O temporizador de hardware assíncrono expirou e emitiu uma redefinição do sistema.</span><span class="sxs-lookup"><span data-stu-id="a73f8-205">Asynchronous hardware timer expired and issued a system reset.</span></span><br/>                                                   |
| <span id="18"></span><dl> <span data-ttu-id="a73f8-206"><dt>**anos**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-206"><dt>**18**</dt></span></span> </dl> | <span data-ttu-id="a73f8-207">Informações de configuração do sistema.</span><span class="sxs-lookup"><span data-stu-id="a73f8-207">System configuration information.</span></span><br/>                                                                                |
| <span id="19"></span><dl> <span data-ttu-id="a73f8-208"><dt>**aprimora**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-208"><dt>**19**</dt></span></span> </dl> | <span data-ttu-id="a73f8-209">Informações de disco rígido.</span><span class="sxs-lookup"><span data-stu-id="a73f8-209">Hard disk information.</span></span><br/>                                                                                           |
| <span id="20"></span><dl> <span data-ttu-id="a73f8-210"><dt>**20,00**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-210"><dt>**20**</dt></span></span> </dl> | <span data-ttu-id="a73f8-211">Sistema reconfigurado.</span><span class="sxs-lookup"><span data-stu-id="a73f8-211">System reconfigured.</span></span><br/>                                                                                             |
| <span id="21"></span><dl> <span data-ttu-id="a73f8-212"><dt>**Abril**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-212"><dt>**21**</dt></span></span> </dl> | <span data-ttu-id="a73f8-213">Erro complexo de CPU incorrigível.</span><span class="sxs-lookup"><span data-stu-id="a73f8-213">Uncorrectable CPU-complex error.</span></span><br/>                                                                                 |
| <span id="22"></span><dl> <span data-ttu-id="a73f8-214"><dt>**22**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-214"><dt>**22**</dt></span></span> </dl> | <span data-ttu-id="a73f8-215">Redefinição da área de log ou desmarcada.</span><span class="sxs-lookup"><span data-stu-id="a73f8-215">Log Area Reset or Cleared.</span></span><br/>                                                                                       |
| <span id="23"></span><dl> <span data-ttu-id="a73f8-216"><dt>**23**</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-216"><dt>**23**</dt></span></span> </dl> | <span data-ttu-id="a73f8-217">Inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="a73f8-217">System boot.</span></span> <span data-ttu-id="a73f8-218">Se implementada, é garantido que essa entrada de log seja a primeira escrita em qualquer inicialização do sistema.</span><span class="sxs-lookup"><span data-stu-id="a73f8-218">If implemented, this log entry is guaranteed to be the first one written on any system boot.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="a73f8-219">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a73f8-219">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73f8-220">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a73f8-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a73f8-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a73f8-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a73f8-222">Tipo de mensagem de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="a73f8-222">Type of event log message.</span></span> <span data-ttu-id="a73f8-223">Essas mensagens correspondem aos códigos de mensagem de log de eventos usados para inserir mensagens de log de eventos pelo provedor de consumidor do log de eventos do Windows quando ele recebe um dos eventos.</span><span class="sxs-lookup"><span data-stu-id="a73f8-223">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="a73f8-224">**BITS de validação \_**</span><span class="sxs-lookup"><span data-stu-id="a73f8-224">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a73f8-225">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a73f8-225">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a73f8-226">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a73f8-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a73f8-227">Bits de validação usados para indicar a validade dos campos subsequentes.</span><span class="sxs-lookup"><span data-stu-id="a73f8-227">Validation bits used to indicate the validity of the subsequent fields.</span></span> <span data-ttu-id="a73f8-228">Um valor de 1 (0x1) significa que o **\_ evento SMBIOS** é válido.</span><span class="sxs-lookup"><span data-stu-id="a73f8-228">A value of 1 (0x1) means that the **SMBIOS\_EVENT** is valid.</span></span>

<span data-ttu-id="a73f8-229">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a73f8-229">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a73f8-230">Comentários</span><span class="sxs-lookup"><span data-stu-id="a73f8-230">Remarks</span></span>

<span data-ttu-id="a73f8-231">A classe **MSMCAEvent \_ SMBIOSError** é derivada de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="a73f8-231">The **MSMCAEvent\_SMBIOSError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a73f8-232">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a73f8-232">Requirements</span></span>



| <span data-ttu-id="a73f8-233">Requisito</span><span class="sxs-lookup"><span data-stu-id="a73f8-233">Requirement</span></span> | <span data-ttu-id="a73f8-234">Valor</span><span class="sxs-lookup"><span data-stu-id="a73f8-234">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a73f8-235">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a73f8-235">Minimum supported client</span></span><br/> | <span data-ttu-id="a73f8-236">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a73f8-236">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="a73f8-237">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a73f8-237">Minimum supported server</span></span><br/> | <span data-ttu-id="a73f8-238">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a73f8-238">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="a73f8-239">Namespace</span><span class="sxs-lookup"><span data-stu-id="a73f8-239">Namespace</span></span><br/>                | <span data-ttu-id="a73f8-240">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="a73f8-240">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="a73f8-241">MOF</span><span class="sxs-lookup"><span data-stu-id="a73f8-241">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a73f8-242"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-242"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="a73f8-243">DLL</span><span class="sxs-lookup"><span data-stu-id="a73f8-243">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a73f8-244"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a73f8-244"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a73f8-245">Confira também</span><span class="sxs-lookup"><span data-stu-id="a73f8-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a73f8-246">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="a73f8-246">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="a73f8-247">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="a73f8-247">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

