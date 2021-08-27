---
description: O elemento <property> opcional especifica uma propriedade usada pelo conector de pesquisa. Essas propriedades são específicas para esse conector de pesquisa, portanto, não há um conjunto predefinido de nomes a ser usado. Esse elemento não tem elementos filho.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: elemento property de propertyStore (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0319e86674eb91bf8915ce6218bb387ac9d79e87
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122464993"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a>elemento property de propertyStore (esquema do conector de pesquisa)

O elemento <property> opcional especifica uma propriedade usada pelo conector de pesquisa. Essas propriedades são específicas para esse conector de pesquisa, portanto, não há um conjunto predefinido de nomes a ser usado. Esse elemento não tem elementos filho.

## <a name="syntax"></a>Sintaxe


```
<!-- property for propertyStore element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded">
            <xs:complexType>
                <xs:complexContent>
                    <xs:extension base="xs:anyType">
                        <xs:attribute name="name" type="canonical-name" use="required"/>
                        <xs:attribute name="type"/>
                    </xs:extension>
                </xs:complexContent>
            </xs:complexType>
        </xs:element>
    </xs:element>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                                           | Elementos filho |
|------------------------------------------------------------------------------------------|----------------|
| [Elemento propertyStore (esquema do conector de pesquisa)](search-schema-sconn-propertystore.md) |                |



 

## <a name="attributes"></a>Atributos




| Atributo | Descrição | Valores | 
|-----------|-------------|--------|
| name | Público. Obrigatórios. O nome para exibição da propriedade. |   | 
| tipo | Público. Obrigatórios. O tipo de propriedade. | Qualquer: padrão. O valor não será coercido pelo subsistema de propriedade. VT_NULL será retornado por GetPropertyType.<ul><li>Null: não há nenhum valor para essa propriedade. VT_NULL será retornado por GetPropertyType.</li><li>Cadeia de caracteres: o valor deve ser um VT_LPWSTR.</li><li>Booliana: o valor deve ser um VT_BOOL.</li><li>Byte: o valor deve ser um VT_UI1.</li><li>Buffer: o valor deve ser um VT_UI1 | VT_VECTOR buffer de bytes.</li><li>Int16: o valor deve ser um VT_I2.</li><li>UInt16: o valor deve ser um VT_UI2.</li><li>Int32: o valor deve ser um VT_I4.</li><li>UInt32: o valor deve ser um VT_UI4.</li><li>Int64: o valor deve ser um VT_I8.</li><li>UInt64: o valor deve ser um VT_UI8</li><li>Double: o valor deve ser um VT_R8.</li><li>DateTime: o valor deve ser um VT_FILETIME.</li><li>Guid: o valor deve ser um VT_CLSID.</li><li>Blob: o valor deve ser um VT_BLOB.</li><li>Objeto: o valor deve ser um VT_UNKNOWN.</li><li>Fluxo: o valor deve ser um VT_STREAM.</li><li>Área de transferência: o valor deve ser um VT_CF.</li></ul> | 
| esquema | Público. Opcional. O esquema em que a propriedade é definida. |   | 




 

## <a name="remarks"></a>Comentários

OpenSearch de pesquisa podem usar a propriedade OpenSearchHTMLRolloverTemplate. Essa propriedade identifica um modelo formatado seguindo a convenção OpenSearch modelo. O modelo OpenSearchHTMLRolloverTemplate é usado quando o usuário clica no botão "Pesquisar no site" na barra de comandos.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra <propertyStore> um elemento com dois <property> elementos.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



