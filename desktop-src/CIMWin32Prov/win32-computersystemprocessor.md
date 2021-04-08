---
description: A \_ classe WMI de associação ComputerSystemProcessor do Win32 relaciona um sistema de computador e um processador em execução nesse sistema.
ms.assetid: e630ebea-19bf-43c7-a8a0-7acfda3a752b
ms.tgt_platform: multiple
title: Classe Win32_ComputerSystemProcessor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProcessor
- Win32_ComputerSystemProcessor.PartComponent
- Win32_ComputerSystemProcessor.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2f836d8f5e9053029763c38d2c4f2116987b08fe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089028"
---
# <a name="win32_computersystemprocessor-class"></a>\_Classe Win32 ComputerSystemProcessor

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ ComputerSystemProcessor do Win32** relaciona um sistema de computador e um processador em execução nesse sistema.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{719A6839-C124-11d2-85E8-0000F8102E5F}"), AMENDMENT]
class Win32_ComputerSystemProcessor : Win32_SystemDevices
{
  Win32_Processor      REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ ComputerSystemProcessor** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ ComputerSystemProcessor** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ sistema de ComputerSystem Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Um **\_ sistema** de computadores Win32 que descreve as propriedades do sistema de computador em que o processador está sendo executado.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ processador Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| processador WMI Win32 \_ ")
</dt> </dl>

Um [**\_ processador Win32**](win32-processor.md) que descreve as propriedades de um processador que está executando o sistema de computador.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ ComputerSystemProcessor** é derivada de [**Win32 \_ SystemDevices**](win32-systemdevices.md).

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

[**\_SystemDevices Win32**](win32-systemdevices.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

