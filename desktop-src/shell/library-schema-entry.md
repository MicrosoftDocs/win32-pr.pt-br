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
# <a name="library-description-schema"></a><span data-ttu-id="a177c-103">Esquema de descrição da biblioteca</span><span class="sxs-lookup"><span data-stu-id="a177c-103">Library Description Schema</span></span>

<span data-ttu-id="a177c-104">Arquivos de descrição da biblioteca são arquivos XML que definem bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="a177c-104">Library description files are XML files that define libraries.</span></span> <span data-ttu-id="a177c-105">As bibliotecas agregam itens de locais de armazenamento local e remoto em uma única exibição no Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="a177c-105">Libraries aggregate items from local and remote storage locations into a single view in Windows Explorer.</span></span> <span data-ttu-id="a177c-106">Os arquivos de descrição da biblioteca seguem o esquema de Descrição da Biblioteca e são salvos como \* arquivos .library-ms.</span><span class="sxs-lookup"><span data-stu-id="a177c-106">Library description files follow the Library Description schema and are saved as \*.library-ms files.</span></span>

<span data-ttu-id="a177c-107">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="a177c-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="a177c-108">Visão geral do esquema de descrição da biblioteca</span><span class="sxs-lookup"><span data-stu-id="a177c-108">Overview of the Library Description Schema</span></span>](#overview-of-the-library-description-schema)
-   [<span data-ttu-id="a177c-109">Versão do namespace</span><span class="sxs-lookup"><span data-stu-id="a177c-109">Namespace Versioning</span></span>](#namespace-versioning)
-   [<span data-ttu-id="a177c-110">Exemplo de um arquivo de descrição da biblioteca</span><span class="sxs-lookup"><span data-stu-id="a177c-110">Example of a Library Description File</span></span>](#example-of-a-library-description-file)
-   [<span data-ttu-id="a177c-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a177c-111">Related topics</span></span>](#related-topics)

## <a name="overview-of-the-library-description-schema"></a><span data-ttu-id="a177c-112">Visão geral do esquema de descrição da biblioteca</span><span class="sxs-lookup"><span data-stu-id="a177c-112">Overview of the Library Description Schema</span></span>

<span data-ttu-id="a177c-113">As bibliotecas contêm arquivos armazenados em um ou mais locais de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a177c-113">Libraries contain files that are stored in one or more storage locations.</span></span> <span data-ttu-id="a177c-114">As bibliotecas não armazenam esses arquivos; Em vez disso, eles monitoram as pastas que contêm os arquivos e permitem que os usuários acessem e organizem os arquivos de maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="a177c-114">Libraries do not actually store these files; instead, they monitor the folders that contain the files, and let users access and arrange the files in different ways.</span></span> <span data-ttu-id="a177c-115">Por exemplo, um usuário pode ter arquivos de música em várias pastas em um disco rígido local e também em um disco rígido externo.</span><span class="sxs-lookup"><span data-stu-id="a177c-115">For example, a user can have music files in multiple folders on a local hard disk and also on an external hard disk.</span></span> <span data-ttu-id="a177c-116">Usando a **Biblioteca de** Música , o usuário pode acessar todos esses arquivos ao mesmo tempo e classificar todos eles por nome de artista ou título de álbum como um único grupo.</span><span class="sxs-lookup"><span data-stu-id="a177c-116">Using the **Music Library**, the user can access all of those files at the same time and sort them all by artist name or album title as a single group.</span></span>

<span data-ttu-id="a177c-117">O esquema de Descrição da Biblioteca consiste em três partes principais, descritas na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="a177c-117">The Library Description schema consists of three major parts, described in the following table:</span></span>



| <span data-ttu-id="a177c-118">Parte</span><span class="sxs-lookup"><span data-stu-id="a177c-118">Part</span></span>                        | <span data-ttu-id="a177c-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="a177c-119">Description</span></span>                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a177c-120">Informações gerais da biblioteca</span><span class="sxs-lookup"><span data-stu-id="a177c-120">General library information</span></span> | <span data-ttu-id="a177c-121">Informações sobre a biblioteca, como nome, proprietário, versão, ícone, que Windows Explorer pode usar quando exibe a biblioteca para um usuário.</span><span class="sxs-lookup"><span data-stu-id="a177c-121">Information about the library, such as name, owner, version, icon, that Windows Explorer can use when it displays the library to a user.</span></span>                   |
| <span data-ttu-id="a177c-122">Propriedades da biblioteca</span><span class="sxs-lookup"><span data-stu-id="a177c-122">Library properties</span></span>          | <span data-ttu-id="a177c-123">Uma ou mais propriedades que descrevem a biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a177c-123">One or more properties that describe the library.</span></span> <span data-ttu-id="a177c-124">Essas propriedades personalizadas são específicas da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a177c-124">These custom properties are specific to the library.</span></span>                                                     |
| <span data-ttu-id="a177c-125">Locais da biblioteca</span><span class="sxs-lookup"><span data-stu-id="a177c-125">Library locations</span></span>           | <span data-ttu-id="a177c-126">Um ou mais conectores de pesquisa que identificam os locais de armazenamento a incluir na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a177c-126">One or more search connectors that identify storage locations to include in the library.</span></span> <span data-ttu-id="a177c-127">Cada um desses locais também pode ter um conjunto exclusivo de propriedades.</span><span class="sxs-lookup"><span data-stu-id="a177c-127">Each of these locations can also have a unique set of properties.</span></span> |



 

<span data-ttu-id="a177c-128">Os arquivos de biblioteca Windows 7 são armazenados na pasta conhecida, Bibliotecas \_ FOLDERID.</span><span class="sxs-lookup"><span data-stu-id="a177c-128">Library files in Windows 7 are stored in the known folder, FOLDERID\_Libraries.</span></span> <span data-ttu-id="a177c-129">Por padrão, a pasta Bibliotecas FOLDERID está localizada \_ em %USERPROFILE% \\ AppData \\ Roaming \\ Microsoft Windows \\ \\ Bibliotecas.</span><span class="sxs-lookup"><span data-stu-id="a177c-129">By default, the FOLDERID\_Libraries folder is located at %USERPROFILE%\\AppData\\Roaming\\Microsoft\\Windows\\Libraries.</span></span>

## <a name="namespace-versioning"></a><span data-ttu-id="a177c-130">Versão do namespace</span><span class="sxs-lookup"><span data-stu-id="a177c-130">Namespace Versioning</span></span>

<span data-ttu-id="a177c-131">As versões do formato de arquivo Descrição da Biblioteca ( \* .library-ms) são controladas alterando o namespace .</span><span class="sxs-lookup"><span data-stu-id="a177c-131">Versions of the Library Description file format (\*.library-ms) are tracked by changing the namespace.</span></span> <span data-ttu-id="a177c-132">Por Windows 7, o formato de arquivo tem o seguinte namespace padrão: https://schemas.microsoft.com/windows/2009/library .</span><span class="sxs-lookup"><span data-stu-id="a177c-132">For Windows 7, the file format has the following default namespace: https://schemas.microsoft.com/windows/2009/library.</span></span>

<span data-ttu-id="a177c-133">No entanto, as versões do conteúdo da biblioteca são rastreadas usando o [<version>](schema-library-version.md) elemento em um arquivo de Descrição da Biblioteca específico.</span><span class="sxs-lookup"><span data-stu-id="a177c-133">Versions of the library contents, however, are tracked by using the [<version>](schema-library-version.md) element in a specific Library Description file.</span></span>

## <a name="example-of-a-library-description-file"></a><span data-ttu-id="a177c-134">Exemplo de um arquivo de descrição da biblioteca</span><span class="sxs-lookup"><span data-stu-id="a177c-134">Example of a Library Description File</span></span>

<span data-ttu-id="a177c-135">A seguir está um exemplo de um arquivo de Descrição da Biblioteca que define uma biblioteca para arquivos de documento.</span><span class="sxs-lookup"><span data-stu-id="a177c-135">The following is an example of a Library Description file that defines a library for document files.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="a177c-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a177c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a177c-137">Elemento folderType (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="a177c-137">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="a177c-138">Elemento iconReference (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="a177c-138">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="a177c-139">Elemento isLibraryPinned (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="a177c-139">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="a177c-140">Elemento libraryDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="a177c-140">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="a177c-141">Elemento name (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="a177c-141">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="a177c-142">Elemento ownerSID (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="a177c-142">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="a177c-143">Elemento property (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="a177c-143">property Element (Library Schema)</span></span>](schema-library-property.md)
</dt> <dt>

[<span data-ttu-id="a177c-144">Elemento propertyStore (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="a177c-144">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="a177c-145">Elemento searchConnectorDescription (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="a177c-145">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="a177c-146">Elemento searchConnectorDescriptionList (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="a177c-146">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="a177c-147">Elemento templateInfo (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="a177c-147">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="a177c-148">Elemento version (esquema de biblioteca)</span><span class="sxs-lookup"><span data-stu-id="a177c-148">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> <dt>

[<span data-ttu-id="a177c-149">Esquema de descrição do conector de pesquisa</span><span class="sxs-lookup"><span data-stu-id="a177c-149">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
