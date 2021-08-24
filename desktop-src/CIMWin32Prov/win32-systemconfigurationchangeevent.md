---
description: O Win32 \_ SystemConfigurationChangeEvent&\# 8194; A classe WMI indica que a lista de dispositivos no sistema foi atualizada (um dispositivo foi adicionado ou removido ou a configuração foi alterada).
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.tgt_platform: multiple
title: Win32_SystemConfigurationChangeEvent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 63a0708f2e081ffc8c5fb359be1e57aacd1cd62bd1db1daee2063e66e2fb55c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751296"
---
# <a name="win32_systemconfigurationchangeevent-class"></a>Classe Win32 \_ SystemConfigurationChangeEvent

A classe  [WMI](../wmisdk/retrieving-a-class.md) **Win32 \_ SystemConfigurationChangeEvent** indica que a lista de dispositivos no sistema foi atualizada (um dispositivo foi adicionado ou removido ou a configuração foi alterada). Um evento é acionado e uma instância desse é criada quando a mensagem "DevMgrRefreshOn<*ComputerName>"* é enviada. A alteração exata na lista de dispositivos não está contida na mensagem, portanto, uma atualização do dispositivo é necessária para obter as configurações atuais do sistema. Exemplos de alterações de configuração afetadas são configurações de IRQ, portas COM e versões do BIOS.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ SystemConfigurationChangeEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ SystemConfigurationChangeEvent** tem essas propriedades.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32APIDevice Management Messages \| WM \_ DEVICECHANGE \| wParam", "Win32APIDevice Management Messages \| WM \_ SETTINGCHANGE")
</dt> </dl>

Tipo de notificação de alteração de evento que ocorreu.

Essa propriedade é herdada de [**Win32 \_ DeviceChangeEvent.**](win32-devicechangeevent.md)

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

**Configuração alterada** (1)


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

**Chegada do** dispositivo (2)


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

**Remoção do** dispositivo (3)


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

**Encaixe** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**DESCRITOR \_ DE SEGURANÇA**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descritor usado pelo provedor de eventos para determinar quais usuários podem receber o evento. Essa propriedade é herdada do [**\_ \_ Evento**](../wmisdk/--event.md). Para obter mais informações sobre constantes usadas para definir esse descritor de segurança, consulte [Constantes de segurança WMI](../wmisdk/wmi-security-constants.md).

</dd> <dt>

**TEMPO \_ CRIADO**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor exclusivo que indica a hora em que o evento foi gerado. Esse é um valor de 64 bits que representa o número de intervalos de 100 nanossegundos após 1º de janeiro de 1601. As informações estão no formato UTC (Tempos Universais Coordenados).

Essa propriedade é herdada do [**\_ \_ Evento**](../wmisdk/--event.md).

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe Win32 \_ SystemConfigurationChangeEvent** é derivada de [**Win32 \_ DeviceChangeEvent.**](win32-devicechangeevent.md)

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

[**Win32 \_ DeviceChangeEvent**](win32-devicechangeevent.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> </dl>

 

 
