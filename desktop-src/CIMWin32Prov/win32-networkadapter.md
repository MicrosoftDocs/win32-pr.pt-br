---
description: A classe NetworkAdapter do Win32 \_ foi preterida. Em vez disso, use a classe MSFT \_ NetAdapter. A classe Win32 NetworkAdapterWMI representa um adaptador de rede de um computador \_ que executa um Windows operacional.
ms.assetid: f79cb2a1-a249-479d-a495-37a44fdea995
ms.tgt_platform: multiple
title: Win32_NetworkAdapter classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter
- Win32_NetworkAdapter.Reset
- Win32_NetworkAdapter.SetPowerState
- Win32_NetworkAdapter.AdapterType
- Win32_NetworkAdapter.AdapterTypeID
- Win32_NetworkAdapter.AutoSense
- Win32_NetworkAdapter.Availability
- Win32_NetworkAdapter.Caption
- Win32_NetworkAdapter.ConfigManagerErrorCode
- Win32_NetworkAdapter.ConfigManagerUserConfig
- Win32_NetworkAdapter.CreationClassName
- Win32_NetworkAdapter.Description
- Win32_NetworkAdapter.DeviceID
- Win32_NetworkAdapter.ErrorCleared
- Win32_NetworkAdapter.ErrorDescription
- Win32_NetworkAdapter.GUID
- Win32_NetworkAdapter.Index
- Win32_NetworkAdapter.InstallDate
- Win32_NetworkAdapter.Installed
- Win32_NetworkAdapter.InterfaceIndex
- Win32_NetworkAdapter.LastErrorCode
- Win32_NetworkAdapter.MACAddress
- Win32_NetworkAdapter.Manufacturer
- Win32_NetworkAdapter.MaxNumberControlled
- Win32_NetworkAdapter.MaxSpeed
- Win32_NetworkAdapter.Name
- Win32_NetworkAdapter.NetConnectionID
- Win32_NetworkAdapter.NetConnectionStatus
- Win32_NetworkAdapter.NetEnabled
- Win32_NetworkAdapter.NetworkAddresses
- Win32_NetworkAdapter.PermanentAddress
- Win32_NetworkAdapter.PhysicalAdapter
- Win32_NetworkAdapter.PNPDeviceID
- Win32_NetworkAdapter.PowerManagementCapabilities
- Win32_NetworkAdapter.PowerManagementSupported
- Win32_NetworkAdapter.ProductName
- Win32_NetworkAdapter.ServiceName
- Win32_NetworkAdapter.Speed
- Win32_NetworkAdapter.Status
- Win32_NetworkAdapter.StatusInfo
- Win32_NetworkAdapter.SystemCreationClassName
- Win32_NetworkAdapter.SystemName
- Win32_NetworkAdapter.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55ee65b151778dbfbb4bb8e09fabfb3ae59392966344b951586cd9e08dd1f984
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973022"
---
# <a name="win32_networkadapter-class"></a>Classe NetworkAdapter do Win32 \_

A **classe \_ NetworkAdapter do Win32** foi preterida. Em vez disso, use [**a classe MSFT \_ NetAdapter.**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) A classe [WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ NetworkAdapter** representa um adaptador de rede de um computador que executa um Windows operacional.

**Win32 \_ NetworkAdapter fornece** apenas dados IPv4. Para obter mais informações, consulte [Suporte a IPv6 e IPv4 no WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapter : CIM_NetworkAdapter
{
  string   AdapterType;
  uint16   AdapterTypeID;
  boolean  AutoSense;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   GUID;
  uint32   Index;
  datetime InstallDate;
  boolean  Installed;
  uint32   InterfaceIndex;
  uint32   LastErrorCode;
  string   MACAddress;
  string   Manufacturer;
  uint32   MaxNumberControlled;
  uint64   MaxSpeed;
  string   Name;
  string   NetConnectionID;
  uint16   NetConnectionStatus;
  boolean  NetEnabled;
  string   NetworkAddresses[];
  string   PermanentAddress;
  boolean  PhysicalAdapter;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProductName;
  string   ServiceName;
  uint64   Speed;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a>Membros

A **classe \_ NetworkAdapter do Win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ NetworkAdapter do Win32** tem esses métodos.



| Método                                                          | Descrição                                                                                                                                                                                                                     |
|:----------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Desabilitar**](disable-method-in-class-win32-networkadapter.md) | Desabilita o adaptador de rede.<br/>                                                                                                                                                                                        |
| [**Habilitar**](enable-method-in-class-win32-networkadapter.md)   | Habilita o adaptador de rede.<br/>                                                                                                                                                                                         |
| **Redefinir**                                                       | Não implementado. Para obter mais informações sobre como implementar esse método, consulte [**o método Reset**](reset-method-in-class-cim-controller.md) em CIM [**\_ NetworkAdapter**](cim-networkadapter.md).<br/>                 |
| **SetPowerState**                                               | Não implementado. Para obter mais informações sobre como implementar esse método, consulte [**o método SetPowerState**](setpowerstate-method-in-class-cim-controller.md) em [**CIM \_ NetworkAdapter**](cim-networkadapter.md).<br/> |



 

### <a name="properties"></a>Propriedades

A **classe \_ NetworkAdapter do Win32** tem essas propriedades.

<dl> <dt>

**AdapterType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ GEN MEDIA IN \_ \_ \_ USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")
</dt> </dl>

Meio de rede em uso. Os adaptadores de rede são os seguinte:

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802.3** ("Ethernet 802.3")


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

**Token Ring 802.5** ("Token Ring 802.5")


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

**Fiber Distributed Data Interface (FDDI)** ("Fiber Distributed Data Interface (FDDI)")


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

**WAN (Rede de Área Larga)** ("WAN (Rede de Área Larga)")


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

**LocalTalk** ("LocalTalk")


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

**Ethernet usando o formato de header DIX** ("Ethernet usando o formato de header DIX")


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

**ARCNET** ("ARCNET")


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

**ARCNET (878.2)** ("ARCNET (878.2)")


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

**ATM** ("ATM")


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

**Sem fio** ("Sem fio")


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

**Sem fio sem fio** sem fio inomeado ("sem fio sem fio")


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

**Bpc** ("Bpc")


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

**CoWan** ("CoWan")


</dt> <dd></dd> <dt>

<span id="1394"></span>

**1394** ("1394")


</dt> <dd></dd> </dl>

</dd> <dt>

**AdapterTypeID**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ GEN MEDIA IN \_ \_ \_ USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")
</dt> </dl>

Meio de rede em uso. Retorna as mesmas informações que a **propriedade AdapterType,** exceto que as informações estão na forma de um inteiro.

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802.3** (0)


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

**Token Ring 802.5** (1)


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

**Fiber Distributed Data Interface (FDDI)** (2)


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

**WAN (Rede de Área Larga)** (3)


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

**LocalTalk** (4)


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

**Ethernet usando o formato de header DIX** (5)


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

**ARCNET** (6)


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

**ARCNET (878.2)** (7)


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

**ATM** (8)


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

**Sem fio** (9)


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

**Sem fio inomeado** (10)


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

**Bpc** (11)


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

**CoWan** (12)


</dt> <dd></dd> <dt>

<span id="1394"></span>

**1394** (13)


</dt> <dd></dd> </dl>

</dd> <dt>

**Auto**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **True**, o adaptador de rede poderá determinar automaticamente a velocidade da mídia anexada ou de rede.

Essa propriedade é herdada de [**CIM \_ NetworkAdapter.**](cim-networkadapter.md)

Essa propriedade ainda não foi implementada. Ele retorna um **valor NULL** por padrão.

</dd> <dt>

**Disponibilidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Estado Operacional DMTF \| \| 003.5", "MIB. IETF \| HOST-RESOURCES-MIB.hrDeviceStatus")
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

O dispositivo é conhecido por estar em um estado de economia de energia, mas seu status exato é desconhecido.

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

O dispositivo está em um estado de aviso, embora também em um estado de economia de energia.

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

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Legenda")
</dt> </dl>

Descrição curta do objeto – uma cadeia de caracteres de uma linha.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**ConfigManagerErrorCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Windows Gerenciador de Configurações código de erro.

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

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")
</dt> </dl>

Se **True**, o dispositivo está usando uma configuração definida pelo usuário.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **Chave CIM \_**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância. Quando usada com as outras propriedades de chave da classe , a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

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

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Deviceid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [](../wmisdk/key-qualifier.md)Chave [**,**](../wmisdk/standard-qualifiers.md) Substituir ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Classe de controle CurrentControlSet do sistema Win32Registry \| \\ \\ \\ \\ \\ \\ \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")
</dt> </dl>

Identificador exclusivo do adaptador de rede de outros dispositivos no sistema.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**ErrorCleared**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **True**, o erro relatado em **LastErrorCode** agora será limpo.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser tomadas.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**GUID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identificador global exclusivo para a conexão.

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Classe de controle CurrentControlSet do sistema Win32Registry \| \\ \\ \\ \\ \\ \\ \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")
</dt> </dl>

Número de índice do adaptador de rede, armazenado no registro do sistema.

Exemplo: 0

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Data de instalação")
</dt> </dl>

Data e hora em que o objeto foi instalado. Essa propriedade não precisa de um valor para indicar que o objeto está instalado.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

Essa propriedade ainda não foi implementada. Ele retorna um **valor NULL** por padrão.

</dd> <dt>

**Instalado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**PRETERIDO,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ NetworkCards \| DriverDate")
</dt> </dl>

Se **True**, o adaptador de rede será instalado no sistema.

</dd> <dt>

**Interfaceindex**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor de índice que identifica exclusivamente o interface de rede local. O valor nessa propriedade é o mesmo que o valor na propriedade **InterfaceIndex** na instância de [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) que representa o interface de rede na tabela de rotas.

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

**MACAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Funções de entrada e saída do dispositivo Win32API \| \| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)")
</dt> </dl>

Endereço de controle de acesso de mídia para este adaptador de rede. Um endereço MAC é um número exclusivo de 48 bits atribuído ao adaptador de rede pelo fabricante. Ele identifica exclusivamente esse adaptador de rede e é usado para mapear comunicações de rede TCP/IP.

</dd> <dt>

**Fabricante**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry Software Microsoft Windows NT Fabricante de Caracteres de Rede \| \\ \\ \\ \\ \\ \\ \\ \\ CurrentVersion") \|
</dt> </dl>

Nome do fabricante do adaptador de rede.

Exemplo: "3COM"

</dd> <dt>

**MaxNumberControlled**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Número máximo de anexos da porta do Barramento DMTF \| \| 001.9") \|
</dt> </dl>

Número máximo de portas diretamente acessível com suporte por esse adaptador de rede. Um valor de 0 (zero) deverá ser usado se o número for desconhecido.

</dd> <dt>

**Maxspeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")
</dt> </dl>

Velocidade máxima, em bits por segundo, para o adaptador de rede.

Essa propriedade é herdada de [**CIM \_ NetworkAdapter.**](cim-networkadapter.md)

Essa propriedade ainda não foi implementada. Ele retorna um **valor NULL** por padrão.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nome")
</dt> </dl>

Rótulo pelo qual o objeto é conhecido. Quando subclasse, a propriedade pode ser substituído para ser uma propriedade de chave.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**NetConnectionID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Nome da conexão de rede como aparece no programa **de Conexões** Painel de Controle Rede.

</dd> <dt>

**NetConnectionStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Estado da conexão do adaptador de rede com a rede.

<dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

**Desconectado** (0)


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

**Conectando** (1)


</dt> <dd></dd> <dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

**Conectado** (2)


</dt> <dd></dd> <dt>

<span id="Disconnecting"></span><span id="disconnecting"></span><span id="DISCONNECTING"></span>

**Desconexão** (3)


</dt> <dd></dd> <dt>

<span id="Hardware_Not_Present"></span><span id="hardware_not_present"></span><span id="HARDWARE_NOT_PRESENT"></span>

**Hardware não presente** (4)


</dt> <dd></dd> <dt>

<span id="Hardware_Disabled"></span><span id="hardware_disabled"></span><span id="HARDWARE_DISABLED"></span>

**Hardware desabilitado** (5)


</dt> <dd></dd> <dt>

<span id="Hardware_Malfunction"></span><span id="hardware_malfunction"></span><span id="HARDWARE_MALFUNCTION"></span>

**Problema de hardware** (6)


</dt> <dd></dd> <dt>

<span id="Media_Disconnected"></span><span id="media_disconnected"></span><span id="MEDIA_DISCONNECTED"></span>

**Mídia desconectada** (7)


</dt> <dd></dd> <dt>

<span id="Authenticating"></span><span id="authenticating"></span><span id="AUTHENTICATING"></span>

**Autenticação** (8)


</dt> <dd></dd> <dt>

<span id="Authentication_Succeeded"></span><span id="authentication_succeeded"></span><span id="AUTHENTICATION_SUCCEEDED"></span>

**Autenticação bem-sucedida** (9)


</dt> <dd></dd> <dt>

<span id="Authentication_Failed"></span><span id="authentication_failed"></span><span id="AUTHENTICATION_FAILED"></span>

**Falha na autenticação** (10)


</dt> <dd></dd> <dt>

<span id="Invalid_Address"></span><span id="invalid_address"></span><span id="INVALID_ADDRESS"></span>

**Endereço inválido** (11)


</dt> <dd></dd> <dt>

<span id="Credentials_Required"></span><span id="credentials_required"></span><span id="CREDENTIALS_REQUIRED"></span>

**Credenciais necessárias** (12)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outras**


</dt> <dd>13–65535</dd> </dl>

</dd> <dt>

**NetEnabled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o adaptador está habilitado ou não. Se **True**, o adaptador será habilitado. Você pode habilitar ou desabilitar a NIC usando os [**métodos Habilitar**](enable-method-in-class-win32-networkadapter.md) [**e Desabilitar.**](disable-method-in-class-win32-networkadapter.md)

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Adaptador de Rede DMTF \| 802 Porta \| 001.3")
</dt> </dl>

Matriz de endereços de rede para um adaptador.

Essa propriedade é herdada de [**CIM \_ NetworkAdapter.**](cim-networkadapter.md)

Essa propriedade ainda não foi implementada. Ele retorna um **valor NULL** por padrão.

</dd> <dt>

**PermanentAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Adaptador de Rede DMTF \| 802 Porta \| 001.2")
</dt> </dl>

Endereço de rede codificado em um adaptador. Esse endereço em código pode ser alterado pela atualização de firmware ou pela configuração de software. Nesse caso, esse campo deverá ser atualizado quando a alteração for feita. A propriedade deverá ser deixada em branco se não houver nenhum endereço codificado para o adaptador de rede.

Essa propriedade é herdada de [**CIM \_ NetworkAdapter.**](cim-networkadapter.md)

Essa propriedade ainda não foi implementada. Ele retorna um **valor NULL** por padrão.

</dd> <dt>

**PhysicalAdapter**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o adaptador é um adaptador físico ou lógico. Se **True**, o adaptador será físico.

</dd> <dt>

**PNPDeviceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")
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

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

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

Há suporte para o método [**SetPowerState.**](setpowerstate-method-in-class-cim-controller.md) Esse método é encontrado na classe [**\_ LogicalDevice cim**](cim-logicaldevice.md) pai e pode ser implementado. Para obter mais informações, consulte [Designando classes Managed Object Format (MOF).](../wmisdk/designing-managed-object-format--mof--classes.md)

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

**ProductName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")
</dt> </dl>

Nome do produto do adaptador de rede.

Exemplo: "Fast EtherLink XL"

</dd> <dt>

**ServiceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ NetworkCards \| ProductName")
</dt> </dl>

Nome do serviço do adaptador de rede. Esse nome geralmente é menor que o nome completo do produto.

Exemplo: "Elnkii"

</dd> <dt>

**Velocidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| RFC1213-MIB.ifSpeed", "MIF. Adaptador de Rede DMTF \| 802 Porta \| 001.5"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")
</dt> </dl>

Estimativa da largura de banda atual em bits por segundo. Para pontos de extremidade que variam em largura de banda ou para aqueles em que nenhuma estimativa precisa pode ser feita, essa propriedade deve conter a largura de banda nominal.

Essa propriedade é herdada de [**CIM \_ NetworkAdapter.**](cim-networkadapter.md)

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](/previous-versions//aa393262(v=vs.85)).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")
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

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. Estado Operacional DMTF \| \| 003.3")
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

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**Sistema CIM \_**](cim-system.md).**CreationClassName**"), [**chave CIM \_**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Valor da propriedade **CreationClassName** do computador de definição de tela.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("[**Sistema CIM \_**](cim-system.md).**Nome**"), [**Chave CIM \_**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Nome do sistema de scoping.

Essa propriedade é herdada de [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

</dd> <dt>

**TimeOfLastReset**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SOFTWARE \\ \\ Microsoft Windows NT \\ \\ \\ \\ CurrentVersion \\ \\ Perflib \\ \\ 009 \| System Up Time")
</dt> </dl>

Data e hora em que o adaptador de rede foi redefinido pela última vez.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ NetworkAdapter Win32** é derivada de [**CIM \_ NetworkAdapter.**](cim-networkadapter.md)

A lista a seguir descreve as classes associator para **Win32 \_ NetworkAdapter**:

-   [**Win32 \_ PnPEntity**](win32-pnpentity.md)
-   [**Win32 \_ ComputerSystem**](win32-computersystem.md)
-   [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)
-   [**Win32 \_ IRQResource**](win32-irqresource.md)
-   [**Win32 \_ DeviceMemoryAddress**](win32-devicememoryaddress.md)
-   [**Win32 \_ PortResource**](win32-portresource.md)
-   [**Win32 \_ NetworkProtocol**](win32-networkprotocol.md)
-   [**Win32 \_ SystemDriver**](win32-systemdriver.md)

Muitos sistemas têm vários adaptadores de rede neles. Considere usar o seguinte como uma referência para encontrar os adaptadores atuais:

``` syntax
AdapterType: "Ethernet 802.3"
MACAddress: String Length > 16
Availability: 3
PNPDeviceID: InStr ( PNPDeviceID, "PCI") = 1
Installed: vbTrue
ConfigManagerErrorCode: 0
: <keep this as an index to Win32_NetworkAdapterConfiguration>
```

Mesmo usando os qualificadores acima, você provavelmente recuperará mais de um adaptador de rede válido. Se esse for o caso, você poderá usar as seguintes informações para qualificar ainda mais sua pesquisa de \_ NetworkAdapterConfiguration do Win32:

``` syntax
Index: <match to DeviceID above>
MACAddress: Length > 16
DefaultIPGateway: String Length > 6
DNSServerSearchOrder: Array of strings with length > 6
IPEnabled: vbTrue
IPAddress: Array of strings with length > 6
```

Depois de fazer isso, você provavelmente terá reduzido sua lista para um ou dois adaptadores configurados.

Você também pode usar o procedimento a seguir para encontrar o adaptador padrão:

1.  Execute a seguinte consulta:

    `"SELECT InterfaceIndex, Destination FROM Win32_IP4RouteTable WHERE Destination='0.0.0.0'"`

    Você deve ter apenas um destino de rede padrão 0.0.0.0.

2.  Use **InterfaceIndex para** recuperar o Adaptador de Rede que você deseja.

    `"SELECT * FROM Win32_NetworkAdapter WHERE InterfaceIndex=" + insertVariableHere`

## <a name="examples"></a>Exemplos

O exemplo de código do PowerShell two [WMI Functions](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) na Galeria do TechNet usa **Win32 \_ NetworkAdapter** para criar o cmdlet [Windows Get-NetAdapter.](/powershell/module/netadapter/get-netadapter?view=win10-ps)

O exemplo [do PowerShell Get-ComputerInfo – Query Computer From Local/Remote Computers – (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) na Galeria do TechNet usa várias chamadas para hardware e software, incluindo **Win32 \_ NetworkAdapter,** para exibir informações sobre um sistema local ou remoto.

O exemplo de código C \# a seguir usa o namespace [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) para recuperar os adaptadores de rede atuais no computador local.


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapter");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
                Console.WriteLine();
            }

            Console.ReadLine();
        }
```



O exemplo de código C \# a seguir usa o https://msdn.microsoft.com/library/system.management.aspx namespace para recuperar os adaptadores de rede atuais no computador local.

> [!Note]  
> https://msdn.microsoft.com/library/system.management.aspxcontém as classes originais usadas para acessar o WMI; no entanto, eles são considerados mais lentos e geralmente não são dimensionamentos, bem como seus equivalentes [Microsoft.Management.Infrastructure.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapter");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("MACAddress : {0}", m["Description"]);
                Console.WriteLine();
            }
            Console.ReadLine();

        }
```



O exemplo de código VBScript a seguir descreve como recuperar os adaptadores de rede atuais no computador local.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapter")

For Each objItem in colItems 
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo
Next
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

[**CIM \_ NetworkAdapter**](cim-networkadapter.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> <dt>

[Tarefas WMI: Rede](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[Suporte a IPv6 e IPv4 no WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
