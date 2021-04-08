---
description: A \_ classe de exportação CIM representa uma associação entre um sistema de arquivos local e seus diretórios, o que indica que os diretórios especificados estão disponíveis para montagem.
ms.assetid: 4c43ba5a-e003-4985-85b3-68ecf13a4bf5
ms.tgt_platform: multiple
title: Classe CIM_Export
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Export
- CIM_Export.Directory
- CIM_Export.ExportedDirectoryName
- CIM_Export.LocalFS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 447601b61fb79cfa779ea0cab75962c835210c52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920391"
---
# <a name="cim_export-class"></a>\_Classe de exportação CIM

A classe de **\_ exportação CIM** representa uma associação entre um sistema de arquivos local e seus diretórios, o que indica que os diretórios especificados estão disponíveis para montagem. Ao exportar um sistema de arquivos inteiro, o diretório deve fazer referência ao diretório de nível superior do sistema de arquivos.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Association, UUID("{75BCF4F8-DB46-11D2-B4C8-80080C7B6371}"), AMENDMENT]
class CIM_Export
{
  CIM_Directory       REF Directory;
  string                  ExportedDirectoryName;
  CIM_LocalFileSystem REF LocalFS;
};
```

## <a name="members"></a>Membros

A classe de **\_ exportação CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ exportação CIM** tem essas propriedades.

<dl> <dt>

**Diretório**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ diretório CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao diretório exportado para montagem NFS (sistema de arquivos de rede).

</dd> <dt>

**ExportedDirectoryName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome sob o qual o diretório é exportado.

</dd> <dt>

**LocalFS**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ LocalFileSystem**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referência ao sistema de arquivos local.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

