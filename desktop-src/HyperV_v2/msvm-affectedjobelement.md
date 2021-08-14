---
description: Representa uma associação entre um trabalho e o elemento gerenciado que pode ser afetado pela sua execução.
ms.assetid: 125A4976-A4E3-4D7A-A43B-86045C3B00AE
title: Classe Msvm_AffectedJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedJobElement
- Msvm_AffectedJobElement.AffectedElement
- Msvm_AffectedJobElement.AffectingElement
- Msvm_AffectedJobElement.ElementEffects
- Msvm_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f39d800516f96cf602257abc3bd8ed9ed5a8d5561f4b4a5e60f5eb140fc1c308
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693536"
---
# <a name="msvm_affectedjobelement-class"></a>\_Classe Msvm AffectedJobElement

Representa uma associação entre um trabalho e o elemento gerenciado que pode ser afetado pela sua execução.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_ConcreteJob   REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ AffectedJobElement** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ AffectedJobElement** tem essas propriedades.

<dl> <dt>

**Afetadoselement**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O elemento gerenciado afetado pela execução do trabalho. Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**Afetando**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ ConcreteJob**](msvm-concretejob.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O trabalho que está afetando o elemento gerenciado. Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma enumeração que descreve o efeito sobre o elemento gerenciado. Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fornece detalhes para o efeito na posição da matriz correspondente em **ElementEffects**. Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ AffectedJobElement** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_AFFECTEDJOBELEMENT CIM**](cim-affectedjobelement.md)
</dt> <dt>

[**\_AFFECTEDJOBELEMENT CIM**](/previous-versions//cc150663(v=vs.85))
</dt> <dt>

[Classes de gerenciamento do sistema virtual](virtual-system-management-classes.md)
</dt> </dl>

 

