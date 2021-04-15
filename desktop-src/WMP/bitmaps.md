---
title: Bitmaps (SDK do Windows Media Player)
description: Bitmaps
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Capas do Windows Media Player Mobile, bitmaps
- capas, bitmaps
- referência para capas, bitmaps
- bitmaps em capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad690b691c22154bad4db0981e2b5ab760400b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454495"
---
# <a name="bitmaps-windows-media-player-sdk"></a><span data-ttu-id="8cf84-107">Bitmaps (SDK do Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="8cf84-107">Bitmaps (Windows Media Player SDK)</span></span>

<span data-ttu-id="8cf84-108">Você deve usar uma ou mais imagens em sua capa e cada imagem deve ser definida no arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="8cf84-108">You must use one or more images in your skin, and each image must be defined in the skin definition file.</span></span> <span data-ttu-id="8cf84-109">Se você não definir uma imagem nesta seção, sua capa não será capaz de usá-la.</span><span class="sxs-lookup"><span data-stu-id="8cf84-109">If you do not define an image in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="8cf84-110">O termo "bitmap" é usado em toda a referência em um sentido genérico e refere-se a imagens de bitmap com uma extensão. bmp, imagens GIF com uma extensão. gif, imagens JPEG com uma extensão. jpg e imagens PNG com uma extensão. png.</span><span class="sxs-lookup"><span data-stu-id="8cf84-110">The term "bitmap" is used throughout the reference in a generic sense, and refers to bitmap images with a .bmp extension, GIF images with a .gif extension, JPEG images with a .jpg extension, and PNG images with a .png extension.</span></span>

<span data-ttu-id="8cf84-111">A seção bitmaps do arquivo de definição de capa começa com esta linha:</span><span class="sxs-lookup"><span data-stu-id="8cf84-111">The Bitmaps section of the skin definition file begins with this line:</span></span>


```C++
[ Bitmaps ]

```



<span data-ttu-id="8cf84-112">Em seguida, você deve adicionar uma ou mais linhas que contêm informações sobre cada uma das imagens em sua capa.</span><span class="sxs-lookup"><span data-stu-id="8cf84-112">You then must add one or more lines that contain information about each of the images in your skin.</span></span>

<span data-ttu-id="8cf84-113">Uma linha típica pode ser:</span><span class="sxs-lookup"><span data-stu-id="8cf84-113">A typical line might be:</span></span>


```C++
    Background  Background.bmp  0,0

```



<span data-ttu-id="8cf84-114">Você pode usar o modelo a seguir para a seção bitmaps do seu arquivo de definição de capa:</span><span class="sxs-lookup"><span data-stu-id="8cf84-114">You can use the following template for the Bitmaps section of your skin definition file:</span></span>


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



<span data-ttu-id="8cf84-115">Você deve usar a seguinte ordem para informações de bitmap para cada linha na seção de bitmap.</span><span class="sxs-lookup"><span data-stu-id="8cf84-115">You must use the following order for bitmap information for each line in the Bitmap section.</span></span> <span data-ttu-id="8cf84-116">Cada parte da linha é necessária.</span><span class="sxs-lookup"><span data-stu-id="8cf84-116">Each part of the line is required.</span></span>

1.  [<span data-ttu-id="8cf84-117">Tipo de bitmap</span><span class="sxs-lookup"><span data-stu-id="8cf84-117">Bitmap Type</span></span>](bitmap-type.md)
2.  [<span data-ttu-id="8cf84-118">Nome do Arquivo</span><span class="sxs-lookup"><span data-stu-id="8cf84-118">File Name</span></span>](file-name.md)
3.  [<span data-ttu-id="8cf84-119">Coordenadas</span><span class="sxs-lookup"><span data-stu-id="8cf84-119">Coordinates</span></span>](coordinates.md)

<span data-ttu-id="8cf84-120">Para obter um exemplo de código de bitmap, consulte a [seção bitmap de exemplo](sample-bitmap-section.md).</span><span class="sxs-lookup"><span data-stu-id="8cf84-120">For an example of bitmap code, see [Sample Bitmap Section](sample-bitmap-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8cf84-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8cf84-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8cf84-122">**Referência de capa**</span><span class="sxs-lookup"><span data-stu-id="8cf84-122">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




