---
description: A classe WMI de associação MemoryArrayLocation do Win32 relaciona uma matriz de memória lógica e a matriz de memória física na \_ qual ela existe.
ms.assetid: 455daeee-ad67-4599-84d6-fa3f4ac593aa
ms.tgt_platform: multiple
title: Win32_MemoryArrayLocation classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArrayLocation
- Win32_MemoryArrayLocation.Dependent
- Win32_MemoryArrayLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a0fd01751794dc9177f3840804f0412db70531f6706a452793fe6cbcf3aa2389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079790"
---
# <a name="win32_memoryarraylocation-class"></a>Classe Win32 \_ MemoryArrayLocation

A classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ MemoryArrayLocation do Win32** relaciona uma matriz de memória lógica e a matriz de memória física na qual ela existe.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF561-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryArrayLocation : CIM_Realizes
{
  Win32_MemoryArray         REF Dependent;
  Win32_PhysicalMemoryArray REF Antecedent;
};
```

## <a name="members"></a>Membros

A **classe \_ MemoryArrayLocation do Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ MemoryArrayLocation do Win32** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ PhysicalMemoryArray**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ PhysicalMemoryArray")
</dt> </dl>

Um [**Win32 \_ PhysicalMemoryArray**](win32-physicalmemoryarray.md) que descreve a matriz de memória física que implementa a matriz de memória lógica.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ MemoryArray**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryArray")
</dt> </dl>

Uma [**\_ MemoryArray do Win32**](win32-memoryarray.md) que descreve a matriz de memória lógica implementada pela matriz de memória física.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ MemoryArrayLocation win32** é derivada de [**CIM \_ Realizes**](cim-realizes.md).

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

[**Cim \_ Realiza**](cim-realizes.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

