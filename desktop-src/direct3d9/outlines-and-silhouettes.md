---
description: Você pode usar o buffer de estêncil para efeitos mais abstratos, como contornos e silhuetas.
ms.assetid: 8b9cd2b3-c1bf-4ac9-aae5-7fc0c9e049ff
title: Contornos e silhuetas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46a282b650b96cdbb36dc252e1f31cb81d91f0bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645658"
---
# <a name="outlines-and-silhouettes-direct3d-9"></a><span data-ttu-id="fa8ea-103">Contornos e silhuetas (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="fa8ea-103">Outlines and Silhouettes (Direct3D 9)</span></span>

<span data-ttu-id="fa8ea-104">Você pode usar o buffer de estêncil para efeitos mais abstratos, como contornos e silhuetas.</span><span class="sxs-lookup"><span data-stu-id="fa8ea-104">You can use the stencil buffer for more abstract effects, such as outlining and silhouetting.</span></span>

<span data-ttu-id="fa8ea-105">Se seu aplicativo aplicar uma máscara de estêncil à imagem de um objeto primitivo com o mesmo formato, mas um pouco menor, a imagem resultante terá apenas o contorno do objeto primitivo.</span><span class="sxs-lookup"><span data-stu-id="fa8ea-105">If your application applies a stencil mask to the image of a primitive that is the same shape but slightly smaller, the resulting image contains only the primitive's outline.</span></span> <span data-ttu-id="fa8ea-106">O app pode preencher a área com máscara de estêncil da imagem com uma cor sólida, dando à primitiva uma aparência em alto-relevo.</span><span class="sxs-lookup"><span data-stu-id="fa8ea-106">The application can then fill the stencil-masked area of the image with a solid color, giving the primitive an embossed look.</span></span>

<span data-ttu-id="fa8ea-107">Se a máscara de estêncial tiver o mesmo tamanho e formato da primitiva que está sendo renderizado, a imagem resultante terá um buraco onde o primitivo deveria estar.</span><span class="sxs-lookup"><span data-stu-id="fa8ea-107">If the stencil mask is the same size and shape as the primitive you are rendering, the resulting image contains a hole where the primitive should be.</span></span> <span data-ttu-id="fa8ea-108">Seu app poderá preencher o buraco com cor preta para produzir uma silhueta da primitiva.</span><span class="sxs-lookup"><span data-stu-id="fa8ea-108">Your application can then fill the hole with black to produce a silhouette of the primitive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa8ea-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa8ea-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa8ea-110">Técnicas de buffer de estêncil</span><span class="sxs-lookup"><span data-stu-id="fa8ea-110">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



