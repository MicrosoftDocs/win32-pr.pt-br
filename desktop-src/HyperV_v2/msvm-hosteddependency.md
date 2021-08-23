---
description: Associa uma instância de máquina virtual ao objeto do sistema de computador que representa o sistema físico de hospedagem.
ms.assetid: 755624D7-04D0-47EA-8623-DEDE6B1D5CBC
title: Msvm_HostedDependency classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedDependency
- Msvm_HostedDependency.Antecedent
- Msvm_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b0c67df565be0085d4579bf82b2a2d2e542f856e93321240821bc512be692c6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014514"
---
# <a name="msvm_hosteddependency-class"></a>Classe HostedDependency Msvm \_

Associa uma instância de máquina virtual ao objeto do sistema de computador que representa o sistema físico de hospedagem.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedDependency : CIM_HostedDependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a>Membros

A **classe \_ HostedDependency do Msvm** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ HostedDependency do Msvm** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência ao sistema de computador de hospedagem. Essa propriedade é herdada de [**CIM \_ HostedDependency.**](/previous-versions//cc136861(v=vs.85))

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência à máquina virtual. Essa propriedade é herdada de [**CIM \_ HostedDependency.**](/previous-versions//cc136861(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe \_ HostedDependency do Msvm** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ HostedDependency**](cim-hosteddependency.md)
</dt> <dt>

[**CIM \_ HostedDependency**](/previous-versions//cc136861(v=vs.85))
</dt> <dt>

[Classes de gerenciamento de sistema virtual](virtual-system-management-classes.md)
</dt> </dl>

 

