---
description: O registro do Win32 \_&\# 8194; A classe WMI representa o registro do sistema em um sistema de computador executando o Windows.
ms.assetid: 4a6cd7d7-2845-434d-b024-d6dbb77371ea
ms.tgt_platform: multiple
title: Classe Win32_Registry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Registry
- Win32_Registry.Caption
- Win32_Registry.Description
- Win32_Registry.InstallDate
- Win32_Registry.Status
- Win32_Registry.CurrentSize
- Win32_Registry.MaximumSize
- Win32_Registry.Name
- Win32_Registry.ProposedSize
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a1dc5fd89ee589aabda5da5f97632d86b39f6beb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920204"
---
# <a name="win32_registry-class"></a><span data-ttu-id="211c3-103">\_Classe de Registro Win32</span><span class="sxs-lookup"><span data-stu-id="211c3-103">Win32\_Registry class</span></span>

<span data-ttu-id="211c3-104">A  [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ registro do Win32** representa o registro do sistema em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="211c3-104">The **Win32\_Registry** [WMI class](../wmisdk/retrieving-a-class.md) represents the system registry on a computer system running Windows.</span></span>

<span data-ttu-id="211c3-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="211c3-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="211c3-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="211c3-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="211c3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="211c3-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Registry : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  uint32   CurrentSize;
  uint32   MaximumSize;
  string   Name;
  uint32   ProposedSize;
};
```

## <a name="members"></a><span data-ttu-id="211c3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="211c3-108">Members</span></span>

<span data-ttu-id="211c3-109">A classe de **\_ registro do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="211c3-109">The **Win32\_Registry** class has these types of members:</span></span>

-   [<span data-ttu-id="211c3-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="211c3-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="211c3-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="211c3-111">Properties</span></span>

<span data-ttu-id="211c3-112">A classe de **\_ registro do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="211c3-112">The **Win32\_Registry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="211c3-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="211c3-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211c3-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="211c3-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="211c3-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="211c3-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="211c3-116">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="211c3-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="211c3-117">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="211c3-117">A short textual description of the object.</span></span>

<span data-ttu-id="211c3-118">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="211c3-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="211c3-119">**CurrentSize**</span><span class="sxs-lookup"><span data-stu-id="211c3-119">**CurrentSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211c3-120">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="211c3-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="211c3-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="211c3-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="211c3-122">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \|NTDLL.DLL\| [**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation) \| SystemRegistryQuotaInformation"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="211c3-122">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|NTDLL.DLL\|[**NtQuerySystemInformation**](/windows/win32/api/winternl/nf-winternl-ntquerysysteminformation)\|SystemRegistryQuotaInformation"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="211c3-123">Tamanho físico atual do registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="211c3-123">Current physical size of the Windows registry.</span></span>

<span data-ttu-id="211c3-124">Exemplo: 10</span><span class="sxs-lookup"><span data-stu-id="211c3-124">Example: 10</span></span>

</dd> <dt>

<span data-ttu-id="211c3-125">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="211c3-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211c3-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="211c3-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="211c3-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="211c3-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="211c3-128">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="211c3-128">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="211c3-129">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="211c3-129">A textual description of the object.</span></span>

<span data-ttu-id="211c3-130">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="211c3-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="211c3-131">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="211c3-131">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211c3-132">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="211c3-132">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="211c3-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="211c3-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="211c3-134">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="211c3-134">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="211c3-135">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="211c3-135">Indicates when the object was installed.</span></span> <span data-ttu-id="211c3-136">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="211c3-136">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="211c3-137">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="211c3-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="211c3-138">**MaximumSize**</span><span class="sxs-lookup"><span data-stu-id="211c3-138">**MaximumSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211c3-139">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="211c3-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="211c3-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="211c3-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="211c3-141">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \| RegistrySizeLimit"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="211c3-141">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\|RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="211c3-142">Tamanho máximo do registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="211c3-142">Maximum size of the Windows registry.</span></span> <span data-ttu-id="211c3-143">Se o sistema for bem-sucedido ao usar a propriedade **proposedSize** , **MaximumSize** deverá conter o mesmo valor.</span><span class="sxs-lookup"><span data-stu-id="211c3-143">If the system is successful in using the **ProposedSize** property, **MaximumSize** should contain the same value.</span></span>

</dd> <dt>

<span data-ttu-id="211c3-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="211c3-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211c3-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="211c3-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="211c3-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="211c3-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="211c3-147">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span><span class="sxs-lookup"><span data-stu-id="211c3-147">Qualifiers: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Name"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry")</span></span>
</dt> </dl>

<span data-ttu-id="211c3-148">Nome do registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="211c3-148">Name of the Windows registry.</span></span> <span data-ttu-id="211c3-149">O tamanho máximo é de 256 caracteres.</span><span class="sxs-lookup"><span data-stu-id="211c3-149">The maximum length is 256 characters.</span></span>

</dd> <dt>

<span data-ttu-id="211c3-150">**ProposedSize**</span><span class="sxs-lookup"><span data-stu-id="211c3-150">**ProposedSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211c3-151">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="211c3-151">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="211c3-152">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="211c3-152">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="211c3-153">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \| RegistrySizeLimit"), [**unidades**](../wmisdk/standard-qualifiers.md) ("megabytes")</span><span class="sxs-lookup"><span data-stu-id="211c3-153">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|SYSTEM\\\\CurrentControlSet\\\\Control\|RegistrySizeLimit"), [**Units**](../wmisdk/standard-qualifiers.md) ("megabytes")</span></span>
</dt> </dl>

<span data-ttu-id="211c3-154">Tamanho proposto do registro do Windows.</span><span class="sxs-lookup"><span data-stu-id="211c3-154">Proposed size of the Windows registry.</span></span> <span data-ttu-id="211c3-155">É a única configuração do registro que pode ser modificada e sua proposta é tentada na próxima vez em que o sistema for inicializado.</span><span class="sxs-lookup"><span data-stu-id="211c3-155">It is the only registry setting that can be modified, and its proposal is attempted the next time the system boots.</span></span>

</dd> <dt>

<span data-ttu-id="211c3-156">**Status**</span><span class="sxs-lookup"><span data-stu-id="211c3-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="211c3-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="211c3-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="211c3-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="211c3-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="211c3-159">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="211c3-159">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="211c3-160">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="211c3-160">String that indicates the current status of the object.</span></span> <span data-ttu-id="211c3-161">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="211c3-161">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="211c3-162">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="211c3-162">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="211c3-163">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="211c3-163">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="211c3-164">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="211c3-164">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="211c3-165">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="211c3-165">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="211c3-166">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="211c3-166">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="211c3-167">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="211c3-167">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="211c3-168">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="211c3-168">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="211c3-169">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="211c3-169">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="211c3-170">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="211c3-170">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="211c3-171">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="211c3-171">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="211c3-172">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="211c3-172">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="211c3-173">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="211c3-173">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="211c3-174">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="211c3-174">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="211c3-175">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="211c3-175">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="211c3-176">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="211c3-176">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="211c3-177">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="211c3-177">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="211c3-178">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="211c3-178">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="211c3-179">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="211c3-179">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="211c3-180">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="211c3-180">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="211c3-181"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="211c3-181"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="211c3-182">Comentários</span><span class="sxs-lookup"><span data-stu-id="211c3-182">Remarks</span></span>

<span data-ttu-id="211c3-183">A classe de **\_ registro do Win32** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="211c3-183">The **Win32\_Registry** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="211c3-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="211c3-184">Requirements</span></span>



| <span data-ttu-id="211c3-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="211c3-185">Requirement</span></span> | <span data-ttu-id="211c3-186">Valor</span><span class="sxs-lookup"><span data-stu-id="211c3-186">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="211c3-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="211c3-187">Minimum supported client</span></span><br/> | <span data-ttu-id="211c3-188">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="211c3-188">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="211c3-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="211c3-189">Minimum supported server</span></span><br/> | <span data-ttu-id="211c3-190">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="211c3-190">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="211c3-191">Namespace</span><span class="sxs-lookup"><span data-stu-id="211c3-191">Namespace</span></span><br/>                | <span data-ttu-id="211c3-192">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="211c3-192">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="211c3-193">MOF</span><span class="sxs-lookup"><span data-stu-id="211c3-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="211c3-194"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="211c3-194"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="211c3-195">DLL</span><span class="sxs-lookup"><span data-stu-id="211c3-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="211c3-196"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="211c3-196"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="211c3-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="211c3-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="211c3-198">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="211c3-198">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="211c3-199">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="211c3-199">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
