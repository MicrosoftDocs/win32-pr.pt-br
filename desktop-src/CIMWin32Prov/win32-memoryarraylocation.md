---
description: A \_ classe WMI de associação do Win32 MemoryArrayLocation relaciona uma matriz de memória lógica e a matriz de memória física na qual ela existe.
ms.assetid: 455daeee-ad67-4599-84d6-fa3f4ac593aa
ms.tgt_platform: multiple
title: Classe Win32_MemoryArrayLocation
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
ms.openlocfilehash: 62aae3bf672b12bdb947ff8ce6b76f919eaa11b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501063"
---
# <a name="win32_memoryarraylocation-class"></a>\_Classe Win32 MemoryArrayLocation

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação do **Win32 \_ MemoryArrayLocation** relaciona uma matriz de memória lógica e a matriz de memória física na qual ela existe.

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

A classe **Win32 \_ MemoryArrayLocation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ MemoryArrayLocation** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ PhysicalMemoryArray**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ PhysicalMemoryArray")
</dt> </dl>

Um [**\_ PhysicalMemoryArray Win32**](win32-physicalmemoryarray.md) que descreve a matriz de memória física que implementa a matriz de memória lógica.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ MemoryArray**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryArray")
</dt> </dl>

Um [**\_ MemoryArray Win32**](win32-memoryarray.md) que descreve a matriz de memória lógica implementada pela matriz de memória física.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ MemoryArrayLocation** é derivada do [**CIM \_**](cim-realizes.md).

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

[**O CIM \_ percebe**](cim-realizes.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

