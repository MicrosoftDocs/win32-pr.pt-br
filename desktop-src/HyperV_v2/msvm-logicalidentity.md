---
description: Associa dois elementos gerenciados que representam diferentes aspectos da mesma entidade subjacente.
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Classe Msvm_LogicalIdentity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalIdentity
- Msvm_LogicalIdentity.SameElement
- Msvm_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2f8d2ee522fde3769c08bcbb78611b99eed8e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505859"
---
# <a name="msvm_logicalidentity-class"></a>\_Classe Msvm LogicalIdentity

Associa dois elementos gerenciados que representam diferentes aspectos da mesma entidade subjacente. Essa classe deriva do [**CIM \_ LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalIdentity : CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ LogicalIdentity** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ LogicalIdentity** tem essas propriedades.

<dl> <dt>

**Mesmoelement**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ LogicalElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência a um aspecto alternativo da entidade do sistema.

</dd> <dt>

**Sistema de**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ LogicalElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência a um aspecto do elemento lógico.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                 |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_LOGICALIDENTITY CIM**](cim-logicalidentity.md)
</dt> <dt>

[**\_LOGICALIDENTITY CIM**](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

