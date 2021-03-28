---
description: O Windows GDI+ fornece a classe Image e a classe bitmap para armazenar imagens na memória e manipular imagens na memória.
ms.assetid: f9a5b4b1-4e25-42c8-a96b-a3104841e5f3
title: Usando codificadores de imagem e decodificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c55c75e00b3d624d27ba888ae26afb3a5ee0fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090322"
---
# <a name="using-image-encoders-and-decoders"></a><span data-ttu-id="2357a-103">Usando codificadores de imagem e decodificadores</span><span class="sxs-lookup"><span data-stu-id="2357a-103">Using Image Encoders and Decoders</span></span>

<span data-ttu-id="2357a-104">O Windows GDI+ fornece a classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e a classe [**bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) para armazenar imagens na memória e manipular imagens na memória.</span><span class="sxs-lookup"><span data-stu-id="2357a-104">Windows GDI+ provides the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class and the [**Bitmap**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-bitmap) class for storing images in memory and manipulating images in memory.</span></span> <span data-ttu-id="2357a-105">O GDI+ grava imagens em arquivos de disco com a ajuda de codificadores de imagem e carrega imagens de arquivos de disco com a ajuda de decodificadores de imagem.</span><span class="sxs-lookup"><span data-stu-id="2357a-105">GDI+ writes images to disk files with the help of image encoders and loads images from disk files with the help of image decoders.</span></span> <span data-ttu-id="2357a-106">Um codificador converte os dados em um objeto de **imagem** ou **bitmap** em um formato de arquivo de disco designado.</span><span class="sxs-lookup"><span data-stu-id="2357a-106">An encoder translates the data in an **Image** or **Bitmap** object into a designated disk file format.</span></span> <span data-ttu-id="2357a-107">Um decodificador traduz os dados em um arquivo de disco para o formato exigido pelos objetos **Image** e **bitmap** .</span><span class="sxs-lookup"><span data-stu-id="2357a-107">A decoder translates the data in a disk file to the format required by the **Image** and **Bitmap** objects.</span></span> <span data-ttu-id="2357a-108">O GDI+ tem codificadores internos e decodificadores que dão suporte aos seguintes tipos de arquivo:</span><span class="sxs-lookup"><span data-stu-id="2357a-108">GDI+ has built-in encoders and decoders that support the following file types:</span></span>

-   <span data-ttu-id="2357a-109">BMP</span><span class="sxs-lookup"><span data-stu-id="2357a-109">BMP</span></span>
-   <span data-ttu-id="2357a-110">GIF</span><span class="sxs-lookup"><span data-stu-id="2357a-110">GIF</span></span>
-   <span data-ttu-id="2357a-111">JPEG</span><span class="sxs-lookup"><span data-stu-id="2357a-111">JPEG</span></span>
-   <span data-ttu-id="2357a-112">PNG</span><span class="sxs-lookup"><span data-stu-id="2357a-112">PNG</span></span>
-   <span data-ttu-id="2357a-113">TIFF</span><span class="sxs-lookup"><span data-stu-id="2357a-113">TIFF</span></span>

<span data-ttu-id="2357a-114">O GDI+ também tem decodificadores internos que dão suporte aos seguintes tipos de arquivo:</span><span class="sxs-lookup"><span data-stu-id="2357a-114">GDI+ also has built-in decoders that support the following file types:</span></span>

-   <span data-ttu-id="2357a-115">WINDOWS MANAGEMENT FRAMEWORK</span><span class="sxs-lookup"><span data-stu-id="2357a-115">WMF</span></span>
-   <span data-ttu-id="2357a-116">EMF</span><span class="sxs-lookup"><span data-stu-id="2357a-116">EMF</span></span>
-   <span data-ttu-id="2357a-117">ICON</span><span class="sxs-lookup"><span data-stu-id="2357a-117">ICON</span></span>

<span data-ttu-id="2357a-118">Os tópicos a seguir abordam os codificadores e decodificadores mais detalhadamente:</span><span class="sxs-lookup"><span data-stu-id="2357a-118">The following topics discuss encoders and decoders in more detail:</span></span>

-   [<span data-ttu-id="2357a-119">Listando codificadores instalados</span><span class="sxs-lookup"><span data-stu-id="2357a-119">Listing Installed Encoders</span></span>](-gdiplus-listing-installed-encoders-use.md)
-   [<span data-ttu-id="2357a-120">Listando decodificadores instalados</span><span class="sxs-lookup"><span data-stu-id="2357a-120">Listing Installed Decoders</span></span>](-gdiplus-listing-installed-decoders-use.md)
-   [<span data-ttu-id="2357a-121">Recuperando o identificador de classe para um codificador</span><span class="sxs-lookup"><span data-stu-id="2357a-121">Retrieving the Class Identifier for an Encoder</span></span>](-gdiplus-retrieving-the-class-identifier-for-an-encoder-use.md)
-   [<span data-ttu-id="2357a-122">Determinando os parâmetros com suporte de um codificador</span><span class="sxs-lookup"><span data-stu-id="2357a-122">Determining the Parameters Supported by an Encoder</span></span>](-gdiplus-determining-the-parameters-supported-by-an-encoder-use.md)
-   [<span data-ttu-id="2357a-123">Convertendo uma imagem BMP em uma imagem PNG</span><span class="sxs-lookup"><span data-stu-id="2357a-123">Converting a BMP Image to a PNG Image</span></span>](-gdiplus-converting-a-bmp-image-to-a-png-image-use.md)
-   [<span data-ttu-id="2357a-124">Definindo o nível de compactação JPEG</span><span class="sxs-lookup"><span data-stu-id="2357a-124">Setting JPEG Compression Level</span></span>](-gdiplus-setting-jpeg-compression-level-use.md)
-   [<span data-ttu-id="2357a-125">Transformando uma imagem JPEG sem perda de informações</span><span class="sxs-lookup"><span data-stu-id="2357a-125">Transforming a JPEG Image Without Loss of Information</span></span>](-gdiplus-transforming-a-jpeg-image-without-loss-of-information-use.md)
-   [<span data-ttu-id="2357a-126">Criar e salvar uma imagem de vários quadros</span><span class="sxs-lookup"><span data-stu-id="2357a-126">Creating and Saving a Multiple-Frame Image</span></span>](-gdiplus-creating-and-saving-a-multiple-frame-image-use.md)
-   [<span data-ttu-id="2357a-127">Copiando quadros individuais de uma imagem de Multiple-Frame</span><span class="sxs-lookup"><span data-stu-id="2357a-127">Copying Individual Frames from a Multiple-Frame Image</span></span>](-gdiplus-copying-individual-frames-from-a-multiple-frame-image-use.md)

 

 



