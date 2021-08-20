---
description: A classe WMI de associação \_ Win32 DriverForDevice relaciona uma instância de impressora a uma instância de driver de impressora.
ms.assetid: 56ff74b2-31ba-4d8e-b389-9f962932aa03
ms.tgt_platform: multiple
title: Win32_DriverForDevice classe
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
ms.openlocfilehash: f55025c84b8ab7e7114f5a1746d84f8fbdb6b0a7dfe952abfe84efb980430881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546316"
---
# <a name="win32_driverfordevice-class"></a>Classe Win32 \_ DriverForDevice

A classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **de associação Win32 \_ DriverForDevice** relaciona uma instância de impressora a uma instância de driver de impressora.

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

A **classe Win32 \_ DriverForDevice** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ DriverForDevice** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Impressora Win32 \_**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Referência à instância [**da Impressora \_ Win32**](win32-printer.md) que representa a impressora.

Essa propriedade é herdada da [**\_ Dependência CIM.**](cim-dependency.md)

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Impressora Win32Driver \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência à instância [**do \_ PrinterDriver win32**](win32-printerdriver.md) que representa o driver de impressora para a impressora.

Essa propriedade é herdada da [**\_ Dependência CIM.**](cim-dependency.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe Win32 \_ DriverForDevice** é derivada da [**\_ Dependência CIM.**](cim-dependency.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

