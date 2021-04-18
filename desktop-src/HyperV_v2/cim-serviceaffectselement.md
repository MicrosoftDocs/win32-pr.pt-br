---
description: Representa uma associação entre um serviço e um elemento gerenciado que pode ser afetado pela sua execução.
ms.assetid: 2fd9199f-9ab0-4c42-9708-d6cd6911f77a
title: Classe CIM_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ServiceAffectsElement
- CIM_ServiceAffectsElement.AffectedElement
- CIM_ServiceAffectsElement.AffectingElement
- CIM_ServiceAffectsElement.ElementEffects
- CIM_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2e4dd4fe00d1ee4a537741ce69240413e78aca85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756772"
---
# <a name="cim_serviceaffectselement-class"></a>\_Classe CIM Imafetaelement

Representa uma associação entre um serviço e um elemento gerenciado que pode ser afetado pela sua execução.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Membros

A classe **CIM \_ fileafetelement** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ fileafetelement** tem essas propriedades.

<dl> <dt>

**Afetadoselement**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ managedelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O elemento gerenciado que é afetado pelo serviço.

</dd> <dt>

**Afetando**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ serviço CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O serviço que está afetando o elemento gerenciado.

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM imafetaelement**.**OtherElementEffectsDescriptions**")
</dt> </dl>

O efeito no elemento gerenciado. Essa matriz corresponde à matriz **OtherElementEffectsDescriptions** .

\- Uso exclusivo (2): nenhum outro serviço pode ter essa associação com o elemento.

\- Impacto no desempenho (3): preterido em favor de "consumir", "aprimorar o desempenho" ou "degradar o desempenho". A execução do serviço pode aprimorar ou degradar o desempenho do elemento. Isso pode ser um efeito colateral de execução ou como uma conseqüência pretendida de métodos fornecidos pelo serviço.

\- Integridade do elemento (4): preterida em favor de "consumir", "aprimorar a integridade" ou "degradar a integridade". A execução do serviço pode aprimorar ou degradar a integridade do elemento. Isso pode ser um efeito colateral de execução ou como uma conseqüência pretendida de métodos fornecidos pelo serviço.

\- Gerencia (5): o serviço gerencia o elemento.

\- Consome (6): a execução do serviço consome parte ou todos os elementos associados como consequência da execução do serviço. Por exemplo, o serviço pode consumir ciclos de CPU, o que pode afetar o desempenho ou o armazenamento que pode afetar o desempenho e a integridade. (Por exemplo, a falta de armazenamento livre pode prejudicar a integridade, reduzindo a capacidade de salvar o estado. ) "Consuma" pode ser usado sozinha ou em conjunto com outros valores, em particular, "degradar o desempenho" e "degradar a integridade".

"Gerencia" e não "consome" devem ser usados para refletir os serviços de alocação que podem ser fornecidos por um serviço.

\- Aprimora a integridade (7): o serviço pode aprimorar a integridade do elemento associado.

\- Degrada a integridade (8): o serviço pode prejudicar a integridade do elemento associado.

\- Aprimora o desempenho (9): o serviço pode melhorar o desempenho do elemento associado.

\- Degrada o desempenho (10): o serviço pode prejudicar o desempenho do elemento associado.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Exclusive_Use"></span><span id="exclusive_use"></span><span id="EXCLUSIVE_USE"></span>

**Uso exclusivo** (2)


</dt> <dd></dd> <dt>

<span id="Performance_Impact"></span><span id="performance_impact"></span><span id="PERFORMANCE_IMPACT"></span>

**Impacto no desempenho** (3)


</dt> <dd></dd> <dt>

<span id="Element_Integrity"></span><span id="element_integrity"></span><span id="ELEMENT_INTEGRITY"></span>

**Integridade do elemento** (4)


</dt> <dd></dd> <dt>

<span id="Manages"></span><span id="manages"></span><span id="MANAGES"></span>

**Gerencia** (5)


</dt> <dd></dd> <dt>

<span id="Consumes"></span><span id="consumes"></span><span id="CONSUMES"></span>

**Consumo** (6)


</dt> <dd></dd> <dt>

<span id="Enhances_Integrity"></span><span id="enhances_integrity"></span><span id="ENHANCES_INTEGRITY"></span>

**Aprimora a integridade** (7)


</dt> <dd></dd> <dt>

<span id="Degrades_Integrity"></span><span id="degrades_integrity"></span><span id="DEGRADES_INTEGRITY"></span>

**Degradação da integridade** (8)


</dt> <dd></dd> <dt>

<span id="Enhances_Performance"></span><span id="enhances_performance"></span><span id="ENHANCES_PERFORMANCE"></span>

**Melhora o desempenho** (9)


</dt> <dd></dd> <dt>

<span id="Degrades_Performance"></span><span id="degrades_performance"></span><span id="DEGRADES_PERFORMANCE"></span>

**Degrada o desempenho** (10)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor reservado** (0x8000.. 0xFFFF


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM imafetaelement**.**ElementEffects**")
</dt> </dl>

Cada item na matriz fornece informações adicionais para o item correspondente na matriz **ElementEffects** . Uma descrição é necessária para qualquer item na matriz **ElementEffects** que está definida como **Other** ("1").

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

