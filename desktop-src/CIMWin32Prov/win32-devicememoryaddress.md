---
description: A \_ classe WMI DeviceMemoryAddress do Win32 representa um endereço de memória do dispositivo em um sistema de computador executando o Windows.
ms.assetid: f0a70724-5ced-47fe-b17e-e153e65b80df
ms.tgt_platform: multiple
title: Classe Win32_DeviceMemoryAddress
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aa7472e3c20808ff52f6f45b0dca57fd19f9dd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920494"
---
# <a name="win32_devicememoryaddress-class"></a><span data-ttu-id="8bf38-103">\_Classe Win32 DeviceMemoryAddress</span><span class="sxs-lookup"><span data-stu-id="8bf38-103">Win32\_DeviceMemoryAddress class</span></span>

<span data-ttu-id="8bf38-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ DeviceMemoryAddress do Win32** representa um endereço de memória do dispositivo em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="8bf38-104">The **Win32\_DeviceMemoryAddress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a device memory address on a computer system running Windows.</span></span>

<span data-ttu-id="8bf38-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="8bf38-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="8bf38-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="8bf38-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bf38-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8bf38-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceMemoryAddress : Win32_SystemMemoryResource
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   MemoryType;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="8bf38-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8bf38-108">Members</span></span>

<span data-ttu-id="8bf38-109">A classe **Win32 \_ DeviceMemoryAddress** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="8bf38-109">The **Win32\_DeviceMemoryAddress** class has these types of members:</span></span>

-   [<span data-ttu-id="8bf38-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8bf38-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8bf38-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="8bf38-111">Properties</span></span>

<span data-ttu-id="8bf38-112">A classe **Win32 \_ DeviceMemoryAddress** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="8bf38-112">The **Win32\_DeviceMemoryAddress** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bf38-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="8bf38-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf38-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8bf38-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bf38-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-116">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="8bf38-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="8bf38-117">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="8bf38-117">Short description of the object a one-line string.</span></span>

<span data-ttu-id="8bf38-118">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8bf38-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bf38-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8bf38-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf38-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8bf38-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bf38-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-122">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8bf38-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8bf38-123">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="8bf38-123">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="8bf38-124">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="8bf38-124">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="8bf38-125">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="8bf38-125">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bf38-126">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="8bf38-126">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf38-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8bf38-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bf38-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-129">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="8bf38-129">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="8bf38-130">Nome da classe de criação do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="8bf38-130">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="8bf38-131">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="8bf38-131">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bf38-132">**CSName**</span><span class="sxs-lookup"><span data-stu-id="8bf38-132">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf38-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8bf38-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bf38-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-135">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="8bf38-135">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="8bf38-136">Nome do sistema de computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="8bf38-136">Name of the scoping computer system.</span></span>

<span data-ttu-id="8bf38-137">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="8bf38-137">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bf38-138">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8bf38-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf38-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8bf38-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bf38-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-141">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="8bf38-141">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="8bf38-142">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="8bf38-142">Description of the object.</span></span>

<span data-ttu-id="8bf38-143">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8bf38-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bf38-144">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="8bf38-144">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf38-145">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8bf38-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bf38-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-147">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|E/s 1,2 de memória DMTF mapeada \| )</span><span class="sxs-lookup"><span data-stu-id="8bf38-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="8bf38-148">Endereço final da e/s mapeada pela memória.</span><span class="sxs-lookup"><span data-stu-id="8bf38-148">Ending address of memory-mapped I/O.</span></span>

<span data-ttu-id="8bf38-149">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="8bf38-149">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="8bf38-150">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8bf38-150">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8bf38-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="8bf38-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf38-152">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="8bf38-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bf38-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-154">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="8bf38-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="8bf38-155">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="8bf38-155">Date and time the object was installed.</span></span> <span data-ttu-id="8bf38-156">Essa propriedade não requer um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="8bf38-156">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="8bf38-157">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8bf38-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bf38-158">**Memorytype**</span><span class="sxs-lookup"><span data-stu-id="8bf38-158">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf38-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8bf38-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bf38-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-161">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| sinalizadores de \| \_ descritor de recursos parciais do win32api SystemStructures cm \_ \_ \| ")</span><span class="sxs-lookup"><span data-stu-id="8bf38-161">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SystemStructures\|CM\_PARTIAL\_RESOURCE\_DESCRIPTOR\|Flags")</span></span>
</dt> </dl>

<span data-ttu-id="8bf38-162">Características do recurso de memória no sistema de computador que executa o Windows.</span><span class="sxs-lookup"><span data-stu-id="8bf38-162">Characteristics of the memory resource on the computer system running Windows.</span></span> <span data-ttu-id="8bf38-163">Os valores são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="8bf38-163">Values are the following.</span></span>

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span data-ttu-id="8bf38-164"><span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**ReadWrite** ("ReadWrite")</span><span class="sxs-lookup"><span data-stu-id="8bf38-164"><span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**ReadWrite** ("ReadWrite")</span></span>


</dt> <dd>

<span data-ttu-id="8bf38-165">A memória pode ser lida e gravada.</span><span class="sxs-lookup"><span data-stu-id="8bf38-165">The memory can be both read and written.</span></span>

</dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span data-ttu-id="8bf38-166"><span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**ReadOnly** ("ReadOnly")</span><span class="sxs-lookup"><span data-stu-id="8bf38-166"><span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**ReadOnly** ("ReadOnly")</span></span>


</dt> <dd>

<span data-ttu-id="8bf38-167">A memória é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8bf38-167">The memory is read-only.</span></span>

</dd> <dt>

<span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>

<span data-ttu-id="8bf38-168"><span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**WriteOnly** ("WriteOnly")</span><span class="sxs-lookup"><span data-stu-id="8bf38-168"><span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**WriteOnly** ("WriteOnly")</span></span>


</dt> <dd>

<span data-ttu-id="8bf38-169">A memória só pode ser gravada.</span><span class="sxs-lookup"><span data-stu-id="8bf38-169">The memory can only be written.</span></span>

</dd> <dt>

<span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>

<span data-ttu-id="8bf38-170"><span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Prefetch** ("pré-busca")</span><span class="sxs-lookup"><span data-stu-id="8bf38-170"><span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Prefetchable** ("Prefetchable")</span></span>


</dt> <dd>

<span data-ttu-id="8bf38-171">Um bloco de memória é copiado da memória principal em um buffer pequeno gerenciado pelo chipset de memória.</span><span class="sxs-lookup"><span data-stu-id="8bf38-171">A block of memory is copied from main memory into a small buffer managed by the memory chipset.</span></span> <span data-ttu-id="8bf38-172">Operações de leitura repetidas da mesma parte da memória são mais rápidas com memória de pré-busca.</span><span class="sxs-lookup"><span data-stu-id="8bf38-172">Repeated read operations from the same part of memory are faster with prefetchable memory.</span></span>

</dd> <dt>

<span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>

<span data-ttu-id="8bf38-173"><span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**CombinedWrite** ("CombinedWrite")</span><span class="sxs-lookup"><span data-stu-id="8bf38-173"><span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**CombinedWrite** ("CombinedWrite")</span></span>


</dt> <dd>

<span data-ttu-id="8bf38-174">TBD</span><span class="sxs-lookup"><span data-stu-id="8bf38-174">TBD</span></span>

</dd> <dt>

<span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>

<span data-ttu-id="8bf38-175"><span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ("Type24")</span><span class="sxs-lookup"><span data-stu-id="8bf38-175"><span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ("Type24")</span></span>


</dt> <dd>

<span data-ttu-id="8bf38-176">TBD</span><span class="sxs-lookup"><span data-stu-id="8bf38-176">TBD</span></span>

</dd> <dt>

<span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>

<span data-ttu-id="8bf38-177"><span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>**Armazenável em cache** ("armazenável em cache")</span><span class="sxs-lookup"><span data-stu-id="8bf38-177"><span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>**Cacheable** ("Cacheable")</span></span>


</dt> <dd>

<span data-ttu-id="8bf38-178">TBD</span><span class="sxs-lookup"><span data-stu-id="8bf38-178">TBD</span></span>

</dd> <dt>

<span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>

<span data-ttu-id="8bf38-179"><span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**WindowDecode** ("WindowDecode")</span><span class="sxs-lookup"><span data-stu-id="8bf38-179"><span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**WindowDecode** ("WindowDecode")</span></span>


</dt> <dd>

<span data-ttu-id="8bf38-180">TBD</span><span class="sxs-lookup"><span data-stu-id="8bf38-180">TBD</span></span>

</dd> <dt>

<span id="Bar"></span><span id="bar"></span><span id="BAR"></span>

<span data-ttu-id="8bf38-181"><span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Barra** ("barra")</span><span class="sxs-lookup"><span data-stu-id="8bf38-181"><span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Bar** ("Bar")</span></span>


</dt> <dd>

<span data-ttu-id="8bf38-182">TBD</span><span class="sxs-lookup"><span data-stu-id="8bf38-182">TBD</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="8bf38-183">**Nome**</span><span class="sxs-lookup"><span data-stu-id="8bf38-183">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf38-184">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8bf38-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-185">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bf38-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-186">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="8bf38-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="8bf38-187">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="8bf38-187">Label by which the object is known.</span></span> <span data-ttu-id="8bf38-188">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="8bf38-188">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="8bf38-189">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8bf38-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="8bf38-190">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="8bf38-190">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf38-191">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="8bf38-191">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bf38-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-193">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartingAddress"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|E/s 1,1 de memória DMTF mapeada \| )</span><span class="sxs-lookup"><span data-stu-id="8bf38-193">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartingAddress"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="8bf38-194">Endereço inicial da e/s mapeada pela memória.</span><span class="sxs-lookup"><span data-stu-id="8bf38-194">Starting address of memory-mapped I/O.</span></span> <span data-ttu-id="8bf38-195">A propriedade do identificador de recurso de hardware deve ser definida com esse valor para construir a chave de recurso de e/s mapeada.</span><span class="sxs-lookup"><span data-stu-id="8bf38-195">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="8bf38-196">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="8bf38-196">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="8bf38-197">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="8bf38-197">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="8bf38-198">**Status**</span><span class="sxs-lookup"><span data-stu-id="8bf38-198">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bf38-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="8bf38-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8bf38-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bf38-201">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="8bf38-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="8bf38-202">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="8bf38-202">Current status of the object.</span></span> <span data-ttu-id="8bf38-203">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="8bf38-203">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="8bf38-204">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="8bf38-204">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="8bf38-205">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="8bf38-205">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="8bf38-206">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="8bf38-206">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="8bf38-207">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="8bf38-207">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="8bf38-208">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="8bf38-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="8bf38-209">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8bf38-209">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="8bf38-210">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="8bf38-210">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="8bf38-211">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="8bf38-211">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="8bf38-212">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="8bf38-212">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="8bf38-213">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="8bf38-213">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="8bf38-214">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="8bf38-214">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="8bf38-215">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="8bf38-215">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="8bf38-216">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="8bf38-216">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="8bf38-217">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="8bf38-217">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="8bf38-218">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="8bf38-218">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="8bf38-219">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="8bf38-219">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="8bf38-220">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="8bf38-220">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="8bf38-221">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="8bf38-221">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="8bf38-222"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8bf38-222"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="8bf38-223">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bf38-223">Remarks</span></span>

<span data-ttu-id="8bf38-224">A classe **Win32 \_ DeviceMemoryAddress** é derivada de [**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md).</span><span class="sxs-lookup"><span data-stu-id="8bf38-224">The **Win32\_DeviceMemoryAddress** class is derived from [**Win32\_SystemMemoryResource**](win32-systemmemoryresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8bf38-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bf38-225">Requirements</span></span>



| <span data-ttu-id="8bf38-226">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bf38-226">Requirement</span></span> | <span data-ttu-id="8bf38-227">Valor</span><span class="sxs-lookup"><span data-stu-id="8bf38-227">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bf38-228">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bf38-228">Minimum supported client</span></span><br/> | <span data-ttu-id="8bf38-229">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8bf38-229">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8bf38-230">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8bf38-230">Minimum supported server</span></span><br/> | <span data-ttu-id="8bf38-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bf38-231">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8bf38-232">Namespace</span><span class="sxs-lookup"><span data-stu-id="8bf38-232">Namespace</span></span><br/>                | <span data-ttu-id="8bf38-233">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8bf38-233">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8bf38-234">MOF</span><span class="sxs-lookup"><span data-stu-id="8bf38-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bf38-235"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bf38-235"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bf38-236">DLL</span><span class="sxs-lookup"><span data-stu-id="8bf38-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bf38-237"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bf38-237"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8bf38-238">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bf38-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8bf38-239">**\_SystemMemoryResource Win32**</span><span class="sxs-lookup"><span data-stu-id="8bf38-239">**Win32\_SystemMemoryResource**</span></span>](win32-systemmemoryresource.md)
</dt> <dt>

[<span data-ttu-id="8bf38-240">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="8bf38-240">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

