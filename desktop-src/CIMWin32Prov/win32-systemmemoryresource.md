---
description: A \_ classe WMI abstrata do Win32 SystemMemoryResource representa um recurso de memória do sistema em um sistema de computador executando o Windows.
ms.assetid: a834a1e4-f3e4-4b57-9521-98520c301016
ms.tgt_platform: multiple
title: Classe Win32_SystemMemoryResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemMemoryResource
- Win32_SystemMemoryResource.Caption
- Win32_SystemMemoryResource.Description
- Win32_SystemMemoryResource.InstallDate
- Win32_SystemMemoryResource.Name
- Win32_SystemMemoryResource.Status
- Win32_SystemMemoryResource.CreationClassName
- Win32_SystemMemoryResource.CSCreationClassName
- Win32_SystemMemoryResource.CSName
- Win32_SystemMemoryResource.EndingAddress
- Win32_SystemMemoryResource.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6064f2d983978998c47518ee50b93c3a7fedfde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826661"
---
# <a name="win32_systemmemoryresource-class"></a><span data-ttu-id="6ceea-103">\_Classe Win32 SystemMemoryResource</span><span class="sxs-lookup"><span data-stu-id="6ceea-103">Win32\_SystemMemoryResource class</span></span>

<span data-ttu-id="6ceea-104">A [classe WMI](../wmisdk/retrieving-a-class.md) abstrata do **Win32 \_ SystemMemoryResource** representa um recurso de memória do sistema em um sistema de computador executando o Windows.</span><span class="sxs-lookup"><span data-stu-id="6ceea-104">The **Win32\_SystemMemoryResource** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents a system memory resource on a computer system running Windows.</span></span>

<span data-ttu-id="6ceea-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="6ceea-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="6ceea-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="6ceea-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ceea-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6ceea-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4CE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemMemoryResource : CIM_MemoryMappedIO
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

## <a name="members"></a><span data-ttu-id="6ceea-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6ceea-108">Members</span></span>

<span data-ttu-id="6ceea-109">A classe **Win32 \_ SystemMemoryResource** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6ceea-109">The **Win32\_SystemMemoryResource** class has these types of members:</span></span>

-   [<span data-ttu-id="6ceea-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6ceea-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6ceea-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6ceea-111">Properties</span></span>

<span data-ttu-id="6ceea-112">A classe **Win32 \_ SystemMemoryResource** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6ceea-112">The **Win32\_SystemMemoryResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6ceea-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="6ceea-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ceea-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6ceea-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ceea-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-116">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="6ceea-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="6ceea-117">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6ceea-117">A short textual description of the object.</span></span>

<span data-ttu-id="6ceea-118">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6ceea-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ceea-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6ceea-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ceea-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6ceea-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ceea-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-122">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6ceea-122">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6ceea-123">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="6ceea-123">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="6ceea-124">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="6ceea-124">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="6ceea-125">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="6ceea-125">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ceea-126">**CSCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="6ceea-126">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ceea-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6ceea-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ceea-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-129">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="6ceea-129">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="6ceea-130">Propriedade **CreationClassName** do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="6ceea-130">Scoping computer system's **CreationClassName** property.</span></span>

<span data-ttu-id="6ceea-131">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="6ceea-131">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ceea-132">**CSName**</span><span class="sxs-lookup"><span data-stu-id="6ceea-132">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ceea-133">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6ceea-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ceea-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-135">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema de ComputerSystem CIM**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="6ceea-135">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="6ceea-136">Propriedade do **nome** do sistema do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="6ceea-136">Scoping computer system's **Name** property.</span></span>

<span data-ttu-id="6ceea-137">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="6ceea-137">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ceea-138">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6ceea-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ceea-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6ceea-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ceea-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-141">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="6ceea-141">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="6ceea-142">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6ceea-142">A textual description of the object.</span></span>

<span data-ttu-id="6ceea-143">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6ceea-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ceea-144">**EndingAddress**</span><span class="sxs-lookup"><span data-stu-id="6ceea-144">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ceea-145">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6ceea-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ceea-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-147">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|E/s 1,2 de memória DMTF mapeada \| )</span><span class="sxs-lookup"><span data-stu-id="6ceea-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="6ceea-148">Endereço final da e/s mapeada da memória.</span><span class="sxs-lookup"><span data-stu-id="6ceea-148">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="6ceea-149">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="6ceea-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="6ceea-150">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="6ceea-150">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ceea-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="6ceea-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ceea-152">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="6ceea-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-153">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ceea-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-154">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="6ceea-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="6ceea-155">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="6ceea-155">Indicates when the object was installed.</span></span> <span data-ttu-id="6ceea-156">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="6ceea-156">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="6ceea-157">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6ceea-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ceea-158">**Nome**</span><span class="sxs-lookup"><span data-stu-id="6ceea-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ceea-159">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6ceea-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ceea-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-161">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="6ceea-161">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="6ceea-162">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="6ceea-162">Label by which the object is known.</span></span> <span data-ttu-id="6ceea-163">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="6ceea-163">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="6ceea-164">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6ceea-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ceea-165">**StartingAddress**</span><span class="sxs-lookup"><span data-stu-id="6ceea-165">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ceea-166">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="6ceea-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ceea-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-168">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|E/s 1,1 de memória DMTF mapeada \| )</span><span class="sxs-lookup"><span data-stu-id="6ceea-168">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="6ceea-169">Endereço inicial da e/s mapeada da memória.</span><span class="sxs-lookup"><span data-stu-id="6ceea-169">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="6ceea-170">A propriedade do identificador de recurso de hardware deve ser definida com esse valor para construir a chave de recurso de e/s mapeada.</span><span class="sxs-lookup"><span data-stu-id="6ceea-170">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="6ceea-171">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="6ceea-171">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="6ceea-172">Essa propriedade é herdada do [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="6ceea-172">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ceea-173">**Status**</span><span class="sxs-lookup"><span data-stu-id="6ceea-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6ceea-174">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6ceea-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6ceea-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6ceea-176">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="6ceea-176">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="6ceea-177">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="6ceea-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="6ceea-178">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="6ceea-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="6ceea-179">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="6ceea-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="6ceea-180">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="6ceea-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="6ceea-181">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="6ceea-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="6ceea-182">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="6ceea-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="6ceea-183">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="6ceea-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="6ceea-184">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="6ceea-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="6ceea-185">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6ceea-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="6ceea-186">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="6ceea-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="6ceea-187">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="6ceea-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="6ceea-188">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="6ceea-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6ceea-189">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="6ceea-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="6ceea-190">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="6ceea-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="6ceea-191">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="6ceea-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="6ceea-192">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="6ceea-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="6ceea-193">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="6ceea-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="6ceea-194">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="6ceea-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="6ceea-195">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="6ceea-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="6ceea-196">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="6ceea-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="6ceea-197">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="6ceea-197">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="6ceea-198"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6ceea-198"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="6ceea-199">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ceea-199">Remarks</span></span>

<span data-ttu-id="6ceea-200">A classe **Win32 \_ SystemMemoryResource** é derivada de [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="6ceea-200">The **Win32\_SystemMemoryResource** class is derived from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ceea-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ceea-201">Requirements</span></span>



| <span data-ttu-id="6ceea-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ceea-202">Requirement</span></span> | <span data-ttu-id="6ceea-203">Valor</span><span class="sxs-lookup"><span data-stu-id="6ceea-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ceea-204">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ceea-204">Minimum supported client</span></span><br/> | <span data-ttu-id="6ceea-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ceea-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6ceea-206">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6ceea-206">Minimum supported server</span></span><br/> | <span data-ttu-id="6ceea-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ceea-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6ceea-208">Namespace</span><span class="sxs-lookup"><span data-stu-id="6ceea-208">Namespace</span></span><br/>                | <span data-ttu-id="6ceea-209">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6ceea-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6ceea-210">MOF</span><span class="sxs-lookup"><span data-stu-id="6ceea-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6ceea-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6ceea-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6ceea-212">DLL</span><span class="sxs-lookup"><span data-stu-id="6ceea-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ceea-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ceea-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ceea-214">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ceea-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ceea-215">**\_MEMORYMAPPEDIO CIM**</span><span class="sxs-lookup"><span data-stu-id="6ceea-215">**CIM\_MemoryMappedIO**</span></span>](cim-memorymappedio.md)
</dt> <dt>

[<span data-ttu-id="6ceea-216">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="6ceea-216">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
