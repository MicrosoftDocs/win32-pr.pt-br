---
description: O &lt; elemento folderType &gt; especifica um GUID para o tipo de pasta. Esse elemento será necessário se o &lt; elemento templateInfo &gt; existir, caso contrário, ele será opcional. Esse elemento não tem atributos e nenhum elemento filho.
title: Elemento folderType (esquema de biblioteca)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba9d0163a00ab525fb0a52267c1226b6a48230a4
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880862"
---
# <a name="foldertype-element-library-schema"></a>Elemento folderType (esquema de biblioteca)

O &lt; elemento folderType &gt; especifica um GUID para o tipo de pasta. Esse elemento será necessário se o &lt; elemento templateInfo &gt; existir, caso contrário, ele será opcional. Esse elemento não tem atributos e nenhum elemento filho.

## <a name="syntax"></a>Syntax


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a>Informações do elemento



| Elemento pai                                                           | Elementos filho |
|--------------------------------------------------------------------------|----------------|
| [Elemento templateInfo (esquema de biblioteca)](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a>Comentários

Definir um tipo de pasta determina as colunas e os detalhes que aparecem no Windows Explorer por padrão. Identificadores de tipo de pasta ([**FOLDERTYPEID**](foldertypeid.md)) são GUIDs definidos em Shlguid.h. A tabela a seguir lista os GUIDs de tipos de pasta comuns.



| Tipo de pasta      | GUID                                   |
|------------------|----------------------------------------|
| Biblioteca Genérica  | {5f4eab9a-6833-4f61-899d-31cf46979d49} |
| Bibliotecas de usuários  | {C4D98F09-6124-4fe0-9942-826416082DA9} |
| Pasta Documentos | {7D49D726-3C21-4F05-99AA-FDC2C9474656} |
| Pasta Imagens  | {B3690E58-E961-423B-B687-386EBFD83239} |
| Pasta Vídeos    | {5fa96407-7e77-483c-ac93-691d05850de8} |
| Pasta Jogos     | {b689b0d0-76d3-4cbb-87f7-585d0e0ce070} |
| Pasta Música     | {94d6ddcc-4a68-4175-a374-bd584a510b78} |
| Contatos         | {DE2B70EC-9BF7-4A93-BD3D-243F7881D492} |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Elemento iconReference (esquema de biblioteca)](schema-library-iconreference.md)
</dt> <dt>

[Elemento isLibraryPinned (esquema de biblioteca)](schema-library-islibrarypinned.md)
</dt> <dt>

[Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[Elemento name (esquema de biblioteca)](schema-library-name.md)
</dt> <dt>

[Elemento ownerSID (esquema de biblioteca)](schema-library-ownersid.md)
</dt> <dt>

[Elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md)
</dt> <dt>

[Elemento searchConnectorDescription (esquema de biblioteca)](schema-library-searchconnectordescription.md)
</dt> <dt>

[Elemento searchConnectorDescriptionList (esquema de biblioteca)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[Elemento templateInfo (esquema de biblioteca)](schema-library-templateinfo.md)
</dt> <dt>

[Elemento version (esquema de biblioteca)](schema-library-version.md)
</dt> </dl>

 

 



