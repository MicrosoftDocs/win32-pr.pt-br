---
description: Representa um erro de barramento PCI de MCA (arquitetura de verificação de máquina). Essa classe está disponível somente para computadores que executam o em um sistema operacional Windows de 64 bits.
ms.assetid: d8995909-a91b-4fcc-a37f-011d8df95ce8
title: Classe MSMCAEvent_PCIBusError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_PCIBusError
- MSMCAEvent_PCIBusError.Active
- MSMCAEvent_PCIBusError.AdditionalErrors
- MSMCAEvent_PCIBusError.Cpu
- MSMCAEvent_PCIBusError.ErrorSeverity
- MSMCAEvent_PCIBusError.InstanceName
- MSMCAEvent_PCIBusError.PCI_BUS_ADDRESS
- MSMCAEvent_PCIBusError.PCI_BUS_CMD
- MSMCAEvent_PCIBusError.PCI_BUS_DATA
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_STATUS
- MSMCAEvent_PCIBusError.PCI_BUS_ERROR_TYPE
- MSMCAEvent_PCIBusError.PCI_BUS_ID_BusNumber
- MSMCAEvent_PCIBusError.PCI_BUS_ID_SegmentNumber
- MSMCAEvent_PCIBusError.PCI_BUS_REQUESTOR_ID
- MSMCAEvent_PCIBusError.PCI_BUS_RESPONDER_ID
- MSMCAEvent_PCIBusError.RawRecord
- MSMCAEvent_PCIBusError.RecordId
- MSMCAEvent_PCIBusError.Size
- MSMCAEvent_PCIBusError.Type
- MSMCAEvent_PCIBusError.VALIDATION_BITS
- MSMCAEvent_PCIBusError.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 7f2b800a07c0b979468a5df5a8be67e6adee39de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647120"
---
# <a name="msmcaevent_pcibuserror-class"></a><span data-ttu-id="0d5f2-104">\_Classe MSMCAEvent PCIBusError</span><span class="sxs-lookup"><span data-stu-id="0d5f2-104">MSMCAEvent\_PCIBusError class</span></span>

<span data-ttu-id="0d5f2-105">A classe **MSMCAEvent \_ PCIBusError** representa um erro de barramento PCI MCA (arquitetura de verificação de máquina).</span><span class="sxs-lookup"><span data-stu-id="0d5f2-105">The **MSMCAEvent\_PCIBusError** class represents a Machine Check Architecture (MCA) PCI bus error.</span></span> <span data-ttu-id="0d5f2-106">Essa classe está disponível somente para computadores que executam o em um sistema operacional Windows de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-106">This class is available only for computers running on a 64-bit Windows operating system.</span></span>

<span data-ttu-id="0d5f2-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="0d5f2-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d5f2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d5f2-109">Syntax</span></span>

``` syntax
class MSMCAEvent_PCIBusError : WMIEvent
{
  boolean Active;
  uint32  AdditionalErrors;
  uint32  Cpu;
  uint8   ErrorSeverity;
  string  InstanceName;
  uint64  PCI_BUS_ADDRESS;
  uint64  PCI_BUS_CMD;
  uint64  PCI_BUS_DATA;
  uint64  PCI_BUS_ERROR_STATUS;
  uint16  PCI_BUS_ERROR_TYPE;
  uint8   PCI_BUS_ID_BusNumber;
  uint8   PCI_BUS_ID_SegmentNumber;
  uint64  PCI_BUS_REQUESTOR_ID;
  uint64  PCI_BUS_RESPONDER_ID;
  uint8   RawRecord[];
  uint64  RecordId;
  uint32  Size;
  uint32  Type;
  uint64  VALIDATION_BITS;
  uint32  LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="0d5f2-110">Membros</span><span class="sxs-lookup"><span data-stu-id="0d5f2-110">Members</span></span>

<span data-ttu-id="0d5f2-111">A classe **MSMCAEvent \_ PCIBusError** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0d5f2-111">The **MSMCAEvent\_PCIBusError** class has these types of members:</span></span>

-   [<span data-ttu-id="0d5f2-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d5f2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0d5f2-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0d5f2-113">Properties</span></span>

<span data-ttu-id="0d5f2-114">A classe **MSMCAEvent \_ PCIBusError** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-114">The **MSMCAEvent\_PCIBusError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0d5f2-115">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-115">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-116">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-116">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-118">**True**, se esta instância da classe estiver ativa; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-118">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-119">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-119">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-122">Número de erros adicionais no registro.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-122">Number of additional errors in the record.</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-123">**CPUs**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-123">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-124">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-126">CPU que relatou o erro.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-126">CPU that reported the error.</span></span> <span data-ttu-id="0d5f2-127">Essa propriedade se aplica somente a um sistema multiprocessador no qual o primeiro processador recebe o número 0, o segundo processador recebe o número 1 e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-127">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-128">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-128">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-129">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-129">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-131">Nível de severidade do erro relatado.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-131">Severity level of the error reported.</span></span>



| <span data-ttu-id="0d5f2-132">Valor</span><span class="sxs-lookup"><span data-stu-id="0d5f2-132">Value</span></span>                                                                                                | <span data-ttu-id="0d5f2-133">Significado</span><span class="sxs-lookup"><span data-stu-id="0d5f2-133">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="0d5f2-134"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-134"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="0d5f2-135">Recuperado</span><span class="sxs-lookup"><span data-stu-id="0d5f2-135">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="0d5f2-136"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-136"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="0d5f2-137">Fatais</span><span class="sxs-lookup"><span data-stu-id="0d5f2-137">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="0d5f2-138"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-138"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="0d5f2-139">Corrigível</span><span class="sxs-lookup"><span data-stu-id="0d5f2-139">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="0d5f2-140">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-140">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-143">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="0d5f2-143">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-144">Identificador exclusivo desta instância da classe.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-144">Unique identifier of this instance of the class.</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-145">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-145">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-146">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-146">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-148">Se for 0 (zero), esse evento não será registrado no log de eventos do sistema.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-148">If 0 (zero), then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-149">**\_endereço de barramento PCI \_**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-149">**PCI\_BUS\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-150">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-152">Memória ou endereço de e/s no barramento PCI no momento do evento.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-152">Memory or I/O address on the PCI bus at the time of the event.</span></span>

<span data-ttu-id="0d5f2-153">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d5f2-153">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-154">**\_cmd de barramento PCI \_**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-154">**PCI\_BUS\_CMD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-155">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-155">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-157">Comando ou operação de barramento no momento do evento.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-157">Bus command or operation at the time of the event.</span></span>

<span data-ttu-id="0d5f2-158">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d5f2-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-159">**\_dados de barramento PCI \_**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-159">**PCI\_BUS\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-160">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-160">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-162">Dados no barramento PCI no momento do evento.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-162">Data on the PCI bus at the time of the event.</span></span>

<span data-ttu-id="0d5f2-163">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d5f2-163">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-164">**\_status de \_ erro do barramento PCI \_**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-164">**PCI\_BUS\_ERROR\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-165">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-165">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-167">Status do barramento no momento do erro.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-167">Bus status at the time of the error.</span></span>

<span data-ttu-id="0d5f2-168">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d5f2-168">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-169">**\_tipo de \_ erro do barramento PCI \_**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-169">**PCI\_BUS\_ERROR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-170">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-172">Tipo de erro de barramento PCI.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-172">Type of PCI bus error.</span></span>



| <span data-ttu-id="0d5f2-173">Valor</span><span class="sxs-lookup"><span data-stu-id="0d5f2-173">Value</span></span>                                                                                                | <span data-ttu-id="0d5f2-174">Significado</span><span class="sxs-lookup"><span data-stu-id="0d5f2-174">Meaning</span></span>                                                     |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="0"></span><dl> <span data-ttu-id="0d5f2-175"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-175"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="0d5f2-176">Erro desconhecido ou específico do sistema OEM.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-176">Unknown or OEM System Specific Error.</span></span><br/>            |
| <span id="1"></span><dl> <span data-ttu-id="0d5f2-177"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-177"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="0d5f2-178">Erro de paridade de dados.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-178">Data Parity Error.</span></span><br/>                               |
| <span id="2"></span><dl> <span data-ttu-id="0d5f2-179"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-179"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="0d5f2-180">Erro do sistema.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-180">System Error.</span></span><br/>                                    |
| <span id="3"></span><dl> <span data-ttu-id="0d5f2-181"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-181"><dt>**3**</dt></span></span> </dl> | <span data-ttu-id="0d5f2-182">Anulação mestre.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-182">Master Abort.</span></span><br/>                                    |
| <span id="4"></span><dl> <span data-ttu-id="0d5f2-183"><dt>**quatro**</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-183"><dt>**4**</dt></span></span> </dl> | <span data-ttu-id="0d5f2-184">Tempo limite de barramento ou nenhum dispositivo presente (sem DEVSEL \# ).</span><span class="sxs-lookup"><span data-stu-id="0d5f2-184">Bus Time Out or No Device Present (NO DEVSEL\#).</span></span><br/> |
| <span id="5"></span><dl> <span data-ttu-id="0d5f2-185"><dt>**05**</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-185"><dt>**5**</dt></span></span> </dl> | <span data-ttu-id="0d5f2-186">Erro de paridade de dados mestre.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-186">Master Data Parity Error.</span></span><br/>                        |
| <span id="6"></span><dl> <span data-ttu-id="0d5f2-187"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-187"><dt>**6**</dt></span></span> </dl> | <span data-ttu-id="0d5f2-188">Erro de paridade de endereço.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-188">Address Parity Error.</span></span><br/>                            |
| <span id="7"></span><dl> <span data-ttu-id="0d5f2-189"><dt>**7**</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-189"><dt>**7**</dt></span></span> </dl> | <span data-ttu-id="0d5f2-190">Erro de paridade de comando.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-190">Command Parity Error.</span></span><br/>                            |



 

</dd> <dt>

<span data-ttu-id="0d5f2-191">**\_ID do barramento PCI \_ \_ BusNumber**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-191">**PCI\_BUS\_ID\_BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-192">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-192">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-193">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-194">Identificador designado para o barramento PCI que encontrou o erro.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-194">Designated identifier for the PCI bus that encountered the error.</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-195">**\_ID do barramento PCI \_ \_ SegmentNumber**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-195">**PCI\_BUS\_ID\_SegmentNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-196">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-196">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-198">Identificador de segmento designado para o barramento PCI que encontrou o erro.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-198">Designated segment identifier for the PCI bus that encountered the error.</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-199">**\_ID do \_ solicitante do barramento PCI \_**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-199">**PCI\_BUS\_REQUESTOR\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-200">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-200">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-202">Identificador do solicitante de barramento PCI no momento do evento.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-202">PCI Bus requestor identifier at the time of the event.</span></span>

<span data-ttu-id="0d5f2-203">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d5f2-203">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-204">**\_ID do \_ respondente do barramento PCI \_**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-204">**PCI\_BUS\_RESPONDER\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-205">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-205">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-207">Identificador de respondente do barramento PCI no momento do evento.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-207">PCI Bus Responder identifier at the time of the event.</span></span>

<span data-ttu-id="0d5f2-208">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d5f2-208">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-209">**RawRecord**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-209">**RawRecord**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-210">Tipo de dados: matriz **uint8**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-210">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-211">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-212">Matriz de bytes que contém o registro de erro bruto conforme apresentado ao Windows pela camada de abstração do sistema (SAL).</span><span class="sxs-lookup"><span data-stu-id="0d5f2-212">Array of bytes that contains the raw error record as presented to Windows by the system abstraction layer (SAL).</span></span> <span data-ttu-id="0d5f2-213">O número de elementos na matriz é especificado pela propriedade **size** .</span><span class="sxs-lookup"><span data-stu-id="0d5f2-213">The number of elements in the array is specified by the **Size** property.</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-214">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-214">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-215">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-215">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-216">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-217">Identificador de registro do registro de erro para este erro.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-217">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="0d5f2-218">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d5f2-218">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-219">**Tamanho**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-219">**Size**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-220">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-222">Tamanho do registro de erro bruto.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-222">Size of the raw error record.</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-223">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-223">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-224">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-226">Tipo de mensagem de log de eventos.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-226">Type of event log message.</span></span> <span data-ttu-id="0d5f2-227">Essas mensagens correspondem aos códigos de mensagem de log de eventos usados para inserir mensagens de log de eventos pelo provedor de consumidor do log de eventos do Windows quando ele recebe um dos eventos.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-227">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> <dt>

<span data-ttu-id="0d5f2-228">**BITS de validação \_**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-228">**VALIDATION\_BITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0d5f2-229">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-229">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="0d5f2-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0d5f2-230">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0d5f2-231">Bits de validação usados para indicar a validade dos campos subsequentes.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-231">Validation bits used to indicate the validity of the subsequent fields.</span></span>



| <span data-ttu-id="0d5f2-232">Valores</span><span class="sxs-lookup"><span data-stu-id="0d5f2-232">Values</span></span>                                                                                  | <span data-ttu-id="0d5f2-233">Significado</span><span class="sxs-lookup"><span data-stu-id="0d5f2-233">Meaning</span></span>                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="0d5f2-234"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-234"><dt>1 (0x1)</dt></span></span> </dl>      | <span data-ttu-id="0d5f2-235">O \_ status de erro do barramento PCI \_ \_ é válido.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-235">PCI\_BUS\_ERROR\_STATUS is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="0d5f2-236"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-236"><dt>2 (0x2)</dt></span></span> </dl>      | <span data-ttu-id="0d5f2-237">O \_ tipo de erro do barramento PCI \_ \_ é válido.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-237">PCI\_BUS\_ERROR\_TYPE is valid.</span></span><br/>       |
| <dl> <span data-ttu-id="0d5f2-238"><dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-238"><dt>4 (0x4)</dt></span></span> </dl>      | <span data-ttu-id="0d5f2-239">A \_ ID do barramento PCI \_ é válida.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-239">PCI\_BUS\_ID is valid.</span></span><br/>                |
| <dl> <span data-ttu-id="0d5f2-240"><dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-240"><dt>8 (0x8)</dt></span></span> </dl>      | <span data-ttu-id="0d5f2-241">O \_ endereço de barramento PCI \_ é válido.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-241">PCI\_BUS\_ADDRESS is valid.</span></span><br/>           |
| <dl> <span data-ttu-id="0d5f2-242"><dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-242"><dt>16 (0x10)</dt></span></span> </dl>    | <span data-ttu-id="0d5f2-243">\_Os dados do barramento PCI \_ são válidos.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-243">PCI\_BUS\_DATA is valid.</span></span><br/>              |
| <dl> <span data-ttu-id="0d5f2-244"><dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-244"><dt>32 (0x20)</dt></span></span> </dl>    | <span data-ttu-id="0d5f2-245">O \_ cmd de barramento PCI \_ é válido.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-245">PCI\_BUS\_CMD is valid.</span></span><br/>               |
| <dl> <span data-ttu-id="0d5f2-246"><dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-246"><dt>64 (0x40)</dt></span></span> </dl>    | <span data-ttu-id="0d5f2-247">A \_ ID do solicitante do barramento PCI \_ \_ é válida.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-247">PCI\_BUS\_REQUESTOR\_ID is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="0d5f2-248"><dt>128 (0x80)</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-248"><dt>128 (0x80)</dt></span></span> </dl>   | <span data-ttu-id="0d5f2-249">A \_ ID do respondente do barramento PCI \_ \_ é válida.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-249">PCI\_BUS\_RESPONDER\_ID is valid.</span></span><br/>     |
| <dl> <span data-ttu-id="0d5f2-250"><dt>256 (0x100)</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-250"><dt>256 (0x100)</dt></span></span> </dl>  | <span data-ttu-id="0d5f2-251">A \_ ID de destino do barramento PCI \_ \_ é válida.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-251">PCI\_BUS\_TARGET\_ID is valid.</span></span><br/>        |
| <dl> <span data-ttu-id="0d5f2-252"><dt>512 (0x200)</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-252"><dt>512 (0x200)</dt></span></span> </dl>  | <span data-ttu-id="0d5f2-253">A \_ ID OEM do barramento PCI \_ \_ é válida.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-253">PCI\_BUS\_OEM\_ID is valid.</span></span><br/>           |
| <dl> <span data-ttu-id="0d5f2-254"><dt>1024 (0x400)</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-254"><dt>1024 (0x400)</dt></span></span> </dl> | <span data-ttu-id="0d5f2-255">O \_ struct de dados OEM do barramento PCI \_ \_ \_ é válido.</span><span class="sxs-lookup"><span data-stu-id="0d5f2-255">PCI\_BUS\_OEM\_DATA\_STRUCT is valid.</span></span><br/> |



 

<span data-ttu-id="0d5f2-256">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0d5f2-256">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d5f2-257">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d5f2-257">Remarks</span></span>

<span data-ttu-id="0d5f2-258">A classe **MSMCAEvent \_ PCIBusError** é derivada de [**WmiEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="0d5f2-258">The **MSMCAEvent\_PCIBusError** class is derived from [**WMIEvent**](wmievent.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d5f2-259">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d5f2-259">Requirements</span></span>



| <span data-ttu-id="0d5f2-260">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d5f2-260">Requirement</span></span> | <span data-ttu-id="0d5f2-261">Valor</span><span class="sxs-lookup"><span data-stu-id="0d5f2-261">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d5f2-262">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d5f2-262">Minimum supported client</span></span><br/> | <span data-ttu-id="0d5f2-263">Windows XP</span><span class="sxs-lookup"><span data-stu-id="0d5f2-263">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="0d5f2-264">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0d5f2-264">Minimum supported server</span></span><br/> | <span data-ttu-id="0d5f2-265">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="0d5f2-265">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="0d5f2-266">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d5f2-266">Namespace</span></span><br/>                | <span data-ttu-id="0d5f2-267">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="0d5f2-267">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="0d5f2-268">MOF</span><span class="sxs-lookup"><span data-stu-id="0d5f2-268">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0d5f2-269"><dt>Wmicore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-269"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="0d5f2-270">DLL</span><span class="sxs-lookup"><span data-stu-id="0d5f2-270">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d5f2-271"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d5f2-271"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d5f2-272">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d5f2-272">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d5f2-273">Classes MSMCA</span><span class="sxs-lookup"><span data-stu-id="0d5f2-273">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="0d5f2-274">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="0d5f2-274">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

