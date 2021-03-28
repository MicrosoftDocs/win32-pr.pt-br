---
description: O <searchConnectorDescription> elemento é o elemento contêiner de nível superior de uma definição de conector de pesquisa.
ms.assetid: 383CAA20-56CA-4bdc-AC79-E57A1D59785C
title: Elemento searchConnectorDescription (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa6c213d43a648ebea51b58b4c3103a0ee42f13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968130"
---
# <a name="searchconnectordescription-element-library-schema"></a><span data-ttu-id="91ec7-103">Elemento searchConnectorDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="91ec7-103">searchConnectorDescription Element (Library Schema)</span></span>

<span data-ttu-id="91ec7-104">O <searchConnectorDescription> elemento é o elemento contêiner de nível superior de uma definição de conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="91ec7-104">The <searchConnectorDescription> element is the top level container element of a search connector definition.</span></span> <span data-ttu-id="91ec7-105">O <searchConnectorDescription> elemento é uma extensão do <searchConnectorDescriptionType> tipo de elemento associado aos conectores de pesquisa federada do Windows; no entanto, não é possível incluir conectores de pesquisa para a pesquisa federada do Windows ou manipuladores de protocolo em uma biblioteca.</span><span class="sxs-lookup"><span data-stu-id="91ec7-105">The <searchConnectorDescription> element is an extension of the <searchConnectorDescriptionType> element type associated with Windows Federated Search connectors; however, you cannot include search connectors for Windows Federated Search or protocol handlers in a library.</span></span>

## <a name="syntax"></a><span data-ttu-id="91ec7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="91ec7-106">Syntax</span></span>

``` syntax
<!-- searchConnectorDescription -->
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

## <a name="element-information"></a><span data-ttu-id="91ec7-107">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="91ec7-107">Element Information</span></span>

<span data-ttu-id="91ec7-108">Consulte a documentação do esquema no [Windows Search](/previous-versions/bb268030(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="91ec7-108">Refer to the schema documentation in [Windows Search](/previous-versions/bb268030(v=msdn.10))</span></span>



| <span data-ttu-id="91ec7-109">Elemento pai</span><span class="sxs-lookup"><span data-stu-id="91ec7-109">Parent Element</span></span>                                                                                               | <span data-ttu-id="91ec7-110">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="91ec7-110">Child Elements</span></span>                        |
|--------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [<span data-ttu-id="91ec7-111">Elemento searchConnectorDescriptionList (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="91ec7-111">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md) | <span data-ttu-id="91ec7-112"><isSearchOnlyI. tem></span><span class="sxs-lookup"><span data-stu-id="91ec7-112"><isSearchOnlyI.tem></span></span>             |
|                                                                                                              | <description>                   |
|                                                                                                              | <iconReference>                 |
|                                                                                                              | <imageLink>                     |
|                                                                                                              | <author>                        |
|                                                                                                              | <dateCreated>                   |
|                                                                                                              | <templateInfo>                  |
|                                                                                                              | <locationProvider>              |
|                                                                                                              | <scope>                         |
|                                                                                                              | <propertyStore>                 |
|                                                                                                              | <domain>                        |
|                                                                                                              | <supportsAdvancedQuerySyntax>   |
|                                                                                                              | <isDefaultSaveLocation>         |
|                                                                                                              | <isDefaultNonOwnerSaveLocation> |
|                                                                                                              | <isIndexed>                     |
|                                                                                                              | <simpleLocation>                |
|                                                                                                              | <includeInStartMenu>            |



 

## <a name="attributes"></a><span data-ttu-id="91ec7-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="91ec7-113">Attributes</span></span>



| <span data-ttu-id="91ec7-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="91ec7-114">Attribute</span></span> | <span data-ttu-id="91ec7-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="91ec7-115">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="91ec7-116">editor</span><span class="sxs-lookup"><span data-stu-id="91ec7-116">publisher</span></span> | <span data-ttu-id="91ec7-117">Opcional.</span><span class="sxs-lookup"><span data-stu-id="91ec7-117">Optional.</span></span> <span data-ttu-id="91ec7-118">O nome de exibição do Publicador que fornece o conector de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="91ec7-118">The display name of the publisher providing the search connector.</span></span>      |
| <span data-ttu-id="91ec7-119">product</span><span class="sxs-lookup"><span data-stu-id="91ec7-119">product</span></span>   | <span data-ttu-id="91ec7-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="91ec7-120">Optional.</span></span> <span data-ttu-id="91ec7-121">O nome de exibição do produto ao qual o conector de pesquisa se aplica.</span><span class="sxs-lookup"><span data-stu-id="91ec7-121">The display name of the product to which the search connector applies.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="91ec7-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="91ec7-122">Remarks</span></span>

<span data-ttu-id="91ec7-123">O <searchConnectorDescription> elemento de uma biblioteca usa a mesma definição de esquema do <searchConnectorDescription> para a pesquisa federada do Windows.</span><span class="sxs-lookup"><span data-stu-id="91ec7-123">The <searchConnectorDescription> element of a library uses the same schema definition as the <searchConnectorDescription> for Windows Federated Search.</span></span> <span data-ttu-id="91ec7-124">Embora eles usem os mesmos esquemas, os conectores de pesquisa para a pesquisa federada do Windows não podem ser incluídos em uma biblioteca.</span><span class="sxs-lookup"><span data-stu-id="91ec7-124">Although they use the same schemas, search connectors for Windows Federated search cannot be included in a library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91ec7-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="91ec7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91ec7-126">Esquema de descrição da biblioteca</span><span class="sxs-lookup"><span data-stu-id="91ec7-126">Library Description Schema</span></span>](library-schema-entry.md)
</dt> <dt>

[<span data-ttu-id="91ec7-127">Esquema de descrição do conector de pesquisa</span><span class="sxs-lookup"><span data-stu-id="91ec7-127">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
