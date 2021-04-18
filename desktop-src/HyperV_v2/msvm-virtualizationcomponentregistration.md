---
description: Representa o registro de um serviço na plataforma Microsoft Hyper-V.
ms.assetid: 706557C2-49D6-453F-9DC0-2C655888EEBE
title: Classe Msvm_VirtualizationComponentRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponentRegistration
- Msvm_VirtualizationComponentRegistration.Component
- Msvm_VirtualizationComponentRegistration.ResourceType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e9704dcade0474a10ca60383280941ec2e3591b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789798"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a>\_Classe Msvm VirtualizationComponentRegistration

Representa o registro de um serviço na plataforma Microsoft Hyper-V.

A sintaxe a seguir é simplificada formato MOF código (MOF).

## <a name="syntax"></a>Sintaxe

``` syntax
class Msvm_VirtualizationComponentRegistration
{
  Msvm_VirtualizationComponent REF Component;
  Msvm_ResourceTypeDefinition  REF ResourceType;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualizationComponentRegistration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualizationComponentRegistration** tem essas propriedades.

<dl> <dt>

**Componente**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência a uma instância que descreve o objeto COM que implementa essa classe.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência a uma instância que descreve um tipo de recurso com suporte pelo serviço.

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ VirtualizationComponentRegistration** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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



 

