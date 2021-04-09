---
description: O Win32 \_ SystemSlot &\# 32; A classe WMI representa pontos de conexão física, incluindo portas, slots de placa-mãe e periféricos e pontos de conexão proprietários.
ms.assetid: 0bdce597-dcbe-4593-b0d6-68c3bfecd0ee
ms.tgt_platform: multiple
title: Classe Win32_SystemSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemSlot
- Win32_SystemSlot.BusNumber
- Win32_SystemSlot.Caption
- Win32_SystemSlot.ConnectorPinout
- Win32_SystemSlot.ConnectorType
- Win32_SystemSlot.CreationClassName
- Win32_SystemSlot.CurrentUsage
- Win32_SystemSlot.Description
- Win32_SystemSlot.DeviceNumber
- Win32_SystemSlot.FunctionNumber
- Win32_SystemSlot.HeightAllowed
- Win32_SystemSlot.InstallDate
- Win32_SystemSlot.LengthAllowed
- Win32_SystemSlot.Manufacturer
- Win32_SystemSlot.MaxDataWidth
- Win32_SystemSlot.Model
- Win32_SystemSlot.Name
- Win32_SystemSlot.Number
- Win32_SystemSlot.OtherIdentifyingInfo
- Win32_SystemSlot.PartNumber
- Win32_SystemSlot.PMESignal
- Win32_SystemSlot.PoweredOn
- Win32_SystemSlot.PurposeDescription
- Win32_SystemSlot.SegmentGroupNumber
- Win32_SystemSlot.SerialNumber
- Win32_SystemSlot.Shared
- Win32_SystemSlot.SKU
- Win32_SystemSlot.SlotDesignation
- Win32_SystemSlot.SpecialPurpose
- Win32_SystemSlot.Status
- Win32_SystemSlot.SupportsHotPlug
- Win32_SystemSlot.Tag
- Win32_SystemSlot.ThermalRating
- Win32_SystemSlot.VccMixedVoltageSupport
- Win32_SystemSlot.Version
- Win32_SystemSlot.VppMixedVoltageSupport
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1e2913aa2d8850aae4fdad8fbca71f216cd848f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089593"
---
# <a name="win32_systemslot-class"></a><span data-ttu-id="22c5c-103">\_Classe Win32 SystemSlot</span><span class="sxs-lookup"><span data-stu-id="22c5c-103">Win32\_SystemSlot class</span></span>

<span data-ttu-id="22c5c-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SystemSlot do Win32** representa pontos de conexão físicos, incluindo portas, slots de placa-mãe e periféricos, e pontos de conexão proprietários.</span><span class="sxs-lookup"><span data-stu-id="22c5c-104">The **Win32\_SystemSlot** [WMI class](../wmisdk/retrieving-a-class.md) represents physical connection points including ports, motherboard slots and peripherals, and proprietary connection points.</span></span>

<span data-ttu-id="22c5c-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="22c5c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="22c5c-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="22c5c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="22c5c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="22c5c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B91-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_SystemSlot : CIM_Slot
{
  uint32   BusNumber;
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  uint16   CurrentUsage;
  string   Description;
  uint32   DeviceNumber;
  uint32   FunctionNumber;
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
  boolean  PMESignal;
  boolean  PoweredOn;
  string   PurposeDescription;
  uint32   SegmentGroupNumber;
  string   SerialNumber;
  boolean  Shared;
  string   SKU;
  string   SlotDesignation;
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

## <a name="members"></a><span data-ttu-id="22c5c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="22c5c-108">Members</span></span>

<span data-ttu-id="22c5c-109">A classe **Win32 \_ SystemSlot** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="22c5c-109">The **Win32\_SystemSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="22c5c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="22c5c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="22c5c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="22c5c-111">Properties</span></span>

<span data-ttu-id="22c5c-112">A classe **Win32 \_ SystemSlot** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="22c5c-112">The **Win32\_SystemSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22c5c-113">**BusNumber**</span><span class="sxs-lookup"><span data-stu-id="22c5c-113">**BusNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-114">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22c5c-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-116">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| número do barramento do tipo SMBIOS 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="22c5c-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Bus Number")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-117">Número do barramento SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-117">SMBIOS Bus Number.</span></span>

<span data-ttu-id="22c5c-118">Esse valor é proveniente do membro de **número de barramento** da estrutura de **slots do sistema** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-118">This value comes from the **Bus Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="22c5c-119">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="22c5c-119">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-120">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="22c5c-120">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-123">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="22c5c-123">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-124">Breve descrição de um objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="22c5c-124">Short description of an object—a one-line string.</span></span>

<span data-ttu-id="22c5c-125">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-126">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="22c5c-126">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-127">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-129">Cadeia de caracteres de forma livre que descreve a configuração de PIN e o uso de sinal de um conector físico.</span><span class="sxs-lookup"><span data-stu-id="22c5c-129">Free-form string that describes the pin configuration and signal usage of a physical connector.</span></span>

<span data-ttu-id="22c5c-130">Essa propriedade é herdada do [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-130">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-131">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="22c5c-131">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-132">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22c5c-132">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-134">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de slot do SMBIOS \| tipo 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="22c5c-134">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Type")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-135">Matriz de atributos físicos do conector que este slot usa.</span><span class="sxs-lookup"><span data-stu-id="22c5c-135">Array of physical attributes of the connector that this slot uses.</span></span>

<span data-ttu-id="22c5c-136">Esse valor é proveniente do membro de **tipo de slot** da estrutura de **slots do sistema** nas informações de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-136">This value comes from the **Slot Type** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="22c5c-137">Essa propriedade é herdada do [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-137">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

<span data-ttu-id="22c5c-138">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="22c5c-138">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22c5c-139">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="22c5c-139">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="22c5c-140">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="22c5c-140">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="22c5c-141">**Masculino** (2)</span><span class="sxs-lookup"><span data-stu-id="22c5c-141">**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="22c5c-142">**Fêmea** (3)</span><span class="sxs-lookup"><span data-stu-id="22c5c-142">**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="22c5c-143">**Blindado** (4)</span><span class="sxs-lookup"><span data-stu-id="22c5c-143">**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="22c5c-144">Não **blindado** (5)</span><span class="sxs-lookup"><span data-stu-id="22c5c-144">**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="22c5c-145">**SCSI (A) High-Density (50 Pins)** (6)</span><span class="sxs-lookup"><span data-stu-id="22c5c-145">**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="22c5c-146">**SCSI (A) Low-Density (50 Pins)** (7)</span><span class="sxs-lookup"><span data-stu-id="22c5c-146">**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="22c5c-147">**SCSI (P) High-Density (68 Pins)** (8)</span><span class="sxs-lookup"><span data-stu-id="22c5c-147">**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="22c5c-148">**SCSI SCA-I (80 pinos)** (9)</span><span class="sxs-lookup"><span data-stu-id="22c5c-148">**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="22c5c-149">**SCSI SCA-II (80 pinos)** (10)</span><span class="sxs-lookup"><span data-stu-id="22c5c-149">**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="22c5c-150">**Fibre Channel SCSI (DB-9, cobre)** (11)</span><span class="sxs-lookup"><span data-stu-id="22c5c-150">**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="22c5c-151">**SCSI Fibre Channel (Fibre)** (12)</span><span class="sxs-lookup"><span data-stu-id="22c5c-151">**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="22c5c-152">**SCSI Fibre Channel SCA-II (40 pinos)** (13)</span><span class="sxs-lookup"><span data-stu-id="22c5c-152">**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="22c5c-153">**SCSI Fibre Channel SCA-II (20 pinos)** (14)</span><span class="sxs-lookup"><span data-stu-id="22c5c-153">**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="22c5c-154">**SCSI Fibre Channel BNC** (15)</span><span class="sxs-lookup"><span data-stu-id="22c5c-154">**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="22c5c-155">**ATA 3-1/2 polegada (40 pinos)** (16)</span><span class="sxs-lookup"><span data-stu-id="22c5c-155">**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="22c5c-156">**ATA 2-1/2 polegada (44 pinos)** (17)</span><span class="sxs-lookup"><span data-stu-id="22c5c-156">**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="22c5c-157">**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="22c5c-157">**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="22c5c-158">**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="22c5c-158">**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="22c5c-159">**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="22c5c-159">**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="22c5c-160">**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="22c5c-160">**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="22c5c-161">**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="22c5c-161">**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="22c5c-162">**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="22c5c-162">**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="22c5c-163">**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="22c5c-163">**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="22c5c-164">**RS-232C** (25)</span><span class="sxs-lookup"><span data-stu-id="22c5c-164">**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="22c5c-165">**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="22c5c-165">**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="22c5c-166">**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="22c5c-166">**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="22c5c-167">**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="22c5c-167">**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="22c5c-168">**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="22c5c-168">**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="22c5c-169">**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="22c5c-169">**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="22c5c-170">**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="22c5c-170">**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="22c5c-171">**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="22c5c-171">**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="22c5c-172">**AUI** (33)</span><span class="sxs-lookup"><span data-stu-id="22c5c-172">**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="22c5c-173">**UTP categoria 3** (34)</span><span class="sxs-lookup"><span data-stu-id="22c5c-173">**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="22c5c-174">**UTP categoria 4** (35)</span><span class="sxs-lookup"><span data-stu-id="22c5c-174">**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="22c5c-175">**UTP categoria 5** (36)</span><span class="sxs-lookup"><span data-stu-id="22c5c-175">**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="22c5c-176">**BNC** (37)</span><span class="sxs-lookup"><span data-stu-id="22c5c-176">**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="22c5c-177">**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="22c5c-177">**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="22c5c-178">**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="22c5c-178">**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="22c5c-179">**MIC de fibra** (40)</span><span class="sxs-lookup"><span data-stu-id="22c5c-179">**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="22c5c-180">**Apple AUI** (41)</span><span class="sxs-lookup"><span data-stu-id="22c5c-180">**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="22c5c-181">**Apple GeoPort** (42)</span><span class="sxs-lookup"><span data-stu-id="22c5c-181">**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="22c5c-182">**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="22c5c-182">**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="22c5c-183">**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="22c5c-183">**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="22c5c-184">**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="22c5c-184">**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="22c5c-185">**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="22c5c-185">**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="22c5c-186">**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="22c5c-186">**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="22c5c-187">**Tipo de PCMCIA I** (48)</span><span class="sxs-lookup"><span data-stu-id="22c5c-187">**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="22c5c-188">**PCMCIA tipo II** (49)</span><span class="sxs-lookup"><span data-stu-id="22c5c-188">**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="22c5c-189">**Tipo de PCMCIA III** (50)</span><span class="sxs-lookup"><span data-stu-id="22c5c-189">**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="22c5c-190">**Porta ZV** (51)</span><span class="sxs-lookup"><span data-stu-id="22c5c-190">**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="22c5c-191">**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="22c5c-191">**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="22c5c-192">**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="22c5c-192">**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="22c5c-193">**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="22c5c-193">**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="22c5c-194">**HIPPI** (55)</span><span class="sxs-lookup"><span data-stu-id="22c5c-194">**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="22c5c-195">**HSSDC (6 pinos)** (56)</span><span class="sxs-lookup"><span data-stu-id="22c5c-195">**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="22c5c-196">**GBIC** (57)</span><span class="sxs-lookup"><span data-stu-id="22c5c-196">**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="22c5c-197">**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="22c5c-197">**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="22c5c-198">**Mini-DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="22c5c-198">**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="22c5c-199">**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="22c5c-199">**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="22c5c-200">**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="22c5c-200">**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="22c5c-201">**Infravermelho** (62)</span><span class="sxs-lookup"><span data-stu-id="22c5c-201">**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="22c5c-202">**HP-Hil** (63)</span><span class="sxs-lookup"><span data-stu-id="22c5c-202">**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="22c5c-203">**Access. Bus** (64)</span><span class="sxs-lookup"><span data-stu-id="22c5c-203">**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="22c5c-204">**NuBus** (65)</span><span class="sxs-lookup"><span data-stu-id="22c5c-204">**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="22c5c-205">**Centronics** (66)</span><span class="sxs-lookup"><span data-stu-id="22c5c-205">**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="22c5c-206">**Mini-Centronics** (67)</span><span class="sxs-lookup"><span data-stu-id="22c5c-206">**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="22c5c-207">**Tipo de mini-Centronics-14** (68)</span><span class="sxs-lookup"><span data-stu-id="22c5c-207">**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="22c5c-208">**Tipo de mini-Centronics-20** (69)</span><span class="sxs-lookup"><span data-stu-id="22c5c-208">**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="22c5c-209">**Tipo de mini-Centronics-26** (70)</span><span class="sxs-lookup"><span data-stu-id="22c5c-209">**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="22c5c-210">**Mouse de barramento** (71)</span><span class="sxs-lookup"><span data-stu-id="22c5c-210">**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="22c5c-211">**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="22c5c-211">**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="22c5c-212">**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="22c5c-212">**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="22c5c-213">**Barramento de VM** (74)</span><span class="sxs-lookup"><span data-stu-id="22c5c-213">**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="22c5c-214">**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="22c5c-214">**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="22c5c-215">**Proprietário** (76)</span><span class="sxs-lookup"><span data-stu-id="22c5c-215">**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="22c5c-216">**Slot do cartão de processador proprietário** (77)</span><span class="sxs-lookup"><span data-stu-id="22c5c-216">**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="22c5c-217">**Slot de placa de memória proprietária** (78)</span><span class="sxs-lookup"><span data-stu-id="22c5c-217">**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="22c5c-218">**Slot de riser de e/s proprietário** (79)</span><span class="sxs-lookup"><span data-stu-id="22c5c-218">**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="22c5c-219">**PCI-66MHZ** (80)</span><span class="sxs-lookup"><span data-stu-id="22c5c-219">**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="22c5c-220">**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="22c5c-220">**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="22c5c-221">**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="22c5c-221">**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="22c5c-222">**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="22c5c-222">**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="22c5c-223">**PC-98-Hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="22c5c-223">**PC-98-Hireso** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="22c5c-224">**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="22c5c-224">**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="22c5c-225">**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="22c5c-225">**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="22c5c-226">**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="22c5c-226">**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

<span data-ttu-id="22c5c-227">**PCI-X** (88)</span><span class="sxs-lookup"><span data-stu-id="22c5c-227">**PCI-X** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

<span data-ttu-id="22c5c-228">**Sbus IEEE 1396-1993 32 bit** (89)</span><span class="sxs-lookup"><span data-stu-id="22c5c-228">**Sbus IEEE 1396-1993 32 bit** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

<span data-ttu-id="22c5c-229">**Sbus IEEE 1396-1993 64 bit** (90)</span><span class="sxs-lookup"><span data-stu-id="22c5c-229">**Sbus IEEE 1396-1993 64 bit** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="22c5c-230">**MCA** (91)</span><span class="sxs-lookup"><span data-stu-id="22c5c-230">**MCA** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

<span data-ttu-id="22c5c-231">**Gio** (92)</span><span class="sxs-lookup"><span data-stu-id="22c5c-231">**GIO** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

<span data-ttu-id="22c5c-232">**Xio** (93)</span><span class="sxs-lookup"><span data-stu-id="22c5c-232">**XIO** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

<span data-ttu-id="22c5c-233">**HIO** (94)</span><span class="sxs-lookup"><span data-stu-id="22c5c-233">**HIO** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

<span data-ttu-id="22c5c-234">**NGIO** (95)</span><span class="sxs-lookup"><span data-stu-id="22c5c-234">**NGIO** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

<span data-ttu-id="22c5c-235">**PMC** (96)</span><span class="sxs-lookup"><span data-stu-id="22c5c-235">**PMC** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

<span data-ttu-id="22c5c-236">**E/s futura** (97)</span><span class="sxs-lookup"><span data-stu-id="22c5c-236">**Future I/O** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="22c5c-237">**InfiniBand** (98)</span><span class="sxs-lookup"><span data-stu-id="22c5c-237">**InfiniBand** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP8X"></span><span id="agp8x"></span>

<span data-ttu-id="22c5c-238">**AGP8X** (99)</span><span class="sxs-lookup"><span data-stu-id="22c5c-238">**AGP8X** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-E"></span><span id="pci-e"></span>

<span data-ttu-id="22c5c-239">**PCI-E** (100)</span><span class="sxs-lookup"><span data-stu-id="22c5c-239">**PCI-E** (100)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="22c5c-240">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="22c5c-240">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-241">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-243">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="22c5c-243">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-244">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="22c5c-244">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="22c5c-245">Quando usado com as outras propriedades de chave de uma classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="22c5c-245">When used with the other key properties of a class, this property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="22c5c-246">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-246">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-247">**CurrentUsage**</span><span class="sxs-lookup"><span data-stu-id="22c5c-247">**CurrentUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-248">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22c5c-248">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-249">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-249">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-250">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de SMBIOS \| 9 \| uso atual")</span><span class="sxs-lookup"><span data-stu-id="22c5c-250">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Current Usage")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-251">Status do uso do slot do sistema.</span><span class="sxs-lookup"><span data-stu-id="22c5c-251">Status of system slot use.</span></span>

<span data-ttu-id="22c5c-252">Esse valor é proveniente do membro de **uso atual** da estrutura de **slots do sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-252">This value comes from the **Current Usage** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="22c5c-253">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="22c5c-253">The possible values are.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="22c5c-254">**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="22c5c-254">**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="22c5c-255">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="22c5c-255">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22c5c-256">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="22c5c-256">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="22c5c-257">**Disponível** (3)</span><span class="sxs-lookup"><span data-stu-id="22c5c-257">**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_use"></span><span id="in_use"></span><span id="IN_USE"></span>

<span data-ttu-id="22c5c-258">**Em uso** (4)</span><span class="sxs-lookup"><span data-stu-id="22c5c-258">**In use** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="22c5c-259">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="22c5c-259">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-260">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-260">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-262">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="22c5c-262">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-263">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="22c5c-263">Description of the object.</span></span>

<span data-ttu-id="22c5c-264">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-264">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-265">**DeviceNumber**</span><span class="sxs-lookup"><span data-stu-id="22c5c-265">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-266">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22c5c-266">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-267">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-267">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-268">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("número de dispositivo do SMBIOS \| tipo 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="22c5c-268">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Device Number")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-269">Número do dispositivo SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-269">SMBIOS Device Number.</span></span>

<span data-ttu-id="22c5c-270">Esse valor é proveniente do membro do **número do dispositivo/função** da estrutura de **slots do sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-270">This value comes from the **Device/Function Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="22c5c-271">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="22c5c-271">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-272">**FunctionNumber**</span><span class="sxs-lookup"><span data-stu-id="22c5c-272">**FunctionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-273">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22c5c-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-274">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-275">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("número de função do SMBIOS \| tipo 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="22c5c-275">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Function Number")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-276">Número da função SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-276">SMBIOS Function Number.</span></span>

<span data-ttu-id="22c5c-277">Esse valor é proveniente do membro do **número do dispositivo/função** da estrutura de **slots do sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-277">This value comes from the **Device/Function Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="22c5c-278">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="22c5c-278">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-279">**HeightAllowed**</span><span class="sxs-lookup"><span data-stu-id="22c5c-279">**HeightAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-280">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="22c5c-280">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-281">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-281">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-282">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="22c5c-282">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-283">Altura máxima de uma placa de adaptador que pode ser inserida no slot — em polegadas.</span><span class="sxs-lookup"><span data-stu-id="22c5c-283">Maximum height of an adapter card that can be inserted into the slot—in inches.</span></span>

<span data-ttu-id="22c5c-284">Essa propriedade é herdada [**do \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-284">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-285">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="22c5c-285">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-286">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="22c5c-286">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-287">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-287">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-288">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="22c5c-288">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-289">Data e hora em que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="22c5c-289">Date and time the object is installed.</span></span> <span data-ttu-id="22c5c-290">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="22c5c-290">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="22c5c-291">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-291">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-292">**LengthAllowed**</span><span class="sxs-lookup"><span data-stu-id="22c5c-292">**LengthAllowed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-293">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="22c5c-293">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-295">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="22c5c-295">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-296">Comprimento máximo de uma placa de adaptador que pode ser inserida no slot — em polegadas.</span><span class="sxs-lookup"><span data-stu-id="22c5c-296">Maximum length of an adapter card that can be inserted into the slot—in inches.</span></span>

<span data-ttu-id="22c5c-297">Essa propriedade é herdada [**do \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-297">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-298">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="22c5c-298">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-299">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-301">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="22c5c-301">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-302">Nome da organização que produz o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="22c5c-302">Name of the organization that produces the physical element.</span></span>

<span data-ttu-id="22c5c-303">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-303">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-304">**MaxDataWidth**</span><span class="sxs-lookup"><span data-stu-id="22c5c-304">**MaxDataWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-305">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22c5c-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-307">Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("MaxDataWidth"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Slot do sistema DMTF \| 4,3 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits ")</span><span class="sxs-lookup"><span data-stu-id="22c5c-307">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("MaxDataWidth"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.3"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-308">Largura máxima do barramento de placas de adaptador que podem ser inseridas nesse slot — em bits.</span><span class="sxs-lookup"><span data-stu-id="22c5c-308">Maximum bus width of adapter cards that can be inserted into this slot—in bits.</span></span> <span data-ttu-id="22c5c-309">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="22c5c-309">This can be one of the following values.</span></span>

<span data-ttu-id="22c5c-310">Esse valor é proveniente do membro **largura do barramento de dados do slot** da estrutura slots do **sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-310">This value comes from the **Slot Data Bus Width** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="22c5c-311">Essa propriedade é herdada [**do \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-311">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="22c5c-312">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="22c5c-312">The possible values are.</span></span>

<dt>

<span id="8"></span>

<span data-ttu-id="22c5c-313"><span id="8"></span>**8** (0)</span><span class="sxs-lookup"><span data-stu-id="22c5c-313"><span id="8"></span>**8** (0)</span></span>


</dt> <dd>

<span data-ttu-id="22c5c-314">Largura máxima dos dados (bits): 8</span><span class="sxs-lookup"><span data-stu-id="22c5c-314">Maximum data width (bits): 8</span></span>

</dd> <dt>

<span id="16"></span>

<span data-ttu-id="22c5c-315"><span id="16"></span>**16** (1)</span><span class="sxs-lookup"><span data-stu-id="22c5c-315"><span id="16"></span>**16** (1)</span></span>


</dt> <dd>

<span data-ttu-id="22c5c-316">Largura máxima dos dados (bits): 16</span><span class="sxs-lookup"><span data-stu-id="22c5c-316">Maximum data width (bits): 16</span></span>

</dd> <dt>

<span id="32"></span>

<span data-ttu-id="22c5c-317"><span id="32"></span>**32** (2)</span><span class="sxs-lookup"><span data-stu-id="22c5c-317"><span id="32"></span>**32** (2)</span></span>


</dt> <dd>

<span data-ttu-id="22c5c-318">Largura máxima dos dados (bits): 32</span><span class="sxs-lookup"><span data-stu-id="22c5c-318">Maximum data width (bits): 32</span></span>

</dd> <dt>

<span id="64"></span>

<span data-ttu-id="22c5c-319"><span id="64"></span>**64** (3)</span><span class="sxs-lookup"><span data-stu-id="22c5c-319"><span id="64"></span>**64** (3)</span></span>


</dt> <dd>

<span data-ttu-id="22c5c-320">Largura máxima dos dados (bits): 64</span><span class="sxs-lookup"><span data-stu-id="22c5c-320">Maximum data width (bits): 64</span></span>

</dd> <dt>

<span id="128"></span>

<span data-ttu-id="22c5c-321"><span id="128"></span>**128** (4)</span><span class="sxs-lookup"><span data-stu-id="22c5c-321"><span id="128"></span>**128** (4)</span></span>


</dt> <dd>

<span data-ttu-id="22c5c-322">Largura máxima dos dados (bits): 128</span><span class="sxs-lookup"><span data-stu-id="22c5c-322">Maximum data width (bits): 128</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="22c5c-323">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="22c5c-323">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-324">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-324">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-325">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-325">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-326">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="22c5c-326">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-327">Nome do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="22c5c-327">Name for the physical element.</span></span>

<span data-ttu-id="22c5c-328">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-328">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-329">**Nome**</span><span class="sxs-lookup"><span data-stu-id="22c5c-329">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-330">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-330">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-332">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="22c5c-332">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-333">Rótulo do objeto.</span><span class="sxs-lookup"><span data-stu-id="22c5c-333">Label for the object.</span></span> <span data-ttu-id="22c5c-334">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="22c5c-334">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="22c5c-335">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-335">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-336">**Número**</span><span class="sxs-lookup"><span data-stu-id="22c5c-336">**Number**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-337">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22c5c-337">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-338">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-339">Número de slot físico que pode ser usado como um índice em uma tabela de slot do sistema, independentemente de esse slot estar fisicamente vazio.</span><span class="sxs-lookup"><span data-stu-id="22c5c-339">Physical slot number that can be used as an index into a system slot table, whether or not that slot is physically empty.</span></span>

<span data-ttu-id="22c5c-340">Esse valor é proveniente do membro **ID do slot** da estrutura slots do **sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-340">This value comes from the **Slot ID** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="22c5c-341">Essa propriedade é herdada [**do \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-341">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-342">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="22c5c-342">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-343">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-344">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-345">Dados adicionais (ou seja, mais do que as informações de marca do ativo), que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="22c5c-345">Additional data (that is, more than the asset tag information), that can be used to identify a physical element.</span></span> <span data-ttu-id="22c5c-346">Um exemplo são os dados de código de barras associados a um elemento que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="22c5c-346">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="22c5c-347">Observe que se apenas os dados de código de barras estiverem disponíveis e for exclusivo ou puderem ser usados como uma chave de elemento, essa propriedade será **nula** e os dados de código de barras serão usados como a chave de classe na propriedade de **marca** .</span><span class="sxs-lookup"><span data-stu-id="22c5c-347">Note that if only bar code data is available, and it is unique or can be used as an element key, this property is **NULL**, and the bar code data is used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="22c5c-348">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-348">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-349">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="22c5c-349">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-350">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-350">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-351">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-351">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-352">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="22c5c-352">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-353">Número de peça que o produtor ou fabricante atribui ao elemento físico.</span><span class="sxs-lookup"><span data-stu-id="22c5c-353">Part number that the producer or manufacturer assigns to the physical element.</span></span>

<span data-ttu-id="22c5c-354">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-354">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-355">**PMESignal**</span><span class="sxs-lookup"><span data-stu-id="22c5c-355">**PMESignal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-356">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="22c5c-356">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-357">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-357">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-358">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| características do slot do tipo SMBIOS 9 \| 2")</span><span class="sxs-lookup"><span data-stu-id="22c5c-358">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Characteristics 2")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-359">Se for **true**, o sinal PME (gerenciamento de energia de barramento PCI) habilitado é suportado por este slot.</span><span class="sxs-lookup"><span data-stu-id="22c5c-359">If **TRUE**, the PCI bus Power Management Enabled (PME) signal is supported by this slot.</span></span>

<span data-ttu-id="22c5c-360">Esse valor é proveniente do membro **características do slot 2** da estrutura **slots do sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-360">This value comes from the **Slot Characteristics 2** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-361">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="22c5c-361">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-362">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="22c5c-362">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-363">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-363">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-364">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="22c5c-364">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="22c5c-365">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-365">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-366">**PurposeDescription**</span><span class="sxs-lookup"><span data-stu-id="22c5c-366">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-367">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-369">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ slot CIM**](cim-slot.md).**SpecialPurpose**")</span><span class="sxs-lookup"><span data-stu-id="22c5c-369">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Slot**](cim-slot.md).**SpecialPurpose**")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-370">Cadeia de caracteres de forma livre que descreve como esse slot é fisicamente exclusivo e pode conter tipos especiais de hardware.</span><span class="sxs-lookup"><span data-stu-id="22c5c-370">Free-form string that describes how this slot is physically unique and may hold special types of hardware.</span></span> <span data-ttu-id="22c5c-371">Essa propriedade só tem significado quando a propriedade correspondente **SpecialPurpose** é **true**.</span><span class="sxs-lookup"><span data-stu-id="22c5c-371">This property only has meaning when the corresponding property **SpecialPurpose** is **TRUE**.</span></span>

<span data-ttu-id="22c5c-372">Essa propriedade é herdada [**do \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-372">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-373">**SegmentGroupNumber**</span><span class="sxs-lookup"><span data-stu-id="22c5c-373">**SegmentGroupNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-374">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22c5c-374">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-375">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-376">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("número do grupo de segmentos do SMBIOS \| tipo 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="22c5c-376">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Segment Group Number")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-377">Número do grupo de segmentos do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-377">SMBIOS Segment Group Number.</span></span>

<span data-ttu-id="22c5c-378">Esse valor é proveniente do membro **número do grupo de segmentos** da estrutura slots do **sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-378">This value comes from the **Segment Group Number** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="22c5c-379">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="22c5c-379">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-380">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="22c5c-380">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-381">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-381">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-382">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-382">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-383">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="22c5c-383">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-384">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="22c5c-384">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="22c5c-385">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-385">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-386">**Compartilhado**</span><span class="sxs-lookup"><span data-stu-id="22c5c-386">**Shared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-387">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="22c5c-387">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-389">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| características do slot do tipo SMBIOS 9 \| 1")</span><span class="sxs-lookup"><span data-stu-id="22c5c-389">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Characteristics 1")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-390">Se **for true**, dois ou mais slots compartilharão um local na placa-base, como um slot compartilhado de PCI/EISA.</span><span class="sxs-lookup"><span data-stu-id="22c5c-390">If **TRUE**, two or more slots share a location on the baseboard, such as a PCI/EISA shared slot.</span></span>

<span data-ttu-id="22c5c-391">Esse valor é proveniente do membro **características do slot 1** da estrutura de **slots do sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-391">This value comes from the **Slot Characteristics 1** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-392">**SKU**</span><span class="sxs-lookup"><span data-stu-id="22c5c-392">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-393">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-393">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-394">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-394">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-395">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="22c5c-395">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-396">Número de unidade manutenção para o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="22c5c-396">Stockkeeping unit number for the physical element.</span></span>

<span data-ttu-id="22c5c-397">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-397">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-398">**SlotDesignation**</span><span class="sxs-lookup"><span data-stu-id="22c5c-398">**SlotDesignation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-399">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-401">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| designação de slot do SMBIOS tipo 9 \| ")</span><span class="sxs-lookup"><span data-stu-id="22c5c-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 9\|Slot Designation")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-402">Cadeia de caracteres do SMBIOS que identifica a designação do slot do sistema do slot na placa-mãe.</span><span class="sxs-lookup"><span data-stu-id="22c5c-402">SMBIOS string that identifies the system slot designation of the slot on the motherboard.</span></span>

<span data-ttu-id="22c5c-403">Exemplo: "PCI-1"</span><span class="sxs-lookup"><span data-stu-id="22c5c-403">Example: "PCI-1"</span></span>

<span data-ttu-id="22c5c-404">Esse valor é proveniente do membro de **designação de slot** da estrutura de **slots do sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-404">This value comes from the **Slot Designation** member of the **System Slots** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-405">**SpecialPurpose**</span><span class="sxs-lookup"><span data-stu-id="22c5c-405">**SpecialPurpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-406">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="22c5c-406">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-408">Qualificadores: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**\_ slot CIM**](cim-slot.md).**PurposeDescription**")</span><span class="sxs-lookup"><span data-stu-id="22c5c-408">Qualifiers: [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM\_Slot**](cim-slot.md).**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-409">Se for **true**, esse slot será fisicamente exclusivo e poderá conter tipos especiais de hardware, como um slot de processador gráfico.</span><span class="sxs-lookup"><span data-stu-id="22c5c-409">If **TRUE**, this slot is physically unique and may hold special types of hardware, such as a graphics processor slot.</span></span> <span data-ttu-id="22c5c-410">Se **for true**, **PurposeDescription** deverá especificar a natureza da exclusividade ou da finalidade do slot.</span><span class="sxs-lookup"><span data-stu-id="22c5c-410">If **TRUE**, then **PurposeDescription** should specify the nature of the uniqueness or purpose of the slot.</span></span>

<span data-ttu-id="22c5c-411">Essa propriedade é herdada [**do \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-411">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-412">**Status**</span><span class="sxs-lookup"><span data-stu-id="22c5c-412">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-413">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-413">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-414">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-414">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-415">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="22c5c-415">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-416">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="22c5c-416">Current status of the object.</span></span> <span data-ttu-id="22c5c-417">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="22c5c-417">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="22c5c-418">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="22c5c-418">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="22c5c-419">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="22c5c-419">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="22c5c-420">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="22c5c-420">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="22c5c-421">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="22c5c-421">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="22c5c-422">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-422">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="22c5c-423">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="22c5c-423">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="22c5c-424">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="22c5c-424">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="22c5c-425">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="22c5c-425">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="22c5c-426">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="22c5c-426">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22c5c-427">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="22c5c-427">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="22c5c-428">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="22c5c-428">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="22c5c-429">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="22c5c-429">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="22c5c-430">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="22c5c-430">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="22c5c-431">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="22c5c-431">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="22c5c-432">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="22c5c-432">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="22c5c-433">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="22c5c-433">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="22c5c-434">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="22c5c-434">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="22c5c-435">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="22c5c-435">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="22c5c-436">**SupportsHotPlug**</span><span class="sxs-lookup"><span data-stu-id="22c5c-436">**SupportsHotPlug**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-437">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="22c5c-437">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-438">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-439">Se **for true**, o slot dará suporte à conexão automática de placas de adaptador.</span><span class="sxs-lookup"><span data-stu-id="22c5c-439">If **TRUE**, the slot supports hot-plugging of adapter cards.</span></span>

<span data-ttu-id="22c5c-440">Esse valor é proveniente do membro **características do slot 2** da estrutura **slots do sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-440">This value comes from the **Slot Characteristics 2** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="22c5c-441">Essa propriedade é herdada [**do \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-441">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-442">**Tag**</span><span class="sxs-lookup"><span data-stu-id="22c5c-442">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-443">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-444">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-445">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="22c5c-445">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-446">O slot do sistema representado por uma instância desta classe.</span><span class="sxs-lookup"><span data-stu-id="22c5c-446">System slot represented by an instance of this class.</span></span>

<span data-ttu-id="22c5c-447">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-447">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="22c5c-448">Exemplo: "slot do sistema 1"</span><span class="sxs-lookup"><span data-stu-id="22c5c-448">Example: "System Slot 1"</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-449">**ThermalRating**</span><span class="sxs-lookup"><span data-stu-id="22c5c-449">**ThermalRating**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-450">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="22c5c-450">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-451">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-451">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-452">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Slot do sistema DMTF \| 4,11 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" miliwatts ")</span><span class="sxs-lookup"><span data-stu-id="22c5c-452">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.11"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliwatts")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-453">Dissipação térmica máxima do slot em miliwatts.</span><span class="sxs-lookup"><span data-stu-id="22c5c-453">Maximum thermal dissipation of the slot in milliwatts.</span></span>

<span data-ttu-id="22c5c-454">Essa propriedade é herdada [**do \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-454">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-455">**VccMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="22c5c-455">**VccMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-456">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22c5c-456">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-457">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-457">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-458">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Slot do sistema DMTF \| 4,9 ")</span><span class="sxs-lookup"><span data-stu-id="22c5c-458">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.9")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-459">Matriz de inteiros enumerados que indicam a tensão VCC suportada por este slot.</span><span class="sxs-lookup"><span data-stu-id="22c5c-459">Array of enumerated integers indicating the Vcc voltage supported by this slot.</span></span>

<span data-ttu-id="22c5c-460">Esse valor é proveniente do membro **características do slot 1** da estrutura de **slots do sistema** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="22c5c-460">This value comes from the **Slot Characteristics 1** member of the **System Slots** structure in the SMBIOS information.</span></span>

<span data-ttu-id="22c5c-461">Essa propriedade é herdada [**do \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-461">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="22c5c-462">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="22c5c-462">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22c5c-463">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="22c5c-463">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="22c5c-464">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="22c5c-464">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="22c5c-465">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="22c5c-465">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="22c5c-466">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="22c5c-466">**5V** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="22c5c-467">**Versão**</span><span class="sxs-lookup"><span data-stu-id="22c5c-467">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-468">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="22c5c-468">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-469">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-469">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-470">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="22c5c-470">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-471">Versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="22c5c-471">Version of the physical element.</span></span>

<span data-ttu-id="22c5c-472">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-472">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="22c5c-473">**VppMixedVoltageSupport**</span><span class="sxs-lookup"><span data-stu-id="22c5c-473">**VppMixedVoltageSupport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22c5c-474">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22c5c-474">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-475">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="22c5c-475">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22c5c-476">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Slot do sistema DMTF \| 4,10 ")</span><span class="sxs-lookup"><span data-stu-id="22c5c-476">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|System Slot\|004.10")</span></span>
</dt> </dl>

<span data-ttu-id="22c5c-477">Matriz de inteiros enumerados que indicam a tensão de VPP com suporte neste slot.</span><span class="sxs-lookup"><span data-stu-id="22c5c-477">Array of enumerated integers indicating the Vpp voltage supported by this slot.</span></span>

<span data-ttu-id="22c5c-478">Essa propriedade é herdada [**do \_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-478">This property is inherited from [**CIM\_Slot**](cim-slot.md).</span></span>

<span data-ttu-id="22c5c-479">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="22c5c-479">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="22c5c-480">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="22c5c-480">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="22c5c-481">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="22c5c-481">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="3.3V"></span><span id="3.3v"></span>

<span data-ttu-id="22c5c-482">**3.3 v** (2)</span><span class="sxs-lookup"><span data-stu-id="22c5c-482">**3.3V** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="5V"></span><span id="5v"></span>

<span data-ttu-id="22c5c-483">**5V** (3)</span><span class="sxs-lookup"><span data-stu-id="22c5c-483">**5V** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="12V"></span><span id="12v"></span>

<span data-ttu-id="22c5c-484">**12V** (4)</span><span class="sxs-lookup"><span data-stu-id="22c5c-484">**12V** (4)</span></span>


<span data-ttu-id="22c5c-485"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="22c5c-485"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="22c5c-486">Comentários</span><span class="sxs-lookup"><span data-stu-id="22c5c-486">Remarks</span></span>

<span data-ttu-id="22c5c-487">A classe **Win32 \_ SystemSlot** é derivada do [**\_ slot CIM**](cim-slot.md).</span><span class="sxs-lookup"><span data-stu-id="22c5c-487">The **Win32\_SystemSlot** class is derived from [**CIM\_Slot**](cim-slot.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22c5c-488">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22c5c-488">Requirements</span></span>



| <span data-ttu-id="22c5c-489">Requisito</span><span class="sxs-lookup"><span data-stu-id="22c5c-489">Requirement</span></span> | <span data-ttu-id="22c5c-490">Valor</span><span class="sxs-lookup"><span data-stu-id="22c5c-490">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="22c5c-491">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22c5c-491">Minimum supported client</span></span><br/> | <span data-ttu-id="22c5c-492">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22c5c-492">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="22c5c-493">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="22c5c-493">Minimum supported server</span></span><br/> | <span data-ttu-id="22c5c-494">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="22c5c-494">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="22c5c-495">Namespace</span><span class="sxs-lookup"><span data-stu-id="22c5c-495">Namespace</span></span><br/>                | <span data-ttu-id="22c5c-496">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="22c5c-496">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="22c5c-497">MOF</span><span class="sxs-lookup"><span data-stu-id="22c5c-497">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22c5c-498"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22c5c-498"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="22c5c-499">DLL</span><span class="sxs-lookup"><span data-stu-id="22c5c-499">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22c5c-500"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22c5c-500"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22c5c-501">Confira também</span><span class="sxs-lookup"><span data-stu-id="22c5c-501">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c5c-502">**\_Slot CIM**</span><span class="sxs-lookup"><span data-stu-id="22c5c-502">**CIM\_Slot**</span></span>](cim-slot.md)
</dt> <dt>

[<span data-ttu-id="22c5c-503">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="22c5c-503">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
