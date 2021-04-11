---
description: A \_ classe WMI PortConnector do Win32 representa portas de conexão física, como DB-25 Pin masculino, Centronics ou PS/2.
ms.assetid: 85788d1d-0641-4dba-b4ae-a84eb6c4992a
ms.tgt_platform: multiple
title: Classe Win32_PortConnector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortConnector
- Win32_PortConnector.Caption
- Win32_PortConnector.ConnectorPinout
- Win32_PortConnector.ConnectorType
- Win32_PortConnector.CreationClassName
- Win32_PortConnector.Description
- Win32_PortConnector.ExternalReferenceDesignator
- Win32_PortConnector.InstallDate
- Win32_PortConnector.InternalReferenceDesignator
- Win32_PortConnector.Manufacturer
- Win32_PortConnector.Model
- Win32_PortConnector.Name
- Win32_PortConnector.OtherIdentifyingInfo
- Win32_PortConnector.PartNumber
- Win32_PortConnector.PortType
- Win32_PortConnector.PoweredOn
- Win32_PortConnector.SerialNumber
- Win32_PortConnector.SKU
- Win32_PortConnector.Status
- Win32_PortConnector.Tag
- Win32_PortConnector.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dcf9eea51d3a65ad07879cca3e47ae79bde92d53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163926"
---
# <a name="win32_portconnector-class"></a><span data-ttu-id="1934d-103">\_Classe Win32 PortConnector</span><span class="sxs-lookup"><span data-stu-id="1934d-103">Win32\_PortConnector class</span></span>

<span data-ttu-id="1934d-104">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PortConnector do Win32** representa portas de conexão física, como DB-25 Pin masculino, Centronics ou PS/2.</span><span class="sxs-lookup"><span data-stu-id="1934d-104">The **Win32\_PortConnector** [WMI class](../wmisdk/retrieving-a-class.md) represents physical connection ports, such as DB-25 pin male, Centronics, or PS/2.</span></span>

<span data-ttu-id="1934d-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1934d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1934d-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1934d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1934d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1934d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B92-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_PortConnector : CIM_PhysicalConnector
{
  string   Caption;
  string   ConnectorPinout;
  uint16   ConnectorType[];
  string   CreationClassName;
  string   Description;
  string   ExternalReferenceDesignator;
  datetime InstallDate;
  string   InternalReferenceDesignator;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  uint16   PortType;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Status;
  string   Tag;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="1934d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1934d-108">Members</span></span>

<span data-ttu-id="1934d-109">A classe **Win32 \_ PortConnector** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1934d-109">The **Win32\_PortConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="1934d-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1934d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1934d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1934d-111">Properties</span></span>

<span data-ttu-id="1934d-112">A classe **Win32 \_ PortConnector** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1934d-112">The **Win32\_PortConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1934d-113">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1934d-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-116">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1934d-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1934d-117">Breve descrição do objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="1934d-117">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="1934d-118">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1934d-119">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="1934d-119">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-120">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1934d-122">Fixar a configuração e o uso do sinal de um conector físico.</span><span class="sxs-lookup"><span data-stu-id="1934d-122">Pin configuration and signal usage of a physical connector.</span></span>

<span data-ttu-id="1934d-123">Essa propriedade é herdada do [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-123">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

</dd> <dt>

<span data-ttu-id="1934d-124">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="1934d-124">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-125">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1934d-125">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1934d-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-127">Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("tipo de conector do SMBIOS \| tipo 8 \| interno/externo")</span><span class="sxs-lookup"><span data-stu-id="1934d-127">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("ConnectorType"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Internal/External Connector Type")</span></span>
</dt> </dl>

<span data-ttu-id="1934d-128">Matriz de atributos físicos do conector usado por esta porta.</span><span class="sxs-lookup"><span data-stu-id="1934d-128">Array of physical attributes of the connector used by this port.</span></span>

<span data-ttu-id="1934d-129">Essa propriedade é herdada do [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-129">This property is inherited from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span> <span data-ttu-id="1934d-130">A lista a seguir lista os valores.</span><span class="sxs-lookup"><span data-stu-id="1934d-130">The following list lists the values.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1934d-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1934d-131"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1934d-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1934d-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="1934d-133"><span id="Male"></span><span id="male"></span><span id="MALE"></span>**Masculino** (2)</span><span class="sxs-lookup"><span data-stu-id="1934d-133"><span id="Male"></span><span id="male"></span><span id="MALE"></span>**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="1934d-134"><span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**Fêmea** (3)</span><span class="sxs-lookup"><span data-stu-id="1934d-134"><span id="Female"></span><span id="female"></span><span id="FEMALE"></span>**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="1934d-135"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Blindado** (4)</span><span class="sxs-lookup"><span data-stu-id="1934d-135"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="1934d-136"><span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>Não **blindado** (5)</span><span class="sxs-lookup"><span data-stu-id="1934d-136"><span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="1934d-137"><span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI (A) High-Density (50 Pins)** (6)</span><span class="sxs-lookup"><span data-stu-id="1934d-137"><span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="1934d-138"><span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI (A) Low-Density (50 Pins)** (7)</span><span class="sxs-lookup"><span data-stu-id="1934d-138"><span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="1934d-139"><span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**SCSI (P) High-Density (68 Pins)** (8)</span><span class="sxs-lookup"><span data-stu-id="1934d-139"><span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="1934d-140"><span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 pinos)** (9)</span><span class="sxs-lookup"><span data-stu-id="1934d-140"><span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="1934d-141"><span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 pinos)** (10)</span><span class="sxs-lookup"><span data-stu-id="1934d-141"><span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="1934d-142"><span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**Fibre Channel SCSI (DB-9, cobre)** (11)</span><span class="sxs-lookup"><span data-stu-id="1934d-142"><span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="1934d-143"><span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**SCSI Fibre Channel (Fibre)** (12)</span><span class="sxs-lookup"><span data-stu-id="1934d-143"><span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="1934d-144"><span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI Fibre Channel SCA-II (40 pinos)** (13)</span><span class="sxs-lookup"><span data-stu-id="1934d-144"><span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="1934d-145"><span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI Fibre Channel SCA-II (20 pinos)** (14)</span><span class="sxs-lookup"><span data-stu-id="1934d-145"><span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="1934d-146"><span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI Fibre Channel BNC** (15)</span><span class="sxs-lookup"><span data-stu-id="1934d-146"><span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="1934d-147"><span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 polegada (40 pinos)** (16)</span><span class="sxs-lookup"><span data-stu-id="1934d-147"><span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="1934d-148"><span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 polegada (44 pinos)** (17)</span><span class="sxs-lookup"><span data-stu-id="1934d-148"><span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="1934d-149"><span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="1934d-149"><span id="ATA-2"></span><span id="ata-2"></span>**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="1934d-150"><span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="1934d-150"><span id="ATA-3"></span><span id="ata-3"></span>**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="1934d-151"><span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="1934d-151"><span id="ATA_66"></span><span id="ata_66"></span>**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="1934d-152"><span id="DB-9"></span><span id="db-9"></span>**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="1934d-152"><span id="DB-9"></span><span id="db-9"></span>**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="1934d-153"><span id="DB-15"></span><span id="db-15"></span>**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="1934d-153"><span id="DB-15"></span><span id="db-15"></span>**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="1934d-154"><span id="DB-25"></span><span id="db-25"></span>**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="1934d-154"><span id="DB-25"></span><span id="db-25"></span>**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="1934d-155"><span id="DB-36"></span><span id="db-36"></span>**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="1934d-155"><span id="DB-36"></span><span id="db-36"></span>**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="1934d-156"><span id="RS-232C"></span><span id="rs-232c"></span>**RS-232C** (25)</span><span class="sxs-lookup"><span data-stu-id="1934d-156"><span id="RS-232C"></span><span id="rs-232c"></span>**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="1934d-157"><span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="1934d-157"><span id="RS-422"></span><span id="rs-422"></span>**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="1934d-158"><span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="1934d-158"><span id="RS-423"></span><span id="rs-423"></span>**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="1934d-159"><span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="1934d-159"><span id="RS-485"></span><span id="rs-485"></span>**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="1934d-160"><span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="1934d-160"><span id="RS-449"></span><span id="rs-449"></span>**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="1934d-161"><span id="v.35"></span>**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="1934d-161"><span id="v.35"></span>**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="1934d-162"><span id="x.21"></span>**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="1934d-162"><span id="x.21"></span>**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="1934d-163"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="1934d-163"><span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="1934d-164"><span id="AUI"></span><span id="aui"></span>**AUI** (33)</span><span class="sxs-lookup"><span data-stu-id="1934d-164"><span id="AUI"></span><span id="aui"></span>**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="1934d-165"><span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**UTP categoria 3** (34)</span><span class="sxs-lookup"><span data-stu-id="1934d-165"><span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="1934d-166"><span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP categoria 4** (35)</span><span class="sxs-lookup"><span data-stu-id="1934d-166"><span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="1934d-167"><span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**UTP categoria 5** (36)</span><span class="sxs-lookup"><span data-stu-id="1934d-167"><span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="1934d-168"><span id="BNC"></span><span id="bnc"></span>**BNC** (37)</span><span class="sxs-lookup"><span data-stu-id="1934d-168"><span id="BNC"></span><span id="bnc"></span>**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="1934d-169"><span id="RJ11"></span><span id="rj11"></span>**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="1934d-169"><span id="RJ11"></span><span id="rj11"></span>**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="1934d-170"><span id="RJ45"></span><span id="rj45"></span>**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="1934d-170"><span id="RJ45"></span><span id="rj45"></span>**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="1934d-171"><span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**MIC de fibra** (40)</span><span class="sxs-lookup"><span data-stu-id="1934d-171"><span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="1934d-172"><span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**Apple AUI** (41)</span><span class="sxs-lookup"><span data-stu-id="1934d-172"><span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="1934d-173"><span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Apple GeoPort** (42)</span><span class="sxs-lookup"><span data-stu-id="1934d-173"><span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="1934d-174"><span id="PCI"></span><span id="pci"></span>**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="1934d-174"><span id="PCI"></span><span id="pci"></span>**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="1934d-175"><span id="ISA"></span><span id="isa"></span>**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="1934d-175"><span id="ISA"></span><span id="isa"></span>**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="1934d-176"><span id="EISA"></span><span id="eisa"></span>**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="1934d-176"><span id="EISA"></span><span id="eisa"></span>**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="1934d-177"><span id="VESA"></span><span id="vesa"></span>**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="1934d-177"><span id="VESA"></span><span id="vesa"></span>**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="1934d-178"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="1934d-178"><span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="1934d-179"><span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**Tipo de PCMCIA I** (48)</span><span class="sxs-lookup"><span data-stu-id="1934d-179"><span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="1934d-180"><span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**PCMCIA tipo II** (49)</span><span class="sxs-lookup"><span data-stu-id="1934d-180"><span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="1934d-181"><span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**Tipo de PCMCIA III** (50)</span><span class="sxs-lookup"><span data-stu-id="1934d-181"><span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="1934d-182"><span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**Porta ZV** (51)</span><span class="sxs-lookup"><span data-stu-id="1934d-182"><span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="1934d-183"><span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="1934d-183"><span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="1934d-184"><span id="USB"></span><span id="usb"></span>**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="1934d-184"><span id="USB"></span><span id="usb"></span>**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="1934d-185"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="1934d-185"><span id="IEEE_1394"></span><span id="ieee_1394"></span>**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="1934d-186"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (55)</span><span class="sxs-lookup"><span data-stu-id="1934d-186"><span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="1934d-187"><span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**HSSDC (6 pinos)** (56)</span><span class="sxs-lookup"><span data-stu-id="1934d-187"><span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="1934d-188"><span id="GBIC"></span><span id="gbic"></span>**GBIC** (57)</span><span class="sxs-lookup"><span data-stu-id="1934d-188"><span id="GBIC"></span><span id="gbic"></span>**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="1934d-189"><span id="DIN"></span><span id="din"></span>**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="1934d-189"><span id="DIN"></span><span id="din"></span>**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="1934d-190"><span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**Mini-DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="1934d-190"><span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="1934d-191"><span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="1934d-191"><span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="1934d-192"><span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="1934d-192"><span id="PS_2"></span><span id="ps_2"></span>**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="1934d-193"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infravermelho** (62)</span><span class="sxs-lookup"><span data-stu-id="1934d-193"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="1934d-194"><span id="HP-HIL"></span><span id="hp-hil"></span>**HP-Hil** (63)</span><span class="sxs-lookup"><span data-stu-id="1934d-194"><span id="HP-HIL"></span><span id="hp-hil"></span>**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="1934d-195"><span id="access.bus"></span><span id="ACCESS.BUS"></span>**Access. Bus** (64)</span><span class="sxs-lookup"><span data-stu-id="1934d-195"><span id="access.bus"></span><span id="ACCESS.BUS"></span>**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="1934d-196"><span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**NuBus** (65)</span><span class="sxs-lookup"><span data-stu-id="1934d-196"><span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="1934d-197"><span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Centronics** (66)</span><span class="sxs-lookup"><span data-stu-id="1934d-197"><span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="1934d-198"><span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**Mini-Centronics** (67)</span><span class="sxs-lookup"><span data-stu-id="1934d-198"><span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="1934d-199"><span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**Tipo de mini-Centronics-14** (68)</span><span class="sxs-lookup"><span data-stu-id="1934d-199"><span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="1934d-200"><span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**Tipo de mini-Centronics-20** (69)</span><span class="sxs-lookup"><span data-stu-id="1934d-200"><span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="1934d-201"><span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**Tipo de mini-Centronics-26** (70)</span><span class="sxs-lookup"><span data-stu-id="1934d-201"><span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="1934d-202"><span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**Mouse de barramento** (71)</span><span class="sxs-lookup"><span data-stu-id="1934d-202"><span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="1934d-203"><span id="ADB"></span><span id="adb"></span>**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="1934d-203"><span id="ADB"></span><span id="adb"></span>**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="1934d-204"><span id="AGP"></span><span id="agp"></span>**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="1934d-204"><span id="AGP"></span><span id="agp"></span>**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="1934d-205"><span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**Barramento de VM** (74)</span><span class="sxs-lookup"><span data-stu-id="1934d-205"><span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="1934d-206"><span id="VME64"></span><span id="vme64"></span>**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="1934d-206"><span id="VME64"></span><span id="vme64"></span>**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="1934d-207"><span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**Proprietário** (76)</span><span class="sxs-lookup"><span data-stu-id="1934d-207"><span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="1934d-208"><span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**Slot do cartão de processador proprietário** (77)</span><span class="sxs-lookup"><span data-stu-id="1934d-208"><span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="1934d-209"><span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>**Slot de placa de memória proprietária** (78)</span><span class="sxs-lookup"><span data-stu-id="1934d-209"><span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="1934d-210"><span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**Slot de riser de e/s proprietário** (79)</span><span class="sxs-lookup"><span data-stu-id="1934d-210"><span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="1934d-211"><span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66MHZ** (80)</span><span class="sxs-lookup"><span data-stu-id="1934d-211"><span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="1934d-212"><span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="1934d-212"><span id="AGP2X"></span><span id="agp2x"></span>**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="1934d-213"><span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="1934d-213"><span id="AGP4X"></span><span id="agp4x"></span>**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="1934d-214"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="1934d-214"><span id="PC-98"></span><span id="pc-98"></span>**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>

<span data-ttu-id="1934d-215"><span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98Hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="1934d-215"><span id="PC-98Hireso"></span><span id="pc-98hireso"></span><span id="PC-98HIRESO"></span>**PC-98Hireso** (84)</span></span>


</dt> <dd>

<span data-ttu-id="1934d-216">PC-98-Hireso</span><span class="sxs-lookup"><span data-stu-id="1934d-216">PC-98-Hireso</span></span>

</dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="1934d-217"><span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="1934d-217"><span id="PC-H98"></span><span id="pc-h98"></span>**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="1934d-218"><span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="1934d-218"><span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="1934d-219"><span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="1934d-219"><span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

<span data-ttu-id="1934d-220"><span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**Mini-tomada** (88)</span><span class="sxs-lookup"><span data-stu-id="1934d-220"><span id="Mini-Jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>**Mini-Jack** (88)</span></span>


</dt> <dd>

<span data-ttu-id="1934d-221">ADAPTADOR SSA SCSI</span><span class="sxs-lookup"><span data-stu-id="1934d-221">SSA SCSI</span></span>

</dd> <dt>

<span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>

<span data-ttu-id="1934d-222"><span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**Disquete de placa** (89)</span><span class="sxs-lookup"><span data-stu-id="1934d-222"><span id="On_Board_Floppy"></span><span id="on_board_floppy"></span><span id="ON_BOARD_FLOPPY"></span>**On Board Floppy** (89)</span></span>


</dt> <dd>

<span data-ttu-id="1934d-223">Circular</span><span class="sxs-lookup"><span data-stu-id="1934d-223">Circular</span></span>

</dd> <dt>

<span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>

<span data-ttu-id="1934d-224"><span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**9 pinos em linha dupla (pino 10 recortado)** (90)</span><span class="sxs-lookup"><span data-stu-id="1934d-224"><span id="9_Pin_Dual_Inline__pin_10_cut_"></span><span id="9_pin_dual_inline__pin_10_cut_"></span><span id="9_PIN_DUAL_INLINE__PIN_10_CUT_"></span>**9 Pin Dual Inline (pin 10 cut)** (90)</span></span>


</dt> <dd>

<span data-ttu-id="1934d-225">Conector IDE integrado</span><span class="sxs-lookup"><span data-stu-id="1934d-225">On Board IDE Connector</span></span>

</dd> <dt>

<span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>

<span data-ttu-id="1934d-226"><span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**25 pinos em linha dupla (pino 26 recortado)** (91)</span><span class="sxs-lookup"><span data-stu-id="1934d-226"><span id="25_Pin_Dual_Inline__pin_26_cut_"></span><span id="25_pin_dual_inline__pin_26_cut_"></span><span id="25_PIN_DUAL_INLINE__PIN_26_CUT_"></span>**25 Pin Dual Inline (pin 26 cut)** (91)</span></span>


</dt> <dd>

<span data-ttu-id="1934d-227">Conector de disquete de placa</span><span class="sxs-lookup"><span data-stu-id="1934d-227">On Board Floppy Connector</span></span>

</dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

<span data-ttu-id="1934d-228"><span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**50 Pin Dual inline** (92)</span><span class="sxs-lookup"><span data-stu-id="1934d-228"><span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>**50 Pin Dual Inline** (92)</span></span>


</dt> <dd>

<span data-ttu-id="1934d-229">9 pinos em linha dupla</span><span class="sxs-lookup"><span data-stu-id="1934d-229">9 Pin Dual Inline</span></span>

</dd> <dt>

<span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>

<span data-ttu-id="1934d-230"><span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**68 PIN Dual inline** (93)</span><span class="sxs-lookup"><span data-stu-id="1934d-230"><span id="68_Pin__Dual_Inline"></span><span id="68_pin__dual_inline"></span><span id="68_PIN__DUAL_INLINE"></span>**68 Pin Dual Inline** (93)</span></span>


</dt> <dd>

<span data-ttu-id="1934d-231">25 pinos em linha dupla</span><span class="sxs-lookup"><span data-stu-id="1934d-231">25 Pin Dual Inline</span></span>

</dd> <dt>

<span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>

<span data-ttu-id="1934d-232"><span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**Entrada de som de placa do CD-ROM** (94)</span><span class="sxs-lookup"><span data-stu-id="1934d-232"><span id="On_Board_Sound_Input_from_CD-ROM"></span><span id="on_board_sound_input_from_cd-rom"></span><span id="ON_BOARD_SOUND_INPUT_FROM_CD-ROM"></span>**On Board Sound Input from CD-ROM** (94)</span></span>


</dt> <dd>

<span data-ttu-id="1934d-233">50 pino duplo embutido</span><span class="sxs-lookup"><span data-stu-id="1934d-233">50 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="1934d-234">95</span><span class="sxs-lookup"><span data-stu-id="1934d-234">95</span></span>
</dt> <dd>

<span data-ttu-id="1934d-235">68 pino duplo embutido</span><span class="sxs-lookup"><span data-stu-id="1934d-235">68 Pin Dual Inline</span></span>

</dd> <dt>

<span data-ttu-id="1934d-236">96</span><span class="sxs-lookup"><span data-stu-id="1934d-236">96</span></span>
</dt> <dd>

<span data-ttu-id="1934d-237">Conector de som do quadro</span><span class="sxs-lookup"><span data-stu-id="1934d-237">On Board Sound Connector</span></span>

</dd> <dt>

<span data-ttu-id="1934d-238">97</span><span class="sxs-lookup"><span data-stu-id="1934d-238">97</span></span>
</dt> <dd>

<span data-ttu-id="1934d-239">Mini-Jack</span><span class="sxs-lookup"><span data-stu-id="1934d-239">Mini-Jack</span></span>

</dd> <dt>

<span data-ttu-id="1934d-240">98</span><span class="sxs-lookup"><span data-stu-id="1934d-240">98</span></span>
</dt> <dd>

<span data-ttu-id="1934d-241">PCI-X</span><span class="sxs-lookup"><span data-stu-id="1934d-241">PCI-X</span></span>

</dd> <dt>

<span data-ttu-id="1934d-242">99</span><span class="sxs-lookup"><span data-stu-id="1934d-242">99</span></span>
</dt> <dd>

<span data-ttu-id="1934d-243">Sbus IEEE 1396-1993 32 bit</span><span class="sxs-lookup"><span data-stu-id="1934d-243">Sbus IEEE 1396-1993 32 Bit</span></span>

</dd> <dt>

<span data-ttu-id="1934d-244">100</span><span class="sxs-lookup"><span data-stu-id="1934d-244">100</span></span>
</dt> <dd>

<span data-ttu-id="1934d-245">Sbus IEEE 1396-1993 64 bit</span><span class="sxs-lookup"><span data-stu-id="1934d-245">Sbus IEEE 1396-1993 64 Bit</span></span>

</dd> <dt>

<span data-ttu-id="1934d-246">101</span><span class="sxs-lookup"><span data-stu-id="1934d-246">101</span></span>
</dt> <dd>

<span data-ttu-id="1934d-247">MCA</span><span class="sxs-lookup"><span data-stu-id="1934d-247">MCA</span></span>

</dd> <dt>

<span data-ttu-id="1934d-248">102</span><span class="sxs-lookup"><span data-stu-id="1934d-248">102</span></span>
</dt> <dd>

<span data-ttu-id="1934d-249">GIO</span><span class="sxs-lookup"><span data-stu-id="1934d-249">GIO</span></span>

</dd> <dt>

<span data-ttu-id="1934d-250">103</span><span class="sxs-lookup"><span data-stu-id="1934d-250">103</span></span>
</dt> <dd>

<span data-ttu-id="1934d-251">XIO</span><span class="sxs-lookup"><span data-stu-id="1934d-251">XIO</span></span>

</dd> <dt>

<span data-ttu-id="1934d-252">104</span><span class="sxs-lookup"><span data-stu-id="1934d-252">104</span></span>
</dt> <dd>

<span data-ttu-id="1934d-253">HIO</span><span class="sxs-lookup"><span data-stu-id="1934d-253">HIO</span></span>

</dd> <dt>

<span data-ttu-id="1934d-254">105</span><span class="sxs-lookup"><span data-stu-id="1934d-254">105</span></span>
</dt> <dd>

<span data-ttu-id="1934d-255">NGIO</span><span class="sxs-lookup"><span data-stu-id="1934d-255">NGIO</span></span>

</dd> <dt>

<span data-ttu-id="1934d-256">106</span><span class="sxs-lookup"><span data-stu-id="1934d-256">106</span></span>
</dt> <dd>

<span data-ttu-id="1934d-257">PMC</span><span class="sxs-lookup"><span data-stu-id="1934d-257">PMC</span></span>

</dd> <dt>

<span data-ttu-id="1934d-258">107</span><span class="sxs-lookup"><span data-stu-id="1934d-258">107</span></span>
</dt> <dd>

<span data-ttu-id="1934d-259">MTRJ</span><span class="sxs-lookup"><span data-stu-id="1934d-259">MTRJ</span></span>

</dd> <dt>

<span data-ttu-id="1934d-260">108</span><span class="sxs-lookup"><span data-stu-id="1934d-260">108</span></span>
</dt> <dd>

<span data-ttu-id="1934d-261">VF-45</span><span class="sxs-lookup"><span data-stu-id="1934d-261">VF-45</span></span>

</dd> <dt>

<span data-ttu-id="1934d-262">109</span><span class="sxs-lookup"><span data-stu-id="1934d-262">109</span></span>
</dt> <dd>

<span data-ttu-id="1934d-263">E/s futura</span><span class="sxs-lookup"><span data-stu-id="1934d-263">Future I/O</span></span>

</dd> <dt>

<span data-ttu-id="1934d-264">110</span><span class="sxs-lookup"><span data-stu-id="1934d-264">110</span></span>
</dt> <dd>

<span data-ttu-id="1934d-265">SC</span><span class="sxs-lookup"><span data-stu-id="1934d-265">SC</span></span>

</dd> <dt>

<span data-ttu-id="1934d-266">111</span><span class="sxs-lookup"><span data-stu-id="1934d-266">111</span></span>
</dt> <dd>

<span data-ttu-id="1934d-267">SG</span><span class="sxs-lookup"><span data-stu-id="1934d-267">SG</span></span>

</dd> <dt>

<span data-ttu-id="1934d-268">112</span><span class="sxs-lookup"><span data-stu-id="1934d-268">112</span></span>
</dt> <dd>

<span data-ttu-id="1934d-269">Elétrica</span><span class="sxs-lookup"><span data-stu-id="1934d-269">Electrical</span></span>

</dd> <dt>

<span data-ttu-id="1934d-270">113</span><span class="sxs-lookup"><span data-stu-id="1934d-270">113</span></span>
</dt> <dd>

<span data-ttu-id="1934d-271">Unidades</span><span class="sxs-lookup"><span data-stu-id="1934d-271">Optical</span></span>

</dd> <dt>

<span data-ttu-id="1934d-272">114</span><span class="sxs-lookup"><span data-stu-id="1934d-272">114</span></span>
</dt> <dd>

<span data-ttu-id="1934d-273">Faixa de opções</span><span class="sxs-lookup"><span data-stu-id="1934d-273">Ribbon</span></span>

</dd> <dt>

<span data-ttu-id="1934d-274">115</span><span class="sxs-lookup"><span data-stu-id="1934d-274">115</span></span>
</dt> <dd>

<span data-ttu-id="1934d-275">GLM</span><span class="sxs-lookup"><span data-stu-id="1934d-275">GLM</span></span>

</dd> <dt>

<span data-ttu-id="1934d-276">116</span><span class="sxs-lookup"><span data-stu-id="1934d-276">116</span></span>
</dt> <dd>

<span data-ttu-id="1934d-277">1x9</span><span class="sxs-lookup"><span data-stu-id="1934d-277">1x9</span></span>

</dd> <dt>

<span data-ttu-id="1934d-278">117</span><span class="sxs-lookup"><span data-stu-id="1934d-278">117</span></span>
</dt> <dd>

<span data-ttu-id="1934d-279">Mini SG</span><span class="sxs-lookup"><span data-stu-id="1934d-279">Mini SG</span></span>

</dd> <dt>

<span data-ttu-id="1934d-280">118</span><span class="sxs-lookup"><span data-stu-id="1934d-280">118</span></span>
</dt> <dd>

<span data-ttu-id="1934d-281">LC</span><span class="sxs-lookup"><span data-stu-id="1934d-281">LC</span></span>

</dd> <dt>

<span data-ttu-id="1934d-282">119</span><span class="sxs-lookup"><span data-stu-id="1934d-282">119</span></span>
</dt> <dd>

<span data-ttu-id="1934d-283">HSSC</span><span class="sxs-lookup"><span data-stu-id="1934d-283">HSSC</span></span>

</dd> <dt>

<span data-ttu-id="1934d-284">120</span><span class="sxs-lookup"><span data-stu-id="1934d-284">120</span></span>
</dt> <dd>

<span data-ttu-id="1934d-285">VHDCI blindado (68 pinos)</span><span class="sxs-lookup"><span data-stu-id="1934d-285">VHDCI Shielded (68 pins)</span></span>

</dd> <dt>

<span data-ttu-id="1934d-286">121</span><span class="sxs-lookup"><span data-stu-id="1934d-286">121</span></span>
</dt> <dd>

<span data-ttu-id="1934d-287">InfiniBand</span><span class="sxs-lookup"><span data-stu-id="1934d-287">InfiniBand</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1934d-288">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1934d-288">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-289">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-290">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-290">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-291">Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1934d-291">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1934d-292">Nome da primeira classe concreta que aparece na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="1934d-292">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="1934d-293">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="1934d-293">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="1934d-294">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-294">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1934d-295">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1934d-295">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-296">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-296">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-297">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-297">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-298">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="1934d-298">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1934d-299">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="1934d-299">Description of the object.</span></span>

<span data-ttu-id="1934d-300">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-300">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1934d-301">**ExternalReferenceDesignator**</span><span class="sxs-lookup"><span data-stu-id="1934d-301">**ExternalReferenceDesignator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-302">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-302">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-303">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-303">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-304">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS \| Type 8 \| external Reference designation")</span><span class="sxs-lookup"><span data-stu-id="1934d-304">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|External Reference Designator")</span></span>
</dt> </dl>

<span data-ttu-id="1934d-305">Designador de referência externa da porta.</span><span class="sxs-lookup"><span data-stu-id="1934d-305">External reference designator of the port.</span></span> <span data-ttu-id="1934d-306">Os designadores de referência externa são identificadores que determinam o tipo e o uso da porta.</span><span class="sxs-lookup"><span data-stu-id="1934d-306">External reference designators are identifiers that determine the type and use of the port.</span></span>

<span data-ttu-id="1934d-307">Exemplo: "COM1"</span><span class="sxs-lookup"><span data-stu-id="1934d-307">Example: "COM1"</span></span>

</dd> <dt>

<span data-ttu-id="1934d-308">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1934d-308">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-309">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1934d-309">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-310">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-310">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-311">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="1934d-311">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1934d-312">Data e hora em que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="1934d-312">Date and time the object is installed.</span></span> <span data-ttu-id="1934d-313">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="1934d-313">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1934d-314">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-314">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1934d-315">**InternalReferenceDesignator**</span><span class="sxs-lookup"><span data-stu-id="1934d-315">**InternalReferenceDesignator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-316">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-318">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo de referência interna do SMBIOS Type 8 \| ")</span><span class="sxs-lookup"><span data-stu-id="1934d-318">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Internal Reference Designator")</span></span>
</dt> </dl>

<span data-ttu-id="1934d-319">Designador de referência interna da porta.</span><span class="sxs-lookup"><span data-stu-id="1934d-319">Internal reference designator of the port.</span></span> <span data-ttu-id="1934d-320">Os designadores de referência internos são específicos para o fabricante e identificam o local da placa de circuito ou o uso da porta.</span><span class="sxs-lookup"><span data-stu-id="1934d-320">Internal reference designators are specific to the manufacturer, and identify the circuit board location or use of the port.</span></span>

<span data-ttu-id="1934d-321">Exemplo: "J101"</span><span class="sxs-lookup"><span data-stu-id="1934d-321">Example: "J101"</span></span>

</dd> <dt>

<span data-ttu-id="1934d-322">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="1934d-322">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-323">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-323">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-324">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-324">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-325">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1934d-325">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1934d-326">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1934d-326">Name of the organization responsible for producing the physical element.</span></span>

<span data-ttu-id="1934d-327">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-327">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1934d-328">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="1934d-328">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-329">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-330">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-331">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1934d-331">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1934d-332">Nome do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1934d-332">Name for the physical element.</span></span>

<span data-ttu-id="1934d-333">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-333">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1934d-334">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1934d-334">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-335">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-335">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-336">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-336">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-337">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="1934d-337">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1934d-338">Rótulo do objeto.</span><span class="sxs-lookup"><span data-stu-id="1934d-338">Label for the object.</span></span> <span data-ttu-id="1934d-339">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="1934d-339">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="1934d-340">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-340">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1934d-341">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="1934d-341">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-342">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-342">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-343">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-343">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1934d-344">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1934d-344">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="1934d-345">Um exemplo são os dados de código de barras associados a um elemento que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="1934d-345">One example is bar code data associated with an element that also has an asset tag.</span></span> <span data-ttu-id="1934d-346">Se apenas os dados de código de barras estiverem disponíveis e exclusivos ou puderem ser usados como uma chave de elemento, essa propriedade será **nula** e os dados de código de barras serão usados como a chave de classe na propriedade de marca.</span><span class="sxs-lookup"><span data-stu-id="1934d-346">If only bar code data is available and unique or able to be used as an element key, this property is **NULL** and the bar code data is used as the class key in the tag property.</span></span>

<span data-ttu-id="1934d-347">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-347">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1934d-348">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="1934d-348">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-349">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-351">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="1934d-351">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="1934d-352">Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1934d-352">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="1934d-353">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-353">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1934d-354">**PortType**</span><span class="sxs-lookup"><span data-stu-id="1934d-354">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-355">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1934d-355">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-357">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| tipo de porta SMBIOS tipo 8 \| ")</span><span class="sxs-lookup"><span data-stu-id="1934d-357">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SMBIOS\|Type 8\|Port Type")</span></span>
</dt> </dl>

<span data-ttu-id="1934d-358">Função da porta.</span><span class="sxs-lookup"><span data-stu-id="1934d-358">Function of the port.</span></span> <span data-ttu-id="1934d-359">A lista a seguir lista os valores.</span><span class="sxs-lookup"><span data-stu-id="1934d-359">The following list lists the values.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="1934d-360">**Nenhum** (0)</span><span class="sxs-lookup"><span data-stu-id="1934d-360">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_XT_AT_Compatible"></span><span id="parallel_port_xt_at_compatible"></span><span id="PARALLEL_PORT_XT_AT_COMPATIBLE"></span>

<span data-ttu-id="1934d-361">**Porta paralela XT/em compatível** (1)</span><span class="sxs-lookup"><span data-stu-id="1934d-361">**Parallel Port XT/AT Compatible** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_PS_2"></span><span id="parallel_port_ps_2"></span><span id="PARALLEL_PORT_PS_2"></span>

<span data-ttu-id="1934d-362">**Porta paralela PS/2** (2)</span><span class="sxs-lookup"><span data-stu-id="1934d-362">**Parallel Port PS/2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP"></span><span id="parallel_port_ecp"></span><span id="PARALLEL_PORT_ECP"></span>

<span data-ttu-id="1934d-363">**Porta paralela ECP** (3)</span><span class="sxs-lookup"><span data-stu-id="1934d-363">**Parallel Port ECP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_EPP"></span><span id="parallel_port_epp"></span><span id="PARALLEL_PORT_EPP"></span>

<span data-ttu-id="1934d-364">**Porta paralela EPP** (4)</span><span class="sxs-lookup"><span data-stu-id="1934d-364">**Parallel Port EPP** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_Port_ECP_EPP"></span><span id="parallel_port_ecp_epp"></span><span id="PARALLEL_PORT_ECP_EPP"></span>

<span data-ttu-id="1934d-365">**Porta paralela ECP/EPP** (5)</span><span class="sxs-lookup"><span data-stu-id="1934d-365">**Parallel Port ECP/EPP** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_XT_AT_Compatible"></span><span id="serial_port_xt_at_compatible"></span><span id="SERIAL_PORT_XT_AT_COMPATIBLE"></span>

<span data-ttu-id="1934d-366">**Porta serial XT/em compatível** (6)</span><span class="sxs-lookup"><span data-stu-id="1934d-366">**Serial Port XT/AT Compatible** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16450_Compatible"></span><span id="serial_port_16450_compatible"></span><span id="SERIAL_PORT_16450_COMPATIBLE"></span>

<span data-ttu-id="1934d-367">**Porta serial compatível com 16450** (7)</span><span class="sxs-lookup"><span data-stu-id="1934d-367">**Serial Port 16450 Compatible** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550_Compatible"></span><span id="serial_port_16550_compatible"></span><span id="SERIAL_PORT_16550_COMPATIBLE"></span>

<span data-ttu-id="1934d-368">**Porta serial compatível com 16550** (8)</span><span class="sxs-lookup"><span data-stu-id="1934d-368">**Serial Port 16550 Compatible** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_Port_16550A_Compatible"></span><span id="serial_port_16550a_compatible"></span><span id="SERIAL_PORT_16550A_COMPATIBLE"></span>

<span data-ttu-id="1934d-369">**Porta serial compatível com 16550A** (9)</span><span class="sxs-lookup"><span data-stu-id="1934d-369">**Serial Port 16550A Compatible** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Port"></span><span id="scsi_port"></span><span id="SCSI_PORT"></span>

<span data-ttu-id="1934d-370">**Porta SCSI** (10)</span><span class="sxs-lookup"><span data-stu-id="1934d-370">**SCSI Port** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="MIDI_Port"></span><span id="midi_port"></span><span id="MIDI_PORT"></span>

<span data-ttu-id="1934d-371">**Porta MIDI** (11)</span><span class="sxs-lookup"><span data-stu-id="1934d-371">**MIDI Port** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Joy_Stick_Port"></span><span id="joy_stick_port"></span><span id="JOY_STICK_PORT"></span>

<span data-ttu-id="1934d-372">**Porta da Joy Stick** (12)</span><span class="sxs-lookup"><span data-stu-id="1934d-372">**Joy Stick Port** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Keyboard_Port"></span><span id="keyboard_port"></span><span id="KEYBOARD_PORT"></span>

<span data-ttu-id="1934d-373">**Porta do teclado** (13)</span><span class="sxs-lookup"><span data-stu-id="1934d-373">**Keyboard Port** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Mouse_Port"></span><span id="mouse_port"></span><span id="MOUSE_PORT"></span>

<span data-ttu-id="1934d-374">**Porta do mouse** (14)</span><span class="sxs-lookup"><span data-stu-id="1934d-374">**Mouse Port** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

<span data-ttu-id="1934d-375">**SSA SCSI** (15)</span><span class="sxs-lookup"><span data-stu-id="1934d-375">**SSA SCSI** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="1934d-376">**USB** (16)</span><span class="sxs-lookup"><span data-stu-id="1934d-376">**USB** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FireWire__IEEE_P1394_"></span><span id="firewire__ieee_p1394_"></span><span id="FIREWIRE__IEEE_P1394_"></span>

<span data-ttu-id="1934d-377">**FireWire (IEEE P1394)** (17)</span><span class="sxs-lookup"><span data-stu-id="1934d-377">**FireWire (IEEE P1394)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="1934d-378">**Tipo de PCMCIA II** (18)</span><span class="sxs-lookup"><span data-stu-id="1934d-378">**PCMCIA Type II** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="1934d-379">**PCMCIA tipo II** (19)</span><span class="sxs-lookup"><span data-stu-id="1934d-379">**PCMCIA Type II** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="1934d-380">**Tipo de PCMCIA III** (20)</span><span class="sxs-lookup"><span data-stu-id="1934d-380">**PCMCIA Type III** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Cardbus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="1934d-381">**CardBus** (21)</span><span class="sxs-lookup"><span data-stu-id="1934d-381">**Cardbus** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Bus_Port"></span><span id="access_bus_port"></span><span id="ACCESS_BUS_PORT"></span>

<span data-ttu-id="1934d-382">**Porta do barramento de acesso** (22)</span><span class="sxs-lookup"><span data-stu-id="1934d-382">**Access Bus Port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_II"></span><span id="scsi_ii"></span>

<span data-ttu-id="1934d-383">**SCSI II** (23)</span><span class="sxs-lookup"><span data-stu-id="1934d-383">**SCSI II** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Wide"></span><span id="scsi_wide"></span><span id="SCSI_WIDE"></span>

<span data-ttu-id="1934d-384">**SCSI largo** (24)</span><span class="sxs-lookup"><span data-stu-id="1934d-384">**SCSI Wide** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="1934d-385">**PC-98** (25)</span><span class="sxs-lookup"><span data-stu-id="1934d-385">**PC-98** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="1934d-386">**PC-98-Hireso** (26)</span><span class="sxs-lookup"><span data-stu-id="1934d-386">**PC-98-Hireso** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="1934d-387">**PC-H98** (27)</span><span class="sxs-lookup"><span data-stu-id="1934d-387">**PC-H98** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Video_Port"></span><span id="video_port"></span><span id="VIDEO_PORT"></span>

<span data-ttu-id="1934d-388">**Porta de vídeo** (28)</span><span class="sxs-lookup"><span data-stu-id="1934d-388">**Video Port** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Audio_Port"></span><span id="audio_port"></span><span id="AUDIO_PORT"></span>

<span data-ttu-id="1934d-389">**Porta de áudio** (29)</span><span class="sxs-lookup"><span data-stu-id="1934d-389">**Audio Port** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Modem_Port"></span><span id="modem_port"></span><span id="MODEM_PORT"></span>

<span data-ttu-id="1934d-390">**Porta do modem** (30)</span><span class="sxs-lookup"><span data-stu-id="1934d-390">**Modem Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Network_Port"></span><span id="network_port"></span><span id="NETWORK_PORT"></span>

<span data-ttu-id="1934d-391">**Porta de rede** (31)</span><span class="sxs-lookup"><span data-stu-id="1934d-391">**Network Port** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

<span data-ttu-id="1934d-392">**compatível com 8251** (32)</span><span class="sxs-lookup"><span data-stu-id="1934d-392">**8251 Compatible** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="8251_FIFO_Compatible"></span><span id="8251_fifo_compatible"></span><span id="8251_FIFO_COMPATIBLE"></span>

<span data-ttu-id="1934d-393">**8251 FIFO compatível** (33)</span><span class="sxs-lookup"><span data-stu-id="1934d-393">**8251 FIFO Compatible** (33)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1934d-394">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="1934d-394">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-395">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1934d-395">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-396">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-396">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1934d-397">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="1934d-397">If **TRUE**, the physical element is powered on.</span></span>

<span data-ttu-id="1934d-398">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-398">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1934d-399">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="1934d-399">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-400">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-400">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-401">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-401">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-402">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1934d-402">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1934d-403">Número alocado pelo fabricante usado para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1934d-403">Manufacturer-allocated number used to identify a physical element.</span></span>

<span data-ttu-id="1934d-404">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-404">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1934d-405">**SKU**</span><span class="sxs-lookup"><span data-stu-id="1934d-405">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-406">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-408">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1934d-408">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1934d-409">Número de unidade de manutenção de estoque para um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1934d-409">Stock keeping unit number for a physical element.</span></span>

<span data-ttu-id="1934d-410">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-410">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1934d-411">**Status**</span><span class="sxs-lookup"><span data-stu-id="1934d-411">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-412">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-412">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-414">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="1934d-414">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1934d-415">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="1934d-415">Current status of the object.</span></span> <span data-ttu-id="1934d-416">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="1934d-416">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="1934d-417">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="1934d-417">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="1934d-418">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="1934d-418">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1934d-419">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="1934d-419">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1934d-420">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="1934d-420">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1934d-421">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-421">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1934d-422">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1934d-422">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1934d-423">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="1934d-423">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1934d-424">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="1934d-424">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1934d-425">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="1934d-425">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1934d-426">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="1934d-426">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1934d-427">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="1934d-427">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1934d-428">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="1934d-428">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1934d-429">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="1934d-429">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1934d-430">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="1934d-430">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1934d-431">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="1934d-431">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1934d-432">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="1934d-432">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1934d-433">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="1934d-433">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1934d-434">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="1934d-434">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1934d-435">**Tag**</span><span class="sxs-lookup"><span data-stu-id="1934d-435">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-436">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-436">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-437">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-437">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-438">Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span><span class="sxs-lookup"><span data-stu-id="1934d-438">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**Override**](../wmisdk/standard-qualifiers.md) ("Tag"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")</span></span>
</dt> </dl>

<span data-ttu-id="1934d-439">Identificador exclusivo de uma conexão de porta no sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="1934d-439">Unique identifier of a port connection on the computer system.</span></span>

<span data-ttu-id="1934d-440">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-440">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="1934d-441">Exemplo: "conector de porta 1"</span><span class="sxs-lookup"><span data-stu-id="1934d-441">Example: "Port Connector 1"</span></span>

</dd> <dt>

<span data-ttu-id="1934d-442">**Versão**</span><span class="sxs-lookup"><span data-stu-id="1934d-442">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1934d-443">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1934d-443">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1934d-444">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1934d-444">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1934d-445">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="1934d-445">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="1934d-446">Versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="1934d-446">Version of the physical element.</span></span>

<span data-ttu-id="1934d-447">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-447">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1934d-448">Comentários</span><span class="sxs-lookup"><span data-stu-id="1934d-448">Remarks</span></span>

<span data-ttu-id="1934d-449">A classe **Win32 \_ PortConnector** é derivada de [**CIM \_ PhysicalConnector**](cim-physicalconnector.md).</span><span class="sxs-lookup"><span data-stu-id="1934d-449">The **Win32\_PortConnector** class is derived from [**CIM\_PhysicalConnector**](cim-physicalconnector.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1934d-450">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1934d-450">Requirements</span></span>



| <span data-ttu-id="1934d-451">Requisito</span><span class="sxs-lookup"><span data-stu-id="1934d-451">Requirement</span></span> | <span data-ttu-id="1934d-452">Valor</span><span class="sxs-lookup"><span data-stu-id="1934d-452">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1934d-453">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1934d-453">Minimum supported client</span></span><br/> | <span data-ttu-id="1934d-454">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1934d-454">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1934d-455">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1934d-455">Minimum supported server</span></span><br/> | <span data-ttu-id="1934d-456">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1934d-456">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1934d-457">Namespace</span><span class="sxs-lookup"><span data-stu-id="1934d-457">Namespace</span></span><br/>                | <span data-ttu-id="1934d-458">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1934d-458">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1934d-459">MOF</span><span class="sxs-lookup"><span data-stu-id="1934d-459">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1934d-460"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1934d-460"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1934d-461">DLL</span><span class="sxs-lookup"><span data-stu-id="1934d-461">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1934d-462"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1934d-462"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1934d-463">Confira também</span><span class="sxs-lookup"><span data-stu-id="1934d-463">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1934d-464">**\_PHYSICALCONNECTOR CIM**</span><span class="sxs-lookup"><span data-stu-id="1934d-464">**CIM\_PhysicalConnector**</span></span>](cim-physicalconnector.md)
</dt> <dt>

[<span data-ttu-id="1934d-465">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="1934d-465">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
