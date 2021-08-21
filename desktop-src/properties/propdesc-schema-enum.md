---
description: Usado para atribuir texto enumerado a valores discretos.
ms.assetid: c8cc040e-fcce-43a0-98c1-db2b2c616ac3
title: enum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1336a690fe7ac1e19a8606912a4f7d538d3842ab6a490d17b89f90f64bbfbc13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970975"
---
# <a name="enum"></a>enum

Usado para atribuir texto enumerado a valores discretos. Qualquer número desses elementos pode existir em um [enumeratedList](./propdesc-schema-enumeratedlist.md). Por meio de programação, eles são representados como objetos IPropertyEnumType, cujo método [**IPropertyEnumType:: Getenumtype**](/windows/win32/api/propsys/nf-propsys-ipropertyenumtype-getenumtype) retorna um animal \_ discreto.

## <a name="syntax"></a>Syntax


```
<!-- enum -->
<xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
        <xs:attribute name="value" type="xs:string" use="required"/>
        <xs:attribute name="text" type="xs:string" use="required"/>
        <xs:attribute name="mnemonics" type="xs:string"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                         | Elementos filho |
|--------------------------------------------------------|----------------|
| [enumeratedList](./propdesc-schema-enumeratedlist.md) | nenhum           |



 

## <a name="attributes"></a>Atributos



| Atributo | Descrição                                                                                                                                                                                                          |
|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| value     | Público. Obrigatórios. O valor discreto (cadeia de caracteres ou número) ao qual será atribuído o texto enumerado.                                                                                                                           |
| texto      | Público. Obrigatórios. O texto usado para exibir o valor enumerado. A sintaxe permite uma cadeia de caracteres de exibição direta ou uma referência de cadeia de caracteres de exibição indireta; Use a cadeia de caracteres de exibição indireta para que ela possa ser localizada. |
| mnemônico | **Windows 7 e posterior.** Público. Opcional. Uma lista de valores mnemônicos que podem ser usados para fazer referência à propriedade em consultas de pesquisa. A lista é delimitada com o \| caractere ' '.                                     |



 

 

 
