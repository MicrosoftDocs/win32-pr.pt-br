---
description: A classe Impressora CIM \_ representa os recursos e o gerenciamento do dispositivo lógico da impressora.
ms.assetid: e41ff580-0202-4d3f-8d78-4705d5fb41b3
ms.tgt_platform: multiple
title: CIM_Printer classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Printer
- CIM_Printer.Availability
- CIM_Printer.AvailableJobSheets
- CIM_Printer.Capabilities
- CIM_Printer.CapabilityDescriptions
- CIM_Printer.Caption
- CIM_Printer.CharSetsSupported
- CIM_Printer.ConfigManagerErrorCode
- CIM_Printer.ConfigManagerUserConfig
- CIM_Printer.CreationClassName
- CIM_Printer.CurrentCapabilities
- CIM_Printer.CurrentCharSet
- CIM_Printer.CurrentLanguage
- CIM_Printer.CurrentMimeType
- CIM_Printer.CurrentNaturalLanguage
- CIM_Printer.CurrentPaperType
- CIM_Printer.DefaultCapabilities
- CIM_Printer.DefaultCopies
- CIM_Printer.DefaultLanguage
- CIM_Printer.DefaultMimeType
- CIM_Printer.DefaultNumberUp
- CIM_Printer.DefaultPaperType
- CIM_Printer.Description
- CIM_Printer.DetectedErrorState
- CIM_Printer.DeviceID
- CIM_Printer.ErrorCleared
- CIM_Printer.ErrorDescription
- CIM_Printer.ErrorInformation
- CIM_Printer.HorizontalResolution
- CIM_Printer.InstallDate
- CIM_Printer.JobCountSinceLastReset
- CIM_Printer.LanguagesSupported
- CIM_Printer.LastErrorCode
- CIM_Printer.MarkingTechnology
- CIM_Printer.MaxCopies
- CIM_Printer.MaxNumberUp
- CIM_Printer.MaxSizeSupported
- CIM_Printer.MimeTypesSupported
- CIM_Printer.Name
- CIM_Printer.NaturalLanguagesSupported
- CIM_Printer.PaperSizesSupported
- CIM_Printer.PaperTypesAvailable
- CIM_Printer.PNPDeviceID
- CIM_Printer.PowerManagementCapabilities
- CIM_Printer.PowerManagementSupported
- CIM_Printer.PrinterStatus
- CIM_Printer.Status
- CIM_Printer.StatusInfo
- CIM_Printer.SystemCreationClassName
- CIM_Printer.SystemName
- CIM_Printer.TimeOfLastReset
- CIM_Printer.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 001e0fce9645ddc2487a934fcbfa5986771f3dad841f58ea60dd4772e9120d7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921226"
---
# <a name="cim_printer-class"></a>Classe impressora CIM \_

A **\_ classe Impressora CIM** representa os recursos e o gerenciamento do dispositivo lógico da impressora.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada Managed Object Format código (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{8502C54A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Printer : CIM_LogicalDevice
{
  uint16   Availability;
  string   AvailableJobSheets[];
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  string   CharSetsSupported[];
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  uint16   CurrentCapabilities[];
  string   CurrentCharSet;
  uint16   CurrentLanguage;
  string   CurrentMimeType;
  string   CurrentNaturalLanguage;
  string   CurrentPaperType;
  uint16   DefaultCapabilities[];
  uint32   DefaultCopies;
  uint16   DefaultLanguage;
  string   DefaultMimeType;
  uint32   DefaultNumberUp;
  string   DefaultPaperType;
  string   Description;
  uint16   DetectedErrorState;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   ErrorInformation[];
  uint32   HorizontalResolution;
  datetime InstallDate;
  uint32   JobCountSinceLastReset;
  uint16   LanguagesSupported[];
  uint32   LastErrorCode;
  uint16   MarkingTechnology;
  uint32   MaxCopies;
  uint32   MaxNumberUp;
  uint32   MaxSizeSupported;
  string   MimeTypesSupported[];
  string   Name;
  string   NaturalLanguagesSupported[];
  uint16   PaperSizesSupported[];
  string   PaperTypesAvailable[];
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   PrinterStatus;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
  uint32   VerticalResolution;
};
```

## <a name="members"></a>Membros

A **\_ classe impressora CIM** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **\_ classe impressora CIM** tem esses métodos.



| Método                                                             | Descrição                                                                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Redefinir**](reset-method-in-class-cim-printer.md)                 | Solicita uma redefinição do dispositivo lógico. Não implementado pelo WMI.<br/>                                                               |
| [**SetPowerState**](setpowerstate-method-in-class-cim-printer.md) | Define o estado de energia desejado para um dispositivo lógico e quando um dispositivo deve ser colocado nesse estado. Não implementado pelo WMI.<br/> |



 

### <a name="properties"></a>Propriedades

A **\_ classe Impressora CIM** tem essas propriedades.

<dl> <dt>

**Disponibilidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Estado Operacional DMTF \| \| 003.5", "MIB. IETF \| HOST-RESOURCES-MIB.hrDeviceStatus")
</dt> </dl>

Disponibilidade e status do dispositivo.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Executando/energia completa** (3)


</dt> <dd>

Executando ou energia total

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em Teste** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar** (7)


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora de** serviço (9)


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save – Desconhecido** (13)


</dt> <dd>

O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Economia de energia – modo de energia baixa** (14)


</dt> <dd>

O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode apresentar desempenho degradado.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Economia de energia – espera** (15)


</dt> <dd>

O dispositivo não está funcionando, mas pode ser levado ao máximo rapidamente.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save – Aviso** (17)


</dt> <dd>

O dispositivo está em um estado de aviso, embora também em um modo de economia de energia.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Pausado** (18)


</dt> <dd>

O dispositivo está em pausa.

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)


</dt> <dd>

O dispositivo não está pronto.

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)


</dt> <dd>

O dispositivo não está configurado.

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)


</dt> <dd>

O dispositivo está silencioso.

</dd> </dl>

</dd> <dt>

**AvailableJobSheets**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.RequiredJobSheets")
</dt> </dl>

Descreve todas as planilhas de trabalho disponíveis na impressora. Isso também pode ser usado para descrever a faixa que uma impressora pode fornecer no início de cada trabalho ou pode descrever outras opções especificadas pelo usuário.

</dd> <dt>

**Funcionalidades**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Impressora CIM \_**. CapabilityDescriptions", "CIM \_ PrintJob.Finishing", "CIM \_ PrintService.Capabilities")
</dt> </dl>

Funcionalidades de impressora.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impressão de cores** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impressão duplex** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Cópias** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Collation** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Stapling** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impressão de transparência** (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**(8)**


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Cobertura** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Bind** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impressão em preto e branco** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**One Sided** (12)


</dt> <dd>

Lado único

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borda longa com dois lados** (13)


</dt> <dd>

Borda longa de dois lados

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Dois lados de borda curta** (14)


</dt> <dd>

Borda curta de dois lados

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Retrato** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paisagem** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Retrato reverso** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paisagem inversa** (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Qualidade alta** (19)


</dt> <dd>

Qualidade alta

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Quality Normal** (20)


</dt> <dd>

Qualidade normal

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualidade Baixa** (21)


</dt> <dd>

Qualidade baixa

</dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Impressora CIM \_**.**Funcionalidades**")
</dt> </dl>

Cadeias de caracteres de forma livre que fornecem explicações detalhadas para qualquer um dos recursos de impressora indicados na matriz **Recursos.**

> [!Note]  
> Cada entrada dessa matriz está relacionada à entrada na matriz **Recursos** que está localizada no mesmo índice.

 

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Legenda")
</dt> </dl>

Descrição textual curta do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CharSetsSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.CharSet"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. Impressora \| IETF-MIB.prtLocalizationCharacterSet")
</dt> </dl>

Conjuntos de caracteres disponíveis para a saída do texto relacionado ao gerenciamento da impressora. As cadeias de caracteres fornecidas nesta propriedade devem estar em conformidade com a semântica e a sintaxe especificadas pela seção 4.1.2 ("parâmetro Charset") na RFC 2046 (MIME Parte 2) e contidas no registro de conjunto de caracteres IANA. Os exemplos incluem "utf-8", "us-ascii" e "iso-8859-1".

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Código de erro Gerenciador de Configurações Win32.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Esse dispositivo está funcionando corretamente.**  acima (0)


</dt> <dd>

O dispositivo está funcionando corretamente.

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Esse dispositivo não está configurado corretamente.** (1)


</dt> <dd>

O dispositivo não está configurado corretamente.

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows pode carregar o driver para este dispositivo.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para esse dispositivo pode estar corrompido ou seu sistema pode estar com pouca memória ou outros recursos.** (3)


</dt> <dd>

O driver para esse dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Esse dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.** (4)


</dt> <dd>

O dispositivo não está funcionando corretamente. Um de seus drivers ou o registro pode estar corrompido.

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para esse dispositivo precisa de um recurso que Windows pode gerenciar.** (5)


</dt> <dd>

O driver para o dispositivo requer um recurso que Windows pode gerenciar.

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para esse dispositivo entra em conflito com outros dispositivos.**  (6)


</dt> <dd>

A configuração de inicialização para o dispositivo entra em conflito com outros dispositivos.

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.** (7)


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.** (8)


</dt> <dd>

O carregador de driver para o dispositivo está ausente.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Esse dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.** (9)


</dt> <dd>

O dispositivo não está funcionando corretamente. O firmware de controle está relatando incorretamente os recursos para o dispositivo.

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode iniciar.** (10)


</dt> <dd>

O dispositivo não pode iniciar.

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Esse dispositivo falhou.** (11)


</dt> <dd>

Falha no dispositivo.

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Esse dispositivo não pode encontrar recursos gratuitos suficientes que ele possa usar.** (12)


</dt> <dd>

O dispositivo não pode encontrar recursos gratuitos suficientes para usar.

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows pode verificar os recursos desse dispositivo.** (13)


</dt> <dd>

Windows pode verificar os recursos do dispositivo.

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Esse dispositivo não pode funcionar corretamente até que você reinicie o computador.** (14)


</dt> <dd>

O dispositivo não pode funcionar corretamente até que o computador seja reiniciado.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Esse dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.** (15)


</dt> <dd>

O dispositivo não está funcionando corretamente devido a um possível problema de enumeração.

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows pode identificar todos os recursos que esse dispositivo usa.** (16)


</dt> <dd>

Windows pode identificar todos os recursos que o dispositivo usa.

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Esse dispositivo está solicitando um tipo de recurso desconhecido.** (17)


</dt> <dd>

O dispositivo está solicitando um tipo de recurso desconhecido.

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.** (18)


</dt> <dd>

Os drivers de dispositivo devem ser reinstalados.

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.** (19)


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Seu registro pode estar corrompido.** (20)


</dt> <dd>

O Registro pode estar corrompido.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: tente alterar o driver para este dispositivo. Se isso não funcionar, consulte sua documentação de hardware. Windows está removendo esse dispositivo.** (21)


</dt> <dd>

Falha do sistema. Se a alteração do driver de dispositivo for ineficaz, consulte a documentação de hardware. Windows está removendo o dispositivo.

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Esse dispositivo está desabilitado.** (22)


</dt> <dd>

O dispositivo está desabilitado.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: tente alterar o driver para este dispositivo. Se isso não funcionar, consulte sua documentação de hardware.** (23)


</dt> <dd>

Falha do sistema. Se a alteração do driver de dispositivo for ineficaz, consulte a documentação de hardware.

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Esse dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.** (24)


</dt> <dd>

O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows ainda está configurando este dispositivo.** (25)


</dt> <dd>

Windows ainda está configurando o dispositivo.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows ainda está configurando este dispositivo.** (26)


</dt> <dd>

Windows ainda está configurando o dispositivo.

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.** (27)


</dt> <dd>

O dispositivo não tem uma configuração de log válida.

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.** (28)


</dt> <dd>

Os drivers de dispositivo não estão instalados.

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.** (29)


</dt> <dd>

O dispositivo está desabilitado. O firmware do dispositivo não forneceu os recursos necessários.

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.** (30)


</dt> <dd>

O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**este dispositivo não está funcionando corretamente porque Windows não pode carregar os drivers necessários para este dispositivo.** (31)


</dt> <dd>

O dispositivo não está funcionando corretamente. Windows não pode carregar os drivers de dispositivo necessários.

</dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome da classe ou subclasse usada na criação de uma instância. Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

</dd> <dt>

**CurrentCapabilities**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**Recursos**")
</dt> </dl>

As finalidades e outros recursos da impressora que estão em uso no momento. Cada entrada nessa propriedade também deve ser listada na matriz **Capabilities** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impressão de cores** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impressão duplex** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Cópias** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Agrupamento** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grampeamento** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impressão de transparência** (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perfuração** (8)


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Capa** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Associar** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impressão em preto e branco** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Um lado** (12)


</dt> <dd>

Um lado

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borda longa de dois lados** (13)


</dt> <dd>

Borda longa de dois lados

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borda curta de dois lados** (14)


</dt> <dd>

Borda curta de dois lados

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Retrato** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paisagem** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverter retrato** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paisagem reversa** (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Alta qualidade** (19)


</dt> <dd>

Alta qualidade

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualidade normal** (20)


</dt> <dd>

Qualidade normal

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualidade baixa** (21)


</dt> <dd>

Qualidade baixa

</dd> </dl>

</dd> <dt>

**CurrentCharSet**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**CharSetsSupported**")
</dt> </dl>

Conjunto de caracteres atual usado para a saída de texto relacionada ao gerenciamento da impressora. O conjunto de caracteres descrito por essa propriedade também deve ser listado na propriedade **CharsetsSupported** . A cadeia de caracteres especificada por essa propriedade deve estar de acordo com a semântica e a sintaxe especificadas pela seção 4.1.2 ("parâmetro charset") no RFC 2046 (MIME Part 2) e contidas no registro de conjunto de caracteres IANA. Os exemplos incluem "UTF-8", "US-ASCII" e "ISO-8859-1".

</dd> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**. LanguagesSupported "," CIM \_ Printer. CurrentMimeType ")
</dt> </dl>

Idioma da impressora atual que está sendo usado; o idioma também deve ser listado na propriedade **LanguagesSupported** .

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

**IPDS** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

**PPDs** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

**Interoperação** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

**Dados da linha** (15)


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

**MODCA** (16)


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

**Regis** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

**Quic** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

**Texto simples** (31)


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

**Doc** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

**imPress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

**Automático** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

**Páginas** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

**Lips** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

**Diagnóstico** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

**CaPSL** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

**Excl** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

**LCDs** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

**CES** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

**MIME** (47)


</dt> <dd></dd> </dl>

</dd> <dt>

**CurrentMimeType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**CurrentLanguage**")
</dt> </dl>

Tipo MIME atualmente em uso pela impressora quando a propriedade **CurrentLanguage** está definida para indicar que um tipo MIME está em uso.

</dd> <dt>

**CurrentNaturalLanguage**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**NaturalLanguagesSupported**")
</dt> </dl>

Idioma atual em uso pela impressora para gerenciamento. A linguagem listada aqui também deve ser listada em **NaturalLanguagesSupported**.

</dd> <dt>

**CurrentPaperType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**PaperTypesAvailable**")
</dt> </dl>

Tipo de papel atualmente em uso pela impressora. A cadeia de caracteres deve ser expressa no formulário especificado pelo DPA (aplicativo de impressão de documentos) ISO/IEC 10175, que também é resumido no Apêndice C do RFC 1759 (MIB de impressora).

</dd> <dt>

**Funções de recursos**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**Recursos**")
</dt> </dl>

As finalidades padrão e outros recursos da impressora. Cada entrada nessa propriedade também deve ser listada na matriz **Capabilities** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>

<span id="Color_Printing"></span><span id="color_printing"></span><span id="COLOR_PRINTING"></span>**Impressão de cores** (2)


</dt> <dd></dd> <dt>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>

<span id="Duplex_Printing"></span><span id="duplex_printing"></span><span id="DUPLEX_PRINTING"></span>**Impressão duplex** (3)


</dt> <dd></dd> <dt>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>

<span id="Copies"></span><span id="copies"></span><span id="COPIES"></span>**Cópias** (4)


</dt> <dd></dd> <dt>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>

<span id="Collation"></span><span id="collation"></span><span id="COLLATION"></span>**Agrupamento** (5)


</dt> <dd></dd> <dt>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>

<span id="Stapling"></span><span id="stapling"></span><span id="STAPLING"></span>**Grampeamento** (6)


</dt> <dd></dd> <dt>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>

<span id="Transparency_Printing"></span><span id="transparency_printing"></span><span id="TRANSPARENCY_PRINTING"></span>**Impressão de transparência** (7)


</dt> <dd></dd> <dt>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>

<span id="Punch"></span><span id="punch"></span><span id="PUNCH"></span>**Perfuração** (8)


</dt> <dd></dd> <dt>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>

<span id="Cover"></span><span id="cover"></span><span id="COVER"></span>**Capa** (9)


</dt> <dd></dd> <dt>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>

<span id="Bind"></span><span id="bind"></span><span id="BIND"></span>**Associar** (10)


</dt> <dd></dd> <dt>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>

<span id="Black_and_White_Printing"></span><span id="black_and_white_printing"></span><span id="BLACK_AND_WHITE_PRINTING"></span>**Impressão em preto e branco** (11)


</dt> <dd></dd> <dt>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>

<span id="One_Sided"></span><span id="one_sided"></span><span id="ONE_SIDED"></span>**Um lado** (12)


</dt> <dd>

Um lado

</dd> <dt>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>

<span id="Two_Sided_Long_Edge"></span><span id="two_sided_long_edge"></span><span id="TWO_SIDED_LONG_EDGE"></span>**Borda longa de dois lados** (13)


</dt> <dd>

Borda longa de dois lados

</dd> <dt>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>

<span id="Two_Sided_Short_Edge"></span><span id="two_sided_short_edge"></span><span id="TWO_SIDED_SHORT_EDGE"></span>**Borda curta de dois lados** (14)


</dt> <dd>

Borda curta de dois lados

</dd> <dt>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>

<span id="Portrait"></span><span id="portrait"></span><span id="PORTRAIT"></span>**Retrato** (15)


</dt> <dd></dd> <dt>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>

<span id="Landscape"></span><span id="landscape"></span><span id="LANDSCAPE"></span>**Paisagem** (16)


</dt> <dd></dd> <dt>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>

<span id="Reverse_Portrait"></span><span id="reverse_portrait"></span><span id="REVERSE_PORTRAIT"></span>**Reverter retrato** (17)


</dt> <dd></dd> <dt>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>

<span id="Reverse_Landscape"></span><span id="reverse_landscape"></span><span id="REVERSE_LANDSCAPE"></span>**Paisagem reversa** (18)


</dt> <dd></dd> <dt>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>

<span id="Quality_High"></span><span id="quality_high"></span><span id="QUALITY_HIGH"></span>**Alta qualidade** (19)


</dt> <dd>

Alta qualidade

</dd> <dt>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>

<span id="Quality_Normal"></span><span id="quality_normal"></span><span id="QUALITY_NORMAL"></span>**Qualidade normal** (20)


</dt> <dd>

Qualidade normal

</dd> <dt>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>

<span id="Quality_Low"></span><span id="quality_low"></span><span id="QUALITY_LOW"></span>**Qualidade baixa** (21)


</dt> <dd>

Qualidade baixa

</dd> </dl>

</dd> <dt>

**Defaultcopies**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de cópias que um único trabalho produzirá, a menos que especificado de outra forma.

</dd> <dt>

**DefaultLanguage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**. LanguagesSupported "," CIM \_ Printer. Defaultmimetype ")
</dt> </dl>

Idioma padrão da impressora. O idioma também deve ser listado na propriedade **LanguagesSupported** .

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

**IPDS** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

**PPDs** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

**Interoperação** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

**Dados da linha** (15)


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

**MODCA** (16)


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

**Regis** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

**Quic** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

**Texto simples** (31)


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

**Doc** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

**imPress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

**Automático** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

**Páginas** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

**Lips** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

**Diagnóstico** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

**CaPSL** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

**Excl** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

**LCDs** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

**CES** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

**MIME** (47)


</dt> <dd></dd> </dl>

</dd> <dt>

**Defaultmimetype**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**DefaultLanguage**")
</dt> </dl>

Tipo MIME padrão usado pela impressora quando a propriedade **DefaultLanguage** está definida para indicar que um tipo MIME está em uso.

</dd> <dt>

**DefaultNumberUp**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de páginas de fluxo de impressão que a impressora processará em uma única folha de mídia, a menos que um trabalho especifique o contrário.

</dd> <dt>

**Defaultpapertype**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**PaperTypesAvailable**")
</dt> </dl>

Tipo de papel que a impressora usará se PrintJob não especificar um tipo específico. A cadeia de caracteres deve ser expressa no formulário especificado pelo DPA (aplicativo de impressão de documentos) ISO/IEC 10175, que também é resumido no Apêndice C do RFC 1759 (MIB de impressora).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")
</dt> </dl>

Descrição textual do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DetectedErrorState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**ErrorInformation**"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIB. IETF \| Printer-MIB. hrPrinterDetectedErrorState ")
</dt> </dl>

Informações de erro da impressora.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="No_Error"></span><span id="no_error"></span><span id="NO_ERROR"></span>

**Sem erro** (2)


</dt> <dd></dd> <dt>

<span id="Low_Paper"></span><span id="low_paper"></span><span id="LOW_PAPER"></span>

**Papel baixo** (3)


</dt> <dd></dd> <dt>

<span id="No_Paper"></span><span id="no_paper"></span><span id="NO_PAPER"></span>

**Sem papel** (4)


</dt> <dd></dd> <dt>

<span id="Low_Toner"></span><span id="low_toner"></span><span id="LOW_TONER"></span>

**Toner baixo** (5)


</dt> <dd></dd> <dt>

<span id="No_Toner"></span><span id="no_toner"></span><span id="NO_TONER"></span>

**Sem toner** (6)


</dt> <dd></dd> <dt>

<span id="Door_Open"></span><span id="door_open"></span><span id="DOOR_OPEN"></span>

**Porta aberta** (7)


</dt> <dd></dd> <dt>

<span id="Jammed"></span><span id="jammed"></span><span id="JAMMED"></span>

**Emperrado** (8)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Offline** (9)


</dt> <dd></dd> <dt>

<span id="Service_Requested"></span><span id="service_requested"></span><span id="SERVICE_REQUESTED"></span>

**Serviço solicitado** (10)


</dt> <dd></dd> <dt>

<span id="Output_Bin_Full"></span><span id="output_bin_full"></span><span id="OUTPUT_BIN_FULL"></span>

**Escaninho de saída cheio** (11)


</dt> <dd></dd> </dl>

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Endereço ou outras informações de identificação para nomear exclusivamente o dispositivo lógico.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o erro relatado na propriedade **LastErrorCode** será apagado agora.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres de forma livre que fornece informações sobre o erro registrado na propriedade **LastErrorCode** e as ações corretivas a serem executadas.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

</dd> <dt>

**ErrorInformation**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**.**DetectedErrorState**")
</dt> </dl>

Matriz que fornece informações complementares para o estado de erro atual, indicado na propriedade **DetectedErrorState** .

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob. HorizontalResolution"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels por polegada")
</dt> </dl>

Resolução horizontal em pixels por polegada.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" data de instalação ")
</dt> </dl>

Data e hora em que o objeto foi instalado. Essa propriedade não precisa de um valor para indicar que o objeto está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**JobCountSinceLastReset**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **contador**
</dt> </dl>

Trabalhos de impressora processados desde a última redefinição. Esses trabalhos podem ser processados de uma ou mais filas de impressão.

</dd> <dt>

**LanguagesSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtInterpreterLangFamily "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ impressora CIM**. MimeTypesSupported "," CIM \_ PrintJob. Language "," CIM \_ reservice. LanguagesSupported ")
</dt> </dl>

Idiomas de impressão com suporte nativo.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="PCL"></span><span id="pcl"></span>

**PCL** (3)


</dt> <dd></dd> <dt>

<span id="HPGL"></span><span id="hpgl"></span>

**HPGL** (4)


</dt> <dd></dd> <dt>

<span id="PJL"></span><span id="pjl"></span>

**PJL** (5)


</dt> <dd></dd> <dt>

<span id="PS"></span><span id="ps"></span>

**PS** (6)


</dt> <dd></dd> <dt>

<span id="PSPrinter"></span><span id="psprinter"></span><span id="PSPRINTER"></span>

**PSPrinter** (7)


</dt> <dd></dd> <dt>

<span id="IPDS"></span><span id="ipds"></span>

**IPDS** (8)


</dt> <dd></dd> <dt>

<span id="PPDS"></span><span id="ppds"></span>

**PPDs** (9)


</dt> <dd></dd> <dt>

<span id="EscapeP"></span><span id="escapep"></span><span id="ESCAPEP"></span>

**EscapeP** (10)


</dt> <dd></dd> <dt>

<span id="Epson"></span><span id="epson"></span><span id="EPSON"></span>

**Epson** (11)


</dt> <dd></dd> <dt>

<span id="DDIF"></span><span id="ddif"></span>

**DDIF** (12)


</dt> <dd></dd> <dt>

<span id="Interpress"></span><span id="interpress"></span><span id="INTERPRESS"></span>

**Interoperação** (13)


</dt> <dd></dd> <dt>

<span id="ISO6429"></span><span id="iso6429"></span>

**ISO6429** (14)


</dt> <dd></dd> <dt>

<span id="Line_Data"></span><span id="line_data"></span><span id="LINE_DATA"></span>

**Dados da linha** (15)


</dt> <dd></dd> <dt>

<span id="MODCA"></span><span id="modca"></span>

**MODCA** (16)


</dt> <dd></dd> <dt>

<span id="REGIS"></span><span id="regis"></span>

**Regis** (17)


</dt> <dd></dd> <dt>

<span id="SCS"></span><span id="scs"></span>

**SCS** (18)


</dt> <dd></dd> <dt>

<span id="SPDL"></span><span id="spdl"></span>

**SPDL** (19)


</dt> <dd></dd> <dt>

<span id="TEK4014"></span><span id="tek4014"></span>

**TEK4014** (20)


</dt> <dd></dd> <dt>

<span id="PDS"></span><span id="pds"></span>

**PDS** (21)


</dt> <dd></dd> <dt>

<span id="IGP"></span><span id="igp"></span>

**IGP** (22)


</dt> <dd></dd> <dt>

<span id="CodeV"></span><span id="codev"></span><span id="CODEV"></span>

**CodeV** (23)


</dt> <dd></dd> <dt>

<span id="DSCDSE"></span><span id="dscdse"></span>

**DSCDSE** (24)


</dt> <dd></dd> <dt>

<span id="WPS"></span><span id="wps"></span>

**WPS** (25)


</dt> <dd></dd> <dt>

<span id="LN03"></span><span id="ln03"></span>

**LN03** (26)


</dt> <dd></dd> <dt>

<span id="CCITT"></span><span id="ccitt"></span>

**CCITT** (27)


</dt> <dd></dd> <dt>

<span id="QUIC"></span><span id="quic"></span>

**Quic** (28)


</dt> <dd></dd> <dt>

<span id="CPAP"></span><span id="cpap"></span>

**CPAP** (29)


</dt> <dd></dd> <dt>

<span id="DecPPL"></span><span id="decppl"></span><span id="DECPPL"></span>

**DecPPL** (30)


</dt> <dd></dd> <dt>

<span id="Simple_Text"></span><span id="simple_text"></span><span id="SIMPLE_TEXT"></span>

**Texto simples** (31)


</dt> <dd></dd> <dt>

<span id="NPAP"></span><span id="npap"></span>

**NPAP** (32)


</dt> <dd></dd> <dt>

<span id="DOC"></span><span id="doc"></span>

**Doc** (33)


</dt> <dd></dd> <dt>

<span id="imPress"></span><span id="impress"></span><span id="IMPRESS"></span>

**imPress** (34)


</dt> <dd></dd> <dt>

<span id="Pinwriter"></span><span id="pinwriter"></span><span id="PINWRITER"></span>

**Pinwriter** (35)


</dt> <dd></dd> <dt>

<span id="NPDL"></span><span id="npdl"></span>

**NPDL** (36)


</dt> <dd></dd> <dt>

<span id="NEC201PL"></span><span id="nec201pl"></span>

**NEC201PL** (37)


</dt> <dd></dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

**Automático** (38)


</dt> <dd></dd> <dt>

<span id="Pages"></span><span id="pages"></span><span id="PAGES"></span>

**Páginas** (39)


</dt> <dd></dd> <dt>

<span id="LIPS"></span><span id="lips"></span>

**Lips** (40)


</dt> <dd></dd> <dt>

<span id="TIFF"></span><span id="tiff"></span>

**TIFF** (41)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

**Diagnóstico** (42)


</dt> <dd></dd> <dt>

<span id="CaPSL"></span><span id="capsl"></span><span id="CAPSL"></span>

**CaPSL** (43)


</dt> <dd></dd> <dt>

<span id="EXCL"></span><span id="excl"></span>

**Excl** (44)


</dt> <dd></dd> <dt>

<span id="LCDS"></span><span id="lcds"></span>

**LCDs** (45)


</dt> <dd></dd> <dt>

<span id="XES"></span><span id="xes"></span>

**CES** (46)


</dt> <dd></dd> <dt>

<span id="MIME"></span><span id="mime"></span>

**MIME** (47)


</dt> <dd></dd> <dt>

<span id="XPS"></span><span id="xps"></span>

**XPS** (48)


</dt> <dd></dd> <dt>

<span id="HPGL2"></span><span id="hpgl2"></span>

**HPGL2** (49)


</dt> <dd></dd> <dt>

<span id="PCLXL"></span><span id="pclxl"></span>

**PCLXL** (50)


</dt> <dd></dd> </dl>

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Código do último erro relatado pelo dispositivo lógico.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

</dd> <dt>

**MarkingTechnology**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB. prtMarkerMarkTech ")
</dt> </dl>

Marcando a tecnologia usada pela impressora.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_LED"></span><span id="electrophotographic_led"></span><span id="ELECTROPHOTOGRAPHIC_LED"></span>

**LED de Electrophotographic** (3)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Laser"></span><span id="electrophotographic_laser"></span><span id="ELECTROPHOTOGRAPHIC_LASER"></span>

**Electrophotographic laser** (4)


</dt> <dd></dd> <dt>

<span id="Electrophotographic_Other"></span><span id="electrophotographic_other"></span><span id="ELECTROPHOTOGRAPHIC_OTHER"></span>

**Electrophotographic outro** (5)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_9pin"></span><span id="impact_moving_head_dot_matrix_9pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_9PIN"></span>

**Impacto ao mover matriz de ponto de cabeçalho 9pin** (6)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_24pin"></span><span id="impact_moving_head_dot_matrix_24pin"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_24PIN"></span>

**Impacto ao mover matriz de ponto de cabeçalho 24pin** (7)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Dot_Matrix_Other"></span><span id="impact_moving_head_dot_matrix_other"></span><span id="IMPACT_MOVING_HEAD_DOT_MATRIX_OTHER"></span>

**Impacto ao mover matriz de ponto de cabeçalho outro** (8)


</dt> <dd></dd> <dt>

<span id="Impact_Moving_Head_Fully_Formed"></span><span id="impact_moving_head_fully_formed"></span><span id="IMPACT_MOVING_HEAD_FULLY_FORMED"></span>

**Cabeçalho de movimentação de impacto totalmente formado** (9)


</dt> <dd></dd> <dt>

<span id="Impact_Band"></span><span id="impact_band"></span><span id="IMPACT_BAND"></span>

**Faixa de impacto** (10)


</dt> <dd></dd> <dt>

<span id="Impact_Other"></span><span id="impact_other"></span><span id="IMPACT_OTHER"></span>

**Outro impacto** (11)


</dt> <dd></dd> <dt>

<span id="Inkjet_Aqueous"></span><span id="inkjet_aqueous"></span><span id="INKJET_AQUEOUS"></span>

**Jato de aqueous** (12)


</dt> <dd></dd> <dt>

<span id="Inkjet_Solid"></span><span id="inkjet_solid"></span><span id="INKJET_SOLID"></span>

**Jato de radiosolid** (13)


</dt> <dd></dd> <dt>

<span id="Inkjet_Other"></span><span id="inkjet_other"></span><span id="INKJET_OTHER"></span>

**Outro jato** de Radio(14)


</dt> <dd></dd> <dt>

<span id="Pen"></span><span id="pen"></span><span id="PEN"></span>

**Caneta** (15)


</dt> <dd></dd> <dt>

<span id="Thermal_Transfer"></span><span id="thermal_transfer"></span><span id="THERMAL_TRANSFER"></span>

**Transferência térmica** (16)


</dt> <dd></dd> <dt>

<span id="Thermal_Sensitive"></span><span id="thermal_sensitive"></span><span id="THERMAL_SENSITIVE"></span>

**Sensível à térmica** (17)


</dt> <dd></dd> <dt>

<span id="Thermal_Diffusion"></span><span id="thermal_diffusion"></span><span id="THERMAL_DIFFUSION"></span>

**Difusão térmica** (18)


</dt> <dd></dd> <dt>

<span id="Thermal_Other"></span><span id="thermal_other"></span><span id="THERMAL_OTHER"></span>

**Outro** termoelétrico (19)


</dt> <dd></dd> <dt>

<span id="Electroerosion"></span><span id="electroerosion"></span><span id="ELECTROEROSION"></span>

**Erosion** (20)


</dt> <dd></dd> <dt>

<span id="Electrostatic"></span><span id="electrostatic"></span><span id="ELECTROSTATIC"></span>

**Estático** (21)


</dt> <dd></dd> <dt>

<span id="Photographic_Microfiche"></span><span id="photographic_microfiche"></span><span id="PHOTOGRAPHIC_MICROFICHE"></span>

**Microfiche írreo** (22)


</dt> <dd></dd> <dt>

<span id="Photographic_Imagesetter"></span><span id="photographic_imagesetter"></span><span id="PHOTOGRAPHIC_IMAGESETTER"></span>

**Imagesetter de imagens de imagem** (23)


</dt> <dd></dd> <dt>

<span id="Photographic_Other"></span><span id="photographic_other"></span><span id="PHOTOGRAPHIC_OTHER"></span>

**Outro filme** (24)


</dt> <dd></dd> <dt>

<span id="Ion_Deposition"></span><span id="ion_deposition"></span><span id="ION_DEPOSITION"></span>

**Ion Deposition** (25)


</dt> <dd></dd> <dt>

<span id="eBeam"></span><span id="ebeam"></span><span id="EBEAM"></span>

**eBeam** (26)


</dt> <dd></dd> <dt>

<span id="Typesetter"></span><span id="typesetter"></span><span id="TYPESETTER"></span>

**Typesetter** (27)


</dt> <dd></dd> </dl>

</dd> <dt>

**MaxCopies**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.Copies")
</dt> </dl>

Número máximo de cópias que podem ser produzidas pela impressora de um único trabalho.

</dd> <dt>

**MaxNumberUp**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.NumberUp")
</dt> </dl>

Número máximo de páginas de fluxo de impressão que a impressora pode renderizar em uma única folha de mídia.

</dd> <dt>

**MaxSizeSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.JobSize"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes")
</dt> </dl>

Maior trabalho (como um fluxo de byte) que a impressora aceitará em unidades de quilobytes. Um valor de 0 (zero) indica que nenhum limite foi definido.

</dd> <dt>

**MimeTypesSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Impressora CIM \_**. LanguagesSupported", "CIM \_ PrintJob.MimeTypes", "CIM \_ PrintService.MimeTypesSupported")
</dt> </dl>

Cadeias de caracteres de forma livre que fornecem explicações detalhadas dos tipos mime com suporte da impressora. Se os dados são fornecidos para essa propriedade, o valor 47 ("Mime") deve ser incluído na **propriedade LanguagesSupported.**

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome")
</dt> </dl>

Rótulo pelo qual o objeto é conhecido. Quando subclasse, essa propriedade pode ser substituído para ser uma propriedade de chave.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**NaturalLanguagesSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. Impressora \| IETF-MIB.prtLocalizationLanguage"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.NaturalLanguage")
</dt> </dl>

Idiomas disponíveis para cadeias de caracteres usadas pela impressora para saída de informações de gerenciamento. As cadeias de caracteres devem estar em conformidade com o RFC 1766. Por exemplo, "en" é usado para inglês.

</dd> <dt>

**PaperSizesSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipos de papel com suporte.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="A"></span><span id="a"></span>

**A** (2)


</dt> <dd></dd> <dt>

<span id="B"></span><span id="b"></span>

**B** (3)


</dt> <dd></dd> <dt>

<span id="C"></span><span id="c"></span>

**C** (4)


</dt> <dd></dd> <dt>

<span id="D"></span><span id="d"></span>

**D** (5)


</dt> <dd></dd> <dt>

<span id="E"></span><span id="e"></span>

**E** (6)


</dt> <dd></dd> <dt>

<span id="Letter"></span><span id="letter"></span><span id="LETTER"></span>

**Letra** (7)


</dt> <dd></dd> <dt>

<span id="Legal"></span><span id="legal"></span><span id="LEGAL"></span>

**Legal** (8)


</dt> <dd></dd> <dt>

<span id="NA-10x13-Envelope"></span><span id="na-10x13-envelope"></span><span id="NA-10X13-ENVELOPE"></span>

**NA-10x13-Envelope** (9)


</dt> <dd></dd> <dt>

<span id="NA-9x12-Envelope"></span><span id="na-9x12-envelope"></span><span id="NA-9X12-ENVELOPE"></span>

**NA-9x12-Envelope** (10)


</dt> <dd></dd> <dt>

<span id="NA-Number-10-Envelope"></span><span id="na-number-10-envelope"></span><span id="NA-NUMBER-10-ENVELOPE"></span>

**NA-Number-10-Envelope** (11)


</dt> <dd></dd> <dt>

<span id="NA-7x9-Envelope"></span><span id="na-7x9-envelope"></span><span id="NA-7X9-ENVELOPE"></span>

**NA-7x9-Envelope** (12)


</dt> <dd></dd> <dt>

<span id="NA-9x11-Envelope"></span><span id="na-9x11-envelope"></span><span id="NA-9X11-ENVELOPE"></span>

**ENVELOPE NA-9x11** (13)


</dt> <dd></dd> <dt>

<span id="NA-10x14-Envelope"></span><span id="na-10x14-envelope"></span><span id="NA-10X14-ENVELOPE"></span>

**NA-10x14-Envelope** (14)


</dt> <dd></dd> <dt>

<span id="NA-Number-9-Envelope"></span><span id="na-number-9-envelope"></span><span id="NA-NUMBER-9-ENVELOPE"></span>

**NA-Number-9-Envelope** (15)


</dt> <dd></dd> <dt>

<span id="NA-6x9-Envelope"></span><span id="na-6x9-envelope"></span><span id="NA-6X9-ENVELOPE"></span>

**NA-6x9-Envelope** (16)


</dt> <dd></dd> <dt>

<span id="NA-10x15-Envelope"></span><span id="na-10x15-envelope"></span><span id="NA-10X15-ENVELOPE"></span>

**NA-10x15-Envelope** (17)


</dt> <dd></dd> <dt>

<span id="A0"></span><span id="a0"></span>

**A0** (18)


</dt> <dd></dd> <dt>

<span id="A1"></span><span id="a1"></span>

**A1** (19)


</dt> <dd></dd> <dt>

<span id="A2"></span><span id="a2"></span>

**A2** (20)


</dt> <dd></dd> <dt>

<span id="A3"></span><span id="a3"></span>

**A3** (21)


</dt> <dd></dd> <dt>

<span id="A4"></span><span id="a4"></span>

**A4** (22)


</dt> <dd></dd> <dt>

<span id="A5"></span><span id="a5"></span>

**A5** (23)


</dt> <dd></dd> <dt>

<span id="A6"></span><span id="a6"></span>

**A6** (24)


</dt> <dd></dd> <dt>

<span id="A7"></span><span id="a7"></span>

**A7** (25)


</dt> <dd></dd> <dt>

<span id="A8"></span><span id="a8"></span>

**A8** (26)


</dt> <dd></dd> <dt>

<span id="A9A10"></span><span id="a9a10"></span>

**A9A10** (27)


</dt> <dd></dd> <dt>

<span id="B0"></span><span id="b0"></span>

**B0** (28)


</dt> <dd></dd> <dt>

<span id="B1"></span><span id="b1"></span>

**B1** (29)


</dt> <dd></dd> <dt>

<span id="B2"></span><span id="b2"></span>

**B2** (30)


</dt> <dd></dd> <dt>

<span id="B3"></span><span id="b3"></span>

**B3** (31)


</dt> <dd></dd> <dt>

<span id="B4"></span><span id="b4"></span>

**B4** (32)


</dt> <dd></dd> <dt>

<span id="B5"></span><span id="b5"></span>

**B5** (33)


</dt> <dd></dd> <dt>

<span id="B6"></span><span id="b6"></span>

**B6** (34)


</dt> <dd></dd> <dt>

<span id="B7"></span><span id="b7"></span>

**B7** (35)


</dt> <dd></dd> <dt>

<span id="B8"></span><span id="b8"></span>

**B8** (36)


</dt> <dd></dd> <dt>

<span id="B9"></span><span id="b9"></span>

**B9** (37)


</dt> <dd></dd> <dt>

<span id="B10"></span><span id="b10"></span>

**B10** (38)


</dt> <dd></dd> <dt>

<span id="C0"></span><span id="c0"></span>

**C0** (39)


</dt> <dd></dd> <dt>

<span id="C1"></span><span id="c1"></span>

**C1** (40)


</dt> <dd></dd> <dt>

<span id="C2C3"></span><span id="c2c3"></span>

**C2C3** (41)


</dt> <dd></dd> <dt>

<span id="C4"></span><span id="c4"></span>

**C4** (42)


</dt> <dd></dd> <dt>

<span id="C5"></span><span id="c5"></span>

**C5** (43)


</dt> <dd></dd> <dt>

<span id="C6"></span><span id="c6"></span>

**C6** (44)


</dt> <dd></dd> <dt>

<span id="C7"></span><span id="c7"></span>

**C7** (45)


</dt> <dd></dd> <dt>

<span id="C8"></span><span id="c8"></span>

**C8** (46)


</dt> <dd></dd> <dt>

<span id="ISO-Designated"></span><span id="iso-designated"></span><span id="ISO-DESIGNATED"></span>

**ISO-Designated** (47)


</dt> <dd></dd> <dt>

<span id="JIS_B0"></span><span id="jis_b0"></span>

**JIS B0** (48)


</dt> <dd></dd> <dt>

<span id="JIS_B1"></span><span id="jis_b1"></span>

**JIS B1** (49)


</dt> <dd></dd> <dt>

<span id="JIS_B2"></span><span id="jis_b2"></span>

**JIS B2** (50)


</dt> <dd></dd> <dt>

<span id="JIS_B3"></span><span id="jis_b3"></span>

**JIS B3** (51)


</dt> <dd></dd> <dt>

<span id="JIS_B4"></span><span id="jis_b4"></span>

**JIS B4** (52)


</dt> <dd></dd> <dt>

<span id="JIS_B5"></span><span id="jis_b5"></span>

**JIS B5** (53)


</dt> <dd></dd> <dt>

<span id="JIS_B6"></span><span id="jis_b6"></span>

**JIS B6** (54)


</dt> <dd></dd> <dt>

<span id="JIS_B7"></span><span id="jis_b7"></span>

**JIS B7** (55)


</dt> <dd></dd> <dt>

<span id="JIS_B8"></span><span id="jis_b8"></span>

**JIS B8** (56)


</dt> <dd></dd> <dt>

<span id="JIS_B9"></span><span id="jis_b9"></span>

**JIS B9** (57)


</dt> <dd></dd> <dt>

<span id="JIS_B10"></span><span id="jis_b10"></span>

**JIS B10** (58)


</dt> <dd></dd> <dt>

<span id="NA-Letter"></span><span id="na-letter"></span><span id="NA-LETTER"></span>

**Na-Letter** (59)


</dt> <dd></dd> <dt>

<span id="NA-Legal"></span><span id="na-legal"></span><span id="NA-LEGAL"></span>

**NA-Legal** (60)


</dt> <dd></dd> <dt>

<span id="B4-Envelope"></span><span id="b4-envelope"></span><span id="B4-ENVELOPE"></span>

**Envelope B4** (61)


</dt> <dd></dd> <dt>

<span id="B5-Envelope"></span><span id="b5-envelope"></span><span id="B5-ENVELOPE"></span>

**Envelope B5** (62)


</dt> <dd></dd> <dt>

<span id="C3-Envelope"></span><span id="c3-envelope"></span><span id="C3-ENVELOPE"></span>

**Envelope C3** (63)


</dt> <dd></dd> <dt>

<span id="C4-Envelope"></span><span id="c4-envelope"></span><span id="C4-ENVELOPE"></span>

**Envelope C4** (64)


</dt> <dd></dd> <dt>

<span id="C5-Envelope"></span><span id="c5-envelope"></span><span id="C5-ENVELOPE"></span>

**Envelope C5** (65)


</dt> <dd></dd> <dt>

<span id="C6-Envelope"></span><span id="c6-envelope"></span><span id="C6-ENVELOPE"></span>

**Envelope C6** (66)


</dt> <dd></dd> <dt>

<span id="Designated-Long-Envelope"></span><span id="designated-long-envelope"></span><span id="DESIGNATED-LONG-ENVELOPE"></span>

**Envelope longo designado** (67)


</dt> <dd></dd> <dt>

<span id="Monarch-Envelope"></span><span id="monarch-envelope"></span><span id="MONARCH-ENVELOPE"></span>

**Envelope-de-envelope** (68)


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

**Executivo** (69)


</dt> <dd></dd> <dt>

<span id="Folio"></span><span id="folio"></span><span id="FOLIO"></span>

**Folio** (70)


</dt> <dd></dd> <dt>

<span id="Invoice"></span><span id="invoice"></span><span id="INVOICE"></span>

**Fatura** (71)


</dt> <dd></dd> <dt>

<span id="Ledger"></span><span id="ledger"></span><span id="LEDGER"></span>

**Razão** (72)


</dt> <dd></dd> <dt>

<span id="Quarto"></span><span id="quarto"></span><span id="QUARTO"></span>

**Quarto** (73)


</dt> <dd></dd> </dl>

</dd> <dt>

**PaperTypesAvailable**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.RequiredPaperType", "CIM \_ PrintService.PaperTypesAvailable"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. Impressora \| IETF-MIB.prtInputMediaName")
</dt> </dl>

Cadeias de caracteres de forma livre que especificam os tipos de papel que estão disponíveis no momento para a impressora. Cada cadeia de caracteres deve ser expressa no formato especificado pelo APLICATIVO de Impressão de Documentos ISO/IEC 10175 (DPA), que também está resumido no Apêndice C da RFC 1759 (Impressora MIB). Exemplos de cadeias de caracteres válidas são "iso-a4-color" e "na-10x14-envelope". Por definição, um tamanho de papel que está disponível e listado na propriedade **PaperTypesAvailable** também deve aparecer na propriedade **PaperSizesSupported.**

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Win32 Plug and Play identificador de dispositivo lógico do dispositivo lógico. Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

Exemplo: " \* PNP030b"

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz das funcionalidades específicas relacionadas a energia de um dispositivo lógico.

Essa propriedade é herdada de **CIM \_ LogicalDevice.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)


</dt> <dd>

Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)


</dt> <dd>

O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)


</dt> <dd>

Há suporte para o método [**SetPowerState.**](setpowerstate-method-in-class-cim-controller.md) Esse método é encontrado na classe **\_ LogicalDevice cim** pai e pode ser implementado. Para obter mais informações, consulte [Designando classes Managed Object Format (MOF).](/windows/desktop/WmiSdk/designing-managed-object-format--mof--classes)

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling com suporte** (6)


</dt> <dd>

O [**método SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o *parâmetro PowerState* definido como 5 (Power Cycle).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia com tempo de energia com suporte** (7)


</dt> <dd>

O [**método SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (Power Cycle) e *Time* definido como uma data e hora específicas, ou intervalo, para o power-on.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, o dispositivo poderá ser gerenciado por energia, ou seja, colocado em um estado de economia de energia. Se **FALSE**, o valor inteiro 1 ("Sem suporte") deverá ser a única entrada na **matriz PowerManagementCapabilities.**

Essa propriedade não indica se os recursos de gerenciamento de energia estão habilitados no momento ou, se habilitados, quais recursos têm suporte. Para obter mais informações, consulte a **matriz PowerManagementCapabilities.** Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**PrinterStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Printer-MIB.hrPrinterStatus")
</dt> </dl>

Informações de status, além das especificadas na **propriedade Disponibilidade,** para uma impressora.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

**Ocioso** (3)


</dt> <dd></dd> <dt>

<span id="Printing"></span><span id="printing"></span><span id="PRINTING"></span>

**Impressão** (4)


</dt> <dd></dd> <dt>

<span id="Warmup"></span><span id="warmup"></span><span id="WARMUP"></span>

**Aquecimento** (5)


</dt> <dd></dd> <dt>

<span id="Stopped_Printing"></span><span id="stopped_printing"></span><span id="STOPPED_PRINTING"></span>

**Impressão interrompida** (6)


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

**Offline** (7)


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

Status atual do objeto. Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

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

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Estado Operacional DMTF \| \| 003.3")
</dt> </dl>

Estado do dispositivo lógico. Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (Não Aplicável) deverá ser usado.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Desabilitado** (4)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Não aplicável** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](cim-system.md).**CreationClassName**"), [**chave CIM \_**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome da classe de criação do sistema de definição de scoping.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](cim-system.md).**Nome**"), [**Chave CIM \_**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome do sistema de definição de scoping.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Hora da última redefinição da impressora.

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ PrintJob.HorizontalResolution"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pixels por polegada")
</dt> </dl>

Resolução vertical em pixels por polegada.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe Cim \_ Printer** é derivada de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

O WMI não implementa essa classe. Para WMI com classe derivada da **impressora CIM, \_** consulte [Classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

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

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

