---
description: Associa um serviço ao seu sistema de computador de hospedagem.
ms.assetid: 888ABA71-6D67-4933-89E6-40F731AA7153
title: Classe Msvm_HostedService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedService
- Msvm_HostedService.Antecedent
- Msvm_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 284254d32e788e374d56b3822f5c00868552e1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782808"
---
# <a name="msvm_hostedservice-class"></a>\_Classe Msvm HostedService

Associa um serviço ao seu sistema de computador de hospedagem. As instâncias de [**Msvm \_ VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) podem ser descobertas por meio de sua associação com um host.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedService : CIM_HostedService
{
  CIM_ManagedElement REF Antecedent;
  CIM_Service        REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ HostedService** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ HostedService** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência ao sistema de computador de hospedagem. Essa propriedade é herdada de [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência ao serviço que está sendo hospedado. Essa propriedade é herdada de [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ HostedService** pode ser restringido pela filtragem UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemplos

Consulte [consultando objetos de rede](querying-networking-objects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**HostedService do CIM \_**](cim-hostedservice.md)
</dt> <dt>

[**HostedService do CIM \_**](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> <dt>

[Classes de gerenciamento do sistema virtual](virtual-system-management-classes.md)
</dt> </dl>

 

