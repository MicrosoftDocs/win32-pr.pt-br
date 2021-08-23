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
ms.openlocfilehash: 6dbe948dc3dbe84c9c2e89e02a43b45cf22d34af0198e422a883afd8f3384606
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553906"
---
# <a name="manipulating-images-for-use-in-texturing"></a>Manipulando imagens para uso no texturing

A biblioteca de utilitário OpenGL (GLU) fornece dimensionamento de imagem e funções automáticas de mipmapping para simplificar a especificação de imagens de textura. A função [**gluScaleImage**](gluscaleimage.md) dimensiona uma imagem especificada para um tamanho de textura aceito; Você pode passar a imagem resultante para OpenGL como uma textura. As funções automáticas de mipmapping, [**gluBuild1DMipmaps**](glubuild1dmipmaps.md) e [**gluBuild2DMipmaps**](glubuild2dmipmaps.md), criam imagens de textura de mipmapped de uma imagem especificada e as transmitem para [**glTexImage1D**](glteximage1d.md) e [**glTexImage2D**](glteximage2d.md), respectivamente.

 

 




