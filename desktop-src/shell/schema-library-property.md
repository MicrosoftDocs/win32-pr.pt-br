---
description: O <property> elemento Especifica uma propriedade usada pela biblioteca. Essas propriedades são específicas para a biblioteca, portanto, não há nenhum conjunto predefinido de nomes de propriedade a ser usado. Esse elemento é opcional e não tem nenhum elemento filho.
ms.assetid: 8BF6EC7A-A87E-45fe-A8F0-4B49594E9E7B
title: Elemento Property (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b269e8914cf1f5da92d96e1922f7347a161daf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988754"
---
# <a name="property-element-library-schema"></a>Elemento Property (esquema de biblioteca)

O <property> elemento Especifica uma propriedade usada pela biblioteca. Essas propriedades são específicas para a biblioteca, portanto, não há nenhum conjunto predefinido de nomes de propriedade a ser usado. Esse elemento é opcional e não tem nenhum elemento filho.

## <a name="syntax"></a>Syntax

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



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
<th>Valores</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>name</td>
<td>Público. Obrigatórios. O nome para exibição da propriedade.</td>

</tr>
<tr class="even">
<td>tipo</td>
<td>Público. Obrigatórios. O tipo de propriedade.</td>
<td><ul>
<li>Any: padrão. O valor não será forçado pelo subsistema de propriedades. VT_NULL será retornado por getpropertytype.</li>
<li>NULL: não há nenhum valor para essa propriedade. VT_NULL será retornado por getpropertytype.</li>
<li>Cadeia de caracteres: o valor deve ser um VT_LPWSTR.</li>
<li>Booliano: o valor deve ser um VT_BOOL.</li>
<li>Byte: o valor deve ser um VT_UI1.</li>
<li>Buffer: o valor deve ser um VT_UI1 | Buffer de VT_VECTOR de bytes.</li>
<li>Int16: o valor deve ser um VT_I2.</li>
<li>UInt16: o valor deve ser um VT_UI2.</li>
<li>Int32: o valor deve ser um VT_I4.</li>
<li>UInt32: o valor deve ser um VT_UI4.</li>
<li>Int64: o valor deve ser um VT_I8.</li>
<li>UInt64: o valor deve ser um VT_UI8.</li>
<li>Double: o valor deve ser um VT_R8.</li>
<li>DateTime: o valor deve ser um VT_FILETIME.</li>
<li>GUID: o valor deve ser um VT_CLSID.</li>
<li>Blob: o valor deve ser um VT_BLOB.</li>
<li>Objeto: o valor deve ser um VT_UNKNOWN.</li>
<li>Stream: o valor deve ser um VT_STREAM.</li>
<li>Área de transferência: o valor deve ser um VT_CF.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Os requisitos para o elemento de> de nome canônico <correspondem aos requisitos do Windows Search e do sistema de propriedades do Windows. A cadeia de caracteres deve ser do tipo canônico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Esquema de descrição da biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquemas de propriedade](../properties/building-property-handlers-property-schemas.md)
</dt> <dt>

[Esquema de descrição do conector de pesquisa](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
