---
description: A \_ classe CIM RedundancyGroup representa uma coleção de elementos de sistema gerenciados, que indica que os componentes agregados, juntos, fornecem redundância.
ms.assetid: b47899cc-eafc-431f-96d4-edb01bf4bcd1
ms.tgt_platform: multiple
title: Classe CIM_RedundancyGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyGroup
- CIM_RedundancyGroup.Caption
- CIM_RedundancyGroup.Description
- CIM_RedundancyGroup.InstallDate
- CIM_RedundancyGroup.Name
- CIM_RedundancyGroup.Status
- CIM_RedundancyGroup.CreationClassName
- CIM_RedundancyGroup.RedundancyStatus
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1394e052b4741dee5b2646c903d83477bfa1ccf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826152"
---
# <a name="cim_redundancygroup-class"></a><span data-ttu-id="431e8-103">\_Classe CIM RedundancyGroup</span><span class="sxs-lookup"><span data-stu-id="431e8-103">CIM\_RedundancyGroup class</span></span>

<span data-ttu-id="431e8-104">A classe **CIM \_ RedundancyGroup** representa uma coleção de elementos de sistema gerenciados, que indica que os componentes agregados, juntos, fornecem redundância.</span><span class="sxs-lookup"><span data-stu-id="431e8-104">The **CIM\_RedundancyGroup** class represents a collection of managed system elements, which indicates that the aggregated components, together, provide redundancy.</span></span> <span data-ttu-id="431e8-105">Todos os elementos agregados em um grupo de redundância devem ser instanciações da mesma classe de objeto.</span><span class="sxs-lookup"><span data-stu-id="431e8-105">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="431e8-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="431e8-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="431e8-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="431e8-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="431e8-108">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="431e8-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="431e8-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="431e8-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="431e8-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="431e8-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{4C3A040A-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyGroup : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  uint16   RedundancyStatus;
};
```

## <a name="members"></a><span data-ttu-id="431e8-111">Membros</span><span class="sxs-lookup"><span data-stu-id="431e8-111">Members</span></span>

<span data-ttu-id="431e8-112">A classe **CIM \_ RedundancyGroup** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="431e8-112">The **CIM\_RedundancyGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="431e8-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="431e8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="431e8-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="431e8-114">Properties</span></span>

<span data-ttu-id="431e8-115">A classe **CIM \_ RedundancyGroup** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="431e8-115">The **CIM\_RedundancyGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="431e8-116">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="431e8-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431e8-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="431e8-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="431e8-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="431e8-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="431e8-119">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="431e8-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="431e8-120">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="431e8-120">A short textual description of the object.</span></span>

<span data-ttu-id="431e8-121">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="431e8-121">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="431e8-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="431e8-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431e8-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="431e8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="431e8-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="431e8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="431e8-125">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="431e8-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="431e8-126">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="431e8-126">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="431e8-127">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="431e8-127">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="431e8-128">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="431e8-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431e8-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="431e8-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="431e8-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="431e8-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="431e8-131">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="431e8-131">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="431e8-132">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="431e8-132">A textual description of the object.</span></span>

<span data-ttu-id="431e8-133">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="431e8-133">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="431e8-134">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="431e8-134">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431e8-135">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="431e8-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="431e8-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="431e8-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="431e8-137">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="431e8-137">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="431e8-138">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="431e8-138">Indicates when the object was installed.</span></span> <span data-ttu-id="431e8-139">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="431e8-139">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="431e8-140">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="431e8-140">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="431e8-141">**Nome**</span><span class="sxs-lookup"><span data-stu-id="431e8-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431e8-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="431e8-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="431e8-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="431e8-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="431e8-144">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="431e8-144">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="431e8-145">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="431e8-145">Label by which the object is known.</span></span> <span data-ttu-id="431e8-146">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="431e8-146">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="431e8-147">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="431e8-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="431e8-148">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="431e8-148">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431e8-149">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="431e8-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="431e8-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="431e8-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="431e8-151">Informações sobre o estado do grupo de redundância.</span><span class="sxs-lookup"><span data-stu-id="431e8-151">Information about the state of the redundancy group.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="431e8-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="431e8-152"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="431e8-153">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="431e8-153">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="431e8-154"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="431e8-154"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="431e8-155">Outros.</span><span class="sxs-lookup"><span data-stu-id="431e8-155">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="431e8-156"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Totalmente redundante** (2)</span><span class="sxs-lookup"><span data-stu-id="431e8-156"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="431e8-157">Toda a redundância configurada está disponível.</span><span class="sxs-lookup"><span data-stu-id="431e8-157">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="431e8-158"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Redundância degradada** (3)</span><span class="sxs-lookup"><span data-stu-id="431e8-158"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="431e8-159">A quantidade reduzida de redundância está disponível devido a algumas falhas.</span><span class="sxs-lookup"><span data-stu-id="431e8-159">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="431e8-160"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundância perdida** (4)</span><span class="sxs-lookup"><span data-stu-id="431e8-160"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="431e8-161">A redundância não está disponível devido a um número suficiente de falhas.</span><span class="sxs-lookup"><span data-stu-id="431e8-161">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="431e8-162">A próxima falha causará falha geral.</span><span class="sxs-lookup"><span data-stu-id="431e8-162">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="431e8-163">**Status**</span><span class="sxs-lookup"><span data-stu-id="431e8-163">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="431e8-164">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="431e8-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="431e8-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="431e8-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="431e8-166">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="431e8-166">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="431e8-167">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="431e8-167">String that indicates the current status of the object.</span></span> <span data-ttu-id="431e8-168">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="431e8-168">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="431e8-169">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="431e8-169">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="431e8-170">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="431e8-170">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="431e8-171">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="431e8-171">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="431e8-172">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="431e8-172">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="431e8-173">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="431e8-173">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="431e8-174">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="431e8-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="431e8-175">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="431e8-175">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="431e8-176">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="431e8-176">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="431e8-177">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="431e8-177">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="431e8-178">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="431e8-178">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="431e8-179">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="431e8-179">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="431e8-180">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="431e8-180">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="431e8-181">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="431e8-181">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="431e8-182">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="431e8-182">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="431e8-183">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="431e8-183">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="431e8-184">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="431e8-184">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="431e8-185">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="431e8-185">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="431e8-186">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="431e8-186">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="431e8-187">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="431e8-187">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="431e8-188"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="431e8-188"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="431e8-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="431e8-189">Remarks</span></span>

<span data-ttu-id="431e8-190">A classe **CIM \_ RedundancyGroup** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="431e8-190">The **CIM\_RedundancyGroup** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="431e8-191">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="431e8-191">WMI does not implement this class.</span></span>

<span data-ttu-id="431e8-192">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="431e8-192">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="431e8-193">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="431e8-193">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="431e8-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="431e8-194">Requirements</span></span>



| <span data-ttu-id="431e8-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="431e8-195">Requirement</span></span> | <span data-ttu-id="431e8-196">Valor</span><span class="sxs-lookup"><span data-stu-id="431e8-196">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="431e8-197">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="431e8-197">Minimum supported client</span></span><br/> | <span data-ttu-id="431e8-198">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="431e8-198">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="431e8-199">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="431e8-199">Minimum supported server</span></span><br/> | <span data-ttu-id="431e8-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="431e8-200">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="431e8-201">Namespace</span><span class="sxs-lookup"><span data-stu-id="431e8-201">Namespace</span></span><br/>                | <span data-ttu-id="431e8-202">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="431e8-202">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="431e8-203">MOF</span><span class="sxs-lookup"><span data-stu-id="431e8-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="431e8-204"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="431e8-204"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="431e8-205">DLL</span><span class="sxs-lookup"><span data-stu-id="431e8-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="431e8-206"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="431e8-206"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="431e8-207">Confira também</span><span class="sxs-lookup"><span data-stu-id="431e8-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="431e8-208">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="431e8-208">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

