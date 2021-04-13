---
description: Define uma cor de material básica que pode ser aplicada a uma malha completa ou a faces individuais de uma malha. A potência é o expoente especular do material.
ms.assetid: vs|directx_sdk|~\material.htm
title: Material
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54c13d201152350a8a61950bb609f73cbdb2a3aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456370"
---
# <a name="material"></a><span data-ttu-id="62e7f-104">Material</span><span class="sxs-lookup"><span data-stu-id="62e7f-104">Material</span></span>

<span data-ttu-id="62e7f-105">Define uma cor de material básica que pode ser aplicada a uma malha completa ou a faces individuais de uma malha.</span><span class="sxs-lookup"><span data-stu-id="62e7f-105">Defines a basic material color that can be applied to either a complete mesh or a mesh's individual faces.</span></span> <span data-ttu-id="62e7f-106">A potência é o expoente especular do material.</span><span class="sxs-lookup"><span data-stu-id="62e7f-106">The power is the specular exponent of the material.</span></span>

``` syntax
template Material
{
    < 3D82AB4D-62DA-11CF-AB39-0020AF71E433 >
    ColorRGBA faceColor;
    FLOAT power;
    ColorRGB specularColor;
    ColorRGB emissiveColor;
    [...]
} 
```

<span data-ttu-id="62e7f-107">Em que:</span><span class="sxs-lookup"><span data-stu-id="62e7f-107">Where:</span></span>

-   <span data-ttu-id="62e7f-108">faceColor-face de cor.</span><span class="sxs-lookup"><span data-stu-id="62e7f-108">faceColor - Face color.</span></span> <span data-ttu-id="62e7f-109">Um modelo ColorRGBA.</span><span class="sxs-lookup"><span data-stu-id="62e7f-109">A ColorRGBA template.</span></span> <span data-ttu-id="62e7f-110">Consulte [**ColorRGBA**](colorrgba.md).</span><span class="sxs-lookup"><span data-stu-id="62e7f-110">See [**ColorRGBA**](colorrgba.md).</span></span>
-   <span data-ttu-id="62e7f-111">expoente de cor do especular de material de energia.</span><span class="sxs-lookup"><span data-stu-id="62e7f-111">power - Material specular color exponent.</span></span>
-   <span data-ttu-id="62e7f-112">specularColor-cor especular de material.</span><span class="sxs-lookup"><span data-stu-id="62e7f-112">specularColor - Material specular color.</span></span> <span data-ttu-id="62e7f-113">Um modelo ColorRGB.</span><span class="sxs-lookup"><span data-stu-id="62e7f-113">A ColorRGB template.</span></span> <span data-ttu-id="62e7f-114">Consulte [**colorRGB**](colorrgb.md).</span><span class="sxs-lookup"><span data-stu-id="62e7f-114">See [**ColorRGB**](colorrgb.md).</span></span>
-   <span data-ttu-id="62e7f-115">emissiveColor-material emissiva Color.</span><span class="sxs-lookup"><span data-stu-id="62e7f-115">emissiveColor - Material emissive color.</span></span> <span data-ttu-id="62e7f-116">Um modelo ColorRGB.</span><span class="sxs-lookup"><span data-stu-id="62e7f-116">A ColorRGB template.</span></span> <span data-ttu-id="62e7f-117">Consulte [**colorRGB**](colorrgb.md).</span><span class="sxs-lookup"><span data-stu-id="62e7f-117">See [**ColorRGB**](colorrgb.md).</span></span>

> [!Note]  
> <span data-ttu-id="62e7f-118">A cor do ambiente requer um componente alfa.</span><span class="sxs-lookup"><span data-stu-id="62e7f-118">The ambient color requires an alpha component.</span></span>

 

<span data-ttu-id="62e7f-119">[**TextureFilename**](texturefilename.md) é um objeto de dados opcional.</span><span class="sxs-lookup"><span data-stu-id="62e7f-119">[**TextureFilename**](texturefilename.md) is an optional data object.</span></span> <span data-ttu-id="62e7f-120">Se esse objeto não estiver presente, a face não será texturizada.</span><span class="sxs-lookup"><span data-stu-id="62e7f-120">If this object is not present, the face is untextured.</span></span>

## <a name="see-also"></a><span data-ttu-id="62e7f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="62e7f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62e7f-122">Modelos</span><span class="sxs-lookup"><span data-stu-id="62e7f-122">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



