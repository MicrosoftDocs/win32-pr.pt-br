---
description: Associa uma instância de máquina virtual ao serviço de gerenciamento que controla seu estado.
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Msvm_ServiceAffectsElement classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceAffectsElement
- Msvm_ServiceAffectsElement.AffectedElement
- Msvm_ServiceAffectsElement.AffectingElement
- Msvm_ServiceAffectsElement.ElementEffects
- Msvm_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db9ab0ff0aa3eab6f0268f7e85cb5f4efd0e7d2624c7e97a95abb3dd3b414ab2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582276"
---
# <a name="msvm_serviceaffectselement-class"></a>Classe Msvm \_ ServiceAffectsElement

Associa uma instância de máquina virtual ao serviço de gerenciamento que controla seu estado.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceAffectsElement : CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[] = 5;
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ ServiceAffectsElement** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ ServiceAffectsElement** tem essas propriedades.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência à máquina virtual. Essa propriedade é herdada [**de \_ ServiceAffectsElement do CIM.**](/previous-versions//cc136907(v=vs.85))

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Serviço CIM \_**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência ao serviço que controla a máquina virtual. Essa propriedade é herdada [**de \_ ServiceAffectsElement do CIM.**](/previous-versions//cc136907(v=vs.85))

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o tipo de controle que a associação representa. Essa propriedade é herdada [**de \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))do CIM e sempre é definida com o valor a seguir.



| Valor                                                                        | Significado            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>5</dt> </dl> | Gerencia<br/> |



 

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os detalhes do tipo de associação na posição da matriz correspondente na matriz de **propriedades ElementAffects.** Essas informações são necessárias se **ElementAffects** for definido como 1 (Outro). Essa propriedade é herdada [**de Cim \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))e é sempre definida como **Null.**

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe Msvm \_ ServiceAffectsElement** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM \_ ServiceAffectsElement**](cim-serviceaffectselement.md)
</dt> <dt>

[**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))
</dt> </dl>

 

