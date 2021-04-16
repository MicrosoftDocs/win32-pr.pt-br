---
description: A \_ classe WMI de associação PnPDevice do Win32 relaciona um dispositivo (conhecido por Configuration Manager como um PNPEntity) e a função que ele executa.
ms.assetid: 5163a423-60f2-416d-bf82-89517b499f93
ms.tgt_platform: multiple
title: Classe Win32_PnPDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPDevice
- Win32_PnPDevice.SameElement
- Win32_PnPDevice.SystemElement
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c17dc6d4169854469d630e2a622eacc85e8a587c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753798"
---
# <a name="win32_pnpdevice-class"></a>\_Classe Win32 PnPDevice

A [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ PnPDevice do Win32** relaciona um dispositivo (conhecido por Configuration Manager como um PNPEntity) e a função que ele executa. Sua função é representada por uma subclasse do dispositivo lógico que descreve seu uso. Por exemplo, uma instância do Win32 [**\_ Keyboard**](win32-keyboard.md) ou [**Win32 \_ DiskDrive**](win32-diskdrive.md) . Ambos os objetos referenciados representam o mesmo dispositivo de sistema subjacente; as alterações na alocação de recursos no lado do PNPEntity afetarão o dispositivo associado.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("CIMWin32"), UUID("{FE28FD96-C875-11d2-B352-00104BC97924}"), AMENDMENT]
class Win32_PnPDevice
{
  CIM_LogicalDevice REF SameElement;
  Win32_PnPEntity   REF SystemElement;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ PnPDevice** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ PnPDevice** tem essas propriedades.

<dl> <dt>

**Mesmoelement**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ LogicalDevice CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ LogicalDevice")
</dt> </dl>

Referência à instância [**CIM \_ LogicalDevice**](cim-logicaldevice.md) que representa as propriedades de dispositivo lógico associadas ao dispositivo Plug and Play.

</dd> <dt>

**Sistema de**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ PnPEntity**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PnPEntity")
</dt> </dl>

Referência à instância do [**Win32 \_ PnPEntity**](win32-pnpentity.md) que representa o dispositivo Plug and Play associado ao dispositivo lógico.

</dd> </dl>

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

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
