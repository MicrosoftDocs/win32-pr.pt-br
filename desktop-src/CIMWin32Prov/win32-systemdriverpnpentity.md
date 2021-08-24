---
description: a \_ classe WMI de associação SystemDriverPNPEntity do Win32 relaciona um dispositivo Plug and Play no sistema de computador que executa o Windows e o driver que dá suporte ao dispositivo Plug and Play.
ms.assetid: 2696c8e5-3bc3-42e3-807b-a387607c7c09
ms.tgt_platform: multiple
title: Classe Win32_SystemDriverPNPEntity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriverPNPEntity
- Win32_SystemDriverPNPEntity.Antecedent
- Win32_SystemDriverPNPEntity.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4b0de9559d223db4c398387ca846be39b17566b3267c76399bdf4381cdd14e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751106"
---
# <a name="win32_systemdriverpnpentity-class"></a>\_Classe Win32 SystemDriverPNPEntity

a [classe WMI](../wmisdk/retrieving-a-class.md) de associação **\_ SystemDriverPNPEntity do Win32** relaciona um dispositivo Plug and Play no sistema de computador que executa o Windows e o driver que dá suporte ao dispositivo Plug and Play.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0800F074-CB98-11d2-B35D-00104BC97924}"), AMENDMENT]
class Win32_SystemDriverPNPEntity : CIM_Dependency
{
  Win32_PNPEntity    REF Antecedent;
  Win32_SystemDriver REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ SystemDriverPNPEntity** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ SystemDriverPNPEntity** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ PNPEntity**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PNPEntity")
</dt> </dl>

Representa o dispositivo Plug and Play controlado pelo driver.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ systemdrive do Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("dependente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")
</dt> </dl>

Um [**\_ SystemDriver Win32**](win32-systemdriver.md) que representa o driver que dá suporte ao dispositivo de plug and Play.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ SystemDriverPNPEntity** é derivada da [**\_ dependência CIM**](cim-dependency.md).

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

[**\_Dependência CIM**](cim-dependency.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
