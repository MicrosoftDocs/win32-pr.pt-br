---
description: 'Os métodos Image:: Save Methods e Image:: SaveAdd Methods da classe Image recebem um objeto EncoderParameters que contém uma matriz de objetos EncoderParameter.'
ms.assetid: babc89f0-aea5-4341-8cf9-40d11e73fb10
title: Constantes do codificador de imagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8130b90ad7f1d559ca480a581a0b157ff152fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165475"
---
# <a name="image-encoder-constants"></a><span data-ttu-id="f6e8c-103">Constantes do codificador de imagem</span><span class="sxs-lookup"><span data-stu-id="f6e8c-103">Image Encoder Constants</span></span>

<span data-ttu-id="f6e8c-104">Os métodos [Image:: Save Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) e [Image:: SaveAdd Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) da classe [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) recebem um objeto [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) que contém uma matriz de objetos [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) .</span><span class="sxs-lookup"><span data-stu-id="f6e8c-104">The [Image::Save Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-save(inistream_inconstclsid_inconstencoderparameters)) and [Image::SaveAdd Methods](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-image-saveadd(inimage_inconstencoderparameters)) methods of the [**Image**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-image) class receive an [**EncoderParameters**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameters) object that contains an array of [**EncoderParameter**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-encoderparameter) objects.</span></span> <span data-ttu-id="f6e8c-105">Cada objeto **EncoderParameter** tem um membro de dados GUID que especifica a categoria de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f6e8c-105">Each **EncoderParameter** object has a GUID data member that specifies the parameter category.</span></span> <span data-ttu-id="f6e8c-106">As constantes a seguir, definidas em Gdiplusimaging. h, representam GUIDs que especificam as várias categorias de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f6e8c-106">The following constants, defined in Gdiplusimaging.h, represent GUIDs that specify the various parameter categories.</span></span>

-   <span data-ttu-id="f6e8c-107">EncoderChrominanceTable</span><span class="sxs-lookup"><span data-stu-id="f6e8c-107">EncoderChrominanceTable</span></span>
-   <span data-ttu-id="f6e8c-108">EncoderColorDepth</span><span class="sxs-lookup"><span data-stu-id="f6e8c-108">EncoderColorDepth</span></span>
-   <span data-ttu-id="f6e8c-109">EncoderColorSpace</span><span class="sxs-lookup"><span data-stu-id="f6e8c-109">EncoderColorSpace</span></span>
-   <span data-ttu-id="f6e8c-110">EncoderCompression</span><span class="sxs-lookup"><span data-stu-id="f6e8c-110">EncoderCompression</span></span>
-   <span data-ttu-id="f6e8c-111">EncoderLuminanceTable</span><span class="sxs-lookup"><span data-stu-id="f6e8c-111">EncoderLuminanceTable</span></span>
-   <span data-ttu-id="f6e8c-112">EncoderQuality</span><span class="sxs-lookup"><span data-stu-id="f6e8c-112">EncoderQuality</span></span>
-   <span data-ttu-id="f6e8c-113">EncoderRenderMethod</span><span class="sxs-lookup"><span data-stu-id="f6e8c-113">EncoderRenderMethod</span></span>
-   <span data-ttu-id="f6e8c-114">EncoderSaveFlag</span><span class="sxs-lookup"><span data-stu-id="f6e8c-114">EncoderSaveFlag</span></span>
-   <span data-ttu-id="f6e8c-115">EncoderScanMethod</span><span class="sxs-lookup"><span data-stu-id="f6e8c-115">EncoderScanMethod</span></span>
-   <span data-ttu-id="f6e8c-116">EncoderTransformation</span><span class="sxs-lookup"><span data-stu-id="f6e8c-116">EncoderTransformation</span></span>
-   <span data-ttu-id="f6e8c-117">EncoderVersion</span><span class="sxs-lookup"><span data-stu-id="f6e8c-117">EncoderVersion</span></span>
-   <span data-ttu-id="f6e8c-118">EncoderImageItems</span><span class="sxs-lookup"><span data-stu-id="f6e8c-118">EncoderImageItems</span></span>
-   <span data-ttu-id="f6e8c-119">EncoderSaveAsCMYK</span><span class="sxs-lookup"><span data-stu-id="f6e8c-119">EncoderSaveAsCMYK</span></span>

 

 
