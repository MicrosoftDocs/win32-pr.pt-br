---
description: A classe WMI de associação Win32 USBControllerDevice relaciona um controlador USB (barramento serial universal) e \_ a instância logicalDevice cim conectada a \_ ele.
ms.assetid: a0c64984-9116-4cb8-86e0-38c897cb7119
ms.tgt_platform: multiple
title: Win32_USBControllerDevice classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_USBControllerDevice
- Win32_USBControllerDevice.NegotiatedDataWidth
- Win32_USBControllerDevice.NegotiatedSpeed
- Win32_USBControllerDevice.AccessState
- Win32_USBControllerDevice.NumberOfHardResets
- Win32_USBControllerDevice.NumberOfSoftResets
- Win32_USBControllerDevice.Antecedent
- Win32_USBControllerDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3a7627426a094d8c335032363b3213aeca19e400d5761d23ede8b7cecf0dcab5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118007256"
---
# <a name="win32_usbcontrollerdevice-class"></a>Classe Win32 \_ USBControllerDevice

A classe [WMI](../wmisdk/retrieving-a-class.md) de associação **Win32 \_ USBControllerDevice** relaciona um controlador USB (barramento serial universal) e a [**instância \_ logicalDevice cim**](cim-logicaldevice.md) conectada a ele.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{DE57D792-A032-11D2-90F0-0060081A46FD}"), AMENDMENT]
class Win32_USBControllerDevice : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBController REF Antecedent;
  CIM_LogicalDevice REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ USBControllerDevice** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ USBControllerDevice** tem essas propriedades.

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o controlador está ativamente no comando ou acessando o dispositivo. Essas informações são necessárias quando um dispositivo lógico pode ser comandos por vários controladores ou acessados por meio de vários controladores.

Essa propriedade é herdada de [**CIM \_ ControlledBy.**](cim-controlledby.md)

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

**Ativo** (1)


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

**Inativo** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ USBController**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ USBController")
</dt> </dl>

Um [**\_ USBController CIM**](cim-usbcontroller.md) que representa o controlador USB (Barramento Serial Universal) associado a este dispositivo.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ LogicalDevice**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Um [**\_ LogicalDevice CIM que**](cim-logicaldevice.md) descreve o dispositivo lógico conectado ao controlador USB (Barramento Serial Universal).

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Unidades**](../wmisdk/standard-qualifiers.md) ("bits")
</dt> </dl>

Quando várias larguras de dados de conexão ou barramento são possíveis, essa propriedade define aquela em uso entre os dispositivos. A largura dos dados é especificada em bits. Se a largura dos dados não for negociada ou se essas informações não estão disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deve ser definida como 0 (zero).

Essa propriedade é herdada de [**\_ DEVICEConnection cim**](cim-deviceconnection.md).

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")
</dt> </dl>

Quando várias velocidades de conexão ou barramento são possíveis, essa propriedade define aquela que está sendo usada entre os dispositivos. A velocidade é especificada em bits por segundo. Se as velocidades de conexão ou barramento não são negociadas ou se essas informações não estão disponíveis ou importantes para o gerenciamento de dispositivos, a propriedade deve ser definida como 0 (zero).

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](../wmisdk/creating-a-wmi-script.md).

Essa propriedade é herdada de [**\_ DEVICEConnection cim**](cim-deviceconnection.md).

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de redefinições de disco rígido emitidas pelo controlador. Uma redefinição de disco rígido retorna o dispositivo para seu estado de inicialização ou inicialização. Todas as informações de estado do dispositivo interno e os dados são perdidos.

Essa propriedade é herdada de [**CIM \_ ControlledBy.**](cim-controlledby.md)

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de redefinições suaves emitidas pelo controlador. Uma redefinição suave não limpa completamente o estado e os dados atuais do dispositivo. A semântica exata depende do dispositivo e dos protocolos e mecanismos usados para se comunicar com ele.

Essa propriedade é herdada de [**CIM \_ ControlledBy.**](cim-controlledby.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe Win32 \_ USBControllerDevice** é derivada de [**CIM \_ ControlledBy.**](cim-controlledby.md)

Para uma discussão sobre como usar, consulte o artigo no blog [Exibindo dispositivos USB usando wmi.](https://devblogs.microsoft.com/powershell/displaying-usb-devices-using-wmi/) Para obter uma discussão sobre como usar classes de associação, consulte o [artigo Get-USB – Using WMI Association Classes in PowerShell](https://devblogs.microsoft.com/powershell/get-usb-using-wmi-association-classes-in-powershell/) ( Usando classes de associação WMI no PowerShell).

## <a name="examples"></a>Exemplos

O exemplo do PowerShell a seguir recupera o dispositivo lógico dependente e exibe as informações relevantes.


```PowerShell
gwmi Win32_USBControllerDevice |%{[wmi]($_.Dependent)} | Sort Manufacturer,Description,DeviceID | Ft -GroupBy Manufacturer Description,Service,DeviceID
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

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
