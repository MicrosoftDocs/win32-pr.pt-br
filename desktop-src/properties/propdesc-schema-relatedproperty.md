---
description: Novo para Windows 7. Identifica uma propriedade relacionada à propriedade definida no arquivo de descrição da propriedade.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285c0f8b0731ba790cd57105f907cd4df85b6faa41c3f649588aca7ef457418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938676"
---
# <a name="relatedproperty"></a>relatedProperty

Novo para Windows 7. Identifica uma propriedade relacionada à propriedade definida no arquivo de descrição da propriedade. Pode haver tantos elementos [relatedProperty em]() [um relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) quanto necessário.

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

Esse elemento permite mapear uma propriedade para outra. Por exemplo, você pode mapear o texto de sua propriedade personalizada, Fabrikam.StorageCapacity, para System.Capacity:


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
