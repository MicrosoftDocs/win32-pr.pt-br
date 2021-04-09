---
description: Representa uma base, que também é conhecida como placa-mãe ou placa do sistema.
ms.assetid: 04ac7522-8b99-4ffc-9f7d-d1225f55a862
ms.tgt_platform: multiple
title: Classe Win32_BaseBoard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseBoard
- Win32_BaseBoard.IsCompatible
- Win32_BaseBoard.Caption
- Win32_BaseBoard.ConfigOptions
- Win32_BaseBoard.CreationClassName
- Win32_BaseBoard.Depth
- Win32_BaseBoard.Description
- Win32_BaseBoard.Height
- Win32_BaseBoard.HostingBoard
- Win32_BaseBoard.HotSwappable
- Win32_BaseBoard.InstallDate
- Win32_BaseBoard.Manufacturer
- Win32_BaseBoard.Model
- Win32_BaseBoard.Name
- Win32_BaseBoard.OtherIdentifyingInfo
- Win32_BaseBoard.PartNumber
- Win32_BaseBoard.PoweredOn
- Win32_BaseBoard.Product
- Win32_BaseBoard.Removable
- Win32_BaseBoard.Replaceable
- Win32_BaseBoard.RequirementsDescription
- Win32_BaseBoard.RequiresDaughterBoard
- Win32_BaseBoard.SerialNumber
- Win32_BaseBoard.SKU
- Win32_BaseBoard.SlotLayout
- Win32_BaseBoard.SpecialRequirements
- Win32_BaseBoard.Status
- Win32_BaseBoard.Tag
- Win32_BaseBoard.Version
- Win32_BaseBoard.Weight
- Win32_BaseBoard.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4287076a550e25bf74a160b191c777c25d9ab3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010276"
---
# <a name="win32_baseboard-class"></a><span data-ttu-id="de962-103">Classe do Win32 \_ baseboard</span><span class="sxs-lookup"><span data-stu-id="de962-103">Win32\_BaseBoard class</span></span>

<span data-ttu-id="de962-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) da **\_ baseboard do Win32** representa uma base, que também é conhecida como placa-mãe ou placa do sistema.</span><span class="sxs-lookup"><span data-stu-id="de962-104">The **Win32\_BaseBoard** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a baseboard, which is also known as a motherboard or system board.</span></span>

<span data-ttu-id="de962-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="de962-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="de962-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de962-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B95-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_BaseBoard : CIM_Card
{
  string   Caption;
  string   ConfigOptions[];
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HostingBoard;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   Product;
  boolean  Removable;
  boolean  Replaceable;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SerialNumber;
  string   SKU;
  string   SlotLayout;
  boolean  SpecialRequirements;
  string   Status;
  string   Tag;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="de962-107">Membros</span><span class="sxs-lookup"><span data-stu-id="de962-107">Members</span></span>

<span data-ttu-id="de962-108">A classe do **Win32 \_ baseboard** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="de962-108">The **Win32\_BaseBoard** class has these types of members:</span></span>

-   [<span data-ttu-id="de962-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="de962-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="de962-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="de962-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="de962-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="de962-111">Methods</span></span>

<span data-ttu-id="de962-112">A classe do **Win32 \_ baseboard** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="de962-112">The **Win32\_BaseBoard** class has these methods.</span></span>



| <span data-ttu-id="de962-113">Método</span><span class="sxs-lookup"><span data-stu-id="de962-113">Method</span></span>           | <span data-ttu-id="de962-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="de962-114">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="de962-115">**Iscompatível**</span><span class="sxs-lookup"><span data-stu-id="de962-115">**IsCompatible**</span></span> | <span data-ttu-id="de962-116">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="de962-116">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="de962-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="de962-117">Properties</span></span>

<span data-ttu-id="de962-118">A classe do **Win32 \_ baseboard** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="de962-118">The **Win32\_BaseBoard** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="de962-119">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="de962-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-122">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="de962-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="de962-123">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="de962-123">Short description of the object a one-line string.</span></span>

<span data-ttu-id="de962-124">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-125">**Configoptions**</span><span class="sxs-lookup"><span data-stu-id="de962-125">**ConfigOptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-126">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-126">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="de962-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-128">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("cadeia de caracteres de opções de configuração do SMBIOS \| tipo 12 \| ")</span><span class="sxs-lookup"><span data-stu-id="de962-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 12\|Configuration Options Strings")</span></span>
</dt> </dl>

<span data-ttu-id="de962-129">Matriz que representa a configuração dos jumpers e comutadores localizados na placa básica.</span><span class="sxs-lookup"><span data-stu-id="de962-129">Array that represents the configuration of the jumpers and switches located on the baseboard.</span></span>

<span data-ttu-id="de962-130">Exemplo: "JP2: o tamanho do cache 1-2 é 256K, 2-3 o tamanho do cache é 512K, SW1-1: fechar para desabilitar o vídeo no quadro"</span><span class="sxs-lookup"><span data-stu-id="de962-130">Example: "JP2: 1-2 Cache Size is 256K, 2-3 Cache Size is 512K, SW1-1: Close to Disable On Board Video"</span></span>

</dd> <dt>

<span data-ttu-id="de962-131">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="de962-131">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-134">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="de962-134">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="de962-135">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="de962-135">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="de962-136">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="de962-136">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="de962-137">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-137">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-138">**Profundidade**</span><span class="sxs-lookup"><span data-stu-id="de962-138">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-139">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="de962-139">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="de962-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-141">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="de962-141">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="de962-142">Profundidade do pacote físico em polegadas.</span><span class="sxs-lookup"><span data-stu-id="de962-142">Depth of the physical package in inches.</span></span>

<span data-ttu-id="de962-143">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="de962-143">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-144">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="de962-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-147">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="de962-147">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="de962-148">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="de962-148">Description of the object.</span></span>

<span data-ttu-id="de962-149">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-149">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-150">**Altura**</span><span class="sxs-lookup"><span data-stu-id="de962-150">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-151">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="de962-151">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="de962-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-153">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="de962-153">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="de962-154">Altura do pacote físico em polegadas.</span><span class="sxs-lookup"><span data-stu-id="de962-154">Height of the physical package in inches.</span></span>

<span data-ttu-id="de962-155">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="de962-155">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-156">**HostingBoard**</span><span class="sxs-lookup"><span data-stu-id="de962-156">**HostingBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-157">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="de962-157">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de962-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de962-159">Se for **true**, o cartão será uma placa-mãe ou uma placa-base em um chassi.</span><span class="sxs-lookup"><span data-stu-id="de962-159">If **TRUE**, the card is a motherboard, or a baseboard in a chassis.</span></span>

<span data-ttu-id="de962-160">Essa propriedade é herdada [**da \_ placa CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="de962-160">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-161">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="de962-161">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-162">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="de962-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de962-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de962-164">Se **for true**, o pacote poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="de962-164">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="de962-165">Um pacote físico pode ser intercambiável se for possível substituir o elemento por um elemento fisicamente diferente, mas equivalente, enquanto o pacote recipiente tem energia aplicada a ele, enquanto está ligado.</span><span class="sxs-lookup"><span data-stu-id="de962-165">A physical package can be hot-swapped if it is possible to replace the element with a physically different but equivalent element while the containing package has power applied to it that is, while it is ON.</span></span> <span data-ttu-id="de962-166">Por exemplo, um pacote de unidade de disco inserido usando conectores de SCA é removível e pode ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="de962-166">For example, a disk drive package inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="de962-167">Todos os pacotes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.</span><span class="sxs-lookup"><span data-stu-id="de962-167">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="de962-168">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="de962-168">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-169">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="de962-169">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-170">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="de962-170">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="de962-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-172">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="de962-172">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="de962-173">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="de962-173">Date and time the object was installed.</span></span> <span data-ttu-id="de962-174">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="de962-174">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="de962-175">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-175">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-176">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="de962-176">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-179">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="de962-179">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="de962-180">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="de962-180">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="de962-181">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-181">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-182">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="de962-182">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-185">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="de962-185">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="de962-186">Nome pelo qual o elemento físico é conhecido.</span><span class="sxs-lookup"><span data-stu-id="de962-186">Name by which the physical element is known.</span></span>

<span data-ttu-id="de962-187">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-187">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-188">**Nome**</span><span class="sxs-lookup"><span data-stu-id="de962-188">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-189">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-190">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-191">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="de962-191">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="de962-192">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="de962-192">Label by which the object is known.</span></span> <span data-ttu-id="de962-193">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="de962-193">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="de962-194">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-194">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-195">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="de962-195">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-196">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-196">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de962-198">Captura dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="de962-198">Captures additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="de962-199">Um exemplo são os dados de código de barras associados a um elemento que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="de962-199">One example is bar code data that is associated with an element that also has an asset tag.</span></span> <span data-ttu-id="de962-200">Observe que, se apenas os dados de código de barras estiverem disponíveis e exclusivos ou puderem ser usados como uma chave de elemento, o valor da propriedade será **NULL** e os dados do código de barras seriam usados como a chave de classe, na propriedade Tag.</span><span class="sxs-lookup"><span data-stu-id="de962-200">Note that if only bar code data is available and unique or able to be used as an element key, the property value would be **NULL** and the bar code data would be used as the class key, in the tag property.</span></span>

<span data-ttu-id="de962-201">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-201">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-202">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="de962-202">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-205">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="de962-205">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="de962-206">Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="de962-206">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="de962-207">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-207">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-208">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="de962-208">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-209">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="de962-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de962-210">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de962-211">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="de962-211">If **TRUE**, the physical element is powered ON.</span></span>

<span data-ttu-id="de962-212">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-212">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-213">**Product**</span><span class="sxs-lookup"><span data-stu-id="de962-213">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-214">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-216">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| produto SMBIOS tipo 2 \| ")</span><span class="sxs-lookup"><span data-stu-id="de962-216">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 2\|Product")</span></span>
</dt> </dl>

<span data-ttu-id="de962-217">Número de peça da placa-base definida pelo fabricante.</span><span class="sxs-lookup"><span data-stu-id="de962-217">Baseboard part number defined by the manufacturer.</span></span>

</dd> <dt>

<span data-ttu-id="de962-218">**Removível**</span><span class="sxs-lookup"><span data-stu-id="de962-218">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-219">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="de962-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de962-220">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-220">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de962-221">Se for **true**, um pacote será removível.</span><span class="sxs-lookup"><span data-stu-id="de962-221">If **TRUE**, a package is removable.</span></span> <span data-ttu-id="de962-222">Um pacote físico será removível se for projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado sem comprometer a função do empacotamento geral.</span><span class="sxs-lookup"><span data-stu-id="de962-222">A physical package is removable if it is designed to be taken in and out of the physical container in which it is normally found without impairing the function of the overall packaging.</span></span> <span data-ttu-id="de962-223">Um pacote ainda poderá ser removível se a energia precisar ser desativada para realizar a remoção.</span><span class="sxs-lookup"><span data-stu-id="de962-223">A package can still be removable if the power must be OFF to perform the removal.</span></span> <span data-ttu-id="de962-224">Se a energia puder ser ATIVAda e o pacote for removido, o elemento será removível e poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="de962-224">If the power can be ON and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="de962-225">Por exemplo, uma bateria extra em um laptop é removível, assim como um pacote de unidade de disco inserido usando conectores SCA.</span><span class="sxs-lookup"><span data-stu-id="de962-225">For example, an extra battery in a laptop is removable, as is a disk drive package inserted using SCA connectors.</span></span> <span data-ttu-id="de962-226">No entanto, o último também pode ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="de962-226">However, the latter can also be hot-swapped.</span></span> <span data-ttu-id="de962-227">A tela de um laptop não é removível, nem uma fonte de alimentação não redundante.</span><span class="sxs-lookup"><span data-stu-id="de962-227">A laptop's display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="de962-228">A remoção desses componentes afetaria a função do empacotamento geral ou é impossível devido à forte integração do pacote.</span><span class="sxs-lookup"><span data-stu-id="de962-228">Removing these components would impact the function of the overall packaging, or is impossible due to the tight integration of the package.</span></span>

<span data-ttu-id="de962-229">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="de962-229">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-230">**Peças**</span><span class="sxs-lookup"><span data-stu-id="de962-230">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-231">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="de962-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de962-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de962-233">Se for **true**, um pacote será substituível.</span><span class="sxs-lookup"><span data-stu-id="de962-233">If **TRUE**, a package is replaceable.</span></span> <span data-ttu-id="de962-234">Um pacote físico será substituível se for possível substituir (FRU ou atualizar) o elemento por um fisicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="de962-234">A physical package is replaceable if it is possible to replace (FRU or upgrade) the element with a physically different one.</span></span> <span data-ttu-id="de962-235">Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta.</span><span class="sxs-lookup"><span data-stu-id="de962-235">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="de962-236">Nesse caso, diz-se que o processador é substituível.</span><span class="sxs-lookup"><span data-stu-id="de962-236">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="de962-237">Outro exemplo é um pacote de fornecimento de energia montado em trilhos deslizantes.</span><span class="sxs-lookup"><span data-stu-id="de962-237">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="de962-238">Todos os pacotes removíveis são inerentemente substituíveis.</span><span class="sxs-lookup"><span data-stu-id="de962-238">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="de962-239">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="de962-239">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-240">**RequirementsDescription**</span><span class="sxs-lookup"><span data-stu-id="de962-240">**RequirementsDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-241">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-243">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ placa CIM**](cim-card.md).**SpecialRequirements**")</span><span class="sxs-lookup"><span data-stu-id="de962-243">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Card**](cim-card.md).**SpecialRequirements**")</span></span>
</dt> </dl>

<span data-ttu-id="de962-244">Cadeia de caracteres de forma livre que descreve a maneira como esse cartão é fisicamente exclusivo de outros cartões.</span><span class="sxs-lookup"><span data-stu-id="de962-244">Free-form string that describes the way in which this card is physically unique from other cards.</span></span> <span data-ttu-id="de962-245">A propriedade só tem significado quando a propriedade booliana correspondente **SpecialRequirements** está definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="de962-245">The property only has meaning when the corresponding Boolean property **SpecialRequirements** is set to **TRUE**.</span></span>

<span data-ttu-id="de962-246">Essa propriedade é herdada [**da \_ placa CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="de962-246">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-247">**RequiresDaughterBoard**</span><span class="sxs-lookup"><span data-stu-id="de962-247">**RequiresDaughterBoard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-248">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="de962-248">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de962-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-249">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de962-250">Se for **true**, pelo menos um daughterboard ou um cartão auxiliar será necessário para funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="de962-250">If **TRUE**, at least one daughterboard or auxiliary card is required to function properly.</span></span>

<span data-ttu-id="de962-251">Essa propriedade é herdada [**da \_ placa CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="de962-251">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-252">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="de962-252">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-253">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-253">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-254">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-254">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-255">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="de962-255">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="de962-256">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="de962-256">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="de962-257">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-257">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-258">**SKU**</span><span class="sxs-lookup"><span data-stu-id="de962-258">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-259">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-259">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-260">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-260">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-261">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="de962-261">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="de962-262">Número de unidade de manutenção de estoque do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="de962-262">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="de962-263">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-263">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-264">**SlotLayout**</span><span class="sxs-lookup"><span data-stu-id="de962-264">**SlotLayout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-265">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-265">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-266">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-266">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="de962-267">Cadeia de caracteres de forma livre que descreve a posição do slot, o uso típico, as restrições, o espaçamento individual do slot ou qualquer outra informação pertinente para os slots em um cartão.</span><span class="sxs-lookup"><span data-stu-id="de962-267">Free-form string that describes the slot position, typical usage, restrictions, individual slot spacing or any other pertinent information for the slots on a card.</span></span>

<span data-ttu-id="de962-268">Essa propriedade é herdada [**da \_ placa CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="de962-268">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-269">**SpecialRequirements**</span><span class="sxs-lookup"><span data-stu-id="de962-269">**SpecialRequirements**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-270">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="de962-270">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="de962-271">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-272">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ placa CIM**](cim-card.md).**RequirementsDescription**")</span><span class="sxs-lookup"><span data-stu-id="de962-272">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_Card**](cim-card.md).**RequirementsDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="de962-273">Se **for true**, esse cartão será fisicamente exclusivo de outros cartões do mesmo tipo e, portanto, exigirá um slot especial.</span><span class="sxs-lookup"><span data-stu-id="de962-273">If **TRUE**, this card is physically unique from other cards of the same type and therefore requires a special slot.</span></span> <span data-ttu-id="de962-274">Por exemplo, um cartão de largura dupla requer dois slots.</span><span class="sxs-lookup"><span data-stu-id="de962-274">For example, a double-wide card requires two slots.</span></span> <span data-ttu-id="de962-275">Outro exemplo é onde um determinado cartão pode ser usado para a mesma função geral que outros cartões, mas requer um slot especial (por exemplo, extra Long), enquanto os outros cartões podem ser colocados em qualquer slot disponível.</span><span class="sxs-lookup"><span data-stu-id="de962-275">Another example is where a certain card may be used for the same general function as other cards but requires a special slot (for example, extra long), whereas the other cards can be placed in any available slot.</span></span> <span data-ttu-id="de962-276">Se definido como **true**, a propriedade correspondente, **RequirementsDescription**, deverá especificar a natureza da exclusividade ou da finalidade do cartão.</span><span class="sxs-lookup"><span data-stu-id="de962-276">If set to **TRUE**, then the corresponding property, **RequirementsDescription**, should specify the nature of the uniqueness or purpose of the card.</span></span>

<span data-ttu-id="de962-277">Essa propriedade é herdada [**da \_ placa CIM**](cim-card.md).</span><span class="sxs-lookup"><span data-stu-id="de962-277">This property is inherited from [**CIM\_Card**](cim-card.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-278">**Status**</span><span class="sxs-lookup"><span data-stu-id="de962-278">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-279">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-279">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-280">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-281">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="de962-281">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="de962-282">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="de962-282">Current status of the object.</span></span> <span data-ttu-id="de962-283">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="de962-283">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="de962-284">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="de962-284">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="de962-285">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="de962-285">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="de962-286">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="de962-286">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="de962-287">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="de962-287">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="de962-288">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-288">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="de962-289">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="de962-289">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="de962-290">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="de962-290">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="de962-291">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="de962-291">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="de962-292">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="de962-292">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="de962-293">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="de962-293">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="de962-294">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="de962-294">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="de962-295">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="de962-295">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="de962-296">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="de962-296">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="de962-297">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="de962-297">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="de962-298">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="de962-298">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="de962-299">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="de962-299">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="de962-300">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="de962-300">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="de962-301">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="de962-301">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="de962-302">**Tag**</span><span class="sxs-lookup"><span data-stu-id="de962-302">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-303">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-304">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-304">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-305">Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("tag"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="de962-305">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="de962-306">Identificador exclusivo da base do sistema.</span><span class="sxs-lookup"><span data-stu-id="de962-306">Unique identifier of the baseboard of the system.</span></span>

<span data-ttu-id="de962-307">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-307">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="de962-308">Exemplo: "placa base"</span><span class="sxs-lookup"><span data-stu-id="de962-308">Example: "Base Board"</span></span>

</dd> <dt>

<span data-ttu-id="de962-309">**Versão**</span><span class="sxs-lookup"><span data-stu-id="de962-309">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-310">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="de962-310">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="de962-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-312">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="de962-312">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="de962-313">Versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="de962-313">Version of the physical element.</span></span>

<span data-ttu-id="de962-314">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-315">**Weight**</span><span class="sxs-lookup"><span data-stu-id="de962-315">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-316">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="de962-316">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="de962-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-318">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")</span><span class="sxs-lookup"><span data-stu-id="de962-318">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="de962-319">Peso do pacote físico em libras.</span><span class="sxs-lookup"><span data-stu-id="de962-319">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="de962-320">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-320">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="de962-321">**Largura**</span><span class="sxs-lookup"><span data-stu-id="de962-321">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="de962-322">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="de962-322">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="de962-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="de962-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="de962-324">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="de962-324">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="de962-325">Largura do pacote físico em polegadas.</span><span class="sxs-lookup"><span data-stu-id="de962-325">Width of the physical package in inches.</span></span>

<span data-ttu-id="de962-326">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-326">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="de962-327">Comentários</span><span class="sxs-lookup"><span data-stu-id="de962-327">Remarks</span></span>

<span data-ttu-id="de962-328">A classe **Win32 \_ baseboard** é derivada da [**\_ placa CIM**](cim-card.md) , derivada de [**CIM \_ PhysicalPackage**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="de962-328">The **Win32\_BaseBoard** class is derived from [**CIM\_Card**](cim-card.md) which derives from [**CIM\_PhysicalPackage**](cim-physicalelement.md).</span></span>

## <a name="examples"></a><span data-ttu-id="de962-329">Exemplos</span><span class="sxs-lookup"><span data-stu-id="de962-329">Examples</span></span>

<span data-ttu-id="de962-330">O exemplo da [lista de propriedades da placa-base](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) Perl retorna informações sobre a placa-base do computador.</span><span class="sxs-lookup"><span data-stu-id="de962-330">The [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8) Perl sample returns information about the computer baseboard.</span></span>

<span data-ttu-id="de962-331">A amostra do PowerShell [listar Propriedades da placa base do computador](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) retorna informações sobre a placa-base do computador.</span><span class="sxs-lookup"><span data-stu-id="de962-331">The [List Computer Baseboard Properties](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9) PowerShell sample returns information about the computer baseboard.</span></span>

<span data-ttu-id="de962-332">O exemplo de VBScript a seguir também retorna informações sobre a placa-base do computador.</span><span class="sxs-lookup"><span data-stu-id="de962-332">The following VBScript sample also returns information about the computer baseboard.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BaseBoard") 
 
For Each objItem in colItems 
    For Each strOption in objItem.ConfigOptions 
        Wscript.Echo "Configuration Option: " & strOption 
    Next 
    Wscript.Echo "Depth: " & objItem.Depth 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Height: " & objItem.Height 
    Wscript.Echo "Hosting Board: " & objItem.HostingBoard 
    Wscript.Echo "Hot Swappable: " & objItem.HotSwappable 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "Model: " & objItem.Model 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Other Identifying Information: " & _ 
        objItem.OtherIdentifyingInfo 
    Wscript.Echo "Part Number: " & objItem.PartNumber 
    Wscript.Echo "Powered-On: " & objItem.PoweredOn 
    Wscript.Echo "Product: " & objItem.Product 
    Wscript.Echo "Removable: " & objItem.Removable 
    Wscript.Echo "Replaceable: " & objItem.Replaceable 
    Wscript.Echo "Requirements Description: " & objItem.RequirementsDescription 
    Wscript.Echo "Requires Daughterboard: " & objItem.RequiresDaughterBoard 
    Wscript.Echo "Serial Number: " & objItem.SerialNumber 
    Wscript.Echo "SKU: " & objItem.SKU 
    Wscript.Echo "Slot Layout: " & objItem.SlotLayout 
    Wscript.Echo "Special Requirements: " & objItem.SpecialRequirements 
    Wscript.Echo "Tag: " & objItem.Tag 
    Wscript.Echo "Version: " & objItem.Version 
    Wscript.Echo "Weight: " & objItem.Weight 
    Wscript.Echo "Width: " & objItem.Width 
Next 
```



## <a name="requirements"></a><span data-ttu-id="de962-333">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de962-333">Requirements</span></span>



| <span data-ttu-id="de962-334">Requisito</span><span class="sxs-lookup"><span data-stu-id="de962-334">Requirement</span></span> | <span data-ttu-id="de962-335">Valor</span><span class="sxs-lookup"><span data-stu-id="de962-335">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="de962-336">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de962-336">Minimum supported client</span></span><br/> | <span data-ttu-id="de962-337">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="de962-337">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="de962-338">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de962-338">Minimum supported server</span></span><br/> | <span data-ttu-id="de962-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="de962-339">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="de962-340">MOF</span><span class="sxs-lookup"><span data-stu-id="de962-340">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de962-341"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de962-341"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="de962-342">DLL</span><span class="sxs-lookup"><span data-stu-id="de962-342">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de962-343"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de962-343"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de962-344">Confira também</span><span class="sxs-lookup"><span data-stu-id="de962-344">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de962-345">**\_Placa CIM**</span><span class="sxs-lookup"><span data-stu-id="de962-345">**CIM\_Card**</span></span>](cim-card.md)
</dt> <dt>

[<span data-ttu-id="de962-346">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="de962-346">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

