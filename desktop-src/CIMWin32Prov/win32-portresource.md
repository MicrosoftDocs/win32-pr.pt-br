---
description: A \_ classe WMI PortResource do Win32 representa uma porta de e/s em um sistema de computador executando o Windows.
ms.assetid: 820f4f49-571c-4044-aefc-69bac5d59e6f
ms.tgt_platform: multiple
title: Classe Win32_PortResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortResource
- Win32_PortResource.Alias
- Win32_PortResource.Caption
- Win32_PortResource.CreationClassName
- Win32_PortResource.CSCreationClassName
- Win32_PortResource.CSName
- Win32_PortResource.Description
- Win32_PortResource.EndingAddress
- Win32_PortResource.InstallDate
- Win32_PortResource.Name
- Win32_PortResource.StartingAddress
- Win32_PortResource.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3c08424dd1aee555068c78a9308afe732634c61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920208"
---
# <a name="win32_portresource-class"></a><span data-ttu-id="5ee6e-103">\_Classe Win32 PortResource</span><span class="sxs-lookup"><span data-stu-id="5ee6e-103">Win32\_PortResource class</span></span>

<span data-ttu-id="5ee6e-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PortResource do Win32** representa uma porta de e/s em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-104">The **Win32\_PortResource** [WMI class](../wmisdk/retrieving-a-class.md) represents an I/O port on a computer system running Windows.</span></span>

<span data-ttu-id="5ee6e-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="5ee6e-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ee6e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5ee6e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PortResource : Win32_SystemMemoryResource
{
  boolean  Alias;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="5ee6e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5ee6e-108">Members</span></span>

<span data-ttu-id="5ee6e-109">A classe **Win32 \_ PortResource** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5ee6e-109">The **Win32\_PortResource** class has these types of members:</span></span>

-   [<span data-ttu-id="5ee6e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5ee6e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ee6e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5ee6e-111">Properties</span></span>

<span data-ttu-id="5ee6e-112">A classe **Win32 \_ PortResource** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-112">The **Win32\_PortResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ee6e-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ee6e-114">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ee6e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-116">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Configuration Manager \| informações de e/s de estruturas \_ ")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Configuration Manager Structures\|IO\_INFO")</span></span>
</dt> </dl>

<span data-ttu-id="5ee6e-117">Se **for true**, essa instância representará um dos intervalos com um alias.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-117">If **TRUE**, this instance represents one of the ranges with an alias.</span></span> <span data-ttu-id="5ee6e-118">Se **for false**, a instância representará um endereço de porta base.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-118">If **FALSE**, the instance represents a base port address.</span></span> <span data-ttu-id="5ee6e-119">Um endereço de porta base é um endereço de porta predeterminado dedicado a um dispositivo ou serviço específico.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-119">A base port address is a predetermined port address dedicated to a specific service or device.</span></span> <span data-ttu-id="5ee6e-120">Um endereço de alias de porta é aquele que um dispositivo responde como se fosse o endereço real de uma porta de e/s.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-120">A port alias address is one that a device responds to as if it were the actual address of an I/O port.</span></span>

</dd> <dt>

<span data-ttu-id="5ee6e-121">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ee6e-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ee6e-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-124">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5ee6e-125">Breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-125">Short description of the object.</span></span>

<span data-ttu-id="5ee6e-126">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ee6e-127">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-127">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ee6e-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ee6e-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-130">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5ee6e-130">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5ee6e-131">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-131">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="5ee6e-132">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-132">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5ee6e-133">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-133">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ee6e-134">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-134">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ee6e-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ee6e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-137">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="5ee6e-137">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5ee6e-138">Nome da classe de criação do sistema de computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-138">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="5ee6e-139">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-139">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ee6e-140">**CSName**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-140">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ee6e-141">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-142">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ee6e-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-143">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="5ee6e-143">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="5ee6e-144">Nome do sistema de computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-144">Name of the scoping computer system.</span></span>

<span data-ttu-id="5ee6e-145">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-145">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ee6e-146">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ee6e-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ee6e-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-149">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-149">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5ee6e-150">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-150">Description of the object.</span></span>

<span data-ttu-id="5ee6e-151">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ee6e-152">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-152">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ee6e-153">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ee6e-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-155">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|E/s 1,2 de memória DMTF mapeada \| )</span><span class="sxs-lookup"><span data-stu-id="5ee6e-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="5ee6e-156">Endereço final da e/s mapeada da memória.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-156">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="5ee6e-157">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-157">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="5ee6e-158">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ee6e-159">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-159">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ee6e-160">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-160">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ee6e-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-162">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-162">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5ee6e-163">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-163">Date and time the object was installed.</span></span> <span data-ttu-id="5ee6e-164">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-164">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5ee6e-165">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ee6e-166">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ee6e-167">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ee6e-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-169">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-169">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5ee6e-170">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-170">Label by which the object is known.</span></span> <span data-ttu-id="5ee6e-171">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-171">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="5ee6e-172">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ee6e-173">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-173">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ee6e-174">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ee6e-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-176">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("StartingAddress"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|E/s 1,1 de memória DMTF mapeada \| )</span><span class="sxs-lookup"><span data-stu-id="5ee6e-176">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("StartingAddress"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="5ee6e-177">Endereço inicial da e/s mapeada da memória.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-177">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="5ee6e-178">A propriedade do identificador de recurso de hardware deve ser definida com esse valor para construir a chave de recurso de e/s mapeada.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-178">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="5ee6e-179">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-179">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="5ee6e-180">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-180">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ee6e-181">**Status**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-181">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ee6e-182">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5ee6e-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5ee6e-184">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-184">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5ee6e-185">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-185">Current status of the object.</span></span> <span data-ttu-id="5ee6e-186">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-186">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="5ee6e-187">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-187">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="5ee6e-188">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="5ee6e-188">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="5ee6e-189">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-189">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="5ee6e-190">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="5ee6e-190">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="5ee6e-191">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5ee6e-192">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5ee6e-192">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5ee6e-193">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-193">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5ee6e-194">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-194">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5ee6e-195">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-195">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5ee6e-196">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-196">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5ee6e-197">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-197">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5ee6e-198">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-198">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5ee6e-199">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-199">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5ee6e-200">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-200">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5ee6e-201">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-201">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5ee6e-202">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-202">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5ee6e-203">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-203">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5ee6e-204">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="5ee6e-204">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="5ee6e-205"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5ee6e-205"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5ee6e-206">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ee6e-206">Remarks</span></span>

<span data-ttu-id="5ee6e-207">A classe **Win32 \_ PortResource** é derivada de [**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md).</span><span class="sxs-lookup"><span data-stu-id="5ee6e-207">The **Win32\_PortResource** class is derived from [**Win32\_SystemMemoryResource**](win32-systemmemoryresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ee6e-208">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ee6e-208">Requirements</span></span>



| <span data-ttu-id="5ee6e-209">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ee6e-209">Requirement</span></span> | <span data-ttu-id="5ee6e-210">Valor</span><span class="sxs-lookup"><span data-stu-id="5ee6e-210">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee6e-211">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ee6e-211">Minimum supported client</span></span><br/> | <span data-ttu-id="5ee6e-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ee6e-212">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ee6e-213">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5ee6e-213">Minimum supported server</span></span><br/> | <span data-ttu-id="5ee6e-214">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ee6e-214">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ee6e-215">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ee6e-215">Namespace</span></span><br/>                | <span data-ttu-id="5ee6e-216">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5ee6e-216">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5ee6e-217">MOF</span><span class="sxs-lookup"><span data-stu-id="5ee6e-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ee6e-218"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5ee6e-218"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ee6e-219">DLL</span><span class="sxs-lookup"><span data-stu-id="5ee6e-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ee6e-220"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ee6e-220"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ee6e-221">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ee6e-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ee6e-222">**\_SystemMemoryResource Win32**</span><span class="sxs-lookup"><span data-stu-id="5ee6e-222">**Win32\_SystemMemoryResource**</span></span>](win32-systemmemoryresource.md)
</dt> <dt>

[<span data-ttu-id="5ee6e-223">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="5ee6e-223">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
