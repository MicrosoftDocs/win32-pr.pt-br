---
description: O <property> elemento opcional especifica as propriedades usadas pelo provedor de localização.
ms.assetid: c1120dea-cb0b-4746-a5c1-4c83cda6dd7c
title: Elemento de Propriedade do LocalProvider (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71081b8b04ec999daa90958a29708b8efc64bee0
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "105763941"
---
# <a name="property-element-of-locationprovider-search-connector-schema"></a>Elemento de Propriedade do LocalProvider (esquema do conector de pesquisa)

O <property> elemento opcional especifica as propriedades usadas pelo provedor de localização. Essas propriedades são específicas para esse provedor de localização, portanto, não há nenhum conjunto predefinido de nomes a ser usado. O <property> elemento tem dois atributos, conforme descrito neste tópico.

## <a name="syntax"></a>Syntax


```
<!-- property element -->
    <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0">
        <xs:element name="property" minOccurs="0" maxOccurrs="unbounded"/>
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



## <a name="property-element-information"></a><property> Informações do elemento



| Elemento pai                                                                                 | Elementos filho                     |
|------------------------------------------------------------------------------------------------|------------------------------------|
| [Elemento LocationProvider (esquema do conector de pesquisa)](search-schema-sconn-locationprovider.md) | , descrita neste tópico. |



 


## <a name="property-attributes"></a><property> Atributos



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
<td>Obrigatórios. O nome para exibição da propriedade.</td>
<td> </td>
</tr>
<tr class="even">
<td>tipo</td>
<td>Obrigatórios. O tipo de propriedade.</td>
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
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Para o provedor de OpenSearch, as seguintes propriedades são usadas:

-   OpenSearchShortName: nome curto do serviço de pesquisa
-   OpenSearchQueryTemplate: modelo, formatado após a Convenção do modelo de OpenSearch, para o serviço de consulta
-   MaximumResultCount: (número) número máximo de resultados retornados pelo serviço de pesquisa
-   LinkIsFilePath: (booliano) se true, o provedor tentará interpretar os itens retornados como arquivos, usando suas extensões para criar o ShellItem apropriado na exibição. Se for false, os itens serão tratados como atalhos de URL.

 

 



