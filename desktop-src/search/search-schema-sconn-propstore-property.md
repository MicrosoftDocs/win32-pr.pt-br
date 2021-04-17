---
description: O <property> elemento opcional especifica uma propriedade usada pelo conector de pesquisa. Essas propriedades são específicas para esse conector de pesquisa, portanto, não há nenhum conjunto predefinido de nomes a ser usado. Este elemento não tem elementos filho.
ms.assetid: 33854123-d4c0-4385-910b-a32d6922423f
title: Elemento Property de propertyStore (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2e4cee6f26ee65ba03d9225eafcea4a03a7c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501455"
---
# <a name="property-element-of-propertystore-search-connector-schema"></a>Elemento Property de propertyStore (esquema do conector de pesquisa)

O <property> elemento opcional especifica uma propriedade usada pelo conector de pesquisa. Essas propriedades são específicas para esse conector de pesquisa, portanto, não há nenhum conjunto predefinido de nomes a ser usado. Este elemento não tem elementos filho.

## <a name="syntax"></a>Syntax


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
<td> </td>
</tr>
<tr class="even">
<td>tipo</td>
<td>Público. Obrigatórios. O tipo de propriedade.</td>
<td>Any: padrão. O valor não será forçado pelo subsistema de propriedades. VT_NULL será retornado por getpropertytype.
<ul>
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
<li>UInt64: o valor deve ser um VT_UI8</li>
<li>Double: o valor deve ser um VT_R8.</li>
<li>DateTime: o valor deve ser um VT_FILETIME.</li>
<li>GUID: o valor deve ser um VT_CLSID.</li>
<li>Blob: o valor deve ser um VT_BLOB.</li>
<li>Objeto: o valor deve ser um VT_UNKNOWN.</li>
<li>Stream: o valor deve ser um VT_STREAM.</li>
<li>Área de transferência: o valor deve ser um VT_CF.</li>
</ul></td>
</tr>
<tr class="odd">
<td>schema</td>
<td>Público. Opcional. O esquema onde a propriedade é definida.</td>
<td> </td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Os conectores de pesquisa do OpenSearch podem usar a propriedade OpenSearchHTMLRolloverTemplate. Essa propriedade identifica um modelo que é formatado após a Convenção do modelo OpenSearch. O modelo OpenSearchHTMLRolloverTemplate é usado quando o usuário clica no botão "Pesquisar no site" na barra de comandos.

## <a name="example"></a>Exemplo

O exemplo a seguir mostra um <propertyStore> elemento com dois <property> elementos.


```
<propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://www.adventureworks.com/Search/?Query={searchTerms}</property>
    <property name="isExternal" type="boolean">true</property>
</propertyStore>
```



 

 



