---
description: A \_ classe CIM SoftwareFeature representa uma função ou um recurso específico de um produto ou sistema de aplicativos.
ms.assetid: 7beeb32c-d285-44f7-adeb-3b661d8ab037
ms.tgt_platform: multiple
title: Classe CIM_SoftwareFeature
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareFeature
- CIM_SoftwareFeature.Caption
- CIM_SoftwareFeature.Description
- CIM_SoftwareFeature.IdentifyingNumber
- CIM_SoftwareFeature.InstallDate
- CIM_SoftwareFeature.Name
- CIM_SoftwareFeature.ProductName
- CIM_SoftwareFeature.Status
- CIM_SoftwareFeature.Vendor
- CIM_SoftwareFeature.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3959f7b99170cf1470d3688a101e4858f70e9a99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756440"
---
# <a name="cim_softwarefeature-class"></a><span data-ttu-id="f7248-103">\_Classe CIM SoftwareFeature</span><span class="sxs-lookup"><span data-stu-id="f7248-103">CIM\_SoftwareFeature class</span></span>

<span data-ttu-id="f7248-104">A classe **CIM \_ SoftwareFeature** representa uma função ou um recurso específico de um produto ou sistema de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="f7248-104">The **CIM\_SoftwareFeature** class represents a particular function or capability of a product or application system.</span></span> <span data-ttu-id="f7248-105">Essa classe reflete um nível de granularidade que é significativo para um usuário de um produto em vez das unidades que refletem como o produto é compilado ou empacotado (capturado usando uma classe [**CIM \_ softwareelement**](cim-softwareelement.md) ).</span><span class="sxs-lookup"><span data-stu-id="f7248-105">This class reflects a level of granularity that is meaningful to a user of a product rather than the units that reflect how the product is built or packaged (captured using a [**CIM\_SoftwareElement**](cim-softwareelement.md) class).</span></span> <span data-ttu-id="f7248-106">Quando um recurso de software pode existir em várias plataformas ou sistemas operacionais, o recurso de software é uma coleção dos elementos de software para as diferentes plataformas.</span><span class="sxs-lookup"><span data-stu-id="f7248-106">When a software feature can exist on multiple platforms or operating systems, the software feature is a collection of the software elements for the different platforms.</span></span> <span data-ttu-id="f7248-107">Nesse caso, os usuários do modelo estarão geralmente interessados em uma subcoleção dos elementos de software necessários para uma plataforma específica.</span><span class="sxs-lookup"><span data-stu-id="f7248-107">In which case, the users of the model will be typically interested in a sub-collection of the software elements required for a particular platform.</span></span> <span data-ttu-id="f7248-108">Como os recursos são entregues por meio de produtos, os recursos de software são sempre definidos no contexto de uma classe de [**\_ produto CIM**](cim-product.md) usando a associação de [**\_ ProductSoftwareFeatures do CIM**](cim-productsoftwarefeatures.md) .</span><span class="sxs-lookup"><span data-stu-id="f7248-108">Because features are delivered through products, software features are always defined in the context of a [**CIM\_Product**](cim-product.md) class using the [**CIM\_ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) association.</span></span> <span data-ttu-id="f7248-109">Opcionalmente, os recursos de software de um ou mais produtos podem ser organizados em sistemas de aplicativos usando a associação [**\_ ApplicationSystemSoftwareFeature do CIM**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="f7248-109">Optionally, software features from one or more products can be organized into application systems using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f7248-110">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="f7248-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f7248-111">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f7248-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f7248-112">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f7248-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f7248-113">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="f7248-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7248-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7248-114">Syntax</span></span>

``` syntax
[UUID("{E527D7F2-E3D4-11d2-8601-0000F8102E5F}"), abstract, AMENDMENT]
class CIM_SoftwareFeature : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  string   IdentifyingNumber;
  datetime InstallDate;
  string   Name;
  string   ProductName;
  string   Status;
  string   Vendor;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="f7248-115">Membros</span><span class="sxs-lookup"><span data-stu-id="f7248-115">Members</span></span>

<span data-ttu-id="f7248-116">A classe **CIM \_ SoftwareFeature** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f7248-116">The **CIM\_SoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="f7248-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f7248-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f7248-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f7248-118">Properties</span></span>

<span data-ttu-id="f7248-119">A classe **CIM \_ SoftwareFeature** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f7248-119">The **CIM\_SoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f7248-120">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="f7248-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7248-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7248-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7248-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7248-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7248-123">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f7248-123">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f7248-124">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f7248-124">Short textual description of the object.</span></span>

<span data-ttu-id="f7248-125">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7248-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7248-126">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f7248-126">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7248-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7248-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7248-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7248-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7248-129">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="f7248-129">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f7248-130">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f7248-130">Textual description of the object.</span></span>

<span data-ttu-id="f7248-131">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7248-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7248-132">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="f7248-132">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7248-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7248-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7248-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7248-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7248-135">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ produto CIM**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="f7248-135">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**IdentifyingNumber**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="f7248-136">Identificação do produto, como um número de série no software ou um número de chip em um chip de hardware.</span><span class="sxs-lookup"><span data-stu-id="f7248-136">Product identification, such as a serial number on software or a die number on a hardware chip.</span></span>

</dd> <dt>

<span data-ttu-id="f7248-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f7248-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7248-138">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f7248-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f7248-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7248-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7248-140">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="f7248-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f7248-141">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="f7248-141">Date and time the object was installed.</span></span> <span data-ttu-id="f7248-142">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="f7248-142">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="f7248-143">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7248-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7248-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="f7248-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7248-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7248-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7248-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7248-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7248-147">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f7248-147">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f7248-148">Rótulo pelo qual o objeto é conhecido fora do sistema de processamento de dados.</span><span class="sxs-lookup"><span data-stu-id="f7248-148">Label by which the object is known outside of the data processing system.</span></span> <span data-ttu-id="f7248-149">O rótulo é um nome legível que identifica exclusivamente o elemento no contexto do namespace do elemento.</span><span class="sxs-lookup"><span data-stu-id="f7248-149">The label is a human-readable name that uniquely identifies the element in the context of the element's namespace.</span></span>

<span data-ttu-id="f7248-150">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7248-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7248-151">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="f7248-151">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7248-152">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7248-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7248-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7248-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7248-154">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ produto CIM**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="f7248-154">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Name**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="f7248-155">Nome do produto usado normalmente.</span><span class="sxs-lookup"><span data-stu-id="f7248-155">Commonly used product name.</span></span>

</dd> <dt>

<span data-ttu-id="f7248-156">**Status**</span><span class="sxs-lookup"><span data-stu-id="f7248-156">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7248-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7248-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7248-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7248-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7248-159">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="f7248-159">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f7248-160">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="f7248-160">Current status of the object.</span></span>

<span data-ttu-id="f7248-161">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7248-161">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f7248-162">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f7248-162">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f7248-163">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="f7248-163">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f7248-164">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="f7248-164">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f7248-165">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="f7248-165">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f7248-166">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="f7248-166">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f7248-167">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="f7248-167">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f7248-168">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="f7248-168">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f7248-169">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="f7248-169">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f7248-170">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="f7248-170">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f7248-171">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="f7248-171">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f7248-172">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="f7248-172">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f7248-173">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="f7248-173">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f7248-174">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="f7248-174">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f7248-175">**Fornecedor**</span><span class="sxs-lookup"><span data-stu-id="f7248-175">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7248-176">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7248-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7248-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7248-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7248-178">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ produto CIM**](cim-product.md).**Vendor**") [**, \_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 1,1 ")</span><span class="sxs-lookup"><span data-stu-id="f7248-178">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Vendor**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="f7248-179">Nome do fornecedor do produto, que corresponde à propriedade **Vendor** no objeto Product do padrão de troca de solução DMTF.</span><span class="sxs-lookup"><span data-stu-id="f7248-179">Name of the product's supplier, which corresponds to the **Vendor** property in the product object of the DMTF Solution Exchange Standard.</span></span>

</dd> <dt>

<span data-ttu-id="f7248-180">**Versão**</span><span class="sxs-lookup"><span data-stu-id="f7248-180">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f7248-181">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f7248-181">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f7248-182">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f7248-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f7248-183">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ produto CIM**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" DMTF \| ComponentID \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="f7248-183">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Product**](cim-product.md).**Version**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="f7248-184">Informações de versão do produto, que corresponde à propriedade **version** no objeto Product do padrão de troca de solução DMTF.</span><span class="sxs-lookup"><span data-stu-id="f7248-184">Product version information, which corresponds to the **Version** property in the product object of the DMTF Solution Exchange Standard.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f7248-185">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7248-185">Remarks</span></span>

<span data-ttu-id="f7248-186">A classe **CIM \_ SoftwareFeature** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="f7248-186">The **CIM\_SoftwareFeature** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="f7248-187">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="f7248-187">WMI does not implement this class.</span></span> <span data-ttu-id="f7248-188">Para classes WMI derivadas do **CIM \_ SoftwareFeature**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f7248-188">For WMI classes derived from **CIM\_SoftwareFeature**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f7248-189">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="f7248-189">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f7248-190">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="f7248-190">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7248-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7248-191">Requirements</span></span>



| <span data-ttu-id="f7248-192">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7248-192">Requirement</span></span> | <span data-ttu-id="f7248-193">Valor</span><span class="sxs-lookup"><span data-stu-id="f7248-193">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7248-194">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7248-194">Minimum supported client</span></span><br/> | <span data-ttu-id="f7248-195">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7248-195">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f7248-196">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f7248-196">Minimum supported server</span></span><br/> | <span data-ttu-id="f7248-197">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7248-197">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f7248-198">Namespace</span><span class="sxs-lookup"><span data-stu-id="f7248-198">Namespace</span></span><br/>                | <span data-ttu-id="f7248-199">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f7248-199">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f7248-200">MOF</span><span class="sxs-lookup"><span data-stu-id="f7248-200">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f7248-201"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f7248-201"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f7248-202">DLL</span><span class="sxs-lookup"><span data-stu-id="f7248-202">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7248-203"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7248-203"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7248-204">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7248-204">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7248-205">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="f7248-205">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

