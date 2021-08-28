---
description: Os arquivos de descrição da biblioteca são arquivos XML que definem bibliotecas.
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: Esquema de descrição da biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfbaa8401468a6bab79cf4bccc5d7d4cd0ff7bb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879642"
---
# <a name="library-description-schema"></a>Esquema de descrição da biblioteca

Os arquivos de descrição da biblioteca são arquivos XML que definem bibliotecas. as bibliotecas agregam itens de locais de armazenamento local e remoto em uma única exibição no Windows Explorer. Os arquivos de descrição da biblioteca seguem o esquema de descrição da biblioteca e são salvos como \* arquivos. Library-MS.

Este tópico contém as seguintes seções:

-   [Visão geral do esquema de descrição da biblioteca](#overview-of-the-library-description-schema)
-   [Controle de versão do namespace](#namespace-versioning)
-   [Exemplo de um arquivo de descrição de biblioteca](#example-of-a-library-description-file)
-   [Tópicos relacionados](#related-topics)

## <a name="overview-of-the-library-description-schema"></a>Visão geral do esquema de descrição da biblioteca

As bibliotecas contêm arquivos que são armazenados em um ou mais locais de armazenamento. As bibliotecas não armazenam esses arquivos de fato; em vez disso, eles monitoram as pastas que contêm os arquivos e permitem que os usuários acessem e organizem os arquivos de maneiras diferentes. Por exemplo, um usuário pode ter arquivos de música em várias pastas em um disco rígido local e também em um disco rígido externo. Usando a **biblioteca de músicas**, o usuário pode acessar todos esses arquivos ao mesmo tempo e classificá-los por nome de artista ou título de álbum como um único grupo.

O esquema de descrição da biblioteca consiste em três partes principais, descritas na tabela a seguir:



| Parte                        | Descrição                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Informações gerais da biblioteca | informações sobre a biblioteca, como nome, proprietário, versão, ícone, que Windows Explorer pode usar quando ele exibe a biblioteca para um usuário.                   |
| Propriedades da biblioteca          | Uma ou mais propriedades que descrevem a biblioteca. Essas propriedades personalizadas são específicas para a biblioteca.                                                     |
| Locais de biblioteca           | Um ou mais conectores de pesquisa que identificam os locais de armazenamento a serem incluídos na biblioteca. Cada um desses locais também pode ter um conjunto exclusivo de propriedades. |



 

os arquivos de biblioteca no Windows 7 são armazenados na pasta conhecida, nas \_ bibliotecas folderid. por padrão, a pasta de \_ bibliotecas folderid está localizada em% USERPROFILE% \\ AppData \\ roaming \\ Microsoft \\ Windows \\ library.

## <a name="namespace-versioning"></a>Controle de versão do namespace

As versões do formato de arquivo de descrição da biblioteca ( \* . Library-MS) são rastreadas alterando o namespace. para Windows 7, o formato de arquivo tem o seguinte namespace padrão: https://schemas.microsoft.com/windows/2009/library .

As versões do conteúdo da biblioteca, no entanto, são rastreadas usando o elemento [ &lt; version &gt; ](schema-library-version.md) em um arquivo de descrição de biblioteca específico.

## <a name="example-of-a-library-description-file"></a>Exemplo de um arquivo de descrição de biblioteca

Veja a seguir um exemplo de um arquivo de descrição de biblioteca que define uma biblioteca para arquivos de documentos.


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

[Elemento FolderType (esquema de biblioteca)](schema-library-foldertype.md)
</dt> <dt>

[Elemento iconReference (esquema de biblioteca)](schema-library-iconreference.md)
</dt> <dt>

[Elemento isLibraryPinned (esquema de biblioteca)](schema-library-islibrarypinned.md)
</dt> <dt>

[Elemento libraryDescription (esquema de biblioteca)](schema-librarydescription.md)
</dt> <dt>

[Elemento Name (esquema de biblioteca)](schema-library-name.md)
</dt> <dt>

[Elemento OwnerId (esquema de biblioteca)](schema-library-ownersid.md)
</dt> <dt>

[Elemento Property (esquema de biblioteca)](schema-library-property.md)
</dt> <dt>

[Elemento propertyStore (esquema de biblioteca)](schema-library-propertystore.md)
</dt> <dt>

[Elemento searchConnectorDescription (esquema de biblioteca)](schema-library-searchconnectordescription.md)
</dt> <dt>

[Elemento searchConnectorDescriptionList (esquema de biblioteca)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[Elemento templateInfo (esquema de biblioteca)](schema-library-templateinfo.md)
</dt> <dt>

[Elemento Version (esquema de biblioteca)](schema-library-version.md)
</dt> <dt>

[Esquema de descrição do conector de pesquisa](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
