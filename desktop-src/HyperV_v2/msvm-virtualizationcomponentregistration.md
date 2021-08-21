---
description: representa o registro de um serviço na plataforma Microsoft Hyper-V.
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
ms.openlocfilehash: c7acd111ab95f59146763e874d40c4efb411313938c94b1a4527aa1e2d08490c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146550"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a>\_Classe Msvm VirtualizationComponentRegistration

representa o registro de um serviço na plataforma Microsoft Hyper-V.

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
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Fim do suporte do cliente<br/>    | Windows 8.1<br/>                                                                                  |
| Fim do suporte do servidor<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

