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
ms.openlocfilehash: bda0a1a07de4411b9a8c683fb2c7e84156b658361df4f2eaf3aa5709c6d11a95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504286"
---
# <a name="win32_bios-class"></a>\_Classe do Win32 BIOS

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de **\_ BIOS do Win32** representa os atributos dos serviços de entrada/saída básicos (BIOS) do sistema de computador que estão instalados em um computador.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A classe **Win32 \_ BIOS** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ BIOS** tem essas propriedades.

<dl> <dt>

**BiosCharacteristics**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| \| características do BIOS do tipo SMBIOS 0")
</dt> </dl>

Matriz de características do BIOS com suporte do sistema conforme definido pela especificação de referência do BIOS do System Management.

Esse valor é proveniente do membro de **características do BIOS** da estrutura de **informações do BIOS** nas informações do SMBIOS.

Os valores possíveis são.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (0)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Reservado** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>

<span id="BIOS_Characteristics_Not_Supported"></span><span id="bios_characteristics_not_supported"></span><span id="BIOS_CHARACTERISTICS_NOT_SUPPORTED"></span>**Características do BIOS sem suporte** (3)


</dt> <dd></dd> <dt>

<span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>

<span id="ISA_is_supported"></span><span id="isa_is_supported"></span><span id="ISA_IS_SUPPORTED"></span>**Há suporte para o ISA** (4)


</dt> <dd></dd> <dt>

<span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>

<span id="MCA_is_supported"></span><span id="mca_is_supported"></span><span id="MCA_IS_SUPPORTED"></span>**Há suporte para MCA** (5)


</dt> <dd></dd> <dt>

<span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>

<span id="EISA_is_supported"></span><span id="eisa_is_supported"></span><span id="EISA_IS_SUPPORTED"></span>**Há suporte para EISA** (6)


</dt> <dd></dd> <dt>

<span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>

<span id="PCI_is_supported"></span><span id="pci_is_supported"></span><span id="PCI_IS_SUPPORTED"></span>**PCI tem suporte** (7)


</dt> <dd></dd> <dt>

<span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span id="PC_Card__PCMCIA__is_supported"></span><span id="pc_card__pcmcia__is_supported"></span><span id="PC_CARD__PCMCIA__IS_SUPPORTED"></span>**Há suporte para PC Card (PCMCIA)** (8)


</dt> <dd></dd> <dt>

<span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>

<span id="Plug_and_Play_is_supported"></span><span id="plug_and_play_is_supported"></span><span id="PLUG_AND_PLAY_IS_SUPPORTED"></span>**Suporte a plug and Play** (9)


</dt> <dd></dd> <dt>

<span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>

<span id="APM_is_supported"></span><span id="apm_is_supported"></span><span id="APM_IS_SUPPORTED"></span>O **APM tem suporte** (10)


</dt> <dd></dd> <dt>

<span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>

<span id="BIOS_is_Upgradeable__Flash_"></span><span id="bios_is_upgradeable__flash_"></span><span id="BIOS_IS_UPGRADEABLE__FLASH_"></span>O **BIOS é atualizável (flash)** (11)


</dt> <dd>

O BIOS é atualizável (flash)

</dd> <dt>

<span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>

<span id="BIOS_shadowing_is_allowed"></span><span id="bios_shadowing_is_allowed"></span><span id="BIOS_SHADOWING_IS_ALLOWED"></span>**Sombreamento de BIOS é permitido** (12)


</dt> <dd></dd> <dt>

<span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>

<span id="VL-VESA_is_supported"></span><span id="vl-vesa_is_supported"></span><span id="VL-VESA_IS_SUPPORTED"></span>**Há suporte para VL-VESA** (13)


</dt> <dd></dd> <dt>

<span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>

<span id="ESCD_support_is_available"></span><span id="escd_support_is_available"></span><span id="ESCD_SUPPORT_IS_AVAILABLE"></span>O **suporte a ESCD está disponível** (14)


</dt> <dd></dd> <dt>

<span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>

<span id="Boot_from_CD_is_supported"></span><span id="boot_from_cd_is_supported"></span><span id="BOOT_FROM_CD_IS_SUPPORTED"></span>**Há suporte para inicialização do CD** (15)


</dt> <dd></dd> <dt>

<span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>

<span id="Selectable_Boot_is_supported"></span><span id="selectable_boot_is_supported"></span><span id="SELECTABLE_BOOT_IS_SUPPORTED"></span>**Há suporte para a inicialização selecionável** (16)


</dt> <dd></dd> <dt>

<span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>

<span id="BIOS_ROM_is_socketed"></span><span id="bios_rom_is_socketed"></span><span id="BIOS_ROM_IS_SOCKETED"></span>**BIOS ROM está em soquete** (17)


</dt> <dd></dd> <dt>

<span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>

<span id="Boot_From_PC_Card__PCMCIA__is_supported"></span><span id="boot_from_pc_card__pcmcia__is_supported"></span><span id="BOOT_FROM_PC_CARD__PCMCIA__IS_SUPPORTED"></span>A **inicialização do PC Card (PCMCIA) tem suporte** (18)


</dt> <dd></dd> <dt>

<span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>

<span id="EDD__Enhanced_Disk_Drive__Specification_is_supported"></span><span id="edd__enhanced_disk_drive__specification_is_supported"></span><span id="EDD__ENHANCED_DISK_DRIVE__SPECIFICATION_IS_SUPPORTED"></span>**Há suporte para a especificação EDD (unidade de disco avançada)** (19)


</dt> <dd></dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>

<span id="Int_13h_-_Japanese_Floppy_for_NEC_9800_1.2mb__3.5____1k_Bytes_Sector__360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_nec_9800_1.2mb__3.5____1k_bytes_sector__360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_NEC_9800_1.2MB__3.5____1K_BYTES_SECTOR__360_RPM__IS_SUPPORTED"></span>**Int 13h-disquete japonês para NEC 9800 1.2 MB (3,5 \\ ", 1K bytes/setor, 360 rpm) tem suporte** (20)


</dt> <dd>

Int 13h-disquete japonês para NEC 9800 1,2 MB (3,5, 1K bytes/setor, 360 RPM) tem suporte

</dd> <dt>

<span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>

<span id="Int_13h_-_Japanese_Floppy_for_Toshiba_1.2mb__3.5____360_RPM__is_supported"></span><span id="int_13h_-_japanese_floppy_for_toshiba_1.2mb__3.5____360_rpm__is_supported"></span><span id="INT_13H_-_JAPANESE_FLOPPY_FOR_TOSHIBA_1.2MB__3.5____360_RPM__IS_SUPPORTED"></span>**Int 13h-há suporte para o disquete japonês para o Toshiba 1.2 MB (3,5 \\ ", 360 rpm)** (21)


</dt> <dd>

Int 13h-há suporte para o disquete japonês para o Toshiba 1.2 MB (3,5, 360 RPM)

</dd> <dt>

<span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span id="Int_13h_-_5.25_____360_KB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25_____360_kb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25_____360_KB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h-5,25 \\ "/360 KB há suporte para serviços de disquete** (22)


</dt> <dd>

Há suporte para os serviços de disquete int 13h-5,25/360 KB

</dd> <dt>

<span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span id="Int_13h_-_5.25____1.2MB_Floppy_Services_are_supported"></span><span id="int_13h_-_5.25____1.2mb_floppy_services_are_supported"></span><span id="INT_13H_-_5.25____1.2MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h-5,25 \\ "os serviços de disquete/1.2MB têm suporte** (23)


</dt> <dd>

Int 13h-5,25 os serviços de disquete/1.2MB têm suporte

</dd> <dt>

<span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>

<span id="Int_13h_-_3.5_____720_KB_Floppy_Services_are__supported"></span><span id="int_13h_-_3.5_____720_kb_floppy_services_are__supported"></span><span id="INT_13H_-_3.5_____720_KB_FLOPPY_SERVICES_ARE__SUPPORTED"></span>**Int 13h-3,5 \\ "/720 KB há suporte para serviços de disquete** (24)


</dt> <dd>

Há suporte para os serviços de disquete int 13h-3,5/720 KB

</dd> <dt>

<span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>

<span id="Int_13h_-_3.5_____2.88_MB_Floppy_Services_are_supported"></span><span id="int_13h_-_3.5_____2.88_mb_floppy_services_are_supported"></span><span id="INT_13H_-_3.5_____2.88_MB_FLOPPY_SERVICES_ARE_SUPPORTED"></span>**Int 13h-3,5 \\ "/2,88 MB os serviços de disquete têm suporte** (25)


</dt> <dd>

Há suporte para os serviços de disquete int 13h-3,5/2,88 MB

</dd> <dt>

<span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>

<span id="Int_5h__Print_Screen_Service_is_supported"></span><span id="int_5h__print_screen_service_is_supported"></span><span id="INT_5H__PRINT_SCREEN_SERVICE_IS_SUPPORTED"></span>**Int 5h, há suporte para o serviço de tela de impressão** (26)


</dt> <dd></dd> <dt>

<span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>

<span id="Int_9h__8042_Keyboard_services_are_supported"></span><span id="int_9h__8042_keyboard_services_are_supported"></span><span id="INT_9H__8042_KEYBOARD_SERVICES_ARE_SUPPORTED"></span>**Int 9h, há suporte para serviços de teclado 8042** (27)


</dt> <dd></dd> <dt>

<span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>

<span id="Int_14h__Serial_Services_are_supported"></span><span id="int_14h__serial_services_are_supported"></span><span id="INT_14H__SERIAL_SERVICES_ARE_SUPPORTED"></span>**Int 14h, há suporte para serviços seriais** (28)


</dt> <dd></dd> <dt>

<span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>

<span id="Int_17h__printer_services_are_supported"></span><span id="int_17h__printer_services_are_supported"></span><span id="INT_17H__PRINTER_SERVICES_ARE_SUPPORTED"></span>**Int 17h, há suporte para serviços de impressora** (29)


</dt> <dd></dd> <dt>

<span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>

<span id="Int_10h__CGA_Mono_Video_Services_are_supported"></span><span id="int_10h__cga_mono_video_services_are_supported"></span><span id="INT_10H__CGA_MONO_VIDEO_SERVICES_ARE_SUPPORTED"></span>**Int 10h, há suporte para serviços de vídeo CGA/mono** (30)


</dt> <dd></dd> <dt>

<span id="NEC_PC-98"></span><span id="nec_pc-98"></span>

<span id="NEC_PC-98"></span><span id="nec_pc-98"></span>**NEC PC-98** (31)


</dt> <dd></dd> <dt>

<span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>

<span id="ACPI_supported"></span><span id="acpi_supported"></span><span id="ACPI_SUPPORTED"></span>**ACPI com suporte** (32)


</dt> <dd>

Há suporte para ACPI

</dd> <dt>

<span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>

<span id="USB_Legacy_is_supported"></span><span id="usb_legacy_is_supported"></span><span id="USB_LEGACY_IS_SUPPORTED"></span>O **USB Legacy tem suporte** (33)


</dt> <dd></dd> <dt>

<span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>

<span id="AGP_is_supported"></span><span id="agp_is_supported"></span><span id="AGP_IS_SUPPORTED"></span>**Suporte a AGP** (34)


</dt> <dd></dd> <dt>

<span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>

<span id="I2O_boot_is_supported"></span><span id="i2o_boot_is_supported"></span><span id="I2O_BOOT_IS_SUPPORTED"></span>**Há suporte para a inicialização I2O** (35)


</dt> <dd></dd> <dt>

<span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>

<span id="LS-120_boot_is_supported"></span><span id="ls-120_boot_is_supported"></span><span id="LS-120_BOOT_IS_SUPPORTED"></span>**Há suporte para a inicialização LS-120** (36)


</dt> <dd></dd> <dt>

<span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>

<span id="ATAPI_ZIP_Drive_boot_is_supported"></span><span id="atapi_zip_drive_boot_is_supported"></span><span id="ATAPI_ZIP_DRIVE_BOOT_IS_SUPPORTED"></span>A **inicialização da unidade Zip ATAPI tem suporte** (37)


</dt> <dd></dd> <dt>

<span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>

<span id="1394_boot_is_supported"></span><span id="1394_BOOT_IS_SUPPORTED"></span>**1394 a inicialização é suportada** (38)


</dt> <dd></dd> <dt>

<span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>

<span id="Smart_Battery_supported"></span><span id="smart_battery_supported"></span><span id="SMART_BATTERY_SUPPORTED"></span>**Bateria inteligente com suporte** (39)


</dt> <dd>

Há suporte para a bateria inteligente

</dd> <dt>

40 47
</dt> <dd>

Reservado para o fornecedor do BIOS

</dd> <dt>

48 63
</dt> <dd>

Reservado para o fornecedor do sistema

</dd> </dl>

</dd> <dt>

**Biosversion**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz das informações completas do BIOS do sistema. Em muitos computadores, pode haver várias cadeias de caracteres de versão armazenadas no registro e representam as informações do BIOS do sistema.

</dd> <dt>

**BuildNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Informações do componente de software DMTF \| 2,4 ")
</dt> </dl>

Identificador interno desta compilação deste elemento de software.

Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")
</dt> </dl>

Breve descrição do objeto de uma cadeia de caracteres de uma linha.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Código de**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Conjunto de códigos usado por este elemento de software.

Essa propriedade é herdada de [**CIM \_ softwareelement**](cim-softwareelement.md).

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 13 \| idioma atual")
</dt> </dl>

Nome do idioma atual do BIOS.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")
</dt> </dl>

Descrição do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**EmbeddedControllerMajorVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 Embedded Controller Firmware Major \| Release")
</dt> </dl>

A versão principal do firmware do controlador inserido.

Esse valor vem do membro **versão principal** do firmware do controlador inserido da estrutura informações do **BIOS** nas informações do SMBIOS.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Essa propriedade não é suportada antes Windows 10 e Windows Server 2016.

</dd> <dt>

**EmbeddedControllerMinorVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 Embedded Controller Firmware Minor \| Release")
</dt> </dl>

A versão secundária do firmware do controlador inserido.

Esse valor vem do membro **versão secundária** do firmware do controlador inserido da estrutura informações **do BIOS** nas informações do SMBIOS.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Essa propriedade não é suportada antes Windows 10 e Windows Server 2016.

</dd> <dt>

**IdentificationCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Informações do componente de software DMTF \| \| 002.7")
</dt> </dl>

Identificador do fabricante para esse elemento de software. Geralmente, isso será uma SKU (unidade de manutenção de estoque) ou um número de parte.

Essa propriedade é herdada de [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> <dt>

**InstallableLanguages**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 13 \| Installable Languages")
</dt> </dl>

Número de idiomas disponíveis para instalação nesse sistema. O idioma pode determinar propriedades como a necessidade de Unicode e texto bidirecional.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data de instalação")
</dt> </dl>

Data e hora em que o objeto foi instalado. Essa propriedade não precisa de um valor para indicar que o objeto está instalado.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**LanguageEdition**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Informações do componente de software DMTF \| \| 002.6")
</dt> </dl>

Edição de linguagem deste elemento de software. Os códigos de idioma definidos no ISO 639 devem ser usados. Quando o elemento de software representa uma versão multilíngue ou internacional de um produto, a cadeia de caracteres "multilíngue" deve ser usada.

Essa propriedade é herdada de [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings ("Cadeias**](/windows/desktop/WmiSdk/standard-qualifiers) de caracteres de linguagem do tipo SMBIOS \| 13") \|
</dt> </dl>

Matriz de nomes de idiomas disponíveis que podem ser instalados pelo BIOS.

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. SISTEMA DMTF \| BIOS \| 001.2")
</dt> </dl>

Fabricante desse elemento de software.

Esse valor vem do **membro Vendor** da estrutura de Informações **do BIOS** nas informações do SMBIOS.

Essa propriedade é herdada de [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome usado para identificar esse elemento de software.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**OtherTargetOS**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OtherTypeDescription**")
</dt> </dl>

Registra o fabricante e o tipo de sistema operacional para um elemento de software quando a **propriedade TargetOperatingSystem** tem um valor de 1 (Outro). Quando **TargetOperatingSystem** tem um valor de 1, **OtherTargetOS** deve ter um valor nãonull. Para todos os outros valores de **TargetOperatingSystem,** **OtherTargetOS** é **NULL.**

Essa propriedade é herdada de [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. SISTEMA DMTF \| BIOS \| 001.9")
</dt> </dl>

Se **TRUE**, este é o BIOS primário do sistema de computador.

Essa propriedade é herdada de [**CIM \_ BIOSElement.**](cim-bioselement.md)

</dd> <dt>

**Releasedate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data de lançamento do Windows BIOS no formato TEMPO UNIVERSAL COORDENADO (UTC) de AAAAMMDDHHMMSS. MMMMMM(+-)OOO.

Esse valor vem do membro **Data de Lançamento do BIOS** da estrutura Informações do **BIOS** nas informações do SMBIOS.

</dd> <dt>

**Serialnumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.4")
</dt> </dl>

Número de série atribuído do elemento de software.

Essa propriedade é herdada de [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> <dt>

**SMBIOSBIOSVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 \| BIOS Version")
</dt> </dl>

Versão do BIOS conforme relatado por SMBIOS.

Esse valor vem do membro **versão do BIOS** da estrutura de Informações **do BIOS** nas informações do SMBIOS.

</dd> <dt>

**SMBIOSMajorVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| GetVersion")
</dt> </dl>

Número de versão principal do SMBIOS. Essa propriedade será **NULL** se SMBIOS não for encontrado.

</dd> <dt>

**SMBIOSMinorVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| GetVersion")
</dt> </dl>

Número de versão do SMBIOS secundário. Essa propriedade será **NULL** se SMBIOS não for encontrado.

</dd> <dt>

**SMBIOSPresent**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| CSMBios \| Init")
</dt> </dl>

Se **for true,** o SMBIOS estará disponível neste sistema de computador.

</dd> <dt>

**SoftwareElementID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador para este elemento de software; projetado para ser usado em conjunto com outras chaves para criar uma representação exclusiva dessa instância.

Essa propriedade é herdada de [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> <dt>

**SoftwareElementState**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Estado de um elemento de software.

Essa propriedade é herdada de [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

Os valores possíveis são.

<dt>

<span id="Deployable"></span><span id="deployable"></span><span id="DEPLOYABLE"></span>

**Implantável** (0)


</dt> <dd></dd> <dt>

<span id="Installable"></span><span id="installable"></span><span id="INSTALLABLE"></span>

**Instalável** (1)


</dt> <dd></dd> <dt>

<span id="Executable"></span><span id="executable"></span><span id="EXECUTABLE"></span>

**Executável** (2)


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**Executando** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Status atual do objeto. Vários status operacionais e não operacionais podem ser definidos. Os status operacionais incluem: "OK", "Degradado" e "Pred Fail" (um elemento, como uma unidade de disco rígido habilitada para SMART, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo). Os status nãooperacionais incluem: "Error", "Starting", "Stopping" e "Service". O último, "Serviço", pode ser aplicado durante o espelhamento de um disco, o recarregamento de uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros estados.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Os valores possíveis são.

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

**SystemBiosMajorVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 System \| BIOS Major Release")
</dt> </dl>

A versão principal do BIOS do sistema.

Esse valor vem do membro **da Versão Principal do BIOS** do Sistema da estrutura de Informações do **BIOS** nas informações do SMBIOS.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Essa propriedade não é suportada antes Windows 10 e Windows Server 2016.

</dd> <dt>

**SystemBiosMinorVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 0 System \| BIOS Minor Release")
</dt> </dl>

A versão secundária do BIOS do sistema.

Esse valor vem do membro da Versão **Secundária do BIOS** do Sistema da estrutura de Informações **do BIOS** nas informações do SMBIOS.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Essa propriedade não é suportada antes Windows 10 e Windows Server 2016.

</dd> <dt>

**TargetOperatingSystem**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Software Component Information \| 002.5"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ OperatingSystem**](cim-operatingsystem.md).**OSType**")
</dt> </dl>

Sistema operacional de destino do elemento de software de propriedade.

Essa propriedade é herdada de [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

Os valores possíveis são.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="MACOS"></span><span id="macos"></span>

**MACOS** (2)


</dt> <dd></dd> <dt>

<span id="ATTUNIX"></span><span id="attunix"></span>

**ATTUNIX** (3)


</dt> <dd></dd> <dt>

<span id="DGUX"></span><span id="dgux"></span>

**DGUX** (4)


</dt> <dd></dd> <dt>

<span id="DECNT"></span><span id="decnt"></span>

**DECNT** (5)


</dt> <dd></dd> <dt>

<span id="Digital_Unix"></span><span id="digital_unix"></span><span id="DIGITAL_UNIX"></span>

**Digital Unix** (6)


</dt> <dd></dd> <dt>

<span id="OpenVMS"></span><span id="openvms"></span><span id="OPENVMS"></span>

**OpenVMS** (7)


</dt> <dd></dd> <dt>

<span id="HPUX"></span><span id="hpux"></span>

**HPUX** (8)


</dt> <dd></dd> <dt>

<span id="AIX"></span><span id="aix"></span>

**AIX** (9)


</dt> <dd></dd> <dt>

<span id="MVS"></span><span id="mvs"></span>

**MVS** (10)


</dt> <dd></dd> <dt>

<span id="OS400"></span><span id="os400"></span>

**OS400** (11)


</dt> <dd></dd> <dt>

<span id="OS_2"></span><span id="os_2"></span>

**SO/2** (12)


</dt> <dd></dd> <dt>

<span id="JavaVM"></span><span id="javavm"></span><span id="JAVAVM"></span>

**JavaVM** (13)


</dt> <dd></dd> <dt>

<span id="MSDOS"></span><span id="msdos"></span>

**MSDOS** (14)


</dt> <dd></dd> <dt>

<span id="WIN3x"></span><span id="win3x"></span><span id="WIN3X"></span>

**WIN3x** (15)


</dt> <dd></dd> <dt>

<span id="WIN95"></span><span id="win95"></span>

**WIN95** (16)


</dt> <dd></dd> <dt>

<span id="WIN98"></span><span id="win98"></span>

**WIN98** (17)


</dt> <dd></dd> <dt>

<span id="WINNT"></span><span id="winnt"></span>

**WINNT** (18)


</dt> <dd></dd> <dt>

<span id="WINCE"></span><span id="wince"></span>

**WINCE** (19)


</dt> <dd></dd> <dt>

<span id="NCR3000"></span><span id="ncr3000"></span>

**NCR3000** (20)


</dt> <dd></dd> <dt>

<span id="NetWare"></span><span id="netware"></span><span id="NETWARE"></span>

**NetWare** (21)


</dt> <dd></dd> <dt>

<span id="OSF"></span><span id="osf"></span>

**OSF** (22)


</dt> <dd></dd> <dt>

<span id="DC_OS"></span><span id="dc_os"></span>

**DC/SO** (23)


</dt> <dd></dd> <dt>

<span id="Reliant_UNIX"></span><span id="reliant_unix"></span><span id="RELIANT_UNIX"></span>

**Reliant UNIX** (24)


</dt> <dd></dd> <dt>

<span id="SCO_UnixWare"></span><span id="sco_unixware"></span><span id="SCO_UNIXWARE"></span>

**SCO UnixWare** (25)


</dt> <dd></dd> <dt>

<span id="SCO_OpenServer"></span><span id="sco_openserver"></span><span id="SCO_OPENSERVER"></span>

**SCO OpenServer** (26)


</dt> <dd></dd> <dt>

<span id="Sequent"></span><span id="sequent"></span><span id="SEQUENT"></span>

**Sequenciado** (27)


</dt> <dd></dd> <dt>

<span id="IRIX"></span><span id="irix"></span>

**I LTDA** (28)


</dt> <dd></dd> <dt>

<span id="Solaris"></span><span id="solaris"></span><span id="SOLARIS"></span>

**Solaris** (29)


</dt> <dd></dd> <dt>

<span id="SunOS"></span><span id="sunos"></span><span id="SUNOS"></span>

**SunOS** (30)


</dt> <dd></dd> <dt>

<span id="U6000"></span><span id="u6000"></span>

**U6000** (31)


</dt> <dd></dd> <dt>

<span id="ASERIES"></span><span id="aseries"></span>

**ASERIES** (32)


</dt> <dd></dd> <dt>

<span id="TandemNSK"></span><span id="tandemnsk"></span><span id="TANDEMNSK"></span>

**TandemNSK** (33)


</dt> <dd></dd> <dt>

<span id="TandemNT"></span><span id="tandemnt"></span><span id="TANDEMNT"></span>

**TandemNT** (34)


</dt> <dd></dd> <dt>

<span id="BS2000"></span><span id="bs2000"></span>

**BS2000** (35)


</dt> <dd></dd> <dt>

<span id="LINUX"></span><span id="linux"></span>

**LINUX** (36)


</dt> <dd></dd> <dt>

<span id="Lynx"></span><span id="lynx"></span><span id="LYNX"></span>

**Lynx** (37)


</dt> <dd></dd> <dt>

<span id="XENIX"></span><span id="xenix"></span>

**XENIX** (38)


</dt> <dd></dd> <dt>

<span id="VM_ESA"></span><span id="vm_esa"></span>

**VM/ESA** (39)


</dt> <dd></dd> <dt>

<span id="Interactive_UNIX"></span><span id="interactive_unix"></span><span id="INTERACTIVE_UNIX"></span>

**Interactive UNIX** (40)


</dt> <dd></dd> <dt>

<span id="BSDUNIX"></span><span id="bsdunix"></span>

**BSDUNIX** (41)


</dt> <dd></dd> <dt>

<span id="FreeBSD"></span><span id="freebsd"></span><span id="FREEBSD"></span>

**FreeBSD** (42)


</dt> <dd></dd> <dt>

<span id="NetBSD"></span><span id="netbsd"></span><span id="NETBSD"></span>

**NetBSD** (43)


</dt> <dd></dd> <dt>

<span id="GNU_Hurd"></span><span id="gnu_hurd"></span><span id="GNU_HURD"></span>

**GNU – Obstáculos** (44)


</dt> <dd></dd> <dt>

<span id="OS9"></span><span id="os9"></span>

**OS9** (45)


</dt> <dd></dd> <dt>

<span id="MACH_Kernel"></span><span id="mach_kernel"></span><span id="MACH_KERNEL"></span>

**Kernel DE NUM** (46)


</dt> <dd></dd> <dt>

<span id="Inferno"></span><span id="inferno"></span><span id="INFERNO"></span>

**Ela** (47)


</dt> <dd></dd> <dt>

<span id="QNX"></span><span id="qnx"></span>

**QNX** (48)


</dt> <dd></dd> <dt>

<span id="EPOC"></span><span id="epoc"></span>

**EPOC** (49)


</dt> <dd></dd> <dt>

<span id="IxWorks"></span><span id="ixworks"></span><span id="IXWORKS"></span>

**IxWorks** (50)


</dt> <dd></dd> <dt>

<span id="VxWorks"></span><span id="vxworks"></span><span id="VXWORKS"></span>

**VxWorks** (51)


</dt> <dd></dd> <dt>

<span id="MiNT"></span><span id="mint"></span><span id="MINT"></span>

**MiNT** (52)


</dt> <dd></dd> <dt>

<span id="BeOS"></span><span id="beos"></span><span id="BEOS"></span>

**BeOS** (53)


</dt> <dd></dd> <dt>

<span id="HP_MPE"></span><span id="hp_mpe"></span>

**HP MPE** (54)


</dt> <dd></dd> <dt>

<span id="NextStep"></span><span id="nextstep"></span><span id="NEXTSTEP"></span>

**NextStep** (55)


</dt> <dd></dd> <dt>

<span id="PalmPilot"></span><span id="palmpilot"></span><span id="PALMPILOT"></span>

**PalmPilot** (56)


</dt> <dd></dd> <dt>

<span id="Rhapsody"></span><span id="rhapsody"></span><span id="RHAPSODY"></span>

**Rhapsody** (57)


</dt> <dd></dd> <dt>

<span id="Windows_2000"></span><span id="windows_2000"></span><span id="WINDOWS_2000"></span>

**Windows 2000** (58)


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

**Dedicado** (59)


</dt> <dd></dd> <dt>

<span id="VSE"></span><span id="vse"></span>

**VSE** (60)


</dt> <dd></dd> <dt>

<span id="TPF"></span><span id="tpf"></span>

**TPF** (61)


</dt> <dd></dd> </dl>

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Versão"), [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| HARDWARE Description \\ \\ \\ \\ \| SystemBiosVersion")
</dt> </dl>

Versão do BIOS. Essa cadeia de caracteres é criada pelo fabricante do BIOS.

Essa propriedade é herdada de [**CIM \_ SoftwareElement.**](cim-softwareelement.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ BIOS win32** é derivada de [**CIM \_ BIOSElement.**](cim-bioselement.md)

As propriedades na classe **\_ BIOS do Win32** podem mudar para um sistema de computador específico com o mesmo BIOS, por exemplo, inicializando por meio de um modo BIOS herdado versus inicializando por meio do modo UEFI BIOS. No entanto, as propriedades recuperadas das estruturas SMBIOS devem permanecer as mesmas.

## <a name="examples"></a>Exemplos

O exemplo [do PowerShell Get-ComputerInfo – Query Computer From Local/Remote Computers – (WMI) na](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) Galeria do TechNet usa várias chamadas para hardware e software, incluindo **o Win32 \_ BIOS,** para exibir informações sobre um sistema local ou remoto.

O exemplo Gerar informações do sistema como VBScript da hierarquia XML na Galeria do TechNet usa várias chamadas para hardware e software, incluindo o **\_ WIN32 BIOS,** para gerar uma representação [XML](https://Gallery.TechNet.Microsoft.Com/Generate-system-information-3f40629f) de um sistema usando uma saída XML manual.

O exemplo de código do PowerShell a seguir **usa o \_ BIOS do Win32** para retornar características do BIOS


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



O exemplo de código anterior retorna as seguintes informações:

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

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ BIOSElement**](cim-bioselement.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

