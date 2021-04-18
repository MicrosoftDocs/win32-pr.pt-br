---
description: A \_ classe CIM ApplicationSystem representa um sistema de aplicativo ou de software que dá suporte a uma função comercial específica que pode ser gerenciada como uma unidade independente.
ms.assetid: 42471863-ff6c-4464-8b0a-7dad2fd11934
ms.tgt_platform: multiple
title: Classe CIM_ApplicationSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystem
- CIM_ApplicationSystem.Caption
- CIM_ApplicationSystem.Description
- CIM_ApplicationSystem.InstallDate
- CIM_ApplicationSystem.Status
- CIM_ApplicationSystem.CreationClassName
- CIM_ApplicationSystem.Name
- CIM_ApplicationSystem.NameFormat
- CIM_ApplicationSystem.PrimaryOwnerContact
- CIM_ApplicationSystem.PrimaryOwnerName
- CIM_ApplicationSystem.Roles
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a69c05b11c5f3c623824783ed13f42c0a3eab801
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771737"
---
# <a name="cim_applicationsystem-class"></a><span data-ttu-id="15cd0-103">\_Classe CIM ApplicationSystem</span><span class="sxs-lookup"><span data-stu-id="15cd0-103">CIM\_ApplicationSystem class</span></span>

<span data-ttu-id="15cd0-104">A classe **CIM \_ ApplicationSystem** representa um sistema de aplicativo ou de software que dá suporte a uma função comercial específica que pode ser gerenciada como uma unidade independente.</span><span class="sxs-lookup"><span data-stu-id="15cd0-104">The **CIM\_ApplicationSystem** class represents an application or software system that supports a particular business function that can be managed as an independent unit.</span></span> <span data-ttu-id="15cd0-105">Esse sistema pode ser decomposto em seus componentes funcionais usando a classe [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="15cd0-105">Such a system can be decomposed into its functional components using the [**CIM\_SoftwareFeature**](cim-softwarefeature.md) class.</span></span> <span data-ttu-id="15cd0-106">Os recursos de software para um determinado aplicativo ou sistema de software estão localizados usando a associação [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) .</span><span class="sxs-lookup"><span data-stu-id="15cd0-106">The software features for a particular application or software system are located using the [**CIM\_ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="15cd0-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="15cd0-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="15cd0-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="15cd0-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="15cd0-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="15cd0-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="15cd0-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="15cd0-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="15cd0-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15cd0-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{120BB700-DB2B-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ApplicationSystem : CIM_System
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerContact;
  string   PrimaryOwnerName;
  string   Roles[];
};
```

## <a name="members"></a><span data-ttu-id="15cd0-112">Membros</span><span class="sxs-lookup"><span data-stu-id="15cd0-112">Members</span></span>

<span data-ttu-id="15cd0-113">A classe **CIM \_ ApplicationSystem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="15cd0-113">The **CIM\_ApplicationSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="15cd0-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="15cd0-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="15cd0-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="15cd0-115">Properties</span></span>

<span data-ttu-id="15cd0-116">A classe **CIM \_ ApplicationSystem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="15cd0-116">The **CIM\_ApplicationSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="15cd0-117">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="15cd0-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15cd0-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="15cd0-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15cd0-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-120">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="15cd0-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="15cd0-121">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="15cd0-121">A short textual description of the object.</span></span>

<span data-ttu-id="15cd0-122">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="15cd0-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="15cd0-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="15cd0-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15cd0-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="15cd0-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15cd0-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-126">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="15cd0-126">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="15cd0-127">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="15cd0-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="15cd0-128">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="15cd0-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="15cd0-129">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="15cd0-129">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="15cd0-130">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="15cd0-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15cd0-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="15cd0-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15cd0-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-133">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="15cd0-133">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="15cd0-134">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="15cd0-134">A textual description of the object.</span></span>

<span data-ttu-id="15cd0-135">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="15cd0-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="15cd0-136">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="15cd0-136">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15cd0-137">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="15cd0-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-138">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15cd0-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-139">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="15cd0-139">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="15cd0-140">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="15cd0-140">Indicates when the object was installed.</span></span> <span data-ttu-id="15cd0-141">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="15cd0-141">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="15cd0-142">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="15cd0-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="15cd0-143">**Nome**</span><span class="sxs-lookup"><span data-stu-id="15cd0-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15cd0-144">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="15cd0-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15cd0-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-146">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="15cd0-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="15cd0-147">Define o rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="15cd0-147">Defines the label by which the object is known.</span></span>

<span data-ttu-id="15cd0-148">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="15cd0-148">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="15cd0-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="15cd0-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15cd0-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="15cd0-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15cd0-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15cd0-152">Identifica como o nome do sistema foi gerado, usando a heurística de subclasse.</span><span class="sxs-lookup"><span data-stu-id="15cd0-152">Identifies how the system name was generated, using the subclass heuristic.</span></span>

<span data-ttu-id="15cd0-153">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="15cd0-153">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="15cd0-154">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="15cd0-154">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15cd0-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="15cd0-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15cd0-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="15cd0-157">Como o proprietário do sistema primário pode ser alcançado (por exemplo, número de telefone ou endereço de email).</span><span class="sxs-lookup"><span data-stu-id="15cd0-157">How the primary system owner can be reached (for example, phone number or email address).</span></span>

<span data-ttu-id="15cd0-158">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="15cd0-158">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="15cd0-159">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="15cd0-159">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15cd0-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="15cd0-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15cd0-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-162">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="15cd0-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="15cd0-163">Nome do proprietário do sistema primário.</span><span class="sxs-lookup"><span data-stu-id="15cd0-163">Name of the primary system owner.</span></span>

<span data-ttu-id="15cd0-164">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="15cd0-164">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="15cd0-165">**Funções**</span><span class="sxs-lookup"><span data-stu-id="15cd0-165">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15cd0-166">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="15cd0-166">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-167">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="15cd0-167">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="15cd0-168">As funções que o sistema desempenha no ambiente de tecnologia da informação.</span><span class="sxs-lookup"><span data-stu-id="15cd0-168">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="15cd0-169">As subclasses do sistema podem substituir essa propriedade para definir valores de função explícitos.</span><span class="sxs-lookup"><span data-stu-id="15cd0-169">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="15cd0-170">Como alternativa, um grupo de trabalho pode descrever a heurística, as convenções e as diretrizes para especificar funções.</span><span class="sxs-lookup"><span data-stu-id="15cd0-170">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="15cd0-171">Por exemplo, para uma instância de um sistema de rede, essa propriedade pode conter a cadeia de caracteres "switch" ou "Bridge".</span><span class="sxs-lookup"><span data-stu-id="15cd0-171">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

<span data-ttu-id="15cd0-172">Essa propriedade é herdada [**do \_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="15cd0-172">This property is inherited from [**CIM\_System**](cim-system.md).</span></span>

</dd> <dt>

<span data-ttu-id="15cd0-173">**Status**</span><span class="sxs-lookup"><span data-stu-id="15cd0-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="15cd0-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="15cd0-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="15cd0-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="15cd0-176">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="15cd0-176">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="15cd0-177">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="15cd0-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="15cd0-178">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="15cd0-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="15cd0-179">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="15cd0-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="15cd0-180">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="15cd0-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="15cd0-181">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="15cd0-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="15cd0-182">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="15cd0-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="15cd0-183">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="15cd0-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="15cd0-184">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="15cd0-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="15cd0-185">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="15cd0-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="15cd0-186">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="15cd0-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="15cd0-187">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="15cd0-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="15cd0-188">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="15cd0-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="15cd0-189">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="15cd0-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="15cd0-190">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="15cd0-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="15cd0-191">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="15cd0-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="15cd0-192">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="15cd0-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="15cd0-193">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="15cd0-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="15cd0-194">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="15cd0-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="15cd0-195">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="15cd0-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="15cd0-196">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="15cd0-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="15cd0-197">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="15cd0-197">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="15cd0-198"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="15cd0-198"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="15cd0-199">Comentários</span><span class="sxs-lookup"><span data-stu-id="15cd0-199">Remarks</span></span>

<span data-ttu-id="15cd0-200">A classe **CIM \_ ApplicationSystem** é derivada do [**\_ sistema CIM**](cim-system.md).</span><span class="sxs-lookup"><span data-stu-id="15cd0-200">The **CIM\_ApplicationSystem** class is derived from [**CIM\_System**](cim-system.md).</span></span>

<span data-ttu-id="15cd0-201">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="15cd0-201">WMI does not implement this class.</span></span>

<span data-ttu-id="15cd0-202">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="15cd0-202">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="15cd0-203">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="15cd0-203">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="15cd0-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15cd0-204">Requirements</span></span>



| <span data-ttu-id="15cd0-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="15cd0-205">Requirement</span></span> | <span data-ttu-id="15cd0-206">Valor</span><span class="sxs-lookup"><span data-stu-id="15cd0-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15cd0-207">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15cd0-207">Minimum supported client</span></span><br/> | <span data-ttu-id="15cd0-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15cd0-208">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15cd0-209">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15cd0-209">Minimum supported server</span></span><br/> | <span data-ttu-id="15cd0-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15cd0-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15cd0-211">Namespace</span><span class="sxs-lookup"><span data-stu-id="15cd0-211">Namespace</span></span><br/>                | <span data-ttu-id="15cd0-212">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="15cd0-212">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="15cd0-213">MOF</span><span class="sxs-lookup"><span data-stu-id="15cd0-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15cd0-214"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15cd0-214"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="15cd0-215">DLL</span><span class="sxs-lookup"><span data-stu-id="15cd0-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15cd0-216"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15cd0-216"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15cd0-217">Confira também</span><span class="sxs-lookup"><span data-stu-id="15cd0-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15cd0-218">**\_Sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="15cd0-218">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

