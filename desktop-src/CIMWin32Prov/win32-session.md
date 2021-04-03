---
description: A classe de sessão do Win32 \_ define informações de estado sobre a interação entre um usuário e um recurso, como um sistema de computador ou uma sessão de terminal.
ms.assetid: 0649001a-914f-403f-9aee-0e9096392fe9
ms.tgt_platform: multiple
title: Classe Win32_Session
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Session
- Win32_Session.Caption
- Win32_Session.Description
- Win32_Session.InstallDate
- Win32_Session.Name
- Win32_Session.Status
- Win32_Session.StartTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7052eb922ec40aca214600f9389e76e5aec4609
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010114"
---
# <a name="win32_session-class"></a><span data-ttu-id="251f5-103">\_Classe de sessão Win32</span><span class="sxs-lookup"><span data-stu-id="251f5-103">Win32\_Session class</span></span>

<span data-ttu-id="251f5-104">A classe de **\_ sessão do Win32** define informações de estado sobre a interação entre um usuário e um recurso, como um sistema de computador ou uma sessão de terminal.</span><span class="sxs-lookup"><span data-stu-id="251f5-104">The **Win32\_Session** class defines state information about the interaction between a user and a resource, such as a computer system or a terminal session.</span></span>

<span data-ttu-id="251f5-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="251f5-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="251f5-106">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="251f5-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="251f5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="251f5-107">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_Session : CIM_logicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime StartTime;
};
```

## <a name="members"></a><span data-ttu-id="251f5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="251f5-108">Members</span></span>

<span data-ttu-id="251f5-109">A classe de **\_ sessão Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="251f5-109">The **Win32\_Session** class has these types of members:</span></span>

-   [<span data-ttu-id="251f5-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="251f5-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="251f5-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="251f5-111">Properties</span></span>

<span data-ttu-id="251f5-112">A classe de **\_ sessão Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="251f5-112">The **Win32\_Session** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="251f5-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="251f5-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="251f5-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="251f5-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="251f5-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="251f5-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="251f5-116">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="251f5-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="251f5-117">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="251f5-117">A short textual description of the object.</span></span>

<span data-ttu-id="251f5-118">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="251f5-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="251f5-119">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="251f5-119">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="251f5-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="251f5-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="251f5-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="251f5-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="251f5-122">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="251f5-122">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="251f5-123">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="251f5-123">A textual description of the object.</span></span>

<span data-ttu-id="251f5-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="251f5-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="251f5-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="251f5-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="251f5-126">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="251f5-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="251f5-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="251f5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="251f5-128">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="251f5-128">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="251f5-129">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="251f5-129">Indicates when the object was installed.</span></span> <span data-ttu-id="251f5-130">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="251f5-130">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="251f5-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="251f5-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="251f5-132">**Nome**</span><span class="sxs-lookup"><span data-stu-id="251f5-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="251f5-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="251f5-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="251f5-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="251f5-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="251f5-135">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="251f5-135">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="251f5-136">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="251f5-136">Label by which the object is known.</span></span> <span data-ttu-id="251f5-137">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="251f5-137">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="251f5-138">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="251f5-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="251f5-139">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="251f5-139">**StartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="251f5-140">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="251f5-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="251f5-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="251f5-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="251f5-142">Hora em que a sessão foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="251f5-142">Time at which the session started.</span></span>

</dd> <dt>

<span data-ttu-id="251f5-143">**Status**</span><span class="sxs-lookup"><span data-stu-id="251f5-143">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="251f5-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="251f5-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="251f5-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="251f5-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="251f5-146">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="251f5-146">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="251f5-147">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="251f5-147">String that indicates the current status of the object.</span></span> <span data-ttu-id="251f5-148">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="251f5-148">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="251f5-149">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="251f5-149">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="251f5-150">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="251f5-150">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="251f5-151">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="251f5-151">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="251f5-152">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="251f5-152">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="251f5-153">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="251f5-153">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="251f5-154">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="251f5-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="251f5-155">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="251f5-155">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="251f5-156">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="251f5-156">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="251f5-157">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="251f5-157">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="251f5-158">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="251f5-158">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="251f5-159">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="251f5-159">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="251f5-160">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="251f5-160">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="251f5-161">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="251f5-161">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="251f5-162">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="251f5-162">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="251f5-163">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="251f5-163">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="251f5-164">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="251f5-164">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="251f5-165">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="251f5-165">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="251f5-166">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="251f5-166">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="251f5-167">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="251f5-167">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="251f5-168"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="251f5-168"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="251f5-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="251f5-169">Remarks</span></span>

<span data-ttu-id="251f5-170">A classe de **\_ sessão Win32** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="251f5-170">The **Win32\_Session** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="251f5-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="251f5-171">Requirements</span></span>



| <span data-ttu-id="251f5-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="251f5-172">Requirement</span></span> | <span data-ttu-id="251f5-173">Valor</span><span class="sxs-lookup"><span data-stu-id="251f5-173">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="251f5-174">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="251f5-174">Minimum supported client</span></span><br/> | <span data-ttu-id="251f5-175">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="251f5-175">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="251f5-176">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="251f5-176">Minimum supported server</span></span><br/> | <span data-ttu-id="251f5-177">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="251f5-177">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="251f5-178">Namespace</span><span class="sxs-lookup"><span data-stu-id="251f5-178">Namespace</span></span><br/>                | <span data-ttu-id="251f5-179">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="251f5-179">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="251f5-180">MOF</span><span class="sxs-lookup"><span data-stu-id="251f5-180">MOF</span></span><br/>                      | <dl> <span data-ttu-id="251f5-181"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="251f5-181"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="251f5-182">DLL</span><span class="sxs-lookup"><span data-stu-id="251f5-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="251f5-183"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="251f5-183"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="251f5-184">Confira também</span><span class="sxs-lookup"><span data-stu-id="251f5-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="251f5-185">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="251f5-185">**CIM\_logicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

 
