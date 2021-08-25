---
description: A classe CIM ResidesOnExtent representa uma associação entre um sistema de arquivos e \_ a extensão de armazenamento em que ele está localizado. Normalmente, um sistema de arquivos reside em um disco lógico.
ms.assetid: 911a81e9-3032-41ff-a337-044c06d02307
ms.tgt_platform: multiple
title: CIM_ResidesOnExtent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResidesOnExtent
- CIM_ResidesOnExtent.Dependent
- CIM_ResidesOnExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b7149de4ab84b13ef4e0f6b2c3aed908f8ef933ad09541c885f53edd3caec9d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920346"
---
# <a name="cim_residesonextent-class"></a>Classe CIM \_ ResidesOnExtent

A **classe CIM \_ ResidesOnExtent** representa uma associação entre um sistema de arquivos e a extensão de armazenamento em que ele está localizado. Normalmente, um sistema de arquivos reside em um disco lógico.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{10458E26-DB37-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ResidesOnExtent : CIM_Dependency
{
  CIM_FileSystem    REF Dependent;
  CIM_StorageExtent REF Antecedent;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ ResidesOnExtent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ ResidesOnExtent** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ StorageExtent**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")
</dt> </dl>

Um [**\_ StorageExtent cim**](cim-storageextent.md) que descreve a extensão de armazenamento.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ FileSystem**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

Um [**\_ FileSystem CIM**](cim-filesystem.md) que descreve o sistema de arquivos localizado na extensão de armazenamento.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe CIM \_ ResidesOnExtent** é derivada da [**\_ Dependência CIM.**](cim-dependency.md)

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Dependência cim \_**](cim-dependency.md)
</dt> </dl>

 

