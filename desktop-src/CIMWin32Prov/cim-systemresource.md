---
description: A \_ classe CIM SystemResource representa uma entidade gerenciada pelo BIOS ou um sistema operacional que está disponível para uso por software e dispositivos lógicos.
ms.assetid: f232c940-532d-4723-8e1e-09f983664b84
ms.tgt_platform: multiple
title: Classe CIM_SystemResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemResource
- CIM_SystemResource.Caption
- CIM_SystemResource.Description
- CIM_SystemResource.InstallDate
- CIM_SystemResource.Name
- CIM_SystemResource.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f0c111aa0d69119a7d9182732fb18dd5109d3dde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164085"
---
# <a name="cim_systemresource-class"></a><span data-ttu-id="b3402-103">\_Classe CIM SystemResource</span><span class="sxs-lookup"><span data-stu-id="b3402-103">CIM\_SystemResource class</span></span>

<span data-ttu-id="b3402-104">A classe **CIM \_ SystemResource** representa uma entidade gerenciada pelo BIOS ou um sistema operacional que está disponível para uso por software e dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="b3402-104">The **CIM\_SystemResource** class represents an entity managed by BIOS, or an operating system that is available for use by software and logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b3402-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b3402-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b3402-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b3402-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b3402-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b3402-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b3402-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b3402-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3402-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3402-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C519-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_SystemResource : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="b3402-110">Membros</span><span class="sxs-lookup"><span data-stu-id="b3402-110">Members</span></span>

<span data-ttu-id="b3402-111">A classe **CIM \_ SystemResource** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b3402-111">The **CIM\_SystemResource** class has these types of members:</span></span>

-   [<span data-ttu-id="b3402-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b3402-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b3402-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b3402-113">Properties</span></span>

<span data-ttu-id="b3402-114">A classe **CIM \_ SystemResource** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b3402-114">The **CIM\_SystemResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b3402-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b3402-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3402-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3402-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3402-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3402-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3402-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b3402-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b3402-119">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b3402-119">A short textual description of the object.</span></span>

<span data-ttu-id="b3402-120">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3402-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3402-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b3402-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3402-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3402-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3402-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3402-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3402-124">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="b3402-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b3402-125">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b3402-125">A textual description of the object.</span></span>

<span data-ttu-id="b3402-126">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3402-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3402-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b3402-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3402-128">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b3402-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b3402-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3402-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3402-130">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="b3402-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b3402-131">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="b3402-131">Indicates when the object was installed.</span></span> <span data-ttu-id="b3402-132">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="b3402-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b3402-133">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3402-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3402-134">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b3402-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3402-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3402-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3402-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3402-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3402-137">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b3402-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b3402-138">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b3402-138">Label by which the object is known.</span></span> <span data-ttu-id="b3402-139">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="b3402-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="b3402-140">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3402-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3402-141">**Status**</span><span class="sxs-lookup"><span data-stu-id="b3402-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b3402-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b3402-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b3402-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b3402-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b3402-144">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b3402-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b3402-145">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b3402-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="b3402-146">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="b3402-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b3402-147">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="b3402-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b3402-148">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="b3402-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b3402-149">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="b3402-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b3402-150">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="b3402-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b3402-151">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="b3402-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b3402-152">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3402-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b3402-153">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b3402-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b3402-154">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b3402-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b3402-155">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="b3402-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b3402-156">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b3402-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b3402-157">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="b3402-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b3402-158">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b3402-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b3402-159">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="b3402-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b3402-160">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="b3402-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b3402-161">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="b3402-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b3402-162">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="b3402-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b3402-163">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b3402-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b3402-164">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="b3402-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b3402-165">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="b3402-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="b3402-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b3402-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b3402-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3402-167">Remarks</span></span>

<span data-ttu-id="b3402-168">A classe **CIM \_ SystemResource** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b3402-168">The **CIM\_SystemResource** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="b3402-169">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="b3402-169">WMI does not implement this class.</span></span> <span data-ttu-id="b3402-170">Para classes WMI derivadas do **CIM \_ SystemResource**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b3402-170">For WMI classes derived from **CIM\_SystemResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b3402-171">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b3402-171">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b3402-172">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b3402-172">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3402-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3402-173">Requirements</span></span>



| <span data-ttu-id="b3402-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3402-174">Requirement</span></span> | <span data-ttu-id="b3402-175">Valor</span><span class="sxs-lookup"><span data-stu-id="b3402-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b3402-176">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3402-176">Minimum supported client</span></span><br/> | <span data-ttu-id="b3402-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3402-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b3402-178">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b3402-178">Minimum supported server</span></span><br/> | <span data-ttu-id="b3402-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3402-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b3402-180">Namespace</span><span class="sxs-lookup"><span data-stu-id="b3402-180">Namespace</span></span><br/>                | <span data-ttu-id="b3402-181">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b3402-181">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b3402-182">MOF</span><span class="sxs-lookup"><span data-stu-id="b3402-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b3402-183"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b3402-183"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b3402-184">DLL</span><span class="sxs-lookup"><span data-stu-id="b3402-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3402-185"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3402-185"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3402-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3402-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3402-187">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="b3402-187">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

