---
description: A \_ classe WMI de associação do Win32 SerialPortSetting relaciona uma porta serial e suas definições de configuração.
ms.assetid: 57856207-abe5-4d93-9a34-acfe30ccd80c
ms.tgt_platform: multiple
title: Classe Win32_SerialPortSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortSetting
- Win32_SerialPortSetting.Setting
- Win32_SerialPortSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 713cdb57b5ed7135529959d3c17f7453924ce1dc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920180"
---
# <a name="win32_serialportsetting-class"></a>\_Classe Win32 SerialPortSetting

A [classe WMI](../wmisdk/retrieving-a-class.md) de associação do **Win32 \_ SerialPortSetting** relaciona uma porta serial e suas definições de configuração.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortSetting : Win32_DeviceSettings
{
  Win32_SerialPortConfiguration REF Setting;
  Win32_SerialPort              REF Element;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ SerialPortSetting** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ SerialPortSetting** tem essas propriedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ SerialPort do Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")
</dt> </dl>

Uma [**\_ SerialPort do Win32**](win32-serialport.md) que contém as propriedades de uma porta serial no sistema de computador.

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ SerialPortConfiguration**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPortConfiguration")
</dt> </dl>

Um [**\_ SerialPortConfiguration Win32**](win32-serialportconfiguration.md) que contém a definição de configuração para a porta serial.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ SerialPortSetting** é derivada de [**Win32 \_ DeviceSettings**](win32-devicesettings.md).

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

[**\_DeviceSettings Win32**](win32-devicesettings.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
