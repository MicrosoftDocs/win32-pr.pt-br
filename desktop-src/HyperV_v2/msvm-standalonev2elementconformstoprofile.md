---
description: Define os perfis registrados para os quais o sistema autônomo referenciado está em conformidade.
ms.assetid: d9ede8d0-c6f3-48bd-84a9-7f2c31637819
title: Classe Msvm_StandaloneV2ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StandaloneV2ElementConformsToProfile
- Msvm_StandaloneV2ElementConformsToProfile.ConformantStandard
- Msvm_StandaloneV2ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5506119f0e8938a29b94b298460a1f164dab97359d13d956bfa5ca74e97a081b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950235"
---
# <a name="msvm_standalonev2elementconformstoprofile-class"></a>\_Classe Msvm StandaloneV2ElementConformsToProfile

Define os perfis registrados para os quais o sistema autônomo referenciado está em conformidade.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class Msvm_StandaloneV2ElementConformsToProfile : Msvm_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard = $SVP;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ StandaloneV2ElementConformsToProfile** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ StandaloneV2ElementConformsToProfile** tem essas propriedades.

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ RegisteredProfile**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **substituição**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

O perfil registrado no qual o sistema autônomo está de acordo.

</dd> <dt>

**Managedelement**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ ComputerSystem**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers), **MSFT \_ targetNamespace** (" \\ \\ virtualização de raiz \\ \\ v2")
</dt> </dl>

O sistema autônomo que está em conformidade com o perfil registrado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Interoperabilidade raiz<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ ElementConformsToProfile**](msvm-elementconformstoprofile.md)
</dt> </dl>

 

