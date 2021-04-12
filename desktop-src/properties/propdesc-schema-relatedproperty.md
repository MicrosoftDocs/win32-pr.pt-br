---
description: Novo no Windows 7. Identifica uma propriedade que está relacionada à propriedade definida no arquivo de descrição da propriedade.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabde093a47a25834598659d3ad38e0847c1351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296609"
---
# <a name="relatedproperty"></a>relatedProperty

Novo no Windows 7. Identifica uma propriedade que está relacionada à propriedade definida no arquivo de descrição da propriedade. Pode haver tantos elementos [relatedproperty]() dentro de um [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) , conforme necessário.

## <a name="syntax"></a>Syntax


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                   | Elementos filho |
|------------------------------------------------------------------|----------------|
| [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) | Nenhum           |



 

## <a name="attributes"></a>Atributos



| Atributo        | Descrição                                                        |
|------------------|--------------------------------------------------------------------|
| relationshipName | Público. Obrigatórios. O nome canônico da relação de propriedade. |
| propertyName     | Público. Obrigatórios. O nome canônico da propriedade relacionada.      |



 

## <a name="remarks"></a>Comentários

Esse elemento permite mapear uma propriedade para outra. Por exemplo, você pode mapear o texto da propriedade personalizada, fabrikam. StorageCapacity, para System. Capacity:


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
