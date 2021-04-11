---
description: A \_ classe CIM MemoryMappedIO representa e/s mapeada pela memória da arquitetura do computador. Essa classe trata da memória e dos recursos de e/s de porta.
ms.assetid: cf418cd0-1ace-4d86-a878-65e81771787e
ms.tgt_platform: multiple
title: Classe CIM_MemoryMappedIO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryMappedIO
- CIM_MemoryMappedIO.Caption
- CIM_MemoryMappedIO.Description
- CIM_MemoryMappedIO.InstallDate
- CIM_MemoryMappedIO.Name
- CIM_MemoryMappedIO.Status
- CIM_MemoryMappedIO.CreationClassName
- CIM_MemoryMappedIO.CSCreationClassName
- CIM_MemoryMappedIO.CSName
- CIM_MemoryMappedIO.EndingAddress
- CIM_MemoryMappedIO.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 28ce4d60a6bba10e857afae7cc93d2e94c69b29f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010234"
---
# <a name="cim_memorymappedio-class"></a><span data-ttu-id="7b145-104">\_Classe CIM MemoryMappedIO</span><span class="sxs-lookup"><span data-stu-id="7b145-104">CIM\_MemoryMappedIO class</span></span>

<span data-ttu-id="7b145-105">A classe **CIM \_ MemoryMappedIO** representa e/s mapeada pela memória da arquitetura do computador.</span><span class="sxs-lookup"><span data-stu-id="7b145-105">The **CIM\_MemoryMappedIO** class represents computer architecture memory-mapped I/O.</span></span> <span data-ttu-id="7b145-106">Essa classe trata da memória e dos recursos de e/s de porta.</span><span class="sxs-lookup"><span data-stu-id="7b145-106">This class addresses memory and port I/O resources.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7b145-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="7b145-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7b145-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7b145-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7b145-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7b145-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7b145-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="7b145-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b145-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b145-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C51B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryMappedIO : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  uint64   EndingAddress;
  uint64   StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="7b145-112">Membros</span><span class="sxs-lookup"><span data-stu-id="7b145-112">Members</span></span>

<span data-ttu-id="7b145-113">A classe **CIM \_ MemoryMappedIO** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7b145-113">The **CIM\_MemoryMappedIO** class has these types of members:</span></span>

-   [<span data-ttu-id="7b145-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7b145-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b145-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7b145-115">Properties</span></span>

<span data-ttu-id="7b145-116">A classe **CIM \_ MemoryMappedIO** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7b145-116">The **CIM\_MemoryMappedIO** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b145-117">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="7b145-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b145-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b145-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b145-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b145-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b145-120">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="7b145-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="7b145-121">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="7b145-121">A short textual description of the object.</span></span>

<span data-ttu-id="7b145-122">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b145-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b145-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7b145-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b145-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b145-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b145-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b145-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b145-126">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b145-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b145-127">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="7b145-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="7b145-128">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="7b145-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="7b145-129">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="7b145-129">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b145-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b145-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b145-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b145-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b145-132">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7b145-132">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7b145-133">Propriedade **CreationClassName** do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="7b145-133">Scoping computer system's **CreationClassName** property.</span></span>

</dd> <dt>

<span data-ttu-id="7b145-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="7b145-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b145-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b145-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b145-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b145-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b145-137">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="7b145-137">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="7b145-138">Propriedade do **nome** do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="7b145-138">Scoping computer system's **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="7b145-139">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7b145-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b145-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b145-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b145-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b145-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b145-142">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="7b145-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="7b145-143">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="7b145-143">A textual description of the object.</span></span>

<span data-ttu-id="7b145-144">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b145-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b145-145">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="7b145-145">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b145-146">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7b145-146">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7b145-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b145-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b145-148">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|E/s 1,2 de memória DMTF mapeada \| )</span><span class="sxs-lookup"><span data-stu-id="7b145-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="7b145-149">Endereço final da e/s mapeada da memória.</span><span class="sxs-lookup"><span data-stu-id="7b145-149">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="7b145-150">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="7b145-150">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="7b145-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="7b145-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b145-152">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="7b145-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="7b145-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b145-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b145-154">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="7b145-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="7b145-155">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="7b145-155">Indicates when the object was installed.</span></span> <span data-ttu-id="7b145-156">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="7b145-156">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="7b145-157">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b145-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b145-158">**Nome**</span><span class="sxs-lookup"><span data-stu-id="7b145-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b145-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b145-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b145-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b145-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b145-161">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="7b145-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="7b145-162">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="7b145-162">Label by which the object is known.</span></span> <span data-ttu-id="7b145-163">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="7b145-163">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="7b145-164">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b145-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b145-165">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="7b145-165">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b145-166">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="7b145-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="7b145-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b145-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b145-168">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|E/s 1,1 de memória DMTF mapeada \| )</span><span class="sxs-lookup"><span data-stu-id="7b145-168">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="7b145-169">Endereço inicial da e/s mapeada da memória.</span><span class="sxs-lookup"><span data-stu-id="7b145-169">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="7b145-170">A propriedade do identificador de recurso de hardware deve ser definida com esse valor para construir a chave de recurso de e/s mapeada.</span><span class="sxs-lookup"><span data-stu-id="7b145-170">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="7b145-171">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="7b145-171">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="7b145-172">**Status**</span><span class="sxs-lookup"><span data-stu-id="7b145-172">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b145-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b145-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b145-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b145-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b145-175">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="7b145-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="7b145-176">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="7b145-176">String that indicates the current status of the object.</span></span> <span data-ttu-id="7b145-177">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="7b145-177">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="7b145-178">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="7b145-178">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="7b145-179">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="7b145-179">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="7b145-180">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="7b145-180">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="7b145-181">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="7b145-181">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="7b145-182">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="7b145-182">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="7b145-183">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="7b145-183">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="7b145-184">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="7b145-184">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="7b145-185">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="7b145-185">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="7b145-186">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="7b145-186">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="7b145-187">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="7b145-187">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7b145-188">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="7b145-188">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="7b145-189">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="7b145-189">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="7b145-190">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="7b145-190">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="7b145-191">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="7b145-191">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="7b145-192">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="7b145-192">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="7b145-193">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="7b145-193">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="7b145-194">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="7b145-194">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="7b145-195">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="7b145-195">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="7b145-196">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="7b145-196">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="7b145-197"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7b145-197"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="7b145-198">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b145-198">Remarks</span></span>

<span data-ttu-id="7b145-199">A classe **CIM \_ MemoryMappedIO** é derivada de [**\_ SystemResource CIM**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="7b145-199">The **CIM\_MemoryMappedIO** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span>

<span data-ttu-id="7b145-200">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="7b145-200">WMI does not implement this class.</span></span> <span data-ttu-id="7b145-201">Para classes derivadas do **CIM \_ MemoryMappedIO**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="7b145-201">For classes derived from **CIM\_MemoryMappedIO**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="7b145-202">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="7b145-202">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7b145-203">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="7b145-203">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b145-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b145-204">Requirements</span></span>



| <span data-ttu-id="7b145-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b145-205">Requirement</span></span> | <span data-ttu-id="7b145-206">Valor</span><span class="sxs-lookup"><span data-stu-id="7b145-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b145-207">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b145-207">Minimum supported client</span></span><br/> | <span data-ttu-id="7b145-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b145-208">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b145-209">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b145-209">Minimum supported server</span></span><br/> | <span data-ttu-id="7b145-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b145-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b145-211">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b145-211">Namespace</span></span><br/>                | <span data-ttu-id="7b145-212">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7b145-212">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7b145-213">MOF</span><span class="sxs-lookup"><span data-stu-id="7b145-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b145-214"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b145-214"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b145-215">DLL</span><span class="sxs-lookup"><span data-stu-id="7b145-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b145-216"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b145-216"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b145-217">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b145-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b145-218">**\_SYSTEMRESOURCE CIM**</span><span class="sxs-lookup"><span data-stu-id="7b145-218">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

