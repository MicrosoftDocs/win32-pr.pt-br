---
description: Representa o status dos recursos opcionais que estão presentes no sistema operacional.
ms.assetid: 3ac0c227-dfe1-4f33-b3d1-bcd1309c3635
ms.tgt_platform: multiple
title: classe Win32_OptionalFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OptionalFeature
- Win32_OptionalFeature.Description
- Win32_OptionalFeature.InstallDate
- Win32_OptionalFeature.Status
- Win32_OptionalFeature.Caption
- Win32_OptionalFeature.Name
- Win32_OptionalFeature.InstallState
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ee0a8fc631430401328170f15c0dd2653d0ce8b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753800"
---
# <a name="win32_optionalfeature-class"></a><span data-ttu-id="9093a-103">\_Classe Win32 OptionalFeature</span><span class="sxs-lookup"><span data-stu-id="9093a-103">Win32\_OptionalFeature class</span></span>

<span data-ttu-id="9093a-104">Representa o status dos recursos opcionais que estão presentes no sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="9093a-104">Represents the status of the optional features that are present on the operating system.</span></span>

<span data-ttu-id="9093a-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9093a-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9093a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9093a-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0827250D-BA3E-11d2-B361-00105A1F77A2}"), AMENDMENT]
class Win32_OptionalFeature : CIM_LogicalElement
{
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Caption;
  string   Name;
  uint32   InstallState;
};
```

## <a name="members"></a><span data-ttu-id="9093a-107">Membros</span><span class="sxs-lookup"><span data-stu-id="9093a-107">Members</span></span>

<span data-ttu-id="9093a-108">A classe **Win32 \_ OptionalFeature** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9093a-108">The **Win32\_OptionalFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="9093a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9093a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9093a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9093a-110">Properties</span></span>

<span data-ttu-id="9093a-111">A classe **Win32 \_ OptionalFeature** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9093a-111">The **Win32\_OptionalFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9093a-112">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="9093a-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9093a-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9093a-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9093a-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9093a-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9093a-115">Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) (legenda), [**maxlen**](../wmisdk/standard-qualifiers.md) (260)</span><span class="sxs-lookup"><span data-stu-id="9093a-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Caption), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span></span>
</dt> </dl>

<span data-ttu-id="9093a-116">Um nome de exibição de recurso opcional.</span><span class="sxs-lookup"><span data-stu-id="9093a-116">An optional feature display name.</span></span>

</dd> <dt>

<span data-ttu-id="9093a-117">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9093a-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9093a-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9093a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9093a-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9093a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9093a-120">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="9093a-120">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="9093a-121">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9093a-121">A textual description of the object.</span></span>

<span data-ttu-id="9093a-122">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9093a-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9093a-123">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="9093a-123">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9093a-124">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="9093a-124">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="9093a-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9093a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9093a-126">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="9093a-126">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="9093a-127">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="9093a-127">Indicates when the object was installed.</span></span> <span data-ttu-id="9093a-128">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="9093a-128">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="9093a-129">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9093a-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="9093a-130">**InstallState**</span><span class="sxs-lookup"><span data-stu-id="9093a-130">**InstallState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9093a-131">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9093a-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9093a-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9093a-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9093a-133">Identifica o estado do recurso opcional.</span><span class="sxs-lookup"><span data-stu-id="9093a-133">Identifies the state of the optional feature.</span></span> <span data-ttu-id="9093a-134">Os seguintes Estados são possíveis:</span><span class="sxs-lookup"><span data-stu-id="9093a-134">The following states are possible:</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="9093a-135">**Habilitado** (1)</span><span class="sxs-lookup"><span data-stu-id="9093a-135">**Enabled** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="9093a-136">**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="9093a-136">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Absent"></span><span id="absent"></span><span id="ABSENT"></span>

<span data-ttu-id="9093a-137">**Ausente** (3)</span><span class="sxs-lookup"><span data-stu-id="9093a-137">**Absent** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9093a-138">**Desconhecido** (4)</span><span class="sxs-lookup"><span data-stu-id="9093a-138">**Unknown** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="9093a-139">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9093a-139">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9093a-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9093a-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9093a-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9093a-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9093a-142">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) (Name), [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (260)</span><span class="sxs-lookup"><span data-stu-id="9093a-142">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Name), [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (260)</span></span>
</dt> </dl>

<span data-ttu-id="9093a-143">Representa o nome do recurso opcional.</span><span class="sxs-lookup"><span data-stu-id="9093a-143">Represents the name of the optional feature.</span></span>

</dd> <dt>

<span data-ttu-id="9093a-144">**Status**</span><span class="sxs-lookup"><span data-stu-id="9093a-144">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9093a-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9093a-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9093a-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9093a-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9093a-147">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="9093a-147">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="9093a-148">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="9093a-148">String that indicates the current status of the object.</span></span> <span data-ttu-id="9093a-149">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="9093a-149">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="9093a-150">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="9093a-150">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="9093a-151">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="9093a-151">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="9093a-152">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="9093a-152">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="9093a-153">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="9093a-153">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="9093a-154">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="9093a-154">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="9093a-155">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="9093a-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="9093a-156">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="9093a-156">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="9093a-157">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="9093a-157">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="9093a-158">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="9093a-158">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="9093a-159">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="9093a-159">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="9093a-160">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="9093a-160">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="9093a-161">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="9093a-161">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="9093a-162">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="9093a-162">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="9093a-163">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="9093a-163">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="9093a-164">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="9093a-164">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="9093a-165">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="9093a-165">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="9093a-166">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="9093a-166">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="9093a-167">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="9093a-167">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="9093a-168">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="9093a-168">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="9093a-169"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9093a-169"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="9093a-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9093a-170">Requirements</span></span>



| <span data-ttu-id="9093a-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="9093a-171">Requirement</span></span> | <span data-ttu-id="9093a-172">Valor</span><span class="sxs-lookup"><span data-stu-id="9093a-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9093a-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9093a-173">Minimum supported client</span></span><br/> | <span data-ttu-id="9093a-174">Windows 7</span><span class="sxs-lookup"><span data-stu-id="9093a-174">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="9093a-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9093a-175">Minimum supported server</span></span><br/> | <span data-ttu-id="9093a-176">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9093a-176">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="9093a-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="9093a-177">Namespace</span></span><br/>                | <span data-ttu-id="9093a-178">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9093a-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9093a-179">MOF</span><span class="sxs-lookup"><span data-stu-id="9093a-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9093a-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9093a-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9093a-181">DLL</span><span class="sxs-lookup"><span data-stu-id="9093a-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9093a-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9093a-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9093a-183">Confira também</span><span class="sxs-lookup"><span data-stu-id="9093a-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9093a-184">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="9093a-184">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="9093a-185">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="9093a-185">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dt>

[<span data-ttu-id="9093a-186">Consultando o status de recursos opcionais</span><span class="sxs-lookup"><span data-stu-id="9093a-186">Querying the Status of Optional Features</span></span>](../wmisdk/querying-the-status-of-optional-features.md)
</dt> </dl>

 

 
