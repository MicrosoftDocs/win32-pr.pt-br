---
description: A associação CIM \_ ActsAsSpare indica quais elementos podem ser sobressalentes ou substituir outros elementos agregados. Um sobressalente pode operar no modo &\# 0034;hot-standby&0034; conforme especificado em uma base elemento a \# elemento.
ms.assetid: bed8c552-f782-4af9-9441-ff3268182c3b
ms.tgt_platform: multiple
title: CIM_ActsAsSpare classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActsAsSpare
- CIM_ActsAsSpare.Group
- CIM_ActsAsSpare.HotStandby
- CIM_ActsAsSpare.Spare
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b76b9dbd4a5a3302d1aae328bcd096dee5cd03e1615d3c7e30c58f3344ea67f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080950"
---
# <a name="cim_actsasspare-class"></a>Classe CIM \_ ActsAsSpare

A **associação CIM \_ ActsAsSpare** indica quais elementos podem ser sobressalentes ou substituir outros elementos agregados. Um sobressalente pode operar no modo de "espera quente", conforme especificado em uma base elemento a elemento.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Association, UUID("{64C1726E-DB21-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ActsAsSpare
{
  CIM_SpareGroup           REF Group;
  boolean                      HotStandby;
  CIM_ManagedSystemElement REF Spare;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ ActsAsSpare** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ ActsAsSpare** tem essas propriedades.

<dl> <dt>

**Grupo**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ SpareGroup CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência à propriedade **Group** que representa a [**classe \_ SpareGroup CIM.**](cim-sparegroup.md)

</dd> <dt>

**HotStandby**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **TRUE**, o sobressalente está operando como um modo de espera quente.

</dd> <dt>

**Poupar**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ ManagedSystemElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência a um elemento do sistema gerenciado atuando como um sobressalente e participando do grupo sobressalente.

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[CIM Classes](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

