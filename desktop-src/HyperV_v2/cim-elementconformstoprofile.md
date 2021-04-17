---
description: Representa uma associação na qual um elemento gerenciado está em conformidade com o padrão de um perfil registrado.
ms.assetid: 9d5704b6-c764-4f68-bce3-384d5a244e28
title: Classe CIM_ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementConformsToProfile
- CIM_ElementConformsToProfile.ConformantStandard
- CIM_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7034001641029099d1b52090b3cc518b6589dc50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811881"
---
# <a name="cim_elementconformstoprofile-class"></a>\_Classe CIM ElementConformsToProfile

Representa uma associação na qual um elemento gerenciado está em conformidade com o padrão de um perfil registrado. Essa associação geralmente se aplica a uma instância de nível superior, como um sistema, namespace ou serviço. Quando aplicado a uma instância de nível superior, todas as partes constituintes devem se comportar adequadamente para dar suporte à conformidade do Managedelement com o RegisteredProfile nomeado.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.8.0"), UMLPackagePath("CIM::Interop")]
class CIM_ElementConformsToProfile
{
  CIM_RegisteredProfile REF ConformantStandard;
  CIM_ManagedElement    REF ManagedElement;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ElementConformsToProfile** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ElementConformsToProfile** tem essas propriedades.

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ RegisteredProfile**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O perfil registrado no qual o elemento gerenciado está em conformidade.

</dd> <dt>

**Managedelement**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ managedelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O elemento gerenciado que está de acordo com o perfil registrado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

