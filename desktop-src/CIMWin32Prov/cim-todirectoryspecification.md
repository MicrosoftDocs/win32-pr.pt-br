---
description: A \_ associação CIM ToDirectorySpecification identifica o diretório de destino para a ação de arquivo.
ms.assetid: ab31101f-1948-4b3d-baef-0d61d5898b21
ms.tgt_platform: multiple
title: Classe CIM_ToDirectorySpecification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ToDirectorySpecification
- CIM_ToDirectorySpecification.DestinationDirectory
- CIM_ToDirectorySpecification.FileName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e079a5012760507adfd9bff6b9716a6828e1f3e9b516ec252895ab8e93e801d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118677382"
---
# <a name="cim_todirectoryspecification-class"></a>\_Classe CIM ToDirectorySpecification

A associação **CIM \_ ToDirectorySpecification** identifica o diretório de destino para a ação de arquivo. Quando essa associação é usada, supõe-se que o diretório de destino já existe. Essa associação não pode existir com uma associação [**CIM \_ todirectoryaction**](cim-todirectoryaction.md) , pois uma ação de arquivo só pode envolver um único diretório de destino.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{C3E25A3C-DB31-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ToDirectorySpecification
{
  CIM_DirectorySpecification REF DestinationDirectory;
  CIM_CopyFileAction         REF FileName;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ToDirectorySpecification** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ToDirectorySpecification** tem essas propriedades.

<dl> <dt>

**DestinationDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ DirectorySpecification**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Referência ao diretório de destino.

</dd> <dt>

**FileName**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ CopyAction**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (0)
</dt> </dl>

Referência ao nome do arquivo.

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



 

