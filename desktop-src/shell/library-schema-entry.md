---
description: Arquivos de descrição da biblioteca são arquivos XML que definem bibliotecas.
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: Esquema de descrição da biblioteca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a6da99820e81c55e5d705c72d4d0509ea271a4a
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581734"
---
# <a name="library-description-schema"></a>Esquema de descrição da biblioteca

Arquivos de descrição da biblioteca são arquivos XML que definem bibliotecas. As bibliotecas agregam itens de locais de armazenamento local e remoto em uma única exibição no Windows Explorer. Os arquivos de descrição da biblioteca seguem o esquema de Descrição da Biblioteca e são salvos como \* arquivos .library-ms.

Este tópico contém as seguintes seções:

-   [Visão geral do esquema de descrição da biblioteca](#overview-of-the-library-description-schema)
-   [Versão do namespace](#namespace-versioning)
-   [Exemplo de um arquivo de descrição da biblioteca](#example-of-a-library-description-file)
-   [Tópicos relacionados](#related-topics)

## <a name="overview-of-the-library-description-schema"></a>Visão geral do esquema de descrição da biblioteca

As bibliotecas contêm arquivos armazenados em um ou mais locais de armazenamento. As bibliotecas não armazenam esses arquivos; Em vez disso, eles monitoram as pastas que contêm os arquivos e permitem que os usuários acessem e organizem os arquivos de maneiras diferentes. Por exemplo, um usuário pode ter arquivos de música em várias pastas em um disco rígido local e também em um disco rígido externo. Usando a **Biblioteca de** Música , o usuário pode acessar todos esses arquivos ao mesmo tempo e classificar todos eles por nome de artista ou título de álbum como um único grupo.

O esquema de Descrição da Biblioteca consiste em três partes principais, descritas na tabela a seguir:



| Parte                        | Descrição                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Informações gerais da biblioteca | Informações sobre a biblioteca, como nome, proprietário, versão, ícone, que Windows Explorer pode usar quando exibe a biblioteca para um usuário.                   |
| Propriedades da biblioteca          | Uma ou mais propriedades que descrevem a biblioteca. Essas propriedades personalizadas são específicas da biblioteca.                                                     |
| Locais da biblioteca           | Um ou mais conectores de pesquisa que identificam os locais de armazenamento a incluir na biblioteca. Cada um desses locais também pode ter um conjunto exclusivo de propriedades. |



 

Os arquivos de biblioteca Windows 7 são armazenados na pasta conhecida, Bibliotecas \_ FOLDERID. Por padrão, a pasta Bibliotecas FOLDERID está localizada \_ em %USERPROFILE% \\ AppData \\ Roaming \\ Microsoft Windows \\ \\ Bibliotecas.

## <a name="namespace-versioning"></a>Versão do namespace

As versões do formato de arquivo Descrição da Biblioteca ( \* .library-ms) são controladas alterando o namespace . Por Windows 7, o formato de arquivo tem o seguinte namespace padrão: https://schemas.microsoft.com/windows/2009/library .

No entanto, as versões do conteúdo da biblioteca são rastreadas usando o [<version>](schema-library-version.md) elemento em um arquivo de Descrição da Biblioteca específico.

## <a name="example-of-a-library-description-file"></a>Exemplo de um arquivo de descrição da biblioteca

A seguir está um exemplo de um arquivo de Descrição da Biblioteca que define uma biblioteca para arquivos de documento.


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

[Elemento folderType (esquema de biblioteca)](schema-library-foldertype.md)
</dt> <dt>

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

[Elemento property (esquema de biblioteca)](schema-library-property.md)
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
</dt> <dt>

[Esquema de descrição do conector de pesquisa](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
