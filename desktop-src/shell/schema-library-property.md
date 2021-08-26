---
description: O <property> elemento especifica uma propriedade usada pela biblioteca. Essas propriedades são específicas da biblioteca, portanto, não há nenhum conjunto predefinido de nomes de propriedade a ser usado. Esse elemento é opcional e não tem elementos filho.
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: Elemento property (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481122db633750b042172561eedace81fe1d752e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468633"
---
# <a name="property-element-library-schema"></a>Elemento property (esquema de biblioteca)

O <property> elemento especifica uma propriedade usada pela biblioteca. Essas propriedades são específicas da biblioteca, portanto, não há nenhum conjunto predefinido de nomes de propriedade a ser usado. Esse elemento é opcional e não tem elementos filho.

## <a name="syntax"></a>Sintaxe

``` syntax
<!-- property -->
<xs:element name="property" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:complexContent>
            <xs:extension base="xs:anyType">
                <xs:attribute name="name" type="canonical-name" use="required"/>
                    <xs:simpleType name="canonical-name">
                        <xs:restriction base="xs:string">
                            <xs:maxLength value="63"/>
                            <xs:pattern value="[0-9A-Za-z.]*"/>
                        </xs:restriction>
                    </xs:simpleType>
                <xs:attribute name="type"/>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                             | Elementos filho |
|----------------------------------------------------------------------------|----------------|
| [Elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md) | Nenhum           |



 

## <a name="attributes"></a>Atributos




| Atributo | Descrição | Valores | 
|-----------|-------------|--------|
| name | Público. Obrigatórios. O nome para exibição da propriedade. | 
| tipo | Público. Obrigatórios. O tipo de propriedade. | <ul><li>Qualquer: padrão. O valor não será coercido pelo subsistema de propriedade. VT_NULL será retornado por GetPropertyType.</li><li>Null: não há nenhum valor para essa propriedade. VT_NULL será retornado por GetPropertyType.</li><li>Cadeia de caracteres: o valor deve ser um VT_LPWSTR.</li><li>Booliana: o valor deve ser um VT_BOOL.</li><li>Byte: o valor deve ser um VT_UI1.</li><li>Buffer: o valor deve ser um VT_UI1 | VT_VECTOR buffer de bytes.</li><li>Int16: o valor deve ser um VT_I2.</li><li>UInt16: o valor deve ser um VT_UI2.</li><li>Int32: o valor deve ser um VT_I4.</li><li>UInt32: o valor deve ser um VT_UI4.</li><li>Int64: o valor deve ser um VT_I8.</li><li>UInt64: o valor deve ser um VT_UI8.</li><li>Double: o valor deve ser um VT_R8.</li><li>DateTime: o valor deve ser um VT_FILETIME.</li><li>Guid: o valor deve ser um VT_CLSID.</li><li>Blob: o valor deve ser um VT_BLOB.</li><li>Objeto: o valor deve ser um VT_UNKNOWN.</li><li>Fluxo: o valor deve ser um VT_STREAM.</li><li>Área de transferência: o valor deve ser um VT_CF.</li></ul> | 




 

## <a name="remarks"></a>Comentários

Os requisitos para o <nome canônico> os requisitos para o Windows Search e o Windows de propriedade. A cadeia de caracteres deve ser do tipo canonical.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Esquema de descrição da biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquemas de propriedade](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[Esquema de descrição do conector de pesquisa](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
