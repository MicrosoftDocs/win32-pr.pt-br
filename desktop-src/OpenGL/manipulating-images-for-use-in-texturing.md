---
title: Manipulando imagens para uso no texturing
description: A biblioteca de utilitário OpenGL (GLU) fornece dimensionamento de imagem e funções automáticas de mipmapping para simplificar a especificação de imagens de textura.
ms.assetid: 20edf665-1fed-4761-b8b1-beee02c78b0d
keywords:
- Utilitário OpenGL (GLU), dimensionamento de imagem
- GLU (utilitário OpenGL), dimensionamento de imagem
- Utilitário OpenGL (GLU), mipmapping automático
- GLU (utilitário OpenGL), mipmapping automático
- Utilitário OpenGL (GLU), imagens de textura
- GLU (utilitário OpenGL), imagens de textura
- Biblioteca GLU, imagens de textura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16726493bbcb6e0116e4c158e470029f34f5b652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292066"
---
# <a name="manipulating-images-for-use-in-texturing"></a><span data-ttu-id="38f1c-110">Manipulando imagens para uso no texturing</span><span class="sxs-lookup"><span data-stu-id="38f1c-110">Manipulating Images for Use in Texturing</span></span>

<span data-ttu-id="38f1c-111">A biblioteca de utilitário OpenGL (GLU) fornece dimensionamento de imagem e funções automáticas de mipmapping para simplificar a especificação de imagens de textura.</span><span class="sxs-lookup"><span data-stu-id="38f1c-111">The OpenGL Utility library (GLU) provides image scaling and automatic mipmapping functions to simplify the specification of texture images.</span></span> <span data-ttu-id="38f1c-112">A função [**gluScaleImage**](gluscaleimage.md) dimensiona uma imagem especificada para um tamanho de textura aceito; Você pode passar a imagem resultante para OpenGL como uma textura.</span><span class="sxs-lookup"><span data-stu-id="38f1c-112">The [**gluScaleImage**](gluscaleimage.md) function scales a specified image to an accepted texture size; you can pass the resulting image to OpenGL as a texture.</span></span> <span data-ttu-id="38f1c-113">As funções automáticas de mipmapping, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) e [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), criam imagens de textura de mipmapped de uma imagem especificada e as transmitem para [**glTexImage1D**](glteximage1d.md) e [**glTexImage2D**](glteximage2d.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="38f1c-113">The automatic mipmapping functions, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) and [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), create mipmapped texture images from a specified image and pass them to [**glTexImage1D**](glteximage1d.md) and [**glTexImage2D**](glteximage2d.md), respectively.</span></span>

 

 




