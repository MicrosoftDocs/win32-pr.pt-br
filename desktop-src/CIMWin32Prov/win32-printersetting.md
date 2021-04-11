---
description: A \_ classe WMI de associação PrinterSetting do Win32 relaciona uma impressora e suas definições de configuração.
ms.assetid: 5d0f0724-0583-449b-a6da-336e7c8e526e
ms.tgt_platform: multiple
title: Classe Win32_PrinterSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterSetting
- Win32_PrinterSetting.Setting
- Win32_PrinterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 90a77678e61b755550ebb1818c34ccdc3159a88c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164037"
---
# <a name="win32_printersetting-class"></a>\_Classe Win32 PrinterSetting

A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ PrinterSetting do Win32** relaciona uma impressora e suas definições de configuração.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class Win32_PrinterSetting : Win32_DeviceSettings
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ PrinterSetting** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ PrinterSetting** tem essas propriedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ LogicalDevice CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que representa as propriedades do dispositivo lógico no qual as configurações podem ser aplicadas.

Esta propriedade é herdada do [**Win32 \_ DeviceSettings**](win32-devicesettings.md).

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ configuração de CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("configuração CIM CIM \| \_ ")
</dt> </dl>

Uma [**\_ configuração de CIM**](cim-setting.md) que representa as configurações que podem ser aplicadas ao dispositivo lógico.

Esta propriedade é herdada do [**Win32 \_ DeviceSettings**](win32-devicesettings.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ PrinterSetting** é derivada de [**Win32 \_ DeviceSettings**](win32-devicesettings.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>\_Impressora. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_DeviceSettings Win32**](win32-devicesettings.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
