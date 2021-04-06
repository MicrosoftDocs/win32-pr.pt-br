---
description: A \_ classe CIM LogicalElement é a classe base para todos os componentes do sistema que representam componentes do sistema abstratos, como perfis, processos ou recursos do sistema, na forma de dispositivos lógicos.
ms.assetid: 81b2788a-96e8-4570-9a13-d11d229ad789
ms.tgt_platform: multiple
title: Classe CIM_LogicalElement (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalElement
- CIM_LogicalElement.Caption
- CIM_LogicalElement.Description
- CIM_LogicalElement.InstallDate
- CIM_LogicalElement.Name
- CIM_LogicalElement.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 281ba9f97dafb246917d602fcfe1061f4cb03f86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826212"
---
# <a name="cim_logicalelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="e0fec-103">Classe CIM_LogicalElement (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="e0fec-103">CIM_LogicalElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="e0fec-104">A classe **CIM \_ LogicalElement** é a classe base para todos os componentes do sistema que representam componentes do sistema abstratos, como perfis, processos ou recursos do sistema, na forma de dispositivos lógicos.</span><span class="sxs-lookup"><span data-stu-id="e0fec-104">The **CIM\_LogicalElement** class is the base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e0fec-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e0fec-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e0fec-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e0fec-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e0fec-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e0fec-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e0fec-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e0fec-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0fec-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0fec-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Logical Elements (CIM)"), AMENDMENT]
class CIM_LogicalElement : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="e0fec-110">Membros</span><span class="sxs-lookup"><span data-stu-id="e0fec-110">Members</span></span>

<span data-ttu-id="e0fec-111">A classe **CIM \_ LogicalElement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e0fec-111">The **CIM\_LogicalElement** class has these types of members:</span></span>

-   [<span data-ttu-id="e0fec-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e0fec-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0fec-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e0fec-113">Properties</span></span>

<span data-ttu-id="e0fec-114">A classe **CIM \_ LogicalElement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e0fec-114">The **CIM\_LogicalElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0fec-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e0fec-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fec-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e0fec-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0fec-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e0fec-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0fec-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="e0fec-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="e0fec-119">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e0fec-119">A short textual description of the object.</span></span>

<span data-ttu-id="e0fec-120">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0fec-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0fec-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e0fec-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fec-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e0fec-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0fec-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e0fec-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0fec-124">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="e0fec-124">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="e0fec-125">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e0fec-125">A textual description of the object.</span></span>

<span data-ttu-id="e0fec-126">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0fec-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0fec-127">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="e0fec-127">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fec-128">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e0fec-128">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e0fec-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e0fec-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0fec-130">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="e0fec-130">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="e0fec-131">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="e0fec-131">Indicates when the object was installed.</span></span> <span data-ttu-id="e0fec-132">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="e0fec-132">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="e0fec-133">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0fec-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0fec-134">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e0fec-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fec-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e0fec-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0fec-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e0fec-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0fec-137">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="e0fec-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="e0fec-138">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="e0fec-138">Label by which the object is known.</span></span> <span data-ttu-id="e0fec-139">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="e0fec-139">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="e0fec-140">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0fec-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="e0fec-141">**Status**</span><span class="sxs-lookup"><span data-stu-id="e0fec-141">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0fec-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e0fec-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0fec-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e0fec-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0fec-144">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="e0fec-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="e0fec-145">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e0fec-145">String that indicates the current status of the object.</span></span> <span data-ttu-id="e0fec-146">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="e0fec-146">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="e0fec-147">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="e0fec-147">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="e0fec-148">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="e0fec-148">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="e0fec-149">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="e0fec-149">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="e0fec-150">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="e0fec-150">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="e0fec-151">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="e0fec-151">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="e0fec-152">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="e0fec-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="e0fec-153">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="e0fec-153">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="e0fec-154">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="e0fec-154">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="e0fec-155">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="e0fec-155">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="e0fec-156">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="e0fec-156">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="e0fec-157">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="e0fec-157">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="e0fec-158">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="e0fec-158">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="e0fec-159">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="e0fec-159">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="e0fec-160">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="e0fec-160">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="e0fec-161">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="e0fec-161">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="e0fec-162">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="e0fec-162">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="e0fec-163">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="e0fec-163">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="e0fec-164">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="e0fec-164">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="e0fec-165">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="e0fec-165">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="e0fec-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e0fec-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="e0fec-167">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0fec-167">Remarks</span></span>

<span data-ttu-id="e0fec-168">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e0fec-168">WMI does not implement this class.</span></span> <span data-ttu-id="e0fec-169">Para classes derivadas de **CIM \_ LogicalElement**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e0fec-169">For classes derived from **CIM\_LogicalElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e0fec-170">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e0fec-170">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e0fec-171">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e0fec-171">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0fec-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0fec-172">Requirements</span></span>



| <span data-ttu-id="e0fec-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0fec-173">Requirement</span></span> | <span data-ttu-id="e0fec-174">Valor</span><span class="sxs-lookup"><span data-stu-id="e0fec-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0fec-175">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0fec-175">Minimum supported client</span></span><br/> | <span data-ttu-id="e0fec-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e0fec-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e0fec-177">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0fec-177">Minimum supported server</span></span><br/> | <span data-ttu-id="e0fec-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e0fec-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e0fec-179">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0fec-179">Namespace</span></span><br/>                | <span data-ttu-id="e0fec-180">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e0fec-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e0fec-181">MOF</span><span class="sxs-lookup"><span data-stu-id="e0fec-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0fec-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0fec-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0fec-183">DLL</span><span class="sxs-lookup"><span data-stu-id="e0fec-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0fec-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0fec-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0fec-185">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0fec-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0fec-186">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="e0fec-186">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> </dl>

 

