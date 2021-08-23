---
description: Define os perfis registrados para os quais o sistema referenciado está em conformidade.
ms.assetid: F01E79BE-82D9-49E0-AB0C-FD1B48BC4A55
title: Classe Msvm_ElementConformsToProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementConformsToProfile
- Msvm_ElementConformsToProfile.ConformantStandard
- Msvm_ElementConformsToProfile.ManagedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a80dfcb5ab260b4d60b6370bb34698efb201401f0c6d4924b143e8b9041258a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525046"
---
# <a name="msvm_elementconformstoprofile-class"></a>\_Classe Msvm ElementConformsToProfile

Define os perfis registrados para os quais o sistema referenciado está em conformidade. Essa associação pode se aplicar a qualquer elemento gerenciado. O uso típico irá aplicá-lo a uma instância de nível superior, como um sistema, namespace ou serviço. Quando aplicado a uma instância de nível superior, todas as partes constituintes devem se comportar adequadamente para dar suporte à conformidade do elemento gerenciado com o perfil registrado nomeado.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class Msvm_ElementConformsToProfile : CIM_ElementConformsToProfile
{
  Msvm_RegisteredProfile REF ConformantStandard;
  Msvm_ComputerSystem    REF ManagedElement;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ ElementConformsToProfile** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ ElementConformsToProfile** tem essas propriedades.

<dl> <dt>

**ConformantStandard**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ RegisteredProfile**](msvm-registeredprofile.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **substituição**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Uma referência a uma instância da classe [**Msvm \_ RegisteredProfile**](msvm-registeredprofile.md) que representa o perfil registrado no qual o sistema está em conformidade.

</dd> <dt>

**Managedelement**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **substituição**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Uma referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa o sistema que está de acordo com o perfil registrado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

