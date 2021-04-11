---
description: O \_ abstrato DeviceSettings do Win32, a classe WMI de associação relaciona um dispositivo lógico e uma configuração que pode ser aplicada a ele.
ms.assetid: 4f6c4c26-8da9-4e2c-8b8c-cec658ac08d4
ms.tgt_platform: multiple
title: Classe Win32_DeviceSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceSettings
- Win32_DeviceSettings.Setting
- Win32_DeviceSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1cd9cae29cfa608c9f3c0c36ebfe3ca7f903c809
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164124"
---
# <a name="win32_devicesettings-class"></a>\_Classe Win32 DeviceSettings

O **abstrato \_ DeviceSettings do Win32** , a [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação relaciona um dispositivo lógico e uma configuração que pode ser aplicada a ele.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{8502C4FD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceSettings : CIM_ElementSetting
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ DeviceSettings** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ DeviceSettings** tem essas propriedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ LogicalDevice CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("element"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que representa as propriedades do dispositivo lógico no qual as configurações podem ser aplicadas.

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ configuração de CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuração"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("configuração CIM CIM \| \_ ")
</dt> </dl>

Uma [**\_ configuração de CIM**](cim-setting.md) que representa as configurações que podem ser aplicadas ao dispositivo lógico.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ DeviceSettings** é derivada de [**CIM \_ ElementSetting**](cim-elementsetting.md).

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

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

