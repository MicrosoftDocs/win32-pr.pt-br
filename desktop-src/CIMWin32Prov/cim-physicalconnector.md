---
description: A \_ classe CIM PhysicalConnector representa qualquer elemento físico que é usado para se conectar a outros elementos. Qualquer objeto que possa se conectar e transmitir sinais ou potência entre dois ou mais elementos físicos é um descendente (ou membro) dessa classe.
ms.assetid: cc135ae8-5ae1-4028-a2e3-a81db8694d9d
ms.tgt_platform: multiple
title: Classe CIM_PhysicalConnector
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalConnector
- CIM_PhysicalConnector.Caption
- CIM_PhysicalConnector.Description
- CIM_PhysicalConnector.InstallDate
- CIM_PhysicalConnector.Name
- CIM_PhysicalConnector.Status
- CIM_PhysicalConnector.CreationClassName
- CIM_PhysicalConnector.Manufacturer
- CIM_PhysicalConnector.Model
- CIM_PhysicalConnector.OtherIdentifyingInfo
- CIM_PhysicalConnector.PartNumber
- CIM_PhysicalConnector.PoweredOn
- CIM_PhysicalConnector.SerialNumber
- CIM_PhysicalConnector.SKU
- CIM_PhysicalConnector.Tag
- CIM_PhysicalConnector.Version
- CIM_PhysicalConnector.ConnectorPinout
- CIM_PhysicalConnector.ConnectorType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 106b8ab30296b77be550809771db3b0208485872
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750327"
---
# <a name="cim_physicalconnector-class"></a><span data-ttu-id="bba11-104">\_Classe CIM PhysicalConnector</span><span class="sxs-lookup"><span data-stu-id="bba11-104">CIM\_PhysicalConnector class</span></span>

<span data-ttu-id="bba11-105">A classe **CIM \_ PhysicalConnector** representa qualquer elemento físico que é usado para se conectar a outros elementos.</span><span class="sxs-lookup"><span data-stu-id="bba11-105">The **CIM\_PhysicalConnector** class represents any physical element that is used to connect to other elements.</span></span> <span data-ttu-id="bba11-106">Qualquer objeto que possa se conectar e transmitir sinais ou potência entre dois ou mais elementos físicos é um descendente (ou membro) dessa classe.</span><span class="sxs-lookup"><span data-stu-id="bba11-106">Any object that can connect and transmit signals or power between two or more physical elements is a descendant (or member) of this class.</span></span> <span data-ttu-id="bba11-107">Por exemplo, slots e conectores D-shell são tipos de conectores físicos.</span><span class="sxs-lookup"><span data-stu-id="bba11-107">For example, slots and D-shell connectors are types of physical connectors.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bba11-108">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="bba11-108">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bba11-109">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bba11-109">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bba11-110">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="bba11-110">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="bba11-111">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="bba11-111">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bba11-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bba11-112">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B84-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalConnector : CIM_PhysicalElement
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
  string   ConnectorPinout;
  uint16   ConnectorType[];
};
```

## <a name="members"></a><span data-ttu-id="bba11-113">Membros</span><span class="sxs-lookup"><span data-stu-id="bba11-113">Members</span></span>

<span data-ttu-id="bba11-114">A classe **CIM \_ PhysicalConnector** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="bba11-114">The **CIM\_PhysicalConnector** class has these types of members:</span></span>

-   [<span data-ttu-id="bba11-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bba11-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bba11-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="bba11-116">Properties</span></span>

<span data-ttu-id="bba11-117">A classe **CIM \_ PhysicalConnector** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="bba11-117">The **CIM\_PhysicalConnector** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bba11-118">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="bba11-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bba11-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba11-121">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="bba11-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="bba11-122">Uma breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="bba11-122">A short textual description of the object.</span></span>

<span data-ttu-id="bba11-123">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba11-124">**ConnectorPinout**</span><span class="sxs-lookup"><span data-stu-id="bba11-124">**ConnectorPinout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bba11-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bba11-127">Cadeia de caracteres de forma livre que descreve a configuração de PIN e o uso de sinal de um conector físico.</span><span class="sxs-lookup"><span data-stu-id="bba11-127">Free-form string that describes the pin configuration and signal use of a physical connector.</span></span>

</dd> <dt>

<span data-ttu-id="bba11-128">**ConnectorType**</span><span class="sxs-lookup"><span data-stu-id="bba11-128">**ConnectorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-129">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="bba11-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="bba11-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bba11-131">Tipo de conector físico.</span><span class="sxs-lookup"><span data-stu-id="bba11-131">Type of physical connector.</span></span> <span data-ttu-id="bba11-132">Uma matriz é especificada para permitir a descrição de combinações de informações do conector.</span><span class="sxs-lookup"><span data-stu-id="bba11-132">An array is specified to allow the description of combinations of connector information.</span></span> <span data-ttu-id="bba11-133">Por exemplo, uma entrada de matriz poderia especificar RS-232, outro DB-25 e uma terceira entrada poderia definir o conector como "masculino".</span><span class="sxs-lookup"><span data-stu-id="bba11-133">For example, one array entry could specify RS-232, another DB-25, and a third entry could define the connector as "male".</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bba11-134">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="bba11-134">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="bba11-135">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="bba11-135">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

<span data-ttu-id="bba11-136">**Masculino** (2)</span><span class="sxs-lookup"><span data-stu-id="bba11-136">**Male** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

<span data-ttu-id="bba11-137">**Fêmea** (3)</span><span class="sxs-lookup"><span data-stu-id="bba11-137">**Female** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="bba11-138">**Blindado** (4)</span><span class="sxs-lookup"><span data-stu-id="bba11-138">**Shielded** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

<span data-ttu-id="bba11-139">Não **blindado** (5)</span><span class="sxs-lookup"><span data-stu-id="bba11-139">**Unshielded** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

<span data-ttu-id="bba11-140">**SCSI (A) High-Density (50 Pins)** (6)</span><span class="sxs-lookup"><span data-stu-id="bba11-140">**SCSI (A) High-Density (50 pins)** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

<span data-ttu-id="bba11-141">**SCSI (A) Low-Density (50 Pins)** (7)</span><span class="sxs-lookup"><span data-stu-id="bba11-141">**SCSI (A) Low-Density (50 pins)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

<span data-ttu-id="bba11-142">**SCSI (P) High-Density (68 Pins)** (8)</span><span class="sxs-lookup"><span data-stu-id="bba11-142">**SCSI (P) High-Density (68 pins)** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

<span data-ttu-id="bba11-143">**SCSI SCA-I (80 pinos)** (9)</span><span class="sxs-lookup"><span data-stu-id="bba11-143">**SCSI SCA-I (80 pins)** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

<span data-ttu-id="bba11-144">**SCSI SCA-II (80 pinos)** (10)</span><span class="sxs-lookup"><span data-stu-id="bba11-144">**SCSI SCA-II (80 pins)** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

<span data-ttu-id="bba11-145">**Fibre Channel SCSI (DB-9, cobre)** (11)</span><span class="sxs-lookup"><span data-stu-id="bba11-145">**SCSI Fibre Channel (DB-9, Copper)** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

<span data-ttu-id="bba11-146">**SCSI Fibre Channel (Fibre)** (12)</span><span class="sxs-lookup"><span data-stu-id="bba11-146">**SCSI Fibre Channel (Fibre)** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

<span data-ttu-id="bba11-147">**SCSI Fibre Channel SCA-II (40 pinos)** (13)</span><span class="sxs-lookup"><span data-stu-id="bba11-147">**SCSI Fibre Channel SCA-II (40 pins)** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

<span data-ttu-id="bba11-148">**SCSI Fibre Channel SCA-II (20 pinos)** (14)</span><span class="sxs-lookup"><span data-stu-id="bba11-148">**SCSI Fibre Channel SCA-II (20 pins)** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

<span data-ttu-id="bba11-149">**SCSI Fibre Channel BNC** (15)</span><span class="sxs-lookup"><span data-stu-id="bba11-149">**SCSI Fibre Channel BNC** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

<span data-ttu-id="bba11-150">**ATA 3-1/2 polegada (40 pinos)** (16)</span><span class="sxs-lookup"><span data-stu-id="bba11-150">**ATA 3-1/2 Inch (40 pins)** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

<span data-ttu-id="bba11-151">**ATA 2-1/2 polegada (44 pinos)** (17)</span><span class="sxs-lookup"><span data-stu-id="bba11-151">**ATA 2-1/2 Inch (44 pins)** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

<span data-ttu-id="bba11-152">**ATA-2** (18)</span><span class="sxs-lookup"><span data-stu-id="bba11-152">**ATA-2** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

<span data-ttu-id="bba11-153">**ATA-3** (19)</span><span class="sxs-lookup"><span data-stu-id="bba11-153">**ATA-3** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

<span data-ttu-id="bba11-154">**ATA/66** (20)</span><span class="sxs-lookup"><span data-stu-id="bba11-154">**ATA/66** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

<span data-ttu-id="bba11-155">**DB-9** (21)</span><span class="sxs-lookup"><span data-stu-id="bba11-155">**DB-9** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

<span data-ttu-id="bba11-156">**DB-15** (22)</span><span class="sxs-lookup"><span data-stu-id="bba11-156">**DB-15** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

<span data-ttu-id="bba11-157">**DB-25** (23)</span><span class="sxs-lookup"><span data-stu-id="bba11-157">**DB-25** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

<span data-ttu-id="bba11-158">**DB-36** (24)</span><span class="sxs-lookup"><span data-stu-id="bba11-158">**DB-36** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

<span data-ttu-id="bba11-159">**RS-232C** (25)</span><span class="sxs-lookup"><span data-stu-id="bba11-159">**RS-232C** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

<span data-ttu-id="bba11-160">**RS-422** (26)</span><span class="sxs-lookup"><span data-stu-id="bba11-160">**RS-422** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

<span data-ttu-id="bba11-161">**RS-423** (27)</span><span class="sxs-lookup"><span data-stu-id="bba11-161">**RS-423** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

<span data-ttu-id="bba11-162">**RS-485** (28)</span><span class="sxs-lookup"><span data-stu-id="bba11-162">**RS-485** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

<span data-ttu-id="bba11-163">**RS-449** (29)</span><span class="sxs-lookup"><span data-stu-id="bba11-163">**RS-449** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

<span data-ttu-id="bba11-164">**V. 35** (30)</span><span class="sxs-lookup"><span data-stu-id="bba11-164">**V.35** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

<span data-ttu-id="bba11-165">**X. 21** (31)</span><span class="sxs-lookup"><span data-stu-id="bba11-165">**X.21** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span data-ttu-id="bba11-166">**IEEE-488** (32)</span><span class="sxs-lookup"><span data-stu-id="bba11-166">**IEEE-488** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

<span data-ttu-id="bba11-167">**AUI** (33)</span><span class="sxs-lookup"><span data-stu-id="bba11-167">**AUI** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

<span data-ttu-id="bba11-168">**UTP categoria 3** (34)</span><span class="sxs-lookup"><span data-stu-id="bba11-168">**UTP Category 3** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

<span data-ttu-id="bba11-169">**UTP categoria 4** (35)</span><span class="sxs-lookup"><span data-stu-id="bba11-169">**UTP Category 4** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

<span data-ttu-id="bba11-170">**UTP categoria 5** (36)</span><span class="sxs-lookup"><span data-stu-id="bba11-170">**UTP Category 5** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

<span data-ttu-id="bba11-171">**BNC** (37)</span><span class="sxs-lookup"><span data-stu-id="bba11-171">**BNC** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

<span data-ttu-id="bba11-172">**RJ11** (38)</span><span class="sxs-lookup"><span data-stu-id="bba11-172">**RJ11** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

<span data-ttu-id="bba11-173">**RJ45** (39)</span><span class="sxs-lookup"><span data-stu-id="bba11-173">**RJ45** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

<span data-ttu-id="bba11-174">**MIC de fibra** (40)</span><span class="sxs-lookup"><span data-stu-id="bba11-174">**Fiber MIC** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

<span data-ttu-id="bba11-175">**Apple AUI** (41)</span><span class="sxs-lookup"><span data-stu-id="bba11-175">**Apple AUI** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

<span data-ttu-id="bba11-176">**Apple GeoPort** (42)</span><span class="sxs-lookup"><span data-stu-id="bba11-176">**Apple GeoPort** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span data-ttu-id="bba11-177">**PCI** (43)</span><span class="sxs-lookup"><span data-stu-id="bba11-177">**PCI** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span data-ttu-id="bba11-178">**ISA** (44)</span><span class="sxs-lookup"><span data-stu-id="bba11-178">**ISA** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span data-ttu-id="bba11-179">**EISA** (45)</span><span class="sxs-lookup"><span data-stu-id="bba11-179">**EISA** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span data-ttu-id="bba11-180">**VESA** (46)</span><span class="sxs-lookup"><span data-stu-id="bba11-180">**VESA** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span data-ttu-id="bba11-181">**PCMCIA** (47)</span><span class="sxs-lookup"><span data-stu-id="bba11-181">**PCMCIA** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

<span data-ttu-id="bba11-182">**Tipo de PCMCIA I** (48)</span><span class="sxs-lookup"><span data-stu-id="bba11-182">**PCMCIA Type I** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

<span data-ttu-id="bba11-183">**PCMCIA tipo II** (49)</span><span class="sxs-lookup"><span data-stu-id="bba11-183">**PCMCIA Type II** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

<span data-ttu-id="bba11-184">**Tipo de PCMCIA III** (50)</span><span class="sxs-lookup"><span data-stu-id="bba11-184">**PCMCIA Type III** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

<span data-ttu-id="bba11-185">**Porta ZV** (51)</span><span class="sxs-lookup"><span data-stu-id="bba11-185">**ZV Port** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

<span data-ttu-id="bba11-186">**CardBus** (52)</span><span class="sxs-lookup"><span data-stu-id="bba11-186">**CardBus** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

<span data-ttu-id="bba11-187">**USB** (53)</span><span class="sxs-lookup"><span data-stu-id="bba11-187">**USB** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

<span data-ttu-id="bba11-188">**IEEE 1394** (54)</span><span class="sxs-lookup"><span data-stu-id="bba11-188">**IEEE 1394** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span data-ttu-id="bba11-189">**HIPPI** (55)</span><span class="sxs-lookup"><span data-stu-id="bba11-189">**HIPPI** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

<span data-ttu-id="bba11-190">**HSSDC (6 pinos)** (56)</span><span class="sxs-lookup"><span data-stu-id="bba11-190">**HSSDC (6 pins)** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

<span data-ttu-id="bba11-191">**GBIC** (57)</span><span class="sxs-lookup"><span data-stu-id="bba11-191">**GBIC** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

<span data-ttu-id="bba11-192">**DIN** (58)</span><span class="sxs-lookup"><span data-stu-id="bba11-192">**DIN** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

<span data-ttu-id="bba11-193">**Mini-DIN** (59)</span><span class="sxs-lookup"><span data-stu-id="bba11-193">**Mini-DIN** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

<span data-ttu-id="bba11-194">**Micro-DIN** (60)</span><span class="sxs-lookup"><span data-stu-id="bba11-194">**Micro-DIN** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

<span data-ttu-id="bba11-195">**PS/2** (61)</span><span class="sxs-lookup"><span data-stu-id="bba11-195">**PS/2** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="bba11-196">**Infravermelho** (62)</span><span class="sxs-lookup"><span data-stu-id="bba11-196">**Infrared** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

<span data-ttu-id="bba11-197">**HP-Hil** (63)</span><span class="sxs-lookup"><span data-stu-id="bba11-197">**HP-HIL** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

<span data-ttu-id="bba11-198">**Access. Bus** (64)</span><span class="sxs-lookup"><span data-stu-id="bba11-198">**Access.bus** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

<span data-ttu-id="bba11-199">**NuBus** (65)</span><span class="sxs-lookup"><span data-stu-id="bba11-199">**NuBus** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

<span data-ttu-id="bba11-200">**Centronics** (66)</span><span class="sxs-lookup"><span data-stu-id="bba11-200">**Centronics** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

<span data-ttu-id="bba11-201">**Mini-Centronics** (67)</span><span class="sxs-lookup"><span data-stu-id="bba11-201">**Mini-Centronics** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

<span data-ttu-id="bba11-202">**Tipo de mini-Centronics-14** (68)</span><span class="sxs-lookup"><span data-stu-id="bba11-202">**Mini-Centronics Type-14** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

<span data-ttu-id="bba11-203">**Tipo de mini-Centronics-20** (69)</span><span class="sxs-lookup"><span data-stu-id="bba11-203">**Mini-Centronics Type-20** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

<span data-ttu-id="bba11-204">**Tipo de mini-Centronics-26** (70)</span><span class="sxs-lookup"><span data-stu-id="bba11-204">**Mini-Centronics Type-26** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

<span data-ttu-id="bba11-205">**Mouse de barramento** (71)</span><span class="sxs-lookup"><span data-stu-id="bba11-205">**Bus Mouse** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

<span data-ttu-id="bba11-206">**ADB** (72)</span><span class="sxs-lookup"><span data-stu-id="bba11-206">**ADB** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span data-ttu-id="bba11-207">**AGP** (73)</span><span class="sxs-lookup"><span data-stu-id="bba11-207">**AGP** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

<span data-ttu-id="bba11-208">**Barramento de VM** (74)</span><span class="sxs-lookup"><span data-stu-id="bba11-208">**VME Bus** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

<span data-ttu-id="bba11-209">**VME64** (75)</span><span class="sxs-lookup"><span data-stu-id="bba11-209">**VME64** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

<span data-ttu-id="bba11-210">**Proprietário** (76)</span><span class="sxs-lookup"><span data-stu-id="bba11-210">**Proprietary** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

<span data-ttu-id="bba11-211">**Slot do cartão de processador proprietário** (77)</span><span class="sxs-lookup"><span data-stu-id="bba11-211">**Proprietary Processor Card Slot** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

<span data-ttu-id="bba11-212">**Slot de placa de memória proprietária** (78)</span><span class="sxs-lookup"><span data-stu-id="bba11-212">**Proprietary Memory Card Slot** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

<span data-ttu-id="bba11-213">**Slot de riser de e/s proprietário** (79)</span><span class="sxs-lookup"><span data-stu-id="bba11-213">**Proprietary I/O Riser Slot** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

<span data-ttu-id="bba11-214">**PCI-66MHZ** (80)</span><span class="sxs-lookup"><span data-stu-id="bba11-214">**PCI-66MHZ** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

<span data-ttu-id="bba11-215">**AGP2X** (81)</span><span class="sxs-lookup"><span data-stu-id="bba11-215">**AGP2X** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

<span data-ttu-id="bba11-216">**AGP4X** (82)</span><span class="sxs-lookup"><span data-stu-id="bba11-216">**AGP4X** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

<span data-ttu-id="bba11-217">**PC-98** (83)</span><span class="sxs-lookup"><span data-stu-id="bba11-217">**PC-98** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

<span data-ttu-id="bba11-218">**PC-98-Hireso** (84)</span><span class="sxs-lookup"><span data-stu-id="bba11-218">**PC-98-Hireso** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

<span data-ttu-id="bba11-219">**PC-H98** (85)</span><span class="sxs-lookup"><span data-stu-id="bba11-219">**PC-H98** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

<span data-ttu-id="bba11-220">**PC-98Note** (86)</span><span class="sxs-lookup"><span data-stu-id="bba11-220">**PC-98Note** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

<span data-ttu-id="bba11-221">**PC-98Full** (87)</span><span class="sxs-lookup"><span data-stu-id="bba11-221">**PC-98Full** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

<span data-ttu-id="bba11-222">**SSA SCSI** (88)</span><span class="sxs-lookup"><span data-stu-id="bba11-222">**SSA SCSI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Circular"></span><span id="circular"></span><span id="CIRCULAR"></span>

<span data-ttu-id="bba11-223">**Circular** (89)</span><span class="sxs-lookup"><span data-stu-id="bba11-223">**Circular** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_IDE_Connector"></span><span id="on_board_ide_connector"></span><span id="ON_BOARD_IDE_CONNECTOR"></span>

<span data-ttu-id="bba11-224">**Conector IDE integrado** (90)</span><span class="sxs-lookup"><span data-stu-id="bba11-224">**On Board IDE Connector** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_Floppy_Connector"></span><span id="on_board_floppy_connector"></span><span id="ON_BOARD_FLOPPY_CONNECTOR"></span>

<span data-ttu-id="bba11-225">**Conector do disquete de placa** (91)</span><span class="sxs-lookup"><span data-stu-id="bba11-225">**On Board Floppy Connector** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="9_Pin_Dual_Inline"></span><span id="9_pin_dual_inline"></span><span id="9_PIN_DUAL_INLINE"></span>

<span data-ttu-id="bba11-226">**9 pinos embutido duplo** (92)</span><span class="sxs-lookup"><span data-stu-id="bba11-226">**9 Pin Dual Inline** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="25_Pin_Dual_Inline"></span><span id="25_pin_dual_inline"></span><span id="25_PIN_DUAL_INLINE"></span>

<span data-ttu-id="bba11-227">**25 pinos em linha dupla** (93)</span><span class="sxs-lookup"><span data-stu-id="bba11-227">**25 Pin Dual Inline** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

<span data-ttu-id="bba11-228">**50 Pin Dual inline** (94)</span><span class="sxs-lookup"><span data-stu-id="bba11-228">**50 Pin Dual Inline** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="68_Pin_Dual_Inline"></span><span id="68_pin_dual_inline"></span><span id="68_PIN_DUAL_INLINE"></span>

<span data-ttu-id="bba11-229">**68 PIN Dual inline** (95)</span><span class="sxs-lookup"><span data-stu-id="bba11-229">**68 Pin Dual Inline** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="On_Board_Sound_Connector"></span><span id="on_board_sound_connector"></span><span id="ON_BOARD_SOUND_CONNECTOR"></span>

<span data-ttu-id="bba11-230">**Conector de som do quadro** (96)</span><span class="sxs-lookup"><span data-stu-id="bba11-230">**On Board Sound Connector** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini-jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

<span data-ttu-id="bba11-231">**Mini-tomada** (97)</span><span class="sxs-lookup"><span data-stu-id="bba11-231">**Mini-jack** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

<span data-ttu-id="bba11-232">**PCI-X** (98)</span><span class="sxs-lookup"><span data-stu-id="bba11-232">**PCI-X** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

<span data-ttu-id="bba11-233">**Sbus IEEE 1396-1993 32 bit** (99)</span><span class="sxs-lookup"><span data-stu-id="bba11-233">**Sbus IEEE 1396-1993 32 bit** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

<span data-ttu-id="bba11-234">**Sbus IEEE 1396-1993 64 bit** (100)</span><span class="sxs-lookup"><span data-stu-id="bba11-234">**Sbus IEEE 1396-1993 64 bit** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span data-ttu-id="bba11-235">**MCA** (101)</span><span class="sxs-lookup"><span data-stu-id="bba11-235">**MCA** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

<span data-ttu-id="bba11-236">**Gio** (102)</span><span class="sxs-lookup"><span data-stu-id="bba11-236">**GIO** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

<span data-ttu-id="bba11-237">**Xio** (103)</span><span class="sxs-lookup"><span data-stu-id="bba11-237">**XIO** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

<span data-ttu-id="bba11-238">**HIO** (104)</span><span class="sxs-lookup"><span data-stu-id="bba11-238">**HIO** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

<span data-ttu-id="bba11-239">**NGIO** (105)</span><span class="sxs-lookup"><span data-stu-id="bba11-239">**NGIO** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

<span data-ttu-id="bba11-240">**PMC** (106)</span><span class="sxs-lookup"><span data-stu-id="bba11-240">**PMC** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="MTRJ"></span><span id="mtrj"></span>

<span data-ttu-id="bba11-241">**MTRJ** (107)</span><span class="sxs-lookup"><span data-stu-id="bba11-241">**MTRJ** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="VF-45"></span><span id="vf-45"></span>

<span data-ttu-id="bba11-242">**FV-45** (108)</span><span class="sxs-lookup"><span data-stu-id="bba11-242">**VF-45** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

<span data-ttu-id="bba11-243">**E/s futura** (109)</span><span class="sxs-lookup"><span data-stu-id="bba11-243">**Future I/O** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="SC"></span><span id="sc"></span>

<span data-ttu-id="bba11-244">**SC** (110)</span><span class="sxs-lookup"><span data-stu-id="bba11-244">**SC** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="SG"></span><span id="sg"></span>

<span data-ttu-id="bba11-245">**SG** (111)</span><span class="sxs-lookup"><span data-stu-id="bba11-245">**SG** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Electrical"></span><span id="electrical"></span><span id="ELECTRICAL"></span>

<span data-ttu-id="bba11-246">**Elétrico** (112)</span><span class="sxs-lookup"><span data-stu-id="bba11-246">**Electrical** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Optical"></span><span id="optical"></span><span id="OPTICAL"></span>

<span data-ttu-id="bba11-247">**Óptico** (113)</span><span class="sxs-lookup"><span data-stu-id="bba11-247">**Optical** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Ribbon"></span><span id="ribbon"></span><span id="RIBBON"></span>

<span data-ttu-id="bba11-248">**Faixa de Ribbon** (114)</span><span class="sxs-lookup"><span data-stu-id="bba11-248">**Ribbon** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="GLM"></span><span id="glm"></span>

<span data-ttu-id="bba11-249">**GLM** (115)</span><span class="sxs-lookup"><span data-stu-id="bba11-249">**GLM** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="1x9"></span><span id="1X9"></span>

<span data-ttu-id="bba11-250">**1x9** (116)</span><span class="sxs-lookup"><span data-stu-id="bba11-250">**1x9** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Mini_SG"></span><span id="mini_sg"></span><span id="MINI_SG"></span>

<span data-ttu-id="bba11-251">**Mini SG** (117)</span><span class="sxs-lookup"><span data-stu-id="bba11-251">**Mini SG** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="LC"></span><span id="lc"></span>

<span data-ttu-id="bba11-252">**LC** (118)</span><span class="sxs-lookup"><span data-stu-id="bba11-252">**LC** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="HSSC"></span><span id="hssc"></span>

<span data-ttu-id="bba11-253">**HSSC** (119)</span><span class="sxs-lookup"><span data-stu-id="bba11-253">**HSSC** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="VHDCI_Shielded__68_pins_"></span><span id="vhdci_shielded__68_pins_"></span><span id="VHDCI_SHIELDED__68_PINS_"></span>

<span data-ttu-id="bba11-254">**VHDCI blindado (68 pinos)** (120)</span><span class="sxs-lookup"><span data-stu-id="bba11-254">**VHDCI Shielded (68 pins)** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="bba11-255">**InfiniBand** (121)</span><span class="sxs-lookup"><span data-stu-id="bba11-255">**InfiniBand** (121)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bba11-256">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bba11-256">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-257">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bba11-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-258">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-258">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba11-259">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bba11-259">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bba11-260">Nome da classe ou subclasse usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="bba11-260">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="bba11-261">Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="bba11-261">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="bba11-262">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-262">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba11-263">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bba11-263">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-264">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bba11-264">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-265">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-265">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba11-266">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="bba11-266">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="bba11-267">Uma descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="bba11-267">A textual description of the object.</span></span>

<span data-ttu-id="bba11-268">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-268">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba11-269">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="bba11-269">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-270">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="bba11-270">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-271">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-271">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba11-272">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="bba11-272">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="bba11-273">Indica quando o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="bba11-273">Indicates when the object was installed.</span></span> <span data-ttu-id="bba11-274">A falta de um valor não indica que o objeto não está instalado.</span><span class="sxs-lookup"><span data-stu-id="bba11-274">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="bba11-275">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-275">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba11-276">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="bba11-276">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-277">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bba11-277">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-278">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-278">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba11-279">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bba11-279">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bba11-280">Nome da organização responsável por produzir o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="bba11-280">Name of the organization responsible for producing the physical element.</span></span> <span data-ttu-id="bba11-281">Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-281">For more information, see the **Vendor** property of [**CIM\_Product**](cim-product.md).</span></span>

<span data-ttu-id="bba11-282">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-282">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba11-283">**Modelo**</span><span class="sxs-lookup"><span data-stu-id="bba11-283">**Model**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-284">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bba11-284">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-285">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-285">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba11-286">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="bba11-286">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bba11-287">Nome pelo qual o elemento físico é geralmente conhecido.</span><span class="sxs-lookup"><span data-stu-id="bba11-287">Name by which the physical element is generally known.</span></span>

<span data-ttu-id="bba11-288">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-288">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba11-289">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bba11-289">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-290">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bba11-290">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-291">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-291">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba11-292">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span><span class="sxs-lookup"><span data-stu-id="bba11-292">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="bba11-293">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="bba11-293">Label by which the object is known.</span></span> <span data-ttu-id="bba11-294">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="bba11-294">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="bba11-295">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-295">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba11-296">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="bba11-296">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-297">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bba11-297">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-298">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-298">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bba11-299">Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="bba11-299">Additional data, beyond asset tag information, that can be used to identify a physical element.</span></span> <span data-ttu-id="bba11-300">Um exemplo são dados de código de barras associados a um elemento, que também tem uma marca de ativo.</span><span class="sxs-lookup"><span data-stu-id="bba11-300">One example is bar-code data that is associated with an element, which also has an asset tag.</span></span> <span data-ttu-id="bba11-301">Observe que, se apenas os dados de código de barras estiverem disponíveis e for exclusivo e puderem ser usados como uma chave de elemento, essa propriedade será nula e os dados de código de barras seriam usados como a chave de classe na propriedade de **marca** .</span><span class="sxs-lookup"><span data-stu-id="bba11-301">Note that if only bar-code data is available, and is unique and able to be used as an element key, this property would be null and the bar-code data would be used as the class key in the **Tag** property.</span></span>

<span data-ttu-id="bba11-302">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-302">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba11-303">**PartNumber**</span><span class="sxs-lookup"><span data-stu-id="bba11-303">**PartNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-304">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bba11-304">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-305">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-305">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba11-306">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bba11-306">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bba11-307">Número de peça atribuído pela organização responsável por produzir ou fabricar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="bba11-307">Part number assigned by the organization responsible for producing or manufacturing the physical element.</span></span>

<span data-ttu-id="bba11-308">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-308">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba11-309">**Ligado**</span><span class="sxs-lookup"><span data-stu-id="bba11-309">**PoweredOn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-310">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="bba11-310">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-311">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-311">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bba11-312">Se **for true**, o elemento físico será ligado.</span><span class="sxs-lookup"><span data-stu-id="bba11-312">If **TRUE**, the physical element is powered on.</span></span> <span data-ttu-id="bba11-313">Caso contrário, ele estará desativado no momento.</span><span class="sxs-lookup"><span data-stu-id="bba11-313">Otherwise, it is currently off.</span></span>

<span data-ttu-id="bba11-314">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-314">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba11-315">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="bba11-315">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-316">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bba11-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba11-318">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="bba11-318">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bba11-319">Número alocado pelo fabricante usado para identificar o elemento físico.</span><span class="sxs-lookup"><span data-stu-id="bba11-319">Manufacturer-allocated number used to identify the physical element.</span></span>

<span data-ttu-id="bba11-320">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-320">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba11-321">**SKU**</span><span class="sxs-lookup"><span data-stu-id="bba11-321">**SKU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-322">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bba11-322">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba11-324">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="bba11-324">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bba11-325">Número de unidade de manutenção de estoque para este elemento físico.</span><span class="sxs-lookup"><span data-stu-id="bba11-325">Stock-keeping unit number for this physical element.</span></span>

<span data-ttu-id="bba11-326">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-326">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba11-327">**Status**</span><span class="sxs-lookup"><span data-stu-id="bba11-327">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-328">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bba11-328">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-329">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-329">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba11-330">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="bba11-330">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="bba11-331">Cadeia de caracteres que indica o status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="bba11-331">String that indicates the current status of the object.</span></span> <span data-ttu-id="bba11-332">O status operacional e não operacional pode ser definido.</span><span class="sxs-lookup"><span data-stu-id="bba11-332">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="bba11-333">O status operacional pode incluir "OK", "degradado" e "Pred falha".</span><span class="sxs-lookup"><span data-stu-id="bba11-333">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="bba11-334">"Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para inteligente).</span><span class="sxs-lookup"><span data-stu-id="bba11-334">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="bba11-335">O status não operacional pode incluir "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="bba11-335">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="bba11-336">O "serviço" pode ser aplicado durante o espelhamento de disco – reprateando, recarregando uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="bba11-336">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="bba11-337">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="bba11-337">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="bba11-338">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-338">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="bba11-339">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="bba11-339">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="bba11-340">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="bba11-340">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="bba11-341">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="bba11-341">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="bba11-342">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="bba11-342">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="bba11-343">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="bba11-343">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="bba11-344">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="bba11-344">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="bba11-345">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="bba11-345">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="bba11-346">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="bba11-346">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="bba11-347">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="bba11-347">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="bba11-348">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="bba11-348">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="bba11-349">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="bba11-349">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="bba11-350">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="bba11-350">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="bba11-351">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="bba11-351">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="bba11-352">**Tag**</span><span class="sxs-lookup"><span data-stu-id="bba11-352">**Tag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-353">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bba11-353">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-354">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-354">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba11-355">Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="bba11-355">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="bba11-356">Identifica exclusivamente o elemento físico e serve como a chave do elemento.</span><span class="sxs-lookup"><span data-stu-id="bba11-356">Uniquely identifies the physical element and serves as the element's key.</span></span> <span data-ttu-id="bba11-357">Essa propriedade pode conter informações, como a marca de ativo ou os dados de número de série.</span><span class="sxs-lookup"><span data-stu-id="bba11-357">This property can contain information, such as asset tag or serial number data.</span></span> <span data-ttu-id="bba11-358">A chave para [**o \_ físico do CIM**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar de forma independente o hardware ou a entidade, independentemente do posicionamento físico nos gabinetes, adaptadores e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="bba11-358">The key for [**CIM\_PhysicalElement**](cim-physicalelement.md) is placed very high in the object hierarchy to independently identify the hardware or entity, regardless of physical placement in (or on) cabinets, adapters, and so on.</span></span> <span data-ttu-id="bba11-359">Por exemplo, um componente removível que pode ser intercambiável pode ser extraído de seu pacote recipiente (escopo) e estar temporariamente não utilizado.</span><span class="sxs-lookup"><span data-stu-id="bba11-359">For example, a removable component that can be hot-swapped can be taken from its containing (scoping) package and be temporarily unused.</span></span> <span data-ttu-id="bba11-360">O objeto ainda continua existindo e pode até ser inserido em um contêiner de escopo diferente.</span><span class="sxs-lookup"><span data-stu-id="bba11-360">The object still continues to exist and can even be inserted into a different scoping container.</span></span> <span data-ttu-id="bba11-361">A chave para um elemento físico é uma cadeia de caracteres arbitrária que é definida independentemente do posicionamento ou da hierarquia orientada por local.</span><span class="sxs-lookup"><span data-stu-id="bba11-361">The key for a physical element is an arbitrary string that is defined independently of placement or location-oriented hierarchy.</span></span>

<span data-ttu-id="bba11-362">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-362">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="bba11-363">**Versão**</span><span class="sxs-lookup"><span data-stu-id="bba11-363">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bba11-364">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="bba11-364">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bba11-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="bba11-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bba11-366">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="bba11-366">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bba11-367">Indica a versão do elemento físico.</span><span class="sxs-lookup"><span data-stu-id="bba11-367">Indicates the version of the physical element.</span></span>

<span data-ttu-id="bba11-368">Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-368">This property is inherited from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bba11-369">Comentários</span><span class="sxs-lookup"><span data-stu-id="bba11-369">Remarks</span></span>

<span data-ttu-id="bba11-370">A classe **CIM \_ PhysicalConnector** é derivada do [**CIM \_ físicoelement**](cim-physicalelement.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-370">The **CIM\_PhysicalConnector** class is derived from [**CIM\_PhysicalElement**](cim-physicalelement.md).</span></span>

<span data-ttu-id="bba11-371">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="bba11-371">WMI does not implement this class.</span></span> <span data-ttu-id="bba11-372">Para classes WMI que são derivadas do **CIM \_ PhysicalConnector**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bba11-372">For WMI classes that are derived from **CIM\_PhysicalConnector**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="bba11-373">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="bba11-373">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bba11-374">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="bba11-374">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bba11-375">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bba11-375">Requirements</span></span>



| <span data-ttu-id="bba11-376">Requisito</span><span class="sxs-lookup"><span data-stu-id="bba11-376">Requirement</span></span> | <span data-ttu-id="bba11-377">Valor</span><span class="sxs-lookup"><span data-stu-id="bba11-377">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bba11-378">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bba11-378">Minimum supported client</span></span><br/> | <span data-ttu-id="bba11-379">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bba11-379">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bba11-380">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bba11-380">Minimum supported server</span></span><br/> | <span data-ttu-id="bba11-381">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bba11-381">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bba11-382">Namespace</span><span class="sxs-lookup"><span data-stu-id="bba11-382">Namespace</span></span><br/>                | <span data-ttu-id="bba11-383">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bba11-383">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bba11-384">MOF</span><span class="sxs-lookup"><span data-stu-id="bba11-384">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bba11-385"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bba11-385"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bba11-386">DLL</span><span class="sxs-lookup"><span data-stu-id="bba11-386">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bba11-387"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bba11-387"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bba11-388">Confira também</span><span class="sxs-lookup"><span data-stu-id="bba11-388">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bba11-389">**Físico do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="bba11-389">**CIM\_PhysicalElement**</span></span>](cim-physicalelement.md)
</dt> </dl>

 

