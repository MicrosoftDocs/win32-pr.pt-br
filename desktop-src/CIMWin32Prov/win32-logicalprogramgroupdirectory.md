---
description: A \_ classe WMI de associação do Win32 LogicalProgramGroupDirectory relaciona grupos de programas lógicos (agrupamentos no menu Iniciar) e os diretórios de arquivos nos quais eles são armazenados.
ms.assetid: 31a8b56a-d4fd-4cc5-9997-ec6211fe9425
ms.tgt_platform: multiple
title: Classe Win32_LogicalProgramGroupDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupDirectory
- Win32_LogicalProgramGroupDirectory.Antecedent
- Win32_LogicalProgramGroupDirectory.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6ebaddd4455ba1b62832f940d78534c90cefeeb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754387"
---
# <a name="win32_logicalprogramgroupdirectory-class"></a>\_Classe Win32 LogicalProgramGroupDirectory

A [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) de associação do **Win32 \_ LogicalProgramGroupDirectory** relaciona grupos de programas lógicos (agrupamentos no menu **Iniciar** ) e os diretórios de arquivos nos quais eles são armazenados.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{F25FE467-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupDirectory : CIM_Dependency
{
  Win32_LogicalProgramGroup REF Antecedent;
  Win32_Directory           REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ LogicalProgramGroupDirectory** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ LogicalProgramGroupDirectory** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ LogicalProgramGroup**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalProgramGroup")
</dt> </dl>

Referência à instância que representa o grupo de programas lógicos.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ diretório Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| diretório WMI Win32 \_ ")
</dt> </dl>

Referência à instância que representa o diretório de arquivos para o grupo de programas lógicos.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ LogicalProgramGroupDirectory** é derivada da [**\_ dependência CIM**](cim-dependency.md).

O processo de chamada que usa essa classe deve ter o privilégio **se \_ Restore \_ Name** no computador em que o registro reside. Por exemplo, se você enumerar essa classe no computador local, a conta sob a qual seu aplicativo é executado deverá ter esse privilégio. Para obter mais informações, consulte [executando operações privilegiadas](/windows/desktop/WmiSdk/executing-privileged-operations).

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

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

