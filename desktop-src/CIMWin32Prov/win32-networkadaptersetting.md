---
description: A \_ classe WMI de associação NetworkAdapterSetting do Win32 relaciona um adaptador de rede e suas definições de configuração.
ms.assetid: 6fc646c3-05f9-4c92-8598-07ea20fffaca
ms.tgt_platform: multiple
title: Classe Win32_NetworkAdapterSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterSetting
- Win32_NetworkAdapterSetting.Setting
- Win32_NetworkAdapterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c51ef9ed790c902a6a662dc3ebc45df97fa29721
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755431"
---
# <a name="win32_networkadaptersetting-class"></a>\_Classe Win32 NetworkAdapterSetting

A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ NetworkAdapterSetting do Win32** relaciona um adaptador de rede e suas definições de configuração.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterSetting : Win32_DeviceSettings
{
  Win32_NetworkAdapterConfiguration REF Setting;
  Win32_NetworkAdapter              REF Element;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ NetworkAdapterSetting** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ NetworkAdapterSetting** tem essas propriedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ adaptador**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ adaptador")
</dt> </dl>

Um [**\_ adaptador Win32**](win32-networkadapter.md) que descreve as propriedades do adaptador de rede que está usando uma configuração de adaptador de rede específica.

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ NetworkAdapterConfiguration**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration")
</dt> </dl>

Um [**\_ NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md) que descreve as definições de configuração usadas no adaptador de rede.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ NetworkAdapterSetting** é derivada de [**Win32 \_ DeviceSettings**](win32-devicesettings.md).

Para obter informações sobre como usar classes de associação, consulte [associars of Statement](../wmisdk/associators-of-statement.md).

## <a name="examples"></a>Exemplos

O exemplo de VBScript a seguir usa o **Win32 \_ NetworkAdapterSetting** para identificar o endereço IP na conexão de área local.


```VB
strComputer = "."
Set objWMIService = GetObject( _
    "winmgmts:\\" & strComputer & "\root\cimv2")
Set colNics = objWMIService.ExecQuery _
    ("Select * From Win32_NetworkAdapter " _
        & "Where NetConnectionID = " & _
        "'Local Area Connection'")
 
For Each objNic in colNics
    Set colNicConfigs = objWMIService.ExecQuery _
      ("ASSOCIATORS OF " _
          & "{Win32_NetworkAdapter.DeviceID='" & _
      objNic.DeviceID & "'}" & _
      " WHERE AssocClass=Win32_NetworkAdapterSetting")
    For Each objNicConfig In colNicConfigs
        For Each strIPAddress in objNicConfig.IPAddress
            Wscript.Echo "IP Address: " &  strIPAddress
        Next
    Next
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

[**\_DeviceSettings Win32**](win32-devicesettings.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> <dt>

[Tarefas do WMI: rede](../wmisdk/wmi-tasks--networking.md)
</dt> </dl>

 

 
