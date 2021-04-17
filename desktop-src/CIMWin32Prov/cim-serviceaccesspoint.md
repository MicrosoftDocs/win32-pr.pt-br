---
description: A \_ classe CIM ServiceAccessPoint representa a capacidade de usar ou invocar um serviço. Os pontos de acesso representam serviços que estão disponíveis para uso por outras entidades.
ms.assetid: caf828a1-c9a7-4ae8-9734-d77e4ba90b09
ms.tgt_platform: multiple
title: Classe CIM_ServiceAccessPoint (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAccessPoint
- CIM_ServiceAccessPoint.Caption
- CIM_ServiceAccessPoint.Description
- CIM_ServiceAccessPoint.InstallDate
- CIM_ServiceAccessPoint.Status
- CIM_ServiceAccessPoint.CreationClassName
- CIM_ServiceAccessPoint.Name
- CIM_ServiceAccessPoint.SystemCreationClassName
- CIM_ServiceAccessPoint.SystemName
- CIM_ServiceAccessPoint.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 681e5e11de525e535f7965b72adb8ac0e316f7aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500908"
---
# <a name="cim_serviceaccesspoint-class-cimwin32-wmi-providers"></a><span data-ttu-id="a8d3f-104">Classe CIM_ServiceAccessPoint (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="a8d3f-104">CIM_ServiceAccessPoint class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="a8d3f-105">A classe **CIM \_ ServiceAccessPoint** representa a capacidade de usar ou invocar um serviço.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-105">The **CIM\_ServiceAccessPoint** class represents the ability to use or invoke a service.</span></span> <span data-ttu-id="a8d3f-106">Os pontos de acesso representam serviços que estão disponíveis para uso por outras entidades.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-106">Access points represent services that are available for use by other entities.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a8d3f-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a8d3f-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a8d3f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a8d3f-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a8d3f-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8d3f-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8d3f-111">Syntax</span></span>

``` syntax
[UUID("{F126ACC2-E3D4-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ServiceAccessPoint : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="a8d3f-112">Membros</span><span class="sxs-lookup"><span data-stu-id="a8d3f-112">Members</span></span>

<span data-ttu-id="a8d3f-113">A classe **CIM \_ ServiceAccessPoint** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a8d3f-113">The **CIM\_ServiceAccessPoint** class has these types of members:</span></span>

-   [<span data-ttu-id="a8d3f-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a8d3f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8d3f-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a8d3f-115">Properties</span></span>

<span data-ttu-id="a8d3f-116">A classe **CIM \_ ServiceAccessPoint** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-116">The **CIM\_ServiceAccessPoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8d3f-117">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8d3f-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8d3f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-120">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a8d3f-121">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-121">A short textual description of the object.</span></span>

<span data-ttu-id="a8d3f-122">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8d3f-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8d3f-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8d3f-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8d3f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-126">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a8d3f-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a8d3f-127">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="a8d3f-128">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="a8d3f-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8d3f-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8d3f-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-132">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a8d3f-133">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-133">A textual description of the object.</span></span>

<span data-ttu-id="a8d3f-134">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8d3f-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8d3f-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8d3f-136">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8d3f-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-138">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a8d3f-139">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-139">Indicates when the object was installed.</span></span> <span data-ttu-id="a8d3f-140">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a8d3f-141">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8d3f-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8d3f-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8d3f-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8d3f-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-145">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a8d3f-145">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a8d3f-146">Identifica exclusivamente o ponto de acesso de serviço e fornece uma indicação da funcionalidade que é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-146">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="a8d3f-147">Essa funcionalidade é descrita mais detalhadamente na propriedade Description do objeto.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-147">This functionality is described in more detail in the object's Description property.</span></span>

</dd> <dt>

<span data-ttu-id="a8d3f-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8d3f-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8d3f-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-151">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a8d3f-152">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="a8d3f-153">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="a8d3f-154">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="a8d3f-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="a8d3f-155">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="a8d3f-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="a8d3f-156">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="a8d3f-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a8d3f-157">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a8d3f-158">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a8d3f-159">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8d3f-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a8d3f-160">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="a8d3f-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a8d3f-161">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a8d3f-162">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a8d3f-163">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a8d3f-164">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a8d3f-165">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a8d3f-166">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a8d3f-167">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a8d3f-168">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a8d3f-169">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a8d3f-170">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a8d3f-171">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a8d3f-172">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a8d3f-173">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8d3f-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8d3f-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-176">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a8d3f-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a8d3f-177">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-177">The scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="a8d3f-178">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-178">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8d3f-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8d3f-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-181">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a8d3f-181">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a8d3f-182">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-182">The scoping system's name.</span></span>

</dd> <dt>

<span data-ttu-id="a8d3f-183">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-183">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8d3f-184">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-184">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8d3f-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8d3f-186">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="a8d3f-186">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="a8d3f-187">Tipo de SAP, como anexado ou Redirecionado.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-187">Type of SAP, such as attached or redirected.</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="a8d3f-188">**Gravação** (1)</span><span class="sxs-lookup"><span data-stu-id="a8d3f-188">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="a8d3f-189">**Leitura** (2)</span><span class="sxs-lookup"><span data-stu-id="a8d3f-189">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="a8d3f-190">**Redirecionado** (4)</span><span class="sxs-lookup"><span data-stu-id="a8d3f-190">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="a8d3f-191">**Rede \_ Anexado** (8)</span><span class="sxs-lookup"><span data-stu-id="a8d3f-191">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a8d3f-192">**desconhecido** (16)</span><span class="sxs-lookup"><span data-stu-id="a8d3f-192">**unknown** (16)</span></span>


<span data-ttu-id="a8d3f-193"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a8d3f-193"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a8d3f-194">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8d3f-194">Remarks</span></span>

<span data-ttu-id="a8d3f-195">A classe **CIM \_ ServiceAccessPoint** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="a8d3f-195">The **CIM\_ServiceAccessPoint** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="a8d3f-196">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-196">WMI does not implement this class.</span></span> <span data-ttu-id="a8d3f-197">Para classes WMI derivadas do **CIM \_ ServiceAccessPoint**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a8d3f-197">For WMI classes derived from **CIM\_ServiceAccessPoint**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a8d3f-198">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-198">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a8d3f-199">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="a8d3f-199">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8d3f-200">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8d3f-200">Requirements</span></span>



| <span data-ttu-id="a8d3f-201">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8d3f-201">Requirement</span></span> | <span data-ttu-id="a8d3f-202">Valor</span><span class="sxs-lookup"><span data-stu-id="a8d3f-202">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d3f-203">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8d3f-203">Minimum supported client</span></span><br/> | <span data-ttu-id="a8d3f-204">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8d3f-204">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a8d3f-205">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8d3f-205">Minimum supported server</span></span><br/> | <span data-ttu-id="a8d3f-206">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8d3f-206">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a8d3f-207">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8d3f-207">Namespace</span></span><br/>                | <span data-ttu-id="a8d3f-208">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a8d3f-208">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a8d3f-209">MOF</span><span class="sxs-lookup"><span data-stu-id="a8d3f-209">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8d3f-210"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8d3f-210"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8d3f-211">DLL</span><span class="sxs-lookup"><span data-stu-id="a8d3f-211">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8d3f-212"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8d3f-212"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8d3f-213">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8d3f-213">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8d3f-214">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="a8d3f-214">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

