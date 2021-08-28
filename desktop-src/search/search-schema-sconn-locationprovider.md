---
description: O elemento &lt; locationProvider &gt; opcional especifica o provedor de pesquisa a ser usado pelo conector de pesquisa do provedor de serviços Web. Esse elemento contém um atributo obrigatório e um elemento filho opcional.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Elemento locationProvider (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f049a01cc0c51075c147918a2f43b740000f2e36
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883366"
---
# <a name="locationprovider-element-search-connector-schema"></a>Elemento locationProvider (esquema do conector de pesquisa)

O elemento &lt; locationProvider &gt; opcional especifica o provedor de pesquisa a ser usado pelo conector de pesquisa do provedor de serviços Web. Esse elemento contém um atributo obrigatório e um elemento filho opcional.

## <a name="syntax"></a>Syntax


```
<!-- locationProvider -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="locationProvider" minOccurs="0">
                <xs:complexType>
                    <xs:all>
                        <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
                    </xs:all>
                <xs:attribute name="clsid" use="required"/>
                <xs:attribute name="codebase" type="xs:string"/>
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                                                                   | Elementos filho                                                                       |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)](search-schema-searchconnectordescription.md) | [Elemento propertyBag (esquema do conector de pesquisa)](search-schema-sconn-propertybag.md) |



 

## <a name="attributes"></a>Atributos



| Atributo | Descrição                                                    |
|-----------|----------------------------------------------------------------|
| @clsid    | Obrigatórios. O CLSID (identificador de classe) do provedor de pesquisa. |
| Codebase  | Opcional.                                                      |



 

## <a name="remarks"></a>Comentários

O valor do atributo para @clsid o provedor OpenSearch é {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.

Os conectores de pesquisa baseados no sistema de arquivos e no manipulador de protocolo podem usar o [ &lt; elemento simpleLocation. &gt; ](search-schema-sconn-simplelocation.md) Se &lt; locationProvider &gt; estiver presente, NÃO DEVERÁ haver um elemento &lt; simpleLocation &gt; na descrição do Conector de Pesquisa.

## <a name="example-of-a-locationprovider-element"></a>Exemplo de um elemento locationProvider


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



