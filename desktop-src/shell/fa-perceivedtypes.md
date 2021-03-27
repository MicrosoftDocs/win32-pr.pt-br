---
description: Um tipo percebido é uma categoria de tipos de arquivo que permite identificar o tipo de arquivo para Windows (e aplicativos) como sendo uma imagem, áudio, documento ou outro tipo.
title: Tipos observados (o Shell do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 56d4c495-a886-4723-88ca-5b7753398062
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e6136389c717fd4e27621a4d7f9f4cf2895c4116
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104989132"
---
# <a name="perceived-types-the-windows-shell"></a><span data-ttu-id="4e82c-103">Tipos observados (o Shell do Windows)</span><span class="sxs-lookup"><span data-stu-id="4e82c-103">Perceived Types (The Windows Shell)</span></span>

<span data-ttu-id="4e82c-104">Um tipo percebido é uma categoria de tipos de arquivo que permite identificar o tipo de arquivo para Windows (e aplicativos) como sendo uma imagem, áudio, documento ou outro tipo.</span><span class="sxs-lookup"><span data-stu-id="4e82c-104">A perceived type is a category of file types that lets you identify your file type to Windows (and applications) as being an image, audio, document, or other type.</span></span> <span data-ttu-id="4e82c-105">Os tipos observados são usados para várias finalidades, incluindo a determinação do tipo de pasta, que é usado para definir as configurações de exibição padrão.</span><span class="sxs-lookup"><span data-stu-id="4e82c-105">Perceived types are used for several purposes, including the determination of the folder type, which is then used to set the default view settings.</span></span> <span data-ttu-id="4e82c-106">Por exemplo, uma pasta cheia de arquivos que são da imagem do tipo percebido é atribuída a um modo de exibição padrão de miniaturas.</span><span class="sxs-lookup"><span data-stu-id="4e82c-106">For example, a folder full of files that are of the perceived type image is assigned a default view mode of thumbnails.</span></span>

<span data-ttu-id="4e82c-107">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="4e82c-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="4e82c-108">Sobre tipos observados</span><span class="sxs-lookup"><span data-stu-id="4e82c-108">About Perceived Types</span></span>](#about-perceived-types)
-   [<span data-ttu-id="4e82c-109">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="4e82c-109">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="4e82c-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e82c-110">Related topics</span></span>](#related-topics)

## <a name="about-perceived-types"></a><span data-ttu-id="4e82c-111">Sobre tipos observados</span><span class="sxs-lookup"><span data-stu-id="4e82c-111">About Perceived Types</span></span>

<span data-ttu-id="4e82c-112">Os tipos observados, definidos como valores percebido, são semelhantes aos tipos de arquivo, exceto pelo fato de que eles se referem a categorias amplas de tipos de formato de arquivo em vez de tipos de arquivo específicos.</span><span class="sxs-lookup"><span data-stu-id="4e82c-112">Perceived types, defined as PerceivedType values, are similar to file types except that they refer to broad categories of file format types rather than specific file types.</span></span> <span data-ttu-id="4e82c-113">Por exemplo, imagem, texto, áudio e compactado são tipos percebidos.</span><span class="sxs-lookup"><span data-stu-id="4e82c-113">For example, image, text, audio, and compressed are perceived types.</span></span> <span data-ttu-id="4e82c-114">Os tipos de arquivo (geralmente tipos de arquivo públicos) podem ser atribuídos a um tipo percebido e sempre devem ser atribuídos um sempre que houver um que seja apropriado.</span><span class="sxs-lookup"><span data-stu-id="4e82c-114">File types (generally public file types) can be assigned a perceived type, and should always be assigned one whenever there is one that is appropriate.</span></span> <span data-ttu-id="4e82c-115">Por exemplo, o arquivo de imagem Types. bmp,. png,. jpg e. gif também são da imagem de tipo percebida.</span><span class="sxs-lookup"><span data-stu-id="4e82c-115">For example, the image file types .bmp, .png, .jpg, and .gif are also of perceived type image.</span></span>

<span data-ttu-id="4e82c-116">Os tipos observados padrão são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="4e82c-116">The default perceived types are as follows:</span></span>

-   <span data-ttu-id="4e82c-117">Pasta</span><span class="sxs-lookup"><span data-stu-id="4e82c-117">Folder</span></span>
-   <span data-ttu-id="4e82c-118">Texto</span><span class="sxs-lookup"><span data-stu-id="4e82c-118">Text</span></span>
-   <span data-ttu-id="4e82c-119">Imagem</span><span class="sxs-lookup"><span data-stu-id="4e82c-119">Image</span></span>
-   <span data-ttu-id="4e82c-120">Áudio</span><span class="sxs-lookup"><span data-stu-id="4e82c-120">Audio</span></span>
-   <span data-ttu-id="4e82c-121">Vídeo</span><span class="sxs-lookup"><span data-stu-id="4e82c-121">Video</span></span>
-   <span data-ttu-id="4e82c-122">Compressed</span><span class="sxs-lookup"><span data-stu-id="4e82c-122">Compressed</span></span>
-   <span data-ttu-id="4e82c-123">Documento</span><span class="sxs-lookup"><span data-stu-id="4e82c-123">Document</span></span>
-   <span data-ttu-id="4e82c-124">Sistema</span><span class="sxs-lookup"><span data-stu-id="4e82c-124">System</span></span>
-   <span data-ttu-id="4e82c-125">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4e82c-125">Application</span></span>
-   <span data-ttu-id="4e82c-126">Gamemedia</span><span class="sxs-lookup"><span data-stu-id="4e82c-126">Gamemedia</span></span>
-   <span data-ttu-id="4e82c-127">Contatos</span><span class="sxs-lookup"><span data-stu-id="4e82c-127">Contacts</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e82c-128">Recursos adicionais</span><span class="sxs-lookup"><span data-stu-id="4e82c-128">Additional Resources</span></span>

-   <span data-ttu-id="4e82c-129">Para obter informações sobre como registrar tipos observados, consulte [registro de aplicativo](app-registration.md).</span><span class="sxs-lookup"><span data-stu-id="4e82c-129">For information about how to register perceived types, see [Application Registration](app-registration.md).</span></span>
-   <span data-ttu-id="4e82c-130">Para obter uma lista de tipos observados padrão, consulte a enumeração [**percebida**](/windows/win32/api/shtypes/ne-shtypes-perceived) .</span><span class="sxs-lookup"><span data-stu-id="4e82c-130">For a list of default perceived types, see the [**PERCEIVED**](/windows/win32/api/shtypes/ne-shtypes-perceived) enumeration.</span></span>
-   <span data-ttu-id="4e82c-131">Para recuperar o tipo percebido de um arquivo com base em sua extensão de nome de arquivo, consulte a função [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) .</span><span class="sxs-lookup"><span data-stu-id="4e82c-131">To retrieves a file's perceived type based on its file name extension, see the [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e82c-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e82c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e82c-133">registro de Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4e82c-133">Application Registration</span></span>](app-registration.md)
</dt> <dt>

[<span data-ttu-id="4e82c-134">Tipos de arquivo</span><span class="sxs-lookup"><span data-stu-id="4e82c-134">File Types</span></span>](fa-file-types.md)
</dt> <dt>

[<span data-ttu-id="4e82c-135">Como funcionam as associações de arquivo</span><span class="sxs-lookup"><span data-stu-id="4e82c-135">How File Associations Work</span></span>](fa-how-work.md)
</dt> <dt>

[<span data-ttu-id="4e82c-136">Exibição de conteúdo por tipo de arquivo ou tipo</span><span class="sxs-lookup"><span data-stu-id="4e82c-136">Content View By File Type or Kind</span></span>](prophand-content-view.md)
</dt> <dt>

[<span data-ttu-id="4e82c-137">Verificador de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="4e82c-137">File Type Verifier</span></span>](file-type-verifier.md)
</dt> <dt>

[<span data-ttu-id="4e82c-138">Manipuladores de tipo de arquivo</span><span class="sxs-lookup"><span data-stu-id="4e82c-138">File Type Handlers</span></span>](fa-file-extensions.md)
</dt> <dt>

[<span data-ttu-id="4e82c-139">Identificadores programáticos</span><span class="sxs-lookup"><span data-stu-id="4e82c-139">Programmatic Identifiers</span></span>](fa-progids.md)
</dt> <dt>

[<span data-ttu-id="4e82c-140">Matrizes de associação</span><span class="sxs-lookup"><span data-stu-id="4e82c-140">Association Arrays</span></span>](fa-associationarray.md)
</dt> </dl>

 

 



