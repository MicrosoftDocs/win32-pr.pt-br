---
description: Representa as propriedades que estão associadas a um compartimento de sistema físico.
ms.assetid: a8244dc0-a95e-4940-9b92-7820bdf14916
ms.tgt_platform: multiple
title: Classe Win32_SystemEnclosure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemEnclosure
- Win32_SystemEnclosure.IsCompatible
- Win32_SystemEnclosure.AudibleAlarm
- Win32_SystemEnclosure.BreachDescription
- Win32_SystemEnclosure.CableManagementStrategy
- Win32_SystemEnclosure.Caption
- Win32_SystemEnclosure.ChassisTypes
- Win32_SystemEnclosure.CreationClassName
- Win32_SystemEnclosure.CurrentRequiredOrProduced
- Win32_SystemEnclosure.Depth
- Win32_SystemEnclosure.Description
- Win32_SystemEnclosure.HeatGeneration
- Win32_SystemEnclosure.Height
- Win32_SystemEnclosure.HotSwappable
- Win32_SystemEnclosure.InstallDate
- Win32_SystemEnclosure.LockPresent
- Win32_SystemEnclosure.Manufacturer
- Win32_SystemEnclosure.Model
- Win32_SystemEnclosure.Name
- Win32_SystemEnclosure.NumberOfPowerCords
- Win32_SystemEnclosure.OtherIdentifyingInfo
- Win32_SystemEnclosure.PartNumber
- Win32_SystemEnclosure.PoweredOn
- Win32_SystemEnclosure.Removable
- Win32_SystemEnclosure.Replaceable
- Win32_SystemEnclosure.SecurityBreach
- Win32_SystemEnclosure.SecurityStatus
- Win32_SystemEnclosure.SerialNumber
- Win32_SystemEnclosure.ServiceDescriptions
- Win32_SystemEnclosure.ServicePhilosophy
- Win32_SystemEnclosure.SKU
- Win32_SystemEnclosure.SMBIOSAssetTag
- Win32_SystemEnclosure.Status
- Win32_SystemEnclosure.Tag
- Win32_SystemEnclosure.TypeDescriptions
- Win32_SystemEnclosure.Version
- Win32_SystemEnclosure.VisibleAlarm
- Win32_SystemEnclosure.Weight
- Win32_SystemEnclosure.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c7f3b65f6435d8ff828aebf5310f9b21a2ea7f6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920555"
---
# <a name="win32_systemenclosure-class"></a><span data-ttu-id="cfa74-103">\_Classe Win32 SystemEnclosure</span><span class="sxs-lookup"><span data-stu-id="cfa74-103">Win32\_SystemEnclosure class</span></span>

<span data-ttu-id="cfa74-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemEnclosure do Win32** representa as propriedades que estão associadas a um compartimento de sistema físico.</span><span class="sxs-lookup"><span data-stu-id="cfa74-104">The **Win32\_SystemEnclosure** [WMI class](../wmisdk/retrieving-a-class.md) represents the properties that are associated with a physical system enclosure.</span></span>

<span data-ttu-id="cfa74-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cfa74-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="cfa74-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="cfa74-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfa74-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cfa74-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B94-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemEnclosure : CIM_Chassis
{
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  string   Caption;
  uint16   ChassisTypes[];
  string   CreationClassName;
  sint16   CurrentRequiredOrProduced;
  real32   Depth;
  string   Description;
  uint16   HeatGeneration;
  real32   Height;
  boolean  HotSwappable;
  datetime InstallDate;
  boolean  LockPresent;
  string   Manufacturer;
  string   Model;
  string   Name;
  uint16   NumberOfPowerCords;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  boolean  Removable;
  boolean  Replaceable;
  uint16   SecurityBreach;
  uint16   SecurityStatus;
  string   SerialNumber;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  string   SKU;
  string   SMBIOSAssetTag;
  string   Status;
  string   Tag;
  string   TypeDescriptions[];
  string   Version;
  boolean  VisibleAlarm;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a><span data-ttu-id="cfa74-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cfa74-108">Members</span></span>

<span data-ttu-id="cfa74-109">A classe **Win32 \_ SystemEnclosure** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cfa74-109">The **Win32\_SystemEnclosure** class has these types of members:</span></span>

-   [<span data-ttu-id="cfa74-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="cfa74-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="cfa74-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cfa74-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="cfa74-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="cfa74-112">Methods</span></span>

<span data-ttu-id="cfa74-113">A classe **Win32 \_ SystemEnclosure** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="cfa74-113">The **Win32\_SystemEnclosure** class has these methods.</span></span>



| <span data-ttu-id="cfa74-114">Método</span><span class="sxs-lookup"><span data-stu-id="cfa74-114">Method</span></span>           | <span data-ttu-id="cfa74-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="cfa74-115">Description</span></span>                 |
|:-----------------|:----------------------------|
| <span data-ttu-id="cfa74-116">**Iscompatível**</span><span class="sxs-lookup"><span data-stu-id="cfa74-116">**IsCompatible**</span></span> | <span data-ttu-id="cfa74-117">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="cfa74-117">Not implemented.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="cfa74-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cfa74-118">Properties</span></span>

<span data-ttu-id="cfa74-119">A classe **Win32 \_ SystemEnclosure** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cfa74-119">The **Win32\_SystemEnclosure** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cfa74-120">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="cfa74-120">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-121">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cfa74-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-123">Se for **true**, o quadro será equipado com um alarme audível.</span><span class="sxs-lookup"><span data-stu-id="cfa74-123">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="cfa74-124">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-124">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-125">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="cfa74-125">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-128">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="cfa74-128">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-129">Cadeia de caracteres de forma livre que fornece mais informações se a propriedade **SecurityBreach** indicar que ocorreu um evento relacionado à segurança.</span><span class="sxs-lookup"><span data-stu-id="cfa74-129">Free-form string that provides more information if the **SecurityBreach** property indicates that a security-related event occurred.</span></span>

<span data-ttu-id="cfa74-130">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-130">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-131">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="cfa74-131">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-132">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-134">Cadeia de caracteres de forma livre que contém informações sobre como os vários cabos são conectados e agrupados para o quadro.</span><span class="sxs-lookup"><span data-stu-id="cfa74-134">Free-form string that contains information about how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="cfa74-135">Com muitos cabos de rede, relacionados ao armazenamento e de energia, o gerenciamento de cabos pode ser um esforço complexo e desafiador.</span><span class="sxs-lookup"><span data-stu-id="cfa74-135">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="cfa74-136">Essa propriedade contém informações para auxiliar no assembly e no serviço do quadro.</span><span class="sxs-lookup"><span data-stu-id="cfa74-136">This property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="cfa74-137">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-137">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-138">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="cfa74-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-139">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-140">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-141">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="cfa74-141">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-142">Breve descrição do objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="cfa74-142">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="cfa74-143">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-144">**ChassisTypes**</span><span class="sxs-lookup"><span data-stu-id="cfa74-144">**ChassisTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-145">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfa74-145">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-147">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Tabela global de contêiner físico DMTF \| 2,1 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ chassi CIM**](cim-chassis.md).**TypeDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="cfa74-147">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Physical Container Global Table\|002.1"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Chassis**](cim-chassis.md).**TypeDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-148">Matriz de tipos de chassi.</span><span class="sxs-lookup"><span data-stu-id="cfa74-148">Array of chassis types.</span></span>

<span data-ttu-id="cfa74-149">Esse valor é proveniente do membro de **tipo** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="cfa74-149">This value comes from the **Type** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="cfa74-150">Essa propriedade é herdada [**do \_ chassi CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-150">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cfa74-151">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="cfa74-151">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cfa74-152">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="cfa74-152">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="cfa74-153">**Área de trabalho** (3)</span><span class="sxs-lookup"><span data-stu-id="cfa74-153">**Desktop** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span data-ttu-id="cfa74-154">**Área de trabalho de baixo perfil** (4)</span><span class="sxs-lookup"><span data-stu-id="cfa74-154">**Low Profile Desktop** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span data-ttu-id="cfa74-155">**Caixa de pizza** (5)</span><span class="sxs-lookup"><span data-stu-id="cfa74-155">**Pizza Box** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span data-ttu-id="cfa74-156">**Mini-torre** (6)</span><span class="sxs-lookup"><span data-stu-id="cfa74-156">**Mini Tower** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span data-ttu-id="cfa74-157">**Torre** (7)</span><span class="sxs-lookup"><span data-stu-id="cfa74-157">**Tower** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span data-ttu-id="cfa74-158">**Portátil** (8)</span><span class="sxs-lookup"><span data-stu-id="cfa74-158">**Portable** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="cfa74-159">**Laptop** (9)</span><span class="sxs-lookup"><span data-stu-id="cfa74-159">**Laptop** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span data-ttu-id="cfa74-160">**Notebook** (10)</span><span class="sxs-lookup"><span data-stu-id="cfa74-160">**Notebook** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span data-ttu-id="cfa74-161">**Mão suspensa** (11)</span><span class="sxs-lookup"><span data-stu-id="cfa74-161">**Hand Held** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span data-ttu-id="cfa74-162">**Estação de encaixe** (12)</span><span class="sxs-lookup"><span data-stu-id="cfa74-162">**Docking Station** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span data-ttu-id="cfa74-163">**Tudo em um** (13)</span><span class="sxs-lookup"><span data-stu-id="cfa74-163">**All in One** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span data-ttu-id="cfa74-164">**Subnotebook** (14)</span><span class="sxs-lookup"><span data-stu-id="cfa74-164">**Sub Notebook** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span data-ttu-id="cfa74-165">**Economia de espaço** (15)</span><span class="sxs-lookup"><span data-stu-id="cfa74-165">**Space-Saving** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span data-ttu-id="cfa74-166">**Caixa de almoço** (16)</span><span class="sxs-lookup"><span data-stu-id="cfa74-166">**Lunch Box** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span data-ttu-id="cfa74-167">**Chassi do sistema principal** (17)</span><span class="sxs-lookup"><span data-stu-id="cfa74-167">**Main System Chassis** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span data-ttu-id="cfa74-168">**Chassi de expansão** (18)</span><span class="sxs-lookup"><span data-stu-id="cfa74-168">**Expansion Chassis** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span data-ttu-id="cfa74-169">**Subchassi** (19)</span><span class="sxs-lookup"><span data-stu-id="cfa74-169">**SubChassis** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span data-ttu-id="cfa74-170">**Chassi de expansão de barramento** (20)</span><span class="sxs-lookup"><span data-stu-id="cfa74-170">**Bus Expansion Chassis** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span data-ttu-id="cfa74-171">**Chassi de periférico** (21)</span><span class="sxs-lookup"><span data-stu-id="cfa74-171">**Peripheral Chassis** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span data-ttu-id="cfa74-172">**Chassi de armazenamento** (22)</span><span class="sxs-lookup"><span data-stu-id="cfa74-172">**Storage Chassis** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span data-ttu-id="cfa74-173">**Chassi de montagem em rack** (23)</span><span class="sxs-lookup"><span data-stu-id="cfa74-173">**Rack Mount Chassis** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span data-ttu-id="cfa74-174">**PC de caso lacrado** (24)</span><span class="sxs-lookup"><span data-stu-id="cfa74-174">**Sealed-Case PC** (24)</span></span>

</dt> <dd></dd> <dt>

<span id="Tablet"></span><span id="tablet"></span><span id="TABLET"></span>

<span data-ttu-id="cfa74-175">**Tablet** (30)</span><span class="sxs-lookup"><span data-stu-id="cfa74-175">**Tablet** (30)</span></span>

</dt> <dd></dd> <dt>

<span id="Convertible"></span><span id="Convertible"></span><span id="Convertible"></span>

<span data-ttu-id="cfa74-176">**Conversível** (31)</span><span class="sxs-lookup"><span data-stu-id="cfa74-176">**Convertible** (31)</span></span>

</dt> <dd></dd> <dt>

<span id="Detachable"></span><span id="Detachable "></span><span id="Detachable "></span>

<span data-ttu-id="cfa74-177">**Desanexável** (32)</span><span class="sxs-lookup"><span data-stu-id="cfa74-177">**Detachable** (32)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cfa74-178">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="cfa74-178">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-181">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="cfa74-181">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-182">Nome da primeira classe concreta que aparece na cadeia de herança que é usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="cfa74-182">Name of the first concrete class that appears in the inheritance chain that is used in the creation of an instance.</span></span> <span data-ttu-id="cfa74-183">Quando usado com as outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="cfa74-183">When used with the other key properties of the class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="cfa74-184">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-184">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-185">**CurrentRequiredOrProduced**</span><span class="sxs-lookup"><span data-stu-id="cfa74-185">**CurrentRequiredOrProduced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-186">Tipo de dados: **sint16**</span><span class="sxs-lookup"><span data-stu-id="cfa74-186">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-188">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("amps às 120 volts")</span><span class="sxs-lookup"><span data-stu-id="cfa74-188">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("amps at 120 volts")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-189">O atual é exigido pelo chassi em 120V.</span><span class="sxs-lookup"><span data-stu-id="cfa74-189">Current that is required by the chassis at 120V.</span></span> <span data-ttu-id="cfa74-190">Se a energia for fornecida pelo chassi — como no caso de uma fonte de alimentação ininterrupta (UPS) — essa propriedade poderá indicar a amperagem produzida (como um número negativo).</span><span class="sxs-lookup"><span data-stu-id="cfa74-190">If power is provided by the chassis—as in the case of an uninterruptible power supply (UPS)—this property may indicate the amperage produced (as a negative number).</span></span>

<span data-ttu-id="cfa74-191">Essa propriedade é herdada [**do \_ chassi CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-191">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-192">**Profundidade**</span><span class="sxs-lookup"><span data-stu-id="cfa74-192">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-193">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="cfa74-193">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-195">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="cfa74-195">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-196">Profundidade do pacote físico — em polegadas.</span><span class="sxs-lookup"><span data-stu-id="cfa74-196">Depth of the physical package—in inches.</span></span>

<span data-ttu-id="cfa74-197">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-197">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-198">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cfa74-198">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-199">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-201">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="cfa74-201">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-202">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="cfa74-202">Description of the object.</span></span>

<span data-ttu-id="cfa74-203">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-203">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-204">**HeatGeneration**</span><span class="sxs-lookup"><span data-stu-id="cfa74-204">**HeatGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-205">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfa74-205">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-206">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-207">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("BTU por hora")</span><span class="sxs-lookup"><span data-stu-id="cfa74-207">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("BTU per hour")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-208">Quantidade de calor que é gerada pelo chassi em BTU/hora.</span><span class="sxs-lookup"><span data-stu-id="cfa74-208">Amount of heat that is generated by the chassis in BTU/hour.</span></span>

<span data-ttu-id="cfa74-209">Essa propriedade é herdada [**do \_ chassi CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-209">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-210">**Altura**</span><span class="sxs-lookup"><span data-stu-id="cfa74-210">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-211">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="cfa74-211">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-212">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-213">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="cfa74-213">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-214">Altura do pacote físico — em polegadas.</span><span class="sxs-lookup"><span data-stu-id="cfa74-214">Height of the physical package—in inches.</span></span>

<span data-ttu-id="cfa74-215">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-215">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-216">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="cfa74-216">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-217">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cfa74-217">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-218">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-219">Se for **true**, um pacote físico poderá ser trocado de maneira intercambiável (se for possível substituir o elemento por um fisicamente diferente, mas equivalente um, enquanto o pacote recipiente tiver energia aplicada a ele).</span><span class="sxs-lookup"><span data-stu-id="cfa74-219">If **TRUE**, a physical package can be hot-swapped (if it is possible to replace the element with a physically different but equivalent one while the containing package has power applied to it).</span></span> <span data-ttu-id="cfa74-220">Por exemplo, um pacote de unidade de disco inserido usando conectores de SCA é removível e pode ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="cfa74-220">For example, a disk drive package that is inserted using SCA connectors is removable and can be hot-swapped.</span></span> <span data-ttu-id="cfa74-221">Todos os pacotes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.</span><span class="sxs-lookup"><span data-stu-id="cfa74-221">All packages that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="cfa74-222">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-222">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-223">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="cfa74-223">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-224">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="cfa74-224">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-226">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="cfa74-226">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-227">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="cfa74-227">Date and time the object was installed.</span></span> <span data-ttu-id="cfa74-228">Essa propriedade não requer um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="cfa74-228">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="cfa74-229">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-229">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-230">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="cfa74-230">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-231">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cfa74-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-233">Se for **true**, o quadro será protegido com um bloqueio.</span><span class="sxs-lookup"><span data-stu-id="cfa74-233">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="cfa74-234">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-234">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-235">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="cfa74-235">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-236">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-238">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="cfa74-238">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-239">Nome da organização que produz o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="cfa74-239">Name of the organization that produces the physical element.</span></span>

<span data-ttu-id="cfa74-240">Esse valor é proveniente do membro do **fabricante** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="cfa74-240">This value comes from the **Manufacturer** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="cfa74-241">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-241">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-242">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="cfa74-242">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-243">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-243">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-244">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-245">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="cfa74-245">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-246">Nome pelo qual o elemento físico é conhecido.</span><span class="sxs-lookup"><span data-stu-id="cfa74-246">Name by which the physical element is known.</span></span>

<span data-ttu-id="cfa74-247">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-247">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-248">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cfa74-248">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-251">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="cfa74-251">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-252">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="cfa74-252">Label by which the object is known.</span></span> <span data-ttu-id="cfa74-253">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="cfa74-253">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="cfa74-254">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-254">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-255">**NumberOfPowerCords**</span><span class="sxs-lookup"><span data-stu-id="cfa74-255">**NumberOfPowerCords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-256">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfa74-256">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-257">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-258">Número de cabos de alimentação que devem ser conectados ao chassi para que todos os componentes operem.</span><span class="sxs-lookup"><span data-stu-id="cfa74-258">Number of power cords that must be connected to the chassis for all of the components to operate.</span></span>

<span data-ttu-id="cfa74-259">Essa propriedade é herdada [**do \_ chassi CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-259">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-260">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="cfa74-260">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-261">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-261">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-262">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-262">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-263">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="cfa74-263">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="cfa74-264">Um exemplo são os dados de código de barras associados a um elemento que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="cfa74-264">One example is bar code data that is associated with an element that also has an asset tag.</span></span> <span data-ttu-id="cfa74-265">Lembre-se de que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo ou puderem ser usados como uma chave de elemento, essa propriedade será **NULL** e os dados de código de barras usados como a chave de classe, na propriedade Tag.</span><span class="sxs-lookup"><span data-stu-id="cfa74-265">Be aware that if only bar code data is available and is unique or able to be used as an element key, this property would be **NULL** and the bar code data used as the class key, in the tag property.</span></span>

<span data-ttu-id="cfa74-266">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-266">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-267">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="cfa74-267">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-268">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-270">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="cfa74-270">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-271">Número de peça atribuído pela organização que produz ou fabrica o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="cfa74-271">Part number that is assigned by the organization that produces or manufacturing the physical element.</span></span>

<span data-ttu-id="cfa74-272">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-272">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-273">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="cfa74-273">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-274">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cfa74-274">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-275">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-275">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-276">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="cfa74-276">If **TRUE**, the physical element is powered ON.</span></span>

<span data-ttu-id="cfa74-277">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-277">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-278">**Removível**</span><span class="sxs-lookup"><span data-stu-id="cfa74-278">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-279">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cfa74-279">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-280">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-281">Se for **true**, um pacote físico será removível (se for projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem encontrar a função do empacotamento geral).</span><span class="sxs-lookup"><span data-stu-id="cfa74-281">If **TRUE**, a physical package is removable (if it is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging).</span></span> <span data-ttu-id="cfa74-282">Um pacote ainda poderá ser removível se a potência precisar ser "desativada" para executar a remoção.</span><span class="sxs-lookup"><span data-stu-id="cfa74-282">A package can still be removable if the power must be "OFF" to perform the removal.</span></span> <span data-ttu-id="cfa74-283">Se o pacote puder ser removido enquanto a energia estiver ATIVAda, o elemento será removível e poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="cfa74-283">If the package can be removed while the power is ON, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="cfa74-284">Por exemplo, uma bateria extra em um laptop é removível, assim como um pacote de unidade de disco que é inserido usando conectores do aplicativo de configuração de servidor (SCA).</span><span class="sxs-lookup"><span data-stu-id="cfa74-284">For example, an extra battery in a laptop is removable, as is a disk drive package that is inserted using Server Configuration Application (SCA) connectors.</span></span> <span data-ttu-id="cfa74-285">No entanto, o último pode ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="cfa74-285">However, the latter can be hot-swapped.</span></span> <span data-ttu-id="cfa74-286">Uma exibição de laptop não é removível, nem uma fonte de alimentação não redundante.</span><span class="sxs-lookup"><span data-stu-id="cfa74-286">A laptop display is not removable, nor is a nonredundant power supply.</span></span> <span data-ttu-id="cfa74-287">A remoção desses componentes afetaria a função do empacotamento geral ou é impossível devido à forte integração do pacote.</span><span class="sxs-lookup"><span data-stu-id="cfa74-287">Removing these components would affect the function of the overall packaging or is impossible because of the tight integration of the package.</span></span>

<span data-ttu-id="cfa74-288">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-288">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-289">**Peças**</span><span class="sxs-lookup"><span data-stu-id="cfa74-289">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-290">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cfa74-290">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-291">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-292">Se **for true**, esse componente de mídia física poderá ser substituído por um fisicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="cfa74-292">If **TRUE**, this physical media component can be replaced with a physically different one.</span></span> <span data-ttu-id="cfa74-293">Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta.</span><span class="sxs-lookup"><span data-stu-id="cfa74-293">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="cfa74-294">Nesse caso, diz-se que o processador é substituível.</span><span class="sxs-lookup"><span data-stu-id="cfa74-294">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="cfa74-295">Outro exemplo é um pacote de fornecimento de energia montado em trilhos deslizantes.</span><span class="sxs-lookup"><span data-stu-id="cfa74-295">Another example is a power supply package mounted on sliding rails.</span></span> <span data-ttu-id="cfa74-296">Todos os pacotes removíveis são inerentemente substituíveis.</span><span class="sxs-lookup"><span data-stu-id="cfa74-296">All removable packages are inherently replaceable.</span></span>

<span data-ttu-id="cfa74-297">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-297">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-298">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="cfa74-298">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-299">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfa74-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-301">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Tabela global de contêiner físico DMTF \| 2,12 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="cfa74-301">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-302">Status de uma violação física do quadro.</span><span class="sxs-lookup"><span data-stu-id="cfa74-302">Status of a physical breach of the frame.</span></span>

<span data-ttu-id="cfa74-303">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-303">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cfa74-304">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="cfa74-304">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cfa74-305">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="cfa74-305">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="cfa74-306">**Sem violação** (3)</span><span class="sxs-lookup"><span data-stu-id="cfa74-306">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="cfa74-307">**Tentativa de violação** (4)</span><span class="sxs-lookup"><span data-stu-id="cfa74-307">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="cfa74-308">**Violação bem-sucedida** (5)</span><span class="sxs-lookup"><span data-stu-id="cfa74-308">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cfa74-309">**SecurityStatus**</span><span class="sxs-lookup"><span data-stu-id="cfa74-309">**SecurityStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-310">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfa74-310">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-311">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-312">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("status de segurança do SMBIOS \| tipo 3 \| ")</span><span class="sxs-lookup"><span data-stu-id="cfa74-312">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 3\|Security Status")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-313">Configuração de segurança para entrada externa, por exemplo, um teclado, para um computador.</span><span class="sxs-lookup"><span data-stu-id="cfa74-313">Security setting for external input, for example, a keyboard, to a computer.</span></span>

<span data-ttu-id="cfa74-314">Esse valor é proveniente do membro de **status de segurança** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="cfa74-314">This value comes from the **Security Status** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cfa74-315">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="cfa74-315">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cfa74-316">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="cfa74-316">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="cfa74-317">**Nenhum** (3)</span><span class="sxs-lookup"><span data-stu-id="cfa74-317">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="External_interface_locked_out"></span><span id="external_interface_locked_out"></span><span id="EXTERNAL_INTERFACE_LOCKED_OUT"></span>

<span data-ttu-id="cfa74-318">**Interface externa bloqueada** (4)</span><span class="sxs-lookup"><span data-stu-id="cfa74-318">**External interface locked out** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="External_interface_enabled"></span><span id="external_interface_enabled"></span><span id="EXTERNAL_INTERFACE_ENABLED"></span>

<span data-ttu-id="cfa74-319">**Interface externa habilitada** (5)</span><span class="sxs-lookup"><span data-stu-id="cfa74-319">**External interface enabled** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cfa74-320">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="cfa74-320">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-321">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-321">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-322">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-322">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-323">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="cfa74-323">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-324">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="cfa74-324">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="cfa74-325">Esse valor é proveniente do membro de **número de série** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="cfa74-325">This value comes from the **Serial Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="cfa74-326">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-326">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-327">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="cfa74-327">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-328">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-328">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-330">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ CIM PhysicalFrame**](cim-physicalframe.md).**Infilosofia**")</span><span class="sxs-lookup"><span data-stu-id="cfa74-330">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-331">Matriz de explicações mais detalhadas para qualquer uma das entradas na matriz de **unifilosofia** .</span><span class="sxs-lookup"><span data-stu-id="cfa74-331">Array of more detailed explanations for any of the entries in the **ServicePhilosophy** array.</span></span> <span data-ttu-id="cfa74-332">Lembre-se de que cada entrada dessa matriz está relacionada à entrada no **perfilosofia** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="cfa74-332">Be aware that each entry of this array is related to the entry in **ServicePhilosophy** that is located at the same index.</span></span>

<span data-ttu-id="cfa74-333">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-333">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-334">**Infilosofia**</span><span class="sxs-lookup"><span data-stu-id="cfa74-334">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-335">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="cfa74-335">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-337">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ CIM PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="cfa74-337">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-338">Matriz que inclui se o quadro é atendido de cima, para frente, para trás ou para o lado, se o quadro tem bandejas deslizantes ou lados removíveis e se o quadro é móvel, por exemplo, com os cilindros.</span><span class="sxs-lookup"><span data-stu-id="cfa74-338">Array that includes whether the frame is serviced from the top, front, back, or side, whether the frame has sliding trays or removable sides, and whether the frame is moveable—for example, having rollers.</span></span>

<span data-ttu-id="cfa74-339">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-339">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cfa74-340">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="cfa74-340">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="cfa74-341">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="cfa74-341">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="cfa74-342">**Serviço da parte superior** (2)</span><span class="sxs-lookup"><span data-stu-id="cfa74-342">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="cfa74-343">**Serviço da frente** (3)</span><span class="sxs-lookup"><span data-stu-id="cfa74-343">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="cfa74-344">**Serviço de volta** (4)</span><span class="sxs-lookup"><span data-stu-id="cfa74-344">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="cfa74-345">**Serviço do lado** (5)</span><span class="sxs-lookup"><span data-stu-id="cfa74-345">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="cfa74-346">**Bandejas deslizantes** (6)</span><span class="sxs-lookup"><span data-stu-id="cfa74-346">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="cfa74-347">**Lados removíveis** (7)</span><span class="sxs-lookup"><span data-stu-id="cfa74-347">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="cfa74-348">**Móvel** (8)</span><span class="sxs-lookup"><span data-stu-id="cfa74-348">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cfa74-349">**SKU**</span><span class="sxs-lookup"><span data-stu-id="cfa74-349">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-350">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-352">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="cfa74-352">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-353">Número de unidade de manutenção de estoque do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="cfa74-353">Stock keeping unit number for the physical element.</span></span>

<span data-ttu-id="cfa74-354">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-355">**SMBIOSAssetTag**</span><span class="sxs-lookup"><span data-stu-id="cfa74-355">**SMBIOSAssetTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-356">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-356">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-358">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("marca de ativo do SMBIOS \| tipo 3 \| ")</span><span class="sxs-lookup"><span data-stu-id="cfa74-358">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 3\|Asset Tag")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-359">Número da marca do ativo do compartimento do sistema.</span><span class="sxs-lookup"><span data-stu-id="cfa74-359">Asset tag number of the system enclosure.</span></span>

<span data-ttu-id="cfa74-360">Esse valor é proveniente do membro de **número de marca de ativo** do compartimento do **sistema ou** da estrutura do chassi nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="cfa74-360">This value comes from the **Asset Tag Number** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-361">**Status**</span><span class="sxs-lookup"><span data-stu-id="cfa74-361">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-362">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-362">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-363">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-364">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="cfa74-364">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-365">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="cfa74-365">Current status of the object.</span></span> <span data-ttu-id="cfa74-366">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="cfa74-366">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="cfa74-367">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="cfa74-367">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="cfa74-368">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="cfa74-368">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="cfa74-369">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="cfa74-369">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="cfa74-370">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="cfa74-370">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="cfa74-371">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-371">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="cfa74-372">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cfa74-372">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="cfa74-373">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="cfa74-373">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="cfa74-374">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="cfa74-374">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="cfa74-375">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="cfa74-375">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="cfa74-376">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="cfa74-376">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="cfa74-377">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="cfa74-377">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="cfa74-378">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="cfa74-378">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="cfa74-379">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="cfa74-379">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="cfa74-380">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="cfa74-380">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="cfa74-381">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="cfa74-381">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="cfa74-382">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="cfa74-382">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="cfa74-383">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="cfa74-383">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="cfa74-384">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="cfa74-384">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="cfa74-385">**Tag**</span><span class="sxs-lookup"><span data-stu-id="cfa74-385">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-386">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-388">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="cfa74-388">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-389">Identificador exclusivo do compartimento do sistema.</span><span class="sxs-lookup"><span data-stu-id="cfa74-389">Unique identifier of the system enclosure.</span></span>

<span data-ttu-id="cfa74-390">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-390">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="cfa74-391">Exemplo: "compartimento do sistema 1"</span><span class="sxs-lookup"><span data-stu-id="cfa74-391">Example: "System Enclosure 1"</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-392">**TypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="cfa74-392">**TypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-393">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-393">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-395">Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ chassi CIM**](cim-chassis.md).**ChassisTypes**")</span><span class="sxs-lookup"><span data-stu-id="cfa74-395">Qualifiers: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("Indexed"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Chassis**](cim-chassis.md).**ChassisTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-396">Matriz de mais informações sobre as entradas de matriz **ChassisTypes** .</span><span class="sxs-lookup"><span data-stu-id="cfa74-396">Array of more information about the **ChassisTypes** array entries.</span></span> <span data-ttu-id="cfa74-397">Lembre-se de que cada entrada dessa matriz está relacionada à entrada em **ChassisTypes** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="cfa74-397">Be aware that each entry of this array is related to the entry in **ChassisTypes** that is located at the same index.</span></span>

<span data-ttu-id="cfa74-398">Essa propriedade é herdada [**do \_ chassi CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-398">This property is inherited from [**CIM\_Chassis**](cim-chassis.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-399">**Versão**</span><span class="sxs-lookup"><span data-stu-id="cfa74-399">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-400">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="cfa74-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-401">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-402">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="cfa74-402">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-403">Versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="cfa74-403">Version of the physical element.</span></span>

<span data-ttu-id="cfa74-404">Esse valor é proveniente do membro da **versão** do **compartimento do sistema ou** da estrutura do chassi nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="cfa74-404">This value comes from the **Version** member of the **System Enclosure or Chassis** structure in the SMBIOS information.</span></span>

<span data-ttu-id="cfa74-405">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-405">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-406">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="cfa74-406">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-407">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="cfa74-407">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-408">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-408">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-409">Se **for true**, o equipamento incluirá um alarme visível.</span><span class="sxs-lookup"><span data-stu-id="cfa74-409">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="cfa74-410">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-410">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-411">**Weight**</span><span class="sxs-lookup"><span data-stu-id="cfa74-411">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-412">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="cfa74-412">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-414">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("libras")</span><span class="sxs-lookup"><span data-stu-id="cfa74-414">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-415">Peso do pacote físico em libras.</span><span class="sxs-lookup"><span data-stu-id="cfa74-415">Weight of the physical package in pounds.</span></span>

<span data-ttu-id="cfa74-416">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-416">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="cfa74-417">**Largura**</span><span class="sxs-lookup"><span data-stu-id="cfa74-417">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cfa74-418">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="cfa74-418">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-419">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cfa74-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cfa74-420">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="cfa74-420">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="cfa74-421">Largura do pacote físico em polegadas.</span><span class="sxs-lookup"><span data-stu-id="cfa74-421">Width of the physical package in inches.</span></span>

<span data-ttu-id="cfa74-422">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-422">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cfa74-423">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfa74-423">Remarks</span></span>

<span data-ttu-id="cfa74-424">A classe **Win32 \_ SystemEnclosure** é derivada do [**\_ chassi CIM**](cim-chassis.md).</span><span class="sxs-lookup"><span data-stu-id="cfa74-424">The **Win32\_SystemEnclosure** class is derived from [**CIM\_Chassis**](cim-chassis.md).</span></span>

## <a name="examples"></a><span data-ttu-id="cfa74-425">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cfa74-425">Examples</span></span>

<span data-ttu-id="cfa74-426">O exemplo de [coleta de ativos de sistema multithread com](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell do PowerShell na galeria do TechNet usa várias classes, incluindo **Win32 \_ SystemEnclosure**, para recuperar dados de um sistema.</span><span class="sxs-lookup"><span data-stu-id="cfa74-426">The [Multithreaded System Asset Gathering with Powershell](https://Gallery.TechNet.Microsoft.Com/Multithreaded-System-Asset-856a8f7c) PowerShell example on TechNet gallery uses a number of classes, including **Win32\_SystemEnclosure**, to retrieve data from a system.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfa74-427">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfa74-427">Requirements</span></span>



| <span data-ttu-id="cfa74-428">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfa74-428">Requirement</span></span> | <span data-ttu-id="cfa74-429">Valor</span><span class="sxs-lookup"><span data-stu-id="cfa74-429">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfa74-430">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfa74-430">Minimum supported client</span></span><br/> | <span data-ttu-id="cfa74-431">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cfa74-431">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cfa74-432">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cfa74-432">Minimum supported server</span></span><br/> | <span data-ttu-id="cfa74-433">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfa74-433">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cfa74-434">Namespace</span><span class="sxs-lookup"><span data-stu-id="cfa74-434">Namespace</span></span><br/>                | <span data-ttu-id="cfa74-435">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cfa74-435">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cfa74-436">MOF</span><span class="sxs-lookup"><span data-stu-id="cfa74-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfa74-437"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cfa74-437"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfa74-438">DLL</span><span class="sxs-lookup"><span data-stu-id="cfa74-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfa74-439"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfa74-439"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfa74-440">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfa74-440">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfa74-441">**\_Chassi CIM**</span><span class="sxs-lookup"><span data-stu-id="cfa74-441">**CIM\_Chassis**</span></span>](cim-chassis.md)
</dt> <dt>

[<span data-ttu-id="cfa74-442">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="cfa74-442">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="cfa74-443">Tarefas do WMI: hardware do computador</span><span class="sxs-lookup"><span data-stu-id="cfa74-443">WMI Tasks: Computer Hardware</span></span>](../wmisdk/wmi-tasks--computer-hardware.md)
</dt> </dl>

 

 
