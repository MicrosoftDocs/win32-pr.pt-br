---
description: Encoder-Specific entradas do registro
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Encoder-Specific entradas do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49e6fbfafa1f8d3b340d7e3864fddacb8cd7e282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788777"
---
# <a name="encoder-specific-registry-entries"></a><span data-ttu-id="8dfa1-103">Encoder-Specific entradas do registro</span><span class="sxs-lookup"><span data-stu-id="8dfa1-103">Encoder-Specific Registry Entries</span></span>


<span data-ttu-id="8dfa1-104">Além das entradas listadas acima para o codificador, você também deve registrar o codificador na categoria de codificadores do Windows Imaging Component (WIC) para que o mecanismo de descoberta possa encontrá-lo.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-104">In addition to the entries listed above for encoder, you must also register your encoder under the category of Windows Imaging Component (WIC) encoders so the discovery engine can find it.</span></span> <span data-ttu-id="8dfa1-105">Faça isso fazendo as seguintes entradas do registro.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-105">You do this by making the following registry entries.</span></span> <span data-ttu-id="8dfa1-106">O primeiro GUID nas entradas a seguir é o identificador de categoria (CATID) para WICBitmapEncoders.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-106">The first GUID in the following entries is the category identifier (CATID) for WICBitmapEncoders.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a><span data-ttu-id="8dfa1-107">Registrando um formato de contêiner com gravadores de metadados</span><span class="sxs-lookup"><span data-stu-id="8dfa1-107">Registering a Container Format with Metadata Writers</span></span>

<span data-ttu-id="8dfa1-108">Se você criar um novo formato de contêiner para o codec, também deverá criar entradas de registro para dar suporte a gravadores de metadados para os blocos de metadados em suas imagens.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-108">If you create a new container format for your codec, you must also create registry entries to support metadata writers for the metadata blocks in your images.</span></span> <span data-ttu-id="8dfa1-109">As entradas a seguir precisam ser criadas no identificador de classe (CLSID) do gravador de metadados para cada formato de metadados com suporte em seu formato de contêiner.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-109">The following entries need to be created under the class identifier (CLSID) of the metadata writer for each metadata format supported in your container format.</span></span> <span data-ttu-id="8dfa1-110">Se o seu codec usa um contêiner TIFF (Tagged Image File Format), essas informações já estão no registro e você não precisa criar essas entradas.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-110">If your codec uses a Tagged Image File Format (TIFF) container, then this information is already in the registry and you don't need to create these entries.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Writer CLSID}
         Containers
            {Container Format GUID}
               WritePosition = Offset relative to its container
               WriteHeader = Pattern used for metadata header
               WriteOffset = Offset from beginning of header
```

<span data-ttu-id="8dfa1-111">Se você usar um formato de contêiner TIFF ou estilo JPEG, deverá registrar uma associação entre o contêiner e esse formato de contêiner.</span><span class="sxs-lookup"><span data-stu-id="8dfa1-111">If you use a TIFF-style or JPEG-style container format, you must register an association between your container and that container format.</span></span> <span data-ttu-id="8dfa1-112">Para obter mais informações, consulte a introdução em [integração com a Galeria de fotos do Windows e o Windows Explorer](-wic-integrationregentries.md).</span><span class="sxs-lookup"><span data-stu-id="8dfa1-112">For more information, see the introduction in [Integration with Windows Photo Gallery and Windows Explorer](-wic-integrationregentries.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8dfa1-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8dfa1-113">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8dfa1-114">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="8dfa1-114">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8dfa1-115">Entradas gerais do registro</span><span class="sxs-lookup"><span data-stu-id="8dfa1-115">General Registry Entries</span></span>](-wic-generalregentries.md)
</dt> <dt>

[<span data-ttu-id="8dfa1-116">Entradas de registro específicas do codificador</span><span class="sxs-lookup"><span data-stu-id="8dfa1-116">Encoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)
</dt> <dt>

[<span data-ttu-id="8dfa1-117">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="8dfa1-117">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="8dfa1-118">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="8dfa1-118">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



