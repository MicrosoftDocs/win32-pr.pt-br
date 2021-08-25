---
description: A associação CIM \_ FromDirectoryAction identifica o diretório de origem para a ação do arquivo.
ms.assetid: 25d06dad-ae39-4cfc-9331-4be7ef02d87c
ms.tgt_platform: multiple
title: CIM_FromDirectoryAction classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FromDirectoryAction
- CIM_FromDirectoryAction.FileName
- CIM_FromDirectoryAction.SourceDirectory
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2d9055b47448bf21543dd738f5378ac0e19d209ebb0a40346e07cd57e01c8f63
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923726"
---
# <a name="cim_fromdirectoryaction-class"></a>Classe CIM \_ FromDirectoryAction

A **associação CIM \_ FromDirectoryAction** identifica o diretório de origem para a ação do arquivo. Quando essa associação é usada, a suposição é que o diretório de origem foi criado por uma ação anterior. Essa associação não pode existir com uma [**associação CIM \_ FromDirectorySpecification;**](cim-fromdirectoryspecification.md) uma ação de arquivo só pode envolver um único diretório de origem.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{55D5B446-DB2A-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_FromDirectoryAction
{
  CIM_FileAction      REF FileName;
  CIM_DirectoryAction REF SourceDirectory;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ FromDirectoryAction** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ FromDirectoryAction** tem essas propriedades.

<dl> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de dados: **Arquivo \_ CIMAction**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Referência ao nome do arquivo.

</dd> <dt>

**SourceDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **Diretório \_ CIMAction**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Referência ao diretório de origem.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

