---
description: A \_ classe de sistema CIM agrega um conjunto enumerável de elementos do sistema gerenciado.
ms.assetid: cbfa60d4-36ae-4e0c-a57f-aabf219851d0
ms.tgt_platform: multiple
title: Classe CIM_System (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_System
- CIM_System.Caption
- CIM_System.Description
- CIM_System.InstallDate
- CIM_System.Status
- CIM_System.CreationClassName
- CIM_System.Name
- CIM_System.NameFormat
- CIM_System.PrimaryOwnerContact
- CIM_System.PrimaryOwnerName
- CIM_System.Roles
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef04e472e11c848aadb63c98b3dee2ea645a3ce7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920424"
---
# <a name="cim_system-class-cimwin32-wmi-providers"></a><span data-ttu-id="b410d-103">Classe CIM_System (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="b410d-103">CIM_System class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="b410d-104">A classe de **\_ sistema CIM** agrega um conjunto enumerável de elementos do sistema gerenciado.</span><span class="sxs-lookup"><span data-stu-id="b410d-104">The **CIM\_System** class aggregates an enumerable set of managed system elements.</span></span> <span data-ttu-id="b410d-105">A agregação funciona como um todo funcional.</span><span class="sxs-lookup"><span data-stu-id="b410d-105">The aggregation operates as a functional whole.</span></span> <span data-ttu-id="b410d-106">Em qualquer subclasse específica do sistema, há uma lista bem definida de classes de elementos do sistema gerenciado cujas instâncias devem ser agregadas.</span><span class="sxs-lookup"><span data-stu-id="b410d-106">Within any particular subclass of the system, there is a well-defined list of managed system element classes whose instances must be aggregated.</span></span>

<span data-ttu-id="b410d-107">O objeto do **\_ sistema CIM** e seus derivados são objetos de nível superior do CIM.</span><span class="sxs-lookup"><span data-stu-id="b410d-107">The **CIM\_System** object and its derivatives are top-level objects of CIM.</span></span> <span data-ttu-id="b410d-108">Eles fornecem o escopo para inúmeros componentes e precisam ter chaves de sistema exclusivas.</span><span class="sxs-lookup"><span data-stu-id="b410d-108">They provide the scope for numerous components and are required to have unique system keys.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b410d-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b410d-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b410d-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b410d-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b410d-111">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b410d-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="b410d-112">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b410d-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b410d-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b410d-113">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C524-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_System : CIM_LogicalElement
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

## <a name="members"></a><span data-ttu-id="b410d-114">Membros</span><span class="sxs-lookup"><span data-stu-id="b410d-114">Members</span></span>

<span data-ttu-id="b410d-115">A classe de **\_ sistema CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b410d-115">The **CIM\_System** class has these types of members:</span></span>

-   [<span data-ttu-id="b410d-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b410d-116">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b410d-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b410d-117">Properties</span></span>

<span data-ttu-id="b410d-118">A classe de **\_ sistema CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b410d-118">The **CIM\_System** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b410d-119">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="b410d-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b410d-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b410d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b410d-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b410d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b410d-122">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="b410d-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="b410d-123">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b410d-123">A short textual description of the object.</span></span>

<span data-ttu-id="b410d-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b410d-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b410d-125">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="b410d-125">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b410d-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b410d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b410d-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b410d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b410d-128">Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="b410d-128">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="b410d-129">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="b410d-129">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="b410d-130">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="b410d-130">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="b410d-131">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b410d-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b410d-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b410d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b410d-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b410d-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b410d-134">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="b410d-134">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="b410d-135">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b410d-135">A textual description of the object.</span></span>

<span data-ttu-id="b410d-136">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b410d-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b410d-137">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b410d-137">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b410d-138">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b410d-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b410d-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b410d-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b410d-140">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="b410d-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="b410d-141">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="b410d-141">Indicates when the object was installed.</span></span> <span data-ttu-id="b410d-142">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="b410d-142">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b410d-143">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b410d-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b410d-144">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b410d-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b410d-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b410d-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b410d-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b410d-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b410d-147">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b410d-147">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b410d-148">Define o rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b410d-148">Defines the label by which the object is known.</span></span>

</dd> <dt>

<span data-ttu-id="b410d-149">**NameFormat**</span><span class="sxs-lookup"><span data-stu-id="b410d-149">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b410d-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b410d-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b410d-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b410d-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b410d-152">Identifica como o nome do sistema foi gerado, usando a heurística de subclasse.</span><span class="sxs-lookup"><span data-stu-id="b410d-152">Identifies how the system name was generated, using the subclass heuristic.</span></span>

</dd> <dt>

<span data-ttu-id="b410d-153">**PrimaryOwnerContact**</span><span class="sxs-lookup"><span data-stu-id="b410d-153">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b410d-154">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b410d-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b410d-155">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b410d-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b410d-156">Como o proprietário do sistema primário pode ser alcançado (por exemplo, número de telefone ou endereço de email).</span><span class="sxs-lookup"><span data-stu-id="b410d-156">How the primary system owner can be reached (for example, phone number or email address).</span></span>

</dd> <dt>

<span data-ttu-id="b410d-157">**PrimaryOwnerName**</span><span class="sxs-lookup"><span data-stu-id="b410d-157">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b410d-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b410d-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b410d-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b410d-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b410d-160">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b410d-160">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b410d-161">Nome do proprietário do sistema primário.</span><span class="sxs-lookup"><span data-stu-id="b410d-161">Name of the primary system owner.</span></span>

</dd> <dt>

<span data-ttu-id="b410d-162">**Funções**</span><span class="sxs-lookup"><span data-stu-id="b410d-162">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b410d-163">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b410d-163">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b410d-164">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="b410d-164">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b410d-165">As funções que o sistema desempenha no ambiente de tecnologia da informação.</span><span class="sxs-lookup"><span data-stu-id="b410d-165">Roles the system plays in the information technology environment.</span></span> <span data-ttu-id="b410d-166">As subclasses do sistema podem substituir essa propriedade para definir valores de função explícitos.</span><span class="sxs-lookup"><span data-stu-id="b410d-166">Subclasses of the system can override this property to define explicit role values.</span></span> <span data-ttu-id="b410d-167">Como alternativa, um grupo de trabalho pode descrever a heurística, as convenções e as diretrizes para especificar funções.</span><span class="sxs-lookup"><span data-stu-id="b410d-167">Alternately, a working group can describe the heuristics, conventions, and guidelines for specifying roles.</span></span> <span data-ttu-id="b410d-168">Por exemplo, para uma instância de um sistema de rede, essa propriedade pode conter a cadeia de caracteres "switch" ou "Bridge".</span><span class="sxs-lookup"><span data-stu-id="b410d-168">For example, for an instance of a networking system, this property might contain the string "Switch" or "Bridge".</span></span>

</dd> <dt>

<span data-ttu-id="b410d-169">**Status**</span><span class="sxs-lookup"><span data-stu-id="b410d-169">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b410d-170">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b410d-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b410d-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b410d-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b410d-172">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="b410d-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="b410d-173">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="b410d-173">String that indicates the current status of the object.</span></span> <span data-ttu-id="b410d-174">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="b410d-174">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="b410d-175">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="b410d-175">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="b410d-176">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="b410d-176">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="b410d-177">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="b410d-177">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b410d-178">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="b410d-178">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b410d-179">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="b410d-179">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b410d-180">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b410d-180">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="b410d-181">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="b410d-181">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="b410d-182">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="b410d-182">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="b410d-183">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="b410d-183">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="b410d-184">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="b410d-184">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b410d-185">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="b410d-185">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="b410d-186">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="b410d-186">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="b410d-187">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="b410d-187">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="b410d-188">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="b410d-188">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="b410d-189">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="b410d-189">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="b410d-190">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="b410d-190">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="b410d-191">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="b410d-191">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="b410d-192">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="b410d-192">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="b410d-193">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="b410d-193">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="b410d-194"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b410d-194"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="b410d-195">Comentários</span><span class="sxs-lookup"><span data-stu-id="b410d-195">Remarks</span></span>

<span data-ttu-id="b410d-196">A classe de **\_ sistema CIM** é derivada de [**CIM \_ LogicalElement**](cim-logicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="b410d-196">The **CIM\_System** class is derived from [**CIM\_LogicalElement**](cim-logicalelement.md).</span></span>

<span data-ttu-id="b410d-197">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="b410d-197">WMI does not implement this class.</span></span> <span data-ttu-id="b410d-198">Para classes WMI derivadas do **\_ sistema CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b410d-198">For WMI classes derived from **CIM\_System**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="b410d-199">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b410d-199">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b410d-200">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b410d-200">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b410d-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b410d-201">Requirements</span></span>



| <span data-ttu-id="b410d-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="b410d-202">Requirement</span></span> | <span data-ttu-id="b410d-203">Valor</span><span class="sxs-lookup"><span data-stu-id="b410d-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b410d-204">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b410d-204">Minimum supported client</span></span><br/> | <span data-ttu-id="b410d-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b410d-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b410d-206">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b410d-206">Minimum supported server</span></span><br/> | <span data-ttu-id="b410d-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b410d-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b410d-208">Namespace</span><span class="sxs-lookup"><span data-stu-id="b410d-208">Namespace</span></span><br/>                | <span data-ttu-id="b410d-209">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b410d-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b410d-210">MOF</span><span class="sxs-lookup"><span data-stu-id="b410d-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b410d-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b410d-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b410d-212">DLL</span><span class="sxs-lookup"><span data-stu-id="b410d-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b410d-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b410d-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b410d-214">Confira também</span><span class="sxs-lookup"><span data-stu-id="b410d-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b410d-215">**CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="b410d-215">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> </dl>

 

