---
description: O Win32 \_ CacheMemory&\# 32; A classe WMI representa a memória de cache interna e externa em um sistema de computador.
ms.assetid: 9cfb992d-fbac-4e56-b4f3-61c0c93f5852
ms.tgt_platform: multiple
title: Classe Win32_CacheMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CacheMemory
- Win32_CacheMemory.Reset
- Win32_CacheMemory.SetPowerState
- Win32_CacheMemory.Access
- Win32_CacheMemory.AdditionalErrorData
- Win32_CacheMemory.Associativity
- Win32_CacheMemory.Availability
- Win32_CacheMemory.BlockSize
- Win32_CacheMemory.CacheSpeed
- Win32_CacheMemory.CacheType
- Win32_CacheMemory.Caption
- Win32_CacheMemory.ConfigManagerErrorCode
- Win32_CacheMemory.ConfigManagerUserConfig
- Win32_CacheMemory.CorrectableError
- Win32_CacheMemory.CreationClassName
- Win32_CacheMemory.CurrentSRAM
- Win32_CacheMemory.Description
- Win32_CacheMemory.DeviceID
- Win32_CacheMemory.EndingAddress
- Win32_CacheMemory.ErrorAccess
- Win32_CacheMemory.ErrorAddress
- Win32_CacheMemory.ErrorCleared
- Win32_CacheMemory.ErrorCorrectType
- Win32_CacheMemory.ErrorData
- Win32_CacheMemory.ErrorDataOrder
- Win32_CacheMemory.ErrorDescription
- Win32_CacheMemory.ErrorInfo
- Win32_CacheMemory.ErrorMethodology
- Win32_CacheMemory.ErrorResolution
- Win32_CacheMemory.ErrorTime
- Win32_CacheMemory.ErrorTransferSize
- Win32_CacheMemory.FlushTimer
- Win32_CacheMemory.InstallDate
- Win32_CacheMemory.InstalledSize
- Win32_CacheMemory.LastErrorCode
- Win32_CacheMemory.Level
- Win32_CacheMemory.LineSize
- Win32_CacheMemory.Location
- Win32_CacheMemory.MaxCacheSize
- Win32_CacheMemory.Name
- Win32_CacheMemory.NumberOfBlocks
- Win32_CacheMemory.OtherErrorDescription
- Win32_CacheMemory.PNPDeviceID
- Win32_CacheMemory.PowerManagementCapabilities
- Win32_CacheMemory.PowerManagementSupported
- Win32_CacheMemory.Purpose
- Win32_CacheMemory.ReadPolicy
- Win32_CacheMemory.ReplacementPolicy
- Win32_CacheMemory.StartingAddress
- Win32_CacheMemory.Status
- Win32_CacheMemory.StatusInfo
- Win32_CacheMemory.SupportedSRAM
- Win32_CacheMemory.SystemCreationClassName
- Win32_CacheMemory.SystemLevelAddress
- Win32_CacheMemory.SystemName
- Win32_CacheMemory.WritePolicy
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a16a0723ecad2723952bafa77b8a8945475073c5b1330103cc4a7e4b456ea0e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986346"
---
# <a name="win32_cachememory-class"></a>\_Classe Win32 CacheMemory

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CacheMemory do Win32** representa a memória de cache interna e externa em um sistema de computador.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B97-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_CacheMemory : CIM_CacheMemory
{
  uint16   Access;
  uint8    AdditionalErrorData[];
  uint16   Associativity;
  uint16   Availability;
  uint64   BlockSize;
  uint32   CacheSpeed;
  uint16   CacheType;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  boolean  CorrectableError;
  string   CreationClassName;
  uint16   CurrentSRAM[];
  string   Description;
  string   DeviceID;
  uint64   EndingAddress;
  uint16   ErrorAccess;
  uint64   ErrorAddress;
  boolean  ErrorCleared;
  uint16   ErrorCorrectType;
  uint8    ErrorData[];
  uint16   ErrorDataOrder;
  string   ErrorDescription;
  uint16   ErrorInfo;
  string   ErrorMethodology;
  uint64   ErrorResolution;
  datetime ErrorTime;
  uint32   ErrorTransferSize;
  uint32   FlushTimer;
  datetime InstallDate;
  uint32   InstalledSize;
  uint32   LastErrorCode;
  uint16   Level;
  uint32   LineSize;
  uint16   Location;
  uint32   MaxCacheSize;
  string   Name;
  uint64   NumberOfBlocks;
  string   OtherErrorDescription;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   Purpose;
  uint16   ReadPolicy;
  uint16   ReplacementPolicy;
  uint64   StartingAddress;
  string   Status;
  uint16   StatusInfo;
  uint16   SupportedSRAM[];
  string   SystemCreationClassName;
  boolean  SystemLevelAddress;
  string   SystemName;
  uint16   WritePolicy;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ CacheMemory** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ CacheMemory** tem esses métodos.



| Método            | Descrição                                                                                                                                                                                                  |
|:------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Redefinir**         | Não implementado. Para implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ CacheMemory**](cim-cachememory.md) para obter a documentação.<br/>                 |
| **SetPowerState** | Não implementado. Para implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ CacheMemory**](cim-cachememory.md) para obter a documentação.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ CacheMemory** tem essas propriedades.

<dl> <dt>

**Acesso**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de acesso.

Essa propriedade é herdada do [**CIM \_ StorageExtent**](cim-storageextent.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>

<span id="Readable"></span><span id="readable"></span><span id="READABLE"></span>**Legível** (1)


</dt> <dd></dd> <dt>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>

<span id="Writeable"></span><span id="writeable"></span><span id="WRITEABLE"></span>**Gravável** (2)


</dt> <dd>

Gravável

</dd> <dt>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>

<span id="Read_Write_Supported"></span><span id="read_write_supported"></span><span id="READ_WRITE_SUPPORTED"></span>**Suporte de leitura/gravação** (3)


</dt> <dd></dd> <dt>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>

<span id="Write_Once"></span><span id="write_once"></span><span id="WRITE_ONCE"></span>**Gravar uma vez** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**AdditionalErrorData**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,18 "," MIF. \|Matriz de memória física da DMTF \| 1,13 "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)
</dt> </dl>

Matriz de octetos que contém informações de erro adicionais. Um exemplo é a síndrome de ECC ou o retorno dos bits de verificação se uma metodologia de erro baseada em CRC for usada. No último caso, se um erro de bit único for reconhecido e o algoritmo CRC for conhecido, será possível determinar o bit exato que falhou. Esse tipo de dados (síndrome de ECC, bit de verificação, dados de bits de paridade ou outras informações fornecidas pelo fornecedor) está incluído neste campo. Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.

Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).

</dd> <dt>

**Capacidade de associação**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Cache do sistema DMTF \| 3,15 ")
</dt> </dl>

Uma enumeração de inteiros que define a associação de cache do sistema.

Esse valor é proveniente do membro de **Associação** da estrutura de **informações de cache** nas informações de SMBIOS.

Essa propriedade é herdada do [**CIM \_ CacheMemory**](cim-cachememory.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Direct_Mapped"></span><span id="direct_mapped"></span><span id="DIRECT_MAPPED"></span>

**Mapeado direto** (3)


</dt> <dd></dd> <dt>

<span id="2-way_Set-Associative"></span><span id="2-way_set-associative"></span><span id="2-WAY_SET-ASSOCIATIVE"></span>

**conjunto de 2 vias-associativo** (4)


</dt> <dd></dd> <dt>

<span id="4-way_Set-Associative"></span><span id="4-way_set-associative"></span><span id="4-WAY_SET-ASSOCIATIVE"></span>

**conjunto de 4 vias-associativo** (5)


</dt> <dd></dd> <dt>

<span id="Fully_Associative"></span><span id="fully_associative"></span><span id="FULLY_ASSOCIATIVE"></span>

**Totalmente associativo** (6)


</dt> <dd></dd> <dt>

<span id="8-way_Set-Associative"></span><span id="8-way_set-associative"></span><span id="8-WAY_SET-ASSOCIATIVE"></span>

**conjunto de 8 vias – associativo** (7)


</dt> <dd></dd> <dt>

<span id="16-way_Set-Associative"></span><span id="16-way_set-associative"></span><span id="16-WAY_SET-ASSOCIATIVE"></span>

**conjunto de 16 vias – associativo** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**Disponibilidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")
</dt> </dl>

Disponibilidade e status do dispositivo.

Esse valor é proveniente do membro de **configuração de cache** da estrutura de **informações de cache** nas informações de SMBIOS.

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

**BlockSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| host-REsources-MIB. hrStorageAllocationUnits "), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")
</dt> </dl>

Tamanho em bytes dos blocos que formam essa extensão de armazenamento. Se desconhecido ou se um conceito de bloco não for válido (por exemplo, para extensão de agregação, memória ou discos lógicos), insira um 1.

Essa propriedade é herdada de [**Cim \_ StorageExtent.**](cim-storageextent.md)

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**CacheSpeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 7 Cache \| Speed"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("nanossegundos")
</dt> </dl>

Velocidade do cache.

Esse valor vem do membro **Velocidade do Cache** da estrutura Informações do **Cache** nas informações do SMBIOS.

</dd> <dt>

**CacheType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Cache do Sistema DMTF \| \| 003.9")
</dt> </dl>

Tipo de cache.

Esse valor vem do membro **Tipo de Cache do** Sistema da estrutura Informações do **Cache** nas informações do SMBIOS.

Essa propriedade é herdada [**de Cim \_ CacheMemory.**](cim-cachememory.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Instruction"></span><span id="instruction"></span><span id="INSTRUCTION"></span>

**Instrução** (3)


</dt> <dd></dd> <dt>

<span id="Data"></span><span id="data"></span><span id="DATA"></span>

**Dados** (4)


</dt> <dd></dd> <dt>

<span id="Unified"></span><span id="unified"></span><span id="UNIFIED"></span>

**Unificado** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Legenda")
</dt> </dl>

Descrição curta do objeto uma cadeia de caracteres de uma linha.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

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

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows ainda está configurando esse dispositivo.** (25)


</dt> <dd>

Windows ainda está configurando o dispositivo.

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows ainda está configurando esse dispositivo.** (26)


</dt> <dd>

Windows ainda está configurando o dispositivo.

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Esse dispositivo não tem configuração de log válida.** (27)


</dt> <dd>

O dispositivo não tem configuração de log válida.

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.** (28)


</dt> <dd>

Os drivers de dispositivo não estão instalados.

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Esse dispositivo está desabilitado porque o firmware do dispositivo não lhe deu os recursos necessários.** (29)


</dt> <dd>

O dispositivo está desabilitado. O firmware do dispositivo não forneceu os recursos necessários.

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Esse dispositivo está usando um recurso IRQ (Solicitação de Interrupção) que outro dispositivo está usando.** (30)


</dt> <dd>

O dispositivo está usando um recurso IRQ que outro dispositivo está usando.

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Esse dispositivo não está funcionando corretamente porque Windows pode carregar os drivers necessários para esse dispositivo.** (31)


</dt> <dd>

O dispositivo não está funcionando corretamente. Windows pode carregar os drivers de dispositivo necessários.

</dd> </dl>

</dd> <dt>

**ConfigManagerUserConfig**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Se **True**, o dispositivo está usando uma configuração definida pelo usuário.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**CorrectableError**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Dispositivo de memória DMTF \| \| 002.12", "MIF. Matriz de memória física DMTF \| \| 001.8")
</dt> </dl>

Se **True**, o erro mais recente foi corrigida. Se a **propriedade ErrorInfo** for igual a 3 (OK), essa propriedade não terá nenhum significado.

Essa propriedade é herdada da [**Memória CIM. \_**](cim-memory.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **Chave CIM \_**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância. Quando usada com as outras propriedades de chave da classe , a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**CurrentSRAM**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tipo SMBIOS \| 7 \| Tipo SRAM Atual")
</dt> </dl>

Matriz de tipos de SRAM (Memória de Acesso Aleatório Estático) que está sendo usada para a memória de cache.

Esse valor vem do membro **do Tipo SRAM** Atual da estrutura Informações **de Cache** nas informações do SMBIOS.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (0)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (1)


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

**Não estouro** (2)


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

**Burst** (3)


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

**Estouro de** pipeline (4)


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

**Síncrono** (5)


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

**Assíncrono** (6)


</dt> <dd></dd> </dl>

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

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("DeviceId"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI")
</dt> </dl>

Identificador exclusivo do cache representado por uma instância do **\_ Win32 CacheMemory.**

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

Exemplo: "Memória de cache 1"

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Endereços mapeados da matriz de memória DMTF \| \| 001.4", "MIF. Endereços mapeados do dispositivo de memória DMTF \| \| 001.5"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes")
</dt> </dl>

Endereço final, referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória, para esse objeto de memória. O endereço final é especificado em quilobytes.

Essa propriedade é herdada da [**Memória CIM. \_**](cim-memory.md)

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**ErrorAccess**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Dispositivo de memória DMTF \| \| 002.15", "MIF. Matriz de memória física DMTF \| \| 001.10")
</dt> </dl>

Operação de acesso à memória que causou o último erro. O tipo de erro é descrito pela **propriedade ErrorInfo.** Se **ErrorInfo** for igual a 3 (OK), essa propriedade não terá nenhum significado.

Essa propriedade é herdada da [**Memória CIM. \_**](cim-memory.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**Leitura** (3)


</dt> <dd></dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>

**Gravação** (4)


</dt> <dd></dd> <dt>

<span id="Partial_Write"></span><span id="partial_write"></span><span id="PARTIAL_WRITE"></span>

**Gravação parcial** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,19 "," MIF. \|Dispositivo de memória DMTF \| 2,20 "," MIF. \|Matriz de memória física da DMTF \| 1,14 ")
</dt> </dl>

Endereço do último erro de memória. O tipo de erro é descrito pela propriedade **errorInfo** . Se **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.

Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

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

**ErrorCorrectType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| tipo de correção de erro do tipo SMBIOS 7 \| ")
</dt> </dl>

Método de correção de erro usado pela memória de cache.

Esse valor é proveniente do membro de **tipo de correção de erro** da estrutura de informações de **cache** nas informações de SMBIOS.

<dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reservado** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (3)


</dt> <dd></dd> <dt>

<span id="Parity"></span><span id="parity"></span><span id="PARITY"></span>

**Paridade** (4)


</dt> <dd></dd> <dt>

<span id="Single-bit_ECC"></span><span id="single-bit_ecc"></span><span id="SINGLE-BIT_ECC"></span>

**ECC de bit único** (5)


</dt> <dd></dd> <dt>

<span id="Multi-bit_ECC"></span><span id="multi-bit_ecc"></span><span id="MULTI-BIT_ECC"></span>

**ECC de vários bits** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorData**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,17 "," MIF. \|Matriz de memória física da DMTF \| 1,12 "), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (64)
</dt> </dl>

Matriz de dados capturados durante o último acesso de memória incorreto. Os dados ocupam os primeiros *n* octetos da matriz necessários para manter o número de bits especificado pela propriedade **ErrorTransferSize** . Se **ErrorTransferSize** for 0 (zero), essa propriedade não terá significado.

Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).

</dd> <dt>

**ErrorDataOrder**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Ordenação de dados armazenados na propriedade **ErrorData** . Se **ErrorTransferSize** for 0 (zero), essa propriedade não terá significado.

Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Least_Significant_Byte_First"></span><span id="least_significant_byte_first"></span><span id="LEAST_SIGNIFICANT_BYTE_FIRST"></span>

**Byte menos significativo primeiro** (1)


</dt> <dd></dd> <dt>

<span id="Most_Significant_Byte_First"></span><span id="most_significant_byte_first"></span><span id="MOST_SIGNIFICANT_BYTE_FIRST"></span>

**Byte mais significativo primeiro** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.

Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).

</dd> <dt>

**ErrorInfo**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,12 "," MIF. \|Matriz de memória física da DMTF \| 1,8 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ memória CIM**](cim-memory.md).**OtherErrorDescription**")
</dt> </dl>

Tipo de erro que ocorreu mais recentemente. Os valores 12-14 são indefinidos no esquema CIM porque, no DMI, eles misturam a semântica do tipo de erro e se ele era corrigível ou não. O último é indicado na propriedade **CorrectableError**.

Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="OK"></span><span id="ok"></span>

**OK** (3)


</dt> <dd></dd> <dt>

<span id="Bad_Read"></span><span id="bad_read"></span><span id="BAD_READ"></span>

**Leitura inadequada** (4)


</dt> <dd></dd> <dt>

<span id="Parity_Error"></span><span id="parity_error"></span><span id="PARITY_ERROR"></span>

**Erro de paridade** (5)


</dt> <dd></dd> <dt>

<span id="Single-Bit_Error"></span><span id="single-bit_error"></span><span id="SINGLE-BIT_ERROR"></span>

**Erro de bit único** (6)


</dt> <dd></dd> <dt>

<span id="Double-Bit_Error"></span><span id="double-bit_error"></span><span id="DOUBLE-BIT_ERROR"></span>

**Erro de bit duplo** (7)


</dt> <dd></dd> <dt>

<span id="Multi-Bit_Error"></span><span id="multi-bit_error"></span><span id="MULTI-BIT_ERROR"></span>

**Erro de vários bits** (8)


</dt> <dd></dd> <dt>

<span id="Nibble_Error"></span><span id="nibble_error"></span><span id="NIBBLE_ERROR"></span>

**Erro de Nibble** (9)


</dt> <dd></dd> <dt>

<span id="Checksum_Error"></span><span id="checksum_error"></span><span id="CHECKSUM_ERROR"></span>

**Erro de soma de verificação** (10)


</dt> <dd></dd> <dt>

<span id="CRC_Error"></span><span id="crc_error"></span><span id="CRC_ERROR"></span>

**Erro de CRC** (11)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Indefinido** (12)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Indefinido** (13)


</dt> <dd></dd> <dt>

<span id="Undefined"></span><span id="undefined"></span><span id="UNDEFINED"></span>

**Indefinido** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorMethodology**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Matriz de memória física da DMTF \| 1,7 ")
</dt> </dl>

Detalhes sobre os algoritmos de paridade ou CRC, ECC ou outros mecanismos usados.

Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).

</dd> <dt>

**ErrorResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,21 "," MIF. \|Matriz de memória física da DMTF \| 1,15 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bytes ")
</dt> </dl>

Intervalo, em bytes, para o qual o último erro pode ser resolvido. Por exemplo, se os endereços de erro forem resolvidos para o bit 11 (ou seja, em uma base de página típica), os erros poderão ser resolvidos para os limites de 4 KB e essa propriedade será definida como 4000. Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.

Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**ErrorTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Hora em que ocorreu o último erro de memória. O tipo de erro é descrito pela propriedade **errorInfo** . Se a propriedade **errorInfo** for igual a 3 (OK), essa propriedade não terá significado.

Essa propriedade é herdada [**da \_ memória CIM**](cim-memory.md).

</dd> <dt>

**ErrorTransferSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Dispositivo de memória DMTF \| 2,16 "," MIF. \|Matriz de memória física da DMTF \| 1,11 "), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) (" bits ")
</dt> </dl>

Tamanho da transferência de dados em bits que causou o último erro. 0 (zero) indica que não há erro. Se a **propriedade ErrorInfo** for igual a 3 (OK), essa propriedade deverá ser definida como 0 (zero).

Essa propriedade é herdada da [**Memória CIM. \_**](cim-memory.md)

</dd> <dt>

**FlushTimer**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Cache do Sistema DMTF \| \| 003,14"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("segundos")
</dt> </dl>

A quantidade máxima de tempo, em segundos, linhas sujas ou buckets podem permanecer no cache antes que sejam liberados. Um valor de 0 (zero) indica que uma liberação de cache não é controlada por um temporizador de liberação.

Essa propriedade é herdada [**de Cim \_ CacheMemory.**](cim-cachememory.md)

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

**InstalledSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tamanho Instalado do tipo SMBIOS \| \| 7"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes")
</dt> </dl>

Tamanho atual da memória de cache instalada.

Esse valor vem do **membro Tamanho Instalado** da estrutura Informações do **Cache** nas informações do SMBIOS.

</dd> <dt>

**LastErrorCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Último código de erro relatado pelo dispositivo lógico.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Level**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Cache do Sistema DMTF \| \| 003.2")
</dt> </dl>

Nível do cache.

Esse valor vem do membro **de Configuração de Cache** da estrutura Informações do **Cache** nas informações do SMBIOS.

Essa propriedade é herdada [**de Cim \_ CacheMemory.**](cim-cachememory.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>**Primário** (3)


</dt> <dd></dd> <dt>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>

<span id="Secondary"></span><span id="secondary"></span><span id="SECONDARY"></span>**Secundário** (4)


</dt> <dd></dd> <dt>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>

<span id="Tertiary"></span><span id="tertiary"></span><span id="TERTIARY"></span>**Terciário** (5)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**LineSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Cache do Sistema DMTF \| \| 003.10"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes")
</dt> </dl>

Tamanho, em bytes, de um único bucket de cache ou linha.

Essa propriedade é herdada [**de Cim \_ CacheMemory.**](cim-cachememory.md)

</dd> <dt>

**Localização**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| Type 7 \| Location")
</dt> </dl>

Local físico da memória do cache.

Esse valor vem do membro **de Configuração de Cache** da estrutura Informações do **Cache** nas informações do SMBIOS.

<dt>

<span id="Internal"></span><span id="internal"></span><span id="INTERNAL"></span>

**Interno** (0)


</dt> <dd></dd> <dt>

<span id="External"></span><span id="external"></span><span id="EXTERNAL"></span>

**Externo** (1)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Reservado** (2)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**MaxCacheSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tamanho máximo do cache do tipo SMBIOS \| \| 7"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes")
</dt> </dl>

Tamanho máximo de cache instalado para essa memória de cache específica.

Esse valor vem do membro **Tamanho Máximo do Cache** da estrutura Informações do **Cache** nas informações do SMBIOS.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome")
</dt> </dl>

Rótulo pelo qual o objeto é conhecido. Quando subclasse, a propriedade pode ser substituído para ser uma propriedade de chave.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**NumberOfBlocks**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| HOST-RESOURCES-MIB.hrStorageSize")
</dt> </dl>

Número total de blocos consecutivos, cada um bloqueia o tamanho do valor contido na propriedade **BlockSize,** que formam essa extensão de armazenamento. O tamanho total da extensão de armazenamento pode ser calculado multiplicando o valor da propriedade **BlockSize** pelo valor dessa propriedade. Se o valor de **BlockSize** for 1, essa propriedade será o tamanho total da extensão de armazenamento.

Essa propriedade é herdada de [**Cim \_ StorageExtent.**](cim-storageextent.md)

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> <dt>

**OtherErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**MEMÓRIA CIM \_**](cim-memory.md).**ErrorInfo**")
</dt> </dl>

Cadeia de caracteres de forma livre que fornece mais informações se a **propriedade ErrorType** está definida como 1, Outros. Caso contrário, essa cadeia de caracteres não tem nenhum significado.

Essa propriedade é herdada da [**Memória CIM. \_**](cim-memory.md)

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")
</dt> </dl>

Windows Plug and Play identificador de dispositivo lógico do dispositivo lógico.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

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

Tempo Power-On com suporte

O [**método SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (Power Cycle) e *Time* definido como uma data e hora específicas, ou intervalo, para o power-on.

</dd> </dl>

</dd> <dt>

**PowerManagementSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **True**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante). A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Finalidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres de forma livre que descreve a mídia e seu uso.

Esse valor vem do membro **Designação de** Soquete da estrutura **Informações de Cache** nas informações do SMBIOS.

Essa propriedade é herdada de [**Cim \_ StorageExtent.**](cim-storageextent.md)

</dd> <dt>

**ReadPolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Cache do Sistema DMTF \| \| 003.13")
</dt> </dl>

Política que deve ser empregada pelo cache para lidar com solicitações de leitura.

Essa propriedade é herdada [**de Cim \_ CacheMemory.**](cim-cachememory.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>

**Leitura** (3)


</dt> <dd></dd> <dt>

<span id="Read-Ahead"></span><span id="read-ahead"></span><span id="READ-AHEAD"></span>

**Leitura antecipada** (4)


</dt> <dd></dd> <dt>

<span id="Read_and_Read-Ahead"></span><span id="read_and_read-ahead"></span><span id="READ_AND_READ-AHEAD"></span>

**Leitura e leitura antecipada** (5)


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

**Determinação por E/S** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplacementPolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Cache do Sistema DMTF \| \| 003.12")
</dt> </dl>

Algoritmo para determinar quais linhas de cache ou buckets devem ser reutilizados.

Essa propriedade é herdada [**de Cim \_ CacheMemory.**](cim-cachememory.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Least_Recently_Used__LRU_"></span><span id="least_recently_used__lru_"></span><span id="LEAST_RECENTLY_USED__LRU_"></span>

**LRU (menos usado recentemente)** (3)


</dt> <dd></dd> <dt>

<span id="First_In_First_Out__FIFO_"></span><span id="first_in_first_out__fifo_"></span><span id="FIRST_IN_FIRST_OUT__FIFO_"></span>

**Primeiro a entrar (FIFO)** (4)


</dt> <dd></dd> <dt>

<span id="Last_In_First_Out__LIFO_"></span><span id="last_in_first_out__lifo_"></span><span id="LAST_IN_FIRST_OUT__LIFO_"></span>

**Último a entrar primeiro (LIFO)** (5)


</dt> <dd></dd> <dt>

<span id="Least_Frequently_Used__LFU_"></span><span id="least_frequently_used__lfu_"></span><span id="LEAST_FREQUENTLY_USED__LFU_"></span>

**LFU (uso menos frequente)** (6)


</dt> <dd></dd> <dt>

<span id="Most_Frequently_Used__MFU_"></span><span id="most_frequently_used__mfu_"></span><span id="MOST_FREQUENTLY_USED__MFU_"></span>

**MFU (mais usado)** (7)


</dt> <dd></dd> <dt>

<span id="Data_Dependent_Multiple_Algorithms"></span><span id="data_dependent_multiple_algorithms"></span><span id="DATA_DEPENDENT_MULTIPLE_ALGORITHMS"></span>

**Vários algoritmos dependentes de dados** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| Memory Array Mapeado Endereços \| 001.3", "MIF. Endereços mapeados do dispositivo de memória DMTF \| \| 001.4"), [**Unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("quilobytes")
</dt> </dl>

Endereço inicial, referenciado por um aplicativo ou sistema operacional e mapeado por um controlador de memória, para esse objeto de memória. O endereço inicial é especificado em quilobytes.

Essa propriedade é herdada da [**Memória CIM. \_**](cim-memory.md)

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

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

Esse valor vem do membro **de Configuração de Cache** da estrutura Informações do **Cache** nas informações do SMBIOS.

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

**SupportedSRAM**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("tipo SMBIOS \| tipo 7 com suporte de \| SRAM")
</dt> </dl>

Matriz de tipos com suporte de SRAM (Memória de Acesso Aleatório Estático) que podem ser usados para a memória do cache.

Esse valor vem do membro **tipo SRAM com** suporte da estrutura Informações **de Cache** nas informações do SMBIOS.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (0)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (1)


</dt> <dd></dd> <dt>

<span id="Non-Burst"></span><span id="non-burst"></span><span id="NON-BURST"></span>

**Não estouro** (2)


</dt> <dd></dd> <dt>

<span id="Burst"></span><span id="burst"></span><span id="BURST"></span>

**Burst** (3)


</dt> <dd></dd> <dt>

<span id="Pipeline_Burst"></span><span id="pipeline_burst"></span><span id="PIPELINE_BURST"></span>

**Estouro de** pipeline (4)


</dt> <dd></dd> <dt>

<span id="Synchronous"></span><span id="synchronous"></span><span id="SYNCHRONOUS"></span>

**Síncrono** (5)


</dt> <dd></dd> <dt>

<span id="Asynchronous"></span><span id="asynchronous"></span><span id="ASYNCHRONOUS"></span>

**Assíncrono** (6)


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

Valor da propriedade **CreationClassName** do computador de definição de tela.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**SystemLevelAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **True**, as informações de endereço na propriedade **ErrorAddress** são um endereço no nível do sistema. Se **False**, será um endereço físico. Se a **propriedade ErrorInfo** for igual a 3, essa propriedade não terá nenhum significado.

Essa propriedade é herdada da [**Memória CIM. \_**](cim-memory.md)

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](cim-system.md).**Nome**"), [**Chave CIM \_**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Nome do sistema de scoping.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**WritePolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. Cache do Sistema DMTF \| \| 003.5")
</dt> </dl>

Escrever definição de política.

Esse valor vem do membro **de Configuração de Cache** da estrutura Informações do **Cache** nas informações do SMBIOS.

Essa propriedade é herdada [**de Cim \_ CacheMemory.**](cim-cachememory.md)

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (2)


</dt> <dd></dd> <dt>

<span id="Write_Back"></span><span id="write_back"></span><span id="WRITE_BACK"></span>

**Write-back** (3)


</dt> <dd></dd> <dt>

<span id="Write_Through"></span><span id="write_through"></span><span id="WRITE_THROUGH"></span>

**Gravar** (4)


</dt> <dd></dd> <dt>

<span id="Varies_with_Address"></span><span id="varies_with_address"></span><span id="VARIES_WITH_ADDRESS"></span>

**Varia de acordo com o endereço** (5)


</dt> <dd></dd> <dt>

<span id="Determination_Per_I_O"></span><span id="determination_per_i_o"></span><span id="DETERMINATION_PER_I_O"></span>

**Determinação por E/S** (6)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ Win32 CacheMemory** é derivada de [**Cim \_ CacheMemory.**](cim-cachememory.md)

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

[**CIM \_ CacheMemory**](cim-cachememory.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

