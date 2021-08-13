---
description: A \_ classe CIM CollectedCollections é uma associação de agregação que representa uma coleção de elementos do sistema gerenciados (MSE) contidas em uma coleção de MSEs.
ms.assetid: 7baaf429-1211-4545-ace2-c6312d53c0f6
ms.tgt_platform: multiple
title: Classe CIM_CollectedCollections
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectedCollections
- CIM_CollectedCollections.Collection
- CIM_CollectedCollections.CollectionInCollection
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cecac67d96aba6b8ad8c5937f098eaef312af89b80c28febaa8073c5f7be26f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322286"
---
# <a name="cim_collectedcollections-class"></a>\_Classe CIM CollectedCollections

A classe **CIM \_ CollectedCollections** é uma associação de agregação que representa uma coleção de elementos do sistema gerenciados (MSE) contidas em uma coleção de MSEs.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class CIM_CollectedCollections
{
  CIM_CollectionOfMSEs REF Collection;
  CIM_CollectionOfMSEs REF CollectionInCollection;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ CollectedCollections** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ CollectedCollections** tem essas propriedades.

<dl> <dt>

**Coleção**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao elemento "nível superior" ou pai na agregação.

</dd> <dt>

**CollectionInCollection**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ CollectionOfMSEs**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência à **coleção**"coletada".

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



 

 




