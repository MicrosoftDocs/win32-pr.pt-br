---
description: Vários formatos de arquivo de imagem permitem armazenar metadados junto com uma imagem.
ms.assetid: 1eba4b91-bbf4-4f82-b2d7-65f331a84859
title: Constantes de marca de propriedade de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea9a6c3b8ea7ad9f0693032d3bc779bc414d9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967784"
---
# <a name="image-property-tag-constants"></a><span data-ttu-id="69651-103">Constantes de marca de propriedade de imagem</span><span class="sxs-lookup"><span data-stu-id="69651-103">Image Property Tag Constants</span></span>

<span data-ttu-id="69651-104">Vários formatos de arquivo de imagem permitem armazenar metadados junto com uma imagem.</span><span class="sxs-lookup"><span data-stu-id="69651-104">Several image file formats enable you to store metadata along with an image.</span></span> <span data-ttu-id="69651-105">Metadados são informações sobre uma imagem, por exemplo, título, largura, modelo de câmera e artista.</span><span class="sxs-lookup"><span data-stu-id="69651-105">Metadata is information about an image, for example, title, width, camera model, and artist.</span></span> <span data-ttu-id="69651-106">O Windows GDI+ fornece uma maneira uniforme de armazenar e recuperar metadados de arquivos de imagem nos formatos TIFF, JPEG, PNG (Portable Network Graphics) e EXIF (exchangable Image File).</span><span class="sxs-lookup"><span data-stu-id="69651-106">Windows GDI+ provides a uniform way of storing and retrieving metadata from image files in the Tagged Image File Format (TIFF), JPEG, Portable Network Graphics (PNG), and Exchangeable Image File (EXIF) formats.</span></span>

<span data-ttu-id="69651-107">No GDI+, um pedaço de metadados é chamado de *item de propriedade* e um item de propriedade individual é identificado por uma constante numérica chamada de *marca de propriedade*.</span><span class="sxs-lookup"><span data-stu-id="69651-107">In GDI+, a piece of metadata is called a *property item*, and an individual property item is identified by a numerical constant called a *property tag*.</span></span> <span data-ttu-id="69651-108">Você pode armazenar e recuperar metadados chamando os métodos [**Image:: SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) e [**Image:: GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) da classe [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) e não precisa se preocupar com os detalhes de como um formato de arquivo específico armazena esses metadados.</span><span class="sxs-lookup"><span data-stu-id="69651-108">You can store and retrieve metadata by calling the [**Image::SetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-setpropertyitem) and [**Image::GetPropertyItem**](/windows/desktop/api/Gdiplusheaders/nf-gdiplusheaders-image-getpropertyitem) methods of the [**Image**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-image) class, and you don't have to be concerned with the details of how a particular file format stores that metadata.</span></span>

<span data-ttu-id="69651-109">Os tópicos a seguir listam e descrevem os itens de propriedade com suporte no GDI+.</span><span class="sxs-lookup"><span data-stu-id="69651-109">The following topics list and describe the property items supported by GDI+.</span></span> <span data-ttu-id="69651-110">As descrições são breves e gerais para que se apliquem a uma variedade de formatos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="69651-110">The descriptions are brief and general so that they apply to a variety of file formats.</span></span> <span data-ttu-id="69651-111">Para obter uma descrição detalhada de como um item de propriedade é usado em um formato de arquivo específico, consulte a especificação para esse formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="69651-111">For a detailed description of how a property item is used in a particular file format, see the specification for that file format.</span></span> <span data-ttu-id="69651-112">Para obter links para várias especificações de formato de arquivo, consulte [especificações de formato de arquivo de imagem](-gdiplus-constant-image-file-format-specifications.md).</span><span class="sxs-lookup"><span data-stu-id="69651-112">For links to several file format specifications, see [Image File Format Specifications](-gdiplus-constant-image-file-format-specifications.md).</span></span> <span data-ttu-id="69651-113">Para obter mais informações sobre metadados, consulte constantes de [leitura e gravação de metadados](-gdiplus-reading-and-writing-metadata-use.md) e [**tipo de marca de propriedade de imagem**](-gdiplus-constant-image-property-tag-type-constants.md).</span><span class="sxs-lookup"><span data-stu-id="69651-113">For more information about metadata, see [Reading and Writing Metadata](-gdiplus-reading-and-writing-metadata-use.md) and [**Image Property Tag Type Constants**](-gdiplus-constant-image-property-tag-type-constants.md).</span></span>

-   [<span data-ttu-id="69651-114">Marcas de propriedade em ordem numérica</span><span class="sxs-lookup"><span data-stu-id="69651-114">Property Tags in Numerical Order</span></span>](-gdiplus-constant-property-tags-in-numerical-order.md)
-   [<span data-ttu-id="69651-115">Marcas de propriedade em ordem alfabética</span><span class="sxs-lookup"><span data-stu-id="69651-115">Property Tags in Alphabetical Order</span></span>](-gdiplus-constant-property-tags-in-alphabetical-order.md)
-   [<span data-ttu-id="69651-116">Descrições de item de propriedade</span><span class="sxs-lookup"><span data-stu-id="69651-116">Property Item Descriptions</span></span>](-gdiplus-constant-property-item-descriptions.md)

 

 



