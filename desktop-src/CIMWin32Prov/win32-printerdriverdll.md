---
description: A classe WMI de associação \_ PrinterDriverDll do Win32 relaciona uma impressora local e seu arquivo de driver.
ms.assetid: decbd1de-8091-47f7-94a1-42862070b920
ms.tgt_platform: multiple
title: Win32_PrinterDriverDll classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterDriverDll
- Win32_PrinterDriverDll.Antecedent
- Win32_PrinterDriverDll.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 884c52e388da62529a2aceb49c68ca888f18e0fd7701e05d951880774c3ed035
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119971856"
---
# <a name="win32_printerdriverdll-class"></a>Classe \_ PrinterDriverDll do Win32

A classe [WMI](../wmisdk/retrieving-a-class.md) de associação **\_ PrinterDriverDll do Win32** relaciona uma impressora local e seu arquivo de driver.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class Win32_PrinterDriverDll : CIM_Dependency
{
  CIM_DataFile  REF Antecedent;
  Win32_Printer REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe \_ PrinterDriverDll do Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ PrinterDriverDll do Win32** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ DataFile**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **Chave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Referência à instância [**do CIM \_ DataFile**](cim-datafile.md) que representa o arquivo de driver para essa Windows baseada em dados.

Essa propriedade é herdada da [**\_ Dependência CIM.**](cim-dependency.md)

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Impressora Win32 \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **Chave**](../wmisdk/standard-qualifiers.md)
</dt> </dl>

Referência à instância [**da Impressora \_ Win32.**](win32-printer.md)

Essa propriedade é herdada da [**\_ Dependência CIM.**](cim-dependency.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ PrinterDriverDll do Win32** é derivada da [**\_ Dependência CIM.**](cim-dependency.md)

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

[**Dependência cim \_**](cim-dependency.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
