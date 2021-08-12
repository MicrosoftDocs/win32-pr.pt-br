---
description: A classe \_ Cim PhysicalConnector representa qualquer elemento físico usado para se conectar a outros elementos. Qualquer objeto que possa se conectar e transmitir sinais ou energia entre dois ou mais elementos físicos é um descendente (ou membro) dessa classe.
ms.assetid: cc135ae8-5ae1-4028-a2e3-a81db8694d9d
ms.tgt_platform: multiple
title: CIM_PhysicalConnector classe
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
ms.openlocfilehash: e4c5e53c2c8d02abb0762a9c3cc5bc5540f175f0810ec319180eb06435948ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118678268"
---
# <a name="cim_physicalconnector-class"></a>Classe Cim \_ PhysicalConnector

A **classe \_ Cim PhysicalConnector** representa qualquer elemento físico usado para se conectar a outros elementos. Qualquer objeto que possa se conectar e transmitir sinais ou energia entre dois ou mais elementos físicos é um descendente (ou membro) dessa classe. Por exemplo, slots e conectores D-shell são tipos de conectores físicos.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) modelo CIM DMTF são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do Managed Object Format (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A **classe Cim \_ PhysicalConnector** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Cim \_ PhysicalConnector** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Legenda")
</dt> </dl>

Uma breve descrição textual do objeto .

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**ConnectorPinout**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres de forma livre que descreve a configuração de pino e o uso de sinal de um conector físico.

</dd> <dt>

**Connectortype**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de conector físico. Uma matriz é especificada para permitir a descrição de combinações de informações do conector. Por exemplo, uma entrada de matriz pode especificar RS-232, outro DB-25 e uma terceira entrada pode definir o conector como "masculino".

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Male"></span><span id="male"></span><span id="MALE"></span>

**Masculino** (2)


</dt> <dd></dd> <dt>

<span id="Female"></span><span id="female"></span><span id="FEMALE"></span>

**Mulher** (3)


</dt> <dd></dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

**Blindada** (4)


</dt> <dd></dd> <dt>

<span id="Unshielded"></span><span id="unshielded"></span><span id="UNSHIELDED"></span>

**Sem blindagem** (5)


</dt> <dd></dd> <dt>

<span id="SCSI__A__High-Density__50_pins_"></span><span id="scsi__a__high-density__50_pins_"></span><span id="SCSI__A__HIGH-DENSITY__50_PINS_"></span>

**SCSI (A) High-Density (50 pinos)** (6)


</dt> <dd></dd> <dt>

<span id="SCSI__A__Low-Density__50_pins_"></span><span id="scsi__a__low-density__50_pins_"></span><span id="SCSI__A__LOW-DENSITY__50_PINS_"></span>

**SCSI (A) Low-Density (50 pinos)** (7)


</dt> <dd></dd> <dt>

<span id="SCSI__P__High-Density__68_pins_"></span><span id="scsi__p__high-density__68_pins_"></span><span id="SCSI__P__HIGH-DENSITY__68_PINS_"></span>

**SCSI (P) High-Density (68 pinos)** (8)


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-I__80_pins_"></span><span id="scsi_sca-i__80_pins_"></span><span id="SCSI_SCA-I__80_PINS_"></span>

**SCSI SCA-I (80 pinos)** (9)


</dt> <dd></dd> <dt>

<span id="SCSI_SCA-II__80_pins_"></span><span id="scsi_sca-ii__80_pins_"></span><span id="SCSI_SCA-II__80_PINS_"></span>

**SCSI SCA-II (80 pinos)** (10)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__DB-9__Copper_"></span><span id="scsi_fibre_channel__db-9__copper_"></span><span id="SCSI_FIBRE_CHANNEL__DB-9__COPPER_"></span>

**SCSI Fibre Channel (DB-9, Cobre)** (11)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel__Fibre_"></span><span id="scsi_fibre_channel__fibre_"></span><span id="SCSI_FIBRE_CHANNEL__FIBRE_"></span>

**SCSI Fibre Channel (Fibre)** (12)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__40_pins_"></span><span id="scsi_fibre_channel_sca-ii__40_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__40_PINS_"></span>

**SCSI Fibre Channel SCA-II (40 pinos)** (13)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_SCA-II__20_pins_"></span><span id="scsi_fibre_channel_sca-ii__20_pins_"></span><span id="SCSI_FIBRE_CHANNEL_SCA-II__20_PINS_"></span>

**SCSI Fibre Channel SCA-II (20 pinos)** (14)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_BNC"></span><span id="scsi_fibre_channel_bnc"></span><span id="SCSI_FIBRE_CHANNEL_BNC"></span>

**SCSI Fibre Channel BNC** (15)


</dt> <dd></dd> <dt>

<span id="ATA_3-1_2_Inch__40_pins_"></span><span id="ata_3-1_2_inch__40_pins_"></span><span id="ATA_3-1_2_INCH__40_PINS_"></span>

**ATA 3-1/2 Polegada (40 pinos)** (16)


</dt> <dd></dd> <dt>

<span id="ATA_2-1_2_Inch__44_pins_"></span><span id="ata_2-1_2_inch__44_pins_"></span><span id="ATA_2-1_2_INCH__44_PINS_"></span>

**ATA 2-1/2 Polegada (44 pinos)** (17)


</dt> <dd></dd> <dt>

<span id="ATA-2"></span><span id="ata-2"></span>

**ATA-2** (18)


</dt> <dd></dd> <dt>

<span id="ATA-3"></span><span id="ata-3"></span>

**ATA-3** (19)


</dt> <dd></dd> <dt>

<span id="ATA_66"></span><span id="ata_66"></span>

**ATA/66** (20)


</dt> <dd></dd> <dt>

<span id="DB-9"></span><span id="db-9"></span>

**DB-9** (21)


</dt> <dd></dd> <dt>

<span id="DB-15"></span><span id="db-15"></span>

**DB-15** (22)


</dt> <dd></dd> <dt>

<span id="DB-25"></span><span id="db-25"></span>

**DB-25** (23)


</dt> <dd></dd> <dt>

<span id="DB-36"></span><span id="db-36"></span>

**DB-36** (24)


</dt> <dd></dd> <dt>

<span id="RS-232C"></span><span id="rs-232c"></span>

**RS-232C** (25)


</dt> <dd></dd> <dt>

<span id="RS-422"></span><span id="rs-422"></span>

**RS-422** (26)


</dt> <dd></dd> <dt>

<span id="RS-423"></span><span id="rs-423"></span>

**RS-423** (27)


</dt> <dd></dd> <dt>

<span id="RS-485"></span><span id="rs-485"></span>

**RS-485** (28)


</dt> <dd></dd> <dt>

<span id="RS-449"></span><span id="rs-449"></span>

**RS-449** (29)


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

**V.35** (30)


</dt> <dd></dd> <dt>

<span id="X.21"></span><span id="x.21"></span>

**X.21** (31)


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

**IEEE-488** (32)


</dt> <dd></dd> <dt>

<span id="AUI"></span><span id="aui"></span>

**AUI** (33)


</dt> <dd></dd> <dt>

<span id="UTP_Category_3"></span><span id="utp_category_3"></span><span id="UTP_CATEGORY_3"></span>

**Categoria UTP 3** (34)


</dt> <dd></dd> <dt>

<span id="UTP_Category_4"></span><span id="utp_category_4"></span><span id="UTP_CATEGORY_4"></span>

**Categoria UTP 4** (35)


</dt> <dd></dd> <dt>

<span id="UTP_Category_5"></span><span id="utp_category_5"></span><span id="UTP_CATEGORY_5"></span>

**Categoria UTP 5** (36)


</dt> <dd></dd> <dt>

<span id="BNC"></span><span id="bnc"></span>

**BNC** (37)


</dt> <dd></dd> <dt>

<span id="RJ11"></span><span id="rj11"></span>

**RJ11** (38)


</dt> <dd></dd> <dt>

<span id="RJ45"></span><span id="rj45"></span>

**RJ45** (39)


</dt> <dd></dd> <dt>

<span id="Fiber_MIC"></span><span id="fiber_mic"></span><span id="FIBER_MIC"></span>

**Fiber MIC** (40)


</dt> <dd></dd> <dt>

<span id="Apple_AUI"></span><span id="apple_aui"></span><span id="APPLE_AUI"></span>

**Apple AUI** (41)


</dt> <dd></dd> <dt>

<span id="Apple_GeoPort"></span><span id="apple_geoport"></span><span id="APPLE_GEOPORT"></span>

**Apple GeoPort** (42)


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

**PCI** (43)


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

**ISA** (44)


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

**EISA** (45)


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

**VESA** (46)


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

**PCMCIA** (47)


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_I"></span><span id="pcmcia_type_i"></span><span id="PCMCIA_TYPE_I"></span>

**Tipo PCMCIA I** (48)


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_II"></span><span id="pcmcia_type_ii"></span><span id="PCMCIA_TYPE_II"></span>

**PCMCIA Tipo II** (49)


</dt> <dd></dd> <dt>

<span id="PCMCIA_Type_III"></span><span id="pcmcia_type_iii"></span><span id="PCMCIA_TYPE_III"></span>

**PCMCIA Tipo III** (50)


</dt> <dd></dd> <dt>

<span id="ZV_Port"></span><span id="zv_port"></span><span id="ZV_PORT"></span>

**Porta ZV** (51)


</dt> <dd></dd> <dt>

<span id="CardBus"></span><span id="cardbus"></span><span id="CARDBUS"></span>

**CardBus** (52)


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

**USB** (53)


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

**IEEE 1394** (54)


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

**HIPPI** (55)


</dt> <dd></dd> <dt>

<span id="HSSDC__6_pins_"></span><span id="hssdc__6_pins_"></span><span id="HSSDC__6_PINS_"></span>

**HSSDC (6 pinos)** (56)


</dt> <dd></dd> <dt>

<span id="GBIC"></span><span id="gbic"></span>

**GBIC** (57)


</dt> <dd></dd> <dt>

<span id="DIN"></span><span id="din"></span>

**DIN** (58)


</dt> <dd></dd> <dt>

<span id="Mini-DIN"></span><span id="mini-din"></span><span id="MINI-DIN"></span>

**Mini-DIN** (59)


</dt> <dd></dd> <dt>

<span id="Micro-DIN"></span><span id="micro-din"></span><span id="MICRO-DIN"></span>

**Micro-DIN** (60)


</dt> <dd></dd> <dt>

<span id="PS_2"></span><span id="ps_2"></span>

**PS/2** (61)


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

**Inomeado** (62)


</dt> <dd></dd> <dt>

<span id="HP-HIL"></span><span id="hp-hil"></span>

**HP-LTD** (63)


</dt> <dd></dd> <dt>

<span id="Access.bus"></span><span id="access.bus"></span><span id="ACCESS.BUS"></span>

**Access.bus** (64)


</dt> <dd></dd> <dt>

<span id="NuBus"></span><span id="nubus"></span><span id="NUBUS"></span>

**NuBus** (65)


</dt> <dd></dd> <dt>

<span id="Centronics"></span><span id="centronics"></span><span id="CENTRONICS"></span>

**Centronics** (66)


</dt> <dd></dd> <dt>

<span id="Mini-Centronics"></span><span id="mini-centronics"></span><span id="MINI-CENTRONICS"></span>

**Mini-Centronics** (67)


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-14"></span><span id="mini-centronics_type-14"></span><span id="MINI-CENTRONICS_TYPE-14"></span>

**Tipo de mini-Centronics-14** (68)


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-20"></span><span id="mini-centronics_type-20"></span><span id="MINI-CENTRONICS_TYPE-20"></span>

**Tipo de mini-Centronics-20** (69)


</dt> <dd></dd> <dt>

<span id="Mini-Centronics_Type-26"></span><span id="mini-centronics_type-26"></span><span id="MINI-CENTRONICS_TYPE-26"></span>

**Tipo de mini-Centronics-26** (70)


</dt> <dd></dd> <dt>

<span id="Bus_Mouse"></span><span id="bus_mouse"></span><span id="BUS_MOUSE"></span>

**Mouse de barramento** (71)


</dt> <dd></dd> <dt>

<span id="ADB"></span><span id="adb"></span>

**ADB** (72)


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

**AGP** (73)


</dt> <dd></dd> <dt>

<span id="VME_Bus"></span><span id="vme_bus"></span><span id="VME_BUS"></span>

**Barramento de VM** (74)


</dt> <dd></dd> <dt>

<span id="VME64"></span><span id="vme64"></span>

**VME64** (75)


</dt> <dd></dd> <dt>

<span id="Proprietary"></span><span id="proprietary"></span><span id="PROPRIETARY"></span>

**Proprietário** (76)


</dt> <dd></dd> <dt>

<span id="Proprietary_Processor_Card_Slot"></span><span id="proprietary_processor_card_slot"></span><span id="PROPRIETARY_PROCESSOR_CARD_SLOT"></span>

**Slot do cartão de processador proprietário** (77)


</dt> <dd></dd> <dt>

<span id="Proprietary_Memory_Card_Slot"></span><span id="proprietary_memory_card_slot"></span><span id="PROPRIETARY_MEMORY_CARD_SLOT"></span>

**Slot de placa de memória proprietária** (78)


</dt> <dd></dd> <dt>

<span id="Proprietary_I_O_Riser_Slot"></span><span id="proprietary_i_o_riser_slot"></span><span id="PROPRIETARY_I_O_RISER_SLOT"></span>

**Slot de riser de e/s proprietário** (79)


</dt> <dd></dd> <dt>

<span id="PCI-66MHZ"></span><span id="pci-66mhz"></span>

**PCI-66MHZ** (80)


</dt> <dd></dd> <dt>

<span id="AGP2X"></span><span id="agp2x"></span>

**AGP2X** (81)


</dt> <dd></dd> <dt>

<span id="AGP4X"></span><span id="agp4x"></span>

**AGP4X** (82)


</dt> <dd></dd> <dt>

<span id="PC-98"></span><span id="pc-98"></span>

**PC-98** (83)


</dt> <dd></dd> <dt>

<span id="PC-98-Hireso"></span><span id="pc-98-hireso"></span><span id="PC-98-HIRESO"></span>

**PC-98-Hireso** (84)


</dt> <dd></dd> <dt>

<span id="PC-H98"></span><span id="pc-h98"></span>

**PC-H98** (85)


</dt> <dd></dd> <dt>

<span id="PC-98Note"></span><span id="pc-98note"></span><span id="PC-98NOTE"></span>

**PC-98Note** (86)


</dt> <dd></dd> <dt>

<span id="PC-98Full"></span><span id="pc-98full"></span><span id="PC-98FULL"></span>

**PC-98Full** (87)


</dt> <dd></dd> <dt>

<span id="SSA_SCSI"></span><span id="ssa_scsi"></span>

**SSA SCSI** (88)


</dt> <dd></dd> <dt>

<span id="Circular"></span><span id="circular"></span><span id="CIRCULAR"></span>

**Circular** (89)


</dt> <dd></dd> <dt>

<span id="On_Board_IDE_Connector"></span><span id="on_board_ide_connector"></span><span id="ON_BOARD_IDE_CONNECTOR"></span>

**Conector IDE integrado** (90)


</dt> <dd></dd> <dt>

<span id="On_Board_Floppy_Connector"></span><span id="on_board_floppy_connector"></span><span id="ON_BOARD_FLOPPY_CONNECTOR"></span>

**Conector do disquete de placa** (91)


</dt> <dd></dd> <dt>

<span id="9_Pin_Dual_Inline"></span><span id="9_pin_dual_inline"></span><span id="9_PIN_DUAL_INLINE"></span>

**9 pinos embutido duplo** (92)


</dt> <dd></dd> <dt>

<span id="25_Pin_Dual_Inline"></span><span id="25_pin_dual_inline"></span><span id="25_PIN_DUAL_INLINE"></span>

**25 pinos em linha dupla** (93)


</dt> <dd></dd> <dt>

<span id="50_Pin_Dual_Inline"></span><span id="50_pin_dual_inline"></span><span id="50_PIN_DUAL_INLINE"></span>

**50 Pin Dual inline** (94)


</dt> <dd></dd> <dt>

<span id="68_Pin_Dual_Inline"></span><span id="68_pin_dual_inline"></span><span id="68_PIN_DUAL_INLINE"></span>

**68 PIN Dual inline** (95)


</dt> <dd></dd> <dt>

<span id="On_Board_Sound_Connector"></span><span id="on_board_sound_connector"></span><span id="ON_BOARD_SOUND_CONNECTOR"></span>

**Conector de som do quadro** (96)


</dt> <dd></dd> <dt>

<span id="Mini-jack"></span><span id="mini-jack"></span><span id="MINI-JACK"></span>

**Mini-tomada** (97)


</dt> <dd></dd> <dt>

<span id="PCI-X"></span><span id="pci-x"></span>

**PCI-X** (98)


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_32_bit"></span><span id="sbus_ieee_1396-1993_32_bit"></span><span id="SBUS_IEEE_1396-1993_32_BIT"></span>

**Sbus IEEE 1396-1993 32 bit** (99)


</dt> <dd></dd> <dt>

<span id="Sbus_IEEE_1396-1993_64_bit"></span><span id="sbus_ieee_1396-1993_64_bit"></span><span id="SBUS_IEEE_1396-1993_64_BIT"></span>

**Sbus IEEE 1396-1993 64 bit** (100)


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

**MCA** (101)


</dt> <dd></dd> <dt>

<span id="GIO"></span><span id="gio"></span>

**Gio** (102)


</dt> <dd></dd> <dt>

<span id="XIO"></span><span id="xio"></span>

**Xio** (103)


</dt> <dd></dd> <dt>

<span id="HIO"></span><span id="hio"></span>

**HIO** (104)


</dt> <dd></dd> <dt>

<span id="NGIO"></span><span id="ngio"></span>

**NGIO** (105)


</dt> <dd></dd> <dt>

<span id="PMC"></span><span id="pmc"></span>

**PMC** (106)


</dt> <dd></dd> <dt>

<span id="MTRJ"></span><span id="mtrj"></span>

**MTRJ** (107)


</dt> <dd></dd> <dt>

<span id="VF-45"></span><span id="vf-45"></span>

**FV-45** (108)


</dt> <dd></dd> <dt>

<span id="Future_I_O"></span><span id="future_i_o"></span><span id="FUTURE_I_O"></span>

**E/s futura** (109)


</dt> <dd></dd> <dt>

<span id="SC"></span><span id="sc"></span>

**SC** (110)


</dt> <dd></dd> <dt>

<span id="SG"></span><span id="sg"></span>

**SG** (111)


</dt> <dd></dd> <dt>

<span id="Electrical"></span><span id="electrical"></span><span id="ELECTRICAL"></span>

**Elétrico** (112)


</dt> <dd></dd> <dt>

<span id="Optical"></span><span id="optical"></span><span id="OPTICAL"></span>

**Óptico** (113)


</dt> <dd></dd> <dt>

<span id="Ribbon"></span><span id="ribbon"></span><span id="RIBBON"></span>

**Faixa de Ribbon** (114)


</dt> <dd></dd> <dt>

<span id="GLM"></span><span id="glm"></span>

**GLM** (115)


</dt> <dd></dd> <dt>

<span id="1x9"></span><span id="1X9"></span>

**1x9** (116)


</dt> <dd></dd> <dt>

<span id="Mini_SG"></span><span id="mini_sg"></span><span id="MINI_SG"></span>

**Mini SG** (117)


</dt> <dd></dd> <dt>

<span id="LC"></span><span id="lc"></span>

**LC** (118)


</dt> <dd></dd> <dt>

<span id="HSSC"></span><span id="hssc"></span>

**HSSC** (119)


</dt> <dd></dd> <dt>

<span id="VHDCI_Shielded__68_pins_"></span><span id="vhdci_shielded__68_pins_"></span><span id="VHDCI_SHIELDED__68_PINS_"></span>

**VHDCI blindado (68 pinos)** (120)


</dt> <dd></dd> <dt>

<span id="InfiniBand"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

**InfiniBand** (121)


</dt> <dd></dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome da classe ou subclasse usada na criação de uma instância. Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")
</dt> </dl>

Uma descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")
</dt> </dl>

Indica quando o objeto foi instalado. A falta de um valor não indica que o objeto não está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Manufacturer**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome da organização responsável por produzir o elemento físico. Para obter mais informações, consulte a propriedade **Vendor** do [**\_ produto CIM**](cim-product.md).

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**Modelo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Nome pelo qual o elemento físico é geralmente conhecido.

Essa propriedade é herdada do [**CIM \_ físicoelement**](cim-physicalelement.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")
</dt> </dl>

Rótulo pelo qual o objeto é conhecido. Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Dados adicionais, além das informações de marca do ativo, que podem ser usados para identificar um elemento físico. Um exemplo são dados de código de barras associados a um elemento, que também tem uma marca de ativo. Observe que, se apenas os dados de código de barras estão disponíveis e são exclusivos e podem ser usados como uma chave de elemento, essa propriedade seria nula e os dados de código de barra seriam usados como a chave de classe na propriedade **Tag.**

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Número da parte atribuído pela organização responsável por produzir ou fabricar o elemento físico.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, o elemento físico será ligado. Caso contrário, ele está desligado no momento.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Número alocado pelo fabricante usado para identificar o elemento físico.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Número de unidade de manutenção de estoque para esse elemento físico.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Cadeia de caracteres que indica o status atual do objeto. O status operacional e não operacional pode ser definido. O status operacional pode incluir "OK", "Degradado" e "Pred Fail". "Pred Fail" indica que um elemento está funcionando corretamente, mas está prevendo uma falha (por exemplo, uma unidade de disco rígido habilitada para SMART).

O status não operacional pode incluir "Erro", "Iniciando", "Parando" e "Serviço". O "Serviço" pode ser aplicado durante a resilvering de espelhamento de disco, o recarregamento de uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros estados.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Os valores incluem o seguinte:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("Erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("Degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("Desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("Parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("Serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("Sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de vírgula** ("comm perdida")


</dt> <dd></dd> </dl>

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ Chave CIM,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identifica exclusivamente o elemento físico e serve como a chave do elemento. Essa propriedade pode conter informações, como dados de número de série ou marca de ativo. A chave para [**Cim \_ PhysicalElement**](cim-physicalelement.md) é colocada muito alta na hierarquia de objetos para identificar independentemente o hardware ou a entidade, independentemente do posicionamento físico em gabinetes (ou em) gabinetes, adaptadores e assim por diante. Por exemplo, um componente removível que pode ser trocado por hot-swapp pode ser retirado de seu pacote de contenção (scoping) e ser temporariamente não usada. O objeto ainda continua a existir e pode até mesmo ser inserido em um contêiner de scoping diferente. A chave para um elemento físico é uma cadeia de caracteres arbitrária definida independentemente do posicionamento ou da hierarquia orientada à localização.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Indica a versão do elemento físico.

Essa propriedade é herdada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ Cim PhysicalConnector** é derivada de [**CIM \_ PhysicalElement.**](cim-physicalelement.md)

O WMI não implementa essa classe. Para classes WMI derivadas de **Cim \_ PhysicalConnector**, consulte [Classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**CIM \_ PhysicalElement**](cim-physicalelement.md)
</dt> </dl>

 

