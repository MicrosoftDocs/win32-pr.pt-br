---
description: Representa a associação entre um trabalho e os elementos gerenciados que podem ser afetados pela sua execução.
ms.assetid: 81849DE4-9039-426F-B7B1-45BB31A9132C
title: Classe Msvm_AffectedStorageJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedStorageJobElement
- Msvm_AffectedStorageJobElement.AffectedElement
- Msvm_AffectedStorageJobElement.AffectingElement
- Msvm_AffectedStorageJobElement.ElementEffects
- Msvm_AffectedStorageJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9eed09eab5a2bbb6985d1dc230d12a4f60fe5834b3fce1927036b560adc5d7e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693516"
---
# <a name="msvm_affectedstoragejobelement-class"></a>\_Classe Msvm AffectedStorageJobElement

Representa a associação entre um trabalho e os elementos gerenciados que podem ser afetados pela sua execução.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedStorageJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_StorageJob    REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ AffectedStorageJobElement** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ AffectedStorageJobElement** tem essas propriedades.

<dl> <dt>

**Afetadoselement**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

O elemento gerenciado afetado pela execução do trabalho. Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**Afetando**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ StorageJob**](msvm-storagejob.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ AffectedJobElement. influenciaelement")
</dt> </dl>

O trabalho que está afetando o elemento afetado. Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma enumeração que descreve o efeito sobre o elemento gerenciado. Essa matriz corresponde à matriz da propriedade **OtherElementEffectsDescriptions** , em que o último fornece detalhes relacionados aos efeitos de alto nível enumerados por essa propriedade. Detalhes adicionais serão necessários se a matriz da propriedade **ElementEffects** contiver o valor 1, (outro). Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)
</dt> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>**Uso exclusivo** (2)
</dt> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>**Impacto no desempenho** (3)
</dt> <dt>

<span id="Element_Integrity_"></span><span id="element_integrity_"></span><span id="ELEMENT_INTEGRITY_"></span>**Integridade do elemento** (4)
</dt> </dl>

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fornece detalhes para o efeito na posição da matriz correspondente na matriz da propriedade **ElementEffects** . Essas informações são necessárias sempre que o elemento correspondente na matriz da propriedade **ElementEffects** contiver o valor 1 (outro). Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ AffectedStorageJobElement** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[Armazenamento Classe](storage-classes.md)
</dt> </dl>

 

