---
description: A \_ classe Win32 LogonSessionMappedDisk representa uma associação entre uma sessão de logon e os discos lógicos mapeados definidos na sessão.
ms.assetid: 013ae55e-6dd1-42fb-bcba-74d6afa1b905
ms.tgt_platform: multiple
title: Classe Win32_LogonSessionMappedDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSessionMappedDisk
- Win32_LogonSessionMappedDisk.Antecedent
- Win32_LogonSessionMappedDisk.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 203c9dd783dece52fa19905d51ece3bc26584dc6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501104"
---
# <a name="win32_logonsessionmappeddisk-class"></a>\_Classe Win32 LogonSessionMappedDisk

A \_ classe Win32 LogonSessionMappedDisk representa uma associação entre uma sessão de logon e os discos lógicos mapeados definidos na sessão.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_LogonSessionMappedDisk : CIM_Dependency
{
  Win32_LogonSession      REF Antecedent;
  Win32_MappedLogicalDisk REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ LogonSessionMappedDisk** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ LogonSessionMappedDisk** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ LogonSession**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

A propriedade Antecedent faz referência a uma sessão de logon.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ MappedLogicalDisk**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

A Propriedade Dependent faz referência a um disco lógico mapeado definido na sessão referenciada pela propriedade Antecedent.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

