---
description: A \_ classe CIM JobDestination representa onde um trabalho é enviado para processamento.
ms.assetid: ad2a037d-a5d3-4422-972d-8ef10699bb60
ms.tgt_platform: multiple
title: Classe CIM_JobDestination
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_JobDestination
- CIM_JobDestination.Caption
- CIM_JobDestination.Description
- CIM_JobDestination.InstallDate
- CIM_JobDestination.Name
- CIM_JobDestination.Status
- CIM_JobDestination.CreationClassName
- CIM_JobDestination.SystemCreationClassName
- CIM_JobDestination.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d01fbe3b6025795084bf0af4cca3d644fd3cf4a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826450"
---
# <a name="cim_jobdestination-class"></a><span data-ttu-id="39cf1-103">\_Classe CIM JobDestination</span><span class="sxs-lookup"><span data-stu-id="39cf1-103">CIM\_JobDestination class</span></span>

<span data-ttu-id="39cf1-104">A classe **CIM \_ JobDestination** representa onde um trabalho é enviado para processamento.</span><span class="sxs-lookup"><span data-stu-id="39cf1-104">The **CIM\_JobDestination** class represents where a job is submitted for processing.</span></span> <span data-ttu-id="39cf1-105">Ele pode se referir a uma fila que contém zero ou mais trabalhos, como uma fila de impressão que contém trabalhos de impressão.</span><span class="sxs-lookup"><span data-stu-id="39cf1-105">It can refer to a queue that contains zero or more jobs, such as a print queue containing print jobs.</span></span> <span data-ttu-id="39cf1-106">Os destinos de trabalho são hospedados em sistemas, de forma semelhante ao modo como os serviços são hospedados em sistemas.</span><span class="sxs-lookup"><span data-stu-id="39cf1-106">Job destinations are hosted on systems, similar to the way in which services are hosted on systems.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39cf1-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="39cf1-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="39cf1-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="39cf1-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="39cf1-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="39cf1-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="39cf1-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="39cf1-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39cf1-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39cf1-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{673E0A2C-E3D0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_JobDestination : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   SystemCreationClassName;
  string   SystemName;
};
```

## <a name="members"></a><span data-ttu-id="39cf1-112">Membros</span><span class="sxs-lookup"><span data-stu-id="39cf1-112">Members</span></span>

<span data-ttu-id="39cf1-113">A classe **CIM \_ JobDestination** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="39cf1-113">The **CIM\_JobDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="39cf1-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39cf1-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39cf1-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="39cf1-115">Properties</span></span>

<span data-ttu-id="39cf1-116">A classe **CIM \_ JobDestination** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="39cf1-116">The **CIM\_JobDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39cf1-117">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="39cf1-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39cf1-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39cf1-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39cf1-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-120">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="39cf1-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="39cf1-121">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="39cf1-121">A short textual description of the object.</span></span>

<span data-ttu-id="39cf1-122">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="39cf1-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39cf1-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="39cf1-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39cf1-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39cf1-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39cf1-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-126">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="39cf1-126">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="39cf1-127">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="39cf1-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="39cf1-128">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="39cf1-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="39cf1-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="39cf1-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39cf1-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39cf1-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39cf1-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-132">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="39cf1-132">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="39cf1-133">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="39cf1-133">A textual description of the object.</span></span>

<span data-ttu-id="39cf1-134">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="39cf1-134">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39cf1-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="39cf1-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39cf1-136">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="39cf1-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-137">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39cf1-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-138">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="39cf1-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="39cf1-139">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="39cf1-139">Indicates when the object was installed.</span></span> <span data-ttu-id="39cf1-140">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="39cf1-140">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="39cf1-141">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="39cf1-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39cf1-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="39cf1-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39cf1-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39cf1-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39cf1-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-145">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="39cf1-145">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="39cf1-146">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="39cf1-146">Label by which the object is known.</span></span> <span data-ttu-id="39cf1-147">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="39cf1-147">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="39cf1-148">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="39cf1-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="39cf1-149">**Status**</span><span class="sxs-lookup"><span data-stu-id="39cf1-149">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39cf1-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39cf1-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39cf1-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-152">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="39cf1-152">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="39cf1-153">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="39cf1-153">String that indicates the current status of the object.</span></span> <span data-ttu-id="39cf1-154">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="39cf1-154">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="39cf1-155">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="39cf1-155">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="39cf1-156">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="39cf1-156">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="39cf1-157">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="39cf1-157">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="39cf1-158">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="39cf1-158">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="39cf1-159">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="39cf1-159">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="39cf1-160">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="39cf1-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="39cf1-161">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="39cf1-161">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="39cf1-162">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="39cf1-162">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="39cf1-163">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="39cf1-163">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="39cf1-164">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="39cf1-164">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="39cf1-165">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="39cf1-165">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="39cf1-166">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="39cf1-166">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="39cf1-167">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="39cf1-167">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="39cf1-168">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="39cf1-168">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="39cf1-169">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="39cf1-169">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="39cf1-170">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="39cf1-170">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="39cf1-171">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="39cf1-171">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="39cf1-172">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="39cf1-172">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="39cf1-173">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="39cf1-173">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="39cf1-174">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="39cf1-174">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39cf1-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39cf1-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39cf1-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-177">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="39cf1-177">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="39cf1-178">Nome da classe de criação do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="39cf1-178">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="39cf1-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="39cf1-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39cf1-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="39cf1-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="39cf1-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39cf1-182">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Nome**")</span><span class="sxs-lookup"><span data-stu-id="39cf1-182">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_System**](cim-system.md).**Name**")</span></span>
</dt> </dl>

<span data-ttu-id="39cf1-183">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="39cf1-183">Scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39cf1-184">Comentários</span><span class="sxs-lookup"><span data-stu-id="39cf1-184">Remarks</span></span>

<span data-ttu-id="39cf1-185">A classe **CIM \_ JobDestination** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="39cf1-185">The **CIM\_JobDestination** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="39cf1-186">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="39cf1-186">WMI does not implement this class.</span></span>

<span data-ttu-id="39cf1-187">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="39cf1-187">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="39cf1-188">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="39cf1-188">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="39cf1-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39cf1-189">Requirements</span></span>



| <span data-ttu-id="39cf1-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="39cf1-190">Requirement</span></span> | <span data-ttu-id="39cf1-191">Valor</span><span class="sxs-lookup"><span data-stu-id="39cf1-191">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39cf1-192">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39cf1-192">Minimum supported client</span></span><br/> | <span data-ttu-id="39cf1-193">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39cf1-193">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39cf1-194">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="39cf1-194">Minimum supported server</span></span><br/> | <span data-ttu-id="39cf1-195">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39cf1-195">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39cf1-196">Namespace</span><span class="sxs-lookup"><span data-stu-id="39cf1-196">Namespace</span></span><br/>                | <span data-ttu-id="39cf1-197">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="39cf1-197">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="39cf1-198">MOF</span><span class="sxs-lookup"><span data-stu-id="39cf1-198">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39cf1-199"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39cf1-199"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="39cf1-200">DLL</span><span class="sxs-lookup"><span data-stu-id="39cf1-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39cf1-201"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39cf1-201"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39cf1-202">Confira também</span><span class="sxs-lookup"><span data-stu-id="39cf1-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39cf1-203">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="39cf1-203">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

