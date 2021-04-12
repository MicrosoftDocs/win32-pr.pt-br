---
description: Registra um serviço que fornece objetos relacionados a recursos específicos da máquina virtual.
ms.assetid: 85782C4D-E0A3-4EED-9A26-7928862C559B
title: Classe Msvm_VirtualSystemResourceRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceRegistration
- Msvm_VirtualSystemResourceRegistration.ResourceType
- Msvm_VirtualSystemResourceRegistration.Component
- Msvm_VirtualSystemResourceRegistration.IsRootDevice
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7cef3699de973bd22985215a64100c594f223be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501367"
---
# <a name="msvm_virtualsystemresourceregistration-class"></a>\_Classe Msvm VirtualSystemResourceRegistration

Registra um serviço que fornece objetos relacionados a recursos específicos da máquina virtual.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class Msvm_VirtualSystemResourceRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition         REF ResourceType;
  Msvm_VirtualSystemResourceComponent REF Component;
  boolean                                 IsRootDevice = False;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualSystemResourceRegistration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualSystemResourceRegistration** tem essas propriedades.

<dl> <dt>

**Componente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência a uma instância que descreve o objeto COM que implementa essa classe.

</dd> <dt>

**IsRootDevice**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**True** se esse registro indicar se o tipo de recurso especificado é o dispositivo raiz (ou menos) para este serviço; caso contrário, **false**. Somente um registro pode existir quando **IsRootDevice** é definido como **true**. Caso contrário, esse registro representa um mapeamento para um subdispositivo. Essa propriedade é sempre definida como **false**.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência a uma instância que descreve um tipo de recurso com suporte pelo serviço. Esta propriedade é herdada de [**Msvm \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ VirtualSystemResourceRegistration** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Fim do suporte do cliente<br/>    | Windows 8.1<br/>                                                                                  |
| Fim do suporte do servidor<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualizationComponentRegistration**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[**Msvm \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

