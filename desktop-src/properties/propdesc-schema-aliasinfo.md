---
description: Especifica um alias de classificação ou uma lista de aliases de classificação especificando um elemento que contém uma propriedade de classificação ou uma lista de propriedades de classificação.
ms.assetid: 4c514197-0df0-49c6-b39e-8a2a7cefa93d
title: aliasInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 052409864617bdaba7acbf9ae561752c83d18395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814504"
---
# <a name="aliasinfo"></a>aliasInfo

Especifica um alias de classificação ou uma lista de aliases de classificação especificando um elemento que contém uma propriedade de classificação ou uma lista de propriedades de classificação. Deve haver apenas um elemento [aliasInfo]() para cada elemento [propertyDescription](./propdesc-schema-propertydescription.md) . Para propriedades que definem cangroupby = true, a menos que uma propriedade de classificação secundária seja especificada ( aliasInfo/@additionalSortByAliases = prop: example), o usuário pode experimentar um comportamento inesperado ao alterar a ordem de classificação em uma exibição que é agrupada pela propriedade. Especificamente, a ordem dos grupos será alterada, mas a ordem dos itens nos grupos não será.

## <a name="syntax"></a>Syntax


```
<!-- aliasInfo -->
<xs:element name="aliasInfo">
    <xs:complexType>
        <xs:attribute name="sortByAlias" type="canonical-name"/>
        <xs:attribute name="additionalSortByAliases" type="proplist"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                   | Elementos filho |
|------------------------------------------------------------------|----------------|
| [propertyDescription](./propdesc-schema-propertydescription.md) | Nenhum           |



 

## <a name="attributes"></a>Atributos



| Atributo               | Descrição                                                                                                                                                            |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sortByAlias             | Público. Opcional. O nome canônico da propriedade que deve ser usada para classificar. Essa cadeia de caracteres é do tipo canônico.                                            |
| additionalSortByAliases | Público. Opcional. Uma lista delimitada por ponto e vírgula de propriedades adicionais a serem usadas durante a classificação. As propriedades são aplicadas à classificação na sequência em que são dadas. |



 

 

 
