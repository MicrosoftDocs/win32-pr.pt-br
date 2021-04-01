---
description: Associa uma instância de máquina virtual ao serviço de gerenciamento que controla seu estado.
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Classe Msvm_ServiceAffectsElement
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
ms.openlocfilehash: eadb9f33015091999776b73c83d792ccd29396b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090796"
---
# <a name="msvm_serviceaffectselement-class"></a>Classe Msvm não \_ afetaelement

Associa uma instância de máquina virtual ao serviço de gerenciamento que controla seu estado.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

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

A classe **Msvm não \_ afetaelement** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm não \_ afetaelement** tem essas propriedades.

<dl> <dt>

**Afetadoselement**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência à máquina virtual. Essa propriedade é herdada de [**CIM \_ imafetaelement**](/previous-versions//cc136907(v=vs.85)).

</dd> <dt>

**Afetando**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma referência ao serviço que controla a máquina virtual. Essa propriedade é herdada de [**CIM \_ imafetaelement**](/previous-versions//cc136907(v=vs.85)).

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o tipo de controle que a associação representa. Essa propriedade é herdada de [**CIM \_ imafetaelement**](/previous-versions//cc136907(v=vs.85))e é sempre definida como o valor a seguir.



| Valor                                                                        | Significado            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>5</dt> </dl> | Gerencia<br/> |



 

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os detalhes do tipo de associação na posição da matriz correspondente na matriz da propriedade **ElementAffects** . Essas informações serão necessárias se **ElementAffects** estiver definido como 1 (outro). Essa propriedade é herdada de [**CIM \_ imafetaelement**](/previous-versions//cc136907(v=vs.85))e é sempre definida como **nula**.

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm de \_ paraafetaelement** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM \_ Imafetaelement**](cim-serviceaffectselement.md)
</dt> <dt>

[**CIM \_ Imafetaelement**](/previous-versions//cc136907(v=vs.85))
</dt> </dl>

 

