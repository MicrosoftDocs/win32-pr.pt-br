---
description: O <locationProvider> elemento opcional especifica o provedor de pesquisa a ser usado pelo conector de pesquisa do provedor de serviço Web. Esse elemento contém um atributo obrigatório e um elemento filho opcional.
ms.assetid: 5481b1ae-e166-4f09-bf0d-d6b7f7c8a331
title: Elemento LocationProvider (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c68732300c190b44b984bbe64ca031a81ced84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797615"
---
# <a name="locationprovider-element-search-connector-schema"></a>Elemento LocationProvider (esquema do conector de pesquisa)

O <locationProvider> elemento opcional especifica o provedor de pesquisa a ser usado pelo conector de pesquisa do provedor de serviço Web. Esse elemento contém um atributo obrigatório e um elemento filho opcional.

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
| @clsid    | Obrigatórios. O identificador de classe (CLSID) do provedor de pesquisa. |
| bases  | Opcional.                                                      |



 

## <a name="remarks"></a>Comentários

O @clsid valor do atributo para o provedor de OpenSearch é {48E277F6-4E74-4cd6-BA6F-FA4F42898223}.

Os conectores de pesquisa baseados no sistema de arquivos e no manipulador de protocolo podem usar o [<simpleLocation>](search-schema-sconn-simplelocation.md) elemento em vez disso. Se <locationProvider> estiver presente, não deverá haver um <simpleLocation> elemento na descrição do conector de pesquisa.

## <a name="example-of-a-locationprovider-element"></a>Exemplo de um elemento LocalProvider


```
<locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
        <property name="OpenSearchShortName">MSDN</property>
        <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
        <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
</locationProvider>
```



 

 



