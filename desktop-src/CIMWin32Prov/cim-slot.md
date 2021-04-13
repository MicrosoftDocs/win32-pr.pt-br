---
description: A \_ classe de slot CIM representa conectores nos quais os pacotes são inseridos.
ms.assetid: bcb1bdb5-fb1a-47ed-9450-dca38edca0eb
ms.tgt_platform: multiple
title: Classe CIM_Slot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Slot
- CIM_Slot.Caption
- CIM_Slot.ConnectorPinout
- CIM_Slot.ConnectorType
- CIM_Slot.CreationClassName
- CIM_Slot.Description
- CIM_Slot.HeightAllowed
- CIM_Slot.InstallDate
- CIM_Slot.LengthAllowed
- CIM_Slot.Manufacturer
- CIM_Slot.MaxDataWidth
- CIM_Slot.Model
- CIM_Slot.Name
- CIM_Slot.Number
- CIM_Slot.OtherIdentifyingInfo
- CIM_Slot.PartNumber
- CIM_Slot.PoweredOn
- CIM_Slot.PurposeDescription
- CIM_Slot.SerialNumber
- CIM_Slot.SKU
- CIM_Slot.SpecialPurpose
- CIM_Slot.Status
- CIM_Slot.SupportsHotPlug
- CIM_Slot.Tag
- CIM_Slot.ThermalRating
- CIM_Slot.VccMixedVoltageSupport
- CIM_Slot.Version
- CIM_Slot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73a63c8cd200096aa132d8205691669d765e54f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457152"
---
# <a name="cim_slot-class"></a><span data-ttu-id="5165a-103">\_Classe de slot CIM</span><span class="sxs-lookup"><span data-stu-id="5165a-103">CIM\_Slot class</span></span>

<span data-ttu-id="5165a-104">A classe de **\_ slot CIM** representa conectores nos quais os pacotes são inseridos.</span><span class="sxs-lookup"><span data-stu-id="5165a-104">The **CIM\_Slot** class represents connectors into which packages are inserted.</span></span> <span data-ttu-id="5165a-105">Por exemplo, um pacote físico que é uma unidade de disco pode ser inserido em um slot SCA ou um cartão (uma subclasse de [CIM \_ PhysicalPackage](cim-physicalpackage.md)) pode ser inserido em um slot de expansão de 16, 32 ou 64 bits em uma placa de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="5165a-105">For example, a physical package that is a disk drive can be inserted into an SCA slot, or a card (a subclass of [CIM\_PhysicalPackage](cim-physicalpackage.md)) can be inserted into a 16-, 32-, or 64-bit expansion slot on a hosting board.</span></span> <span data-ttu-id="5165a-106">Os slots PCI ou PCMCIA tipo III são exemplos do último.</span><span class="sxs-lookup"><span data-stu-id="5165a-106">PCI or PCMCIA Type III Slots are examples of the latter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5165a-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="5165a-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5165a-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5165a-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5165a-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="5165a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5165a-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="5165a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5165a-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5165a-111">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B86-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Slot : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  real32   HeightAllowed;
  datetime InstallDate;
  real32   LengthAllowed;
  string   Manufacturer;
  uint16   MaxDataWidth;
  string   Model;
  string   Name;
  uint16   Number;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   PurposeDescription;
  string   SerialNumber;
  string   SKU;
  boolean  SpecialPurpose;
  string   Status;
  boolean  SupportsHotPlug;
  string   Tag;
  uint32   ThermalRating;
  uint16   VccMixedVoltageSupport[];
  string   Version;
  uint16   VppMixedVoltageSupport[];
};
```

## <a name="members"></a><span data-ttu-id="5165a-112">Membros</span><span class="sxs-lookup"><span data-stu-id="5165a-112">Members</span></span>

<span data-ttu-id="5165a-113">A classe de **\_ slot CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5165a-113">The **CIM\_Slot** class has these types of members:</span></span>

-   [<span data-ttu-id="5165a-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5165a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5165a-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5165a-115">Properties</span></span>

<span data-ttu-id="5165a-116">A classe de **\_ slot CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5165a-116">The **CIM\_Slot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5165a-117">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="5165a-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-120">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="5165a-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="5165a-121">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5165a-121">Short textual description of the object.</span></span>

<span data-ttu-id="5165a-122">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-123">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="5165a-123">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5165a-126">Cadeia de caracteres de forma livre que descreve a configuração de PIN e o uso de sinal de um conector físico.</span><span class="sxs-lookup"><span data-stu-id="5165a-126">Free-form string that describes the pin configuration and signal use of a physical connector.</span></span>

<span data-ttu-id="5165a-127">Essa propriedade é herdada do [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-127">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-128">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="5165a-128">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-129">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5165a-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5165a-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-131">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Slot do sistema DMTF \| 4,2 ")</span><span class="sxs-lookup"><span data-stu-id="5165a-131">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("ConnectorType"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.2")</span></span>
</dt> </dl>

<span data-ttu-id="5165a-132">Tipo de conector físico.</span><span class="sxs-lookup"><span data-stu-id="5165a-132">Type of physical connector.</span></span> <span data-ttu-id="5165a-133">Uma matriz é especificada para permitir a descrição de combinações de informações do conector.</span><span class="sxs-lookup"><span data-stu-id="5165a-133">An array is specified to allow the description of combinations of connector information.</span></span> <span data-ttu-id="5165a-134">Por exemplo, uma entrada de matriz poderia especificar RS-232, outro DB-25 e um terceiro poderia definir o conector como "masculino".</span><span class="sxs-lookup"><span data-stu-id="5165a-134">For example, one array entry could specify RS-232, another DB-25, and a third could define the connector as "Male".</span></span>

<span data-ttu-id="5165a-135">Essa propriedade é herdada do [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-135">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<dt>

<span data-ttu-id="5165a-136">0</span><span class="sxs-lookup"><span data-stu-id="5165a-136">0</span></span>
</dt> <dd>

<span data-ttu-id="5165a-137">Unknown</span><span class="sxs-lookup"><span data-stu-id="5165a-137">Unknown</span></span>

</dd> <dt>

<span data-ttu-id="5165a-138">1</span><span class="sxs-lookup"><span data-stu-id="5165a-138">1</span></span>
</dt> <dd>

<span data-ttu-id="5165a-139">Outro</span><span class="sxs-lookup"><span data-stu-id="5165a-139">Other</span></span>

</dd> <dt>

<span data-ttu-id="5165a-140">2</span><span class="sxs-lookup"><span data-stu-id="5165a-140">2</span></span>
</dt> <dd>

<span data-ttu-id="5165a-141">Masculino</span><span class="sxs-lookup"><span data-stu-id="5165a-141">Male</span></span>

</dd> <dt>

<span data-ttu-id="5165a-142">3</span><span class="sxs-lookup"><span data-stu-id="5165a-142">3</span></span>
</dt> <dd>

<span data-ttu-id="5165a-143">Feminino</span><span class="sxs-lookup"><span data-stu-id="5165a-143">Female</span></span>

</dd> <dt>

<span data-ttu-id="5165a-144">4</span><span class="sxs-lookup"><span data-stu-id="5165a-144">4</span></span>
</dt> <dd>

<span data-ttu-id="5165a-145">Blindado</span><span class="sxs-lookup"><span data-stu-id="5165a-145">Shielded</span></span>

</dd> <dt>

<span data-ttu-id="5165a-146">5</span><span class="sxs-lookup"><span data-stu-id="5165a-146">5</span></span>
</dt> <dd>

<span data-ttu-id="5165a-147">Não blindada</span><span class="sxs-lookup"><span data-stu-id="5165a-147">Unshielded</span></span>

</dd> <dt>

<span data-ttu-id="5165a-148">6</span><span class="sxs-lookup"><span data-stu-id="5165a-148">6</span></span>
</dt> <dd>

<span data-ttu-id="5165a-149">SCSI (A) de alta densidade (50 Pins)</span><span class="sxs-lookup"><span data-stu-id="5165a-149">SCSI (A) High-density (50 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5165a-150">7</span><span class="sxs-lookup"><span data-stu-id="5165a-150">7</span></span>
</dt> <dd>

<span data-ttu-id="5165a-151">SCSI (A) de baixa densidade (50 Pins)</span><span class="sxs-lookup"><span data-stu-id="5165a-151">SCSI (A) Low-density (50 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5165a-152">8</span><span class="sxs-lookup"><span data-stu-id="5165a-152">8</span></span>
</dt> <dd>

<span data-ttu-id="5165a-153">SCSI (P) de alta densidade (68 pinos)</span><span class="sxs-lookup"><span data-stu-id="5165a-153">SCSI (P) High-density (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5165a-154">9</span><span class="sxs-lookup"><span data-stu-id="5165a-154">9</span></span>
</dt> <dd>

<span data-ttu-id="5165a-155">SCSI SCA-I (80 pinos)</span><span class="sxs-lookup"><span data-stu-id="5165a-155">SCSI SCA-I (80 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5165a-156">10</span><span class="sxs-lookup"><span data-stu-id="5165a-156">10</span></span>
</dt> <dd>

<span data-ttu-id="5165a-157">SCSI SCA-II (80 pinos)</span><span class="sxs-lookup"><span data-stu-id="5165a-157">SCSI SCA-II (80 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5165a-158">11</span><span class="sxs-lookup"><span data-stu-id="5165a-158">11</span></span>
</dt> <dd>

<span data-ttu-id="5165a-159">Fibre Channel SCSI (DB-9, cobre)</span><span class="sxs-lookup"><span data-stu-id="5165a-159">SCSI Fibre Channel (DB-9, Copper)</span></span>

</dd> <dt>

<span data-ttu-id="5165a-160">12</span><span class="sxs-lookup"><span data-stu-id="5165a-160">12</span></span>
</dt> <dd>

<span data-ttu-id="5165a-161">Fibre Channel SCSI (Fibre)</span><span class="sxs-lookup"><span data-stu-id="5165a-161">SCSI Fibre Channel (Fibre)</span></span>

</dd> <dt>

<span data-ttu-id="5165a-162">13</span><span class="sxs-lookup"><span data-stu-id="5165a-162">13</span></span>
</dt> <dd>

<span data-ttu-id="5165a-163">SCSI Fibre Channel SCA-II (40 pinos)</span><span class="sxs-lookup"><span data-stu-id="5165a-163">SCSI Fibre Channel SCA-II (40 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5165a-164">14</span><span class="sxs-lookup"><span data-stu-id="5165a-164">14</span></span>
</dt> <dd>

<span data-ttu-id="5165a-165">SCSI Fibre Channel SCA-II (20 pinos)</span><span class="sxs-lookup"><span data-stu-id="5165a-165">SCSI Fibre Channel SCA-II (20 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5165a-166">15</span><span class="sxs-lookup"><span data-stu-id="5165a-166">15</span></span>
</dt> <dd>

<span data-ttu-id="5165a-167">SCSI Fibre Channel BNC</span><span class="sxs-lookup"><span data-stu-id="5165a-167">SCSI Fibre Channel BNC</span></span>

</dd> <dt>

<span data-ttu-id="5165a-168">16</span><span class="sxs-lookup"><span data-stu-id="5165a-168">16</span></span>
</dt> <dd>

<span data-ttu-id="5165a-169">ATA 3-1/2 polegada (40 pinos)</span><span class="sxs-lookup"><span data-stu-id="5165a-169">ATA 3-1/2 Inch (40 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5165a-170">17</span><span class="sxs-lookup"><span data-stu-id="5165a-170">17</span></span>
</dt> <dd>

<span data-ttu-id="5165a-171">ATA 2-1/2 polegada (44 pinos)</span><span class="sxs-lookup"><span data-stu-id="5165a-171">ATA 2-1/2 Inch (44 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5165a-172">18</span><span class="sxs-lookup"><span data-stu-id="5165a-172">18</span></span>
</dt> <dd>

<span data-ttu-id="5165a-173">ATA-2</span><span class="sxs-lookup"><span data-stu-id="5165a-173">ATA-2</span></span>

</dd> <dt>

<span data-ttu-id="5165a-174">19</span><span class="sxs-lookup"><span data-stu-id="5165a-174">19</span></span>
</dt> <dd>

<span data-ttu-id="5165a-175">ATA-3</span><span class="sxs-lookup"><span data-stu-id="5165a-175">ATA-3</span></span>

</dd> <dt>

<span data-ttu-id="5165a-176">20</span><span class="sxs-lookup"><span data-stu-id="5165a-176">20</span></span>
</dt> <dd>

<span data-ttu-id="5165a-177">ATA/66</span><span class="sxs-lookup"><span data-stu-id="5165a-177">ATA/66</span></span>

</dd> <dt>

<span data-ttu-id="5165a-178">21</span><span class="sxs-lookup"><span data-stu-id="5165a-178">21</span></span>
</dt> <dd>

<span data-ttu-id="5165a-179">DB-9</span><span class="sxs-lookup"><span data-stu-id="5165a-179">DB-9</span></span>

</dd> <dt>

<span data-ttu-id="5165a-180">22</span><span class="sxs-lookup"><span data-stu-id="5165a-180">22</span></span>
</dt> <dd>

<span data-ttu-id="5165a-181">DB-15</span><span class="sxs-lookup"><span data-stu-id="5165a-181">DB-15</span></span>

</dd> <dt>

<span data-ttu-id="5165a-182">23</span><span class="sxs-lookup"><span data-stu-id="5165a-182">23</span></span>
</dt> <dd>

<span data-ttu-id="5165a-183">DB-25</span><span class="sxs-lookup"><span data-stu-id="5165a-183">DB-25</span></span>

</dd> <dt>

<span data-ttu-id="5165a-184">24</span><span class="sxs-lookup"><span data-stu-id="5165a-184">24</span></span>
</dt> <dd>

<span data-ttu-id="5165a-185">DB-36</span><span class="sxs-lookup"><span data-stu-id="5165a-185">DB-36</span></span>

</dd> <dt>

<span data-ttu-id="5165a-186">25</span><span class="sxs-lookup"><span data-stu-id="5165a-186">25</span></span>
</dt> <dd>

<span data-ttu-id="5165a-187">RS-232C</span><span class="sxs-lookup"><span data-stu-id="5165a-187">RS-232C</span></span>

</dd> <dt>

<span data-ttu-id="5165a-188">26</span><span class="sxs-lookup"><span data-stu-id="5165a-188">26</span></span>
</dt> <dd>

<span data-ttu-id="5165a-189">RS-422</span><span class="sxs-lookup"><span data-stu-id="5165a-189">RS-422</span></span>

</dd> <dt>

<span data-ttu-id="5165a-190">27</span><span class="sxs-lookup"><span data-stu-id="5165a-190">27</span></span>
</dt> <dd>

<span data-ttu-id="5165a-191">RS-423</span><span class="sxs-lookup"><span data-stu-id="5165a-191">RS-423</span></span>

</dd> <dt>

<span data-ttu-id="5165a-192">28</span><span class="sxs-lookup"><span data-stu-id="5165a-192">28</span></span>
</dt> <dd>

<span data-ttu-id="5165a-193">RS-485</span><span class="sxs-lookup"><span data-stu-id="5165a-193">RS-485</span></span>

</dd> <dt>

<span data-ttu-id="5165a-194">29</span><span class="sxs-lookup"><span data-stu-id="5165a-194">29</span></span>
</dt> <dd>

<span data-ttu-id="5165a-195">RS-449</span><span class="sxs-lookup"><span data-stu-id="5165a-195">RS-449</span></span>

</dd> <dt>

<span data-ttu-id="5165a-196">30</span><span class="sxs-lookup"><span data-stu-id="5165a-196">30</span></span>
</dt> <dd>

<span data-ttu-id="5165a-197">V. 35</span><span class="sxs-lookup"><span data-stu-id="5165a-197">V.35</span></span>

</dd> <dt>

<span data-ttu-id="5165a-198">31</span><span class="sxs-lookup"><span data-stu-id="5165a-198">31</span></span>
</dt> <dd>

<span data-ttu-id="5165a-199">X. 21</span><span class="sxs-lookup"><span data-stu-id="5165a-199">X.21</span></span>

</dd> <dt>

<span data-ttu-id="5165a-200">32</span><span class="sxs-lookup"><span data-stu-id="5165a-200">32</span></span>
</dt> <dd>

<span data-ttu-id="5165a-201">IEEE-488</span><span class="sxs-lookup"><span data-stu-id="5165a-201">IEEE-488</span></span>

</dd> <dt>

<span data-ttu-id="5165a-202">33</span><span class="sxs-lookup"><span data-stu-id="5165a-202">33</span></span>
</dt> <dd>

<span data-ttu-id="5165a-203">AUI</span><span class="sxs-lookup"><span data-stu-id="5165a-203">AUI</span></span>

</dd> <dt>

<span data-ttu-id="5165a-204">34</span><span class="sxs-lookup"><span data-stu-id="5165a-204">34</span></span>
</dt> <dd>

<span data-ttu-id="5165a-205">UTP categoria 3</span><span class="sxs-lookup"><span data-stu-id="5165a-205">UTP Category 3</span></span>

</dd> <dt>

<span data-ttu-id="5165a-206">35</span><span class="sxs-lookup"><span data-stu-id="5165a-206">35</span></span>
</dt> <dd>

<span data-ttu-id="5165a-207">UTP categoria 4</span><span class="sxs-lookup"><span data-stu-id="5165a-207">UTP Category 4</span></span>

</dd> <dt>

<span data-ttu-id="5165a-208">36</span><span class="sxs-lookup"><span data-stu-id="5165a-208">36</span></span>
</dt> <dd>

<span data-ttu-id="5165a-209">UTP categoria 5</span><span class="sxs-lookup"><span data-stu-id="5165a-209">UTP Category 5</span></span>

</dd> <dt>

<span data-ttu-id="5165a-210">37</span><span class="sxs-lookup"><span data-stu-id="5165a-210">37</span></span>
</dt> <dd>

<span data-ttu-id="5165a-211">BNC</span><span class="sxs-lookup"><span data-stu-id="5165a-211">BNC</span></span>

</dd> <dt>

<span data-ttu-id="5165a-212">38</span><span class="sxs-lookup"><span data-stu-id="5165a-212">38</span></span>
</dt> <dd>

<span data-ttu-id="5165a-213">RJ11</span><span class="sxs-lookup"><span data-stu-id="5165a-213">RJ11</span></span>

</dd> <dt>

<span data-ttu-id="5165a-214">39</span><span class="sxs-lookup"><span data-stu-id="5165a-214">39</span></span>
</dt> <dd>

<span data-ttu-id="5165a-215">RJ45</span><span class="sxs-lookup"><span data-stu-id="5165a-215">RJ45</span></span>

</dd> <dt>

<span data-ttu-id="5165a-216">40</span><span class="sxs-lookup"><span data-stu-id="5165a-216">40</span></span>
</dt> <dd>

<span data-ttu-id="5165a-217">MIC de fibra</span><span class="sxs-lookup"><span data-stu-id="5165a-217">Fiber MIC</span></span>

</dd> <dt>

<span data-ttu-id="5165a-218">41</span><span class="sxs-lookup"><span data-stu-id="5165a-218">41</span></span>
</dt> <dd>

<span data-ttu-id="5165a-219">Apple AUI</span><span class="sxs-lookup"><span data-stu-id="5165a-219">Apple AUI</span></span>

</dd> <dt>

<span data-ttu-id="5165a-220">42</span><span class="sxs-lookup"><span data-stu-id="5165a-220">42</span></span>
</dt> <dd>

<span data-ttu-id="5165a-221">Apple GeoPort</span><span class="sxs-lookup"><span data-stu-id="5165a-221">Apple GeoPort</span></span>

</dd> <dt>

<span data-ttu-id="5165a-222">43</span><span class="sxs-lookup"><span data-stu-id="5165a-222">43</span></span>
</dt> <dd>

<span data-ttu-id="5165a-223">PCI</span><span class="sxs-lookup"><span data-stu-id="5165a-223">PCI</span></span>

</dd> <dt>

<span data-ttu-id="5165a-224">44</span><span class="sxs-lookup"><span data-stu-id="5165a-224">44</span></span>
</dt> <dd>

<span data-ttu-id="5165a-225">ISA</span><span class="sxs-lookup"><span data-stu-id="5165a-225">ISA</span></span>

</dd> <dt>

<span data-ttu-id="5165a-226">45</span><span class="sxs-lookup"><span data-stu-id="5165a-226">45</span></span>
</dt> <dd>

<span data-ttu-id="5165a-227">EISA</span><span class="sxs-lookup"><span data-stu-id="5165a-227">EISA</span></span>

</dd> <dt>

<span data-ttu-id="5165a-228">46</span><span class="sxs-lookup"><span data-stu-id="5165a-228">46</span></span>
</dt> <dd>

<span data-ttu-id="5165a-229">VESA</span><span class="sxs-lookup"><span data-stu-id="5165a-229">VESA</span></span>

</dd> <dt>

<span data-ttu-id="5165a-230">47</span><span class="sxs-lookup"><span data-stu-id="5165a-230">47</span></span>
</dt> <dd>

<span data-ttu-id="5165a-231">PLACA</span><span class="sxs-lookup"><span data-stu-id="5165a-231">PCMCIA</span></span>

</dd> <dt>

<span data-ttu-id="5165a-232">48</span><span class="sxs-lookup"><span data-stu-id="5165a-232">48</span></span>
</dt> <dd>

<span data-ttu-id="5165a-233">Tipo de PCMCIA I</span><span class="sxs-lookup"><span data-stu-id="5165a-233">PCMCIA Type I</span></span>

</dd> <dt>

<span data-ttu-id="5165a-234">49</span><span class="sxs-lookup"><span data-stu-id="5165a-234">49</span></span>
</dt> <dd>

<span data-ttu-id="5165a-235">Tipo de PCMCIA II</span><span class="sxs-lookup"><span data-stu-id="5165a-235">PCMCIA Type II</span></span>

</dd> <dt>

<span data-ttu-id="5165a-236">50</span><span class="sxs-lookup"><span data-stu-id="5165a-236">50</span></span>
</dt> <dd>

<span data-ttu-id="5165a-237">Tipo de PCMCIA III</span><span class="sxs-lookup"><span data-stu-id="5165a-237">PCMCIA Type III</span></span>

</dd> <dt>

<span data-ttu-id="5165a-238">51</span><span class="sxs-lookup"><span data-stu-id="5165a-238">51</span></span>
</dt> <dd>

<span data-ttu-id="5165a-239">Porta ZV</span><span class="sxs-lookup"><span data-stu-id="5165a-239">ZV Port</span></span>

</dd> <dt>

<span data-ttu-id="5165a-240">52</span><span class="sxs-lookup"><span data-stu-id="5165a-240">52</span></span>
</dt> <dd>

<span data-ttu-id="5165a-241">CardBus</span><span class="sxs-lookup"><span data-stu-id="5165a-241">CardBus</span></span>

</dd> <dt>

<span data-ttu-id="5165a-242">53</span><span class="sxs-lookup"><span data-stu-id="5165a-242">53</span></span>
</dt> <dd>

<span data-ttu-id="5165a-243">USB</span><span class="sxs-lookup"><span data-stu-id="5165a-243">USB</span></span>

</dd> <dt>

<span data-ttu-id="5165a-244">54</span><span class="sxs-lookup"><span data-stu-id="5165a-244">54</span></span>
</dt> <dd>

<span data-ttu-id="5165a-245">IEEE 1394</span><span class="sxs-lookup"><span data-stu-id="5165a-245">IEEE 1394</span></span>

</dd> <dt>

<span data-ttu-id="5165a-246">55</span><span class="sxs-lookup"><span data-stu-id="5165a-246">55</span></span>
</dt> <dd>

<span data-ttu-id="5165a-247">HIPPI</span><span class="sxs-lookup"><span data-stu-id="5165a-247">HIPPI</span></span>

</dd> <dt>

<span data-ttu-id="5165a-248">56</span><span class="sxs-lookup"><span data-stu-id="5165a-248">56</span></span>
</dt> <dd>

<span data-ttu-id="5165a-249">HSSDC (6 Pins)</span><span class="sxs-lookup"><span data-stu-id="5165a-249">HSSDC (6 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5165a-250">57</span><span class="sxs-lookup"><span data-stu-id="5165a-250">57</span></span>
</dt> <dd>

<span data-ttu-id="5165a-251">GBICS</span><span class="sxs-lookup"><span data-stu-id="5165a-251">GBIC</span></span>

</dd> <dt>

<span data-ttu-id="5165a-252">58</span><span class="sxs-lookup"><span data-stu-id="5165a-252">58</span></span>
</dt> <dd>

<span data-ttu-id="5165a-253">DIN</span><span class="sxs-lookup"><span data-stu-id="5165a-253">DIN</span></span>

</dd> <dt>

<span data-ttu-id="5165a-254">59</span><span class="sxs-lookup"><span data-stu-id="5165a-254">59</span></span>
</dt> <dd>

<span data-ttu-id="5165a-255">Mini-DIN</span><span class="sxs-lookup"><span data-stu-id="5165a-255">Mini-DIN</span></span>

</dd> <dt>

<span data-ttu-id="5165a-256">60</span><span class="sxs-lookup"><span data-stu-id="5165a-256">60</span></span>
</dt> <dd>

<span data-ttu-id="5165a-257">Micro-DIN</span><span class="sxs-lookup"><span data-stu-id="5165a-257">Micro-DIN</span></span>

</dd> <dt>

<span data-ttu-id="5165a-258">61</span><span class="sxs-lookup"><span data-stu-id="5165a-258">61</span></span>
</dt> <dd>

<span data-ttu-id="5165a-259">PS/2</span><span class="sxs-lookup"><span data-stu-id="5165a-259">PS/2</span></span>

</dd> <dt>

<span data-ttu-id="5165a-260">62</span><span class="sxs-lookup"><span data-stu-id="5165a-260">62</span></span>
</dt> <dd>

<span data-ttu-id="5165a-261">Infravermelho</span><span class="sxs-lookup"><span data-stu-id="5165a-261">Infrared</span></span>

</dd> <dt>

<span data-ttu-id="5165a-262">63</span><span class="sxs-lookup"><span data-stu-id="5165a-262">63</span></span>
</dt> <dd>

<span data-ttu-id="5165a-263">HP-HIL</span><span class="sxs-lookup"><span data-stu-id="5165a-263">HP-HIL</span></span>

</dd> <dt>

<span data-ttu-id="5165a-264">64</span><span class="sxs-lookup"><span data-stu-id="5165a-264">64</span></span>
</dt> <dd>

<span data-ttu-id="5165a-265">Access. Bus</span><span class="sxs-lookup"><span data-stu-id="5165a-265">Access.bus</span></span>

</dd> <dt>

<span data-ttu-id="5165a-266">65</span><span class="sxs-lookup"><span data-stu-id="5165a-266">65</span></span>
</dt> <dd>

<span data-ttu-id="5165a-267">NuBus</span><span class="sxs-lookup"><span data-stu-id="5165a-267">NuBus</span></span>

</dd> <dt>

<span data-ttu-id="5165a-268">66</span><span class="sxs-lookup"><span data-stu-id="5165a-268">66</span></span>
</dt> <dd>

<span data-ttu-id="5165a-269">Centronics</span><span class="sxs-lookup"><span data-stu-id="5165a-269">Centronics</span></span>

</dd> <dt>

<span data-ttu-id="5165a-270">67</span><span class="sxs-lookup"><span data-stu-id="5165a-270">67</span></span>
</dt> <dd>

<span data-ttu-id="5165a-271">Mini-Centronics</span><span class="sxs-lookup"><span data-stu-id="5165a-271">Mini-Centronics</span></span>

</dd> <dt>

<span data-ttu-id="5165a-272">68</span><span class="sxs-lookup"><span data-stu-id="5165a-272">68</span></span>
</dt> <dd>

<span data-ttu-id="5165a-273">Tipo de Mini-Centronics-14</span><span class="sxs-lookup"><span data-stu-id="5165a-273">Mini-Centronics Type-14</span></span>

</dd> <dt>

<span data-ttu-id="5165a-274">69</span><span class="sxs-lookup"><span data-stu-id="5165a-274">69</span></span>
</dt> <dd>

<span data-ttu-id="5165a-275">Tipo de Mini-Centronics-20</span><span class="sxs-lookup"><span data-stu-id="5165a-275">Mini-Centronics Type-20</span></span>

</dd> <dt>

<span data-ttu-id="5165a-276">70</span><span class="sxs-lookup"><span data-stu-id="5165a-276">70</span></span>
</dt> <dd>

<span data-ttu-id="5165a-277">Tipo de Mini-Centronics-26</span><span class="sxs-lookup"><span data-stu-id="5165a-277">Mini-Centronics Type-26</span></span>

</dd> <dt>

<span data-ttu-id="5165a-278">71</span><span class="sxs-lookup"><span data-stu-id="5165a-278">71</span></span>
</dt> <dd>

<span data-ttu-id="5165a-279">Mouse de barramento</span><span class="sxs-lookup"><span data-stu-id="5165a-279">Bus Mouse</span></span>

</dd> <dt>

<span data-ttu-id="5165a-280">72</span><span class="sxs-lookup"><span data-stu-id="5165a-280">72</span></span>
</dt> <dd>

<span data-ttu-id="5165a-281">ADB</span><span class="sxs-lookup"><span data-stu-id="5165a-281">ADB</span></span>

</dd> <dt>

<span data-ttu-id="5165a-282">73</span><span class="sxs-lookup"><span data-stu-id="5165a-282">73</span></span>
</dt> <dd>

<span data-ttu-id="5165a-283">PLACA</span><span class="sxs-lookup"><span data-stu-id="5165a-283">AGP</span></span>

</dd> <dt>

<span data-ttu-id="5165a-284">74</span><span class="sxs-lookup"><span data-stu-id="5165a-284">74</span></span>
</dt> <dd>

<span data-ttu-id="5165a-285">Barramento de VM</span><span class="sxs-lookup"><span data-stu-id="5165a-285">VME Bus</span></span>

</dd> <dt>

<span data-ttu-id="5165a-286">75</span><span class="sxs-lookup"><span data-stu-id="5165a-286">75</span></span>
</dt> <dd>

<span data-ttu-id="5165a-287">VME64</span><span class="sxs-lookup"><span data-stu-id="5165a-287">VME64</span></span>

</dd> <dt>

<span data-ttu-id="5165a-288">76</span><span class="sxs-lookup"><span data-stu-id="5165a-288">76</span></span>
</dt> <dd>

<span data-ttu-id="5165a-289">Proprietário</span><span class="sxs-lookup"><span data-stu-id="5165a-289">Proprietary</span></span>

</dd> <dt>

<span data-ttu-id="5165a-290">77</span><span class="sxs-lookup"><span data-stu-id="5165a-290">77</span></span>
</dt> <dd>

<span data-ttu-id="5165a-291">Slot do cartão de processador proprietário</span><span class="sxs-lookup"><span data-stu-id="5165a-291">Proprietary Processor Card Slot</span></span>

</dd> <dt>

<span data-ttu-id="5165a-292">78</span><span class="sxs-lookup"><span data-stu-id="5165a-292">78</span></span>
</dt> <dd>

<span data-ttu-id="5165a-293">Slot de cartão de memória proprietário</span><span class="sxs-lookup"><span data-stu-id="5165a-293">Proprietary Memory Card Slot</span></span>

</dd> <dt>

<span data-ttu-id="5165a-294">79</span><span class="sxs-lookup"><span data-stu-id="5165a-294">79</span></span>
</dt> <dd>

<span data-ttu-id="5165a-295">Slot de riser de e/s proprietário</span><span class="sxs-lookup"><span data-stu-id="5165a-295">Proprietary I/O Riser Slot</span></span>

</dd> <dt>

<span data-ttu-id="5165a-296">80</span><span class="sxs-lookup"><span data-stu-id="5165a-296">80</span></span>
</dt> <dd>

<span data-ttu-id="5165a-297">PCI-66MHZ</span><span class="sxs-lookup"><span data-stu-id="5165a-297">PCI-66MHZ</span></span>

</dd> <dt>

<span data-ttu-id="5165a-298">81</span><span class="sxs-lookup"><span data-stu-id="5165a-298">81</span></span>
</dt> <dd>

<span data-ttu-id="5165a-299">AGP2X</span><span class="sxs-lookup"><span data-stu-id="5165a-299">AGP2X</span></span>

</dd> <dt>

<span data-ttu-id="5165a-300">82</span><span class="sxs-lookup"><span data-stu-id="5165a-300">82</span></span>
</dt> <dd>

<span data-ttu-id="5165a-301">AGP4X</span><span class="sxs-lookup"><span data-stu-id="5165a-301">AGP4X</span></span>

</dd> <dt>

<span data-ttu-id="5165a-302">83</span><span class="sxs-lookup"><span data-stu-id="5165a-302">83</span></span>
</dt> <dd>

<span data-ttu-id="5165a-303">PC-98</span><span class="sxs-lookup"><span data-stu-id="5165a-303">PC-98</span></span>

</dd> <dt>

<span data-ttu-id="5165a-304">84</span><span class="sxs-lookup"><span data-stu-id="5165a-304">84</span></span>
</dt> <dd>

<span data-ttu-id="5165a-305">PC-98-Hireso</span><span class="sxs-lookup"><span data-stu-id="5165a-305">PC-98-Hireso</span></span>

</dd> <dt>

<span data-ttu-id="5165a-306">85</span><span class="sxs-lookup"><span data-stu-id="5165a-306">85</span></span>
</dt> <dd>

<span data-ttu-id="5165a-307">PC-H98</span><span class="sxs-lookup"><span data-stu-id="5165a-307">PC-H98</span></span>

</dd> <dt>

<span data-ttu-id="5165a-308">86</span><span class="sxs-lookup"><span data-stu-id="5165a-308">86</span></span>
</dt> <dd>

<span data-ttu-id="5165a-309">PC-98Note</span><span class="sxs-lookup"><span data-stu-id="5165a-309">PC-98Note</span></span>

</dd> <dt>

<span data-ttu-id="5165a-310">87</span><span class="sxs-lookup"><span data-stu-id="5165a-310">87</span></span>
</dt> <dd>

<span data-ttu-id="5165a-311">PC-98Full</span><span class="sxs-lookup"><span data-stu-id="5165a-311">PC-98Full</span></span>

</dd> <dt>

<span data-ttu-id="5165a-312">88</span><span class="sxs-lookup"><span data-stu-id="5165a-312">88</span></span>
</dt> <dd>

<span data-ttu-id="5165a-313">ADAPTADOR SSA SCSI</span><span class="sxs-lookup"><span data-stu-id="5165a-313">SSA SCSI</span></span>

</dd> <dt>

<span data-ttu-id="5165a-314">89</span><span class="sxs-lookup"><span data-stu-id="5165a-314">89</span></span>
</dt> <dd>

<span data-ttu-id="5165a-315">Circular</span><span class="sxs-lookup"><span data-stu-id="5165a-315">Circular</span></span>

</dd> <dt>

<span data-ttu-id="5165a-316">90</span><span class="sxs-lookup"><span data-stu-id="5165a-316">90</span></span>
</dt> <dd>

<span data-ttu-id="5165a-317">Conector IDE integrado</span><span class="sxs-lookup"><span data-stu-id="5165a-317">On Board IDE Connector</span></span>

</dd> <dt>

<span data-ttu-id="5165a-318">91</span><span class="sxs-lookup"><span data-stu-id="5165a-318">91</span></span>
</dt> <dd>

<span data-ttu-id="5165a-319">Conector de disquete de placa</span><span class="sxs-lookup"><span data-stu-id="5165a-319">On Board Floppy Connector</span></span>

</dd> <dt>

<span data-ttu-id="5165a-320">92</span><span class="sxs-lookup"><span data-stu-id="5165a-320">92</span></span>
</dt> <dd>

<span data-ttu-id="5165a-321">9 pinos em linha dupla</span><span class="sxs-lookup"><span data-stu-id="5165a-321">9 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="5165a-322">93</span><span class="sxs-lookup"><span data-stu-id="5165a-322">93</span></span>
</dt> <dd>

<span data-ttu-id="5165a-323">25 pinos em linha dupla</span><span class="sxs-lookup"><span data-stu-id="5165a-323">25 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="5165a-324">94</span><span class="sxs-lookup"><span data-stu-id="5165a-324">94</span></span>
</dt> <dd>

<span data-ttu-id="5165a-325">50 pino duplo embutido</span><span class="sxs-lookup"><span data-stu-id="5165a-325">50 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="5165a-326">95</span><span class="sxs-lookup"><span data-stu-id="5165a-326">95</span></span>
</dt> <dd>

<span data-ttu-id="5165a-327">68 pino duplo embutido</span><span class="sxs-lookup"><span data-stu-id="5165a-327">68 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="5165a-328">96</span><span class="sxs-lookup"><span data-stu-id="5165a-328">96</span></span>
</dt> <dd>

<span data-ttu-id="5165a-329">Conector de som do quadro</span><span class="sxs-lookup"><span data-stu-id="5165a-329">On Board Sound Connector</span></span>

</dd> <dt>

<span data-ttu-id="5165a-330">97</span><span class="sxs-lookup"><span data-stu-id="5165a-330">97</span></span>
</dt> <dd>

<span data-ttu-id="5165a-331">Mini-tomada</span><span class="sxs-lookup"><span data-stu-id="5165a-331">Mini-jack</span></span>

</dd> <dt>

<span data-ttu-id="5165a-332">98</span><span class="sxs-lookup"><span data-stu-id="5165a-332">98</span></span>
</dt> <dd>

<span data-ttu-id="5165a-333">PCI-X</span><span class="sxs-lookup"><span data-stu-id="5165a-333">PCI-X</span></span>

</dd> <dt>

<span data-ttu-id="5165a-334">99</span><span class="sxs-lookup"><span data-stu-id="5165a-334">99</span></span>
</dt> <dd>

<span data-ttu-id="5165a-335">Sbus IEEE 1396-1993 32 bit</span><span class="sxs-lookup"><span data-stu-id="5165a-335">Sbus IEEE 1396-1993 32 bit</span></span>

</dd> <dt>

<span data-ttu-id="5165a-336">100</span><span class="sxs-lookup"><span data-stu-id="5165a-336">100</span></span>
</dt> <dd>

<span data-ttu-id="5165a-337">Sbus IEEE 1396-1993 64 bit</span><span class="sxs-lookup"><span data-stu-id="5165a-337">Sbus IEEE 1396-1993 64 bit</span></span>

</dd> <dt>

<span data-ttu-id="5165a-338">101</span><span class="sxs-lookup"><span data-stu-id="5165a-338">101</span></span>
</dt> <dd>

<span data-ttu-id="5165a-339">MCA</span><span class="sxs-lookup"><span data-stu-id="5165a-339">MCA</span></span>

</dd> <dt>

<span data-ttu-id="5165a-340">102</span><span class="sxs-lookup"><span data-stu-id="5165a-340">102</span></span>
</dt> <dd>

<span data-ttu-id="5165a-341">GIO</span><span class="sxs-lookup"><span data-stu-id="5165a-341">GIO</span></span>

</dd> <dt>

<span data-ttu-id="5165a-342">103</span><span class="sxs-lookup"><span data-stu-id="5165a-342">103</span></span>
</dt> <dd>

<span data-ttu-id="5165a-343">XIO</span><span class="sxs-lookup"><span data-stu-id="5165a-343">XIO</span></span>

</dd> <dt>

<span data-ttu-id="5165a-344">104</span><span class="sxs-lookup"><span data-stu-id="5165a-344">104</span></span>
</dt> <dd>

<span data-ttu-id="5165a-345">HIO</span><span class="sxs-lookup"><span data-stu-id="5165a-345">HIO</span></span>

</dd> <dt>

<span data-ttu-id="5165a-346">105</span><span class="sxs-lookup"><span data-stu-id="5165a-346">105</span></span>
</dt> <dd>

<span data-ttu-id="5165a-347">NGIO</span><span class="sxs-lookup"><span data-stu-id="5165a-347">NGIO</span></span>

</dd> <dt>

<span data-ttu-id="5165a-348">106</span><span class="sxs-lookup"><span data-stu-id="5165a-348">106</span></span>
</dt> <dd>

<span data-ttu-id="5165a-349">PMC</span><span class="sxs-lookup"><span data-stu-id="5165a-349">PMC</span></span>

</dd> <dt>

<span data-ttu-id="5165a-350">107</span><span class="sxs-lookup"><span data-stu-id="5165a-350">107</span></span>
</dt> <dd>

<span data-ttu-id="5165a-351">MTRJ</span><span class="sxs-lookup"><span data-stu-id="5165a-351">MTRJ</span></span>

</dd> <dt>

<span data-ttu-id="5165a-352">108</span><span class="sxs-lookup"><span data-stu-id="5165a-352">108</span></span>
</dt> <dd>

<span data-ttu-id="5165a-353">VF-45</span><span class="sxs-lookup"><span data-stu-id="5165a-353">VF-45</span></span>

</dd> <dt>

<span data-ttu-id="5165a-354">109</span><span class="sxs-lookup"><span data-stu-id="5165a-354">109</span></span>
</dt> <dd>

<span data-ttu-id="5165a-355">E/s futura</span><span class="sxs-lookup"><span data-stu-id="5165a-355">Future I/O</span></span>

</dd> <dt>

<span data-ttu-id="5165a-356">110</span><span class="sxs-lookup"><span data-stu-id="5165a-356">110</span></span>
</dt> <dd>

<span data-ttu-id="5165a-357">SC</span><span class="sxs-lookup"><span data-stu-id="5165a-357">SC</span></span>

</dd> <dt>

<span data-ttu-id="5165a-358">111</span><span class="sxs-lookup"><span data-stu-id="5165a-358">111</span></span>
</dt> <dd>

<span data-ttu-id="5165a-359">SG</span><span class="sxs-lookup"><span data-stu-id="5165a-359">SG</span></span>

</dd> <dt>

<span data-ttu-id="5165a-360">112</span><span class="sxs-lookup"><span data-stu-id="5165a-360">112</span></span>
</dt> <dd>

<span data-ttu-id="5165a-361">Elétrica</span><span class="sxs-lookup"><span data-stu-id="5165a-361">Electrical</span></span>

</dd> <dt>

<span data-ttu-id="5165a-362">113</span><span class="sxs-lookup"><span data-stu-id="5165a-362">113</span></span>
</dt> <dd>

<span data-ttu-id="5165a-363">Unidades</span><span class="sxs-lookup"><span data-stu-id="5165a-363">Optical</span></span>

</dd> <dt>

<span data-ttu-id="5165a-364">114</span><span class="sxs-lookup"><span data-stu-id="5165a-364">114</span></span>
</dt> <dd>

<span data-ttu-id="5165a-365">Faixa de opções</span><span class="sxs-lookup"><span data-stu-id="5165a-365">Ribbon</span></span>

</dd> <dt>

<span data-ttu-id="5165a-366">115</span><span class="sxs-lookup"><span data-stu-id="5165a-366">115</span></span>
</dt> <dd>

<span data-ttu-id="5165a-367">GLM</span><span class="sxs-lookup"><span data-stu-id="5165a-367">GLM</span></span>

</dd> <dt>

<span data-ttu-id="5165a-368">116</span><span class="sxs-lookup"><span data-stu-id="5165a-368">116</span></span>
</dt> <dd>

<span data-ttu-id="5165a-369">1x9</span><span class="sxs-lookup"><span data-stu-id="5165a-369">1x9</span></span>

</dd> <dt>

<span data-ttu-id="5165a-370">117</span><span class="sxs-lookup"><span data-stu-id="5165a-370">117</span></span>
</dt> <dd>

<span data-ttu-id="5165a-371">Mini SG</span><span class="sxs-lookup"><span data-stu-id="5165a-371">Mini SG</span></span>

</dd> <dt>

<span data-ttu-id="5165a-372">118</span><span class="sxs-lookup"><span data-stu-id="5165a-372">118</span></span>
</dt> <dd>

<span data-ttu-id="5165a-373">LC</span><span class="sxs-lookup"><span data-stu-id="5165a-373">LC</span></span>

</dd> <dt>

<span data-ttu-id="5165a-374">119</span><span class="sxs-lookup"><span data-stu-id="5165a-374">119</span></span>
</dt> <dd>

<span data-ttu-id="5165a-375">HSSC</span><span class="sxs-lookup"><span data-stu-id="5165a-375">HSSC</span></span>

</dd> <dt>

<span data-ttu-id="5165a-376">120</span><span class="sxs-lookup"><span data-stu-id="5165a-376">120</span></span>
</dt> <dd>

<span data-ttu-id="5165a-377">VHDCI blindado (68 pinos)</span><span class="sxs-lookup"><span data-stu-id="5165a-377">VHDCI Shielded (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="5165a-378">121</span><span class="sxs-lookup"><span data-stu-id="5165a-378">121</span></span>
</dt> <dd>

<span data-ttu-id="5165a-379">InfiniBand</span><span class="sxs-lookup"><span data-stu-id="5165a-379">InfiniBand</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5165a-380">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5165a-380">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-381">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-383">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5165a-383">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5165a-384">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="5165a-384">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="5165a-385">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="5165a-385">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="5165a-386">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-386">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-387">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5165a-387">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-388">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-388">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-389">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-389">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-390">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="5165a-390">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="5165a-391">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5165a-391">Textual description of the object.</span></span>

<span data-ttu-id="5165a-392">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-392">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-393">**HeightAllowed**</span><span class="sxs-lookup"><span data-stu-id="5165a-393">**HeightAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-394">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="5165a-394">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-395">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-395">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-396">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="5165a-396">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5165a-397">Altura máxima, em polegadas, de uma placa de adaptador que pode ser inserida no slot.</span><span class="sxs-lookup"><span data-stu-id="5165a-397">Maximum height, in inches, of an adapter card that can be inserted into the slot.</span></span>

</dd> <dt>

<span data-ttu-id="5165a-398">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5165a-398">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-399">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5165a-399">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-401">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="5165a-401">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="5165a-402">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="5165a-402">Date and time the object was installed.</span></span> <span data-ttu-id="5165a-403">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="5165a-403">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="5165a-404">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-404">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-405">**LengthAllowed**</span><span class="sxs-lookup"><span data-stu-id="5165a-405">**LengthAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-406">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="5165a-406">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-408">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="5165a-408">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="5165a-409">Comprimento máximo, em polegadas, de uma placa de adaptador que pode ser inserida no slot.</span><span class="sxs-lookup"><span data-stu-id="5165a-409">Maximum length, in inches, of an adapter card that can be inserted into the slot.</span></span>

</dd> <dt>

<span data-ttu-id="5165a-410">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="5165a-410">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-411">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-411">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-412">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-412">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-413">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5165a-413">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5165a-414">Organização que produziu o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5165a-414">Organization that produced the physical element.</span></span> <span data-ttu-id="5165a-415">Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-415">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="5165a-416">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-416">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-417">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="5165a-417">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-418">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5165a-418">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-419">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-420">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Slot do sistema DMTF \| 4,3 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="5165a-420">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.3"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="5165a-421">Largura máxima do barramento, em bits, de placas de adaptador que podem ser inseridas no slot.</span><span class="sxs-lookup"><span data-stu-id="5165a-421">Maximum bus width, in bits, of adapter cards that can be inserted into the slot.</span></span>

<dt>

<span id="8"></span>

<span data-ttu-id="5165a-422">**8** (0)</span><span class="sxs-lookup"><span data-stu-id="5165a-422">**8** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="16"></span>

<span data-ttu-id="5165a-423">**16** (1)</span><span class="sxs-lookup"><span data-stu-id="5165a-423">**16** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="32"></span>

<span data-ttu-id="5165a-424">**32** (2)</span><span class="sxs-lookup"><span data-stu-id="5165a-424">**32** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="64"></span>

<span data-ttu-id="5165a-425">**64** (3)</span><span class="sxs-lookup"><span data-stu-id="5165a-425">**64** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="128"></span>

<span data-ttu-id="5165a-426">**128** (4)</span><span class="sxs-lookup"><span data-stu-id="5165a-426">**128** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5165a-427">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="5165a-427">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-428">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-428">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-429">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-429">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-430">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5165a-430">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5165a-431">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="5165a-431">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="5165a-432">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-432">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-433">**Nome**</span><span class="sxs-lookup"><span data-stu-id="5165a-433">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-434">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-435">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-435">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-436">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="5165a-436">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="5165a-437">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="5165a-437">Label by which the object is known.</span></span> <span data-ttu-id="5165a-438">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="5165a-438">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="5165a-439">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-439">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-440">**Número**</span><span class="sxs-lookup"><span data-stu-id="5165a-440">**Number**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-441">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5165a-441">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-442">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-442">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5165a-443">Número de slot físico, que pode ser usado como um índice em uma tabela de slot do sistema, para determinar se o slot está ocupado fisicamente.</span><span class="sxs-lookup"><span data-stu-id="5165a-443">Physical slot number, which can be used as an index into a system slot table, to determine whether the slot is physically occupied.</span></span>

</dd> <dt>

<span data-ttu-id="5165a-444">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="5165a-444">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-445">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-445">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-446">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-446">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5165a-447">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5165a-447">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="5165a-448">Um exemplo são dados de código de barras associados a um elemento, que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="5165a-448">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="5165a-449">Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo e puderem ser usados como uma chave de elemento, essa propriedade será nula e os dados de código de barras seriam usados como a chave de classe na propriedade de **marca** .</span><span class="sxs-lookup"><span data-stu-id="5165a-449">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="5165a-450">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-450">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-451">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="5165a-451">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-452">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-452">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-453">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-453">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-454">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5165a-454">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5165a-455">Número de peça atribuído pela organização que produziu ou fabricou o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5165a-455">Part number assigned by the organization that produced or manufactured the physical element.</span></span>

<span data-ttu-id="5165a-456">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-456">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-457">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="5165a-457">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-458">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5165a-458">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-459">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-459">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5165a-460">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="5165a-460">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="5165a-461">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-461">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-462">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="5165a-462">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-463">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-463">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-464">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-465">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ slot CIM**.**SpecialPurpose**")</span><span class="sxs-lookup"><span data-stu-id="5165a-465">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Slot**.**SpecialPurpose**")</span></span>
</dt> </dl>

<span data-ttu-id="5165a-466">Cadeia de caracteres de forma livre que descreve como esse slot é fisicamente exclusivo e que ele pode conter tipos especiais de hardware.</span><span class="sxs-lookup"><span data-stu-id="5165a-466">Free-form string that describes how this slot is physically unique and that it may hold special types of hardware.</span></span> <span data-ttu-id="5165a-467">Essa propriedade só tem significado quando a propriedade booliana **SpecialPurpose** correspondente é definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="5165a-467">This property only has meaning when the corresponding Boolean **SpecialPurpose** property is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="5165a-468">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="5165a-468">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-469">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-469">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-470">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-470">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-471">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5165a-471">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5165a-472">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5165a-472">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="5165a-473">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-473">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-474">**SKU**</span><span class="sxs-lookup"><span data-stu-id="5165a-474">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-475">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-475">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-476">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-476">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-477">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5165a-477">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5165a-478">Número de unidade de manutenção de estoque do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5165a-478">Stock-keeping unit number for the physical element.</span></span>

<span data-ttu-id="5165a-479">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-479">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-480">**SpecialPurpose**</span><span class="sxs-lookup"><span data-stu-id="5165a-480">**SpecialPurpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-481">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5165a-481">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-482">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-482">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-483">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ slot CIM**.**PurposeDescription**")</span><span class="sxs-lookup"><span data-stu-id="5165a-483">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Slot**.**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="5165a-484">Se for **true**, o slot será fisicamente exclusivo e poderá conter tipos especiais de hardware, (por exemplo, um slot de processador gráfico).</span><span class="sxs-lookup"><span data-stu-id="5165a-484">If **TRUE**, the slot is physically unique and may hold special types of hardware, (for example, a graphics processor slot).</span></span> <span data-ttu-id="5165a-485">Se **for true**, a propriedade **PurposeDescription** deverá especificar como o slot é exclusivo ou a finalidade do slot.</span><span class="sxs-lookup"><span data-stu-id="5165a-485">If **TRUE**, the **PurposeDescription** property should specify how the slot is unique or the slot's purpose.</span></span>

</dd> <dt>

<span data-ttu-id="5165a-486">**Status**</span><span class="sxs-lookup"><span data-stu-id="5165a-486">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-487">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-488">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-489">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="5165a-489">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="5165a-490">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="5165a-490">Current status of the object.</span></span> <span data-ttu-id="5165a-491">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-491">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="5165a-492">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5165a-492">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="5165a-493">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="5165a-493">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="5165a-494">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="5165a-494">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="5165a-495">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="5165a-495">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5165a-496">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="5165a-496">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="5165a-497">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="5165a-497">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="5165a-498">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="5165a-498">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="5165a-499">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="5165a-499">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="5165a-500">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="5165a-500">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="5165a-501">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="5165a-501">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="5165a-502">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="5165a-502">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="5165a-503">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="5165a-503">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="5165a-504">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="5165a-504">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5165a-505">**SupportsHotPlug**</span><span class="sxs-lookup"><span data-stu-id="5165a-505">**SupportsHotPlug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-506">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="5165a-506">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-507">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-507">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5165a-508">Se **for true**, o slot dará suporte à conexão automática de placas de adaptador.</span><span class="sxs-lookup"><span data-stu-id="5165a-508">If **TRUE**, the slot supports hot-plugging of adapter cards.</span></span>

</dd> <dt>

<span data-ttu-id="5165a-509">**Tag**</span><span class="sxs-lookup"><span data-stu-id="5165a-509">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-510">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-510">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-511">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-511">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-512">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="5165a-512">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="5165a-513">Cadeia de caracteres arbitrária que identifica exclusivamente o elemento físico e serve como a chave do elemento.</span><span class="sxs-lookup"><span data-stu-id="5165a-513">Arbitrary string that uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="5165a-514">Essa propriedade pode conter informações, como a marca de ativo ou os dados de número de série.</span><span class="sxs-lookup"><span data-stu-id="5165a-514">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="5165a-515">A chave para [**o \_ físico do CIM**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar de forma independente o hardware/entidade, independentemente do posicionamento físico nos gabinetes, adaptadores e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5165a-515">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware/entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="5165a-516">Por exemplo, um componente removível que pode ser intercambiável pode ser extraído de seu pacote recipiente (escopo) e estar temporariamente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="5165a-516">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="5165a-517">O objeto ainda continua existindo e pode até ser inserido em um contêiner de escopo diferente.</span><span class="sxs-lookup"><span data-stu-id="5165a-517">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="5165a-518">A chave para um elemento físico é uma cadeia de caracteres arbitrária que é definida independentemente do posicionamento ou da hierarquia orientada por local.</span><span class="sxs-lookup"><span data-stu-id="5165a-518">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="5165a-519">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-519">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-520">**ThermalRating**</span><span class="sxs-lookup"><span data-stu-id="5165a-520">**ThermalRating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-521">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5165a-521">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-522">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-523">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Slot do sistema DMTF \| 4,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" miliwatts ")</span><span class="sxs-lookup"><span data-stu-id="5165a-523">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.11"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="5165a-524">Dissipação térmica máxima do slot, em miliwatts.</span><span class="sxs-lookup"><span data-stu-id="5165a-524">Maximum thermal dissipation of the slot, in milliwatts.</span></span>

</dd> <dt>

<span data-ttu-id="5165a-525">**VccMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="5165a-525">**VccMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-526">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5165a-526">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5165a-527">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-527">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-528">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Slot do sistema DMTF \| 4,9 ")</span><span class="sxs-lookup"><span data-stu-id="5165a-528">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="5165a-529">Tensão VCC suportada pelo slot.</span><span class="sxs-lookup"><span data-stu-id="5165a-529">Vcc voltage supported by the slot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5165a-530">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5165a-530">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5165a-531">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5165a-531">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="5165a-532">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="5165a-532">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="5165a-533">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="5165a-533">**5V** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5165a-534">**Versão**</span><span class="sxs-lookup"><span data-stu-id="5165a-534">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-535">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5165a-535">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5165a-536">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-536">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-537">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="5165a-537">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="5165a-538">Versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="5165a-538">Version of the physical element.</span></span>

<span data-ttu-id="5165a-539">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-539">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="5165a-540">**VppMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="5165a-540">**VppMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5165a-541">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5165a-541">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5165a-542">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5165a-542">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5165a-543">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Slot do sistema DMTF \| 4,10 ")</span><span class="sxs-lookup"><span data-stu-id="5165a-543">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Slot\|004.10")</span></span>
</dt> </dl>

<span data-ttu-id="5165a-544">Tensão de VPP suportada pelo slot.</span><span class="sxs-lookup"><span data-stu-id="5165a-544">Vpp voltage supported by the slot.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5165a-545">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5165a-545">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5165a-546">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5165a-546">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="5165a-547">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="5165a-547">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="5165a-548">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="5165a-548">**5V** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

<span data-ttu-id="5165a-549">**12V** (4)</span><span class="sxs-lookup"><span data-stu-id="5165a-549">**12V** (4)</span></span>


<span data-ttu-id="5165a-550"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="5165a-550"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="5165a-551">Comentários</span><span class="sxs-lookup"><span data-stu-id="5165a-551">Remarks</span></span>

<span data-ttu-id="5165a-552">A classe de **\_ slot CIM** é derivada do [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-552">The **CIM\_Slot** class is derived from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<span data-ttu-id="5165a-553">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="5165a-553">WMI does not implement this class.</span></span> <span data-ttu-id="5165a-554">Para classes WMI derivadas do **\_ slot CIM**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="5165a-554">For WMI classes derived from **CIM\_Slot**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="5165a-555">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="5165a-555">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5165a-556">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="5165a-556">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5165a-557">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5165a-557">Requirements</span></span>



| <span data-ttu-id="5165a-558">Requisito</span><span class="sxs-lookup"><span data-stu-id="5165a-558">Requirement</span></span> | <span data-ttu-id="5165a-559">Valor</span><span class="sxs-lookup"><span data-stu-id="5165a-559">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5165a-560">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5165a-560">Minimum supported client</span></span><br/> | <span data-ttu-id="5165a-561">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5165a-561">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5165a-562">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5165a-562">Minimum supported server</span></span><br/> | <span data-ttu-id="5165a-563">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5165a-563">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5165a-564">Namespace</span><span class="sxs-lookup"><span data-stu-id="5165a-564">Namespace</span></span><br/>                | <span data-ttu-id="5165a-565">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5165a-565">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5165a-566">MOF</span><span class="sxs-lookup"><span data-stu-id="5165a-566">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5165a-567"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5165a-567"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5165a-568">DLL</span><span class="sxs-lookup"><span data-stu-id="5165a-568">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5165a-569"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5165a-569"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5165a-570">Confira também</span><span class="sxs-lookup"><span data-stu-id="5165a-570">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5165a-571">**\_PHYSICALCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="5165a-571">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> </dl>

 

