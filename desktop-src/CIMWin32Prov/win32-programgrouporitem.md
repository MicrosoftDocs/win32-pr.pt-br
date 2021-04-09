---
description: A \_ classe WMI abstrata do Win32 ProgramGroupOrItem representa um agrupamento lógico de programas no menu iniciar programas do usuário \\ . Ele contém grupos de programas e itens de grupo de programas.
ms.assetid: 48ec5436-e931-4f00-ab36-03b04ad33529
ms.tgt_platform: multiple
title: Classe Win32_ProgramGroupOrItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ProgramGroupOrItem
- Win32_ProgramGroupOrItem.Caption
- Win32_ProgramGroupOrItem.Description
- Win32_ProgramGroupOrItem.InstallDate
- Win32_ProgramGroupOrItem.Name
- Win32_ProgramGroupOrItem.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb12576acbc8b50befa5d0856343b61e325b9478
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088967"
---
# <a name="win32_programgrouporitem-class"></a><span data-ttu-id="68065-104">\_Classe Win32 ProgramGroupOrItem</span><span class="sxs-lookup"><span data-stu-id="68065-104">Win32\_ProgramGroupOrItem class</span></span>

<span data-ttu-id="68065-105">A [classe WMI](../wmisdk/retrieving-a-class.md) abstrata do **Win32 \_ ProgramGroupOrItem** representa um agrupamento lógico de programas no menu **Iniciar \\ programas** do usuário.</span><span class="sxs-lookup"><span data-stu-id="68065-105">The **Win32\_ProgramGroupOrItem** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents a logical grouping of programs on the user's **Start\\Programs** menu.</span></span> <span data-ttu-id="68065-106">Ele contém grupos de programas e itens de grupo de programas.</span><span class="sxs-lookup"><span data-stu-id="68065-106">It contains program groups and program group items.</span></span>

<span data-ttu-id="68065-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="68065-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="68065-108">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="68065-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="68065-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68065-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{86E30E86-7DB2-11d2-90CB-0060081A46FD}"), AMENDMENT]
class Win32_ProgramGroupOrItem : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="68065-110">Membros</span><span class="sxs-lookup"><span data-stu-id="68065-110">Members</span></span>

<span data-ttu-id="68065-111">A classe **Win32 \_ ProgramGroupOrItem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="68065-111">The **Win32\_ProgramGroupOrItem** class has these types of members:</span></span>

-   [<span data-ttu-id="68065-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="68065-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="68065-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="68065-113">Properties</span></span>

<span data-ttu-id="68065-114">A classe **Win32 \_ ProgramGroupOrItem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="68065-114">The **Win32\_ProgramGroupOrItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68065-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="68065-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68065-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68065-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68065-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68065-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68065-118">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="68065-118">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="68065-119">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="68065-119">A short textual description of the object.</span></span>

<span data-ttu-id="68065-120">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68065-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68065-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="68065-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68065-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68065-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68065-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68065-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68065-124">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="68065-124">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="68065-125">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="68065-125">A textual description of the object.</span></span>

<span data-ttu-id="68065-126">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68065-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68065-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="68065-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68065-128">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="68065-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="68065-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68065-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68065-130">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="68065-130">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="68065-131">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="68065-131">Indicates when the object was installed.</span></span> <span data-ttu-id="68065-132">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="68065-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="68065-133">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68065-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68065-134">**Nome**</span><span class="sxs-lookup"><span data-stu-id="68065-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68065-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68065-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68065-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68065-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68065-137">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="68065-137">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="68065-138">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="68065-138">Label by which the object is known.</span></span> <span data-ttu-id="68065-139">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="68065-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="68065-140">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68065-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="68065-141">**Status**</span><span class="sxs-lookup"><span data-stu-id="68065-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68065-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="68065-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68065-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="68065-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68065-144">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="68065-144">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="68065-145">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="68065-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="68065-146">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="68065-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="68065-147">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="68065-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="68065-148">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="68065-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="68065-149">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="68065-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="68065-150">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="68065-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="68065-151">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="68065-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="68065-152">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="68065-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="68065-153">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="68065-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="68065-154">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="68065-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="68065-155">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="68065-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="68065-156">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="68065-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="68065-157">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="68065-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="68065-158">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="68065-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="68065-159">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="68065-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="68065-160">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="68065-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="68065-161">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="68065-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="68065-162">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="68065-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="68065-163">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="68065-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="68065-164">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="68065-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="68065-165">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="68065-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="68065-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="68065-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="68065-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="68065-167">Remarks</span></span>

<span data-ttu-id="68065-168">A classe **Win32 \_ ProgramGroupOrItem** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="68065-168">The **Win32\_ProgramGroupOrItem** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68065-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68065-169">Requirements</span></span>



| <span data-ttu-id="68065-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="68065-170">Requirement</span></span> | <span data-ttu-id="68065-171">Valor</span><span class="sxs-lookup"><span data-stu-id="68065-171">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="68065-172">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68065-172">Minimum supported client</span></span><br/> | <span data-ttu-id="68065-173">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68065-173">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="68065-174">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="68065-174">Minimum supported server</span></span><br/> | <span data-ttu-id="68065-175">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68065-175">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="68065-176">Namespace</span><span class="sxs-lookup"><span data-stu-id="68065-176">Namespace</span></span><br/>                | <span data-ttu-id="68065-177">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="68065-177">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="68065-178">MOF</span><span class="sxs-lookup"><span data-stu-id="68065-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68065-179"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68065-179"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="68065-180">DLL</span><span class="sxs-lookup"><span data-stu-id="68065-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68065-181"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68065-181"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68065-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="68065-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68065-183">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="68065-183">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dt>

[<span data-ttu-id="68065-184">Classes do sistema operacional</span><span class="sxs-lookup"><span data-stu-id="68065-184">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
