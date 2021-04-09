---
description: A \_ classe WMI SerialPort do Win32 representa uma porta serial em um sistema de computador executando o Windows.
ms.assetid: f2e5cc5a-a12b-4079-92e1-6bb62fe797a0
ms.tgt_platform: multiple
title: Classe Win32_SerialPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPort
- Win32_SerialPort.Reset
- Win32_SerialPort.SetPowerState
- Win32_SerialPort.Availability
- Win32_SerialPort.Binary
- Win32_SerialPort.Capabilities
- Win32_SerialPort.CapabilityDescriptions
- Win32_SerialPort.Caption
- Win32_SerialPort.ConfigManagerErrorCode
- Win32_SerialPort.ConfigManagerUserConfig
- Win32_SerialPort.CreationClassName
- Win32_SerialPort.Description
- Win32_SerialPort.DeviceID
- Win32_SerialPort.ErrorCleared
- Win32_SerialPort.ErrorDescription
- Win32_SerialPort.InstallDate
- Win32_SerialPort.LastErrorCode
- Win32_SerialPort.MaxBaudRate
- Win32_SerialPort.MaximumInputBufferSize
- Win32_SerialPort.MaximumOutputBufferSize
- Win32_SerialPort.MaxNumberControlled
- Win32_SerialPort.Name
- Win32_SerialPort.OSAutoDiscovered
- Win32_SerialPort.PNPDeviceID
- Win32_SerialPort.PowerManagementCapabilities
- Win32_SerialPort.PowerManagementSupported
- Win32_SerialPort.ProtocolSupported
- Win32_SerialPort.ProviderType
- Win32_SerialPort.SettableBaudRate
- Win32_SerialPort.SettableDataBits
- Win32_SerialPort.SettableFlowControl
- Win32_SerialPort.SettableParity
- Win32_SerialPort.SettableParityCheck
- Win32_SerialPort.SettableRLSD
- Win32_SerialPort.SettableStopBits
- Win32_SerialPort.Status
- Win32_SerialPort.StatusInfo
- Win32_SerialPort.Supports16BitMode
- Win32_SerialPort.SupportsDTRDSR
- Win32_SerialPort.SupportsElapsedTimeouts
- Win32_SerialPort.SupportsIntTimeouts
- Win32_SerialPort.SupportsParityCheck
- Win32_SerialPort.SupportsRLSD
- Win32_SerialPort.SupportsRTSCTS
- Win32_SerialPort.SupportsSpecialCharacters
- Win32_SerialPort.SupportsXOnXOff
- Win32_SerialPort.SupportsXOnXOffSet
- Win32_SerialPort.SystemCreationClassName
- Win32_SerialPort.SystemName
- Win32_SerialPort.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7fc2f25bc88d880ba9b10f10b5efde284a62624
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088934"
---
# <a name="win32_serialport-class"></a>\_Classe SerialPort Win32

A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ SerialPort do Win32** representa uma porta serial em um sistema de computador executando o Windows.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4BF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPort : CIM_SerialController
{
  uint16   Availability;
  boolean  Binary;
  uint16   Capabilities[];
  string   CapabilityDescriptions[];
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  datetime InstallDate;
  uint32   LastErrorCode;
  uint32   MaxBaudRate;
  uint32   MaximumInputBufferSize;
  uint32   MaximumOutputBufferSize;
  uint32   MaxNumberControlled;
  string   Name;
  boolean  OSAutoDiscovered;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  uint16   ProtocolSupported;
  string   ProviderType;
  boolean  SettableBaudRate;
  boolean  SettableDataBits;
  boolean  SettableFlowControl;
  boolean  SettableParity;
  boolean  SettableParityCheck;
  boolean  SettableRLSD;
  boolean  SettableStopBits;
  string   Status;
  uint16   StatusInfo;
  boolean  Supports16BitMode;
  boolean  SupportsDTRDSR;
  boolean  SupportsElapsedTimeouts;
  boolean  SupportsIntTimeouts;
  boolean  SupportsParityCheck;
  boolean  SupportsRLSD;
  boolean  SupportsRTSCTS;
  boolean  SupportsSpecialCharacters;
  boolean  SupportsXOnXOff;
  boolean  SupportsXOnXOffSet;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a>Membros

A **classe \_ SerialPort do Win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ SerialPort do Win32** tem esses métodos.



| Método            | Descrição                                                                                                                                                                                          |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Redefinir**         | Não implementado. Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ SerialController**](cim-serialcontroller.md).<br/>                 |
| **SetPowerState** | Não implementado. Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ SerialController**](cim-serialcontroller.md).<br/> |



 

### <a name="properties"></a>Propriedades

A **classe \_ SerialPort do Win32** tem essas propriedades.

<dl> <dt>

**Disponibilidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")
</dt> </dl>

Disponibilidade e status do dispositivo.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)


</dt> <dd>

Energia completa ou em execução

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)


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

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)


</dt> <dd>

O dispositivo é conhecido por estar em um modo de economia de energia, mas seu status exato é desconhecido.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)


</dt> <dd>

O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)


</dt> <dd>

O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)


</dt> <dd>

O dispositivo está em um estado de aviso, embora também esteja em um modo de economia de energia.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)


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

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)


</dt> <dd>

O dispositivo está silencioso.

</dd> </dl>

</dd> <dt>

**Binary**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")
</dt> </dl>

Se for **true**, a porta serial será configurada para transferência de dados binários. Como a API do Windows não dá suporte a transferências de modo não binário, essa propriedade deve ser **verdadeira**.

</dd> <dt>

**Funcionalidades**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Portas seriais DMTF \| 4,7 "), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ SerialController**](cim-serialcontroller.md).**CapabilityDescriptions**")
</dt> </dl>

Matriz de compatibilidade em nível de chip para o controlador serial. Esta propriedade descreve o buffer e outros recursos do controlador serial que podem ser inerentes ao hardware do chip. A propriedade é um inteiro enumerado.

Essa propriedade é herdada do [**CIM \_ SerialController**](cim-serialcontroller.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="XT_AT_Compatible"></span><span id="xt_at_compatible"></span><span id="XT_AT_COMPATIBLE"></span>

**XT/at compatível** (3)


</dt> <dd></dd> <dt>

<span id="16450_Compatible"></span><span id="16450_compatible"></span><span id="16450_COMPATIBLE"></span>

**compatível com 16450** (4)


</dt> <dd></dd> <dt>

<span id="16550_Compatible"></span><span id="16550_compatible"></span><span id="16550_COMPATIBLE"></span>

**compatível com 16550** (5)


</dt> <dd></dd> <dt>

<span id="16550A_Compatible"></span><span id="16550a_compatible"></span><span id="16550A_COMPATIBLE"></span>

**compatível com 16550A** (6)


</dt> <dd></dd> <dt>

<span id="8251_Compatible"></span><span id="8251_compatible"></span><span id="8251_COMPATIBLE"></span>

**compatível com 8251** (160)


</dt> <dd></dd> <dt>

<span id="8251FIFO_Compatible"></span><span id="8251fifo_compatible"></span><span id="8251FIFO_COMPATIBLE"></span>

**compatível com 8251FIFO** (161)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](../wmisdk/standard-qualifiers.md) ("indexado"), [**ModelCorrespondence**](../wmisdk/standard-qualifiers.md) ([**" \_ CIM SerialController**](cim-serialcontroller.md).**Recursos**")
</dt> </dl>

Matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos do controlador serial indicados na matriz **Capabilities** . Observe que cada entrada dessa matriz está relacionada à entrada na matriz de **recursos** que está localizada no mesmo índice.

Essa propriedade é herdada do [**CIM \_ SerialController**](cim-serialcontroller.md).

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrição do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Código de erro do Win32 Configuration Manager.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**  acima (0)


</dt> <dd>

O dispositivo está funcionando corretamente.

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.** (1)


</dt> <dd>

O dispositivo não está configurado corretamente.

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.** (2)


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.** (3)


</dt> <dd>

O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.** (4)


</dt> <dd>

O dispositivo não está funcionando corretamente. Um de seus drivers ou o registro pode estar corrompido.

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.** (5)


</dt> <dd>

O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**  (6)


</dt> <dd>

A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.

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

<span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.** (9)


</dt> <dd>

O dispositivo não está funcionando corretamente. O firmware de controle está relatando incorretamente os recursos para o dispositivo.

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.** (10)


</dt> <dd>

Não é possível iniciar o dispositivo.

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.** (11)


</dt> <dd>

Falha no dispositivo.

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.** 12


</dt> <dd>

O dispositivo não pode encontrar recursos livres suficientes para usar.

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.** (13)


</dt> <dd>

O Windows não pode verificar os recursos do dispositivo.

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.** (14)


</dt> <dd>

O dispositivo não funcionará corretamente até que o computador seja reiniciado.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.** (15)


</dt> <dd>

O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.** (16)


</dt> <dd>

O Windows não pode identificar todos os recursos que o dispositivo usa.

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.** (17)


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

<span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.** (20)


</dt> <dd>

O registro pode estar corrompido.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.** (21)


</dt> <dd>

Falha do sistema. Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware. O Windows está removendo o dispositivo.

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.** (22)


</dt> <dd>

O dispositivo está desabilitado.

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.** (23)


</dt> <dd>

Falha do sistema. Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.** (24)


</dt> <dd>

O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.** (25)


</dt> <dd>

O Windows ainda está configurando o dispositivo.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.** (26)


</dt> <dd>

O Windows ainda está configurando o dispositivo.

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

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.** (31)


</dt> <dd>

O dispositivo não está funcionando corretamente. O Windows não pode carregar os drivers de dispositivo necessários.

</dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")
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

Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância. Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")
</dt> </dl>

Descrição do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| hardware \\ \\ DeviceMap \\ \\ SerialComm")
</dt> </dl>

Identificador exclusivo da porta serial com outros dispositivos no sistema.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres de forma livre fornecendo mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")
</dt> </dl>

Data e hora em que o objeto foi instalado. Essa propriedade não precisa de um valor para indicar que o objeto está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

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

**MaxBaudRate**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Portas seriais DMTF \| 4,6 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits por segundo ")
</dt> </dl>

Taxa de transmissão máxima (em bits por segundo) suportada pelo controlador serial.

Essa propriedade é herdada do [**CIM \_ SerialController**](cim-serialcontroller.md).

</dd> <dt>

**MaximumInputBufferSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwMaxRxQueue"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamanho máximo do buffer de entrada interno do driver de porta serial. Um valor de 0 (zero) indica que nenhum valor máximo é imposto pelo provedor serial.

</dd> <dt>

**MaximumOutputBufferSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwMaxTxQueue"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamanho máximo do buffer de saída interno do driver de porta serial. Um valor de 0 (zero) indica que nenhum valor máximo é imposto pelo provedor serial.

</dd> <dt>

**MaxNumberControlled**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta do barramento DMTF \| 1,9 ")
</dt> </dl>

Número máximo de entidades diretamente endereçáveis com suporte por este controlador. Um valor de 0 (zero) deve ser usado se o número for desconhecido.

Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Rótulo pelo qual o objeto é conhecido. Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**OSAutoDiscovered**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema de descrição de hardware \\ \\ \\ \\ \\ \\ MultifunctionAdapter")
</dt> </dl>

Se **for true**, as instâncias dessa classe foram descobertas automaticamente pelo sistema operacional. Se, por exemplo, o hardware foi adicionado por meio do painel de controle, o sistema operacional localiza instâncias dessa classe consultando o hardware das instâncias desta classe.

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

Exemplo: " \* PNP030b"

</dd> <dt>

**PowerManagementCapabilities**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz de recursos específicos relacionados à energia de um dispositivo lógico.

Essa propriedade é herdada **de \_ LogicalDevice CIM**.

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

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)


</dt> <dd>

Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) . Esse método é encontrado na classe pai **de \_ LogicalDevice CIM** e pode ser implementado. Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)


</dt> <dd>

O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)


</dt> <dd>

Tempo Power-On com suporte

O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante). A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

</dd> <dt>

**ProtocolSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta do barramento DMTF \| 1,2 "," MIF. \|Discos DMTF \| 3,3 ")
</dt> </dl>

Protocolo usado pelo controlador para acessar dispositivos "controlados".

Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md). A lista a seguir mostra os valores possíveis.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="EISA"></span><span id="eisa"></span>

<span id="EISA"></span><span id="eisa"></span>**EISA** (3)


</dt> <dd></dd> <dt>

<span id="ISA"></span><span id="isa"></span>

<span id="ISA"></span><span id="isa"></span>**ISA** (4)


</dt> <dd></dd> <dt>

<span id="PCI"></span><span id="pci"></span>

<span id="PCI"></span><span id="pci"></span>**PCI** (5)


</dt> <dd></dd> <dt>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>

<span id="ATA_ATAPI"></span><span id="ata_atapi"></span>**ATA/ATAPI** (6)


</dt> <dd>

ATA ou ATAPI

</dd> <dt>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>

<span id="Flexible_Diskette"></span><span id="flexible_diskette"></span><span id="FLEXIBLE_DISKETTE"></span>**Disquete flexível** (7)


</dt> <dd></dd> <dt>

<span id="1496"></span>

<span id="1496"></span>**1496** (8)


</dt> <dd></dd> <dt>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>

<span id="SCSI_Parallel_Interface"></span><span id="scsi_parallel_interface"></span><span id="SCSI_PARALLEL_INTERFACE"></span>**Interface paralela SCSI** (9)


</dt> <dd></dd> <dt>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>

<span id="SCSI_Fibre_Channel_Protocol"></span><span id="scsi_fibre_channel_protocol"></span><span id="SCSI_FIBRE_CHANNEL_PROTOCOL"></span>**Protocolo SCSI Fibre Channel** (10)


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>

<span id="SCSI_Serial_Bus_Protocol"></span><span id="scsi_serial_bus_protocol"></span><span id="SCSI_SERIAL_BUS_PROTOCOL"></span>**Protocolo de barramento serial SCSI** (11)


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>

<span id="SCSI_Serial_Bus_Protocol-2__1394_"></span><span id="scsi_serial_bus_protocol-2__1394_"></span><span id="SCSI_SERIAL_BUS_PROTOCOL-2__1394_"></span>**Protocolo de barramento serial SCSI-2 (1394)** (12)


</dt> <dd></dd> <dt>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>

<span id="SCSI_Serial_Storage_Architecture"></span><span id="scsi_serial_storage_architecture"></span><span id="SCSI_SERIAL_STORAGE_ARCHITECTURE"></span>**Arquitetura de armazenamento Serial SCSI** (13)


</dt> <dd></dd> <dt>

<span id="VESA"></span><span id="vesa"></span>

<span id="VESA"></span><span id="vesa"></span>**VESA** (14)


</dt> <dd></dd> <dt>

<span id="PCMCIA"></span><span id="pcmcia"></span>

<span id="PCMCIA"></span><span id="pcmcia"></span>**PCMCIA** (15)


</dt> <dd></dd> <dt>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>

<span id="Universal_Serial_Bus"></span><span id="universal_serial_bus"></span><span id="UNIVERSAL_SERIAL_BUS"></span>**Barramento serial universal** (16)


</dt> <dd></dd> <dt>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>

<span id="Parallel_Protocol"></span><span id="parallel_protocol"></span><span id="PARALLEL_PROTOCOL"></span>**Protocolo paralelo** (17)


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

<span id="ESCON"></span><span id="escon"></span>**ESCON** (18)


</dt> <dd></dd> <dt>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>

<span id="Diagnostic"></span><span id="diagnostic"></span><span id="DIAGNOSTIC"></span>**Diagnóstico** (19)


</dt> <dd></dd> <dt>

<span id="I2C"></span><span id="i2c"></span>

<span id="I2C"></span><span id="i2c"></span>**I2C** (20)


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>**Energia** (21)


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

<span id="HIPPI"></span><span id="hippi"></span>**HIPPI** (22)


</dt> <dd></dd> <dt>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>

<span id="MultiBus"></span><span id="multibus"></span><span id="MULTIBUS"></span>**MultiBus** (23)


</dt> <dd></dd> <dt>

<span id="VME"></span><span id="vme"></span>

<span id="VME"></span><span id="vme"></span>**VM** (24)


</dt> <dd></dd> <dt>

<span id="IPI"></span><span id="ipi"></span>

<span id="IPI"></span><span id="ipi"></span>**IPI** (25)


</dt> <dd></dd> <dt>

<span id="IEEE-488"></span><span id="ieee-488"></span>

<span id="IEEE-488"></span><span id="ieee-488"></span>**IEEE-488** (26)


</dt> <dd></dd> <dt>

<span id="RS232"></span><span id="rs232"></span>

<span id="RS232"></span><span id="rs232"></span>**RS232** (27)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE5"></span><span id="ieee_802.3_10base5"></span>

<span id="ieee_802.3_10base5"></span>**IEEE 802,3 10BASE5** (28)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BASE2"></span><span id="ieee_802.3_10base2"></span>

<span id="ieee_802.3_10base2"></span>**IEEE 802,3 10Base2** (29)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_1BASE5"></span><span id="ieee_802.3_1base5"></span>

<span id="ieee_802.3_1base5"></span>**IEEE 802,3 1BASE5** (30)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_10BROAD36"></span><span id="ieee_802.3_10broad36"></span>

<span id="ieee_802.3_10broad36"></span>**IEEE 802,3 10BROAD36** (31)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3_100BASEVG"></span><span id="ieee_802.3_100basevg"></span>

<span id="ieee_802.3_100basevg"></span>**IEEE 802,3 100BASEVG** (32)


</dt> <dd></dd> <dt>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>

<span id="IEEE_802.5_Token-Ring"></span><span id="ieee_802.5_token-ring"></span><span id="IEEE_802.5_TOKEN-RING"></span>**Token ring do IEEE 802,5** (33)


</dt> <dd></dd> <dt>

<span id="ANSI_X3T9.5_FDDI"></span><span id="ansi_x3t9.5_fddi"></span>

<span id="ansi_x3t9.5_fddi"></span>**ANSI X3T 9.5 FDDI** (34)


</dt> <dd></dd> <dt>

<span id="MCA"></span><span id="mca"></span>

<span id="MCA"></span><span id="mca"></span>**MCA** (35)


</dt> <dd></dd> <dt>

<span id="ESDI"></span><span id="esdi"></span>

<span id="ESDI"></span><span id="esdi"></span>**ESDI** (36)


</dt> <dd></dd> <dt>

<span id="IDE"></span><span id="ide"></span>

<span id="IDE"></span><span id="ide"></span>**IDE** (37)


</dt> <dd></dd> <dt>

<span id="CMD"></span><span id="cmd"></span>

<span id="CMD"></span><span id="cmd"></span>**Cmd** (38)


</dt> <dd></dd> <dt>

<span id="ST506"></span><span id="st506"></span>

<span id="ST506"></span><span id="st506"></span>**ST506** (39)


</dt> <dd></dd> <dt>

<span id="DSSI"></span><span id="dssi"></span>

<span id="DSSI"></span><span id="dssi"></span>**DSSI** (40)


</dt> <dd></dd> <dt>

<span id="QIC2"></span><span id="qic2"></span>

<span id="QIC2"></span><span id="qic2"></span>**QIC2** (41)


</dt> <dd></dd> <dt>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>

<span id="Enhanced_ATA_IDE"></span><span id="enhanced_ata_ide"></span><span id="ENHANCED_ATA_IDE"></span>**ATA/IDE avançado** (42)


</dt> <dd></dd> <dt>

<span id="AGP"></span><span id="agp"></span>

<span id="AGP"></span><span id="agp"></span>**AGP** (43)


</dt> <dd></dd> <dt>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>

<span id="TWIRP__two-way_infrared_"></span><span id="twirp__two-way_infrared_"></span><span id="TWIRP__TWO-WAY_INFRARED_"></span>**TWIRP (infravermelho bidirecional)** (44)


</dt> <dd></dd> <dt>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>

<span id="FIR__fast_infrared_"></span><span id="fir__fast_infrared_"></span><span id="FIR__FAST_INFRARED_"></span>**Fir (infravermelho rápido)** (45)


</dt> <dd></dd> <dt>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>

<span id="SIR__serial_infrared_"></span><span id="sir__serial_infrared_"></span><span id="SIR__SERIAL_INFRARED_"></span>**Sir (infravermelho serial)** (46)


</dt> <dd></dd> <dt>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>

<span id="IrBus"></span><span id="irbus"></span><span id="IRBUS"></span>**IrBus** (47)


</dt> <dd></dd> </dl>

</dd> <dt>

**ProviderType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvSubType")
</dt> </dl>

Tipo de provedor de comunicações.

Os valores são:

<dl> <dd>"Dispositivo de FAX"</dd> <dd>"Protocolo LAT"</dd> <dd>"Dispositivo de modem"</dd> <dd>"Ponte de rede"</dd> <dd>"Porta paralela"</dd> <dd>"Porta serial RS232"</dd> <dd>"Porta RS422"</dd> <dd>"Porta RS423"</dd> <dd>"Porta RS449"</dd> <dd>"Dispositivo de scanner"</dd> <dd>"TelNet TCP/IP"</dd> <dd>"X. 25"</dd> <dd>Não especificado</dd> </dl>

<dt>

<span id="FAX_Device"></span><span id="fax_device"></span><span id="FAX_DEVICE"></span>

**Dispositivo de fax** ("dispositivo de fax")


</dt> <dd></dd> <dt>

<span id="LAT_Protocol"></span><span id="lat_protocol"></span><span id="LAT_PROTOCOL"></span>

**Protocolo Lat** ("protocolo Lat")


</dt> <dd></dd> <dt>

<span id="Modem_Device"></span><span id="modem_device"></span><span id="MODEM_DEVICE"></span>

**Dispositivo de modem** ("dispositivo de modem")


</dt> <dd></dd> <dt>

<span id="Network_Bridge"></span><span id="network_bridge"></span><span id="NETWORK_BRIDGE"></span>

**Ponte de rede** ("ponte de rede")


</dt> <dd></dd> <dt>

<span id="Parallel_Port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

**Porta paralela** ("porta paralela")


</dt> <dd></dd> <dt>

<span id="RS232_Serial_Port"></span><span id="rs232_serial_port"></span><span id="RS232_SERIAL_PORT"></span>

**Porta serial RS232** ("porta serial RS232")


</dt> <dd></dd> <dt>

<span id="RS422_Port"></span><span id="rs422_port"></span><span id="RS422_PORT"></span>

**Porta RS422** ("porta RS422")


</dt> <dd></dd> <dt>

<span id="RS423_Port"></span><span id="rs423_port"></span><span id="RS423_PORT"></span>

**Porta RS423** ("porta RS423")


</dt> <dd></dd> <dt>

<span id="RS449_Port"></span><span id="rs449_port"></span><span id="RS449_PORT"></span>

**Porta RS449** ("porta RS449")


</dt> <dd></dd> <dt>

<span id="Scanner_Device"></span><span id="scanner_device"></span><span id="SCANNER_DEVICE"></span>

**Dispositivo de scanner** ("dispositivo de scanner")


</dt> <dd></dd> <dt>

<span id="TCP_IP_TelNet"></span><span id="tcp_ip_telnet"></span><span id="TCP_IP_TELNET"></span>

**Telnet TCP/IP** ("Telnet TCP/IP")


</dt> <dd></dd> <dt>

<span id="X.25"></span><span id="x.25"></span>

**X. 25** ("X. 25")


</dt> <dd></dd> <dt>

<span id="Unspecified"></span><span id="unspecified"></span><span id="UNSPECIFIED"></span>

**Não especificado** ("não especificado")


</dt> <dd></dd> </dl>

</dd> <dt>

**SettableBaudRate**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ baud")
</dt> </dl>

Se **for true**, a taxa de transmissão poderá ser alterada para essa porta serial.

</dd> <dt>

**SettableDataBits**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ DataBits")
</dt> </dl>

Se **for true**, os bits de dados poderão ser definidos para essa porta serial.

</dd> <dt>

**SettableFlowControl**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ handshake")
</dt> </dl>

Se **for true**, o controle de fluxo poderá ser definido para essa porta serial.

</dd> <dt>

**SettableParity**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ Parity")
</dt> </dl>

Se **for true**, a paridade poderá ser definida para essa porta serial.

</dd> <dt>

**SettableParityCheck**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ Parity \_ check")
</dt> </dl>

Se **for true**, a verificação de paridade poderá ser definida para essa porta serial (se houver suporte para a verificação de paridade).

</dd> <dt>

**SettableRLSD**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ RLSD")
</dt> </dl>

Se **verdadeiro**, a RLSD (detecção de sinal de linha) recebida pode ser definida para esta porta serial (se houver suporte para RLSD).

</dd> <dt>

**SettableStopBits**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwSettableParams \| SP \_ STOPBITS")
</dt> </dl>

Se **for true**, os bits de parada poderão ser definidos para essa porta serial.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Status atual do objeto. Vários status de operação e não operacional podem ser definidos. Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo). Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço". O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Os valores incluem o seguinte:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Falha de Pred** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sob estresse** ("sob estresse")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Não **recuperar** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de comunicação** ("perda de comunicação")


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")
</dt> </dl>

Estado do dispositivo lógico. Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


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

**Supports16BitMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ 16BITMODE")
</dt> </dl>

Se for **true**, o modo de 16 bits terá suporte nesta porta serial.

</dd> <dt>

**SupportsDTRDSR**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ DTRDSR")
</dt> </dl>

Se for **verdadeiro**, os sinais de DTR (Data Terminal Ready) e Data Set Ready (DSR) têm suporte nesta porta serial.

</dd> <dt>

**SupportsElapsedTimeouts**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ TOTALTIMEOUTS")
</dt> </dl>

Se **verdadeiro**, os tempos limite decorridos têm suporte nesta porta serial. Tempos limite decorridos acompanham a quantidade total de tempo entre as transmissões de dados.

</dd> <dt>

**SupportsIntTimeouts**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ INTTIMEOUTS")
</dt> </dl>

Se **for true**, haverá suporte para tempos limite de intervalo. Um tempo limite de intervalo é a quantidade de tempo permitido para decorrer entre a chegada de cada parte dos dados.

</dd> <dt>

**SupportsParityCheck**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF de verificação de \_ paridade \_ ")
</dt> </dl>

Se for **true**, haverá suporte para a verificação de paridade nesta porta serial.

</dd> <dt>

**SupportsRLSD**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ RLSD")
</dt> </dl>

Se **verdadeiro**, a RLSD (detecção de sinal de linha) recebida tem suporte nesta porta serial.

</dd> <dt>

**SupportsRTSCTS**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ RTSCTS")
</dt> </dl>

Se for **verdadeiro**, os sinais de RTS (pronto para enviar) e não criptografar para enviar (CTS) têm suporte nesta porta serial.

</dd> <dt>

**SupportsSpecialCharacters**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ SPECIALCHARS")
</dt> </dl>

Se **for true**, os caracteres de controle de porta serial têm suporte. Esses caracteres sinalizam eventos em vez de dados. Esses caracteres não são exibíveis e são definidos pelo driver. Eles incluem EofChar, ErrorChar, BreakChar, EventChar, XonChar e XoffChar.

</dd> <dt>

**SupportsXOnXOff**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ XONXOFF")
</dt> </dl>

Se for **true**, o controle de fluxo XON ou XOFF terá suporte nesta porta serial.

</dd> <dt>

**SupportsXOnXOffSet**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estruturas de comunicação win32api \| [**COMMPROP**](/windows/win32/api/winbase/ns-winbase-commprop) \| dwProvCapabilities \| PCF \_ SETXCHAR")
</dt> </dl>

Se **for true**, o provedor de comunicações dará suporte à configuração da configuração de controle de fluxo XONor XOFF.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Valor da propriedade **CreationClassName** do computador de escopo.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nome do sistema de escopo.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data e hora da última redefinição deste controlador. Isso pode significar que o controlador estava desligado ou reinicializado.

Essa propriedade é herdada [**do \_ controlador CIM**](cim-controller.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ SerialPort do Win32** é derivada do [**CIM \_ SerialController**](cim-serialcontroller.md).

## <a name="examples"></a>Exemplos

Para obter um método alternativo de recuperação de informações de porta serial (do registro), consulte o exemplo [enumerar portas](https://Gallery.TechNet.Microsoft.Com/scriptcenter/087b4d73-4a5e-4746-b365-ad682911360e) Visual Basic.

O exemplo do PowerShell [listar Propriedades de portas seriais](https://Gallery.TechNet.Microsoft.Com/42ff8eab-7d2b-4549-b178-835daecf4f12) retorna informações sobre as portas de série instaladas em um computador.

O exemplo de VBScript a seguir retorna informações sobre as portas de série instaladas em um computador.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_SerialPort") 
 
For Each objItem in colItems 
    Wscript.Echo "Binary: " & objItem.Binary 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Device ID: " & objItem.DeviceID 
    Wscript.Echo "Maximum Baud Rate: " & objItem.MaxBaudRate 
    Wscript.Echo "Maximum Input Buffer Size: " & objItem.MaximumInputBufferSize 
    Wscript.Echo "Maximum Output Buffer Size: " & _ 
        objItem.MaximumOutputBufferSize 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "OS Auto Discovered: " & objItem.OSAutoDiscovered 
    Wscript.Echo "PNP Device ID: " & objItem.PNPDeviceID 
    Wscript.Echo "Provider Type: " & objItem.ProviderType 
    Wscript.Echo "Settable Baud Rate: " & objItem.SettableBaudRate 
    Wscript.Echo "Settable Data Bits: " & objItem.SettableDataBits 
    Wscript.Echo "Settable Flow Control: " & objItem.SettableFlowControl 
    Wscript.Echo "Settable Parity: " & objItem.SettableParity 
    Wscript.Echo "Settable Parity Check: " & objItem.SettableParityCheck 
    Wscript.Echo "Settable RLSD: " & objItem.SettableRLSD 
    Wscript.Echo "Settable Stop Bits: " & objItem.SettableStopBits 
    Wscript.Echo "Supports 16-Bit Mode: " & objItem.Supports16BitMode 
    Wscript.Echo "Supports DTRDSR: " & objItem.SupportsDTRDSR 
    Wscript.Echo "Supports Elapsed Timeouts: " & _ 
        objItem.SupportsElapsedTimeouts 
    Wscript.Echo "Supports Int Timeouts: " & objItem.SupportsIntTimeouts 
    Wscript.Echo "Supports Parity Check: " & objItem.SupportsParityCheck 
    Wscript.Echo "Supports RLSD: " & objItem.SupportsRLSD 
    Wscript.Echo "Supports RTSCTS: " & objItem.SupportsRTSCTS 
    Wscript.Echo "Supports Special Characters: " & _ 
        objItem.SupportsSpecialCharacters 
    Wscript.Echo "Supports XOn XOff: " & objItem.SupportsXOnXOff 
    Wscript.Echo "Supports XOn XOff Setting: " & objItem.SupportsXOnXOffSet 
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SERIALCONTROLLER CIM**](cim-serialcontroller.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
