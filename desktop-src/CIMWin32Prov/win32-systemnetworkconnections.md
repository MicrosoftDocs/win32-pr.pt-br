---
description: A \_ classe WMI de associação do Win32 SystemNetworkConnections relaciona uma conexão de rede e o sistema de computador no qual ele reside.
ms.assetid: 7c47f653-74a9-4729-a72c-94930181f8c9
ms.tgt_platform: multiple
title: Classe Win32_SystemNetworkConnections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemNetworkConnections
- Win32_SystemNetworkConnections.GroupComponent
- Win32_SystemNetworkConnections.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e90562dd4f98a00cf848fb83a9e3051b387241e4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089602"
---
# <a name="win32_systemnetworkconnections-class"></a>\_Classe Win32 SystemNetworkConnections

A [classe WMI](../wmisdk/retrieving-a-class.md) de associação do **Win32 \_ SystemNetworkConnections** relaciona uma conexão de rede e o sistema de computador no qual ele reside.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F7-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemNetworkConnections : CIM_SystemComponent
{
  Win32_ComputerSystem    REF GroupComponent;
  Win32_NetworkConnection REF PartComponent;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ SystemNetworkConnections** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ SystemNetworkConnections** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ sistema de ComputerSystem Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Referência à instância que representa o sistema de computador conectado à rede.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ NetworkConnection**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkConnection")
</dt> </dl>

Referência à instância que representa a conexão de rede com este sistema de computador.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ SystemNetworkConnections** é derivada de [**CIM \_ Systemcomponent**](cim-systemcomponent.md).

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

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> </dl>

 

 
