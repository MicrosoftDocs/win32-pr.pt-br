---
description: A \_ agregação CIM StorageDefect coleta os erros de armazenamento para uma extensão de armazenamento.
ms.assetid: 7acd3d25-4691-43cb-badc-662684989345
ms.tgt_platform: multiple
title: Classe CIM_StorageDefect
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageDefect
- CIM_StorageDefect.Error
- CIM_StorageDefect.Extent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e6c2be45fe2f44afa407dc72e3ae90c486593ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920541"
---
# <a name="cim_storagedefect-class"></a>\_Classe CIM StorageDefect

A agregação **CIM \_ StorageDefect** coleta os erros de armazenamento para uma extensão de armazenamento.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{5CC70817-DB31-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_StorageDefect
{
  CIM_StorageError  REF Error;
  CIM_StorageExtent REF Extent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ StorageDefect** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ StorageDefect** tem essas propriedades.

<dl> <dt>

**Erro**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ StorageError**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **fraco**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referência ao objeto de erro, que define os endereços inicial e final que são mapeados fora da extensão de armazenamento.

</dd> <dt>

**Extensão**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ StorageExtent**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referência à extensão de armazenamento na qual os erros ocorreram.

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



 

