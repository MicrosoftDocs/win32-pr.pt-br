---
description: O &lt; &gt; elemento searchConnectorDescriptionType é o contêiner de nível superior para a definição do conector de pesquisa.
ms.assetid: a6b45864-210d-4099-804d-7548fd8eb562
title: Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f89621ab34f65fb3c3b1f8e88bbdc8dca246b8d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885075"
---
# <a name="searchconnectordescriptiontype-element-search-connector-schema"></a>Elemento searchConnectorDescriptionType (esquema do conector de pesquisa)

O &lt; &gt; elemento searchConnectorDescriptionType é o contêiner de nível superior para a definição do conector de pesquisa.

-   [Sintaxe](#syntax)
-   [Informações do elemento](#element-information)
-   [Atributos](#attributes)
-   [Comentários](#remarks)
-   [Exemplo de um arquivo de descrição do conector de pesquisa](#example-of-a-search-connector-description-file)
-   [Tópicos relacionados](#related-topics)

## <a name="syntax"></a>Syntax


```
<!-- searchConnectorDescriptionType -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
   <xs:complexType name="searchConnectorDescriptionType">
      <xs:all>
         <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isDefaultSaveLocation" type="xs:boolean" minOccurs="0"/>
         <xs:element name="isDefaultNonOwnerSaveLocation" type="xs:boolean" minOccurs="0"/
         <xs:element name="description" type="xs:string" minOccurs="0"/>
         <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
         <xs:element name="imageLink" minOccurs="0">
            <xs:complexType>
               <xs:sequence>
                  <xs:element name="url" type="xs:anyURI"/>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="author" type="xs:string" minOccurs="0"/>
         <xs:element name="dateCreated" type="xs:dateTime" minOccurs="0"/>
         <xs:element name="templateInfo" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="folderType" minOccurs="0"/>
               </xs:all>
            </xs:complexType>
         </xs:element>
         <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0"/>
         <xs:element name="locationProvider" minOccurs="0">
            <xs:complexType>
               <xs:all>
                  <xs:element name="propertyBag" type="propertyStoreType" minOccurs="0"/>
               </xs:all>
               <xs:attribute name="clsid" use="required"/>
               <xs:attribute name="codebase" type="xs:string"/>
            </xs:complexType>
         </xs:element>
         <xs:element name="scope" minOccurs="0">
            <xs:complexType>
               <xs:sequence minOccurs="0">
                  <xs:element name="scopeItem" maxOccurs="unbounded">
                     <xs:complexType>
                        <xs:all>
                           <xs:element name="mode" default="Include">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Include"/>
                                    <xs:enumeration value="Exclude"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="depth" default="Shallow" minOccurs="0">
                              <xs:simpleType>
                                 <xs:restriction base="xs:string">
                                    <xs:enumeration value="Shallow"/>
                                    <xs:enumeration value="Deep"/>
                                 </xs:restriction>
                              </xs:simpleType>
                           </xs:element>
                           <xs:element name="url" type="xs:anyURI"/>
                        </xs:all>
                     </xs:complexType>
                  </xs:element>
               </xs:sequence>
            </xs:complexType>
         </xs:element>
         <xs:element name="propertyStore" type="propertyStoreType" minOccurs="0"/>
         <xs:element name="includeInStartMenuScope" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="domain" type="xs:string" minOccurs="0"/>
         <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
         <xs:element name="isIndexed" type="xs:boolean" minOccurs="0"/>
      </xs:all>
      <xs:attribute name="publisher" type="xs:string"/>
      <xs:attribute name="product" type="xs:string"/>
   </xs:complexType>
</xs:schema>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai | Elementos filho                                                                                                           |
|----------------|--------------------------------------------------------------------------------------------------------------------------|
|                | [Elemento isSearchOnlyItem (esquema do conector de pesquisa)](search-schema-sconn-issearchonlyitem.md)                           |
|                | [Elemento isDefaultSaveLocation (esquema do conector de pesquisa)](search-schema-sconn-isdefaultsavelocation.md)                 |
|                | [Elemento isDefaultNonOwnerSaveLocation (esquema do conector de pesquisa)](search-schema-sconn-isdefaultnonownersavelocation.md) |
|                | [Elemento Description (esquema do conector de pesquisa)](search-schema-sconn-description.md)                                     |
|                | [Elemento iconReference (esquema do conector de pesquisa)](search-schema-sconn-iconreference.md)                                 |
|                | [Elemento imageLink (esquema do conector de pesquisa)](search-schema-sconn-imagelink.md)                                         |
|                | [Elemento Author (esquema do conector de pesquisa)](search-schema-sconn-author.md)                                               |
|                | [Elemento dateCreated (esquema do conector de pesquisa)](search-schema-sconn-datecreated.md)                                     |
|                | [Elemento templateInfo (esquema do conector de pesquisa)](search-schema-sconn-templateinfo.md)                                   |
|                | [Elemento LocationProvider (esquema do conector de pesquisa)](search-schema-sconn-locationprovider.md)                           |
|                | [Elemento Scope (esquema do conector de pesquisa)](search-schema-sconn-scope.md)                                                 |
|                | [Elemento propertyStore (esquema do conector de pesquisa)](search-schema-sconn-propertystore.md)                                 |
|                | [Elemento includeInStartMenuScope (esquema do conector de pesquisa)](search-schema-sconn-includeinstartmenuscope.md)             |
|                | [Elemento Domain (esquema do conector de pesquisa)](search-schema-sconn-domain.md)                                               |
|                | [Elemento supportsAdvancedQuerySyntax (esquema do conector de pesquisa)](search-schema-sconn-supportsadvancedquerysyntax.md)     |
|                | [Elemento IsIndexed (esquema do conector de pesquisa)](search-schema-sconn-isindexed.md)                                         |



 

## <a name="attributes"></a>Atributos



| Atributo | Descrição                                                                      |
|-----------|----------------------------------------------------------------------------------|
| publicador | Opcional. O nome de exibição do Publicador que fornece o conector de pesquisa.      |
| product   | Opcional. O nome de exibição do produto ao qual o conector de pesquisa se aplica. |



 

## <a name="remarks"></a>Comentários

Os conectores de pesquisa para pesquisa federada não podem ser usados em bibliotecas. O esquema para conectores de pesquisa de biblioteca é uma extensão do esquema descrito aqui e inclui informações específicas para bibliotecas.

## <a name="example-of-a-search-connector-description-file"></a>Exemplo de um arquivo de descrição do conector de pesquisa

Veja a seguir um exemplo de um arquivo de descrição do conector de pesquisa para um serviço Web de pesquisa federado.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
  <description>Search MSDN. Powered by live.com</description>
  <isSearchOnlyItem>true</isSearchOnlyItem>
  <domain>https://social.msdn.microsoft.com</domain>
  <supportsAdvancedQuerySyntax>false</supportsAdvancedQuerySyntax>
  <templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
  </templateInfo>
  <propertyStore>
    <property name="OpenSearchHTMLRolloverTemplate">https://social.msdn.microsoft.com/Search/?Query={searchTerms}</property>
  </propertyStore>
  <locationProvider clsid="{48E277F6-4E74-4cd6-BA6F-FA4F42898223}">
    <propertyBag>
      <property name="OpenSearchShortName">MSDN</property>
      <property name="OpenSearchQueryTemplate">https://social.msdn.microsoft.com/Search/Feed.aspx?locale=en-US&Query={searchTerms}&format=RSS&StartIndex={startIndex}</property>
      <property name="MaximumResultCount" type="uint32">100</property>
    </propertyBag>
  </locationProvider>
</searchConnectorDescription>
```



Veja a seguir um exemplo de um arquivo de descrição do conector de pesquisa para um manipulador de protocolo MAPI.


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    <description>Microsoft Outlook</description>
    <isSearchOnlyItem>true</isSearchOnlyItem>
    <includeInStartMenuScope>true</includeInStartMenuScope>
    <templateInfo>
        <folderType>{91475FE5-586B-4EBA-8D75-D17434B8CDF6}</folderType>
    </templateInfo>
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
</searchConnectorDescription>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Referência**
</dt> <dt>

[Visão geral do esquema de descrição do conector de pesquisa](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Pesquisa federada no Windows](-search-federated-search-overview.md)
</dt> </dl>

 

 



