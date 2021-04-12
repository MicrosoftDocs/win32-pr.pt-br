---
description: Representa os atributos dos serviços de entrada/saída básicos (BIOS) do sistema de computador que estão instalados em um computador.
ms.assetid: e4a5aaf0-0432-4517-97b7-ac05ffd10b5b
ms.tgt_platform: multiple
title: Classe Win32_BIOS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BIOS
- Win32_BIOS.BiosCharacteristics
- Win32_BIOS.BIOSVersion
- Win32_BIOS.BuildNumber
- Win32_BIOS.Caption
- Win32_BIOS.CodeSet
- Win32_BIOS.CurrentLanguage
- Win32_BIOS.Description
- Win32_BIOS.EmbeddedControllerMajorVersion
- Win32_BIOS.EmbeddedControllerMinorVersion
- Win32_BIOS.IdentificationCode
- Win32_BIOS.InstallableLanguages
- Win32_BIOS.InstallDate
- Win32_BIOS.LanguageEdition
- Win32_BIOS.ListOfLanguages
- Win32_BIOS.Manufacturer
- Win32_BIOS.Name
- Win32_BIOS.OtherTargetOS
- Win32_BIOS.PrimaryBIOS
- Win32_BIOS.ReleaseDate
- Win32_BIOS.SerialNumber
- Win32_BIOS.SMBIOSBIOSVersion
- Win32_BIOS.SMBIOSMajorVersion
- Win32_BIOS.SMBIOSMinorVersion
- Win32_BIOS.SMBIOSPresent
- Win32_BIOS.SoftwareElementID
- Win32_BIOS.SoftwareElementState
- Win32_BIOS.Status
- Win32_BIOS.SystemBiosMajorVersion
- Win32_BIOS.SystemBiosMinorVersion
- Win32_BIOS.TargetOperatingSystem
- Win32_BIOS.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 53c1e953c9c1348a133cf4755ab04f6024c42034
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501065"
---
# <a name="win32_bios-class"></a><span data-ttu-id="44e3c-103">\_Classe do Win32 BIOS</span><span class="sxs-lookup"><span data-stu-id="44e3c-103">Win32\_BIOS class</span></span>

<span data-ttu-id="44e3c-104">A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ BIOS do Win32** representa os atributos dos serviços de entrada/saída básicos (BIOS) do sistema de computador que estão instalados em um computador.</span><span class="sxs-lookup"><span data-stu-id="44e3c-104">The **Win32\_BIOS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the attributes of the computer system's basic input/output services (BIOS) that are installed on a computer.</span></span>

<span data-ttu-id="44e3c-105">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="44e3c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="44e3c-106">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="44e3c-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="44e3c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="44e3c-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4E1-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_BIOS : CIM_BIOSElement
{
  uint16   BiosCharacteristics[];
  string   BIOSVersion[];
  string   BuildNumber;
  string   Caption;
  string   CodeSet;
  string   CurrentLanguage;
  string   Description;
  uint8    EmbeddedControllerMajorVersion;
  uint8    EmbeddedControllerMinorVersion;
  string   IdentificationCode;
  uint16   InstallableLanguages;
  datetime InstallDate;
  string   LanguageEdition;
  String   ListOfLanguages[];
  string   Manufacturer;
  string   Name;
  string   OtherTargetOS;
  boolean  PrimaryBIOS;
  datetime ReleaseDate;
  string   SerialNumber;
  string   SMBIOSBIOSVersion;
  uint16   SMBIOSMajorVersion;
  uint16   SMBIOSMinorVersion;
  boolean  SMBIOSPresent;
  string   SoftwareElementID;
  uint16   SoftwareElementState;
  string   Status;
  uint8    SystemBiosMajorVersion;
  uint8    SystemBiosMinorVersion;
  uint16   TargetOperatingSystem;
  string   Version;
};
```

## <a name="members"></a><span data-ttu-id="44e3c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="44e3c-108">Members</span></span>

<span data-ttu-id="44e3c-109">A classe **Win32 \_ BIOS** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="44e3c-109">The **Win32\_BIOS** class has these types of members:</span></span>

-   [<span data-ttu-id="44e3c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="44e3c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44e3c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="44e3c-111">Properties</span></span>

<span data-ttu-id="44e3c-112">A classe **Win32 \_ BIOS** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="44e3c-112">The **Win32\_BIOS** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44e3c-113">**BiosCharacteristics**</span><span class="sxs-lookup"><span data-stu-id="44e3c-113">**BiosCharacteristics**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-114">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44e3c-114">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-116">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| características do BIOS do tipo SMBIOS 0")</span><span class="sxs-lookup"><span data-stu-id="44e3c-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|BIOS Characteristics")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-117">Matriz de características do BIOS com suporte do sistema conforme definido pela especificação de referência do BIOS do System Management.</span><span class="sxs-lookup"><span data-stu-id="44e3c-117">Array of BIOS characteristics supported by the system as defined by the System Management BIOS Reference Specification.</span></span>

<span data-ttu-id="44e3c-118">Esse valor é proveniente do membro de **características do BIOS** da estrutura de **informações do BIOS** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="44e3c-118">This value comes from the **BIOS Characteristics** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="44e3c-119">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="44e3c-119">The possible values are.</span></span>

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="44e3c-120"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="44e3c-120"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span data-ttu-id="44e3c-121"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (1)</span><span class="sxs-lookup"><span data-stu-id="44e3c-121"><span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reserved** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44e3c-122"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="44e3c-122"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>

<span data-ttu-id="44e3c-123"><span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>**Características do BIOS sem suporte** (3)</span><span class="sxs-lookup"><span data-stu-id="44e3c-123"><span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>**BIOS Characteristics Not Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-124"><span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>**Há suporte para o ISA** (4)</span><span class="sxs-lookup"><span data-stu-id="44e3c-124"><span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>**ISA is supported** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-125"><span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>**Há suporte para MCA** (5)</span><span class="sxs-lookup"><span data-stu-id="44e3c-125"><span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>**MCA is supported** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-126"><span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>**Há suporte para EISA** (6)</span><span class="sxs-lookup"><span data-stu-id="44e3c-126"><span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>**EISA is supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-127"><span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>**PCI tem suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="44e3c-127"><span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>**PCI is supported** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-128"><span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Há suporte para PC Card (PCMCIA)** (8)</span><span class="sxs-lookup"><span data-stu-id="44e3c-128"><span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>**PC Card (PCMCIA) is supported** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-129"><span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>**Suporte a plug and Play** (9)</span><span class="sxs-lookup"><span data-stu-id="44e3c-129"><span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>**Plug and Play is supported** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-130"><span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>O **APM tem suporte** (10)</span><span class="sxs-lookup"><span data-stu-id="44e3c-130"><span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>**APM is supported** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>

<span data-ttu-id="44e3c-131"><span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>O **BIOS é atualizável (flash)** (11)</span><span class="sxs-lookup"><span data-stu-id="44e3c-131"><span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>**BIOS is Upgradeable (Flash)** (11)</span></span>


</dt> <dd>

<span data-ttu-id="44e3c-132">O BIOS é atualizável (flash)</span><span class="sxs-lookup"><span data-stu-id="44e3c-132">BIOS is Upgradable (Flash)</span></span>

</dd> <dt>

<span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>

<span data-ttu-id="44e3c-133"><span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>**Sombreamento de BIOS é permitido** (12)</span><span class="sxs-lookup"><span data-stu-id="44e3c-133"><span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>**BIOS shadowing is allowed** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-134"><span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>**Há suporte para VL-VESA** (13)</span><span class="sxs-lookup"><span data-stu-id="44e3c-134"><span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>**VL-VESA is supported** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>

<span data-ttu-id="44e3c-135"><span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>O **suporte a ESCD está disponível** (14)</span><span class="sxs-lookup"><span data-stu-id="44e3c-135"><span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>**ESCD support is available** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-136"><span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>**Há suporte para inicialização do CD** (15)</span><span class="sxs-lookup"><span data-stu-id="44e3c-136"><span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>**Boot from CD is supported** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-137"><span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>**Há suporte para a inicialização selecionável** (16)</span><span class="sxs-lookup"><span data-stu-id="44e3c-137"><span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>**Selectable Boot is supported** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>

<span data-ttu-id="44e3c-138"><span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>**BIOS ROM está em soquete** (17)</span><span class="sxs-lookup"><span data-stu-id="44e3c-138"><span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>**BIOS ROM is socketed** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-139"><span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>A **inicialização do PC Card (PCMCIA) tem suporte** (18)</span><span class="sxs-lookup"><span data-stu-id="44e3c-139"><span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Boot From PC Card (PCMCIA) is supported** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-140"><span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>**Há suporte para a especificação EDD (unidade de disco avançada)** (19)</span><span class="sxs-lookup"><span data-stu-id="44e3c-140"><span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>**EDD (Enhanced Disk Drive) Specification is supported** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-141"><span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>**Int 13h-disquete japonês para NEC 9800 1.2 MB (3,5 \\ ", 1K bytes/setor, 360 rpm) tem suporte** (20)</span><span class="sxs-lookup"><span data-stu-id="44e3c-141"><span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>**Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5\\", 1k Bytes/Sector, 360 RPM) is supported** (20)</span></span>


</dt> <dd>

<span data-ttu-id="44e3c-142">Int 13h-disquete japonês para NEC 9800 1,2 MB (3,5, 1K bytes/setor, 360 RPM) tem suporte</span><span class="sxs-lookup"><span data-stu-id="44e3c-142">Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5, 1k Bytes/Sector, 360 RPM) is supported</span></span>

</dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-143"><span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>**Int 13h-há suporte para o disquete japonês para o Toshiba 1.2 MB (3,5 \\ ", 360 rpm)** (21)</span><span class="sxs-lookup"><span data-stu-id="44e3c-143"><span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>**Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5\\", 360 RPM) is supported** (21)</span></span>


</dt> <dd>

<span data-ttu-id="44e3c-144">Int 13h-há suporte para o disquete japonês para o Toshiba 1.2 MB (3,5, 360 RPM)</span><span class="sxs-lookup"><span data-stu-id="44e3c-144">Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5, 360 RPM) is supported</span></span>

</dd> <dt>

<span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="44e3c-145"><span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h-5,25 \\ "/360 KB há suporte para serviços de disquete** (22)</span><span class="sxs-lookup"><span data-stu-id="44e3c-145"><span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 5.25\\" / 360 KB Floppy Services are supported** (22)</span></span>


</dt> <dd>

<span data-ttu-id="44e3c-146">Há suporte para os serviços de disquete int 13h-5,25/360 KB</span><span class="sxs-lookup"><span data-stu-id="44e3c-146">Int 13h - 5.25 / 360 KB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="44e3c-147"><span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h-5,25 \\ "os serviços de disquete/1.2MB têm suporte** (23)</span><span class="sxs-lookup"><span data-stu-id="44e3c-147"><span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 5.25\\" /1.2MB Floppy Services are supported** (23)</span></span>


</dt> <dd>

<span data-ttu-id="44e3c-148">Int 13h-5,25 os serviços de disquete/1.2MB têm suporte</span><span class="sxs-lookup"><span data-stu-id="44e3c-148">Int 13h - 5.25 /1.2MB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>

<span data-ttu-id="44e3c-149"><span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>**Int 13h-3,5 \\ "/720 KB há suporte para serviços de disquete** (24)</span><span class="sxs-lookup"><span data-stu-id="44e3c-149"><span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>**Int 13h - 3.5\\" / 720 KB Floppy Services are supported** (24)</span></span>


</dt> <dd>

<span data-ttu-id="44e3c-150">Há suporte para os serviços de disquete int 13h-3,5/720 KB</span><span class="sxs-lookup"><span data-stu-id="44e3c-150">Int 13h - 3.5 / 720 KB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="44e3c-151"><span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h-3,5 \\ "/2,88 MB os serviços de disquete têm suporte** (25)</span><span class="sxs-lookup"><span data-stu-id="44e3c-151"><span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h - 3.5\\" / 2.88 MB Floppy Services are supported** (25)</span></span>


</dt> <dd>

<span data-ttu-id="44e3c-152">Há suporte para os serviços de disquete int 13h-3,5/2,88 MB</span><span class="sxs-lookup"><span data-stu-id="44e3c-152">Int 13h - 3.5 / 2.88 MB Floppy Services are supported</span></span>

</dd> <dt>

<span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-153"><span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>**Int 5h, há suporte para o serviço de tela de impressão** (26)</span><span class="sxs-lookup"><span data-stu-id="44e3c-153"><span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>**Int 5h, Print Screen Service is supported** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="44e3c-154"><span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>**Int 9h, há suporte para serviços de teclado 8042** (27)</span><span class="sxs-lookup"><span data-stu-id="44e3c-154"><span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>**Int 9h, 8042 Keyboard services are supported** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="44e3c-155"><span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>**Int 14h, há suporte para serviços seriais** (28)</span><span class="sxs-lookup"><span data-stu-id="44e3c-155"><span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>**Int 14h, Serial Services are supported** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="44e3c-156"><span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>**Int 17h, há suporte para serviços de impressora** (29)</span><span class="sxs-lookup"><span data-stu-id="44e3c-156"><span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>**Int 17h, printer services are supported** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>

<span data-ttu-id="44e3c-157"><span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>**Int 10h, há suporte para serviços de vídeo CGA/mono** (30)</span><span class="sxs-lookup"><span data-stu-id="44e3c-157"><span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>**Int 10h, CGA/Mono Video Services are supported** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="NEC_PC-98"></span><span id="nec_pc-98"></span>

<span data-ttu-id="44e3c-158"><span id="NEC_PC-98"></span><span id="nec_pc-98"></span>**NEC PC-98** (31)</span><span class="sxs-lookup"><span data-stu-id="44e3c-158"><span id="NEC_PC-98"></span><span id="nec_pc-98"></span>**NEC PC-98** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>

<span data-ttu-id="44e3c-159"><span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>**ACPI com suporte** (32)</span><span class="sxs-lookup"><span data-stu-id="44e3c-159"><span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>**ACPI supported** (32)</span></span>


</dt> <dd>

<span data-ttu-id="44e3c-160">Há suporte para ACPI</span><span class="sxs-lookup"><span data-stu-id="44e3c-160">ACPI is supported</span></span>

</dd> <dt>

<span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-161"><span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>O **USB Legacy tem suporte** (33)</span><span class="sxs-lookup"><span data-stu-id="44e3c-161"><span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>**USB Legacy is supported** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-162"><span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>**Suporte a AGP** (34)</span><span class="sxs-lookup"><span data-stu-id="44e3c-162"><span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>**AGP is supported** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-163"><span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>**Há suporte para a inicialização I2O** (35)</span><span class="sxs-lookup"><span data-stu-id="44e3c-163"><span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>**I2O boot is supported** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-164"><span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>**Há suporte para a inicialização LS-120** (36)</span><span class="sxs-lookup"><span data-stu-id="44e3c-164"><span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>**LS-120 boot is supported** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-165"><span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>A **inicialização da unidade Zip ATAPI tem suporte** (37)</span><span class="sxs-lookup"><span data-stu-id="44e3c-165"><span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>**ATAPI ZIP Drive boot is supported** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>

<span data-ttu-id="44e3c-166"><span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>**1394 a inicialização é suportada** (38)</span><span class="sxs-lookup"><span data-stu-id="44e3c-166"><span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>**1394 boot is supported** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>

<span data-ttu-id="44e3c-167"><span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>**Bateria inteligente com suporte** (39)</span><span class="sxs-lookup"><span data-stu-id="44e3c-167"><span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>**Smart Battery supported** (39)</span></span>


</dt> <dd>

<span data-ttu-id="44e3c-168">Há suporte para a bateria inteligente</span><span class="sxs-lookup"><span data-stu-id="44e3c-168">Smart Battery is supported</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-169">40 47</span><span class="sxs-lookup"><span data-stu-id="44e3c-169">40 47</span></span>
</dt> <dd>

<span data-ttu-id="44e3c-170">Reservado para o fornecedor do BIOS</span><span class="sxs-lookup"><span data-stu-id="44e3c-170">Reserved for BIOS vendor</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-171">48 63</span><span class="sxs-lookup"><span data-stu-id="44e3c-171">48 63</span></span>
</dt> <dd>

<span data-ttu-id="44e3c-172">Reservado para o fornecedor do sistema</span><span class="sxs-lookup"><span data-stu-id="44e3c-172">Reserved for system vendor</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="44e3c-173">**Biosversion**</span><span class="sxs-lookup"><span data-stu-id="44e3c-173">**BIOSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-174">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-174">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-176">Matriz das informações completas do BIOS do sistema.</span><span class="sxs-lookup"><span data-stu-id="44e3c-176">Array of the complete system BIOS information.</span></span> <span data-ttu-id="44e3c-177">Em muitos computadores, pode haver várias cadeias de caracteres de versão armazenadas no registro e representam as informações do BIOS do sistema.</span><span class="sxs-lookup"><span data-stu-id="44e3c-177">In many computers there can be several version strings that are stored in the registry and represent the system BIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-178">**BuildNumber**</span><span class="sxs-lookup"><span data-stu-id="44e3c-178">**BuildNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-181">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações do componente de software DMTF \| 2,4 ")</span><span class="sxs-lookup"><span data-stu-id="44e3c-181">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.4")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-182">Identificador interno desta compilação deste elemento de software.</span><span class="sxs-lookup"><span data-stu-id="44e3c-182">Internal identifier for this compilation of this software element.</span></span>

<span data-ttu-id="44e3c-183">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-183">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-184">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="44e3c-184">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-185">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-187">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="44e3c-187">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-188">Breve descrição do objeto de uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="44e3c-188">Short description of the object a one-line string.</span></span>

<span data-ttu-id="44e3c-189">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-190">**Código de**</span><span class="sxs-lookup"><span data-stu-id="44e3c-190">**CodeSet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-193">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="44e3c-193">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-194">Conjunto de códigos usado por este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="44e3c-194">Code set used by this software element.</span></span>

<span data-ttu-id="44e3c-195">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-195">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-196">**CurrentLanguage**</span><span class="sxs-lookup"><span data-stu-id="44e3c-196">**CurrentLanguage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-197">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-197">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-198">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-199">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 13 \| idioma atual")</span><span class="sxs-lookup"><span data-stu-id="44e3c-199">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Current Language")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-200">Nome do idioma atual do BIOS.</span><span class="sxs-lookup"><span data-stu-id="44e3c-200">Name of the current BIOS language.</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-201">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="44e3c-201">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-202">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-203">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-204">Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="44e3c-204">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-205">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="44e3c-205">Description of the object.</span></span>

<span data-ttu-id="44e3c-206">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-206">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-207">**EmbeddedControllerMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="44e3c-207">**EmbeddedControllerMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-208">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="44e3c-208">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-210">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| versão principal do firmware do controlador do tipo SMBIOS 0 \| ")</span><span class="sxs-lookup"><span data-stu-id="44e3c-210">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|Embedded Controller Firmware Major Release")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-211">A versão principal do firmware do controlador incorporado.</span><span class="sxs-lookup"><span data-stu-id="44e3c-211">The major release of the embedded controller firmware.</span></span>

<span data-ttu-id="44e3c-212">Esse valor é proveniente do membro de **liberação principal do firmware do controlador incorporado** da estrutura de **informações do BIOS** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="44e3c-212">This value comes from the **Embedded Controller Firmware Major Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="44e3c-213">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="44e3c-213">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-214">**EmbeddedControllerMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="44e3c-214">**EmbeddedControllerMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-215">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="44e3c-215">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-216">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-216">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-217">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| versão secundária do firmware do controlador do tipo SMBIOS 0 \| ")</span><span class="sxs-lookup"><span data-stu-id="44e3c-217">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|Embedded Controller Firmware Minor Release")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-218">A versão secundária do firmware do controlador incorporado.</span><span class="sxs-lookup"><span data-stu-id="44e3c-218">The minor release of the embedded controller firmware.</span></span>

<span data-ttu-id="44e3c-219">Esse valor é proveniente do membro de **liberação secundária do firmware do controlador incorporado** da estrutura de **informações do BIOS** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="44e3c-219">This value comes from the **Embedded Controller Firmware Minor Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="44e3c-220">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="44e3c-220">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-221">**IdentificationCode**</span><span class="sxs-lookup"><span data-stu-id="44e3c-221">**IdentificationCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-224">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações do componente de software DMTF \| 2,7 ")</span><span class="sxs-lookup"><span data-stu-id="44e3c-224">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.7")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-225">Identificador do fabricante para este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="44e3c-225">Manufacturer's identifier for this software element.</span></span> <span data-ttu-id="44e3c-226">Geralmente, essa será uma SKU (unidade de manutenção de estoque) ou um número de peça.</span><span class="sxs-lookup"><span data-stu-id="44e3c-226">Often this will be a stock keeping unit (SKU) or a part number.</span></span>

<span data-ttu-id="44e3c-227">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-227">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-228">**InstallableLanguages**</span><span class="sxs-lookup"><span data-stu-id="44e3c-228">**InstallableLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-229">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44e3c-229">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-231">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 13 \| idiomas instaláveis")</span><span class="sxs-lookup"><span data-stu-id="44e3c-231">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Installable Languages")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-232">Número de idiomas disponíveis para instalação neste sistema.</span><span class="sxs-lookup"><span data-stu-id="44e3c-232">Number of languages available for installation on this system.</span></span> <span data-ttu-id="44e3c-233">A linguagem pode determinar propriedades como a necessidade de texto Unicode e bidirecional.</span><span class="sxs-lookup"><span data-stu-id="44e3c-233">Language may determine properties such as the need for Unicode and bidirectional text.</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-234">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="44e3c-234">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-235">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="44e3c-235">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-237">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="44e3c-237">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-238">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="44e3c-238">Date and time the object was installed.</span></span> <span data-ttu-id="44e3c-239">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="44e3c-239">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="44e3c-240">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-240">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-241">**LanguageEdition**</span><span class="sxs-lookup"><span data-stu-id="44e3c-241">**LanguageEdition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-242">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-243">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-244">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações do componente de software DMTF \| 2,6 ")</span><span class="sxs-lookup"><span data-stu-id="44e3c-244">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.6")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-245">Language Edition deste elemento de software.</span><span class="sxs-lookup"><span data-stu-id="44e3c-245">Language edition of this software element.</span></span> <span data-ttu-id="44e3c-246">Os códigos de idioma definidos no ISO 639 devem ser usados.</span><span class="sxs-lookup"><span data-stu-id="44e3c-246">The language codes defined in ISO 639 should be used.</span></span> <span data-ttu-id="44e3c-247">Onde o elemento software representa uma versão multilíngue ou internacional de um produto, a cadeia de caracteres "multilíngue" deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="44e3c-247">Where the software element represents a multilingual or international version of a product, the string "multilingual" should be used.</span></span>

<span data-ttu-id="44e3c-248">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-248">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-249">**ListOfLanguages**</span><span class="sxs-lookup"><span data-stu-id="44e3c-249">**ListOfLanguages**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-250">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-250">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-252">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 13 \| Language Strings")</span><span class="sxs-lookup"><span data-stu-id="44e3c-252">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 13\|Language Strings")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-253">Matriz de nomes de idiomas do BIOS instaláveis disponíveis.</span><span class="sxs-lookup"><span data-stu-id="44e3c-253">Array of names of available BIOS-installable languages.</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-254">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="44e3c-254">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-255">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-256">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-257">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="44e3c-257">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-258">Fabricante deste elemento de software.</span><span class="sxs-lookup"><span data-stu-id="44e3c-258">Manufacturer of this software element.</span></span>

<span data-ttu-id="44e3c-259">Esse valor é proveniente do membro do **fornecedor** da estrutura de **informações do BIOS** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="44e3c-259">This value comes from the **Vendor** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="44e3c-260">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-260">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-261">**Nome**</span><span class="sxs-lookup"><span data-stu-id="44e3c-261">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-262">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-262">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-263">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-263">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-264">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="44e3c-264">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-265">Nome usado para identificar este elemento de software.</span><span class="sxs-lookup"><span data-stu-id="44e3c-265">Name used to identify this software element.</span></span>

<span data-ttu-id="44e3c-266">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-266">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-267">**OtherTargetOS**</span><span class="sxs-lookup"><span data-stu-id="44e3c-267">**OtherTargetOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-268">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-268">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-269">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-270">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**sistema \_ operacional CIM**](cim-operatingsystem.md).**OtherTypeDescription**")</span><span class="sxs-lookup"><span data-stu-id="44e3c-270">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-271">Registra o tipo de fabricante e sistema operacional para um elemento de software quando a propriedade **TargetOperatingSystem** tem um valor de 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="44e3c-271">Records the manufacturer and operating system type for a software element when the **TargetOperatingSystem** property has a value of 1 (Other).</span></span> <span data-ttu-id="44e3c-272">Quando **TargetOperatingSystem** tem um valor de 1, **OtherTargetOS** deve ter um valor não nulo.</span><span class="sxs-lookup"><span data-stu-id="44e3c-272">When **TargetOperatingSystem** has a value of 1, **OtherTargetOS** must have a nonnull value.</span></span> <span data-ttu-id="44e3c-273">Para todos os outros valores de **TargetOperatingSystem**, **OtherTargetOS** é **nulo**.</span><span class="sxs-lookup"><span data-stu-id="44e3c-273">For all other values of **TargetOperatingSystem**, **OtherTargetOS** is **NULL**.</span></span>

<span data-ttu-id="44e3c-274">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-274">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-275">**PrimaryBIOS**</span><span class="sxs-lookup"><span data-stu-id="44e3c-275">**PrimaryBIOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-276">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="44e3c-276">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-277">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-277">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-278">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS do sistema DMTF \| 1,9 ")</span><span class="sxs-lookup"><span data-stu-id="44e3c-278">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System BIOS\|001.9")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-279">Se for **true**, esse é o BIOS primário do sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="44e3c-279">If **TRUE**, this is the primary BIOS of the computer system.</span></span>

<span data-ttu-id="44e3c-280">Essa propriedade é herdada do [**CIM \_ bioselement**](cim-bioselement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-280">This property is inherited from [**CIM\_BIOSElement**](cim-bioselement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-281">**Liberado**</span><span class="sxs-lookup"><span data-stu-id="44e3c-281">**ReleaseDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-282">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="44e3c-282">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-284">Data de lançamento do BIOS do Windows no formato UTC (tempo Universal Coordenado) de AAAAMMDDHHMMSS. MMMMMM (+-) OOO.</span><span class="sxs-lookup"><span data-stu-id="44e3c-284">Release date of the Windows BIOS in the Coordinated Universal Time (UTC) format of YYYYMMDDHHMMSS.MMMMMM(+-)OOO.</span></span>

<span data-ttu-id="44e3c-285">Esse valor é proveniente do membro de **data de lançamento do BIOS** da estrutura de **informações do BIOS** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="44e3c-285">This value comes from the **BIOS Release Date** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-286">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="44e3c-286">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-287">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-287">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-288">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-288">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-289">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,4 ")</span><span class="sxs-lookup"><span data-stu-id="44e3c-289">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-290">Número de série atribuído do elemento de software.</span><span class="sxs-lookup"><span data-stu-id="44e3c-290">Assigned serial number of the software element.</span></span>

<span data-ttu-id="44e3c-291">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-291">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-292">**SMBIOSBIOSVersion**</span><span class="sxs-lookup"><span data-stu-id="44e3c-292">**SMBIOSBIOSVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-293">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-294">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-295">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| versão do SMBIOS do tipo 0")</span><span class="sxs-lookup"><span data-stu-id="44e3c-295">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|BIOS Version")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-296">Versão do BIOS conforme relatado pelo SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="44e3c-296">BIOS version as reported by SMBIOS.</span></span>

<span data-ttu-id="44e3c-297">Esse valor é proveniente do membro da **versão do BIOS** da estrutura de **informações do BIOS** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="44e3c-297">This value comes from the **BIOS Version** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-298">**SMBIOSMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="44e3c-298">**SMBIOSMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-299">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44e3c-299">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-300">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-301">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| GetVersion")</span><span class="sxs-lookup"><span data-stu-id="44e3c-301">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|GetVersion")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-302">Número de versão principal do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="44e3c-302">Major SMBIOS version number.</span></span> <span data-ttu-id="44e3c-303">Essa propriedade será **nula** se o Smbios não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="44e3c-303">This property is **NULL** if SMBIOS is not found.</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-304">**SMBIOSMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="44e3c-304">**SMBIOSMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-305">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44e3c-305">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-306">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-307">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| GetVersion")</span><span class="sxs-lookup"><span data-stu-id="44e3c-307">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|GetVersion")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-308">Número de versão do SMBIOS secundário.</span><span class="sxs-lookup"><span data-stu-id="44e3c-308">Minor SMBIOS version number.</span></span> <span data-ttu-id="44e3c-309">Essa propriedade será **nula** se o Smbios não for encontrado.</span><span class="sxs-lookup"><span data-stu-id="44e3c-309">This property is **NULL** if SMBIOS is not found.</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-310">**SMBIOSPresent**</span><span class="sxs-lookup"><span data-stu-id="44e3c-310">**SMBIOSPresent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-311">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="44e3c-311">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-312">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-312">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-313">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| init")</span><span class="sxs-lookup"><span data-stu-id="44e3c-313">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|CSMBios\|Init")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-314">Se for **true**, o Smbios estará disponível neste sistema de computador.</span><span class="sxs-lookup"><span data-stu-id="44e3c-314">If **true**, the SMBIOS is available on this computer system.</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-315">**SoftwareElementID**</span><span class="sxs-lookup"><span data-stu-id="44e3c-315">**SoftwareElementID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-316">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-316">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-317">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-317">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-318">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="44e3c-318">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-319">Identificador para este elemento de software; projetado para ser usado em conjunto com outras chaves para criar uma representação exclusiva dessa instância.</span><span class="sxs-lookup"><span data-stu-id="44e3c-319">Identifier for this software element; designed to be used in conjunction with other keys to create a unique representation of this instance.</span></span>

<span data-ttu-id="44e3c-320">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-320">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-321">**SoftwareElementState**</span><span class="sxs-lookup"><span data-stu-id="44e3c-321">**SoftwareElementState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-322">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44e3c-322">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-323">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-323">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-324">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="44e3c-324">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-325">Estado de um elemento de software.</span><span class="sxs-lookup"><span data-stu-id="44e3c-325">State of a software element.</span></span>

<span data-ttu-id="44e3c-326">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-326">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="44e3c-327">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="44e3c-327">The possible values are.</span></span>

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

<span data-ttu-id="44e3c-328">**Implantável** (0)</span><span class="sxs-lookup"><span data-stu-id="44e3c-328">**Deployable** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

<span data-ttu-id="44e3c-329">**Instalável** (1)</span><span class="sxs-lookup"><span data-stu-id="44e3c-329">**Installable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

<span data-ttu-id="44e3c-330">**Executável** (2)</span><span class="sxs-lookup"><span data-stu-id="44e3c-330">**Executable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span data-ttu-id="44e3c-331">**Em execução** (3)</span><span class="sxs-lookup"><span data-stu-id="44e3c-331">**Running** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="44e3c-332">**Status**</span><span class="sxs-lookup"><span data-stu-id="44e3c-332">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-333">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-333">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-334">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-334">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-335">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")</span><span class="sxs-lookup"><span data-stu-id="44e3c-335">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-336">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="44e3c-336">Current status of the object.</span></span> <span data-ttu-id="44e3c-337">Vários status de operação e não operacional podem ser definidos.</span><span class="sxs-lookup"><span data-stu-id="44e3c-337">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="44e3c-338">Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="44e3c-338">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="44e3c-339">Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço".</span><span class="sxs-lookup"><span data-stu-id="44e3c-339">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="44e3c-340">O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo.</span><span class="sxs-lookup"><span data-stu-id="44e3c-340">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="44e3c-341">Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.</span><span class="sxs-lookup"><span data-stu-id="44e3c-341">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="44e3c-342">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-342">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="44e3c-343">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="44e3c-343">The possible values are.</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="44e3c-344">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="44e3c-344">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="44e3c-345">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="44e3c-345">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="44e3c-346">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="44e3c-346">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44e3c-347">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="44e3c-347">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="44e3c-348">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="44e3c-348">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="44e3c-349">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="44e3c-349">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="44e3c-350">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="44e3c-350">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="44e3c-351">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="44e3c-351">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="44e3c-352">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="44e3c-352">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="44e3c-353">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="44e3c-353">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="44e3c-354">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="44e3c-354">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="44e3c-355">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="44e3c-355">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="44e3c-356">**SystemBiosMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="44e3c-356">**SystemBiosMajorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-357">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="44e3c-357">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-358">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-358">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-359">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| versão principal do BIOS do sistema do SMBIOS tipo 0")</span><span class="sxs-lookup"><span data-stu-id="44e3c-359">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|System BIOS Major Release")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-360">A versão principal do BIOS do sistema.</span><span class="sxs-lookup"><span data-stu-id="44e3c-360">The major release of the System BIOS.</span></span>

<span data-ttu-id="44e3c-361">Esse valor é proveniente do membro da **versão principal do BIOS do sistema** da estrutura de **informações do BIOS** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="44e3c-361">This value comes from the **System BIOS Major Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="44e3c-362">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="44e3c-362">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-363">**SystemBiosMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="44e3c-363">**SystemBiosMinorVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-364">Tipo de dados: **uint8**</span><span class="sxs-lookup"><span data-stu-id="44e3c-364">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-365">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-365">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-366">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| versão secundária do BIOS do sistema do tipo SMBIOS 0")</span><span class="sxs-lookup"><span data-stu-id="44e3c-366">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 0\|System BIOS Minor Release")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-367">A versão secundária do BIOS do sistema.</span><span class="sxs-lookup"><span data-stu-id="44e3c-367">The minor release of the System BIOS.</span></span>

<span data-ttu-id="44e3c-368">Esse valor é proveniente do membro da **versão secundária do BIOS do sistema** da estrutura de **informações do BIOS** nas informações do SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="44e3c-368">This value comes from the **System BIOS Minor Release** member of the **BIOS Information** structure in the SMBIOS information.</span></span>

<span data-ttu-id="44e3c-369">**Windows server 2012 R2, Windows 8.1, Windows server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** Não há suporte para essa propriedade antes do Windows 10 e do Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="44e3c-369">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** This property is not supported before Windows 10 and Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="44e3c-370">**TargetOperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="44e3c-370">**TargetOperatingSystem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-371">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="44e3c-371">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-372">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-372">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-373">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações de componente de software DMTF \| 2,5 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (" sistema [**\_ operacional CIM**](cim-operatingsystem.md).**OSType**")</span><span class="sxs-lookup"><span data-stu-id="44e3c-373">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Software Component Information\|002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_OperatingSystem**](cim-operatingsystem.md).**OSType**")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-374">Sistema operacional de destino do elemento de software proprietário.</span><span class="sxs-lookup"><span data-stu-id="44e3c-374">Target operating system of the owning software element.</span></span>

<span data-ttu-id="44e3c-375">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-375">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

<span data-ttu-id="44e3c-376">Os valores possíveis são.</span><span class="sxs-lookup"><span data-stu-id="44e3c-376">The possible values are.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="44e3c-377">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="44e3c-377">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="44e3c-378">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="44e3c-378">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

<span data-ttu-id="44e3c-379">**MACOS** (2)</span><span class="sxs-lookup"><span data-stu-id="44e3c-379">**MACOS** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

<span data-ttu-id="44e3c-380">**ATTUNIX** (3)</span><span class="sxs-lookup"><span data-stu-id="44e3c-380">**ATTUNIX** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

<span data-ttu-id="44e3c-381">**DGUX** (4)</span><span class="sxs-lookup"><span data-stu-id="44e3c-381">**DGUX** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

<span data-ttu-id="44e3c-382">**DECNT** (5)</span><span class="sxs-lookup"><span data-stu-id="44e3c-382">**DECNT** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

<span data-ttu-id="44e3c-383">**Unix Digital** (6)</span><span class="sxs-lookup"><span data-stu-id="44e3c-383">**Digital Unix** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

<span data-ttu-id="44e3c-384">**OpenVMS** (7)</span><span class="sxs-lookup"><span data-stu-id="44e3c-384">**OpenVMS** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

<span data-ttu-id="44e3c-385">HP **(8** )</span><span class="sxs-lookup"><span data-stu-id="44e3c-385">**HPUX** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

<span data-ttu-id="44e3c-386">**AIX** (9)</span><span class="sxs-lookup"><span data-stu-id="44e3c-386">**AIX** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

<span data-ttu-id="44e3c-387">**MVS** (10)</span><span class="sxs-lookup"><span data-stu-id="44e3c-387">**MVS** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

<span data-ttu-id="44e3c-388">**OS400** (11)</span><span class="sxs-lookup"><span data-stu-id="44e3c-388">**OS400** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

<span data-ttu-id="44e3c-389">**Sistema operacional/2** (12)</span><span class="sxs-lookup"><span data-stu-id="44e3c-389">**OS/2** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

<span data-ttu-id="44e3c-390">**JavaVM** (13)</span><span class="sxs-lookup"><span data-stu-id="44e3c-390">**JavaVM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

<span data-ttu-id="44e3c-391">**MSDOS** (14)</span><span class="sxs-lookup"><span data-stu-id="44e3c-391">**MSDOS** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

<span data-ttu-id="44e3c-392">**WIN3x** (15)</span><span class="sxs-lookup"><span data-stu-id="44e3c-392">**WIN3x** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

<span data-ttu-id="44e3c-393">**Win95** (16)</span><span class="sxs-lookup"><span data-stu-id="44e3c-393">**WIN95** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

<span data-ttu-id="44e3c-394">**Win98** (17)</span><span class="sxs-lookup"><span data-stu-id="44e3c-394">**WIN98** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

<span data-ttu-id="44e3c-395">**WinNT** (18)</span><span class="sxs-lookup"><span data-stu-id="44e3c-395">**WINNT** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

<span data-ttu-id="44e3c-396">**WinCE** (19)</span><span class="sxs-lookup"><span data-stu-id="44e3c-396">**WINCE** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

<span data-ttu-id="44e3c-397">**NCR3000** (20)</span><span class="sxs-lookup"><span data-stu-id="44e3c-397">**NCR3000** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

<span data-ttu-id="44e3c-398">**NetWare** (21)</span><span class="sxs-lookup"><span data-stu-id="44e3c-398">**NetWare** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

<span data-ttu-id="44e3c-399">**Uso** (22)</span><span class="sxs-lookup"><span data-stu-id="44e3c-399">**OSF** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

<span data-ttu-id="44e3c-400">**DC/os** (23)</span><span class="sxs-lookup"><span data-stu-id="44e3c-400">**DC/OS** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

<span data-ttu-id="44e3c-401">**Unix dependente** (24)</span><span class="sxs-lookup"><span data-stu-id="44e3c-401">**Reliant UNIX** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

<span data-ttu-id="44e3c-402">**SCO UnixWare** (25)</span><span class="sxs-lookup"><span data-stu-id="44e3c-402">**SCO UnixWare** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

<span data-ttu-id="44e3c-403">**SCO OpenServer** (26)</span><span class="sxs-lookup"><span data-stu-id="44e3c-403">**SCO OpenServer** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

<span data-ttu-id="44e3c-404">**Subsequentes** (27)</span><span class="sxs-lookup"><span data-stu-id="44e3c-404">**Sequent** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

<span data-ttu-id="44e3c-405">**IRIX** (28)</span><span class="sxs-lookup"><span data-stu-id="44e3c-405">**IRIX** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

<span data-ttu-id="44e3c-406">**Solaris** (29)</span><span class="sxs-lookup"><span data-stu-id="44e3c-406">**Solaris** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

<span data-ttu-id="44e3c-407">**SunOS** (30)</span><span class="sxs-lookup"><span data-stu-id="44e3c-407">**SunOS** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

<span data-ttu-id="44e3c-408">**U6000** (31)</span><span class="sxs-lookup"><span data-stu-id="44e3c-408">**U6000** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

<span data-ttu-id="44e3c-409">**ASeries** (32)</span><span class="sxs-lookup"><span data-stu-id="44e3c-409">**ASERIES** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

<span data-ttu-id="44e3c-410">**TandemNSK** (33)</span><span class="sxs-lookup"><span data-stu-id="44e3c-410">**TandemNSK** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

<span data-ttu-id="44e3c-411">**TandemNT** (34)</span><span class="sxs-lookup"><span data-stu-id="44e3c-411">**TandemNT** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

<span data-ttu-id="44e3c-412">**BS2000** (35)</span><span class="sxs-lookup"><span data-stu-id="44e3c-412">**BS2000** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

<span data-ttu-id="44e3c-413">**Linux** (36)</span><span class="sxs-lookup"><span data-stu-id="44e3c-413">**LINUX** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

<span data-ttu-id="44e3c-414">**Lynx** (37)</span><span class="sxs-lookup"><span data-stu-id="44e3c-414">**Lynx** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

<span data-ttu-id="44e3c-415">**Xenix** (38)</span><span class="sxs-lookup"><span data-stu-id="44e3c-415">**XENIX** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

<span data-ttu-id="44e3c-416">**VM/ESA** (39)</span><span class="sxs-lookup"><span data-stu-id="44e3c-416">**VM/ESA** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

<span data-ttu-id="44e3c-417">**Unix interativo** (40)</span><span class="sxs-lookup"><span data-stu-id="44e3c-417">**Interactive UNIX** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

<span data-ttu-id="44e3c-418">**BSDUNIX** (41)</span><span class="sxs-lookup"><span data-stu-id="44e3c-418">**BSDUNIX** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

<span data-ttu-id="44e3c-419">**FreeBSD** (42)</span><span class="sxs-lookup"><span data-stu-id="44e3c-419">**FreeBSD** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

<span data-ttu-id="44e3c-420">**NetBSD** (43)</span><span class="sxs-lookup"><span data-stu-id="44e3c-420">**NetBSD** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

<span data-ttu-id="44e3c-421">**GNU Hurd** (44)</span><span class="sxs-lookup"><span data-stu-id="44e3c-421">**GNU Hurd** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

<span data-ttu-id="44e3c-422">**OS9** (45)</span><span class="sxs-lookup"><span data-stu-id="44e3c-422">**OS9** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

<span data-ttu-id="44e3c-423">**Kernel Mach** (46)</span><span class="sxs-lookup"><span data-stu-id="44e3c-423">**MACH Kernel** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

<span data-ttu-id="44e3c-424">**Inferno** (47)</span><span class="sxs-lookup"><span data-stu-id="44e3c-424">**Inferno** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

<span data-ttu-id="44e3c-425">**QNX** (48)</span><span class="sxs-lookup"><span data-stu-id="44e3c-425">**QNX** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

<span data-ttu-id="44e3c-426">**EPOC** (49)</span><span class="sxs-lookup"><span data-stu-id="44e3c-426">**EPOC** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

<span data-ttu-id="44e3c-427">**IxWorks** (50)</span><span class="sxs-lookup"><span data-stu-id="44e3c-427">**IxWorks** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

<span data-ttu-id="44e3c-428">**VxWorks** (51)</span><span class="sxs-lookup"><span data-stu-id="44e3c-428">**VxWorks** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

<span data-ttu-id="44e3c-429">**Menta** (52)</span><span class="sxs-lookup"><span data-stu-id="44e3c-429">**MiNT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

<span data-ttu-id="44e3c-430">**BeOS** (53)</span><span class="sxs-lookup"><span data-stu-id="44e3c-430">**BeOS** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

<span data-ttu-id="44e3c-431">**HP MPE** (54)</span><span class="sxs-lookup"><span data-stu-id="44e3c-431">**HP MPE** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

<span data-ttu-id="44e3c-432">**NEXTSTEP** (55)</span><span class="sxs-lookup"><span data-stu-id="44e3c-432">**NextStep** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

<span data-ttu-id="44e3c-433">**PalmPilot** (56)</span><span class="sxs-lookup"><span data-stu-id="44e3c-433">**PalmPilot** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

<span data-ttu-id="44e3c-434">**Rhapsody** (57)</span><span class="sxs-lookup"><span data-stu-id="44e3c-434">**Rhapsody** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

<span data-ttu-id="44e3c-435">**Windows 2000** (58)</span><span class="sxs-lookup"><span data-stu-id="44e3c-435">**Windows 2000** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="44e3c-436">**Dedicado** (59)</span><span class="sxs-lookup"><span data-stu-id="44e3c-436">**Dedicated** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

<span data-ttu-id="44e3c-437">**VSE** (60)</span><span class="sxs-lookup"><span data-stu-id="44e3c-437">**VSE** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

<span data-ttu-id="44e3c-438">**TPF** (61)</span><span class="sxs-lookup"><span data-stu-id="44e3c-438">**TPF** (61)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="44e3c-439">**Versão**</span><span class="sxs-lookup"><span data-stu-id="44e3c-439">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44e3c-440">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="44e3c-440">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-441">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="44e3c-441">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="44e3c-442">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("versão"), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry de \| Descrição de hardware \\ \\ \\ \\ \| SystemBiosVersion")</span><span class="sxs-lookup"><span data-stu-id="44e3c-442">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Version"), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HARDWARE\\\\Description\\\\System\|SystemBiosVersion")</span></span>
</dt> </dl>

<span data-ttu-id="44e3c-443">Versão do BIOS.</span><span class="sxs-lookup"><span data-stu-id="44e3c-443">Version of the BIOS.</span></span> <span data-ttu-id="44e3c-444">Essa cadeia de caracteres é criada pelo fabricante do BIOS.</span><span class="sxs-lookup"><span data-stu-id="44e3c-444">This string is created by the BIOS manufacturer.</span></span>

<span data-ttu-id="44e3c-445">Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-445">This property is inherited from [**CIM\_SoftwareElement**](cim-softwareelement.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="44e3c-446">Comentários</span><span class="sxs-lookup"><span data-stu-id="44e3c-446">Remarks</span></span>

<span data-ttu-id="44e3c-447">A classe **Win32 \_ BIOS** é derivada de [**CIM \_ bioselement**](cim-bioselement.md).</span><span class="sxs-lookup"><span data-stu-id="44e3c-447">The **Win32\_BIOS** class is derived from [**CIM\_BIOSElement**](cim-bioselement.md).</span></span>

<span data-ttu-id="44e3c-448">As propriedades na classe **\_ BIOS do Win32** podem ser alteradas para um sistema de computador específico com o mesmo BIOS, por exemplo, inicializando por meio de um modo BIOS herdado versus inicializando por meio do modo de BIOS UEFI.</span><span class="sxs-lookup"><span data-stu-id="44e3c-448">The properties in the **Win32\_BIOS** class may change for a specific computer system with the same BIOS, for example booting through a legacy BIOS mode vs. booting through UEFI BIOS mode.</span></span> <span data-ttu-id="44e3c-449">No entanto, as propriedades recuperadas das estruturas do SMBIOS devem permanecer as mesmas.</span><span class="sxs-lookup"><span data-stu-id="44e3c-449">However the properties retrieved from the SMBIOS structures should remain the same.</span></span>

## <a name="examples"></a><span data-ttu-id="44e3c-450">Exemplos</span><span class="sxs-lookup"><span data-stu-id="44e3c-450">Examples</span></span>

<span data-ttu-id="44e3c-451">As [informações do computador get-ComputerInfo-Query de computadores locais/remotos-(WMI) exemplo do](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell na galeria do TechNet usam várias chamadas para hardware e software, incluindo o **Win32 \_ BIOS**, para exibir informações sobre um sistema local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="44e3c-451">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_BIOS**, to display information about a local or remote system.</span></span>

<span data-ttu-id="44e3c-452">A amostra [gerar informações do sistema como uma hierarquia XML](https://Gallery.TechNet.Microsoft.Com/Generate-system-information-3f40629f) do VBScript na galeria do TechNet usa várias chamadas para hardware e software, incluindo o **Win32 \_ BIOS**, para gerar uma representação XML de um sistema usando uma saída de XML manual.</span><span class="sxs-lookup"><span data-stu-id="44e3c-452">The [Generate system information as XML hierarchy](https://Gallery.TechNet.Microsoft.Com/Generate-system-information-3f40629f) VBScript sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_BIOS**, to generate an XML representation of a system using a manual XML output.</span></span>

<span data-ttu-id="44e3c-453">O exemplo de código do PowerShell a seguir usa o **\_ BIOS Win32** para retornar características do BIOS</span><span class="sxs-lookup"><span data-stu-id="44e3c-453">The following PowerShell code sample uses **Win32\_BIOS** to return characteristics of the BIOS</span></span>


```PowerShell
# wmi-win32_bios.ps1
# Demonstrates use of Win32_Bios WMI class
# Thomas Lee - tfl@psp.co.uk



# Helper function to return characterics of the BIOS
function get-WmiBiosCharacteristics {
param ([uint16] $char)

# parse and return values

If ($char -le 39) {

switch ($char) {
0   {"00-Reserved"}
1   {"01-Reserved"}
2   {"02-Unknown"}
3   {"03-BIOS Characteristics Not Supported"}
4   {"04-ISA is supported"}
5   {"05-MCA is supported"}
6   {"06-EISA is supported"}
7   {"07-PCI is supported"}
8   {"08-PC Card (PCMCIA) is supported"}
9   {"09-Plug and Play is supported"}
10  {"10-APM is supported"}
11  {"11-BIOS is Upgradable (Flash)"}
12  {"12-BIOS shadowing is allowed"}
13  {"13-VL-VESA is supported"}
14  {"14-ESCD support is available"}
15  {"15-Boot from CD is supported"}
16  {"16-Selectable Boot is supported"}
17  {"17-BIOS ROM is socketed"}
18  {"18-Boot From PC Card (PCMCIA) is supported"}
19  {"19-EDD (Enhanced Disk Drive) Specification is supported"}
20  {"20-Int 13h - Japanese Floppy for NEC 9800 1.2mb (3.5, 1k Bytes/Sector, 360 RPM) is supported"}
21  {"21-Int 13h - Japanese Floppy for Toshiba 1.2mb (3.5, 360 RPM) is supported"}
22  {"22-Int 13h - 5.25 / 360 KB Floppy Services are supported"}
23  {"23-Int 13h - 5.25 /1.2MB Floppy Services are supported"}
24  {"24-Int 13h - 3.5 / 720 KB Floppy Services are supported"}
25  {"25-Int 13h - 3.5 / 2.88 MB Floppy Services are supported"}
26  {"26-Int 5h, Print Screen Service is supported"}
27  {"27-Int 9h, 8042 Keyboard services are supported"}
28  {"28-Int 14h, Serial Services are supported"}
29  {"29-Int 17h, printer services are supported"}
30  {"30-Int 10h, CGA/Mono Video Services are supported"}
31  {"31-NEC PC-98"}
32  {"32-ACPI supported"}
33  {"33-USB Legacy is supported"}
34  {"34-AGP is supported"}
35  {"35-I2O boot is supported"}
36  {"36-LS-120 boot is supported"}
37  {"37-ATAPI ZIP Drive boot is supported"}
38  {"38-1394 boot is supported"}
39  {"39-Smart Battery supported"}
}
Return
}

If ($char -ge 40 -and $char -le 45) {
          "{0}-Reserved for BIOS vendor" -f $char
return
}

If ($char -ge 48 -and $char -le 63) {
           "{0}-Reserved for system vendor" -f $char
return
}
"{0}-Unknown Value " -f $char
}

# Get BIOS information from WMI
$bios = Get-WMIObject Win32_Bios

# Display BIOS Details
"Win32_Bios WMI Information"
"Bios Characteristics"
foreach ($ch in $bios.BiosCharacteristics) {
"                      :  {0}" -f  (Get-WmiBiosCharacteristics($ch))
} 
"Bios Version          :  {0}" -f $bios.BiosVersion
"Codeset               :  {0}" -f $bios.Codeset
"CurrentLanguage       :  {0}" -f $bios.CurrentLanguage
"Description           :  {0}" -f $bios.Description
"IdentificatonCode     :  {0}" -f $bios.IdentificatonCode
"InstallableLanguages  :  {0}" -f $bios.InstallableLanguages
"InstallDate           :  {0}" -f $bios.InstallDate 
"LanguageEdition       :  {0}" -f $bios.LanguageEdition
"ListOfLanguages       :  {0}" -f $bios.ListOfLanguages
"Manufacturer          :  {0}" -f $bios.Manufacturer
"OtherTargetOS         :  {0}" -f $bios.OtherTargetOS
"PrimaryBIOS           :  {0}" -f $bios.PrimaryBIOS
"ReleaseDate           :  {0}" -f $bios.ReleaseDate
"SerialNumber          :  {0}" -f $bios.SerialNumber
"SMBIOSBIOSVersion     :  {0}" -f $bios.SMBIOSBIOSVersion
"SMBIOSMajorVersion    :  {0}" -f $bios.SMBIOSMajorVersion
"SMBIOSMinorVersion    :  {0}" -f $bios.SMBIOSMinorVersion
"SoftwareElementID     :  {0}" -f $bios.SoftwareElementID 
"SoftwareElementState  :  {0}" -f $bios.SoftwareElementState
"TargetOperatingSystem :  {0}" -f $bios.TargetOperatingSystem
"Version               :  {0}" -f $bios.Version 
```



<span data-ttu-id="44e3c-454">O exemplo de código anterior retorna as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="44e3c-454">The previous code sample returns the following information:</span></span>

``` syntax
Win32_Bios WMI Information
Bios Characteristics
                      :  04-ISA is supported
                      :  07-PCI is supported
                      :  08-PC Card (PCMCIA) is supported
                      :  09-Plug and Play is supported
                      :  11-BIOS is Upgradable (Flash)
                      :  12-BIOS shadowing is allowed
                      :  15-Boot from CD is supported
                      :  16-Selectable Boot is supported
                      :  24-Int 13h - 3.5 / 720 KB Floppy Services are supported
                      :  26-Int 5h, Print Screen Service is supported
                      :  27-Int 9h, 8042 Keyboard services are supported
                      :  28-Int 14h, Serial Services are supported
                      :  29-Int 17h, printer services are supported
                      :  30-Int 10h, CGA/Mono Video Services are supported
                      :  32-ACPI supported
                      :  33-USB Legacy is supported
                      :  34-AGP is supported
                      :  39-Smart Battery supported
                      :  40-Reserved for BIOS vendor
                      :  41-Reserved for BIOS vendor
                      :  42-Reserved for BIOS vendor
                      :  58-Reserved for system vendor
                      :  74-Unknown Value
Bios Version          :  DELL   - 27d60a0d
Codeset               :
CurrentLanguage       :  en|US|iso8859-1
Description           :  Phoenix ROM BIOS PLUS Version 1.10 A04
IdentificatonCode     :
InstallableLanguages  :  1
InstallDate           :
LanguageEdition       :
ListOfLanguages       :  en|US|iso8859-1
Manufacturer          :  Dell Inc.
OtherTargetOS         :
PrimaryBIOS           :  True
ReleaseDate           :  20061013000000.000000+000
SerialNumber          :  DDC2H2J
SMBIOSBIOSVersion     :  A04
SMBIOSMajorVersion    :  2
SMBIOSMinorVersion    :  4
SoftwareElementID     :  Phoenix ROM BIOS PLUS Version 1.10 A04
SoftwareElementState  :  3
TargetOperatingSystem :  0
Version               :  DELL   - 27d60a0d
```

## <a name="requirements"></a><span data-ttu-id="44e3c-455">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44e3c-455">Requirements</span></span>



| <span data-ttu-id="44e3c-456">Requisito</span><span class="sxs-lookup"><span data-stu-id="44e3c-456">Requirement</span></span> | <span data-ttu-id="44e3c-457">Valor</span><span class="sxs-lookup"><span data-stu-id="44e3c-457">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44e3c-458">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44e3c-458">Minimum supported client</span></span><br/> | <span data-ttu-id="44e3c-459">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44e3c-459">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="44e3c-460">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="44e3c-460">Minimum supported server</span></span><br/> | <span data-ttu-id="44e3c-461">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44e3c-461">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="44e3c-462">Namespace</span><span class="sxs-lookup"><span data-stu-id="44e3c-462">Namespace</span></span><br/>                | <span data-ttu-id="44e3c-463">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="44e3c-463">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="44e3c-464">MOF</span><span class="sxs-lookup"><span data-stu-id="44e3c-464">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44e3c-465"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44e3c-465"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="44e3c-466">DLL</span><span class="sxs-lookup"><span data-stu-id="44e3c-466">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44e3c-467"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44e3c-467"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44e3c-468">Confira também</span><span class="sxs-lookup"><span data-stu-id="44e3c-468">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44e3c-469">**CIM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="44e3c-469">**CIM\_BIOSElement**</span></span>](cim-bioselement.md)
</dt> <dt>

[<span data-ttu-id="44e3c-470">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="44e3c-470">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

