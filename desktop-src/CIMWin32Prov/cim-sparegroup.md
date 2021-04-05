---
description: A \_ classe de Spar sobressalente CIM é derivada da \_ classe CIM RedundancyGroup e indica que um ou mais dos elementos agregados podem ser resobrados.
ms.assetid: e60f8cab-a9e8-4f5a-b8d7-833c7832ef7e
ms.tgt_platform: multiple
title: Classe CIM_SpareGroup
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SpareGroup
- CIM_SpareGroup.Caption
- CIM_SpareGroup.Description
- CIM_SpareGroup.InstallDate
- CIM_SpareGroup.Name
- CIM_SpareGroup.Status
- CIM_SpareGroup.CreationClassName
- CIM_SpareGroup.RedundancyStatus
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 17907c62ace9f75c8d807e56d35b91f4c28e5f42
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646232"
---
# <a name="cim_sparegroup-class"></a><span data-ttu-id="2eed9-103">\_Classe de Spar sobressalente CIM</span><span class="sxs-lookup"><span data-stu-id="2eed9-103">CIM\_SpareGroup class</span></span>

<span data-ttu-id="2eed9-104">A classe de **\_ Spar sobressalente CIM** é derivada da classe [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) e indica que um ou mais dos elementos agregados podem ser resobrados.</span><span class="sxs-lookup"><span data-stu-id="2eed9-104">The **CIM\_SpareGroup** class is derived from the [**CIM\_RedundancyGroup**](cim-redundancygroup.md) class and indicates that one or more of the aggregated elements can be spared.</span></span> <span data-ttu-id="2eed9-105">Os spares são definidos usando a associação [**CIM \_ ActsAsSpare**](cim-actsasspare.md) .</span><span class="sxs-lookup"><span data-stu-id="2eed9-105">Spares are defined using the [**CIM\_ActsAsSpare**](cim-actsasspare.md) association.</span></span> <span data-ttu-id="2eed9-106">Um exemplo de spare é o uso de NICs redundantes em um sistema de computador, em que uma NIC é primária e a outra é sobressalente.</span><span class="sxs-lookup"><span data-stu-id="2eed9-106">An example of a spare is the use of redundant NICs in a computer system, where one NIC is primary and the other is spare.</span></span> <span data-ttu-id="2eed9-107">A NIC primária seria um membro do grupo sobressalente, associado usando a classe [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md) e a outra NIC seria associada usando o relacionamento **CIM \_ ActsAsSpare** .</span><span class="sxs-lookup"><span data-stu-id="2eed9-107">The primary NIC would be a member of the spare group, associated using the [**CIM\_RedundancyComponent**](cim-redundancycomponent.md) class, and the other NIC would be associated using the **CIM\_ActsAsSpare** relationship.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2eed9-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="2eed9-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2eed9-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2eed9-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2eed9-110">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2eed9-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2eed9-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="2eed9-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eed9-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2eed9-112">Syntax</span></span>

``` syntax
[Abstract, UUID("{64B86CA6-E3D1-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_SpareGroup : CIM_RedundancyGroup
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

## <a name="members"></a><span data-ttu-id="2eed9-113">Membros</span><span class="sxs-lookup"><span data-stu-id="2eed9-113">Members</span></span>

<span data-ttu-id="2eed9-114">A classe de **\_ spare do CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2eed9-114">The **CIM\_SpareGroup** class has these types of members:</span></span>

-   [<span data-ttu-id="2eed9-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2eed9-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2eed9-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2eed9-116">Properties</span></span>

<span data-ttu-id="2eed9-117">A classe de **\_ Spar sobressalente CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2eed9-117">The **CIM\_SpareGroup** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2eed9-118">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="2eed9-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eed9-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2eed9-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eed9-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2eed9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eed9-121">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2eed9-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2eed9-122">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="2eed9-122">A short textual description of the object.</span></span>

<span data-ttu-id="2eed9-123">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2eed9-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eed9-124">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2eed9-124">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eed9-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2eed9-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eed9-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2eed9-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eed9-127">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2eed9-127">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2eed9-128">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="2eed9-128">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="2eed9-129">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="2eed9-129">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2eed9-130">Essa propriedade é herdada do [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="2eed9-130">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eed9-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2eed9-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eed9-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2eed9-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eed9-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2eed9-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eed9-134">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="2eed9-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2eed9-135">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="2eed9-135">A textual description of the object.</span></span>

<span data-ttu-id="2eed9-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2eed9-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eed9-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2eed9-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eed9-138">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2eed9-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2eed9-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2eed9-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eed9-140">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="2eed9-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2eed9-141">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="2eed9-141">Indicates when the object was installed.</span></span> <span data-ttu-id="2eed9-142">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="2eed9-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="2eed9-143">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2eed9-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eed9-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2eed9-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eed9-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2eed9-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eed9-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2eed9-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eed9-147">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="2eed9-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2eed9-148">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="2eed9-148">Label by which the object is known.</span></span> <span data-ttu-id="2eed9-149">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="2eed9-149">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="2eed9-150">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2eed9-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2eed9-151">**RedundancyStatus**</span><span class="sxs-lookup"><span data-stu-id="2eed9-151">**RedundancyStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eed9-152">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2eed9-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2eed9-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2eed9-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2eed9-154">Informações sobre o estado do grupo de redundância.</span><span class="sxs-lookup"><span data-stu-id="2eed9-154">Information about the state of the redundancy group.</span></span>

<span data-ttu-id="2eed9-155">Essa propriedade é herdada do [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="2eed9-155">This property is inherited from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eed9-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="2eed9-156"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="2eed9-157">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="2eed9-157">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="2eed9-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="2eed9-158"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="2eed9-159">Outros.</span><span class="sxs-lookup"><span data-stu-id="2eed9-159">Other.</span></span>

</dd> <dt>

<span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>

<span data-ttu-id="2eed9-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Totalmente redundante** (2)</span><span class="sxs-lookup"><span data-stu-id="2eed9-160"><span id="Fully_Redundant"></span><span id="fully_redundant"></span><span id="FULLY_REDUNDANT"></span>**Fully Redundant** (2)</span></span>


</dt> <dd>

<span data-ttu-id="2eed9-161">Toda a redundância configurada está disponível.</span><span class="sxs-lookup"><span data-stu-id="2eed9-161">All of the configured redundancy is available.</span></span>

</dd> <dt>

<span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>

<span data-ttu-id="2eed9-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Redundância degradada** (3)</span><span class="sxs-lookup"><span data-stu-id="2eed9-162"><span id="Degraded_Redundancy"></span><span id="degraded_redundancy"></span><span id="DEGRADED_REDUNDANCY"></span>**Degraded Redundancy** (3)</span></span>


</dt> <dd>

<span data-ttu-id="2eed9-163">A quantidade reduzida de redundância está disponível devido a algumas falhas.</span><span class="sxs-lookup"><span data-stu-id="2eed9-163">Reduced amount of redundancy is available due to some failures.</span></span>

</dd> <dt>

<span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>

<span data-ttu-id="2eed9-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundância perdida** (4)</span><span class="sxs-lookup"><span data-stu-id="2eed9-164"><span id="Redundancy_Lost"></span><span id="redundancy_lost"></span><span id="REDUNDANCY_LOST"></span>**Redundancy Lost** (4)</span></span>


</dt> <dd>

<span data-ttu-id="2eed9-165">A redundância não está disponível devido a um número suficiente de falhas.</span><span class="sxs-lookup"><span data-stu-id="2eed9-165">Redundancy is unavailable due to a sufficient number of failures.</span></span> <span data-ttu-id="2eed9-166">A próxima falha causará falha geral.</span><span class="sxs-lookup"><span data-stu-id="2eed9-166">The next failure will cause overall failure.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2eed9-167">**Status**</span><span class="sxs-lookup"><span data-stu-id="2eed9-167">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2eed9-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2eed9-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2eed9-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2eed9-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2eed9-170">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="2eed9-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2eed9-171">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="2eed9-171">String that indicates the current status of the object.</span></span> <span data-ttu-id="2eed9-172">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="2eed9-172">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="2eed9-173">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="2eed9-173">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="2eed9-174">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="2eed9-174">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="2eed9-175">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="2eed9-175">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2eed9-176">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="2eed9-176">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2eed9-177">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="2eed9-177">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2eed9-178">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2eed9-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2eed9-179">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2eed9-179">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2eed9-180">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="2eed9-180">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2eed9-181">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="2eed9-181">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2eed9-182">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="2eed9-182">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2eed9-183">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="2eed9-183">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2eed9-184">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="2eed9-184">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2eed9-185">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="2eed9-185">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2eed9-186">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="2eed9-186">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2eed9-187">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="2eed9-187">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2eed9-188">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="2eed9-188">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2eed9-189">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="2eed9-189">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2eed9-190">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="2eed9-190">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2eed9-191">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="2eed9-191">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="2eed9-192"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2eed9-192"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="2eed9-193">Comentários</span><span class="sxs-lookup"><span data-stu-id="2eed9-193">Remarks</span></span>

<span data-ttu-id="2eed9-194">A classe de **\_ Spar sobressalente CIM** é derivada do [**CIM \_ RedundancyGroup**](cim-redundancygroup.md).</span><span class="sxs-lookup"><span data-stu-id="2eed9-194">The **CIM\_SpareGroup** class is derived from [**CIM\_RedundancyGroup**](cim-redundancygroup.md).</span></span>

<span data-ttu-id="2eed9-195">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="2eed9-195">WMI does not implement this class.</span></span>

<span data-ttu-id="2eed9-196">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="2eed9-196">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2eed9-197">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="2eed9-197">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eed9-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2eed9-198">Requirements</span></span>



| <span data-ttu-id="2eed9-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="2eed9-199">Requirement</span></span> | <span data-ttu-id="2eed9-200">Valor</span><span class="sxs-lookup"><span data-stu-id="2eed9-200">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2eed9-201">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2eed9-201">Minimum supported client</span></span><br/> | <span data-ttu-id="2eed9-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2eed9-202">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2eed9-203">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2eed9-203">Minimum supported server</span></span><br/> | <span data-ttu-id="2eed9-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2eed9-204">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2eed9-205">Namespace</span><span class="sxs-lookup"><span data-stu-id="2eed9-205">Namespace</span></span><br/>                | <span data-ttu-id="2eed9-206">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2eed9-206">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2eed9-207">MOF</span><span class="sxs-lookup"><span data-stu-id="2eed9-207">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2eed9-208"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2eed9-208"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2eed9-209">DLL</span><span class="sxs-lookup"><span data-stu-id="2eed9-209">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2eed9-210"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2eed9-210"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eed9-211">Confira também</span><span class="sxs-lookup"><span data-stu-id="2eed9-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eed9-212">**\_REDUNDANCYGROUP CIM**</span><span class="sxs-lookup"><span data-stu-id="2eed9-212">**CIM\_RedundancyGroup**</span></span>](cim-redundancygroup.md)
</dt> </dl>

 

