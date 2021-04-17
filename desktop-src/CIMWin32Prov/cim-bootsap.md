---
description: A \_ classe CIM BootSAP representa os pontos de acesso de um serviço de inicialização.
ms.assetid: eea6d6c5-3930-4e20-b7d3-b6d5722662cd
ms.tgt_platform: multiple
title: Classe CIM_BootSAP
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootSAP
- CIM_BootSAP.Caption
- CIM_BootSAP.Description
- CIM_BootSAP.InstallDate
- CIM_BootSAP.Status
- CIM_BootSAP.CreationClassName
- CIM_BootSAP.Name
- CIM_BootSAP.SystemCreationClassName
- CIM_BootSAP.SystemName
- CIM_BootSAP.Type
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d4868497c2d604457a45273b1c0cc609ae361ad9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749353"
---
# <a name="cim_bootsap-class"></a><span data-ttu-id="f5dcc-103">\_Classe CIM BootSAP</span><span class="sxs-lookup"><span data-stu-id="f5dcc-103">CIM\_BootSAP class</span></span>

<span data-ttu-id="f5dcc-104">A classe **CIM \_ BootSAP** representa os pontos de acesso de um serviço de inicialização.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-104">The **CIM\_BootSAP** class represents the access points of a boot service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5dcc-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f5dcc-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f5dcc-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f5dcc-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f5dcc-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5dcc-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f5dcc-109">Syntax</span></span>

``` syntax
[UUID("{F6FEF20A-E3D2-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BootSAP : CIM_ServiceAccessPoint
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

## <a name="members"></a><span data-ttu-id="f5dcc-110">Membros</span><span class="sxs-lookup"><span data-stu-id="f5dcc-110">Members</span></span>

<span data-ttu-id="f5dcc-111">A classe **CIM \_ BootSAP** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f5dcc-111">The **CIM\_BootSAP** class has these types of members:</span></span>

-   [<span data-ttu-id="f5dcc-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f5dcc-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5dcc-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f5dcc-113">Properties</span></span>

<span data-ttu-id="f5dcc-114">A classe **CIM \_ BootSAP** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-114">The **CIM\_BootSAP** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5dcc-115">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5dcc-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f5dcc-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-118">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f5dcc-119">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-119">A short textual description of the object.</span></span>

<span data-ttu-id="f5dcc-120">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5dcc-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5dcc-121">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-121">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5dcc-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f5dcc-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-124">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f5dcc-124">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f5dcc-125">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-125">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f5dcc-126">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-126">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="f5dcc-127">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="f5dcc-127">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5dcc-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5dcc-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f5dcc-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-131">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f5dcc-132">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-132">A textual description of the object.</span></span>

<span data-ttu-id="f5dcc-133">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5dcc-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5dcc-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5dcc-135">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f5dcc-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-137">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f5dcc-138">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-138">Indicates when the object was installed.</span></span> <span data-ttu-id="f5dcc-139">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f5dcc-140">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5dcc-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5dcc-141">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5dcc-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f5dcc-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-144">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f5dcc-144">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f5dcc-145">Identifica exclusivamente o ponto de acesso de serviço e fornece uma indicação da funcionalidade que é gerenciada.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-145">Uniquely identifies the service access point and provides an indication of the functionality that is managed.</span></span> <span data-ttu-id="f5dcc-146">Essa funcionalidade é descrita mais detalhadamente na propriedade Description do objeto.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-146">This functionality is described in more detail in the object's Description property.</span></span>

<span data-ttu-id="f5dcc-147">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="f5dcc-147">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5dcc-148">**Status**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5dcc-149">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f5dcc-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-151">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f5dcc-152">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-152">String that indicates the current status of the object.</span></span> <span data-ttu-id="f5dcc-153">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-153">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f5dcc-154">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="f5dcc-154">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f5dcc-155">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="f5dcc-155">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f5dcc-156">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="f5dcc-156">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f5dcc-157">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-157">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f5dcc-158">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-158">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f5dcc-159">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f5dcc-159">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f5dcc-160">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f5dcc-160">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f5dcc-161">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-161">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f5dcc-162">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-162">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f5dcc-163">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-163">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f5dcc-164">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-164">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f5dcc-165">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-165">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f5dcc-166">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-166">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f5dcc-167">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-167">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f5dcc-168">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-168">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f5dcc-169">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-169">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f5dcc-170">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-170">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f5dcc-171">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-171">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f5dcc-172">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-172">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f5dcc-173">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-173">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5dcc-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f5dcc-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-176">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f5dcc-176">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f5dcc-177">O nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-177">The scoping system's creation class name.</span></span>

<span data-ttu-id="f5dcc-178">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="f5dcc-178">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5dcc-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5dcc-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f5dcc-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-182">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f5dcc-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f5dcc-183">O nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-183">The scoping system's name.</span></span>

<span data-ttu-id="f5dcc-184">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="f5dcc-184">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5dcc-185">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-185">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5dcc-186">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-186">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f5dcc-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5dcc-188">Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="f5dcc-188">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="f5dcc-189">Tipo de SAP, como anexado ou Redirecionado.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-189">Type of SAP, such as attached or redirected.</span></span>

<span data-ttu-id="f5dcc-190">Essa propriedade é herdada do [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="f5dcc-190">This property is inherited from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

<span data-ttu-id="f5dcc-191">**Gravação** (1)</span><span class="sxs-lookup"><span data-stu-id="f5dcc-191">**Write** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

<span data-ttu-id="f5dcc-192">**Leitura** (2)</span><span class="sxs-lookup"><span data-stu-id="f5dcc-192">**Read** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Redirected"></span><span id="redirected"></span><span id="REDIRECTED"></span>

<span data-ttu-id="f5dcc-193">**Redirecionado** (4)</span><span class="sxs-lookup"><span data-stu-id="f5dcc-193">**Redirected** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Net_Attached"></span><span id="net_attached"></span><span id="NET_ATTACHED"></span>

<span data-ttu-id="f5dcc-194">**Rede \_ Anexado** (8)</span><span class="sxs-lookup"><span data-stu-id="f5dcc-194">**Net\_Attached** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f5dcc-195">**desconhecido** (16)</span><span class="sxs-lookup"><span data-stu-id="f5dcc-195">**unknown** (16)</span></span>


<span data-ttu-id="f5dcc-196"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f5dcc-196"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="f5dcc-197">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5dcc-197">Remarks</span></span>

<span data-ttu-id="f5dcc-198">A classe **CIM \_ BootSAP** é derivada de [**\_ ServiceAccessPoint CIM**](cim-serviceaccesspoint.md).</span><span class="sxs-lookup"><span data-stu-id="f5dcc-198">The **CIM\_BootSAP** class is derived from [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md).</span></span>

<span data-ttu-id="f5dcc-199">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-199">WMI does not implement this class.</span></span>

<span data-ttu-id="f5dcc-200">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-200">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f5dcc-201">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="f5dcc-201">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5dcc-202">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5dcc-202">Requirements</span></span>



| <span data-ttu-id="f5dcc-203">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5dcc-203">Requirement</span></span> | <span data-ttu-id="f5dcc-204">Valor</span><span class="sxs-lookup"><span data-stu-id="f5dcc-204">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5dcc-205">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5dcc-205">Minimum supported client</span></span><br/> | <span data-ttu-id="f5dcc-206">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f5dcc-206">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f5dcc-207">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f5dcc-207">Minimum supported server</span></span><br/> | <span data-ttu-id="f5dcc-208">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5dcc-208">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f5dcc-209">Namespace</span><span class="sxs-lookup"><span data-stu-id="f5dcc-209">Namespace</span></span><br/>                | <span data-ttu-id="f5dcc-210">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f5dcc-210">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f5dcc-211">MOF</span><span class="sxs-lookup"><span data-stu-id="f5dcc-211">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5dcc-212"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5dcc-212"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5dcc-213">DLL</span><span class="sxs-lookup"><span data-stu-id="f5dcc-213">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5dcc-214"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5dcc-214"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5dcc-215">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5dcc-215">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5dcc-216">**\_SERVICEACCESSPOINT CIM**</span><span class="sxs-lookup"><span data-stu-id="f5dcc-216">**CIM\_ServiceAccessPoint**</span></span>](cim-serviceaccesspoint.md)
</dt> </dl>

 

