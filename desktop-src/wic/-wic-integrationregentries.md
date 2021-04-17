---
description: Este tópico aplica-se ao Windows Vista e posterior.
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: Integração com a Galeria de fotos do Windows e o Windows Explorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ab2bb725b151a069f53a94a8fb2e31766132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749495"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a><span data-ttu-id="5aed6-103">Integração com a Galeria de fotos do Windows e o Windows Explorer</span><span class="sxs-lookup"><span data-stu-id="5aed6-103">Integration with Windows Photo Gallery and Windows Explorer</span></span>

<span data-ttu-id="5aed6-104">Este tópico aplica-se ao Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="5aed6-104">This topic applies to Windows Vista and later.</span></span> <span data-ttu-id="5aed6-105">Ele contém as seções a seguir:</span><span class="sxs-lookup"><span data-stu-id="5aed6-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="5aed6-106">Introdução</span><span class="sxs-lookup"><span data-stu-id="5aed6-106">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="5aed6-107">Integração com o armazenamento de propriedades do Windows</span><span class="sxs-lookup"><span data-stu-id="5aed6-107">Integration with the Windows Property Store</span></span>](#integration-with-the-windows-property-store)
-   [<span data-ttu-id="5aed6-108">Integração com a Galeria de fotos do Windows</span><span class="sxs-lookup"><span data-stu-id="5aed6-108">Integration with the Windows Photo Gallery</span></span>](#integration-with-the-windows-photo-gallery)
-   [<span data-ttu-id="5aed6-109">Integração com o cache de miniaturas do Windows</span><span class="sxs-lookup"><span data-stu-id="5aed6-109">Integration with the Windows Thumbnail Cache</span></span>](#integration-with-the-windows-thumbnail-cache)
-   [<span data-ttu-id="5aed6-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5aed6-110">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="5aed6-111">Introdução</span><span class="sxs-lookup"><span data-stu-id="5aed6-111">Introduction</span></span>

<span data-ttu-id="5aed6-112">Para habilitar a Galeria de fotos do Windows e o Windows Explorer para exibir miniaturas e pesquisar e atualizar metadados de imagem padrão, um codec deve ter uma implementação das interfaces [manipuladordeminiaturai](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) e [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="5aed6-112">To enable Windows Photo Gallery and Windows Explorer to display thumbnails and search and update standard image metadata, a codec must have an implementation of the [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) and [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore) interfaces associated with it.</span></span> <span data-ttu-id="5aed6-113">A interface Manipuladordeminiaturai é usada para recuperar miniaturas e preencher o cache de miniaturas, e a interface IPropertyStore é usada para pesquisar e atualizar os metadados associados a um arquivo.</span><span class="sxs-lookup"><span data-stu-id="5aed6-113">The IThumbnailProvider interface is used to retrieve thumbnails and populate the thumbnail cache, and the IPropertyStore interface is used for searching and updating metadata associated with a file.</span></span> <span data-ttu-id="5aed6-114">A partir do Windows Vista, todos os tipos de arquivo têm miniaturas e metadados, mas tipos de arquivo diferentes exigem implementações diferentes dessas interfaces para recuperar ou gerar as miniaturas e os metadados para eles.</span><span class="sxs-lookup"><span data-stu-id="5aed6-114">As of Windows Vista, all file types have thumbnails and metadata, but different file types require different implementations of these interfaces to retrieve or generate the thumbnails and metadata for them.</span></span> <span data-ttu-id="5aed6-115">O sistema fornece implementações padrão dessas interfaces.</span><span class="sxs-lookup"><span data-stu-id="5aed6-115">The system provides default implementations of these interfaces.</span></span> <span data-ttu-id="5aed6-116">A implementação padrão de Manipuladordeminiaturai pode ser usada para qualquer formato de imagem habilitado para o Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="5aed6-116">The default implementation of IThumbnailProvider can be used for any Windows Imaging Component (WIC)–enabled image format.</span></span> <span data-ttu-id="5aed6-117">A implementação padrão de IPropertyStore pode ser usada com qualquer formato de imagem habilitado para WIC com base em um formato TIFF ou JPEG.</span><span class="sxs-lookup"><span data-stu-id="5aed6-117">The default implementation of IPropertyStore can be used with any WIC-enabled image format that is based on a Tagged Image File Format (TIFF) or JPEG container.</span></span> <span data-ttu-id="5aed6-118">Para associar seu formato de imagem às implementações padrão de ambas as interfaces, você deve adicionar apenas algumas entradas do registro.</span><span class="sxs-lookup"><span data-stu-id="5aed6-118">To associate your image format with the default implementations of both of these interfaces, you must add just a few registry entries.</span></span>

<span data-ttu-id="5aed6-119">As entradas a seguir indicam à galeria de fotos do Windows e ao Windows Explorer que uma extensão de nome de arquivo (. ext) e seu tipo MIME associado estão associados a um formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="5aed6-119">The following entries indicate to the Windows Photo Gallery and Windows Explorer that a file name extension (.ext) and its associated MIME type are associated with an image format.</span></span>

<span data-ttu-id="5aed6-120">A entrada a seguir indica ao Windows e aos aplicativos que usam o tipo de conteúdo (também conhecido como tipo MIME) que um arquivo com uma extensão específica (. ext) é um formato de imagem.</span><span class="sxs-lookup"><span data-stu-id="5aed6-120">The following entry indicates to Windows and applications that use content type (also known as mime type) that a file with a given extension (.ext) is an image format.</span></span> <span data-ttu-id="5aed6-121">O proprietário do tipo de arquivo precisa escolher um `<image sub type value>` que identifique exclusivamente o formato de arquivo e que esse valor de tipo de conteúdo precisa ser registrado no IANA.</span><span class="sxs-lookup"><span data-stu-id="5aed6-121">The file type owner needs to choose a `<image sub type value>` that uniquely identifies the file format and this content type value needs to be register with IANA.</span></span>

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

<span data-ttu-id="5aed6-122">A entrada a seguir indica o Windows, o Windows Search e os aplicativos que usam o [System. Kind](../properties/props-system-kind.md) que uma extensão de nome de arquivo (. ext) deve ser tratada como uma imagem.</span><span class="sxs-lookup"><span data-stu-id="5aed6-122">The following entry indicates to Windows, Windows search and applications that use [System.Kind](../properties/props-system-kind.md) that a file name extension (.ext) should be treated as a picture.</span></span> <span data-ttu-id="5aed6-123">Especificamente, isso indica que a propriedade System. Kind da extensão do arquivo deve ser definida como Picture.</span><span class="sxs-lookup"><span data-stu-id="5aed6-123">Specifically, it indicates that the file extension’s System.Kind property should be set to Picture.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     {.ext} = Picture
```

## <a name="integration-with-the-windows-property-store"></a><span data-ttu-id="5aed6-124">Integração com o armazenamento de propriedades do Windows</span><span class="sxs-lookup"><span data-stu-id="5aed6-124">Integration with the Windows Property Store</span></span>

<span data-ttu-id="5aed6-125">Às vezes, as mesmas propriedades de metadados são expostas em esquemas de metadados diferentes, geralmente com nomes de propriedade diferentes.</span><span class="sxs-lookup"><span data-stu-id="5aed6-125">Sometimes the same metadata properties are exposed in different metadata schemas, often with different property names.</span></span> <span data-ttu-id="5aed6-126">Quando uma dessas propriedades é atualizada, mas as outras não são, os metadados dentro do arquivo podem ficar fora de sincronia. O manipulador de propriedade de foto fornece a implementação de **IPropertyStore** padrão para imagens e é usado por aplicativos, bem como pela galeria de fotos do Windows e pelo Windows Explorer para garantir que todos os metadados em uma imagem permaneçam em sincronia e que as propriedades exibidas pelos aplicativos sejam consistentes com aquelas exibidas pela galeria de fotos do Windows e pelo Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="5aed6-126">When one of these properties is updated, but the others are not, the metadata within the file can get out of sync. The photo property handler provides the default **IPropertyStore** implementation for images, and is used by applications as well as by the Windows Photo Gallery and Windows Explorer to ensure that all the metadata in an image stays in sync, and that the properties displayed by applications are consistent with those displayed by the Windows Photo Gallery and Windows Explorer.</span></span> <span data-ttu-id="5aed6-127">Quando o manipulador de propriedades de foto atualiza metadados, ele garante que essas propriedades sejam atualizadas de forma consistente em todos os formatos de metadados comuns presentes no arquivo.</span><span class="sxs-lookup"><span data-stu-id="5aed6-127">When the photo property handler updates metadata, it makes sure that these properties are updated consistently across all the common metadata formats that are present in the file.</span></span>

<span data-ttu-id="5aed6-128">O manipulador de propriedade de foto deve entender o formato de contêiner e como localizar as várias propriedades dentro dele.</span><span class="sxs-lookup"><span data-stu-id="5aed6-128">The photo property handler must understand the container format and how to locate the various properties within it.</span></span> <span data-ttu-id="5aed6-129">Em geral, não é possível que o manipulador de propriedades fotográficas saiba como os vários blocos de metadados são dispostos em um formato de contêiner proprietário.</span><span class="sxs-lookup"><span data-stu-id="5aed6-129">In general, it isn’t possible for the photo property handler to know how the various metadata blocks are laid out in a proprietary container format.</span></span> <span data-ttu-id="5aed6-130">No entanto, se os metadados em seu formato de contêiner forem dispostos da mesma forma que os metadados em um formato de contêiner TIFF ou em um formato de contêiner JPEG, o manipulador de propriedade de foto também poderá aproveitar esse conhecimento para atualizar os metadados de forma consistente em seu formato de contêiner.</span><span class="sxs-lookup"><span data-stu-id="5aed6-130">However, if the metadata in your container format is laid out the same way as the metadata in either a TIFF container format or a JPEG container format, the photo property handler can take advantage of that knowledge to update metadata consistently in your container format as well.</span></span>

<span data-ttu-id="5aed6-131">Você pode registrar essa associação criando a seguinte entrada de registro.</span><span class="sxs-lookup"><span data-stu-id="5aed6-131">You can register this association by creating the following registry entry.</span></span> <span data-ttu-id="5aed6-132">Essa entrada notifica o manipulador de propriedades de foto que o formato de contêiner identificado por esse GUID compreende os mesmos caminhos de linguagem de consulta de metadados que o formato de contêiner com o GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3.</span><span class="sxs-lookup"><span data-stu-id="5aed6-132">This entry notifies the photo property handler that the container format identified by this GUID understands the same metadata query language paths as the container format with the GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3.</span></span> <span data-ttu-id="5aed6-133">(163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 é o GUID para o formato de contêiner TIFF.)</span><span class="sxs-lookup"><span data-stu-id="5aed6-133">(163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 is the GUID for the TIFF container format.)</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  ContainerAssociations
                     {Container Format GUID} = {163bcc30-e2e9-4f0b-961d-a3e9fdb788a3}
```

<span data-ttu-id="5aed6-134">A entrada a seguir associa a implementação padrão do Gerenciador de propriedades de fotos de **IPropertyStore** com arquivos que têm a extensão ". ext".</span><span class="sxs-lookup"><span data-stu-id="5aed6-134">The following entry associates the photo property handler’s default implementation of **IPropertyStore** with files that have the extension ".ext".</span></span> <span data-ttu-id="5aed6-135">O primeiro GUID é o IID da interface **IPropertyStore** e o segundo é o GUID da implementação do manipulador de propriedades fotográficas dele.</span><span class="sxs-lookup"><span data-stu-id="5aed6-135">The first GUID is the IID of the **IPropertyStore** interface, and the second is the GUID of the photo property handler’s implementation of it.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  {.ext}
                     (Default) = {a38b883c-1682-497e-97b0-0a3a9e801682}
```

<span data-ttu-id="5aed6-136">Os codecs que usam um formato proprietário que não é compatível com o formato de contêiner TIFF ou JPEG devem escrever sua própria implementação **IPropertyStore** .</span><span class="sxs-lookup"><span data-stu-id="5aed6-136">Codecs that use a proprietary format that is not compatible with either the TIFF or JPEG container format must write their own **IPropertyStore** implementation.</span></span>

## <a name="integration-with-the-windows-photo-gallery"></a><span data-ttu-id="5aed6-137">Integração com a Galeria de fotos do Windows</span><span class="sxs-lookup"><span data-stu-id="5aed6-137">Integration with the Windows Photo Gallery</span></span>

<span data-ttu-id="5aed6-138">A Galeria de fotos do Windows foi criada no WIC e pode exibir qualquer formato de imagem habilitado para WIC para o qual o codec está instalado.</span><span class="sxs-lookup"><span data-stu-id="5aed6-138">Windows Photo Gallery is built on WIC and can display any WIC-enabled image format for which the codec is installed.</span></span> <span data-ttu-id="5aed6-139">Para notificar o sistema de que seu formato de imagem pode ser aberto na Galeria de fotos do Windows, você precisa criar uma associação de arquivo criando as entradas de registro a seguir.</span><span class="sxs-lookup"><span data-stu-id="5aed6-139">To notify the system that your image format can be opened in Windows Photo Gallery, you need to create a file association by creating the following registry entries.</span></span>

```
HKEY_CLASSES_ROOT
   {.ext}
      (Default) = {ProgID} for example, jpegfile)
      OpenWithProgids
         {ProgID}
      OpenWithList
         PhotoViewer.dll
      ShellEx
         ContextMenuHandlers
            ShellImagePreview
               (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   SystemFileAssociations
      {.ext}
         OpenWithList
            PhotoViewer.dll
         ShellEx
            ContextMenuHandlers
               ShellImagePreview
                  (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   {Image Format ProgID}
      (Default) = Name of Image Format
      DefaultIcon
         (Default) = Path to icon for type, icon index
      shell
         open
            MuiVerb = @%PROGRAMFILES%\Windows Photo Gallery\photoviewer.dll,-3043
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%ProgramFiles%\Windows Photo Gallery\PhotoViewer.dll", ImageView_Fullscreen %1
            DropTarget
               Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
         printo
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%SystemRoot%\System32\shimgvw.dll", ImageView_PrintTo /pt "%1" "%2" "%3" "%4"
```

<span data-ttu-id="5aed6-140">O ProgID normalmente é a extensão de nome de arquivo anexada à palavra "File".</span><span class="sxs-lookup"><span data-stu-id="5aed6-140">The ProgID is usually the file name extension appended with the word "file".</span></span> <span data-ttu-id="5aed6-141">(Por exemplo, se a extensão de nome de arquivo for. txt, a ProgID normalmente seria "txtfile".)</span><span class="sxs-lookup"><span data-stu-id="5aed6-141">(For example, if the file name extension is .txt, the ProgID would usually be "txtfile".)</span></span>

<span data-ttu-id="5aed6-142">Há outras entradas de registro padrão que talvez você precise criar para dar suporte a associações de arquivo; no entanto, como the'y não são específicos do WIC, eles estão além do escopo deste tópico.</span><span class="sxs-lookup"><span data-stu-id="5aed6-142">There are other standard registry entries you may need to create to support file associations; however, because the’y are not specific to WIC, they are beyond the scope of this topic.</span></span>

## <a name="integration-with-the-windows-thumbnail-cache"></a><span data-ttu-id="5aed6-143">Integração com o cache de miniaturas do Windows</span><span class="sxs-lookup"><span data-stu-id="5aed6-143">Integration with the Windows Thumbnail Cache</span></span>

<span data-ttu-id="5aed6-144">As duas entradas a seguir indicam que a implementação do provedor de miniaturas do WIC padrão pode ser usada para recuperar miniaturas de arquivos com essa extensão.</span><span class="sxs-lookup"><span data-stu-id="5aed6-144">The following two entries indicate that the standard WIC thumbnail provider implementation can be used to retrieve thumbnails for files with this extension.</span></span> <span data-ttu-id="5aed6-145">O primeiro GUID é o IID da interface [manipuladordeminiaturai](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) e o segundo é o GUID da implementação do sistema padrão dessa interface.</span><span class="sxs-lookup"><span data-stu-id="5aed6-145">The first GUID is the IID of the [IThumbnailProvider](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) interface, and the second is the GUID of the standard system implementation of this interface.</span></span> <span data-ttu-id="5aed6-146">(Todas as entradas em HLCR \\ . ext \\ shellex \\ são repetidas em HKCR \\ SystemFileAssociations \\ . ext \\ shellex \\ .)</span><span class="sxs-lookup"><span data-stu-id="5aed6-146">(All entries under HLCR\\.ext\\ShellEx\\ are repeated under HKCR\\SystemFileAssociations\\.ext\\ShellEx\\.)</span></span>

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a><span data-ttu-id="5aed6-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5aed6-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5aed6-148">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="5aed6-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5aed6-149">Entradas de registro específicas do codificador</span><span class="sxs-lookup"><span data-stu-id="5aed6-149">Encoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)
</dt> <dt>

[<span data-ttu-id="5aed6-150">Instalação e registro de CODEC</span><span class="sxs-lookup"><span data-stu-id="5aed6-150">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="5aed6-151">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="5aed6-151">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="5aed6-152">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="5aed6-152">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
