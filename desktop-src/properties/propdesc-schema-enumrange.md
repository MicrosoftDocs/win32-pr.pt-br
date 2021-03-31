---
description: Atribui o texto de enumeração a um intervalo de valores. Cada elemento enumRange especifica um valor mínimo e se estende até o valor mínimo do próximo elemento ou até que não haja mais elementos enumRange.
ms.assetid: 00c56c2d-6693-4b09-b28a-21d69930bf35
title: enumRange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 964835c376c5496d23e8d277409575758002a0d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921340"
---
# <a name="enumrange"></a>enumRange

Atribui o texto de enumeração a um intervalo de valores. Cada elemento [enumRange]() especifica um valor mínimo e se estende até o valor mínimo do próximo elemento ou até que não haja mais elementos enumRange.

## <a name="syntax"></a>Syntax

``` syntax
<!-- enumRange -->
<xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="image" minOccurs="0" maxOccurs="1"/>
        </xs:sequence>
            <xs:attribute name="minValue" type="xs:integer" use="required"/>
            <xs:attribute name="setValue" type="xs:integer"/>
            <xs:attribute name="text" type="xs:string"/>
            <xs:attribute name="name" type="canonical-name"/> <!--Maximum of 64 characters-->
            <xs:attribute name="mnemonics" type="xs:string"/> 
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Informações do elemento



| Elemento pai                                         | Elementos filho |
|--------------------------------------------------------|----------------|
| [enumeratedList](./propdesc-schema-enumeratedlist.md) | none           |



 

## <a name="attributes"></a>Atributos



| Atributo | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| minValue  | Público. Obrigatórios. O valor mínimo no intervalo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| setValue  | Público. Opcional. Quando um usuário seleciona essa enumeração de um controle de Propriedade ListBox, esse valor discreto é atribuído como o valor da propriedade.                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| text      | Público. Opcional. O texto usado para exibir o valor enumerado. A sintaxe permite uma cadeia de caracteres de exibição direta ou uma referência de cadeia de caracteres de exibição indireta; Use a cadeia de caracteres de exibição indireta para que ela possa ser localizada.                                                                                                                                                                                                                                                                                                                                                                                                   |
| mnemônico | **Windows 7 e posterior.** Público. Opcional. Uma lista de valores mnemônicos que podem ser usados para fazer referência à propriedade em consultas de pesquisa. A lista é delimitada com o \| caractere ' '.                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| name      | Obrigatórios. O nome da propriedade canônica, exclusivo para o sistema; por exemplo, System. rating. Esse atributo é limitado a 64 caracteres. O nome diferencia maiúsculas de minúsculas e deve usar a seguinte sintaxe: Publisher. Application. PropertyName. Os métodos a seguir retornam este valor: [**IExplorerCommand:: Getcanôniconame**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getcanonicalname), [**IPropertyDescription:: getcanôniconame**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname), [**IPropertyDescription2:: getcanônicaname**](/windows/desktop/api/Propsys/nn-propsys-ipropertydescription2)e [**IPropertyUI:: getcanônicaname**](/previous-versions/windows/desktop/legacy/dd758076(v=vs.85)). |



 

 

 
