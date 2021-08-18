---
description: A classe WMI de associação LogicalProgramGroupItemDataFile do Win32 relaciona os itens do grupo de programas do menu Iniciar e os arquivos nos quais \_ eles estão armazenados.
ms.assetid: 9327c205-d0ad-4f2b-a65e-2a648e7c13e0
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupItemDataFile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItemDataFile
- Win32_LogicalProgramGroupItemDataFile.Antecedent
- Win32_LogicalProgramGroupItemDataFile.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6f69c23ae545de837e9d6578ba2f64eed51ecbc6f10780e40c809cb2e362b33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973043"
---
# <a name="win32_logicalprogramgroupitemdatafile-class"></a>Classe \_ LogicalProgramGroupItemDataFile do Win32

A classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação **\_ LogicalProgramGroupItemDataFile do Win32** relaciona os itens do grupo de programas do **menu** Iniciar e os arquivos nos quais eles estão armazenados.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{08FFAD62-8050-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItemDataFile : CIM_Dependency
{
  Win32_LogicalProgramGroupItem REF Antecedent;
  CIM_DataFile                  REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe \_ LogicalProgramGroupItemDataFile do Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ LogicalProgramGroupItemDataFile do Win32** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ LogicalProgramGroupItem**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalProgramGroupItem")
</dt> </dl>

Referência à instância que representa os grupos de programas **no** menu Iniciar.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ DataFile**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ DataFile")
</dt> </dl>

Referência à instância que representa a classe associada ao grupo de programas.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ LogicalProgramGroupItemDataFile do Win32** é derivada da [**\_ Dependência CIM.**](cim-dependency.md)

O processo de chamada que usa essa classe deve ter ES **\_ privilégio RESTORE \_ NAME** no computador no qual o Registro reside. Por exemplo, se você enumerar essa classe no computador local, a conta na qual o aplicativo é executado deverá ter esse privilégio. Para obter mais informações, consulte [Executando operações privilegiadas.](/windows/desktop/WmiSdk/executing-privileged-operations)

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

[**Dependência cim \_**](cim-dependency.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

