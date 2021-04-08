---
description: A \_ classe de chassi CIM representa os elementos físicos que incluem outros elementos e fornece funcionalidade definíveis, como um desktop, nó de processamento, UPS, armazenamento em disco ou fita ou uma combinação desses.
ms.assetid: 4c55dbff-bc4a-4cc9-8f34-29636defaa56
ms.tgt_platform: multiple
title: Classe CIM_Chassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis
- CIM_Chassis.Caption
- CIM_Chassis.Description
- CIM_Chassis.InstallDate
- CIM_Chassis.Name
- CIM_Chassis.Status
- CIM_Chassis.CreationClassName
- CIM_Chassis.Manufacturer
- CIM_Chassis.Model
- CIM_Chassis.OtherIdentifyingInfo
- CIM_Chassis.PartNumber
- CIM_Chassis.PoweredOn
- CIM_Chassis.SerialNumber
- CIM_Chassis.SKU
- CIM_Chassis.Tag
- CIM_Chassis.Version
- CIM_Chassis.Depth
- CIM_Chassis.Height
- CIM_Chassis.HotSwappable
- CIM_Chassis.Removable
- CIM_Chassis.Replaceable
- CIM_Chassis.Weight
- CIM_Chassis.Width
- CIM_Chassis.AudibleAlarm
- CIM_Chassis.BreachDescription
- CIM_Chassis.CableManagementStrategy
- CIM_Chassis.LockPresent
- CIM_Chassis.SecurityBreach
- CIM_Chassis.ServiceDescriptions
- CIM_Chassis.ServicePhilosophy
- CIM_Chassis.VisibleAlarm
- CIM_Chassis.ChassisTypes
- CIM_Chassis.CurrentRequiredOrProduced
- CIM_Chassis.HeatGeneration
- CIM_Chassis.NumberOfPowerCords
- CIM_Chassis.TypeDescriptions
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b1eb7f5e2733056cf48c1c9333453613ace699c6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089354"
---
# <a name="cim_chassis-class"></a><span data-ttu-id="01e1a-103">\_Classe de chassi CIM</span><span class="sxs-lookup"><span data-stu-id="01e1a-103">CIM\_Chassis class</span></span>

<span data-ttu-id="01e1a-104">A classe de **\_ chassi CIM** representa os elementos físicos que incluem outros elementos e fornece funcionalidade definíveis, como um desktop, nó de processamento, UPS, armazenamento em disco ou fita ou uma combinação desses.</span><span class="sxs-lookup"><span data-stu-id="01e1a-104">The **CIM\_Chassis** class represents the physical elements that enclose other elements and provide definable functionality, such as a desktop, processing node, UPS, disk or tape storage, or a combination of these.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01e1a-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="01e1a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="01e1a-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="01e1a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="01e1a-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="01e1a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="01e1a-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="01e1a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01e1a-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01e1a-109">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B72-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chassis : CIM_PhysicalFrame
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  boolean  LockPresent;
  uint16   SecurityBreach;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  boolean  VisibleAlarm;
  uint16   ChassisTypes[];
  sint16   CurrentRequiredOrProduced;
  uint16   HeatGeneration;
  uint16   NumberOfPowerCords;
  string   TypeDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="01e1a-110">Membros</span><span class="sxs-lookup"><span data-stu-id="01e1a-110">Members</span></span>

<span data-ttu-id="01e1a-111">A classe de **\_ chassi CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="01e1a-111">The **CIM\_Chassis** class has these types of members:</span></span>

-   [<span data-ttu-id="01e1a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="01e1a-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="01e1a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01e1a-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="01e1a-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="01e1a-114">Methods</span></span>

<span data-ttu-id="01e1a-115">A classe de **\_ chassi CIM** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="01e1a-115">The **CIM\_Chassis** class has these methods.</span></span>



| <span data-ttu-id="01e1a-116">Método</span><span class="sxs-lookup"><span data-stu-id="01e1a-116">Method</span></span>                                                           | <span data-ttu-id="01e1a-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="01e1a-117">Description</span></span>                                                                                                                                      |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01e1a-118">**Iscompatível**</span><span class="sxs-lookup"><span data-stu-id="01e1a-118">**IsCompatible**</span></span>](iscompatible-method-in-class-cim-chassis.md) | <span data-ttu-id="01e1a-119">Verifica se o elemento físico referenciado pode ser contido ou inserido no pacote físico.</span><span class="sxs-lookup"><span data-stu-id="01e1a-119">Verifies whether the referenced physical element can be contained by, or inserted into, the physical package.</span></span> <span data-ttu-id="01e1a-120">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="01e1a-120">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="01e1a-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="01e1a-121">Properties</span></span>

<span data-ttu-id="01e1a-122">A classe de **\_ chassi CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="01e1a-122">The **CIM\_Chassis** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01e1a-123">**AudibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="01e1a-123">**AudibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-124">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="01e1a-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-126">Se for **true**, o quadro será equipado com um alarme audível.</span><span class="sxs-lookup"><span data-stu-id="01e1a-126">If **TRUE**, the frame is equipped with an audible alarm.</span></span>

<span data-ttu-id="01e1a-127">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-127">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-128">**BreachDescription**</span><span class="sxs-lookup"><span data-stu-id="01e1a-128">**BreachDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-131">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span><span class="sxs-lookup"><span data-stu-id="01e1a-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-132">Cadeia de caracteres de forma livre que fornece mais informações se a propriedade **SecurityBreach** indicar que ocorreu uma violação ou algum outro evento relacionado à segurança.</span><span class="sxs-lookup"><span data-stu-id="01e1a-132">Free-form string that provides more information if the **SecurityBreach** property indicates that a breach or some other security-related event occurred.</span></span>

<span data-ttu-id="01e1a-133">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-133">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-134">**CableManagementStrategy**</span><span class="sxs-lookup"><span data-stu-id="01e1a-134">**CableManagementStrategy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-137">Cadeia de caracteres de forma livre que contém informações sobre como os vários cabos são conectados e agrupados para o quadro.</span><span class="sxs-lookup"><span data-stu-id="01e1a-137">Free-form string that contains information on how the various cables are connected and bundled for the frame.</span></span> <span data-ttu-id="01e1a-138">Com muitos cabos de rede, relacionados ao armazenamento e de energia, o gerenciamento de cabos pode ser um esforço complexo e desafiador.</span><span class="sxs-lookup"><span data-stu-id="01e1a-138">With many networking, storage-related, and power cables, cable management can be a complex and challenging endeavor.</span></span> <span data-ttu-id="01e1a-139">Essa propriedade de cadeia de caracteres contém informações para auxiliar no assembly e no serviço do quadro.</span><span class="sxs-lookup"><span data-stu-id="01e1a-139">This string property contains information to aid in assembly and service of the frame.</span></span>

<span data-ttu-id="01e1a-140">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-140">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-141">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="01e1a-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-144">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="01e1a-144">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-145">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="01e1a-145">A short textual description of the object.</span></span>

<span data-ttu-id="01e1a-146">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-147">**ChassisTypes**</span><span class="sxs-lookup"><span data-stu-id="01e1a-147">**ChassisTypes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-148">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01e1a-148">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-150">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Tabela global de contêiner físico DMTF \| 2,1 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ chassi CIM**.**TypeDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="01e1a-150">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.1"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Chassis**.**TypeDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-151">Enumeração, matriz com valor inteiro que indica o tipo de chassi.</span><span class="sxs-lookup"><span data-stu-id="01e1a-151">Enumerated, integer-valued array that indicates the type of chassis.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="01e1a-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="01e1a-152"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-153">Outros.</span><span class="sxs-lookup"><span data-stu-id="01e1a-153">Other.</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01e1a-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="01e1a-154"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-155">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="01e1a-155">Unknown.</span></span>

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="01e1a-156"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Área de trabalho** (3)</span><span class="sxs-lookup"><span data-stu-id="01e1a-156"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (3)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-157">Desktop.</span><span class="sxs-lookup"><span data-stu-id="01e1a-157">Desktop.</span></span>

</dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span data-ttu-id="01e1a-158"><span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Área de trabalho de baixo perfil** (4)</span><span class="sxs-lookup"><span data-stu-id="01e1a-158"><span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**Low Profile Desktop** (4)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-159">Área de trabalho de baixo perfil.</span><span class="sxs-lookup"><span data-stu-id="01e1a-159">Low-profile desktop.</span></span>

</dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span data-ttu-id="01e1a-160"><span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Caixa de pizza** (5)</span><span class="sxs-lookup"><span data-stu-id="01e1a-160"><span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**Pizza Box** (5)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-161">Caixa de pizza.</span><span class="sxs-lookup"><span data-stu-id="01e1a-161">Pizza box.</span></span>

</dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span data-ttu-id="01e1a-162"><span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Mini-torre** (6)</span><span class="sxs-lookup"><span data-stu-id="01e1a-162"><span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**Mini Tower** (6)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-163">Mini-torre.</span><span class="sxs-lookup"><span data-stu-id="01e1a-163">Mini tower.</span></span>

</dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span data-ttu-id="01e1a-164"><span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Torre** (7)</span><span class="sxs-lookup"><span data-stu-id="01e1a-164"><span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**Tower** (7)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-165">Torre.</span><span class="sxs-lookup"><span data-stu-id="01e1a-165">Tower.</span></span>

</dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span data-ttu-id="01e1a-166"><span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Portátil** (8)</span><span class="sxs-lookup"><span data-stu-id="01e1a-166"><span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**Portable** (8)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-167">Portátil.</span><span class="sxs-lookup"><span data-stu-id="01e1a-167">Portable.</span></span>

</dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="01e1a-168"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (9)</span><span class="sxs-lookup"><span data-stu-id="01e1a-168"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (9)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-169">Laptop.</span><span class="sxs-lookup"><span data-stu-id="01e1a-169">Laptop.</span></span>

</dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span data-ttu-id="01e1a-170"><span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Notebook** (10)</span><span class="sxs-lookup"><span data-stu-id="01e1a-170"><span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**Notebook** (10)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-171">D430.</span><span class="sxs-lookup"><span data-stu-id="01e1a-171">Notebook.</span></span>

</dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span data-ttu-id="01e1a-172"><span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Mão suspensa** (11)</span><span class="sxs-lookup"><span data-stu-id="01e1a-172"><span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**Hand Held** (11)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-173">Mão.</span><span class="sxs-lookup"><span data-stu-id="01e1a-173">Hand-held.</span></span>

</dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span data-ttu-id="01e1a-174"><span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Estação de encaixe** (12)</span><span class="sxs-lookup"><span data-stu-id="01e1a-174"><span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**Docking Station** (12)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-175">Estação de encaixe.</span><span class="sxs-lookup"><span data-stu-id="01e1a-175">Docking station.</span></span>

</dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span data-ttu-id="01e1a-176"><span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**Tudo em um** (13)</span><span class="sxs-lookup"><span data-stu-id="01e1a-176"><span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**All in One** (13)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-177">Tudo-em-um.</span><span class="sxs-lookup"><span data-stu-id="01e1a-177">All-in-one.</span></span>

</dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span data-ttu-id="01e1a-178"><span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Subnotebook** (14)</span><span class="sxs-lookup"><span data-stu-id="01e1a-178"><span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**Sub Notebook** (14)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-179">Subnotebook.</span><span class="sxs-lookup"><span data-stu-id="01e1a-179">Subnotebook.</span></span>

</dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span data-ttu-id="01e1a-180"><span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Economia de espaço** (15)</span><span class="sxs-lookup"><span data-stu-id="01e1a-180"><span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**Space-Saving** (15)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-181">Economia de espaço.</span><span class="sxs-lookup"><span data-stu-id="01e1a-181">Space-saving.</span></span>

</dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span data-ttu-id="01e1a-182"><span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Caixa de almoço** (16)</span><span class="sxs-lookup"><span data-stu-id="01e1a-182"><span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>**Lunch Box** (16)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-183">Caixa de almoço.</span><span class="sxs-lookup"><span data-stu-id="01e1a-183">Lunch box.</span></span>

</dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span data-ttu-id="01e1a-184"><span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Chassi do sistema principal** (17)</span><span class="sxs-lookup"><span data-stu-id="01e1a-184"><span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**Main System Chassis** (17)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-185">Chassi do sistema principal.</span><span class="sxs-lookup"><span data-stu-id="01e1a-185">Main system chassis.</span></span>

</dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span data-ttu-id="01e1a-186"><span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Chassi de expansão** (18)</span><span class="sxs-lookup"><span data-stu-id="01e1a-186"><span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**Expansion Chassis** (18)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-187">Chassi de expansão.</span><span class="sxs-lookup"><span data-stu-id="01e1a-187">Expansion chassis.</span></span>

</dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span data-ttu-id="01e1a-188"><span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**Subchassi** (19)</span><span class="sxs-lookup"><span data-stu-id="01e1a-188"><span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**SubChassis** (19)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-189">Subchassi.</span><span class="sxs-lookup"><span data-stu-id="01e1a-189">Subchassis.</span></span>

</dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span data-ttu-id="01e1a-190"><span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Chassi de expansão de barramento** (20)</span><span class="sxs-lookup"><span data-stu-id="01e1a-190"><span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**Bus Expansion Chassis** (20)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-191">Chassi de expansão de barramento.</span><span class="sxs-lookup"><span data-stu-id="01e1a-191">Bus-expansion chassis.</span></span>

</dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span data-ttu-id="01e1a-192"><span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Chassi de periférico** (21)</span><span class="sxs-lookup"><span data-stu-id="01e1a-192"><span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**Peripheral Chassis** (21)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-193">Chassi periférico.</span><span class="sxs-lookup"><span data-stu-id="01e1a-193">Peripheral chassis.</span></span>

</dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span data-ttu-id="01e1a-194"><span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Chassi de armazenamento** (22)</span><span class="sxs-lookup"><span data-stu-id="01e1a-194"><span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**Storage Chassis** (22)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-195">Chassi de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="01e1a-195">Storage chassis.</span></span>

</dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span data-ttu-id="01e1a-196"><span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Chassi de montagem em rack** (23)</span><span class="sxs-lookup"><span data-stu-id="01e1a-196"><span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**Rack Mount Chassis** (23)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-197">Chassi de montagem de rack.</span><span class="sxs-lookup"><span data-stu-id="01e1a-197">Rack-mount chassis.</span></span>

</dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span data-ttu-id="01e1a-198"><span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**PC de caso lacrado** (24)</span><span class="sxs-lookup"><span data-stu-id="01e1a-198"><span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**Sealed-Case PC** (24)</span></span>


</dt> <dd>

<span data-ttu-id="01e1a-199">Computador com casos lacrados.</span><span class="sxs-lookup"><span data-stu-id="01e1a-199">Sealed-case computer.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="01e1a-200">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="01e1a-200">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-201">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-201">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-202">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-202">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-203">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="01e1a-203">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-204">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="01e1a-204">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="01e1a-205">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="01e1a-205">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="01e1a-206">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-206">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-207">**CurrentRequiredOrProduced**</span><span class="sxs-lookup"><span data-stu-id="01e1a-207">**CurrentRequiredOrProduced**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-208">Tipo de dados: **sint16**</span><span class="sxs-lookup"><span data-stu-id="01e1a-208">Data type: **sint16**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-210">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("amps às 120 volts")</span><span class="sxs-lookup"><span data-stu-id="01e1a-210">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("amps at 120 volts")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-211">Atualmente exigido pelo chassi às 120 volts.</span><span class="sxs-lookup"><span data-stu-id="01e1a-211">Currently required by the chassis at 120 volts.</span></span> <span data-ttu-id="01e1a-212">Se a energia for fornecida pelo chassi (como no caso de um UPS), essa propriedade poderá indicar a amperagem produzida, como um número negativo.</span><span class="sxs-lookup"><span data-stu-id="01e1a-212">If power is provided by the chassis (as in the case of a UPS), this property can indicate the amperage produced, as a negative number.</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-213">**Profundidade**</span><span class="sxs-lookup"><span data-stu-id="01e1a-213">**Depth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-214">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="01e1a-214">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-215">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-216">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="01e1a-216">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-217">Profundidade do pacote físico, em polegadas.</span><span class="sxs-lookup"><span data-stu-id="01e1a-217">Depth of the physical package, in inches.</span></span>

<span data-ttu-id="01e1a-218">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-218">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-219">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="01e1a-219">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-220">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-221">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-221">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-222">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="01e1a-222">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-223">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="01e1a-223">A textual description of the object.</span></span>

<span data-ttu-id="01e1a-224">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-224">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-225">**HeatGeneration**</span><span class="sxs-lookup"><span data-stu-id="01e1a-225">**HeatGeneration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-226">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01e1a-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-227">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-228">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("BTU por hora")</span><span class="sxs-lookup"><span data-stu-id="01e1a-228">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("BTU per hour")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-229">Quantidade de calor gerada pelo chassi em BTU/hora.</span><span class="sxs-lookup"><span data-stu-id="01e1a-229">Amount of heat generated by the chassis in Btu/hour.</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-230">**Altura**</span><span class="sxs-lookup"><span data-stu-id="01e1a-230">**Height**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-231">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="01e1a-231">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-233">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="01e1a-233">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-234">Altura do pacote físico, em polegadas.</span><span class="sxs-lookup"><span data-stu-id="01e1a-234">Height of the physical package, in inches.</span></span>

<span data-ttu-id="01e1a-235">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-235">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-236">**HotSwappable**</span><span class="sxs-lookup"><span data-stu-id="01e1a-236">**HotSwappable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-237">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="01e1a-237">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-239">Se **for true**, o pacote poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="01e1a-239">If **TRUE**, the package can be hot-swapped.</span></span> <span data-ttu-id="01e1a-240">Um pacote físico pode ser intercambiável se o elemento puder ser substituído por um fisicamente diferente (mas equivalente) um enquanto o pacote que o contém está ativado.</span><span class="sxs-lookup"><span data-stu-id="01e1a-240">A physical package can be hot-swapped if the element can be replaced by a physically different (but equivalent) one while the containing package is turned on.</span></span> <span data-ttu-id="01e1a-241">Por exemplo, um componente de ventilador pode ser projetado para ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="01e1a-241">For example, a fan component may be designed to be hot-swapped.</span></span> <span data-ttu-id="01e1a-242">Todos os componentes que podem ser intercambiáveis são inerentemente removíveis e substituíveis.</span><span class="sxs-lookup"><span data-stu-id="01e1a-242">All components that can be hot-swapped are inherently removable and replaceable.</span></span>

<span data-ttu-id="01e1a-243">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-243">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-244">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="01e1a-244">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-245">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="01e1a-245">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-247">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="01e1a-247">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-248">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="01e1a-248">Indicates when the object was installed.</span></span> <span data-ttu-id="01e1a-249">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="01e1a-249">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="01e1a-250">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-250">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-251">**LockPresent**</span><span class="sxs-lookup"><span data-stu-id="01e1a-251">**LockPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-252">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="01e1a-252">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-253">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-254">Se for **true**, o quadro será protegido com um bloqueio.</span><span class="sxs-lookup"><span data-stu-id="01e1a-254">If **TRUE**, the frame is protected with a lock.</span></span>

<span data-ttu-id="01e1a-255">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-255">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-256">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="01e1a-256">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-259">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="01e1a-259">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-260">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="01e1a-260">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="01e1a-261">Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-261">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="01e1a-262">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-263">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="01e1a-263">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-266">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="01e1a-266">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-267">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="01e1a-267">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="01e1a-268">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-268">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-269">**Nome**</span><span class="sxs-lookup"><span data-stu-id="01e1a-269">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-270">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-270">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-271">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-272">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="01e1a-272">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-273">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="01e1a-273">Label by which the object is known.</span></span> <span data-ttu-id="01e1a-274">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="01e1a-274">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="01e1a-275">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-275">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-276">**NumberOfPowerCords**</span><span class="sxs-lookup"><span data-stu-id="01e1a-276">**NumberOfPowerCords**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-277">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01e1a-277">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-278">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-279">Número de cabos de alimentação que devem ser conectados ao chassi para que todos os componentes possam operar.</span><span class="sxs-lookup"><span data-stu-id="01e1a-279">Number of power cords that must be connected to the chassis so that all of the components can operate.</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-280">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="01e1a-280">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-281">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-281">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-282">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-282">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-283">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="01e1a-283">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="01e1a-284">Um exemplo são dados de código de barras associados a um elemento, que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="01e1a-284">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="01e1a-285">Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo e puderem ser usados como uma chave de elemento, essa propriedade será nula e os dados de código de barras seriam usados como a chave de classe na propriedade de **marca** .</span><span class="sxs-lookup"><span data-stu-id="01e1a-285">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="01e1a-286">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-286">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-287">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="01e1a-287">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-288">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-288">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-289">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-289">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-290">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="01e1a-290">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-291">Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="01e1a-291">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="01e1a-292">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-292">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-293">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="01e1a-293">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-294">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="01e1a-294">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-295">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-296">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="01e1a-296">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="01e1a-297">Caso contrário, ele estará desativado no momento.</span><span class="sxs-lookup"><span data-stu-id="01e1a-297">Otherwise, it is currently off.</span></span>

<span data-ttu-id="01e1a-298">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-298">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-299">**Removível**</span><span class="sxs-lookup"><span data-stu-id="01e1a-299">**Removable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-300">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="01e1a-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-301">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-302">Se for **true**, o pacote será projetado para ser levado para dentro e para fora do contêiner físico no qual ele normalmente é encontrado, sem comprometer a função do empacotamento geral.</span><span class="sxs-lookup"><span data-stu-id="01e1a-302">If **TRUE**, the package is designed to be taken in and out of the physical container in which it is normally found, without impairing the function of the overall packaging.</span></span> <span data-ttu-id="01e1a-303">Um pacote é considerado removível, mesmo que a energia precise ser desligada para executar a remoção.</span><span class="sxs-lookup"><span data-stu-id="01e1a-303">A package is considered removable even if the power must be off to perform the removal.</span></span> <span data-ttu-id="01e1a-304">Se a energia puder ser ativada e o pacote for removido, o elemento será removível e poderá ser intercambiável.</span><span class="sxs-lookup"><span data-stu-id="01e1a-304">If the power can be on and the package removed, then the element is removable and can be hot-swapped.</span></span> <span data-ttu-id="01e1a-305">Por exemplo, um chip de processador atualizável é removível.</span><span class="sxs-lookup"><span data-stu-id="01e1a-305">For example, an upgradeable processor chip is removable.</span></span>

<span data-ttu-id="01e1a-306">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-306">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-307">**Peças**</span><span class="sxs-lookup"><span data-stu-id="01e1a-307">**Replaceable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-308">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="01e1a-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-309">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-310">Se for **true**, é possível substituir o elemento por um fisicamente diferente.</span><span class="sxs-lookup"><span data-stu-id="01e1a-310">If **TRUE**, it is possible to replace the element with a physically different one.</span></span> <span data-ttu-id="01e1a-311">Por exemplo, alguns sistemas de computador permitem que o chip do processador principal seja atualizado para uma classificação de clock mais alta.</span><span class="sxs-lookup"><span data-stu-id="01e1a-311">For example, some computer systems allow the main processor chip to be upgraded to one of a higher clock rating.</span></span> <span data-ttu-id="01e1a-312">Nesse caso, diz-se que o processador é substituível.</span><span class="sxs-lookup"><span data-stu-id="01e1a-312">In this case, the processor is said to be replaceable.</span></span> <span data-ttu-id="01e1a-313">Todos os componentes removíveis são inerentemente substituíveis.</span><span class="sxs-lookup"><span data-stu-id="01e1a-313">All removable components are inherently replaceable.</span></span>

<span data-ttu-id="01e1a-314">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-314">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-315">**SecurityBreach**</span><span class="sxs-lookup"><span data-stu-id="01e1a-315">**SecurityBreach**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-316">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01e1a-316">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-318">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Tabela global de contêiner físico DMTF \| 2,12 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span><span class="sxs-lookup"><span data-stu-id="01e1a-318">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Physical Container Global Table\|002.12"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**BreachDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-319">Indica se uma violação física do quadro foi tentada, mas malsucedida, ou se foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="01e1a-319">Indicates whether a physical breach of the frame was attempted but unsuccessful, or attempted and successful.</span></span>

<span data-ttu-id="01e1a-320">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-320">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="01e1a-321">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="01e1a-321">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01e1a-322">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="01e1a-322">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

<span data-ttu-id="01e1a-323">**Sem violação** (3)</span><span class="sxs-lookup"><span data-stu-id="01e1a-323">**No Breach** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

<span data-ttu-id="01e1a-324">**Tentativa de violação** (4)</span><span class="sxs-lookup"><span data-stu-id="01e1a-324">**Breach Attempted** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

<span data-ttu-id="01e1a-325">**Violação bem-sucedida** (5)</span><span class="sxs-lookup"><span data-stu-id="01e1a-325">**Breach Successful** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01e1a-326">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="01e1a-326">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-327">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-327">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-328">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-328">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-329">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="01e1a-329">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-330">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="01e1a-330">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="01e1a-331">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-331">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-332">**ServiceDescriptions**</span><span class="sxs-lookup"><span data-stu-id="01e1a-332">**ServiceDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-333">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-333">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-335">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ CIM PhysicalFrame**](cim-physicalframe.md).**Infilosofia**")</span><span class="sxs-lookup"><span data-stu-id="01e1a-335">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServicePhilosophy**")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-336">Cadeias de caracteres de forma livre que fornecem explicações detalhadas para entradas na matriz de **unifilosofia** .</span><span class="sxs-lookup"><span data-stu-id="01e1a-336">Free-form strings that provide detailed explanations for entries in the **ServicePhilosophy** array.</span></span>

> [!Note]  
> <span data-ttu-id="01e1a-337">Cada entrada dessa matriz está relacionada à entrada na matriz de **unifilosofia** que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="01e1a-337">Each entry of this array is related to the entry in **ServicePhilosophy** array that is located at the same index.</span></span>

 

<span data-ttu-id="01e1a-338">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-338">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-339">**Infilosofia**</span><span class="sxs-lookup"><span data-stu-id="01e1a-339">**ServicePhilosophy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-340">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="01e1a-340">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-341">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-341">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-342">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ CIM PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="01e1a-342">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_PhysicalFrame**](cim-physicalframe.md).**ServiceDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-343">Indica se o quadro é atendido de cima, para frente, para trás ou para o lado; e se ele tem bandejas deslizantes ou lados removíveis e se o quadro é móvel (por exemplo, com cilindros).</span><span class="sxs-lookup"><span data-stu-id="01e1a-343">Indicates whether the frame is serviced from the top, front, back, or side; and whether it has sliding trays or removable sides, and whether the frame is moveable (for example, having rollers).</span></span>

<span data-ttu-id="01e1a-344">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-344">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01e1a-345">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="01e1a-345">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="01e1a-346">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="01e1a-346">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

<span data-ttu-id="01e1a-347">**Serviço da parte superior** (2)</span><span class="sxs-lookup"><span data-stu-id="01e1a-347">**Service From Top** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

<span data-ttu-id="01e1a-348">**Serviço da frente** (3)</span><span class="sxs-lookup"><span data-stu-id="01e1a-348">**Service From Front** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

<span data-ttu-id="01e1a-349">**Serviço de volta** (4)</span><span class="sxs-lookup"><span data-stu-id="01e1a-349">**Service From Back** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

<span data-ttu-id="01e1a-350">**Serviço do lado** (5)</span><span class="sxs-lookup"><span data-stu-id="01e1a-350">**Service From Side** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

<span data-ttu-id="01e1a-351">**Bandejas deslizantes** (6)</span><span class="sxs-lookup"><span data-stu-id="01e1a-351">**Sliding Trays** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

<span data-ttu-id="01e1a-352">**Lados removíveis** (7)</span><span class="sxs-lookup"><span data-stu-id="01e1a-352">**Removable Sides** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

<span data-ttu-id="01e1a-353">**Móvel** (8)</span><span class="sxs-lookup"><span data-stu-id="01e1a-353">**Moveable** (8)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01e1a-354">**SKU**</span><span class="sxs-lookup"><span data-stu-id="01e1a-354">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-355">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-357">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="01e1a-357">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-358">Número de unidade de manutenção de estoque para este elemento físico.</span><span class="sxs-lookup"><span data-stu-id="01e1a-358">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="01e1a-359">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-359">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-360">**Status**</span><span class="sxs-lookup"><span data-stu-id="01e1a-360">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-361">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-362">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-362">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-363">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="01e1a-363">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-364">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="01e1a-364">String that indicates the current status of the object.</span></span> <span data-ttu-id="01e1a-365">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="01e1a-365">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="01e1a-366">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="01e1a-366">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="01e1a-367">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="01e1a-367">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="01e1a-368">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="01e1a-368">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="01e1a-369">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="01e1a-369">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="01e1a-370">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="01e1a-370">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="01e1a-371">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-371">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="01e1a-372">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="01e1a-372">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="01e1a-373">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="01e1a-373">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="01e1a-374">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="01e1a-374">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="01e1a-375">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="01e1a-375">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="01e1a-376">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="01e1a-376">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="01e1a-377">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="01e1a-377">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="01e1a-378">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="01e1a-378">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="01e1a-379">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="01e1a-379">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="01e1a-380">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="01e1a-380">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="01e1a-381">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="01e1a-381">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="01e1a-382">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="01e1a-382">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="01e1a-383">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="01e1a-383">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="01e1a-384">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="01e1a-384">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="01e1a-385">**Tag**</span><span class="sxs-lookup"><span data-stu-id="01e1a-385">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-386">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-386">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-387">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-387">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-388">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="01e1a-388">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-389">Identifica exclusivamente o elemento físico e serve como a chave do elemento.</span><span class="sxs-lookup"><span data-stu-id="01e1a-389">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="01e1a-390">Essa propriedade pode conter informações, como a marca de ativo ou os dados de número de série.</span><span class="sxs-lookup"><span data-stu-id="01e1a-390">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="01e1a-391">A chave para [**o \_ físico do CIM**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar de forma independente o hardware ou a entidade, independentemente do posicionamento físico nos gabinetes, adaptadores e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="01e1a-391">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="01e1a-392">Por exemplo, um componente removível que pode ser intercambiável pode ser extraído de seu pacote recipiente (escopo) e estar temporariamente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="01e1a-392">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="01e1a-393">O objeto ainda continua existindo e pode até ser inserido em um contêiner de escopo diferente.</span><span class="sxs-lookup"><span data-stu-id="01e1a-393">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="01e1a-394">A chave para um elemento físico é uma cadeia de caracteres arbitrária que é definida independentemente do posicionamento ou da hierarquia orientada por local.</span><span class="sxs-lookup"><span data-stu-id="01e1a-394">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="01e1a-395">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-395">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-396">**TypeDescriptions**</span><span class="sxs-lookup"><span data-stu-id="01e1a-396">**TypeDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-397">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-397">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-398">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-398">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-399">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ chassi CIM**.**ChassisTypes**")</span><span class="sxs-lookup"><span data-stu-id="01e1a-399">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Chassis**.**ChassisTypes**")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-400">Matriz de cadeias de caracteres de forma livre que fornece informações sobre as entradas da matriz **ChassisTypes** .</span><span class="sxs-lookup"><span data-stu-id="01e1a-400">Array of free-form strings that provides information about the **ChassisTypes** array entries.</span></span>

> [!Note]  
> <span data-ttu-id="01e1a-401">Cada entrada de matriz está relacionada à entrada na propriedade **ChassisTypes** , que está localizada no mesmo índice.</span><span class="sxs-lookup"><span data-stu-id="01e1a-401">Each array entry is related to the entry in the **ChassisTypes** property, which is located at the same index.</span></span>

 

</dd> <dt>

<span data-ttu-id="01e1a-402">**Versão**</span><span class="sxs-lookup"><span data-stu-id="01e1a-402">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-403">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="01e1a-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-404">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-404">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-405">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="01e1a-405">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-406">Indica a versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="01e1a-406">Indicates the version of the physical element.</span></span>

<span data-ttu-id="01e1a-407">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-407">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-408">**VisibleAlarm**</span><span class="sxs-lookup"><span data-stu-id="01e1a-408">**VisibleAlarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-409">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="01e1a-409">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-411">Se **for true**, o equipamento incluirá um alarme visível.</span><span class="sxs-lookup"><span data-stu-id="01e1a-411">If **TRUE**, the equipment includes a visible alarm.</span></span>

<span data-ttu-id="01e1a-412">Essa propriedade é herdada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-412">This property is inherited from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-413">**Weight**</span><span class="sxs-lookup"><span data-stu-id="01e1a-413">**Weight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-414">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="01e1a-414">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-415">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-415">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-416">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("libras")</span><span class="sxs-lookup"><span data-stu-id="01e1a-416">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("pounds")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-417">Peso do pacote físico, em libras.</span><span class="sxs-lookup"><span data-stu-id="01e1a-417">Weight of the physical package, in pounds.</span></span>

<span data-ttu-id="01e1a-418">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-418">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> <dt>

<span data-ttu-id="01e1a-419">**Largura**</span><span class="sxs-lookup"><span data-stu-id="01e1a-419">**Width**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01e1a-420">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="01e1a-420">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-421">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="01e1a-421">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01e1a-422">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="01e1a-422">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="01e1a-423">Largura do pacote físico, em polegadas.</span><span class="sxs-lookup"><span data-stu-id="01e1a-423">Width of the physical package, in inches.</span></span>

<span data-ttu-id="01e1a-424">Essa propriedade é herdada do [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-424">This property is inherited from [**CIM\_PhysicalPackage**](cim-physicalpackage.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01e1a-425">Comentários</span><span class="sxs-lookup"><span data-stu-id="01e1a-425">Remarks</span></span>

<span data-ttu-id="01e1a-426">A classe de **\_ chassi CIM** é derivada do [**CIM \_ PhysicalFrame**](cim-physicalframe.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-426">The **CIM\_Chassis** class is derived from [**CIM\_PhysicalFrame**](cim-physicalframe.md).</span></span>

<span data-ttu-id="01e1a-427">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="01e1a-427">WMI does not implement this class.</span></span> <span data-ttu-id="01e1a-428">Para obter mais informações sobre classes derivadas **do \_ chassi CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="01e1a-428">For more information about classes derived from **CIM\_Chassis**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="01e1a-429">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="01e1a-429">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="01e1a-430">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="01e1a-430">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="01e1a-431">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01e1a-431">Requirements</span></span>



| <span data-ttu-id="01e1a-432">Requisito</span><span class="sxs-lookup"><span data-stu-id="01e1a-432">Requirement</span></span> | <span data-ttu-id="01e1a-433">Valor</span><span class="sxs-lookup"><span data-stu-id="01e1a-433">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01e1a-434">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01e1a-434">Minimum supported client</span></span><br/> | <span data-ttu-id="01e1a-435">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01e1a-435">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01e1a-436">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="01e1a-436">Minimum supported server</span></span><br/> | <span data-ttu-id="01e1a-437">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01e1a-437">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01e1a-438">Namespace</span><span class="sxs-lookup"><span data-stu-id="01e1a-438">Namespace</span></span><br/>                | <span data-ttu-id="01e1a-439">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="01e1a-439">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01e1a-440">MOF</span><span class="sxs-lookup"><span data-stu-id="01e1a-440">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01e1a-441"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01e1a-441"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01e1a-442">DLL</span><span class="sxs-lookup"><span data-stu-id="01e1a-442">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01e1a-443"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01e1a-443"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01e1a-444">Confira também</span><span class="sxs-lookup"><span data-stu-id="01e1a-444">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01e1a-445">**\_PHYSICALFRAME CIM**</span><span class="sxs-lookup"><span data-stu-id="01e1a-445">**CIM\_PhysicalFrame**</span></span>](cim-physicalframe.md)
</dt> </dl>

 

