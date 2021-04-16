---
description: A \_ classe WMI de associação DriverForDevice do Win32 relaciona uma instância de impressora a uma instância de driver de impressora.
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Classe Win32_DriverForDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DriverForDevice
- Win32_DriverForDevice.Antecedent
- Win32_DriverForDevice.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5fb384eed80c6a614af448477c50be3204d3080
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105750951"
---
# <a name="win32_driverfordevice-class"></a>\_Classe Win32 DriverForDevice

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ DriverForDevice do Win32** relaciona uma instância de impressora a uma instância de driver de impressora.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class Win32_DriverForDevice : CIM_Dependency
{
  Win32_Printer       REF Antecedent;
  Win32_PrinterDriver REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ DriverForDevice** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ DriverForDevice** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ impressora Win32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Referência à instância [**de \_ impressora do Win32**](win32-printer.md) que representa a impressora.

Essa propriedade é herdada [**da \_ dependência CIM**](cim-dependency.md).

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ PrinterDriver**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência à instância do [**Win32 \_ PrinterDriver**](win32-printerdriver.md) que representa o driver de impressora para a impressora.

Essa propriedade é herdada [**da \_ dependência CIM**](cim-dependency.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ DriverForDevice** é derivada da [**\_ dependência CIM**](cim-dependency.md).

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

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

