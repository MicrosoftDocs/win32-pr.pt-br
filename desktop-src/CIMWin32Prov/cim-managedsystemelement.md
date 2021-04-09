---
description: A \_ classe CIM ManagedSystemElement é a classe base para a hierarquia de elementos do sistema. Qualquer componente de sistema diferencial é um candidato para inclusão nessa classe.
ms.assetid: f1b952f4-4bed-4420-ad5d-62478846be8e
ms.tgt_platform: multiple
title: Classe CIM_ManagedSystemElement (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ManagedSystemElement
- CIM_ManagedSystemElement.Caption
- CIM_ManagedSystemElement.Description
- CIM_ManagedSystemElement.InstallDate
- CIM_ManagedSystemElement.Name
- CIM_ManagedSystemElement.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60684d131a034f809a18898ec05ccc5f73f253f0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089268"
---
# <a name="cim_managedsystemelement-class-cimwin32-wmi-providers"></a><span data-ttu-id="b1acb-104">Classe CIM_ManagedSystemElement (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="b1acb-104">CIM_ManagedSystemElement class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b1acb-105">A classe **CIM \_ ManagedSystemElement** é a classe base para a hierarquia de elementos do sistema.</span><span class="sxs-lookup"><span data-stu-id="b1acb-105">The **CIM\_ManagedSystemElement** class is the base class for the system element hierarchy.</span></span> <span data-ttu-id="b1acb-106">Qualquer componente de sistema diferencial é um candidato para inclusão nessa classe.</span><span class="sxs-lookup"><span data-stu-id="b1acb-106">Any distinguishable system component is a candidate for inclusion in this class.</span></span> <span data-ttu-id="b1acb-107">Os exemplos incluem componentes de software, como arquivos; dispositivos, como unidades de disco e controladores; e componentes físicos, como chips e cartões.</span><span class="sxs-lookup"><span data-stu-id="b1acb-107">Examples include software components, such as files; devices, such as disk drives and controllers; and physical components, such as chips and cards.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1acb-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b1acb-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b1acb-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b1acb-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b1acb-110">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b1acb-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b1acb-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b1acb-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1acb-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b1acb-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C517-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Managed System Elements (CIM)"), AMENDMENT]
class CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="b1acb-113">Membros</span><span class="sxs-lookup"><span data-stu-id="b1acb-113">Members</span></span>

<span data-ttu-id="b1acb-114">A classe **CIM \_ ManagedSystemElement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b1acb-114">The **CIM\_ManagedSystemElement** class has these types of members:</span></span>

-   [<span data-ttu-id="b1acb-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b1acb-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b1acb-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b1acb-116">Properties</span></span>

<span data-ttu-id="b1acb-117">A classe **CIM \_ ManagedSystemElement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b1acb-117">The **CIM\_ManagedSystemElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b1acb-118">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b1acb-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1acb-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1acb-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1acb-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1acb-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1acb-121">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b1acb-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b1acb-122">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b1acb-122">A short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="b1acb-123">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b1acb-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1acb-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1acb-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1acb-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1acb-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1acb-126">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="b1acb-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b1acb-127">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b1acb-127">A textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="b1acb-128">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b1acb-128">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1acb-129">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b1acb-129">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b1acb-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1acb-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1acb-131">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="b1acb-131">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b1acb-132">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="b1acb-132">Indicates when the object was installed.</span></span> <span data-ttu-id="b1acb-133">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="b1acb-133">Lack of a value does not indicate that the object is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="b1acb-134">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b1acb-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1acb-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1acb-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1acb-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1acb-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1acb-137">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="b1acb-137">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="b1acb-138">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b1acb-138">Label by which the object is known.</span></span> <span data-ttu-id="b1acb-139">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="b1acb-139">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> <dt>

<span data-ttu-id="b1acb-140">**Status**</span><span class="sxs-lookup"><span data-stu-id="b1acb-140">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b1acb-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b1acb-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b1acb-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b1acb-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b1acb-143">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b1acb-143">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b1acb-144">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b1acb-144">String that indicates the current status of the object.</span></span> <span data-ttu-id="b1acb-145">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="b1acb-145">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b1acb-146">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="b1acb-146">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b1acb-147">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="b1acb-147">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b1acb-148">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="b1acb-148">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b1acb-149">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="b1acb-149">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b1acb-150">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="b1acb-150">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b1acb-151">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b1acb-151">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b1acb-152">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b1acb-152">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b1acb-153">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="b1acb-153">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b1acb-154">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b1acb-154">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b1acb-155">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="b1acb-155">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b1acb-156">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b1acb-156">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b1acb-157">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="b1acb-157">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b1acb-158">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="b1acb-158">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b1acb-159">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="b1acb-159">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b1acb-160">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="b1acb-160">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b1acb-161">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b1acb-161">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b1acb-162">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="b1acb-162">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b1acb-163">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="b1acb-163">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="b1acb-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b1acb-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b1acb-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="b1acb-165">Remarks</span></span>

<span data-ttu-id="b1acb-166">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="b1acb-166">WMI does not implement this class.</span></span> <span data-ttu-id="b1acb-167">Para classes WMI derivadas dessa classe, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b1acb-167">For WMI classes derived from this class, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b1acb-168">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b1acb-168">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b1acb-169">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b1acb-169">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1acb-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1acb-170">Requirements</span></span>



| <span data-ttu-id="b1acb-171">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1acb-171">Requirement</span></span> | <span data-ttu-id="b1acb-172">Valor</span><span class="sxs-lookup"><span data-stu-id="b1acb-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1acb-173">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1acb-173">Minimum supported client</span></span><br/> | <span data-ttu-id="b1acb-174">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1acb-174">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1acb-175">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b1acb-175">Minimum supported server</span></span><br/> | <span data-ttu-id="b1acb-176">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1acb-176">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1acb-177">Namespace</span><span class="sxs-lookup"><span data-stu-id="b1acb-177">Namespace</span></span><br/>                | <span data-ttu-id="b1acb-178">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b1acb-178">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b1acb-179">MOF</span><span class="sxs-lookup"><span data-stu-id="b1acb-179">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b1acb-180"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b1acb-180"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b1acb-181">DLL</span><span class="sxs-lookup"><span data-stu-id="b1acb-181">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1acb-182"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1acb-182"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

