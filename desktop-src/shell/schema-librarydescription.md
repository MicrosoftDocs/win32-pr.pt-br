---
description: O <libraryDescription> elemento é o contêiner de nível superior para a definição de biblioteca. Este elemento é obrigatório.
ms.assetid: 62098944-E1B2-46e8-AC87-314C55F96B62
title: Elemento libraryDescription (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 125cb01ce1bd38418c10f5b14ff7b28f64efba87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967473"
---
# <a name="librarydescription-element-library-schema"></a>Elemento libraryDescription (esquema de biblioteca)

O <libraryDescription> elemento é o contêiner de nível superior para a definição de biblioteca. Este elemento é obrigatório.

## <a name="syntax"></a>Syntax


```
<!-- libraryDescription -->
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema xmlns:xs="https://www.w3.org/2001/XMLSchema" elementFormDefault="qualified" attributeFormDefault="unqualified">
    <xs:include schemaLocation="commonTypes-ms.xsd"/>
    <xs:element name="libraryDescription">
        <xs:complexType>
            <xs:all>
                <xs:element name="name" type="xs:string"/>
                <xs:element name="ownerSID" minOccurs="0"/>
                <xs:element name="version" type="xs:int" minOccurs="0"/>
                <xs:element name="isLibraryPinned" type="xs:boolean" default="false" minOccurs="0"/>
                <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
                <xs:element name="propertyStore" minOccurs="0">
                    <xs:complexType>
                        <xs:complexContent>
                            <xs:extension base="propertyStoreType"/>
                        </xs:complexContent>
                    </xs:complexType>
                </xs:element>
                <xs:element name="templateInfo" minOccurs="0">
                    <xs:complexType>
                        <xs:all>
                            <xs:element name="folderType" minOccurs="0"/>
                        </xs:all>
                    </xs:complexType>
                </xs:element>
                <xs:element name="searchConnectorDescriptionList" minOccurs="0">
                    <xs:complexType>
                        <xs:sequence minOccurs="0">
                            <xs:element name="searchConnectorDescription" 
                             type="searchConnectorDescriptionType" minOccurs="0" 
                             maxOccurs="unbounded"/>
                        </xs:sequence>
                    </xs:complexType>
                </xs:element>
            </xs:all>
        </xs:complexType>
    </xs:element>
</xs:schema>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai | Elementos filho                                                                                                          |
|----------------|-------------------------------------------------------------------------------------------------------------------------|
|                | [elemento Name (esquema de biblioteca)](schema-library-name.md). Obrigatórios.                                                     |
|                | [elemento OwnerId (esquema de biblioteca)](schema-library-ownersid.md). Opcional.                                             |
|                | [elemento Version (esquema de biblioteca)](schema-library-version.md). Opcional.                                               |
|                | [elemento isLibraryPinned (esquema de biblioteca)](schema-library-islibrarypinned.md). Opcional.                               |
|                | [elemento iconReference (esquema de biblioteca)](schema-library-iconreference.md). Opcional.                                   |
|                | [elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md). Opcional.                                   |
|                | [elemento templateInfo (esquema de biblioteca)](schema-library-templateinfo.md). Opcional.                                     |
|                | [elemento searchConnectorDescriptionList (esquema de biblioteca)](schema-library-searchconnectordescriptionlist.md). Obrigatórios. |



 

## <a name="remarks"></a>Comentários

Cada biblioteca pode conter um ou mais locais que podem ser procurados ou pesquisados por um usuário usando o Windows Explorer. Os locais são definidos por conectores de pesquisa usando [<searchConnectorDescription>](schema-library-searchconnectordescription.md) elementos em um [<searchConnectorDescriptionList>](schema-library-searchconnectordescriptionlist.md) elemento de contêiner.

Uma biblioteca pode ter um conjunto exclusivo de propriedades, e os locais na biblioteca também podem ter conjuntos exclusivos de propriedades. Essas propriedades são definidas em [<property>](schema-library-property.md) elementos dentro de um [<propertyStore>](schema-library-propertystore.md) elemento de contêiner.

## <a name="example"></a>Exemplo


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
    <name>@shell32.dll,-34575</name>
    <ownerSID>S-1-5-21-379071477-2495173225-776587366-1000</ownerSID>
    <version>1</version>
    <isLibraryPinned>true</isLibraryPinned>
    <iconReference>imageres.dll,-1002</iconReference>
    <templateInfo>
        <folderType>{7d49d726-3c21-4f05-99aa-fdc2c9474656}</folderType>
    </templateInfo>
    <searchConnectorDescriptionList>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34577</description>
            <isDefaultSaveLocation>true</isDefaultSaveLocation>
            <simpleLocation>
                <url>knownfolder:{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</url>
                <serialized>MBAAAEAFCAAA...MFNVAAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34579</description>
            <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
            <simpleLocation>
                <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
                <serialized>MBAAAEAFCAAA...HJIfK9AAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
    </searchConnectorDescriptionList>
</libraryDescription>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Esquema de descrição da biblioteca](library-schema-entry.md)
</dt> <dt>

[Esquema de descrição do conector de pesquisa](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
