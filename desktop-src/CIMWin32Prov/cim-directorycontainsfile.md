---
description: A \_ classe CIM DirectoryContainsFile representa uma associação entre um diretório e os arquivos contidos nesse diretório.
ms.assetid: e05ec86e-c3cf-4589-9815-83850e0c84ed
ms.tgt_platform: multiple
title: Classe CIM_DirectoryContainsFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DirectoryContainsFile
- CIM_DirectoryContainsFile.PartComponent
- CIM_DirectoryContainsFile.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8bd1913352d19a1ed5889413eed5e7fc4640ac53
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826531"
---
# <a name="cim_directorycontainsfile-class"></a>\_Classe CIM DirectoryContainsFile

A classe **CIM \_ DirectoryContainsFile** representa uma associação entre um diretório e os arquivos contidos nesse diretório.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{6F9D4740-8324-11d2-AAD9-006008C78BC7}"), AMENDMENT]
class CIM_DirectoryContainsFile : CIM_Component
{
  CIM_DataFile  REF PartComponent;
  CIM_Directory REF GroupComponent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ DirectoryContainsFile** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ DirectoryContainsFile** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ diretório CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)
</dt> </dl>

Um [**\_ diretório CIM**](cim-directory.md) que descreve o diretório.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ DataFile do CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Um [**\_ DataFile do CIM**](cim-datafile.md) que descreve o LogicalFile contido no diretório.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI implementa a classe **CIM \_ DirectoryContainsFile** , que é uma classe dinâmica.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

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

[**\_Componente CIM**](cim-component.md)
</dt> </dl>

 

